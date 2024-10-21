---
dg-publish: true
---
[[M0373 - Projecte 1 'Glamour Camping']]
## **Objectiu:** 
Configurar un entorn de desenvolupament utilitzant GitHub Codespaces i començar a treballar en el projecte web, creant les tres pàgines HTML segons els requisits definits.
## Tasques:

### Tasca 1. Configuració de GitHub Codespaces:
- **Accedeix a GitHub Codespaces:** 
	- Inicia sessió a GitHub i obre el teu repositori o crea'n un nou amb nom ``daw1-apellido-apellido-nombre-glamourcamping``. 
	
	-![[Pasted image 20240826160812.png]]
	
	- Després, accedeix a la secció de "Codespaces" i crea un nou Codespace per al teu repositori.
	![[Pasted image 20240826161003.png]]

- **Configura l'entorn de treball:** 
	- Assegura't que GitHub Codespaces estigui configurat amb les eines necessàries, com Visual Studio Code, per treballar amb arxius HTML i CSS. 
	- Verifica que la configuració inclogui les extensions recomanades per a HTML i CSS.
	![[Pasted image 20240826161246.png]]
### Tasca 2. Creació del Repositori i Configuració Inicial:
 
 - **Configura l'estructura de fitxers:** Crea els fitxers inicials necessaris dins del repositori, incloent `index.html` i una carpeta ``articles`` amb els fitxers `article1.html`, `article2.html`, i `article3.html`. Assegura't de seguir les convencions de nomenclatura i estructura establertes.
### Tasca 3. Desenvolupament:
    
- **Desenvolupa la pàgina principal:** Treballa en la creació de `index.html` amb una estructura bàsica (``html``, ``head``, ``body``, ``header``, ``main``, ``footer``)
- **Desenvolupa les pàgines d'articles:** Implementa els fitxers `article1.html`, `article2.html`, i `article3.html` amb una estructura bàsica.

*Exemple codi index.html*

```html
<!DOCTYPE html>
<html lang="ca">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Glamour Camping</title>
</head>
<body>
  <header>
    Glamour Camping
  </header>
  <main>
    <h1>Pàgina home</h1>
    <nav>
      <a href="articles/article1.html">article1</a>
      <a href="articles/article2.html">article2</a>
      <a href="articles/article3.html">article3</a>
   </nav>
  </main>
  <footer>
    Pàgina creada per: Carlos Arrebola
  </footer>
</body>
</html>>
```

### Tasca 4. Comprovació i Confirmació de Canvis:
    
- **Visualitza els canvis:** Utilitza l'entorn de GitHub Codespaces per visualitzar i provar les pàgines web en un navegador integrat. Pots fer servir el **LiveServer**

	*Resultat de la pàgina index.html:*	
	
	![[Pasted image 20240826165659.png]]

- **Fes commit i puja els canvis:** Un cop completades les edicions, utilitza Git per fer commit dels canvis al teu repositori i puja els canvis a GitHub.

	![[Pasted image 20240826162813.png]]
### Tasca 5. Documentació i Informes:
    
- **Documenta el teu treball:** Documenta el que has fet a l'arxiu ``readme.md`` i torna a actualitzar el teu repositori. (Has de fer servir **Markdown**)
- **Comprova el teu repositori desde la pàgina web de GitHub**

	![[Pasted image 20240826163359.png]]

- **Comparteix el repositori:** Assegura't que el repositori estigui accessible per al professor.

	![[Pasted image 20240826163600.png]]

## **Recursos:**

### Git

- **Què és?**: Un sistema de control de versions que permet fer un seguiment dels canvis en fitxers i col·laborar amb altres persones.
- **Per què utilitzar-ho?**: Permet gestionar projectes de manera eficient, guardar diferents versions del codi, i treballar en equip sense conflictes.

### GitHub

- **Què és?**: Una plataforma en línia que utilitza Git per emmagatzemar i gestionar repositoris de codi.
- **Funcionalitats clau**:
    - **Repositoris**: Emmagatzema el codi i l'historial de canvis.
    - **Pull requests**: Permet revisar i integrar canvis d'altres desenvolupadors.
    - **Issues**: Ajuda a gestionar tasques i errors en el projecte.

### GitHub Codespaces

- **Què és?**: Un entorn de desenvolupament basat en el núvol.
- **Per què utilitzar-ho?**: Permet començar a codificar immediatament sense configurar res al teu ordinador. Tot està preparat per tu!

### Visual Studio Code (VSCode)

- **Què és?**: Un editor de codi molt popular i gratuït.
- **Funcionalitats clau**:
    - **Extensible**: Permet instal·lar extensions per millorar la funcionalitat.
    - **Integració amb Git**: Permet fer canvis al codi, gestionar repositoris i fer commits directament des de l'editor.

### Resum de l'ús

1. **Instal·la Git** i configura el teu entorn local.
2. **Crea un repositori a GitHub** per al teu projecte.
3. **Fes servir Git** per fer commits dels teus canvis i pujar-los a GitHub.
4. **Utilitza GitHub Codespaces** si vols començar ràpidament en un entorn preconfigurat.
5. **Crea i edita codi amb VSCode**, aprofitant les seves funcionalitats per facilitar la programació.

Aquestes eines són fonamentals per al treball en equip i el desenvolupament de software, així que és útil familiaritzar-se amb elles! Si vols més detalls sobre cadascuna, pots consultar [Git](https://git-scm.com), [GitHub](https://github.com), [GitHub Codespaces](https://github.com/features/codespaces) i [Visual Studio Code](https://code.visualstudio.com).