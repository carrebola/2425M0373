
  # Gestió d'Usuaris amb Firebase

## Índex

- [Gestió d'Usuaris amb Firebase](#gestió-dusuaris-amb-firebase)
  - [Índex](#índex)
  - [Què és Firebase?](#què-és-firebase)
  - [Com funciona Firebase en aquest projecte?](#com-funciona-firebase-en-aquest-projecte)
    - [1. Configuració de Firebase](#1-configuració-de-firebase)
    - [2. Operacions CRUD](#2-operacions-crud)
  - [Codi principal del projecte](#codi-principal-del-projecte)
    - [Detall pas a pas](#detall-pas-a-pas)
  - [Altres funcions del projecte](#altres-funcions-del-projecte)
  - [Conclusió](#conclusió)
    - [2. Operacions CRUD](#2-operacions-crud-1)
  - [Codi principal del projecte](#codi-principal-del-projecte-1)
    - [Detall pas a pas](#detall-pas-a-pas-1)
  - [Altres funcions del projecte](#altres-funcions-del-projecte-1)
  - [Conclusió](#conclusió-1)

Aquest projecte és una aplicació web que permet gestionar usuaris (crear, llegir, actualitzar i eliminar) utilitzant Firebase com a base de dades en temps real. Està orientat a facilitar una primera experiència pràctica amb Cloud Firestore i operacions CRUD.

---

## Què és Firebase?

Firebase és una plataforma de desenvolupament d'aplicacions web i mòbils proporcionada per Google. Ofereix una varietat d'eines i serveis que faciliten el desenvolupament d'aplicacions modernes, com bases de dades en temps real, autenticació, emmagatzematge al núvol, allotjament, anàlisi i molt més.

En aquest projecte, utilitzem **Cloud Firestore**, una base de dades NoSQL basada en documents que permet emmagatzemar i sincronitzar dades entre aplicacions de manera automàtica i en temps real.

---

## Com funciona Firebase en aquest projecte?

La següent imatge mostra un exemple real del panell de Firestore a Firebase, on s'ha creat una col·lecció anomenada `alumnos`. Dins d'aquesta col·lecció s'emmagatzemen documents que representen usuaris individuals. Cada document té un identificador únic generat automàticament (com `1Gd1cHttMN6AavcYb9Za`) i conté camps com `nombre`, `apellidos` i `email`.

![image](https://github.com/user-attachments/assets/f355f5d6-4dc3-4102-9b96-100012ed9745)


Aquest exemple és representatiu del tipus d'estructura que es crea en executar correctament les operacions CRUD descrites més avall. A la vista es poden observar múltiples documents dins la col·lecció i com es visualitzen els seus camps des de la consola de Firebase.

### 1. Configuració de Firebase

- S'inicialitza Firebase amb les credencials del projecte (obtingudes a la consola de Firebase).
- S'utilitza Firestore com a base de dades per emmagatzemar les dades dels usuaris.

### 2. Operacions CRUD

- **Crear**: Afegir nous usuaris a la base de dades.
- **Llegir**: Obtenir i mostrar els usuaris emmagatzemats a la base de dades.
- **Actualitzar**: Modificar les dades d'un usuari existent.
- **Eliminar**: Eliminar un usuari de la base de dades.

---

## Codi principal del projecte

El següent fragment de codi JavaScript mostra com s'implementa la funció `cargarUsuarios()`, encarregada de llegir els usuaris des de Firestore i mostrar-los en pantalla. A continuació s'explica línia per línia:

```javascript
function cargarUsuarios() {
  // S'obté la referència al cos de la taula on es mostraran els usuaris
  var cuerpoTablaUsuarios = document.querySelector("#userTableBody");

  // Es consulten tots els documents de la col·lecció "alumnos"
  getDocs(collection(db, "alumnos")).then(function (instantaneaConsulta) {
    // S'inicialitza una cadena buida per acumular les files HTML
    var filas = "";

    // S'extreuen els documents obtinguts de la col·lecció com un array
    var documentos = instantaneaConsulta.docs;

    // Es recorre cada document (usuari) per generar una fila de la taula
    for (var i = 0; i < documentos.length; i++) {
      var documento = documentos[i]; // Document individual
      var usuario = documento.data(); // S'extreuen les dades de l'usuari

      // Es construeix la fila amb les dades i botons d'acció
      filas += `
        <tr data-id="${documento.id}">
          <td>${usuario.nombre}</td>
          <td>${usuario.apellidos}</td>
          <td>
            <button class="editar">Editar</button>
            <button class="eliminar">Eliminar</button>
          </td>
        </tr>`;
    }

    // S'injecta l'HTML generat al cos de la taula
    cuerpoTablaUsuarios.innerHTML = filas;

    // S'assignen esdeveniments als botons d'editar i eliminar generats dinàmicament
    añadirEventosBotones();
  });
}
```

### Detall pas a pas

- `document.querySelector("#userTableBody")`: Obté la referència a l'element `<tbody>` de la taula on es renderitzaran els usuaris.
- `getDocs(collection(db, "alumnos"))`: Sol·licita tots els documents de la col·lecció `alumnos` a la base de dades.
- `instantaneaConsulta.docs`: Obté els documents retornats per la consulta com un array.
- `documento.data()`: Extreu les dades de cada document (nom i cognoms de l'usuari).
- `filas += ...`: Construeix dinàmicament l'HTML de cada fila de la taula, incloent-hi botons per editar i eliminar.
- `cuerpoTablaUsuarios.innerHTML = filas`: Insereix el contingut generat a la taula del DOM.
- `añadirEventosBotones()`: Associa esdeveniments de clic als botons d'acció que s'acaben d'afegir.

---

## Altres funcions del projecte

- `crearUsuario(nombre, apellidos)`: Afegeix un nou document a la col·lecció `alumnos` utilitzant `addDoc`.
- `actualizarUsuario(id, nombre, email)`: Modifica un document existent identificat pel seu ID utilitzant `updateDoc`.
- `eliminarUsuario(id)`: Elimina un document específic de la col·lecció mitjançant `deleteDoc`.
- `añadirEventosBotones()`: Afegeix listeners als botons d'edició i eliminació generats dinàmicament per a cada usuari.
- **Gestor del formulari**: Captura l'esdeveniment `submit`, valida els camps i crida `crearUsuario()`.
- `DOMContentLoaded`: Carrega les dades automàticament quan s'inicia l'aplicació.

---

## Conclusió

Aquest document ofereix una guia completa per implementar una interfície senzilla però funcional per gestionar usuaris amb Firebase Firestore. És un bon punt de partida per introduir-se en el món del desenvolupament d'aplicacions web amb bases de dades en temps real. 

Un cop entesa la mecànica bàsica, pots afegir millores com la validació avançada de formularis, missatges d'error amigables, autenticació d'usuaris o funcionalitats com cerca i filtratge dinàmic.

Consulta sempre la [documentació oficial de Firebase](https://firebase.google.com/docs) per mantenir-te al dia amb les novetats i bones pràctiques. Bon desenvolupament i molta sort amb els teus projectes!

### 2. Operacions CRUD

- **Crear**: Afegir nous usuaris a la base de dades.
- **Llegir**: Obtenir i mostrar els usuaris emmagatzemats a la base de dades.
- **Actualitzar**: Modificar les dades d'un usuari existent.
- **Eliminar**: Eliminar un usuari de la base de dades.

---

## Codi principal del projecte

El següent fragment de codi JavaScript mostra com s'implementa la funció `cargarUsuarios()`, encarregada de llegir els usuaris des de Firestore i mostrar-los en pantalla. A continuació s'explica línia per línia:

```javascript
function cargarUsuarios() {
  // S'obté la referència al cos de la taula on es mostraran els usuaris
  var cuerpoTablaUsuarios = document.querySelector("#userTableBody");

  // Es consulten tots els documents de la col·lecció "alumnos"
  getDocs(collection(db, "alumnos")).then(function (instantaneaConsulta) {
    // S'inicialitza una cadena buida per acumular les files HTML
    var filas = "";

    // S'extreuen els documents obtinguts de la col·lecció com un array
    var documentos = instantaneaConsulta.docs;

    // Es recorre cada document (usuari) per generar una fila de la taula
    for (var i = 0; i < documentos.length; i++) {
      var documento = documentos[i]; // Document individual
      var usuario = documento.data(); // S'extreuen les dades de l'usuari

      // Es construeix la fila amb les dades i botons d'acció
      filas += `
        <tr data-id="${documento.id}">
          <td>${usuario.nombre}</td>
          <td>${usuario.apellidos}</td>
          <td>
            <button class="editar">Editar</button>
            <button class="eliminar">Eliminar</button>
          </td>
        </tr>`;
    }

    // S'injecta l'HTML generat al cos de la taula
    cuerpoTablaUsuarios.innerHTML = filas;

    // S'assignen esdeveniments als botons d'editar i eliminar generats dinàmicament
    añadirEventosBotones();
  });
}
```

### Detall pas a pas

- `document.querySelector("#userTableBody")`: Obté la referència a l'element `<tbody>` de la taula on es renderitzaran els usuaris.
- `getDocs(collection(db, "alumnos"))`: Sol·licita tots els documents de la col·lecció `alumnos` a la base de dades.
- `instantaneaConsulta.docs`: Obté els documents retornats per la consulta com un array.
- `documento.data()`: Extreu les dades de cada document (nom i cognoms de l'usuari).
- `filas += ...`: Construeix dinàmicament l'HTML de cada fila de la taula, incloent-hi botons per editar i eliminar.
- `cuerpoTablaUsuarios.innerHTML = filas`: Insereix el contingut generat a la taula del DOM.
- `añadirEventosBotones()`: Associa esdeveniments de clic als botons d'acció que s'acaben d'afegir.

---

## Altres funcions del projecte

- `crearUsuario(nombre, apellidos)`: Afegeix un nou document a la col·lecció `alumnos` utilitzant `addDoc`.
- `actualizarUsuario(id, nombre, email)`: Modifica un document existent identificat pel seu ID utilitzant `updateDoc`.
- `eliminarUsuario(id)`: Elimina un document específic de la col·lecció mitjançant `deleteDoc`.
- `añadirEventosBotones()`: Afegeix listeners als botons d'edició i eliminació generats dinàmicament per a cada usuari.
- **Gestor del formulari**: Captura l'esdeveniment `submit`, valida els camps i crida `crearUsuario()`.
- `DOMContentLoaded`: Carrega les dades automàticament quan s'inicia l'aplicació.

---

## Conclusió

Aquest document ofereix una guia completa per implementar una interfície senzilla però funcional per gestionar usuaris amb Firebase Firestore. És un bon punt de partida per introduir-se en el món del desenvolupament d'aplicacions web amb bases de dades en temps real. 

Un cop entesa la mecànica bàsica, pots afegir millores com la validació avançada de formularis, missatges d'error amigables, autenticació d'usuaris o funcionalitats com cerca i filtratge dinàmic.

Consulta sempre la [documentació oficial de Firebase](https://firebase.google.com/docs) per mantenir-te al dia amb les novetats i bones pràctiques. Bon desenvolupament i molta sort amb els teus projectes!
