
## Ejercicio: Lista de Tareas Dinámica

![image](https://github.com/user-attachments/assets/94593fb5-bd1d-4367-bf00-006131f8a2fa)


### Objetivo

Crear una aplicación web sencilla que permita al usuario agregar tareas a una lista. Cada tarea se almacenará como un objeto dentro de un array. La aplicación debe:
- Obtener el valor de un input para crear una nueva tarea.
- Actualizar el DOM mostrando la lista de tareas mediante **innerHTML**.
- Permitir marcar o desmarcar una tarea como completada al hacer clic, utilizando **classList** para modificar su apariencia.
- Practicar el uso de variables declaradas con **const** y **let**.

### Requisitos Técnicos

- **Variables y Constantes:** Usa `const` para elementos del DOM y `let` para variables que se modificarán (por ejemplo, el array de tareas).
- **Acceso a Elementos:** Accede a los elementos del DOM con `document.querySelector`.
- **Manipulación del DOM:** Actualiza el contenido HTML de la lista con `innerHTML` y gestiona el valor del input con `.value`.
- **Eventos:** Utiliza `addEventListener` para capturar el clic en el botón de agregar y en cada tarea para marcarla como completada.
- **Clases CSS:** Emplea `classList.add` y `classList.remove` (o `classList.toggle`) para cambiar el estilo de la tarea cuando se complete.

### Descripción del Ejercicio

1. **HTML Básico:**  
   Crea una página con:
   - Un input para introducir la tarea.
   - Un botón para agregar la tarea.
   - Un contenedor (por ejemplo, un `<ul>`) para mostrar la lista de tareas.

2. **JavaScript:**  
   - Declara las variables necesarias (elementos del DOM y el array de tareas).
   - Crea un array vacío `tasks` para almacenar los objetos de tarea.
   - Define la estructura de cada tarea como un objeto con al menos dos propiedades: `id`, `name` y `completed` (inicialmente en `false`).
   - Implementa una función que recorra el array y actualice el DOM mostrando cada tarea. Cada elemento de la lista deberá:
     - Mostrar el nombre de la tarea.
     - Al hacer clic, alternar su estado de completado y actualizar su clase CSS (por ejemplo, añadiendo o quitando la clase `"completed"`).
   - Agrega un evento al botón que:
     - Obtenga el valor del input (utilizando `.value`).
     - Cree un objeto tarea con ese valor.
     - Lo añada al array `tasks`.
     - Limpie el input y vuelva a renderizar la lista de tareas.

### Código de Ejemplo

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Lista de Tareas</title>
  <style>
    /* Estilos para tareas completadas */
    .completed {
      text-decoration: line-through;
      color: gray;
    }
  </style>
</head>
<body>
  <h1>Lista de Tareas</h1>
  <!-- Input para ingresar nueva tarea -->
  <input type="text" id="taskInput" placeholder="Escribe una tarea">
  <!-- Botón para agregar la tarea -->
  <button id="addTaskBtn">Agregar Tarea</button>
  <!-- Contenedor para la lista de tareas -->
  <ul id="taskList"></ul>
  <script>
    ... crea tu código aquí
  </script>
</body>

## Puntos Clave del Ejercicio

- **Uso de Const y Let:**  
  - Se usa `const` para elementos del DOM que no se reasignan.  
  - Se usa `let` para el array `tasks`, ya que se modifica con nuevas tareas.

- **Manipulación de Arrays y Objetos:**  
  - El array `tasks` almacena objetos, cada uno representando una tarea.
  - Se accede y modifica la propiedad `completed` de cada objeto tarea.

- **Interacción con el DOM:**  
  - `document.querySelector` selecciona los elementos necesarios.
  - `innerHTML` actualiza la lista de tareas en el contenedor `<ul>`.
  - `.value` obtiene el contenido del input.
  - `addEventListener` se utiliza para manejar eventos de clic tanto en el botón como en cada tarea.
  - `classList.toggle` (además de `classList.add` y `classList.remove`) gestiona la clase `"completed"` para modificar el estilo de las tareas.

Este ejercicio permite poner en práctica varios conceptos fundamentales de JavaScript y manipulación del DOM, resultando ideal para afianzar estos conocimientos de manera práctica.
