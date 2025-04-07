
## Práctica: Generación Dinámica de una Tabla de Criptomonedas con JavaScript

### **Objetivo General:**

Implementar una solución en la que se genere dinámicamente una tabla de datos de criptomonedas utilizando JavaScript. La tabla se insertará en una página HTML que ya contiene el encabezado y una fila de ejemplo (modelo). A través de esta práctica, se pondrán en práctica conceptos fundamentales de JavaScript y manipulación del DOM, tales como la definición de variables, arrays, objetos, recorrido de arrays, inyección de HTML y captura de eventos.
![image](https://github.com/user-attachments/assets/bffafd03-547d-422f-be37-c9fbd8b9e04c)

---

### **Temas a Trabajar:**

1. **Estructura Básica y Vinculación de JavaScript:**
   - Uso de un documento HTML que incluya la hoja de estilos CSS.
   - Inserción de un script externo o interno en el HTML.

2. **Declaración y Uso de Variables, Arrays y Objetos:**
   - Declarar variables con `let` y `const`.
   - Crear un array de objetos que contenga los datos de diversas criptomonedas (por ejemplo, nombre, símbolo, precio, capitalización, y cambio en 24h).

3. **Manipulación del DOM:**
   - Seleccionar elementos mediante `document.querySelector` o `getElementById`.
   - Utilizar la propiedad `innerHTML` para inyectar contenido dinámico en el HTML.

4. **Recorrido de Arrays y Construcción Dinámica de Contenido:**
   - Recorrer el array de objetos con bucles (por ejemplo, `for` o `forEach`).
   - Generar dinámicamente las filas de la tabla utilizando los datos del array.

5. **Captura y Manejo de Eventos:**
   - Capturar el evento de clic en un botón para, por ejemplo, actualizar o regenerar la tabla.
   - Mostrar mensajes en la consola para verificar el flujo de ejecución.

---

### **Enunciado de la Práctica:**

1. **Parte 1 – Preparación del Modelo HTML:**

   Se te proporcionará el siguiente archivo HTML (sin JavaScript) que contiene la estructura básica, estilos y una tabla con el encabezado y una única fila de ejemplo. Esta fila es el modelo que deberás replicar dinámicamente con JS.

   _[Se incluye el HTML del modelo que contiene el encabezado y una única fila de ejemplo de la tabla (ver archivo de referencia).]_

2. **Parte 2 – Definición del Array de Datos:**

   Dentro de un archivo JavaScript vinculado al HTML (o en una etiqueta `<script>` al final del documento), define un array de objetos llamado `criptomonedas`. Cada objeto representará una criptomoneda y deberá tener las siguientes propiedades:
   
   - `name`: Nombre de la criptomoneda (ej. "Bitcoin").
   - `symbol`: Símbolo de la criptomoneda (ej. "BTC").
   - `price`: Precio actual en USD (ej. 45000).
   - `marketCap`: Capitalización de mercado (ej. "850B").
   - `change24h`: Variación en las últimas 24 horas (ej. "+2.5%").

   **Ejemplo de datos:**
   - Bitcoin – BTC – 45000 – 850B – +2.5%
   - Ethereum – ETH – 3200 – 370B – +1.8%
   - Cardano – ADA – 1.2 – 40B – -0.5%
   - Binance Coin – BNB – 410 – 70B – +3.1%
   - Solana – SOL – 100 – 30B – +4.0%

3. **Parte 3 – Generación Dinámica de la Tabla:**

   Utiliza JavaScript para crear una función que haga las siguientes acciones:
   
   - Seleccionar el contenedor del modelo de tabla (por ejemplo, el `<tbody>` o el `<div>` donde se debe inyectar la tabla).
   - Recorrer el array `criptomonedas` y, para cada objeto, generar una nueva fila (`<tr>`) que respete el formato de la fila de ejemplo.
   - Inyectar todas las filas generadas en el lugar adecuado del HTML (por ejemplo, reemplazando el contenido actual del `<tbody>` o agregándolo al contenedor).

4. **Parte 4 – Captura de Evento para Actualización de Datos:**

   Agrega un botón (ya presente en el modelo) que, al pulsarse, ejecute una función en JavaScript que:
   
   - Limpie el contenido existente de la tabla (si es necesario).
   - Vuelva a generar las filas a partir del array (esto puede simular la actualización de datos) utilizando la función creada en el apartado 3.
   - Imprima en la consola un mensaje que confirme que el botón ha sido pulsado y que la tabla se ha actualizado.
   - Modifique el color del botón (modificando su clase) y su contenido por el texto (Tabla actualizada)

5. **Parte 5 – Pruebas y Verificación:**

   - Verifica en la consola que se muestran los mensajes de depuración correspondientes (por ejemplo, al pulsar el botón).
   - Asegúrate de que la tabla en la página se complete con todas las filas generadas dinámicamente, utilizando el modelo de la única fila de ejemplo.

---

### **Resultado Final Esperado:**

- La página HTML debe mostrar la tabla con el encabezado y, en lugar de una única fila de ejemplo, la tabla contendrá tantas filas como objetos existan en el array `criptomonedas`.
- Al cargar la página, la tabla se genera dinámicamente y se inserta en el contenedor designado.
- Al pulsar el botón "Actualizar Datos" (o similar), se debe regenerar la tabla y aparecer un mensaje en la consola que indique que la actualización se realizó correctamente y el debe aparecer el botón modificado.
- Todo el proceso (creación de variables, definición de arrays, manipulación del DOM, recorrido de arrays, y manejo de eventos) debe evidenciarse en la implementación.

---

### **Puntos de Evaluación:**

- **Correcta definición y uso de variables y arrays.**
- **Implementación adecuada del recorrido de arrays para generar contenido dinámico.**
- **Manipulación del DOM para inyectar contenido usando `innerHTML`.**
- **Captura y respuesta a eventos (clic en el botón) con mensajes en la consola.**
- **Cumplimiento del modelo HTML proporcionado, replicando correctamente el formato de la fila de ejemplo.**

---

Con esta práctica, consolidarás los conceptos fundamentales de JavaScript y la manipulación dinámica de HTML, aplicándolos en un contexto real y actual, como lo es la presentación de datos de criptomonedas. ¡Manos a la obra!

A continuación se muestra un prototipo completo de página HTML (sin JavaScript) que presenta una tabla con el encabezado y una única fila de datos de ejemplo. Esta fila sirve como modelo para que, posteriormente, el alumno utilice JavaScript para generar dinámicamente el resto de las filas de la tabla.

---

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Tendencias en Criptomonedas 2025 - Modelo de Fila</title>
  <style>
    /* Reset básico */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: Arial, sans-serif;
      background-color: #f2f2f2;
      color: #333;
      line-height: 1.6;
    }
    
    /* Navbar */
    .navbar {
      background-color: #333;
      color: #fff;
      padding: 15px;
      text-align: center;
    }
    
    .navbar h1 {
      font-size: 24px;
    }
    
    /* Contenedor principal */
    .container {
      max-width: 960px;
      margin: 20px auto;
      padding: 0 20px;
    }
    
    /* Contenedor de la tabla */
    .table-container {
      background-color: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
      margin-top: 20px;
    }
    
    /* Estilos de la tabla */
    table {
      width: 100%;
      border-collapse: collapse;
    }
    
    thead {
      background-color: #444;
      color: #fff;
    }
    
    th, td {
      padding: 12px 15px;
      text-align: left;
      border-bottom: 1px solid #ddd;
    }
    
    tr:hover {
      background-color: #f1f1f1;
    }
  </style>
</head>
<body>
  <!-- Navbar con el título -->
  <nav class="navbar">
    <h1>Tendencias en Criptomonedas 2025</h1>
  </nav>
  
  <!-- Contenedor principal -->
  <div class="container">
    <div class="table-container">
      <h2>Modelo de Fila para Tabla de Criptomonedas</h2>
      <!-- Tabla con encabezado y una única fila de ejemplo -->
      <table>
        <thead>
          <tr>
            <th>Nombre</th>
            <th>Símbolo</th>
            <th>Precio (USD)</th>
            <th>Capitalización</th>
            <th>Cambio 24h</th>
          </tr>
        </thead>
        <tbody>
          <!-- Fila de ejemplo (modelo). El alumno deberá replicar este formato para generar todas las filas dinámicamente mediante JavaScript -->
          <tr>
            <td>Bitcoin</td>
            <td>BTC</td>
            <td>45,000</td>
            <td>850B</td>
            <td>+2.5%</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</body>
</html>
```

---

### Explicación

- **Estructura y Estilos:**  
  La página cuenta con un diseño moderno utilizando únicamente CSS. Se incluye un navbar y un contenedor principal con estilos que otorgan un aspecto limpio y profesional.

- **Tabla de Datos:**  
  La tabla muestra un encabezado con las columnas: *Nombre*, *Símbolo*, *Precio (USD)*, *Capitalización* y *Cambio 24h*.  
  Se ha incluido una única fila de ejemplo que contiene datos de "Bitcoin". Esta fila actúa como modelo para que el alumno pueda replicarla mediante JavaScript y, de esta manera, generar el resto de las filas con datos dinámicos.

Este prototipo sirve como base para que, posteriormente, se implemente la generación dinámica de filas usando JavaScript. ¡Manos a la obra!

