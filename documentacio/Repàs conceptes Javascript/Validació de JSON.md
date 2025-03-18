

# Validació de JSON

1. [Introducció a JSON Schema](#1-introducció-a-json-schema)
2. [Coneixent JSON Schema Validator](#2-coneixent-json-schema-validator)
3. [Creació de l'Esquema i Dades d'Exemple](#3-creació-de-lesquema-i-dades-dexemple)  
   3.1. [Esquema JSON](#31-esquema-json)  
   3.2. [Dades JSON d'Exemple](#32-dades-json-dexemple)
4. [Ús de JSON Schema Validator](#4-ús-de-json-schema-validator)
5. [Resum de les Opcions en JSON Schema](#5-resum-de-les-opcions-en-json-schema)
6. [Bones Pràctiques i Propers Passos](#6-bones-pràctiques-i-propers-passos)

---

## 1. Introducció a JSON Schema

**JSON Schema** és una especificació que et permet definir l'estructura, els tipus i les restriccions de dades en un document JSON. Amb un esquema pots:

- **Verificar l'estructura:** Assegurar-te que les dades tinguin la forma correcta (per exemple, un objecte o un array).
- **Controlar tipus i formats:** Definir que una propietat sigui una cadena, un nombre, booleà, etc., i establir formats com "email" o "date".
- **Aplicar restriccions:** Limitar valors mitjançant `minimum`, `maximum`, `minLength`, `maxLength` o definir patrons amb expressions regulars.
- **Gestionar validacions compostes:** Utilitzar combinacions d'esquemes amb paraules clau com `allOf`, `anyOf`, `oneOf` i `not`.

---

## 2. Coneixent JSON Schema Validator

Els **validadors en línia** et permeten provar i validar els teus esquemes i dades JSON de manera ràpida sense necessitat de configurar un entorn local. Una eina popular és [JSON Schema Lint](https://jsonschemalint.com/), que ofereix:

- **Interfície intuïtiva:** Dos panells on pots enganxar el teu JSON Schema i les teves dades JSON.
- **Retroalimentació immediata:** Visualització instantània d'errors o confirmació de validació amb èxit.
- **Facilitat per a l'experimentació:** Ideal per aprendre, ajustar i compartir exemples amb altres desenvolupadors.

---

## 3. Creació de l'Esquema i Dades d'Exemple

En aquest tutorial validarem un array d'objectes que representen usuaris. Cada usuari ha de tenir:

- **`id`:** Número enter.
- **`nom`:** Cadena de text.
- **`email`:** Cadena en format de correu electrònic.

### 3.1. Esquema JSON

Crea el següent esquema (per exemple, en un fitxer `schema.json` o directament en el panell del validador):

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Llista d'Usuaris",
  "type": "array",
  "items": {
    "type": "object",
    "properties": {
      "id": { "type": "integer" },
      "nom": { "type": "string" },
      "email": { "type": "string", "format": "email" }
    },
    "required": ["id", "nom", "email"]
  }
}
```

**Detalls de l'esquema:**

- **`$schema`:** Indica la versió de l'estàndard que s'utilitza.
- **`title`:** Un títol descriptiu per a l'esquema.
- **`type`:** Defineix el tipus de dada arrel; en aquest cas, un array.
- **`items`:** Descriu l'estructura de cada element dins de l'array.
- **`properties`:** Defineix les propietats de cada objecte i els seus tipus.
- **`required`:** Llista les propietats obligatoris per a cada objecte.

### 3.2. Dades JSON d'Exemple

Prepara el següent JSON per validar (per exemple, en un fitxer `data.json` o en el panell corresponent del validador):

```json
[
  {
    "id": 1,
    "nom": "Joan Pérez",
    "email": "joanperez@example.com"
  },
  {
    "id": 2,
    "nom": "Marta López",
    "email": "marta@example.com"
  }
]
```

Aquest exemple consisteix en un array de dos objectes, cadascun complint amb les regles definides en l'esquema.

---

## 4. Ús de JSON Schema Validator

### Pas 1: Accedir a l'Eina

1. Obre el teu navegador web.
2. Entra a [JSON Schema Lint](https://jsonschemalint.com/).

### Pas 2: Introduir l'Esquema

- En el panell destinat a l'esquema, copia i enganxa el JSON de l'esquema (secció 3.1).

### Pas 3: Introduir les Dades JSON

- En el panell destinat a les dades, enganxa l'array d'objectes (secció 3.2).

### Pas 4: Executar la Validació

- L'eina processarà automàticament ambdós panells i et mostrarà:
  - **Missatge de validació amb èxit:** Si les dades compleixen amb l'esquema.
  - **Errors i advertències:** En cas que existeixin discrepàncies, s'indicaran els problemes i es ressaltaran les àrees conflictives.

**Tot ok**
![image](https://github.com/user-attachments/assets/c8be5350-d613-45a8-af42-d3f1b1cddf44)

**Amb errors**
![image](https://github.com/user-attachments/assets/511d8dad-4223-4839-8c7a-3c8ab3568cb7)



---

## 5. Resum de les Opcions en JSON Schema

A continuació es presenta un resum de les paraules clau i opcions més utilitzades en la creació d'esquemes JSON:

- **`$schema`:**  
  Defineix la versió de l'especificació.  
  *Exemple:* `"http://json-schema.org/draft-07/schema#"`

- **`$id`:**  
  Identificador únic per a l'esquema, útil en esquemes referenciats.

- **`title` i `description`:**  
  Proporcionen un títol i una descripció per documentar l'esquema.

- **`type`:**  
  Defineix el tipus de dada (per exemple, `"object"`, `"array"`, `"string"`, `"number"`, `"integer"`, `"boolean"`, `"null"`).

- **`properties`:**  
  Per a esquemes de tipus objecte, defineix les propietats i les seves restriccions.  
  *Exemple:*
  ```json
  "properties": {
    "nom": { "type": "string" },
    "edat": { "type": "integer", "minimum": 0 }
  }
  ```

- **`required`:**  
  Especifica un array de noms de propietats obligatoris.

- **`additionalProperties`:**  
  Controla si es permeten propietats no definides en l'esquema. Pot ser `true`, `false` o un sub-esquema.

- **`items`:**  
  S'utilitza en arrays per definir l'estructura de cada element.  
  *Exemple:*
  ```json
  "items": {
    "type": "object",
    "properties": { ... },
    "required": [ ... ]
  }
  ```

- **`minItems` i `maxItems`:**  
  Estableixen el nombre mínim i màxim d'elements en un array.

- **`minLength` i `maxLength`:**  
  Defineixen la longitud mínima i màxima de cadenes.

- **`pattern`:**  
  Defineix una expressió regular que la cadena ha de complir.

- **`enum`:**  
  Restringeix el valor a un dels valors específics.  
  *Exemple:*
  ```json
  "enum": ["vermell", "verd", "blau"]
  ```

- **`format`:**  
  Indica formats predefinits per a cadenes (per exemple, `"email"`, `"date"`, `"uri"`).

- **`minimum`, `maximum`, `exclusiveMinimum`, `exclusiveMaximum`:**  
  S'utilitzen per establir límits en valors numèrics.

- **`multipleOf`:**  
  Especifica que un nombre ha de ser múltiple d'un valor determinat.

- **`const`:**  
  Indica que un valor ha de coincidir exactament amb un valor definit.

- **Composició d'esquemes:**
  - **`allOf`:** Tots els esquemes indicats han de ser vàlids.
  - **`anyOf`:** Almenys un dels esquemes ha de ser vàlid.
  - **`oneOf`:** Exactament un dels esquemes ha de ser vàlid.
  - **`not`:** Especifica un esquema que les dades no han de complir.

---

## 6. Bones Pràctiques i Propers Passos

- **Experimenta amb exemples:**  
  Modifica l'esquema i les dades per veure com reaccionen davant errors, omissions o dades mal formats.

- **Documenta el teu treball:**  
  Encara que JSON no permet comentaris, mantingues una documentació externa que expliqui la lògica i les regles del teu esquema.

- **Versiona els teus esquemes:**  
  A mesura que la teva aplicació evolucioni, versiona l'esquema per mantenir compatibilitat i claredat en l'evolució de les teves dades.

- **Integra la validació en el teu flux de treball:**  
  Un cop dominis la validació en línia, considera implementar validacions automàtiques en el teu projecte emprant llibreries com AJV (Node.js), jsonschema (Python) o altres, per assegurar la integritat de les dades en entorns de producció.

---

Amb aquest tutorial complet i l'índex corresponent, tens les bases per crear, validar i documentar esquemes JSON utilitzant un validador en línia com JSON Schema Lint. Ara pots experimentar, modificar i adaptar els teus esquemes per satisfer les necessitats dels teus projectes i assegurar que les teves dades mantinguin la integritat i consistència requerides.

¡Manos a l'obra!
