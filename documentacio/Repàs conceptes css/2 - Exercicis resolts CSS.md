# Exercicis Complets CSS3 - Enunciat i Resolució

Aquests exercicis cobreixen aspectes essencials de CSS3 per a la pràctica de DAW1.

## Índex

- [Exercicis Complets CSS3 - Enunciat i Resolució](#exercicis-complets-css3---enunciat-i-resolució)
  - [Índex](#índex)
  - [Exercicis de Colors i Fons](#exercicis-de-colors-i-fons)
    - [Exercici 1: Color de Fons Hexadecimal](#exercici-1-color-de-fons-hexadecimal)
    - [Exercici 2: Color de Fons RGB](#exercici-2-color-de-fons-rgb)
    - [Exercici 3: Color de Fons RGBA](#exercici-3-color-de-fons-rgba)
    - [Exercici 4: Gradient Horitzontal](#exercici-4-gradient-horitzontal)
    - [Exercici 5: Gradient Radial](#exercici-5-gradient-radial)
    - [Exercici 6: Fons amb Imatge](#exercici-6-fons-amb-imatge)
    - [Exercici 7: Imatge i Color de Fons](#exercici-7-imatge-i-color-de-fons)
  - [Exercicis de Fonts i Tipografia](#exercicis-de-fonts-i-tipografia)
    - [Exercici 8: Fonts de Google Fonts](#exercici-8-fonts-de-google-fonts)
    - [Exercici 9: Text Italic i Bold](#exercici-9-text-italic-i-bold)
    - [Exercici 10: Subratllat i Ratllat](#exercici-10-subratllat-i-ratllat)
    - [Exercici 11: Ombra de Text](#exercici-11-ombra-de-text)
    - [Exercici 12: Text en Majúscules](#exercici-12-text-en-majúscules)
  - [Exercicis del Model de Caixes (Box Model)](#exercicis-del-model-de-caixes-box-model)
    - [Exercici 13: Bord i Radi de Bord](#exercici-13-bord-i-radi-de-bord)
    - [Exercici 14: Esquines Rodones Completes](#exercici-14-esquines-rodones-completes)
    - [Exercici 15: Ombra de Caixa](#exercici-15-ombra-de-caixa)
    - [Exercici 16: Box-Sizing](#exercici-16-box-sizing)
    - [Exercici 17: Margin i Padding](#exercici-17-margin-i-padding)
  - [Exercicis de Display i Alineació](#exercicis-de-display-i-alineació)
    - [Exercici 18: Display Inline i Block](#exercici-18-display-inline-i-block)
    - [Exercici 19: Posicionament Relatiu i Absolut](#exercici-19-posicionament-relatiu-i-absolut)
    - [Exercici 20: Centrat amb Flexbox](#exercici-20-centrat-amb-flexbox)
    - [Exercici 21: Direcció de Columna en Flexbox](#exercici-21-direcció-de-columna-en-flexbox)

## Exercicis de Colors i Fons

### Exercici 1: Color de Fons Hexadecimal
Descripció: Aplica un color de fons utilitzant un codi hexadecimal.

```html
<div class="ex1">Color de Fons Hexadecimal</div>
```
```css
.ex1 {
  width: 200px;
  height: 200px;
  background-color: #FFD700;
}
```

### Exercici 2: Color de Fons RGB
Descripció: Aplica un color de fons en format RGB.

```html
<div class="ex2">Color de Fons RGB</div>
```
```css
.ex2 {
  width: 200px;
  height: 200px;
  background-color: rgb(173, 216, 230);
}
```

### Exercici 3: Color de Fons RGBA
Descripció: Aplica un color de fons semi-transparent amb RGBA.

```html
<div class="ex3">Color de Fons RGBA</div>
```
```css
.ex3 {
  width: 200px;
  height: 200px;
  background-color: rgba(0, 128, 128, 0.5);
}
```

### Exercici 4: Gradient Horitzontal
Descripció: Aplica un gradient horitzontal entre dos colors.

```html
<div class="ex4">Gradient Horitzontal</div>
```
```css
.ex4 {
  width: 200px;
  height: 200px;
  background: linear-gradient(to right, #FF6347, #4682B4);
}
```

### Exercici 5: Gradient Radial
Descripció: Aplica un gradient radial circular.

```html
<div class="ex5">Gradient Radial</div>
```
```css
.ex5 {
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, #FF69B4, #8A2BE2);
}
```

### Exercici 6: Fons amb Imatge
Descripció: Aplica una imatge de fons que cobreixi tota la caixa.

```html
<div class="ex6">Imatge de Fons</div>
```
```css
.ex6 {
  width: 300px;
  height: 150px;
  background-image: url('https://via.placeholder.com/300x150');
  background-size: cover;
}
```

### Exercici 7: Imatge i Color de Fons
Descripció: Aplica un color de fons i una imatge de fons superposada amb lleugera transparència.

```html
<div class="ex7">Imatge i Color de Fons</div>
```
```css
.ex7 {
  width: 300px;
  height: 150px;
  background-color: rgba(0, 0, 0, 0.3);
  background-image: url('https://via.placeholder.com/300x150');
  background-blend-mode: overlay;
  background-size: cover;
}
```

## Exercicis de Fonts i Tipografia

### Exercici 8: Fonts de Google Fonts
Descripció: Importa una font de Google Fonts i aplica-la a un text.

```html
<div class="ex8">Font de Google Fonts</div>
```
```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap');

.ex8 {
  font-family: 'Roboto', sans-serif;
  font-size: 24px;
  color: #FF4500;
}
```

### Exercici 9: Text Italic i Bold
Descripció: Aplica estils italic i bold a un text.

```html
<div class="ex9">Text en Italic i Bold</div>
```
```css
.ex9 {
  font-style: italic;
  font-weight: bold;
}
```

### Exercici 10: Subratllat i Ratllat
Descripció: Aplica subratllat i ratllat a diferents textos.

```html
<div class="ex10 underline">Text Subratllat</div>
<div class="ex10 line-through">Text Ratllat</div>
```
```css
.ex10.underline {
  text-decoration: underline;
}
.ex10.line-through {
  text-decoration: line-through;
}
```

### Exercici 11: Ombra de Text
Descripció: Aplica una ombra al text.

```html
<div class="ex11">Text amb Ombra</div>
```
```css
.ex11 {
  font-size: 24px;
  color: #333;
  text-shadow: 2px 2px 4px #000;
}
```

### Exercici 12: Text en Majúscules
Descripció: Converteix un text a majúscules.

```html
<div class="ex12">Text en Majúscules</div>
```
```css
.ex12 {
  text-transform: uppercase;
  font-size: 20px;
  color: #4682B4;
}
```

## Exercicis del Model de Caixes (Box Model)

### Exercici 13: Bord i Radi de Bord
Descripció: Aplica un bord i un radi de bord.

```html
<div class="ex13">Bord i Radi de Bord</div>
```
```css
.ex13 {
  width: 150px;
  height: 150px;
  border: 2px solid #333;
  border-radius: 10px;
  padding: 10px;
}
```

### Exercici 14: Esquines Rodones Completes
Descripció: Crea una forma circular amb `border-radius: 50%`.

```html
<div class="ex14">Esquines Rodones</div>
```
```css
.ex14 {
  width: 100px;
  height: 100px;
  background-color: #FF6347;
  border-radius: 50%;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### Exercici 15: Ombra de Caixa
Descripció: Aplica una ombra a un div.

```html
<div class="ex15">Ombra de Caixa</div>
```
```css
.ex15 {
  width: 200px;
  height: 100px;
  background-color: #4682B4;
  box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.5);
  color: white;
  padding: 10px;
}
```

### Exercici 16: Box-Sizing
Descripció: Aplica `box-sizing: border-box` a un div.

```html
<div class="ex16">Box-Sizing Border Box</div>
```
```css
.ex16 {
  width: 200px;
  height: 100px;
  padding: 20px;
  border: 5px solid #333;
  box-sizing: border-box;
  background-color: #FFDAB9;
}
```

### Exercici 17: Margin i Padding
Descripció: Aplica marges i padding a un div per observar l’espai interior i exterior.

```html
<div class="ex17">Margin i Padding</div>
```
```css
.ex17 {
  width: 200px;
  height: 100px;
  margin: 20px;
  padding: 20px;
  background-color: #B0E0E6;
}
```

## Exercicis de Display i Alineació

### Exercici 18: Display Inline i Block
Descripció: Aplica `display: inline` i `display: block` a dos elements diferents.

```html
<span class="ex18 inline">Element Inline</span>
<div class="ex18 block">Element Block</div>
```
```css
.ex18.inline {
  display: inline;
  background-color: #4682B4;
  color: #fff;
  padding: 10px;
}
.ex18.block {
  display: block;
  background-color: #87CEEB;
  color: #333;
  padding: 10px;
  margin-top: 10px;
}
```

### Exercici 19: Posicionament Relatiu i Absolut
Descripció: Crea un contenidor amb `position: relative` i un fill amb `position: absolute`.

```html
<div class="ex19 container">
  Contenidor
  <div class="ex19 absolute">Element Absolut</div>
</div>
```
```css
.ex19.container {
  width: 200px;
  height: 200px;
  background-color: #FF6347;
  position: relative;
}
.ex19.absolute {
  width: 100px;
  height: 100px;
  background-color: #4682B4;
  color: white;
  position: absolute;
  top: 20px;
  left: 20px;
}
```

### Exercici 20: Centrat amb Flexbox
Descripció: Utilitza Flexbox per centrar un element dins d’un contenidor.

```html
<div class="ex20 container">
  <div class="ex20 centered">Element Centrat</div>
</div>
```
```css
.ex20.container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 300px;
  height: 200px;
  background-color: #FFEFD5;
}
.ex20.centered {
  background-color: #4682B4;
  color: white;
  padding: 10px;
}
```

### Exercici 21: Direcció de Columna en Flexbox
Descripció: Organitza elements en una columna amb Flexbox.

```html
<div class="ex21 flex-column">
  <div>Element 1</div>
  <div>Element 2</div>
  <div>Element 3</div>
</div>
```
```css
.ex21.flex-column {
  display: flex;
  flex-direction: column;
  gap: 10px;
  background-color: #E6E6FA;
  padding: 20px;
}
```
