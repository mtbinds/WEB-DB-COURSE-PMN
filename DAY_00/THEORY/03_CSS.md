# Partie 04 - Feuilles de styles (CSS)

## 1. Introduction

**CSS (Cascading Style Sheets)**, ou feuilles de style en cascade, est un langage de style utilisé pour décrire la présentation d'un document ***HTML***. ***CSS*** permet de contrôler l'apparence des éléments sur une page web, y compris leur disposition, leurs couleurs, leurs polices, et bien plus encore. En séparant le contenu de sa présentation, CSS facilite la maintenance et l'amélioration de l'expérience utilisateur.

## 2. Pourquoi utiliser CSS ?

### Avantages de CSS :

- **Séparation du contenu et de la présentation** : Permet de gérer le style de manière centralisée, facilitant ainsi la maintenance.
- **Amélioration de la vitesse de chargement** : Les fichiers CSS externes sont souvent plus légers que le code HTML.
- **Consistance** : Applique des styles uniformes à plusieurs pages en utilisant une seule feuille de style.
- **Accessibilité** : Améliore l’accessibilité des sites web en permettant aux utilisateurs de personnaliser l’apparence selon leurs besoins.
- **Réactivité** : Permet de créer des designs réactifs qui s'adaptent à différentes tailles d'écran.

## 3. Syntaxe de CSS

La syntaxe CSS est composée de **sélecteurs** et de **règles**.

### Structure de base

```css
sélecteur {
  propriété: valeur;
}
```

- **Exemple :**

```css
h1 {
  color: blue; /* Change la couleur du texte en bleu */
  font-size: 24px; /* Définit la taille de police à 24 pixels */
}
```
## 4. Sélecteurs

Les sélecteurs permettent de cibler des éléments HTML spécifiques pour appliquer des styles. Voici une liste détaillée des types de sélecteurs courants :

### 4.1 Sélecteurs d'éléments

Ciblent tous les éléments d'un type donné.

```css
p {
  color: red; /* Tous les paragraphes en rouge */
}
```
### 4.2 Sélecteurs de classe

Ciblent les éléments ayant une classe spécifique, précédé d'un point ..

```css
.important {
  font-weight: bold; /* Tous les éléments avec la classe 'important' en gras */
}
```
### 4.3 Sélecteurs d'identifiant

Ciblent un élément ayant un identifiant spécifique, précédé d’un ***#***.

```css
#header {
  background-color: gray; /* L'élément avec l'ID 'header' a un fond gris */
}
```
### 4.4 Sélecteurs combinés

Ciblent les éléments en fonction de leur relation hiérarchique.

```css
div p {
  color: green; /* Tous les paragraphes à l'intérieur des div en vert */
}
```
### 4.5 Sélecteurs d'attributs

Ciblent des éléments en fonction de la présence d'un attribut.

```css
a[target="_blank"] {
  color: orange; /* Les liens qui ouvrent dans un nouvel onglet en orange */
}
```
### 4.6 Sélecteurs pseudo-classes

Appliquent des styles à des éléments dans un état particulier.

```css
a:hover {
  text-decoration: underline; /* Sousligne les liens au survol */
}
```
### 4.7 Sélecteurs pseudo-éléments

Ciblent une partie spécifique d'un élément.

```css
p::first-line {
  font-weight: bold; /* Met en gras la première ligne des paragraphes */
}
```
### 4.8 Sélecteurs universels

Ciblent tous les éléments d'une page.

```css
* {
  margin: 0; /* Réinitialise la marge de tous les éléments */
}
```
## 5. Propriétés CSS

### 5.1 Couleurs et fonds

- Couleur de texte :

```css
p {
  color: blue; /* Change la couleur du texte en bleu */
}
```
- Couleur de fond :

```css
body {
  background-color: lightgrey; /* Change la couleur de fond du body en gris clair */
}
```
- Image de fond :

```css
body {
  background-image: url('background.jpg'); /* Définit une image de fond */
  background-size: cover; /* Couvre tout l'élément */
}
```
### 5.2 Typographie

- Taille de police :

```css
h1 {
  font-size: 36px; /* Définit la taille de la police du h1 */
}
```
- Style de police :

```css
h2 {
  font-style: italic; /* Définit le texte en italique */
}
```

- Poids de la police :

```css
p {
  font-weight: bold; /* Définit le texte en gras */
}
```
- Famille de police :

```css
body {
  font-family: 'Arial', sans-serif; /* Définit la famille de police */
}
```
### 5.3 Mise en page

- Marge et remplissage :

```css
div {
  margin: 20px; /* Définit une marge de 20 pixels autour du div */
  padding: 10px; /* Définit un remplissage de 10 pixels à l'intérieur du div */
}
```
- Largeur et hauteur :

```css
img {
  width: 100%; /* Définit l'image pour qu'elle occupe toute la largeur de son conteneur */
  height: auto; /* Maintient le rapport d'aspect de l'image */
}
```
### 5.4 Boîte CSS

Le modèle de boîte CSS décrit comment les éléments sont organisés et espacés sur la page. Chaque élément a une boîte composée de :

- **Contenu :** L’élément lui-même (texte, image, etc.).
- **Remplissage (padding) :** L’espace entre le contenu et la bordure.
- **Bordure (border) :** La ligne entourant l'élément.
- **Marge (margin) :** L’espace extérieur entre la bordure de l'élément et les autres éléments.

- **Exemple de boîte :**

```css
.box {
  margin: 20px; /* Marge extérieure */
  padding: 10px; /* Remplissage intérieur */
  border: 2px solid black; /* Bordure noire de 2 pixels */
}
```
## 6. Positionnement

Le positionnement permet de contrôler l'emplacement d'un élément sur la page.

### 6.1 Position statique

C'est la valeur par défaut. Les éléments sont placés selon l'ordre normal du document.

### 6.2 Position relative

L'élément est positionné par rapport à sa position d'origine.

```css
.relative {
  position: relative;
  top: 10px; /* Déplace l'élément de 10 pixels vers le bas */
}
```
### 6.3 Position absolue

L'élément est positionné par rapport à son ancêtre le plus proche qui n'est pas statique.

```css
.absolute {
  position: absolute;
  right: 0; /* Place l'élément en bas à droite */
}
```
### 6.4 Position fixe

L'élément est fixé à une position dans la fenêtre du navigateur, même lors du défilement.

```css
.fixed {
  position: fixed;
  bottom: 0; /* Place l'élément en bas de la fenêtre */
}
```
### 6.5 Position collante

L'élément est traité comme positionné relativement jusqu'à ce qu'il atteigne une position spécifique lors du défilement.

```css
.sticky {
  position: sticky;
  top: 0; /* L'élément reste en haut lorsqu'il est atteint lors du défilement */
}
```
## 7. Flexbox et Grid

### 7.1 Flexbox

Flexbox est un modèle de mise en page qui permet de disposer des éléments en ligne ou en colonne. Il facilite l'alignement et la distribution de l'espace.

- **Exemple de Flexbox :**
  
```css
.container {
  display: flex; /* Active le modèle Flexbox */
  justify-content: space-between; /* Distribue l'espace entre les éléments */
  align-items: center; /* Aligne les éléments au centre verticalement */
}
```
### 7.2 Grid

Grid est un autre modèle de mise en page qui permet de créer des grilles complexes en définissant des lignes et des colonnes.

- **Exemple de Grid :**

```css
.grid {
  display: grid; /* Active le modèle Grid */
  grid-template-columns: repeat(3, 1fr); /* Crée 3 colonnes de taille égale */
  grid-gap: 10px; /* Espacement entre les colonnes et les lignes */
}
```
### 7.3 Exemples de mise en page avec Flexbox et Grid

- **Exemples Flexbox :**
  
```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>
```
```css
.container {
  display: flex;
}

.item {
  flex: 1; /* Chaque élément prend une part égale de l'espace */
  margin: 5px; /* Marge entre les éléments */
  background-color: lightcoral; /* Couleur de fond des éléments */
  text-align: center; /* Centrer le texte */
  padding: 20px; /* Remplissage des éléments */
}
```
- **Exemples Grid :**

```html
<div class="grid">
  <div class="grid-item">1</div>
  <div class="grid-item">2</div>
  <div class="grid-item">3</div>
  <div class="grid-item">4</div>
</div>
```
```css
.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr); /* Deux colonnes */
  gap: 10px; /* Espacement entre les éléments */
}

.grid-item {
  background-color: lightblue; /* Couleur de fond des éléments */
  padding: 20px; /* Remplissage des éléments */
  text-align: center; /* Centrer le texte */
}
```
## 8. Liens vers des feuilles de style

Il existe plusieurs façons d'intégrer CSS dans un document HTML :

### 8.1 Styles inline

Appliquent des styles directement sur un élément HTML à l'aide de l'attribut style.

```html
<h1 style="color: red;">Titre rouge</h1>
```
### 8.2 Styles internes

Définissent des styles dans une section `<style>` de l'élément <head>.

```html
<head>
  <style>
    body {
      background-color: lightblue; /* Change la couleur de fond */
    }
  </style>
</head>
```
### 8.3 Styles externes

Les feuilles de style externes sont des fichiers CSS séparés, liés à l'aide de la balise `<link>`.

```html
<head>
  <link rel="stylesheet" href="styles.css"> <!-- Lien vers le fichier CSS -->
</head>
```
## 9. Media Queries

Les media queries permettent d'appliquer des styles différents selon la taille de l'écran ou d'autres conditions. Cela est particulièrement utile pour créer des designs réactifs.

- **Exemple de media query :**
  
```css
@media (max-width: 600px) {
  body {
    background-color: lightyellow; /* Change la couleur de fond sur les petits écrans */
  }

  .grid {
    grid-template-columns: 1fr; /* Une seule colonne sur petits écrans */
  }
}
```
## 10.  Transitions et animations

### 10.1 Transitions

Les transitions permettent de créer des effets de changement doux lors du passage d'un état à un autre.

- **Exemple de transition :**
  
```css
.button {
  background-color: blue;
  transition: background-color 0.3s ease; /* Transition de couleur en 0.3 seconde */
}

.button:hover {
  background-color: red; /* Change la couleur au survol */
}
```
### 10.2 Animations

Les animations permettent de créer des mouvements complexes en définissant des étapes clés.

- **Exemple d'animation :**

```css
@keyframes slide {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(100px); /* Déplace l'élément de 100 pixels vers la droite */
  }
}

.box {
  animation: slide 2s infinite; /* Applique l'animation */
}
```
## 11.  Variables CSS

Les variables CSS permettent de définir des valeurs réutilisables dans le code.

- **Exemple de variables CSS :**

```css
:root {
  --main-color: #3498db; /* Définition d'une variable */
}

body {
  background-color: var(--main-color); /* Utilisation de la variable */
}

.button {
  background-color: var(--main-color);
  color: white;
}
```
## 12. Conclusion

Le CSS est un outil essentiel pour quiconque souhaite concevoir des sites web attrayants et fonctionnels. En maîtrisant les concepts de base, comme la syntaxe, les sélecteurs, les propriétés, le positionnement et les modèles de mise en page, vous pouvez créer des designs réactifs et adaptables qui améliorent l’expérience utilisateur. Grâce à l'utilisation de transitions, d'animations et de variables, vous pouvez ajouter une touche professionnelle à vos projets.