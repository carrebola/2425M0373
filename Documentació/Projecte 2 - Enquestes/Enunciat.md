# Projecte: Gestió d'Enquestes amb XML

## Visió del Producte
Crear una aplicació senzilla per gestionar enquestes realitzades al carrer, aprofitant tecnologies XML i eines associades. Aquest projecte ajudarà els estudiants a adquirir competències pràctiques en:

- Creació i validació estructurada de documents XML.
- Execució de consultes mitjançant XPath i XQuery.
- Transformació d'XML a HTML utilitzant XSLT.
- Automatització de processos amb scripts Node.js.

## Tecnologies del Projecte

### Tecnologies Fonamentals
- **XML (eXtensible Markup Language):** Llenguatge per emmagatzemar i transportar dades de manera estructurada i fàcilment llegible.
- **XSD (XML Schema Definition):** Llenguatge per definir i validar l'estructura i contingut d'un document XML.
- **XPath:** Llenguatge que permet seleccionar elements específics dins d'un document XML.
- **XQuery:** Llenguatge per fer consultes avançades sobre documents XML.
- **XSLT (eXtensible Stylesheet Language Transformations):** Llenguatge per transformar documents XML en altres formats, com HTML.
- **Node.js:** Plataforma per automatitzar tasques mitjançant scripts JavaScript.

### Aplicacions i Eines
- **Altova XMLSpy:** Eina visual per validar XML amb esquemes XSD i realitzar transformacions amb XSLT.
- **BaseX:** Base de dades XML per executar consultes XPath i XQuery.

## Backlog del Producte

### Sprint 1: Estructura i Validació XML

**Història d'Usuari 1: Creació de l'XML**
- Crear un document XML amb múltiples enquestes.
- Definir clarament elements essencials: data, lloc (carrer, ciutat, província, país), preguntes i respostes.

**Història d'Usuari 2: Disseny i Validació de l'Esquema XSD**
- Crear un esquema XSD amb restriccions específiques per assegurar la qualitat de les dades.
- Validar visualment el document XML amb Altova XMLSpy.

### Sprint 2: Transformació XML a HTML

**Història d'Usuari 3: Transformació XML a HTML**
- Crear un full d'estils XSLT per transformar eficaçment l'XML en una taula HTML clara.
- Realitzar la transformació amb Altova XMLSpy i generar el fitxer HTML.

### Sprint 3: Base de Dades i Consultes XML

**Història d'Usuari 4: Creació de Base de Dades XML amb BaseX**
- Crear i configurar una base de dades XML nativa amb BaseX.

**Història d'Usuari 5: Consultes XPath i XQuery**
- Desenvolupar consultes específiques utilitzant BaseX:
  - Filtrar enquestes per una ciutat concreta.
  - Obtenir totes les respostes d'una enquesta específica.

### Sprint 4: Automatització amb Node.js

**Història d'Usuari 6: Configuració d'entorn Node.js**
- Preparar l'entorn de desenvolupament Node.js per executar scripts d'automatització.

**Història d'Usuari 7: Automatització del Procés**
- Crear un script en Node.js per executar automàticament les consultes definides en BaseX.
- Mostrar clarament a la consola els resultats obtinguts.

## Lliurables Finals del Projecte
Cada estudiant lliurarà:
- Document XML validat.
- Esquema XSD complet.
- Fitxer XSLT operatiu per la transformació XML-HTML.
- Base de dades XML creada amb BaseX.
- Script Node.js funcional per l'automatització del procés.
- Informe tutorial amb tot el procés.

