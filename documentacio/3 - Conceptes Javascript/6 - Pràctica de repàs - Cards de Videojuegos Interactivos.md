

## Ejercicio: Cards de Videojuegos Interactivos
![image](https://github.com/user-attachments/assets/355acdca-66c1-458c-bda2-185d5f8b5a9b)

### Objetivo

Crear una página web que muestre un conjunto de cards, cada una representando un videojuego. Cada card incluirá una imagen, el título y una breve descripción del videojuego. Además, se podrá interactuar con cada card de la siguiente manera:
- Al hacer clic en la card se mostrará un detalle del videojuego (por ejemplo, mediante un `alert`).
- Cada card tendrá un icono "like" que, al pulsarlo, cambiará de estado (empleando **classList.add**, **classList.remove** o **toggle**).

### Requisitos

- **Variables:**  
  - Utilizar `const` para seleccionar elementos del DOM.
  - Utilizar `let` para variables que se modificarán, como el array de videojuegos.

- **Manipulación del DOM:**  
  - Utilizar `document.querySelector` para acceder a los elementos.
  - Utilizar `innerHTML` para insertar el contenido dinámico en las cards.

- **Eventos e Interacción:**  
  - Utilizar `addEventListener` para gestionar los clics tanto en las cards como en el icono "like".
  - Utilizar `classList.toggle` para modificar la clase del icono "like" y reflejar el cambio de estado.

### Código de Ejemplo

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Cards de Videojuegos</title>
  <style>
    /* Estilos básicos para las cards */
    .card {
      border: 1px solid #ccc;
      border-radius: 8px;
      padding: 16px;
      margin: 8px;
      text-align: center;
      width: 200px;
      display: inline-block;
      transition: transform 0.3s, box-shadow 0.3s;
      cursor: pointer;
    }
    .card:hover {
      transform: scale(1.05);
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }
    .card img {
      width: 100%;
      border-radius: 8px;
    }
    .like {
      cursor: pointer;
      font-size: 24px;
      color: gray;
      user-select: none;
    }
    .like.active {
      color: red;
    }
  </style>
</head>
<body>
  <h1>Cards de Videojuegos</h1>
  <!-- Contenedor para las cards -->
  <div id="cardsContainer"></div>

  <script>
    // Array de objetos que representa los videojuegos
    let games = [
      {
        id: 1,
        title: "Aventura Épica",
        description: "Embárcate en una aventura llena de misterios y retos.",
        image: "https://via.placeholder.com/200x150?text=Aventura",
        liked: false
      },
      {
        id: 2,
        title: "Carreras Extrema",
        description: "Siente la adrenalina en cada carrera y domina la pista.",
        image: "https://via.placeholder.com/200x150?text=Carreras",
        liked: false
      },
      {
        id: 3,
        title: "Mundo Fantástico",
        description: "Explora reinos mágicos llenos de criaturas asombrosas.",
        image: "https://via.placeholder.com/200x150?text=Fantástico",
        liked: false
      }
    ];

    
  </script>
</body>
</html>
```

---

## Explicación

1. **Estructura de Datos:**  
   Se define un array `games` que contiene objetos. Cada objeto representa un videojuego y tiene propiedades como `id`, `title`, `description`, `image` y `liked`.

2. **Acceso y Manipulación del DOM:**  
   Se utiliza `document.querySelector` para seleccionar el contenedor donde se mostrarán las cards. La función `renderCards()` genera dinámicamente el contenido HTML de cada card utilizando `innerHTML`.

3. **Interacción:**  
   - Cada card tiene un evento de clic que muestra un `alert` con detalles del videojuego.  
   - El icono "like" cuenta con su propio evento de clic para alternar su estado, utilizando `classList.toggle` para cambiar la apariencia.

Este ejercicio permite poner en práctica el manejo de arrays de objetos, la manipulación del DOM y la gestión de eventos en JavaScript, aplicándolo en un contexto de videojuegos de forma interactiva.
