---
dg-publish: true
---
## Objectiu: 

Actualitza les pàgines HTML que mostrin els articles proporcionats, així com la pàgina principal, utilitzant les etiquetes HTML adequades per estructurar i formatar el contingut de manera semàntica.
### Tasca 1. Actualització dels continguts dels articles

-  Actualitza les tres pàgines HTML individuals (`article1.html`, `article2.html`, `article3.html`), cada una amb el títol i el contingut d'un article específic.
- Utilitzar etiquetes HTML com `<h1>`, `<h2>`, `<p>`, `<strong>`, `<em>`, `<blockquote>`, i llistes `<ul>` o `<ol>` per formatar el contingut adequadament.

	*Exemple de com quedaria la pàgina ``article1.html``*
	![[Pasted image 20240826165922.png]]


### Tasca 2. Actualització dels continguts textuals de la pàgina 'Home' (``index.html``)

-  Actualitza la pàgina Home amb els contiguts que trovaràs a l'apartat 'Continguts' d'aquest document. La estructura principal hauria de ser com aquesta:

```html
<html lang="ca">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Glamour Camping</title>
</head>
<body>
  <header>
   Aquí tindrem la part superior de la web
  </header>
  <main>
    <section id="about"> 

    </section>
    <section id="activity">
  
    </section>
    <section id="action">

    </section>
    <section id="booking">

    </section>
    <section id="news">

    </section>
    <section id="gallery">

    </section>
  </main>

  <footer>
    Subscribe to our newletter
    Pàgina creada per: Carlos Arrebola
  </footer>
</body>
</html>

```

- Utilitza els divs que consideris necessaris per agrupar els continguts. Per exemple:
```html
	<div id="iconos">
	  <div id="autocarava">
		<img src="images/iconoAutocaravana.png" alt="icono autocaravana">
		<p>30 CAMPER SITES</p>
	  </div>
```

*El resultat de la pàgina home amb una part dels continguts de les seccions **about** i **booking** seria semblant al següent:*

![[Pasted image 20240826175742.png]]
![[Pasted image 20240826175823.png]]
![[Pasted image 20240826175857.png]]
![[Pasted image 20240826175919.png]]

### Tasca 3. Comprovació i Confirmació de Canvis:
    
- **Visualitza els canvis:** Utilitza l'entorn de GitHub Codespaces per visualitzar i provar les pàgines web en un navegador integrat.
- **Validació:** Confirma que les pàgines validen correctament.
- **Fes commit i puja els canvis:** Un cop completades les edicions, utilitza Git per fer commit dels canvis al teu repositori i puja els canvis a GitHub.
### Tasca 4. Documentació i Informes:
    
- **Documenta el teu treball:** Documenta el que has fet a l'arxiu ``readme.md`` i actualitza el repositori.

	![[Pasted image 20240826180335.png]]


## Recursos

### Continguts

#### **Article 1: 

--- 
# L'Encant d'Acampar al Costat del Llac**

Hi ha poques experiències a la vida tan tranquil·les i refrescants com **acampar al costat d'un llac**. La combinació de la natura en el seu estat més pur amb la calma de les aigües és simplement irresistible. Quan arribes al càmping i plantes la tenda a prop de la riba, la primera cosa que notes és la pau que envolta l'entorn. El lleuger onatge de l'aigua i el suau xiuxiueig del vent entre els arbres et conviden a desconnectar del món i gaudir de cada moment.

<blockquote> "La proximitat de l'aigua aporta una pau que no es troba en cap altre lloc. Despertar amb la vista del llac és una experiència que tots haurien de viure almenys una vegada." </blockquote>

Acampar al costat d'un llac no només ofereix unes vistes espectaculars, sinó que també proporciona una multitud d'activitats per gaudir. Pots començar el dia amb una refrescant banyada a primera hora del matí o fer una passejada amb caiac mentre el sol surt per l'horitzó. La **pesca** és una altra activitat popular, on pots provar la teva sort i capturar el sopar del dia. A la nit, encén una foguera i gaudeix d'un sopar a l'aire lliure mentre el sol es pon sobre les aigües tranquil·les del llac.

<em>Acampar al costat d'un llac també és ideal per a les famílies</em>. Els nens poden passar hores jugant a la vora de l'aigua, construint castells de sorra o buscant pedres especials. La proximitat a l'aigua també afegeix una dimensió única a l'experiència de càmping, fent que sigui més relaxant i oferint moltes oportunitats per connectar amb la natura.

Per aquells que busquen una experiència de càmping autèntica però còmoda, els càmpings a la vora del llac són l'elecció perfecta. La combinació de la **bellesa natural** amb la serenitat de l'aigua crea un entorn incomparable, ideal per a aquells que volen desconnectar i gaudir de la natura en estat pur.

---

#### **Article 2: 
---
# Glamping: Una Nova Manera de Gaudir de la Natura**

El **<strong>glamping</strong>** (glamour + camping) és la tendència més recent en el món del turisme de natura, oferint una combinació única entre el luxe d'un hotel i l'experiència d'acampar a l'aire lliure. Aquesta forma d'acampada permet gaudir de tots els avantatges de la natura, sense renunciar a les comoditats modernes.

Si sempre t'ha atret l'idea d'acampar però t'intimiden les incomoditats associades amb el càmping tradicional, el glamping és la solució perfecta. Les tendes de glamping solen estar equipades amb **<em>llits còmodes</em>**, electricitat, banys privats i fins i tot cuines equipades. Això significa que pots gaudir de les estrelles a la nit i despertar-te amb els sons de la natura, però sense sacrificar el confort.

Una altra de les avantatges del glamping és la seva ubicació. Moltes destinacions de glamping estan situades en llocs espectaculars, com parcs nacionals, muntanyes, deserts i, per descomptat, a la vora de llacs. Aquestes ubicacions privilegiades permeten als hostes gaudir de la **<strong>bellesa natural</strong>** sense la necessitat d'equipament complex o experiència prèvia en càmping.

<blockquote> "El glamping ofereix una manera més sostenible de viatjar, utilitzant materials ecològics i dissenys amb un impacte mínim sobre el medi ambient." </blockquote>

En resum, el glamping és la manera ideal de combinar la comoditat amb l'aventura. És perfecte per a parelles que busquen una escapada romàntica, famílies que volen experimentar la natura sense renunciar al confort, o per a qualsevol que desitgi una experiència única a l'aire lliure sense les complicacions del càmping tradicional.

---

#### **Article 3:**
___
# **Els Millors Destins per Gaudir del Glamping amb Estil**

El **glamping** ha esdevingut una de les maneres més populars de connectar amb la natura sense renunciar a les comoditats modernes. Però no tots els destins de glamping són iguals; hi ha llocs que porten aquesta experiència al següent nivell, oferint una fusió perfecta entre luxe i natura. Aquí et presentem alguns dels millors destins per gaudir del glamping amb estil.

<ul> <li><strong>El Montseny, Catalunya:</strong> Conegut per les seves muntanyes verdes i boscos frondosos, el Montseny ofereix una experiència de glamping incomparable. Envoltats de natura exuberant, les tendes de glamping en aquesta zona estan equipades amb totes les comoditats, des de llits king-size fins a banyeres exteriors amb vistes espectaculars. És el lloc perfecte per desconnectar i gaudir de la tranquil·litat.</li> <li><strong>El Delta de l’Ebre:</strong> Aquest paradís natural és ideal per als amants de la biodiversitat. Aquí, el glamping permet gaudir de la rica fauna i flora del Delta sense perdre confort. Pots passar el dia explorant els canals amb bicicleta o en caiac, i tornar a la teva tenda de glamping per gaudir d'un sopar preparat amb productes locals mentre el sol es pon sobre les aigües tranquil·les.</li> <li><strong>Els Pirineus:</strong> Si ets un amant de les muntanyes, els Pirineus són una destinació imprescindible. Aquí trobaràs opcions de glamping que combinen la proximitat a rutes de senderisme impressionants amb allotjaments de luxe. Després d’un dia d’aventures, podràs relaxar-te en una tenda equipada amb totes les comoditats modernes, incloent calefacció per les nits fredes de muntanya.</li> <li><strong>La Costa Brava:</strong> Per aquells que volen gaudir del mar, la Costa Brava ofereix una experiència de glamping única. Amb tendes situades a pocs passos de platges de sorra fina, podràs gaudir d'unes vacances al costat del mar amb tot el luxe d’un hotel de cinc estrelles. Des de veure la sortida del sol des de la teva tenda fins a gaudir de menjars gourmet preparats amb ingredients locals, el glamping a la Costa Brava és una experiència inoblidable.</li> </ul>

El glamping és molt més que una simple tendència; és una nova manera de viatjar que combina l'amor per la natura amb les comoditats de la vida moderna. Si busques una experiència de vacances que ofereixi el millor dels dos mons, aquests destins de glamping amb estil són l'opció perfecta.

---

## Resum de conceptes HTML per estructurar i formatar pàgines web de manera semàntica

HTML proporciona etiquetes semàntiques que ajuden a estructurar el contingut d'una manera clara i comprensible, tant per a usuaris com per a motors de cerca. A continuació s'explica com utilitzar algunes de les etiquetes més comunes...

#### 1. **Estructura bàsica d'una pàgina HTML**

L'estructura típica d'una pàgina HTML comença amb la declaració del tipus de document i es divideix en dues parts principals: `<head>` i `<body>`.

```html
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