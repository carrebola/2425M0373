# Tutorial Javascript básico
Cada sección incluye ejemplos prácticos de código y explicaciones para que puedas ir aprendiendo paso a paso.


## Índice del Tutorial de JavaScript

1. [Sección 1: Crear un Documento HTML con JS Vinculado y Sacar un Mensaje en la Consola](#sección-1-crear-un-documento-html-con-js-vinculado-y-sacar-un-mensaje-en-la-consola)
2. [Sección 2: Ejemplos con Tipos de Variables, Arrays y Objetos](#sección-2-ejemplos-con-tipos-de-variables-arrays-y-objetos)
3. [Sección 3: Inyectar Código HTML en un Elemento del DOM con `innerHTML` y `querySelector`](#sección-3-inyectar-código-html-en-un-elemento-del-dom-con-innerhtml-y-queryselector)
4. [Sección 4: Recorrer un Array con un Bucle y Mostrarlo en la Consola](#sección-4-recorrer-un-array-con-un-bucle-y-mostrarlo-en-la-consola)
5. [Sección 5: Crear un Array de Objetos con Datos de Usuarios y Acceder a sus Elementos Mostrándolos en la Consola](#sección-5-crear-un-array-de-objetos-con-datos-de-usuarios-y-acceder-a-sus-elementos-mostr%C3%A1ndolos-en-la-consola)
6. [Sección 6: Recorrer el Array de Objetos y Construir una Lista/Tabla a Partir de sus Datos](#sección-6-recorrer-el-array-de-objetos-y-construir-una-lista/tabla-a-partir-de-sus-datos)
7. [Sección 7: Capturar Evento Clic al Pulsar un Botón y Ejecutar una Función](#sección-7-capturar-evento-clic-al-pulsar-un-botón-y-ejecutar-una-función)
8. [Sección 8: Inyectar una Tabla de Datos a Partir de un Array de Objetos al Pulsar un Botón](#sección-8-inyectar-una-tabla-de-datos-a-partir-de-un-array-de-objetos-al-pulsar-un-botón)
9. [Cómo Probar el Tutorial](#cómo-probar-el-tutorial)

---

## Sección 1: Crear un Documento HTML con JS Vinculado y Sacar un Mensaje en la Consola

**index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Tutorial Básico de JavaScript</title>
</head>
<body>
  <h1>Tutorial Básico de JavaScript</h1>
  
  <!-- Un contenedor para mostrar contenido dinámico -->
  <div id="contenedor"></div>
  
  <!-- Botón para las secciones 7 y 8 -->
  <button id="btnTabla">Mostrar Tabla de Usuarios</button>
  
  <!-- Vinculación del archivo JavaScript -->
  <script src="script.js"></script>
</body>
</html>
```

**script.js** (fragmento inicial)
```js
// Sección 1: Mensaje en la consola al cargar el script.
console.log("Sección 1: ¡Hola desde JavaScript!");
```

---

## Sección 2: Ejemplos con Tipos de Variables, Arrays y Objetos

En esta sección veremos cómo declarar variables con `let` y `const`, y ejemplos de un array y un objeto.

```js
// Sección 2: Tipos de Variables

// Variable que puede modificarse
let variableLet = "Soy una variable con let";
console.log("Sección 2 - let:", variableLet);

// Constante cuyo valor no puede cambiar
const constante = "Soy una constante";
console.log("Sección 2 - const:", constante);

// Ejemplo de Array
let numeros = [1, 2, 3, 4, 5];
console.log("Sección 2 - Array de números:", numeros);

// Ejemplo de Objeto
let usuario = {
  nombre: "Ana",
  edad: 28,
  ciudad: "Madrid"
};
console.log("Sección 2 - Objeto usuario:", usuario);
```

---

## Sección 3: Inyectar Código HTML en un Elemento del DOM con `innerHTML` y `querySelector`

Utilizaremos `document.querySelector` para seleccionar un elemento y la propiedad `innerHTML` para inyectar nuevo contenido HTML.

```js
// Sección 3: Inyectar HTML en el contenedor
const contenedor = document.querySelector("#contenedor");
contenedor.innerHTML = "<p>Sección 3: Este contenido fue inyectado dinámicamente.</p>";
```

---

## Sección 4: Recorrer un Array con un Bucle y Mostrarlo en la Consola

Se crea un array sencillo y se recorre utilizando un bucle `for`, mostrando cada elemento en la consola.

```js
// Sección 4: Recorrer un Array
let frutas = ["Manzana", "Banana", "Cereza"];
for (let i = 0; i < frutas.length; i++) {
  console.log(`Sección 4: Elemento en la posición ${i}: ${frutas[i]}`);
}
```

---

## Sección 5: Crear un Array de Objetos con Datos de Usuarios y Acceder a sus Elementos Mostrándolos en la Consola

Aquí creamos un array que contiene objetos, cada uno representando un usuario, y mostramos algunos datos en la consola.

```js
// Sección 5: Array de Objetos de Usuarios
let usuarios = [
  { id: 1, nombre: "Juan", edad: 30 },
  { id: 2, nombre: "María", edad: 25 },
  { id: 3, nombre: "Pedro", edad: 35 }
];

// Acceder a elementos individuales
console.log("Sección 5: Primer usuario:", usuarios[0]);
console.log("Sección 5: Nombre del segundo usuario:", usuarios[1].nombre);
```

---

## Sección 6: Recorrer el Array de Objetos y Construir una Lista/Tabla a Partir de sus Datos

Recorremos el array de usuarios y construimos una lista HTML (por ejemplo, un `<ul>`) para mostrar sus datos en la página.

```js
// Sección 6: Construir una Lista de Usuarios en HTML
let listaHTML = "<h2>Sección 6: Lista de Usuarios</h2><ul>";
for (let i = 0; i < usuarios.length; i++) {
  listaHTML += `<li>ID: ${usuarios[i].id} - Nombre: ${usuarios[i].nombre} - Edad: ${usuarios[i].edad}</li>`;
}
listaHTML += "</ul>";

// Inyectamos la lista en el contenedor
contenedor.innerHTML += listaHTML;
```

---

## Sección 7: Capturar Evento Clic al Pulsar un Botón y Ejecutar una Función

En esta sección, se agrega un evento de clic a un botón para ejecutar una función y mostrar un mensaje en la consola.

```js
// Sección 7: Capturar el evento clic en el botón
const btnTabla = document.getElementById("btnTabla");
btnTabla.addEventListener("click", function() {
  console.log("Sección 7: Botón clickeado. Se ejecuta la función.");
});
```

---

## Sección 8: Inyectar una Tabla de Datos a Partir de un Array de Objetos al Pulsar un Botón

Al hacer clic en el botón, se genera e inyecta una tabla HTML que muestra los datos del array de objetos `usuarios`.

```js
// Sección 8: Inyectar una Tabla de Usuarios al Pulsar el Botón
btnTabla.addEventListener("click", function() {
  // Construir la tabla HTML a partir del array de usuarios
  let tablaHTML = `
    <h2>Sección 8: Tabla de Usuarios</h2>
    <table border="1" cellpadding="5">
      <thead>
        <tr>
          <th>ID</th>
          <th>Nombre</th>
          <th>Edad</th>
        </tr>
      </thead>
      <tbody>
  `;

  for (let i = 0; i < usuarios.length; i++) {
    tablaHTML += `
      <tr>
        <td>${usuarios[i].id}</td>
        <td>${usuarios[i].nombre}</td>
        <td>${usuarios[i].edad}</td>
      </tr>
    `;
  }

  tablaHTML += `
      </tbody>
    </table>
  `;

  // Inyectamos la tabla en el contenedor (se agrega al contenido existente)
  contenedor.innerHTML += tablaHTML;
});
```

---



## Cómo Probar el Tutorial

1. **Crea los Archivos:**  
   - Crea un archivo `index.html` con el contenido mostrado en la Sección 1.  
   - Crea un archivo `script.js` en la misma carpeta y copia todo el código de las Secciones 1 a 8.

2. **Abre el HTML en tu Navegador:**  
   - Al cargar la página, abre la consola del navegador para ver los mensajes y resultados de las primeras secciones.
   - Verás el contenido inyectado en el `<div id="contenedor">`.

3. **Interacción con el Botón:**  
   - Haz clic en el botón “Mostrar Tabla de Usuarios” para activar las Secciones 7 y 8, donde se muestra un mensaje en la consola y se inyecta una tabla de datos en la página.

