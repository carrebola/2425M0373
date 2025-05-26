# Projecte: Gestió d'Enquestes amb XML

*Actualitzat: 19‑maig‑2025*

---

## Visió del Producte

Crear una aplicació senzilla per gestionar enquestes realitzades al carrer, aprofitant tecnologies XML i eines associades. Aquest projecte ajudarà els estudiants a adquirir competències pràctiques en:

* Creació i validació estructurada de documents XML.
* Execució de consultes mitjançant XPath i XQuery.
* Transformació d'XML a HTML utilitzant XSLT.
* Automatització de processos amb scripts Node.js.

---

## Tecnologies del Projecte

### Tecnologies Fonamentals

* **XML (eXtensible Markup Language):** Llenguatge per emmagatzemar i transportar dades de manera estructurada i fàcilment llegible.
* **XSD (XML Schema Definition):** Llenguatge per definir i validar l'estructura i contingut d'un document XML.
* **XPath:** Llenguatge que permet seleccionar elements específics dins d'un document XML.
* **XQuery:** Llenguatge per fer consultes avançades sobre documents XML.
* **XSLT (eXtensible Stylesheet Language Transformations):** Llenguatge per transformar documents XML en altres formats, com HTML.
* **Node.js:** Plataforma per automatitzar tasques mitjançant scripts JavaScript.

### Aplicacions i Eines

* **Altova XMLSpy:** Eina visual per validar XML amb esquemes XSD i realitzar transformacions amb XSLT.
* **BaseX:** Base de dades XML per executar consultes XPath i XQuery.

---

## Backlog del Producte

### Sprint 1: Estructura de dades XML i validació amb XSD

**Història d'Usuari 1: Creació de l'XML**

* Crear un document XML amb múltiples enquestes.
* Definir clarament elements essencials: data, lloc (carrer, ciutat, província, país), preguntes i respostes.

**Història d'Usuari 2: Disseny i Validació de l'Esquema XSD**

* Crear un esquema XSD amb restriccions específiques per assegurar la qualitat de les dades.
* Validar visualment el document XML amb Altova XMLSpy.

### Sprint 2: Creació d’una base de dades nativa XML i consultes

**Història d'Usuari 3: Creació de Base de Dades XML amb BaseX**

* Crear i configurar una base de dades XML nativa amb BaseX.

**Història d'Usuari 4: Consultes XPath i XQuery**

* Desenvolupar consultes específiques utilitzant BaseX:

  * Filtrar enquestes per una ciutat concreta.
  * Obtenir totes les respostes d'una enquesta específica.

### Sprint 3: Transformació XML a HTML per a la web

**Història d'Usuari 5: Transformació XML a HTML**

* Crear un full d'estils XSLT per transformar eficientment l'XML en una taula HTML clara.
* Realitzar la transformació amb Altova XMLSpy i generar el fitxer HTML.

---

## Estructura lògica de la Base de Dades XML

```
<enquestes>                     (1..1)
 └─ <enquesta id="ID" data="YYYY-MM-DD">  (1..*)
     ├─ <lloc>                  (1)
     │   ├─ <carrer>...</carrer>        (1..1)
     │   ├─ <ciutat>...</ciutat>        (1..1)
     │   ├─ <provincia>...</provincia>  (1..1)
     │   └─ <pais>ES</pais>             (1..1)
     ├─ <preguntes>             (1)
     │   └─ <pregunta id="ID" tipus="likert|boolean|oberta">Text...</pregunta> (1..*)
     └─ <respostes>             (1)
         └─ <resposta encestat="ID">   (1..*)
             ├─ <dades>         (0..1)
             │   ├─ <edat>...</edat>
             │   ├─ <genere>...</genere>
             │   └─ <ocupacio>...</ocupacio>
             └─ <valor pregunta="IDREF">Contingut</valor> (1..*)
```

---

## Regles de Validació (resum simplificat)

* **Estructura general**: l’arrel `<enquestes>` ha de contenir una o més `<enquesta>`.
* **Identificadors únics**: `@id` de `<enquesta>`, `@id` de `<pregunta>` i `@encestat` de `<resposta>` han de ser únics dins del seu àmbit.
* **Dates**: l’atribut `data` de `<enquesta>` ha de complir el format ISO `YYYY-MM-DD`.
* **Localització**:

  * `<carrer>`: mínim 1 caràcter, màxim 100.
  * `<pais>`: exactament dues lletres majúscules (codi ISO‑3166‑1 alfa‑2).
* **Preguntes**:

  * Cada `<enquesta>` requereix almenys una `<pregunta>`.
  * Atribut `tipus` limitat a `likert`, `boolean` o `oberta`.
* **Respostes**:

  * Cada `<resposta>` pot incloure opcionalment `<dades>` amb:

    * `<edat>` entre 18 i 99.
    * `<genere>`: `home`, `dona`, `no_binari` o `ns_nc`.
    * `<ocupacio>`: màxim 100 caràcters.
  * Requereix almenys un `<valor>`.
* **Valors de preguntes**:

  * L’atribut `pregunta` de `<valor>` ha de referir-se a una `<pregunta>` existent.
  * Contingut serà text.

---

## Lliurables Finals del Projecte

Cada estudiant lliurarà:

1. **Document XML validat** amb un mínim de 3 persones enquestades i 10 respostes totals.
2. **Esquema XSD complet** que implementi les regles anteriors.
3. **Fitxer XSLT operatiu** per a la transformació XML‑HTML.
4. **Base de dades XML** creada i poblada a BaseX.
5. **Informe tutorial** que descrigui el procés, incloent consultes XPath/XQuery i captures de les validacions.
