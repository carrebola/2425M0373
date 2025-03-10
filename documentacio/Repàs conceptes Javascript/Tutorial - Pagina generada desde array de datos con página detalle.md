# Guía Completa: Pagina generada desde array de datos con página detalle

Este tutorial te muestra cómo crear y manejar tarjetas (cards) cuyo `id` coincide directamente con su posición en el array, evitando el uso de búsquedas adicionales. El flujo es más sencillo al generar una página principal que muestra las tarjetas y otra página de detalle que recibe el `id` en la URL.

---

## 1. Estructura de Archivos

Contaremos con dos páginas principales:

- `index.html`: Genera tarjetas dinámicamente y asigna eventos para redirigir a la página de detalles.
- `detalle.html`: Recibe el ID como parámetro de la URL y muestra la información correspondiente.

Organización sugerida:
```
mi-proyecto/
  ├─ index.html
  ├─ detalle.html
  └─ js/
      ├─ index.js
      └─ detalle.js
```

---

## 2. Página Principal (`index.html`)

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Página Principal</title>
</head>
<body>
  <h1>Listado de Tarjetas</h1>
  <!-- Contenedor para las tarjetas -->
  <div id="contenedor-cards"></div>

  <script src="js/index.js"></script>
</body>
</html>
```

En esta página definimos el contenedor `<div id="contenedor-cards"></div>` que usaremos para inyectar las tarjetas.

---

## 3. Generar Tarjetas en `index.js` con `innerHTML`

### Ventaja Principal
Establecer el `id` de cada objeto para que coincida con su posición en el array permite un acceso directo a través de `data[<posición>]`, sin recurrir a métodos como `find`.

```js
// 1. Array de objetos de ejemplo
// Observa que cada "id" coincide con el índice en el array.
const data = [
  { id: 0, titulo: "Tarjeta 0", descripcion: "Descripción de la tarjeta 0" },
  { id: 1, titulo: "Tarjeta 1", descripcion: "Descripción de la tarjeta 1" },
  { id: 2, titulo: "Tarjeta 2", descripcion: "Descripción de la tarjeta 2" }
];

// 2. Seleccionar el contenedor
const contenedor = document.querySelector('#contenedor-cards');

// 3. Construir un string de HTML con un bucle for y asignarlo a innerHTML
let htmlCards = '';

for (let i = 0; i < data.length; i++) {
  const item = data[i];
  htmlCards += `
    <div class="card">
      <h2>${item.titulo}</h2>
      <p>${item.descripcion}</p>
      <button class="mi-clase" id="btn-${item.id}">Ver Detalles</button>
    </div>
  `;
}

contenedor.innerHTML = htmlCards;

// 4. Asignar eventos de clic a los botones generados
const elementos = document.querySelectorAll('.mi-clase');

for (let i = 0; i < elementos.length; i++) {
  elementos[i].addEventListener('click', function () {
    // Ejemplo: "btn-1" -> extraer "1"
    const itemId = this.id.split('-')[1];

    // Redirigir a detalle.html con el parámetro "id"
    // Como itemId es igual al índice en el array, luego lo usaremos para hacer data[itemId]
    window.location.href = `detalle.html?id=${itemId}`;
  });
}
```

---

## 4. Página de Detalle (`detalle.html`)

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Página de Detalle</title>
</head>
<body>
  <h1>Detalle del Elemento</h1>
  <p>ID recibido: <span id="id-recibido"></span></p>
  <p>Título: <span id="titulo"></span></p>
  <p>Descripción: <span id="descripcion"></span></p>

  <script src="js/detalle.js"></script>
</body>
</html>
```

---

## 5. Mostrar Datos en `detalle.js` sin `find`

Al tener el `id` como posición del array, simplemente usaremos `data[idRecibido]`.

```js
// Mantenemos el mismo array (con IDs que coinciden con el índice)
const data = [
  { id: 0, titulo: "Tarjeta 0", descripcion: "Descripción de la tarjeta 0" },
  { id: 1, titulo: "Tarjeta 1", descripcion: "Descripción de la tarjeta 1" },
  { id: 2, titulo: "Tarjeta 2", descripcion: "Descripción de la tarjeta 2" }
];

// 1. Obtener la parte "?id=..." de la URL
const queryString = window.location.search;
const urlParams = new URLSearchParams(queryString);
const idRecibido = urlParams.get('id'); // p. ej.: "1"

// 2. Mostrar el ID en la página
const spanIdRecibido = document.querySelector('#id-recibido');
if (spanIdRecibido) {
  spanIdRecibido.textContent = idRecibido;
}

// 3. Convertir idRecibido a número e ir directamente al elemento
const index = parseInt(idRecibido);

// Validar que el índice exista en data
if (index >= 0 && index < data.length) {
  const objetoEncontrado = data[index];

  // 4. Mostrar sus datos
  const tituloSpan = document.querySelector('#titulo');
  const descSpan = document.querySelector('#descripcion');

  if (tituloSpan) {
    tituloSpan.textContent = objetoEncontrado.titulo;
  }
  if (descSpan) {
    descSpan.textContent = objetoEncontrado.descripcion;
  }
} else {
  console.log('El ID no es válido:', idRecibido);
}
```

> **Nota**: Al tener `id` == índice, evitas el uso de `Array.find()` y accedes al objeto con `data[index]`.

---

## 6. Pasos para Probar la Aplicación

1. **Abre `index.html`** en tu navegador. Verás las tarjetas con IDs 0, 1, 2.
2. Al hacer clic en el botón "Ver Detalles" (por ejemplo, ID 1), irás a `detalle.html?id=1`.
3. En `detalle.html`, se convierte esa cadena en un número y se utiliza directamente `data[index]` para cargar la información.

---

## Conclusión

1. Ajustamos el array para que el `id` coincida con la posición del elemento.
2. Evitamos `find`: usamos `data[id]` para recuperar el objeto.
3. Generamos las tarjetas con un bucle `for` y asignamos eventos de clic usando `innerHTML`.
4. En la página de detalle, leemos el `id` en la URL y accedemos al objeto por índice.

He añadido algunos retoques finales y he comprobado la gramática. ¡Disfruta de esta versión simplificada del flujo de datos!

