# Partie 04 - Sélecteurs et valeurs CSS3

## 1. Introduction

**CSS3 (Cascading Style Sheets Level 3)** est la dernière version du langage de style CSS, offrant de nouvelles fonctionnalités et améliorations par rapport à ses prédécesseurs. Les sélecteurs et valeurs CSS3 permettent un contrôle précis de l'apparence des éléments HTML, facilitant la création de mises en page complexes et réactives.

## 2. Sélecteurs CSS3

Les sélecteurs ***CSS3*** permettent de cibler des éléments spécifiques pour leur appliquer des styles. Voici un aperçu des différents types de sélecteurs disponibles dans ***CSS3***.

### 2.1 Sélecteurs de type

Ces sélecteurs ciblent tous les éléments d'un certain type.

#### Exemple :

```css
p {
  font-size: 16px; /* Applique une taille de police de 16px à tous les paragraphes */
}
```
### 2.2 Sélecteurs de classe

Ciblent tous les éléments ayant une classe spécifique. Les classes sont définies avec un point (.) devant leur nom.

- **Exemple :**

```css
.button {
  background-color: blue; /* Applique un fond bleu aux éléments avec la classe 'button' */
  color: white; /* Change la couleur du texte en blanc */
  padding: 10px 15px; /* Applique un remplissage de 10px en haut/bas et 15px à gauche/droite */
  border-radius: 5px; /* Arrondit les coins du bouton */
}
```
### 2.3 Sélecteurs d'identifiant

Ciblent un élément unique ayant un identifiant spécifique, précédé d’un ***#***. Les identifiants doivent être uniques dans un document HTML.

- ***Exemple :***

```css
#header {
  background-color: #f1f1f1; /* Applique un fond gris clair à l'élément avec l'ID 'header' */
  height: 60px; /* Définit la hauteur de l'en-tête */
}
```
### 2.4 Sélecteurs d'attributs

Ces sélecteurs ciblent des éléments en fonction de la présence ou de la valeur d'un attribut spécifique.

- **Exemples :**
  
- Cibler les éléments avec un attribut spécifique :

```css
input[type="text"] {
  border: 1px solid black; /* Applique une bordure noire aux champs de texte */
  padding: 5px; /* Ajoute un remplissage de 5px */
}
```
- Cibler les éléments ayant un attribut sans valeur :

```css
input[disabled] {
  background-color: lightgray; /* Applique un fond gris aux champs désactivés */
}
```
### 2.5 Sélecteurs pseudo-classes

Les pseudo-classes permettent de cibler des éléments dans un état particulier, tels que ***:hover***, ***:active***, ou ***:focus***.

- ***Exemples :***

- Cibler les liens au survol :

```css
a:hover {
  text-decoration: underline; /* Souligne les liens au survol */
  color: red; /* Change la couleur du texte en rouge lors du survol */
}
```
- Cibler les éléments sélectionnés :

```css
option:checked {
  background-color: lightblue; /* Change la couleur de fond des options sélectionnées */
}
```
### 2.6 Sélecteurs pseudo-éléments

Les pseudo-éléments ciblent une partie spécifique d'un élément, comme la première ligne ou la première lettre.

- **Exemples :**
  
Cibler la première ligne d'un paragraphe :

```css
p::first-line {
  font-weight: bold; /* Met en gras la première ligne des paragraphes */
  color: blue; /* Change la couleur de la première ligne en bleu */
}
```
- Cibler le premier caractère d'un élément :

```css
p::first-letter {
  font-size: 2em; /* Augmente la taille de la première lettre d'un paragraphe */
  color: green; /* Change la couleur de la première lettre en vert */
}
```
### 2.7 Sélecteurs de groupe

Les sélecteurs de groupe permettent d'appliquer le même style à plusieurs éléments. Cela réduit la redondance dans le code.

- **Exemple :**

```css
h1, h2, h3 {
  color: green; /* Applique une couleur verte aux titres h1, h2 et h3 */
  margin-bottom: 10px; /* Ajoute une marge inférieure de 10px */
}
```
### 2.8 Sélecteurs de descendant

Ciblent les éléments qui sont des descendants d'un autre élément. Cela permet de cibler des éléments de manière hiérarchique.

- **Exemple :**

```css
div p {
  color: blue; /* Change la couleur des paragraphes à l'intérieur des divs en bleu */
  line-height: 1.5; /* Définit l'espacement des lignes à 1.5 */
}
```
### 2.9 Sélecteurs adjacents

Ciblent un élément qui suit immédiatement un autre élément dans le document.

- **Exemple :**

```css
h2 + p {
  margin-top: 0; /* Supprime la marge supérieure du premier paragraphe suivant un h2 */
  color: gray; /* Change la couleur du texte en gris */
}
```
### 2.10 Sélecteurs d'enfants

Ciblent uniquement les éléments enfants directs d'un élément. Cela garantit que seuls les enfants immédiats sont stylés.

- **Exemple :**

```css
ul > li {
  list-style-type: square; /* Change le style des points des éléments de liste enfants directs d'une ul */
  color: navy; /* Change la couleur du texte en bleu marine */
}
```
### 2.11 Sélecteurs de liaison

Ces sélecteurs sont utilisés pour combiner plusieurs sélecteurs, permettant ainsi de créer des règles de style complexes.

- **Exemple :**

```css
div.box p.intro {
  font-weight: bold; /* Met en gras le paragraphe ayant la classe 'intro' dans un élément 'div' ayant la classe 'box' */
}
```
## 3. Valeurs CSS3

Les valeurs CSS définissent le style des propriétés. Voici les principales catégories de valeurs CSS3 :

### 3.1 Valeurs de couleur

Les couleurs peuvent être définies de plusieurs manières :

- Noms de couleurs :

```css
h1 {
  color: red; /* Utilise le nom de couleur 'red' */
}
```
- Valeurs hexadécimales :

```css
h1 {
  color: #FF5733; /* Utilise une valeur hexadécimale */
}
```
- Valeurs RGB :

```css
h1 {
  color: rgb(255, 87, 51); /* Utilise la notation RGB */
}
```
- Valeurs RGBA (ajout de la transparence) :

```css
h1 {
  color: rgba(255, 87, 51, 0.5); /* Couleur avec transparence */
}
```
- Valeurs HSL :

```css
h1 {
  color: hsl(12, 100%, 60%); /* Utilise la notation HSL */
}
```
- Valeurs HSLA (ajout de la transparence) :

```css
h1 {
  color: hsla(12, 100%, 60%, 0.5); /* Couleur HSL avec transparence */
}
```
### 3.2 Valeurs de taille

Les tailles peuvent être spécifiées en différentes unités :

- Pixels (px) :

```css
h1 {
  font-size: 24px; /* Taille de police en pixels */
}
```
- Pourcentages (%) :

```css
h1 {
  font-size: 150%; /* Taille de police en pourcentage */
}
```
- Unités relatives (em, rem) :

```css
h1 {
  font-size: 2em; /* Taille de police relative à la taille de police de l'élément parent */
}

h1 {
  font-size: 2rem; /* Taille de police relative à la taille de police de l'élément racine */
}
```
### 3.3 Valeurs de positionnement

Les propriétés de position peuvent être définies avec des valeurs qui déterminent comment un élément doit être positionné dans le flux de la page.

- **Exemple :**

```css
.box {
  position: absolute; /* Position absolue */
  top: 20px; /* Position 20 pixels du haut */
  left: 30px; /* Position 30 pixels de la gauche */
  z-index: 1; /* Définit la pile d'éléments */
}
```
### 3.4 Valeurs de liste

Les propriétés de liste définissent le style et la présentation des éléments de liste.

- **Exemple :**

```css
ul {
  list-style-type: circle; /* Utilise des cercles pour les éléments de liste */
  margin: 20px; /* Définit la marge autour de la liste */
  padding: 10px; /* Définit le remplissage à l'intérieur de la liste */
}
```
### 3.5 Valeurs de bordure

Les propriétés de bordure peuvent être définies avec plusieurs valeurs pour le style, la largeur et la couleur.

- **Exemple :**

```css
.box {
  border: 2px solid black; /* Bordure de 2 pixels, solide et noire */
  border-radius: 5px; /* Arrondit les coins du bloc */
}
```
### 3.6 Valeurs de marge et de remplissage

Les marges (espace à l'extérieur d'un élément) et les remplissages (espace à l'intérieur d'un élément) peuvent être spécifiés de manière individuelle ou combinée.

- **Exemples :**

- Valeurs individuelles :

```css
.container {
  margin: 10px; /* Marge de 10 pixels tout autour */
  padding: 20px; /* Remplissage de 20 pixels tout autour */
}
```
- Valeurs combinées :

```css
.box {
  margin: 10px 15px; /* 10 pixels en haut/bas et 15 pixels à gauche/droite */
  padding: 5px 10px 15px; /* 5 pixels en haut, 10 pixels à gauche/droite, et 15 pixels en bas */
}
```
### 3.7 Valeurs d'affichage

Les valeurs d'affichage déterminent comment un élément est affiché dans le flux de mise en page. Les valeurs incluent block, inline, inline-block, flex, grid, et none.

- **Exemples :**

```css
.box {
  display: block; /* L'élément est un bloc */
}

.inline {
  display: inline; /* L'élément est en ligne */
}

.flex {
  display: flex; /* Utilise le modèle de mise en page Flexbox */
}

.grid {
  display: grid; /* Utilise le modèle de mise en page Grid */
}

.hidden {
  display: none; /* Masque complètement l'élément */
}
```
### 3.8 Valeurs de transition et d'animation

Les valeurs pour les transitions et les animations peuvent inclure des durées, des propriétés à animer et des fonctions de temporisation.

- **Exemples :**

- Transition :

```css
.box {
  transition: background-color 0.5s ease; /* Transition de la couleur de fond en 0.5 seconde */
}

.box:hover {
  background-color: red; /* Change la couleur de fond au survol */
}
```
- Animation :

```css
@keyframes slide {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(100px);
  }
}

.animated {
  animation: slide 2s infinite; /* Animation qui se répète indéfiniment */
}
```
## 4. Sélecteurs avancés

CSS3 a introduit plusieurs sélecteurs avancés qui permettent un ciblage plus spécifique.

### 4.1 Sélecteurs de premier enfant et dernier enfant

Ces sélecteurs ciblent respectivement le premier et le dernier enfant d'un élément.

- **Exemples :**

```css
ul li:first-child {
  font-weight: bold; /* Met en gras le premier élément de la liste */
}

ul li:last-child {
  color: red; /* Change la couleur du dernier élément de la liste en rouge */
}
```
### 4.2 Sélecteurs de nth-child

Cible les éléments en fonction de leur position dans le DOM. Vous pouvez cibler le n-ième enfant, ou des motifs comme tous les deux, trois, etc.

- **Exemples :**

```css
li:nth-child(2n) {
  background-color: lightgray; /* Change le fond des éléments pairs de la liste */
}

li:nth-child(3) {
  color: blue; /* Change la couleur du troisième élément de la liste en bleu */
}
```
### 4.3 Sélecteurs de ()

Le sélecteur ***:not()*** permet d'exclure certains éléments de la sélection.

- **Exemple :**

```css
p:not(.special) {
  color: gray; /* Change la couleur de tous les paragraphes sauf ceux ayant la classe 'special' */
}
```
## 5. Conclusion

Les sélecteurs et les valeurs CSS3 offrent une flexibilité immense dans le style et la présentation des éléments HTML. En maîtrisant ces outils, vous pouvez créer des designs riches, interactifs et adaptables, améliorant ainsi l'expérience utilisateur de vos sites web.

## 6. Ressources supplémentaires

- [MDN Web Docs - CSS Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)

