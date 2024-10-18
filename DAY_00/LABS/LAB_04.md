# TP : Partie 04 - Sélecteurs et valeurs CSS3

## Objectifs

- Comprendre les différents types de sélecteurs CSS.
- Apprendre à utiliser des valeurs CSS pour styliser les éléments HTML.
- Pratiquer la création et l'application de styles à l'aide de CSS.

## Prérequis

- Connaissance de base en HTML.
- Un éditeur de texte (comme ***Visual Studio Code***, ***Sublime Text***, etc.) et un navigateur web pour tester vos pages.

## Exercice 1 : Création d'une page HTML

### Instructions

1. Créez un fichier HTML (`index.html`) avec le contenu suivant :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercice CSS3</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Bienvenue dans l'exercice CSS3</h1>
        <nav>
            <ul>
                <li><a href="#section1">Section 1</a></li>
                <li><a href="#section2">Section 2</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section id="section1">
            <h2>Titre de la Section 1</h2>
            <p>Ceci est un paragraphe de contenu pour la section 1.</p>
        </section>
        <section id="section2">
            <h2>Titre de la Section 2</h2>
            <p>Ceci est un paragraphe de contenu pour la section 2.</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Mon Site Web. Tous droits réservés.</p>
    </footer>
</body>
</html>
```
### Livrable

- Soumettez votre fichier HTML (avec le nom index.html).

## Exercice 2 : Création d'une feuille de styles CSS

### Instructions

1. Créez un fichier CSS (***styles.css***) et liez-le à votre fichier ***HTML***.

2. Dans votre fichier CSS, utilisez les sélecteurs suivants pour styliser votre page :

- **Sélecteur de type :** Stylisez les balises `<h1>`, `<h2>`, `<p>`, et `<a>`.
- **Sélecteur de classe :** Créez une classe ***.important*** et appliquez-la à au moins un élément.
- **Sélecteur d'identifiant :** Stylisez le `<section>` avec l'identifiant ***#section1***.
Sélecteurs de descendant : Stylisez les éléments d'une liste dans la balise `<nav>` (ex. ***nav*** ***ul*** ***li***).

- Exemples de styles à appliquer

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 10px 0;
}

h1 {
    font-size: 2.5em;
}

h2 {
    font-size: 2em;
}

p {
    font-size: 1.2em;
}

nav ul {
    list-style-type: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin-right: 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

nav ul li a:hover {
    text-decoration: underline;
}

.important {
    color: red;
    font-weight: bold;
}

#section1 {
    background-color: #f9f9f9;
    padding: 20px;
}
```
### Livrable

- Soumettez votre fichier CSS (avec le nom ***styles.css***).

## Exercice 3 : Utilisation avancée des sélecteurs CSS

### Instructions

1. Ajoutez les sélecteurs CSS suivants dans votre fichier ***styles.css*** :

- **Sélecteurs d'attribut :** Stylisez les liens en fonction de leur attribut href. Par exemple, tous les liens menant à une section de la même page.
- **Pseudo-classes :** Utilisez des pseudo-classes comme ***:hover*** pour changer la couleur d'un lien lorsque le curseur passe dessus.
- **Pseudo-éléments :** Appliquez un style à la première lettre d'un paragraphe avec ***::first-letter***.

- Exemple de styles à appliquer

```css
nav ul li a[href^="#"] {
    font-weight: bold;
}

p::first-letter {
    font-size: 2em;
    color: blue;
}
```
### Livrable

- Soumettez votre fichier CSS mis à jour.

## Exercice 4 : Valeurs CSS

### Instructions

1. Ajoutez des styles à votre page pour explorer différentes valeurs CSS :

- Utilisez des unités de mesure différentes (***px***, ***em***, ***%***, ***rem***) pour les marges, les tailles de police et les espaces.
- **Expérimentez avec des couleurs :** définissez des couleurs en utilisant les noms de couleurs, les valeurs hexadécimales, et les valeurs ***RGB*** ou ***RGBA***.

- Exemple de styles à appliquer

```css
h2 {
    margin-top: 20px;
    margin-bottom: 10px;
    color: #333; /* couleur hexadécimale */
}

p {
    line-height: 1.5; /* espace entre les lignes */
    margin: 10px 0;
}

header {
    color: rgba(255, 255, 255, 0.9); /* couleur RGBA */
}
```
### Livrable

- Soumettez votre fichier CSS mis à jour.

## Exercice 5 : Test et validation

### Instructions

1. Ouvrez votre fichier HTML dans un navigateur pour vérifier que les styles CSS sont appliqués correctement.
2. Modifiez les styles selon vos préférences et expérimentez avec différentes valeurs et sélecteurs.
3. Utilisez les outils de développement du navigateur ***(F12)*** pour inspecter les éléments et voir quels styles CSS sont appliqués.

### Livrable

- Soumettez un rapport (***1 page***) sur ce que vous avez appris en travaillant sur ce TP, en incluant les modifications que vous avez apportées à votre fichier CSS.

## Conclusion

Ce TP vous a permis d'explorer les sélecteurs et les valeurs ***CSS3***. Vous avez appris à styliser une page HTML en utilisant divers sélecteurs, valeurs, et techniques avancées. Ces compétences sont essentielles pour la création de sites web attrayants et interactifs.

### Points clés à retenir

- Les sélecteurs CSS permettent de cibler des éléments spécifiques pour appliquer des styles.
- Les valeurs CSS peuvent varier en type et en unité, influençant l'apparence des éléments sur une page.
- La pratique des styles et des sélecteurs est cruciale pour développer des compétences en développement web.
