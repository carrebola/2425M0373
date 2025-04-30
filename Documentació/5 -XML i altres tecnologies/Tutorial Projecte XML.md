# Tutorial Projecte XML per a Gestió d'Inventari de Productes

Aquest tutorial detalla pas a pas com crear un projecte per gestionar l'inventari d'una botiga, permetent-te aprendre i aplicar tècniques XML, XSD, XQuery/XPath, XSLT i Node.js.

## Requisits previs:
- Instal·lar BaseX: https://basex.org/
- Instal·lar Node.js: https://nodejs.org/
- Instal·lar Altova XMLSpy: https://www.altova.com/xmlspy

## Pas 1: Crear document XML
Tasques:
- Crear un fitxer nou anomenat `inventari.xml`.
- Definir clarament l'estructura de dades que contingui:
  - **inventari**
    - **producte** (amb atribut obligatori `id` únic per cada producte)
      - **nom**: Text descriptiu clar del producte.
      - **categoria**: Categoria a la qual pertany el producte.
      - **preu**: Preu del producte (decimal positiu).
      - **quantitat**: Quantitat en estoc (enter positiu).

Exemple XML:

```xml
<inventari>
  <producte id="P001">
    <nom>Ratolí sense fil</nom>
    <categoria>Electrònica</categoria>
    <preu>25.99</preu>
    <quantitat>100</quantitat>
  </producte>
  <producte id="P002">
    <nom>Teclat mecànic</nom>
    <categoria>Electrònica</categoria>
    <preu>75.50</preu>
    <quantitat>50</quantitat>
  </producte>
</inventari>
```
![image](https://github.com/user-attachments/assets/fa2e7d73-5500-486d-9c96-001eb6caa665)

## Pas 2: Crear esquema XSD amb regles de validació
Tasques:
- Crear un fitxer `inventari.xsd` per validar la integritat de l'XML.
- Definir restriccions específiques:
  - El camp `preu` ha de ser obligatòriament un número decimal positiu superior a 0.
  - El camp `quantitat` ha de ser obligatòriament un enter positiu major que 0.
  - Tots els camps són obligatoris i no poden estar buits.

Exemple XSD:

```xml
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="inventari">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="producte" maxOccurs="unbounded">
          <xs:complexType>
            <xs:sequence>
              <xs:element name="nom" type="xs:string"/>
              <xs:element name="categoria" type="xs:string"/>
              <xs:element name="preu">
                <xs:simpleType>
                  <xs:restriction base="xs:decimal">
                    <xs:minInclusive value="0.01"/>
                  </xs:restriction>
                </xs:simpleType>
              </xs:element>
              <xs:element name="quantitat">
                <xs:simpleType>
                  <xs:restriction base="xs:integer">
                    <xs:minInclusive value="1"/>
                  </xs:restriction>
                </xs:simpleType>
              </xs:element>
            </xs:sequence>
            <xs:attribute name="id" type="xs:string" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
```
![image](https://github.com/user-attachments/assets/9e9824dc-a533-49f5-a3fa-640850e2180e)
![image](https://github.com/user-attachments/assets/d6828fab-2b97-45bb-bb17-d11c39a3faa4)

## Pas 3: Validació XML amb Altova XMLSpy
Tasques:
- Obrir Altova XMLSpy.
- Carregar el fitxer XML (`inventari.xml`) i l'esquema XSD (`inventari.xsd`).
- Executar el procés de validació per confirmar que el document compleix totes les regles definides.
![image](https://github.com/user-attachments/assets/24f319e7-0f57-494a-9188-45c164c6cd33)

## Pas 4: Consultes XPath i XQuery amb BaseX
Tasques:
- Obrir BaseX.
- Desa el teu arxiu xml a la carpeta `basex` de de la aplicació baseX
- Executar consultes per obtenir productes específics segons criteris com la categoria.

Exemple XQuery:

```xquery
for $p in doc("inventari.xml")//producte
where $p/categoria = "Electrònica"
return $p/nom
```
![image](https://github.com/user-attachments/assets/f016184d-d4a8-440d-a565-b4e54e656be1)

## Pas 5: Transformació XML a HTML amb XSLT
Tasques:
- Crear mitjançant XMLSpy un fitxer `plantilla.xsl`.
- Dissenyar una plantilla XSLT que converteixi clarament les dades XML a format HTML.

Exemple arxiu plantilla.xsl:

```xml
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
  <xsl:output method="html"/>
  <xsl:template match="/inventari">
    <html>
      <body>
        <table border="1">
          <tr><th>ID</th><th>Nom</th><th>Categoria</th><th>Preu</th><th>Quantitat</th></tr>
          <xsl:for-each select="producte">
            <tr>
              <td><xsl:value-of select="@id"/></td>
              <td><xsl:value-of select="nom"/></td>
              <td><xsl:value-of select="categoria"/></td>
              <td><xsl:value-of select="preu"/></td>
              <td><xsl:value-of select="quantitat"/></td>
            </tr>
          </xsl:for-each>
        </table>
      </body>
    </html>
  </xsl:template>
</xsl:stylesheet>
```
![image](https://github.com/user-attachments/assets/01dc9cde-2ac0-4aa0-be84-373707c3c9a7)

Utilitzar Altova XMLSpy per executar aquesta transformació i generar el fitxer HTML.
![image](https://github.com/user-attachments/assets/efea9865-66ad-4ab5-a5f4-be6995903530)
![image](https://github.com/user-attachments/assets/64b962ff-f630-4ca5-8769-d18662aef5ca)

## Pas 6: Automatització amb Node.js
Tasques:
- Crear un fitxer `automatitzacio.js`.
- Escriure un script que automatitzi l'execució de consultes en BaseX i mostri resultats per consola.

Exemple script Node.js:

```javascript
const { exec } = require('child_process');

exec('basex -q "for $p in doc(\'inventari.xml\')//producte return $p"', (err, stdout, stderr) => {
  if (err) {
    console.error(`Error: ${err}`);
    return;
  }
  console.log(`Resultat:\n${stdout}`);
});
```

Executar:

```bash
node automatitzacio.js
```


