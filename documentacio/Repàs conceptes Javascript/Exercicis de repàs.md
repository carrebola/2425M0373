
## Ejercicio 1: Documento Básico y Mensaje en Consola

### **Enunciado y Explicación:**

En este primer ejercicio aprenderás a crear un documento HTML básico y vincularlo a un archivo JavaScript externo. La idea es asegurarte de que la configuración del entorno es correcta. Se trabajará en la creación del archivo HTML, la vinculación del script y la verificación de que el archivo JavaScript se ejecuta correctamente mediante la impresión de un mensaje en la consola del navegador.

### **Lo que se va a trabajar:**

- **Estructura básica de HTML.**
- **Vinculación de un archivo JavaScript externo.**
- **Uso de `console.log` para mostrar mensajes en la consola.**

### **Resultado Específico Esperado:**

- **En la Página Web:**  
  Verás una página sencilla con un título o encabezado que indique "Ejercicio 1: Documento Básico". No habrá contenido interactivo ni elementos dinámicos adicionales.

- **En la Consola del Navegador:**  
  Al abrir la consola (por ejemplo, pulsando F12), aparecerá el mensaje:
  ```
  ¡Hola desde JavaScript en el Ejercicio 1!
  ```

---

## Ejercicio 2: Manejo de Variables, Arrays y Objetos

### **Enunciado y Explicación:**

Este ejercicio se centra en los fundamentos de JavaScript. Deberás declarar variables utilizando `let` y `const`, crear un array y un objeto, y recorrer el array con un bucle. Esto te permitirá familiarizarte con la sintaxis y la manipulación de datos básicos en JavaScript.

### **Lo que se va a trabajar:**

- **Declaración y uso de variables (`let` y `const`).**
- **Creación y manipulación de arrays.**
- **Definición de objetos y acceso a sus propiedades.**
- **Uso de bucles (`for`) para recorrer arrays.**
- **Salida de información en la consola.**

### **Resultado Específico Esperado (ver en la Consola):**

- **Variables:**  
  Verás mensajes que muestren el contenido de la variable y de la constante, por ejemplo:
  ```
  Mensaje: Este es un mensaje con let
  Valor de PI: 3.1416
  ```

- **Array y Recorrido:**  
  Se imprimirá el array completo (por ejemplo, `["Rojo", "Verde", "Azul"]`) y, además, un mensaje por cada elemento indicando su posición, como:
  ```
  Color en la posición 0: Rojo
  Color en la posición 1: Verde
  Color en la posición 2: Azul
  ```

- **Objeto:**  
  Verás un mensaje que muestre el objeto completo, por ejemplo:
  ```
  Objeto persona: { nombre: "Laura", edad: 29, ciudad: "Valencia" }
  ```

---

## Ejercicio 3: Inyección de HTML en el DOM

### **Enunciado y Explicación:**

En este ejercicio aprenderás a manipular el DOM. Utilizarás `document.querySelector` para seleccionar un elemento específico del documento HTML (por ejemplo, un `<div>`) y luego usarás la propiedad `innerHTML` para inyectar contenido HTML dinámicamente en ese elemento.

### **Lo que se va a trabajar:**

- **Selección de elementos del DOM con `querySelector`.**
- **Manipulación del contenido de un elemento mediante `innerHTML`.**
- **Actualización dinámica de la página sin necesidad de recargar.**

### **Resultado Específico Esperado en la Página Web:**

- **Contenido Inyectado:**  
  Dentro del contenedor designado (por ejemplo, un `<div>`), se mostrará:
  - Un encabezado de nivel 2 con el texto:
    ```
    Contenido Inyectado
    ```
  - Un párrafo debajo con el texto:
    ```
    Este contenido fue agregado dinámicamente usando innerHTML.
    ```

---

## Ejercicio 4: Array de Objetos y Construcción de una Lista HTML

### **Enunciado y Explicación:**

Este ejercicio te permitirá trabajar con datos estructurados. Deberás crear un array de objetos, donde cada objeto representa un usuario con propiedades como `id`, `nombre` y `edad`. Luego, recorrerás el array para acceder a los datos y construirás una lista HTML (por ejemplo, una lista desordenada) que se inyectará en el documento.

### **Lo que se va a trabajar:**

- **Creación y manejo de arrays de objetos.**
- **Acceso a propiedades de objetos dentro de un array.**
- **Uso de bucles para recorrer arrays de objetos.**
- **Construcción dinámica de contenido HTML (listas) y su inyección en el DOM.**
- **Salida de información adicional en la consola (por ejemplo, mostrando el primer objeto o el nombre del segundo usuario).**

### **Resultado Específico Esperado:**

- **En la Consola:**  
  Se mostrarán mensajes que indiquen, por ejemplo:
  ```
  Primer usuario: { id: 1, nombre: "Juan", edad: 30 }
  Nombre del segundo usuario: María
  ```

- **En la Página Web:**  
  Dentro del contenedor, se verá un encabezado que diga:
  ```
  Lista de Usuarios
  ```
  Y debajo una lista (una `<ul>`) con cada usuario representado en un elemento de la lista. Cada elemento mostrará datos de un usuario, por ejemplo:
  ```
  ID: 1 - Nombre: Juan - Edad: 30
  ID: 2 - Nombre: María - Edad: 25
  ID: 3 - Nombre: Pedro - Edad: 35
  ```

---

## Ejercicio 5: Eventos y Creación Dinámica de una Tabla

### **Enunciado y Explicación:**

El último ejercicio se centra en la interacción con el usuario mediante eventos. Se trata de capturar el evento de clic en un botón para ejecutar una función que construya dinámicamente una tabla HTML a partir de un array de objetos (usuarios) y la inyecte en el documento. Esto te ayudará a comprender el manejo de eventos y la actualización dinámica del contenido del DOM.

### **Lo que se va a trabajar:**

- **Captura y manejo de eventos (clic en un botón).**
- **Construcción dinámica de una tabla HTML a partir de datos estructurados.**
- **Inyección de contenido HTML (tabla) en el DOM.**
- **Interacción en tiempo real y actualización del contenido en la página.**

### **Resultado Específico Esperado:**

- **Antes de la Interacción:**  
  La página mostrará un botón con el texto:
  ```
  Generar Tabla de Usuarios
  ```
  y el contenedor podrá tener otros contenidos previos (como los resultados de ejercicios anteriores).

- **Al Pulsar el Botón:**
  - **En la Consola:**  
    Se imprimirá un mensaje indicando que el botón fue pulsado, por ejemplo:
    ```
    Ejercicio 5: Botón clickeado, generando tabla...
    ```
  - **En la Página Web:**  
    Se inyectará una tabla HTML dentro del contenedor, con el siguiente formato:
    - **Encabezado:** Una fila con tres columnas tituladas "ID", "Nombre" y "Edad".
    - **Cuerpo de la Tabla:** Varias filas, cada una representando un usuario. Por ejemplo:
      - Fila 1:  
        ```
        ID: 1    Nombre: Juan    Edad: 30
        ```
      - Fila 2:  
        ```
        ID: 2    Nombre: María   Edad: 25
        ```
      - Fila 3:  
        ```
        ID: 3    Nombre: Pedro   Edad: 35
        ```

  La tabla se mostrará de forma ordenada y estructurada, permitiendo visualizar claramente los datos de cada usuario.

---

Cada uno de estos ejercicios está diseñado para que avances progresivamente en el aprendizaje de JavaScript y la manipulación del DOM, desde los conceptos básicos hasta la interacción dinámica con el usuario. Estos ejercicios te ayudarán a consolidar la estructura de un documento HTML, la vinculación de JavaScript, la manipulación de variables, arrays, objetos, la inyección de contenido HTML, y el manejo de eventos.
