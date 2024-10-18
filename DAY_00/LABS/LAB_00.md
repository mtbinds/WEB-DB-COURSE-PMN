# TP : Partie 00 - HTML et XHTML

## Objectifs

- Comprendre les différences entre ***HTML*** et ***XHTML***.
- Être capable de créer des pages web en utilisant ***HTML*** et ***XHTML***.
- Appliquer les meilleures pratiques de structuration et de validation du code.

## Prérequis

- Avoir un éditeur de texte (comme ***Visual Studio Code***, ***Sublime Text*** ou ***Notepad++***).
- Avoir un navigateur web pour tester vos pages (comme ***Chrome***, ***Firefox*** ou ***Safari***).

## Exercice 1 : Création d'une page HTML simple

### Instructions

1. Créez un fichier nommé `index.html`.
2. Rédigez le code suivant pour créer une page HTML simple :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ma Première Page HTML</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Bienvenue sur ma page HTML</h1>
    </header>
    <main>
        <section>
            <h2>À propos de moi</h2>
            <p>Je suis un étudiant en développement web.</p>
        </section>
        <section>
            <h2>Mes hobbies</h2>
            <ul>
                <li>Programmation</li>
                <li>Musique</li>
                <li>Voyage</li>
            </ul>
        </section>
    </main>
    <footer>
        <p>© 2024 Mon Site Web</p>
    </footer>
</body>
</html>
```
### Validation

- Ouvrez le fichier ***index.html*** dans votre navigateur pour voir la page.
- Vérifiez que la structure est correcte, et que tous les éléments s'affichent comme prévu.

## Exercice 2 : Conversion en XHTML

### Instructions

1. Créez un nouveau fichier nommé ***index.xhtml***.
2. Convertissez le code de votre fichier ***index.html*** en ***XHTML***. Voici quelques points à prendre en compte :

- Utilisez des balises auto-fermantes pour les éléments vides (comme `<br />` et `<img />`).
- Assurez-vous que toutes les balises sont correctement imbriquées et fermées.
- Vérifiez que les attributs sont en minuscule.

- **Exemple**

Voici à quoi pourrait ressembler une partie de votre code ***XHTML*** :

```xml
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="fr">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ma Première Page XHTML</title>
    <link rel="stylesheet" href="styles.css" />
</head>
<body>
    <header>
        <h1>Bienvenue sur ma page XHTML</h1>
    </header>
    <main>
        <section>
            <h2>À propos de moi</h2>
            <p>Je suis un étudiant en développement web.</p>
        </section>
        <section>
            <h2>Mes hobbies</h2>
            <ul>
                <li>Programmation</li>
                <li>Musique</li>
                <li>Voyage</li>
            </ul>
        </section>
    </main>
    <footer>
        <p>© 2024 Mon Site Web</p>
    </footer>
</body>
</html>
```
### Validation

- Ouvrez le fichier ***index.xhtml*** dans votre navigateur pour voir la page.
- Utilisez un validateur ***XHTML*** (comme le [W3C Validator](https://validator.w3.org/)) pour vous assurer que votre code est valide.

## Exercice 3 : Ajout de styles CSS

### Instructions

1. Créez un fichier nommé ***styles.css***.

2. Ajoutez des styles pour personnaliser votre page ***HTML*** et ***XHTML***. Par exemple :

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #007BFF;
    color: white;
    padding: 10px;
    text-align: center;
}

main {
    margin: 20px;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: #333;
    color: white;
}
```
### Validation

- Appliquez vos styles en ouvrant vos fichiers ***index.html*** et ***index.xhtml*** dans le navigateur.
- Vérifiez que les styles s'appliquent correctement.

## Exercice 4 : Utilisation de balises sémantiques

### Instructions

1. Modifiez vos fichiers ***index.html*** et ***index.xhtml*** pour utiliser des balises sémantiques supplémentaires, comme `<article>`, `<aside>`, et `<nav>`.

- Par exemple, vous pouvez ajouter une section pour une barre de navigation :

```html
<nav>
    <ul>
        <li><a href="#about">À propos</a></li>
        <li><a href="#hobbies">Hobbies</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>
```
### Validation

- Ouvrez vos fichiers dans le navigateur pour vérifier que les nouvelles balises s'affichent correctement.
- Assurez-vous que la structure reste valide après vos modifications.

## Exercice 5 : Validation et bonnes pratiques

### Instructions

1. Utilisez un validateur ***HTML*** et ***XHTML*** pour vérifier la validité de votre code.
  - [W3C Markup Validation Service](https://validator.w3.org/).
2. Assurez-vous que votre code suit les bonnes pratiques de structuration :
3. Utilisez l'indentation correcte pour rendre votre code lisible.
4. Commentez les sections de votre code pour expliquer votre logique si nécessaire.

### Validation

- Corrigez les erreurs signalées par le validateur et testez à nouveau.
- Soumettez votre travail (les fichiers ***index.html***, ***index.xhtml***, et ***styles.css***).

## Conclusion

Ce TP vous a permis de vous familiariser avec les bases de ***HTML*** et ***XHTML***, de créer des pages web simples, et d'appliquer des styles CSS. N'hésitez pas à explorer davantage et à expérimenter avec d'autres balises et propriétés CSS pour enrichir vos compétences en développement web.


## Points importants à retenir

- **HTML** est le langage de balisage standard pour créer des pages web.
- **XHTML** est une version plus stricte et bien formée de ***HTML*** qui utilise ***XML***.
- La structure et la validation du code sont essentielles pour garantir la compatibilité et la lisibilité.

**Good Luck !**