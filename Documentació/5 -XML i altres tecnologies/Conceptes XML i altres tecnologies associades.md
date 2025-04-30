# Apunts sobre XML i tecnologies relacionades

## Índex

- [Apunts sobre XML i tecnologies relacionades](#apunts-sobre-xml-i-tecnologies-relacionades)
  - [Índex](#índex)
  - [XML (eXtensible Markup Language)](#xml-extensible-markup-language)
    - [Algunes regles per a un document XML ben format](#algunes-regles-per-a-un-document-xml-ben-format)
    - [Com comprovar si un XML està ben format](#com-comprovar-si-un-xml-està-ben-format)
    - [Exemple document XML](#exemple-document-xml)
    - [Exemples de vocabularis XML](#exemples-de-vocabularis-xml)
  - [XPath (XML Path Language)](#xpath-xml-path-language)
  - [XQuery](#xquery)
    - [Estructura d'una expressió XQuery](#estructura-duna-expressió-xquery)
  - [XSD (XML Schema Definition)](#xsd-xml-schema-definition)
    - [Diferència entre ben format i vàlid](#diferència-entre-ben-format-i-vàlid)
    - [Com vincular un document XML amb un fitxer XSD](#com-vincular-un-document-xml-amb-un-fitxer-xsd)
  - [XSLT (Extensible Stylesheet Language Transformations)](#xslt-extensible-stylesheet-language-transformations)
    - [Procés per transformar XML en HTML](#procés-per-transformar-xml-en-html)
    - [Exemple de transformació XML a HTML](#exemple-de-transformació-xml-a-html)
  - [BaseX](#basex)
  - [Altova XMLSpy](#altova-xmlspy)
  - [Conclusió](#conclusió)

---

## XML (eXtensible Markup Language)

XML és un **metalenguatge**, és a dir, un llenguatge per definir altres llenguatges de marques. Això vol dir que no només s'utilitza per emmagatzemar dades, sinó també per crear **vocabularis específics** segons el context o aplicació. És auto-descriptiu i molt utilitzat en l'intercanvi de dades entre aplicacions i sistemes.

### Algunes regles per a un document XML ben format

1. **Element arrel únic**:
   ```xml
   <llibres>
     <llibre>...</llibre>
   </llibres>
   ```
2. **Etiquetes tancades correctament**:
   ```xml
   <titol>1984</titol> <!-- Correcte -->
   <titol>1984 <!-- Incorrecte -->
   ```
3. **Etiquetes ben imbricades**:
   ```xml
   <autor><nom>Orwell</nom></autor> <!-- Correcte -->
   <autor><nom>Orwell</autor></nom> <!-- Incorrecte -->
   ```
4. **Atributs entre cometes**:
   ```xml
   <llibre any="1949"> <!-- Correcte -->
   <llibre any=1949> <!-- Incorrecte -->
   ```

### Com comprovar si un XML està ben format

- Amb editors com Visual Studio Code o Altova XMLSpy.
- Amb eines online com [xmlvalidation.com](https://www.xmlvalidation.com/).

### Exemple document XML

Aquest exemple mostra una estructura XML ben formada i pensada per practicar diferents tipus de consultes. És útil per aplicar coneixements de sintaxi bàsica, XPath, XQuery i validació amb XSD. A continuació, es pot veure una mostra de dades amb diversos llibres, cadascun amb el seu títol, autor i any de publicació. 
```xml
<llibres>
  <llibre>
    <titol>1984</titol>
    <autor>George Orwell</autor>
    <any>1949</any>
  </llibre>
  <llibre>
    <titol>El joc d'Ender</titol>
    <autor>Orson Scott Card</autor>
    <any>1985</any>
  </llibre>
  <llibre>
    <titol>El nom del vent</titol>
    <autor>Patrick Rothfuss</autor>
    <any>2007</any>
  </llibre>
</llibres>
```


### Exemples de vocabularis XML

Aquest tipus de vocabularis es defineixen utilitzant XML per a diferents propòsits segons el domini o aplicació:

- **SVG (Scalable Vector Graphics)**: per a gràfics vectorials 2D.
- **XSD (XML Schema Definition)**: per validar estructures XML.
- **DOCX**: format de documents de Word, basat en arxius XML empaquetats.

## XPath (XML Path Language)

XPath és un llenguatge que permet navegar i localitzar parts específiques dins d’un document XML mitjançant expressions de camí. És molt utilitzat per accedir a elements, atributs i contingut de manera eficient, ja sigui dins d’aplicacions o com a part de processos d’anàlisi de dades XML. XPath pot treballar amb estructures jeràrquiques i fer consultes precises sobre la posició, el valor o les relacions dels nodes.

- **Funció**: Accedir a nodes dins d’un document XML.
- **Sintaxi**:
  - `/`: arrel
  - `//`: qualsevol lloc del document
  - `@`: atribut

**Exemples de consultes (amb resultats sobre l'XML anterior):**

- `/llibres/llibre/titol` → Retorna:
  - 1984
  - El joc d'Ender
  - El nom del vent

- `//autor` → Retorna:
  - George Orwell
  - Orson Scott Card
  - Patrick Rothfuss

- `//llibre[any>2000]/titol` → Retorna:
  - El nom del vent

## XQuery

XQuery és un llenguatge de consulta funcional creat específicament per interrogar i transformar dades XML. Està estretament relacionat amb XPath, ja que utilitza la seva sintaxi per accedir als nodes, però ofereix una potència molt més gran, incloent estructures de control, condicions, assignacions de variables, i capacitat per generar nous documents XML com a resultat. S'utilitza sovint en sistemes de gestió de dades, aplicacions web, i eines de transformació massiva d'informació estructurada.

- **Funció**: Realitzar consultes XML més avançades que XPath.

### Estructura d'una expressió XQuery

Una consulta XQuery sol estar composta per diferents expressions clau que defineixen com accedir i manipular dades XML:

- `for $x in ...` → Itera sobre una col·lecció de nodes. Cada element es guarda a la variable `$x`.
- `let $x := ...` → Assigna una expressió a una variable sense fer iteració.
- `where ...` → Filtra els resultats obtinguts segons una condició (semblant a una clàusula WHERE en SQL).
- `order by ...` → Ordena els resultats.
- `return ...` → Indica què ha de retornar per a cada iteració o coincidència.
- `if ... then ... else ...` → Condicional per controlar l'estructura dels resultats.



**Exemple:**

- **Funció**: Realitzar consultes XML més avançades que XPath.

**Exemple:**
```xquery
for $x in doc("llibres.xml")//llibre
where $x/any > 2000
return $x/titol
```

**Resultat esperat:**
```xml
<titol>El nom del vent</titol>
```

## XSD (XML Schema Definition)

XSD (XML Schema Definition) és un llenguatge basat en XML que permet definir l'estructura, el contingut i les restriccions d'un document XML. Amb un fitxer XSD es pot especificar quins elements són obligatoris, quins atributs poden aparèixer, quin tipus de dades contenen (com string, integer, date...), així com l'ordre i la jerarquia dels elements. 

A diferència de DTD (Document Type Definition), XSD admet tipus de dades més avançats i està escrit amb la mateixa sintaxi XML, fet que facilita el seu ús i validació. Utilitzar un esquema XSD permet garantir que un document XML no només sigui sintàcticament correcte, sinó que també compleixi unes regles específiques de contingut i estructura.


### Diferència entre ben format i vàlid

- **Ben format**: compleix la sintaxi XML.
- **Vàlid**: a més, compleix amb un esquema XSD.

**Exemple ben format però no vàlid:**
```xml
<persona>
  <nom>Maria</nom>
  <edat>trenta</edat>
</persona>
```

**Esquema XSD:**
```xml
<xs:element name="persona">
  <xs:complexType>
    <xs:sequence>
      <xs:element name="nom" type="xs:string"/>
      <xs:element name="edat" type="xs:integer"/>
    </xs:sequence>
  </xs:complexType>
</xs:element>
```

### Com vincular un document XML amb un fitxer XSD

```xml
<persona xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:noNamespaceSchemaLocation="esquema.xsd">
  <nom>Maria</nom>
  <edat>30</edat>
</persona>
```

## XSLT (Extensible Stylesheet Language Transformations)

XSLT és un llenguatge dissenyat per transformar documents XML en altres formats com HTML, text pla o nous documents XML. Funciona mitjançant plantilles que indiquen com processar i mostrar diferents parts del document d'origen.

Aquest llenguatge és molt útil quan es vol mostrar contingut XML de forma més visual o quan es vol migrar informació cap a altres estructures de dades. La transformació es realitza a través de regles (plantilles) que es defineixen dins d'un document XSL, el qual es pot aplicar al XML mitjançant processadors XSLT.

### Procés per transformar XML en HTML

Per transformar un document XML en una pàgina HTML visualitzable, cal seguir aquests passos:

1. **Crear el document XML**: defineix la informació estructurada.
2. **Crear l'estil XSLT**: defineix les plantilles de transformació.
3. **Enllaçar l’XML amb l’XSLT** mitjançant una instrucció `<?xml-stylesheet?>`.
4. **Executar la transformació** amb un navegador compatible o una eina com Altova XMLSpy, BaseX o XSLTProcessor en JavaScript.

### Exemple de transformació XML a HTML

**Document XML:**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" href="estil.xsl"?>
<llibres>
  <llibre>
    <titol>1984</titol>
    <autor>George Orwell</autor>
  </llibre>
  <llibre>
    <titol>El nombre del viento</titol>
    <autor>Patrick Rothfuss</autor>
  </llibre>
</llibres>
```

**Estil XSLT (estil.xsl):**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet version="1.0"
    xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
  <xsl:template match="/">
    <html>
      <body>
        <h1>Llibres</h1>
        <xsl:for-each select="llibres/llibre">
          <div>
            <h2><xsl:value-of select="titol"/></h2>
            <p><xsl:value-of select="autor"/></p>
          </div>
        </xsl:for-each>
      </body>
    </html>
  </xsl:template>
</xsl:stylesheet>
```

**Resultat HTML renderitzat:**
```html
<html>
  <body>
    <h1>Llibres</h1>
    <div>
      <h2>1984</h2>
      <p>George Orwell</p>
    </div>
    <div>
      <h2>El nombre del viento</h2>
      <p>Patrick Rothfuss</p>
    </div>
  </body>
</html>
```

Aquest procés permet transformar dades XML en una presentació HTML personalitzada mitjançant plantilles definides a l’arxiu XSL.



## BaseX

BaseX és un sistema gestor de bases de dades nadiu per a XML, lleuger i molt eficient. Està dissenyat per emmagatzemar, gestionar i consultar grans quantitats de dades XML de forma òptima.

- **Descripció**: Gestor de base de dades per a XML, de codi obert i multiplataforma.
- **Característiques**:
  - Suporta XPath i XQuery
  - Optimitzat per a grans volums de dades
  - Interfície gràfica i línia de comandes

## Altova XMLSpy

Altova XMLSpy és una eina de desenvolupament (IDE) especialitzada per treballar amb XML i tecnologies relacionades. És molt utilitzada tant en entorns educatius com professionals per la seva potència i versatilitat.

- **Descripció**: IDE per treballar amb XML.
- **Funcions**:
  - Edició visual i textual
  - Validació contra XSD
  - Disseny de plantilles XSLT
  - Execució de consultes XPath/XQuery
  - Visualització d’esquemes

---

## Conclusió

Aquest recull d’apunts ofereix una visió global, clara i ordenada de les principals tecnologies relacionades amb XML. Serveix com a referència ràpida per a l’estudi, pràctica o consulta tècnica.

Dominar XML i les seves eines com XPath, XQuery, XSLT o XSD és essencial per treballar amb dades estructurades en entorns web, empresarials i tecnològics. Practicar amb eines com BaseX o Altova XMLSpy pot ajudar a consolidar els coneixements i aprofundir en la seva aplicació pràctica.

Amb aquests coneixements ben establerts, seràs capaç de construir, validar, consultar i transformar documents XML de manera eficient i robusta.

