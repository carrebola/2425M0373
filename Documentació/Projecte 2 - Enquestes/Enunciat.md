# Projecte: Gestió d'Enquestes amb XML 

## Visió del Producte
Crear una aplicació senzilla per gestionar enquestes realitzades al carrer, aprofitant tecnologies XML i eines associades. El producte permetrà als estudiants adquirir competències pràctiques en:

- Creació i validació estructurada de documents XML.
- Execució precisa de consultes mitjançant XPath i XQuery.
- Transformació eficient d'XML a HTML utilitzant XSLT.
- Automatització efectiva de processos fent servir scripts en Node.js.

## Tecnologies de l'Sprint

### Tecnologies fonamentals
- **XML (eXtensible Markup Language):** Llenguatge de marcatge dissenyat per emmagatzemar i transportar dades de manera estructurada i llegible tant per humans com per màquines. En aquest projecte, XML s'utilitza per representar les dades recollides en enquestes.
- **XSD (XML Schema Definition):** Llenguatge utilitzat per definir restriccions i validar l'estructura de documents XML, assegurant que les dades emmagatzemades segueixin un format específic.
- **XPath:** Llenguatge que permet seleccionar elements específics dins d'un document XML, facilitant cerques i filtratges precisos.
- **XQuery:** Llenguatge dissenyat per fer consultes complexes sobre documents XML, permetent l'extracció eficient de dades.
- **XSLT (eXtensible Stylesheet Language Transformations):** Llenguatge emprat per transformar documents XML en altres formats com HTML, fent més accessibles les dades per als usuaris finals.
- **Node.js:** Entorn d'execució per JavaScript al servidor que permet automatitzar processos mitjançant scripts, oferint agilitat i eficiència en el flux de treball.

### Aplicacions i Eines específiques
- **Altova XMLSpy:** Eina visual avançada que permet validar documents XML davant d'esquemes XSD i realitzar transformacions XML mitjançant XSLT.
- **BaseX:** Base de dades XML i processador de consultes que facilita l'execució ràpida de consultes XPath i XQuery sobre documents XML.

## Backlog del Producte

### Història d'Usuari 1: Creació de l'XML
- Crear un document XML detallat amb múltiples enquestes.
- Definir clarament elements essencials com data, lloc (carrer, ciutat, província, país), preguntes i respostes.

### Història d'Usuari 2: Disseny de l'Esquema XSD
- Elaborar un esquema XSD amb restriccions específiques per garantir la qualitat de les dades.
- Validar visualment l'XML usant l'eina Altova XMLSpy.

### Història d'Usuari 3: Consultes amb XPath i XQuery
- Desenvolupar consultes específiques utilitzant BaseX:
  - Filtrar enquestes per una ciutat determinada.
  - Obtenir totes les respostes donades en una enquesta concreta.

### Història d'Usuari 4: Transformació XML a HTML
- Dissenyar un full d'estils XSLT per convertir eficaçment l'XML en una taula HTML visualment clara.
- Executar la transformació visual utilitzant Altova XMLSpy i generar un fitxer HTML.

### Història d'Usuari 5: Automatització amb Node.js
- Crear un script d'automatització en Node.js per:
  - Executar automàticament consultes definides amb BaseX.
  - Mostrar clarament en consola els resultats del procés.

## Lliurables de l'Sprint
Cada estudiant lliurarà:
- Document XML final validat.
- Esquema XSD complet i funcional.
- Fitxer XSLT operatiu per a transformació.
- Script Node.js que automatitzi consultes i reporti resultats.


