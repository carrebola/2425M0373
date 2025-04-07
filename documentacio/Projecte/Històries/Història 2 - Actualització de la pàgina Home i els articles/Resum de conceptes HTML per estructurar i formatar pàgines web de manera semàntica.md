---
dg-publish: true
---

HTML proporciona etiquetes semàntiques que ajuden a estructurar el contingut d'una manera clara i comprensible, tant per a usuaris com per a motors de cerca. A continuació s'explica com utilitzar algunes de les etiquetes més comunes...

#### 1. **Estructura bàsica d'una pàgina HTML**

L'estructura típica d'una pàgina HTML comença amb la declaració del tipus de document i es divideix en dues parts principals: `<head>` i `<body>`.

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

- **`head`**: Conté metadades sobre la pàgina (jocs de caràcters, títol, enllaços a CSS, etc.).
- **`body`**: On es troba el contingut visible, com text, imatges, seccions, etc.

#### 2. **Encapçalaments** (`<h1>` a `<h6>`)

Els encapçalaments són utilitzats per estructurar el contingut en seccions jeràrquiques.

```html
<h1>Títol principal de la pàgina</h1>
<h2>Subtítol</h2>
<h3>Encapçalament de nivell 3</h3>
```

- **`<h1>`** és el títol principal d'una pàgina, i **`<h2>`** a **`<h6>`** indiquen subseccions.

#### 3. **Pàragraf** (`<p>`)

Els paràgrafs són la manera principal de presentar text en blocs.

```html
<p>Aquest és un paràgraf de text. Es pot combinar amb altres etiquetes per formatar el text.</p>
```

#### 4. **Text en negreta** (`<strong>`) i **cursiva** (`<em>`)

Es fan servir per donar èmfasi al text.

```html 
<p>Aquest text és <strong>molt important</strong> i aquest altre és <em>rellevant</em>.</p>
```

- **`<strong>`**: Marca text amb importància semàntica (apareix en negreta).
- **`<em>`**: Marca èmfasi, normalment en cursiva.

#### 5. **Llistes no ordenades** (`<ul>`) i **llistes ordenades** (`<ol>`)

Les llistes són útils per estructurar informació en punts o numerar ítems.

- **Llista no ordenada (amb punts):**
```html 
<ul>
  <li>Ítem 1</li>
  <li>Ítem 2</li>
  <li>Ítem 3</li>
</ul>
```

- **Llista ordenada (amb números):**

```html
<ol>
  <li>Ítem 1</li>
  <li>Ítem 2</li>
  <li>Ítem 3</li>
</ol>
```

#### 6. **Cites** (`<blockquote>`)

Per a textos citats o destacats.

```html
<blockquote>
  "Aquesta és una cita famosa."
</blockquote>
```
Apareix destacat i normalment indenta el text.

#### 7. **Seccions semàntiques** (`<header>`, `<main>`, `<section>`, `<footer>`)

Aquestes etiquetes s'utilitzen per a una millor organització i claredat en la disposició de la pàgina.

```html
<header>
  <h1>Títol de la pàgina</h1>
</header>
<main>
  <section>
    <h2>Secció principal</h2>
    <p>Aquesta és la secció principal del contingut.</p>
  </section>
</main>

<footer>
  <p>&copy; 2024 La meva pàgina web</p>
</footer>
```

- **`<header>`**: Per al contingut superior com el títol i menús de navegació.
- **`<main>`**: Secció principal del document (únic per pàgina).
- **`<section>`**: Per dividir el contingut en parts lògiques.
- **`<footer>`**: Per a la part inferior de la pàgina, com informació legal o crèdits.

#### 8. **Divs per agrupació** (`<div>`)

Les **divs** són contenidors genèrics utilitzats per agrupar altres elements per estil o estructura.

```html
<div class="box">
  <p>Aquest és un paràgraf dins d'un div.</p>
</div>
```

#### 9. **Etiqueta `<img>` per inserir imatges**

L'etiqueta `<img>` s'utilitza per inserir imatges en una pàgina web. És una etiqueta auto-tancada, el que significa que no necessita una etiqueta de tancament. Els atributs més comuns per a aquesta etiqueta són `src`, `alt`, `width`, i `height`.
### Sintaxi bàsica

```html
<img src="ruta/de/la/imatge.jpg" alt="Descripció de la imatge" width="500" height="300">
```

### Atributs importants:

- **`src`**: És l'atribut més important i especifica la ruta de la imatge que es vol mostrar. Pot ser una ruta relativa o una URL.

    _Exemple:_ 
```html
    <img src="images/foto1.jpg" alt="Paisatge muntanyós"> 
```

- **`alt`**: Proporciona una descripció alternativa per a la imatge, la qual és útil si la imatge no es carrega o per a usuaris amb discapacitats visuals que utilitzen lectors de pantalla.

_Exemple:_ 
```html
    <img src="images/foto1.jpg" alt="Paisatge muntanyós amb arbres"> '
```

- **`width`** i **`height`**: Aquests atributs defineixen l'amplada i l'alçada de la imatge en píxels.

_Exemple:_
```html
    <img src="images/foto1.jpg" alt="Paisatge muntanyós" width="500" height="300"> 
```

### Exemples

1. Imatge amb ruta relativa: 
```html
<img src="imatges/logo.png" alt="Logo de l'empresa">
```

2. Imatge amb URL absoluta:

```html
<img src="https://example.com/imatges/banner.jpg" alt="Banner de la pàgina web">
```