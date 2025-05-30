## Resum de Conceptes bàsics CSS 

### **Formes d'aplicar estils en un document web**

1. **Estils en línia (inline styles)**:
    
    - S'apliquen directament a les etiquetes HTML utilitzant l'atribut `style`.
    - Exemple: `<p style="color: red;">Text en vermell</p>`.
    - Són útils per estils molt específics, però es recomana no abusar-ne perquè fan el codi més difícil de mantenir.
2. **Fulls d'estil interns (internal styles)**:
    
    - S'inclouen dins de l'element `<style>` a la capçalera (`<head>`) de l'HTML.
    - Exemple:   
        `<style>   p { color: blue; } </style>`
    - Són útils per pàgines petites o quan només s'apliquen estils a un únic document.
3. **Fulls d'estil externs (external styles)**:
    
    - S'escriuen en un fitxer CSS separat i es vinculen amb l'HTML mitjançant l'etiqueta `<link>`.
    - Exemple:
		`<link rel="stylesheet" href="styles.css">`
    - Són els més recomanats, ja que permeten reutilitzar els estils en múltiples pàgines i faciliten la seva organització i manteniment.

---

### **Tipus de selectors CSS**

1. **Selectors per etiquetes (type selectors)**:
    - Seleccionen tots els elements d'un tipus específic (per exemple, totes les etiquetes `<p>`).
    - Exemple: `p { color: blue; }` (canvia el color de tots els paràgrafs).
2. **Selectors de classe (class selectors)**:
    - Seleccionen elements que tenen una classe assignada.
    - Exemple: `.classe { color: red; }` (aplica aquest estil als elements amb la classe "classe").
3. **Selectors d'identificador (ID selectors)**:
    - Seleccionen elements amb un identificador únic (ID) especificat.
    - Exemple: `#idUnic { font-size: 20px; }` (canvia la mida de lletra de l'element amb aquest ID).
4. **Selectors universals**:
    - Seleccionen tots els elements del document.
    - Exemple: `* { margin: 0; padding: 0; }` (aplica aquests estils a tots els elements).
5. **Selectors combinats**:
    - Es poden combinar selectors per fer seleccions més específiques.
    - Exemple: `div p { color: green; }` (selecciona tots els paràgrafs dins d'un `div`).
6. **Pseudo-selectors**:
    - Seleccionen elements en un estat específic, com ara quan l'usuari passa el cursor per sobre d'ells.
    - Exemple: `a:hover { color: red; }` (canvia el color dels enllaços quan el cursor hi passa per sobre).

---

### **Explicació dels selectors i estils del codi**

1. **Selector `body`**: Aplica estils globals a tot el document, com el color de text, la font principal i el pes de la lletra. Aquest selector es refereix a l'element principal que conté tot el contingut visible de la pàgina.
    
2. **Selector `.titolArticle` (classe)**: S'utilitza per estilitzar els títols dels articles, aplicant un color verd, una vora inferior i centrant el text. Aquest selector s'aplicarà a qualsevol element amb la classe `titolArticle`.
    
3. **Selector `.citas` (classe)**: Defineix els estils per a blocs de text destacats, aplicant un fons clar, una vora amb transparència parcial i arrodonint les cantonades. S'aplicarà als elements amb la classe `citas`.
    
4. **Selector per a `header`, `main` i `footer` (etiquetes)**: Aplica un color de fons aquamarina i un marge extern per ajudar a visualitzar la separació d'aquests tres elements dins de la pàgina.
    
5. **Selector `div` (etiqueta)**: Assigna una vora sòlida de color gris i un marge extern a tots els elements `div`, permetent que tots els contenidors `div` dins de la pàgina estiguin clarament delimitats.
    
6. **Selector `#cards` (ID)**: Aplica un color de fons verd fosc a l'element amb l'identificador `cards`, destacant aquest element específic.
    
7. **Selector `.targetes` (classe)**: Defineix un color de fons semitransparent verd clar per als elements amb la classe `targetes`, aplicant un to suau que destaca visualment però amb certa transparència.
    
8. **Selector `section` (etiqueta)**: Aplica un color de fons "cornflowerblue" i un marge extern als elements `section`, ajudant a identificar visualment les diferents seccions de la pàgina.
    
9. **Selector `article` (etiqueta)**: Defineix una vora sòlida de color blau i un marge extern per als elements `article`, per separar clarament aquests blocs de contingut dins del document.

### **Propietats CSS i la seva funció**

1. **`color`**: Defineix el color del text dins de l'element seleccionat. Exemple del teu codi: `color: #2D2D2D;`. El color es defineix mitjançant un codi hexadecimal. En aquest cas, `#2D2D2D` és un gris fosc.
    
2. **`background-color`**: Estableix el color de fons d'un element. Exemple: `background-color: aquamarine;` Utilitza un nom de color predefinit ("aquamarine") o pot utilitzar un codi hexadecimal o `rgba` per definir colors personalitzats. Un altre exemple: `background-color: #F7F2DB;` Aquí s'utilitza un codi hexadecimal (`#F7F2DB`), que defineix un to clar groguenc.
    
3. **`font-family`**: Defineix el tipus de lletra (font) que s’utilitzarà en l’element. Exemple: `font-family: "Inter", sans-serif;` Es selecciona la font "Inter" i, si aquesta no està disponible, es farà servir una font de tipus sans-serif per defecte.
    
4. **`font-optical-sizing`**: Ajusta automàticament la mida òptica de la font per millorar la llegibilitat en diferents mides. Exemple: `font-optical-sizing: auto;`
    
5. **`font-weight`**: Defineix el gruix del text. Els valors més baixos com `100` indiquen un text més fi, mentre que els més alts indiquen un text més gruixut. Exemple: `font-weight: 100;`
    
6. **`font-style`**: Defineix si el text és normal o en cursiva. Exemple: `font-style: normal;`
    
7. **`border`**: Estableix les propietats de la vora de l'element, incloent el gruix, el tipus de línia i el color. Exemple: `border: 1px solid grey;` Crea una vora d'1 píxel de gruix, sòlida i de color gris. Un altre exemple: `border-bottom: 2px solid #97A483;` Afegeix una vora a la part inferior de l'element amb un gruix de 2 píxels i un color verd (`#97A483`).
    
8. **`border-radius`**: Arrodoneix les cantonades d’un element. Exemple: `border-radius: 10px;` Les cantonades de l'element es faran arrodonides amb un radi de 10 píxels.
    
9. **`padding`**: Defineix l’espai intern (interior) entre el contingut d’un element i la seva vora. Exemple: `padding: 20px;` Aplica un espai de 20 píxels dins de l’element. En un altre cas: `padding: 10px 0;` Aplica un espaiat vertical de 10 píxels a la part superior i inferior de l'element.
    
10. **`margin`**: Defineix l’espai extern (fora) entre l'element i altres elements adjacents. Exemple: `margin: 10px;` Aplica un marge de 10 píxels a tots els costats de l'element.
    
11. **`text-align`**: Controla l'alineació horitzontal del contingut dins d'un element. Exemple: `text-align: center;` Alinea el text al centre de l’element.
    

### **Tipus de codis de colors utilitzats**

1. **Codi hexadecimal**: Format: `#RRGGBB` on `RR`, `GG` i `BB` són valors hexadecimals per als colors vermell, verd i blau respectivament. Exemple: `#2D2D2D` és un gris fosc.
    
2. **Noms de colors**: Alguns colors tenen noms predefinits. Exemple: `aquamarine` és un color verd blavós clar.
    
3. **`rgba()`**: Format: `rgba(red, green, blue, alpha)` on `alpha` és el nivell de transparència (de 0 a 1). Exemple: `rgba(120, 200, 12, 0.5);` Aplica un color verd clar amb una opacitat del 50%.
