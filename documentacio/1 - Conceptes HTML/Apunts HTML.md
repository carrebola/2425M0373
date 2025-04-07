
# Guia essencial d’etiquetes HTML

HTML proporciona etiquetes que ajuden a estructurar el contingut d'una manera clara i comprensible, tant per a usuaris com per a motors de cerca. A continuació s'explica com utilitzar algunes de les etiquetes més comunes i útils per construir pàgines web ben organitzades i accessibles.

## Índex

1. [Estructura bàsica d'una pàgina HTML](#1-estructura-bàsica-duna-pàgina-html)
2. [Encapçalaments (`<h1>` a `<h6>`)](#2-encapçalaments-h1-a-h6)
3. [Pàragraf (`<p>`)](#3-pàragraf-p)
4. [Text en negreta (`<strong>`) i cursiva (`<em>`)](#4-text-en-negreta-strong-i-cursiva-em)
5. [Llistes (`<ul>` i `<ol>`)](#5-llistes-no-ordenades-ul-i-llistes-ordenades-ol)
6. [Cites (`<blockquote>`)](#6-cites-blockquote)
7. [Seccions estructurals (`<header>`, `<main>`, `<section>`, `<footer>`)](#7-seccions-estructurals-header-main-section-footer)
8. [Divs per agrupació (`<div>`)](#8-divs-per-agrupació-div)
9. [Etiqueta `<img>` per inserir imatges](#9-etiqueta-img-per-inserir-imatges)
10. [Enllaços (`<a>`)](#10-enllaços-a)
11. [Taules (`<table>`)](#11-taules-table)
12. [Formularis (`<form>`, `<input>`, etc.)](#12-formularis-form-input-etc)
13. [Botons (`<button>`)](#13-botons-button)
14. [Span (`<span>`)](#14-span)

## 1. **Estructura bàsica d'una pàgina HTML**

```html
<!DOCTYPE html>
<html lang="ca">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Títol de la pàgina</title>
</head>
<body>
  <!-- Contingut principal va aquí -->
</body>
</html>
```

- `<head>`: Conté metadades sobre la pàgina (joc de caràcters, títol, enllaços a CSS, etc.).
- `<body>`: Inclou el contingut visible com text, imatges i seccions.

## 2. **Encapçalaments (`<h1>` a `<h6>`)**

S'utilitzen per estructurar el contingut en seccions jeràrquiques.

```html
<h1>Títol principal</h1>
<h2>Subtítol</h2>
<h3>Encapçalament de nivell 3</h3>
```

## 3. **Pàragraf (`<p>`)**

Serveix per agrupar i presentar text en blocs.

```html
<p>Aquest és un paràgraf de text.</p>
```

## 4. **Text en negreta (`<strong>`) i cursiva (`<em>`)**

```html
<p>Aquest text és <strong>important</strong> i aquest <em>rellevant</em>.</p>
```

## 5. **Llistes (`<ul>` i `<ol>`)**

- **Llista no ordenada:**
```html
<ul>
  <li>Ítem 1</li>
  <li>Ítem 2</li>
</ul>
```

- **Llista ordenada:**
```html
<ol>
  <li>Primer</li>
  <li>Segon</li>
</ol>
```

## 6. **Cites (`<blockquote>`)**

```html
<blockquote>
  "Aquesta és una cita famosa."
</blockquote>
```

## 7. **Seccions estructurals (`<header>`, `<main>`, `<section>`, `<footer>`)**

```html
<header>
  <h1>Títol de la pàgina</h1>
</header>
<main>
  <section>
    <h2>Secció principal</h2>
    <p>Contingut rellevant aquí.</p>
  </section>
</main>
<footer>
  <p>&copy; 2024 La meva pàgina web</p>
</footer>
```

## 8. **Divs per agrupació (`<div>`)**

```html
<div class="caixa">
  <p>Contingut agrupat dins d'un div.</p>
</div>
```

## 9. **Etiqueta `<img>` per inserir imatges**

```html
<img src="imatges/logo.png" alt="Logo de l'empresa" width="500" height="300">
```

## 10. **Enllaços (`<a>`)**

```html
<a href="https://example.com" target="_blank">Visita la nostra web</a>
```

## 11. **Taules (`<table>`)**

Les taules permeten presentar dades en format de files i columnes. Es componen de diverses etiquetes:

- `<table>`: Crea la taula.
- `<thead>`: Defineix l’encapçalament.
- `<tbody>`: Cos principal de la taula.
- `<tr>`: Defineix una fila.
- `<th>`: Cel·la d'encapçalament.
- `<td>`: Cel·la de dades.

```html
<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Edat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Anna</td>
      <td>28</td>
    </tr>
    <tr>
      <td>Joan</td>
      <td>35</td>
    </tr>
  </tbody>
</table>
```

## 12. **Formularis (`<form>`, `<input>`, etc.)**

Els formularis permeten recollir dades dels usuaris. Es poden construir amb diverses etiquetes:

- `<form>`: Contenidor principal.
- `<label>`: Associació descriptiva.
- `<input>`: Entrada de dades.
- `<textarea>`: Camp multilínia.
- `<select>` i `<option>`: Llistes desplegables.

```html
<form action="/enviar" method="post">
  <label for="nom">Nom:</label>
  <input type="text" id="nom" name="nom" required>

  <label for="email">Correu electrònic:</label>
  <input type="email" id="email" name="email">

  <label for="comentari">Comentari:</label>
  <textarea id="comentari" name="comentari"></textarea>

  <label for="opcio">Selecciona una opció:</label>
  <select id="opcio" name="opcio">
    <option value="1">Opció 1</option>
    <option value="2">Opció 2</option>
  </select>

  <button type="submit">Enviar</button>
</form>
```

## 13. **Botons (`<button>`)**

```html
<button type="button" onclick="alert('Hola!')">Fes clic aquí</button>
```

## 14. **Span (`<span>`)**

```html
<p>El <span style="color:red">text en vermell</span> és destacat.</p>
```

- Útil per estilització CSS o manipulació amb JavaScript.


