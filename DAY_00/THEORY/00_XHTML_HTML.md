# Partie 00 - HTML et XHTML

## 1. Introduction

**HTML (HyperText Markup Language)** et **XHTML (eXtensible HyperText Markup Language)** sont des langages de balisage utilisés pour structurer et présenter du contenu sur le Web. Ils sont les fondations de toute page web, permettant aux navigateurs d’afficher du texte, des images, des vidéos, et d'autres types de contenu.

**HTML** est flexible et permissif en termes de syntaxe, tandis que **XHTML** suit des règles plus strictes issues du XML, garantissant un code bien formé et rigoureux.

## 2. Qu'est-ce que HTML ?

HTML est un **langage de balisage** qui permet de structurer un document web en sections (titres, paragraphes, listes, etc.). Ce n’est pas un langage de programmation, mais un moyen de "marquer" des éléments pour les décrire et les organiser sur une page.


### 2.1 Les bases de HTML :

- HTML est composé de **balises** (tags) qui encadrent le contenu. Les balises sont délimitées par des chevrons, comme `<p>` pour débuter un paragraphe et `</p>` pour le fermer.
- La structure de base d'une page HTML inclut :
  
  ```html
  <!DOCTYPE html>
  <html lang="fr">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Titre de la page</title>
    </head>
    <body>
      <h1>Mon premier titre</h1>
      <p>Voici un paragraphe d'exemple.</p>
    </body>
  </html>
  ```
### 2.2 Les balises de HTML et Leur Utilisation :

#### Structure générale

- **`<!DOCTYPE html>`**  
  Déclaration indiquant la version du document HTML. Elle doit être placée en tout premier dans tout document HTML5.

- **`<html>`**  
  Conteneur racine qui englobe tout le contenu HTML d'une page.

- **`<head>`**  
  Section contenant des métadonnées sur le document, comme les liens vers les fichiers CSS, le charset, le titre, etc.

- **`<title>`**  
  Définit le titre de la page, affiché dans l'onglet du navigateur.

- **`<meta>`**  
  Fournit des métadonnées comme l'encodage des caractères (`<meta charset="UTF-8">`) ou les balises pour les moteurs de recherche.

- **`<body>`**  
  Contient le contenu visible de la page web (texte, images, liens, etc.).

#### Titres et textes

- **`<h1> à <h6>`**  
  Balises de titres, du plus important `<h1>` au moins important `<h6>`. Utilisées pour structurer les titres et sous-titres.

- **`<p>`**  
  Définit un paragraphe de texte.

- **`<br>`**  
  Insère un saut de ligne.

- **`<hr>`**  
  Insère une ligne horizontale (souvent utilisée pour séparer du contenu).

- **`<b>`**  
  Met le texte en gras (sans signification sémantique).

- **`<strong>`**  
  Met le texte en gras avec une importance sémantique.

- **`<i>`**  
  Met le texte en italique (sans signification sémantique).

- **`<em>`**  
  Met le texte en italique avec un effet d'emphase sémantique.

- **`<blockquote>`**  
  Définit une citation longue avec indentation.

- **`<code>`**  
  Définit un fragment de code informatique à l'intérieur du texte.

#### Liens et médias

- **`<a>`**  
  Crée un lien hypertexte. Utilise l’attribut `href` pour spécifier l'URL cible.

  ```html
  <a href="https://www.example.com">Cliquez ici</a>
  ```

- **`<img>`**  
  Insère une image. Utilise l’attribut `src` pour définir l'URL de l'image et `alt` pour la description alternative.

  ```html
  <img src="image.jpg" alt="Description de l'image">
  ```

- **`<audio>`**  
  Insère un fichier audio. Peut être contrôlé avec des attributs comme `controls` pour afficher un lecteur.

  ```html
  <audio controls>
    <source src="audio.mp3" type="audio/mpeg">
  </audio>
  ```

- **`<video>`**  
  Insère un fichier vidéo avec des attributs comme `controls` pour afficher des contrôles de lecture.

  ```html
  <video controls>
    <source src="video.mp4" type="video/mp4">
  </video>
  ```

#### Listes

- **`<ul>`**  
  Crée une liste à puces non ordonnée.

- **`<ol>`**  
  Crée une liste ordonnée (numérotée).

- **`<li>`**  
  Définit un élément dans une liste (utilisé dans `<ul>` ou `<ol>`).

  ```html
  <ul>
    <li>Élément 1</li>
    <li>Élément 2</li>
  </ul>
  ```

#### Tableaux

- **`<table>`**  
  Crée un tableau.

- **`<tr>`**  
  Crée une ligne dans un tableau.

- **`<td>`**  
  Définit une cellule dans une ligne de tableau.

- **`<th>`**  
  Définit une cellule d'en-tête dans un tableau (souvent utilisée avec l'attribut `scope`).

  ```html
  <table>
    <tr>
      <th>Nom</th>
      <th>Âge</th>
    </tr>
    <tr>
      <td>John</td>
      <td>25</td>
    </tr>
  </table>
  ```

#### Formulaires

- **`<form>`**  
  Crée un formulaire interactif pour soumettre des données à un serveur.

- **`<input>`**  
  Champ de saisie pour un formulaire (texte, mot de passe, bouton radio, case à cocher, etc.).

  ```html
  <input type="text" placeholder="Votre nom">
  ```

- **`<textarea>`**  
  Crée une zone de texte multi-lignes.

- **`<button>`**  
  Crée un bouton dans un formulaire.

- **`<label>`**  
  Associe un texte descriptif à un élément de formulaire.

- **`<select>`**  
  Crée un menu déroulant.

  ```html
  <select>
    <option value="val1">Option 1</option>
    <option value="val2">Option 2</option>
  </select>
  ```

#### Sémantique et structure

- **`<header>`**  
  Définit l'en-tête d'une page ou d'une section.

- **`<footer>`**  
  Définit le pied de page.

- **`<section>`**  
  Définit une section générale d'un document.

- **`<article>`**  
  Définit un contenu autonome (article, blog, etc.).

- **`<aside>`**  
  Définit du contenu en lien avec la page principale (comme une barre latérale).

- **`<nav>`**  
  Définit une section de navigation pour des liens de navigation principaux.

- **`<main>`**  
  Représente le contenu principal de la page.

#### Autres balises utiles

- **`<div>`**  
  Utilisé pour créer un conteneur générique pour le contenu (souvent utilisé avec CSS pour la mise en page).

- **`<span>`**  
  Utilisé pour appliquer des styles à une partie de texte inline sans créer de rupture de ligne.

Pour plus de balises, veuillez consulter [ce lien](https://www.apprendre-en-ligne.net/javascript/HTML_balises.pdf)

## 2. Qu'est-ce que XHTML ?

XHTML est une version stricte de HTML basée sur le XML. Les documents XHTML doivent être **bien formés**, ce qui signifie qu'ils respectent des règles de syntaxe strictes.

### 2.1 Caractéristiques principales de XHTML :

- **Syntaxe stricte** : Toutes les balises doivent être fermées, par exemple, `<br />` au lieu de `<br>`.
- **Casse des balises** : Les balises doivent être en **minuscules**.
- **Nesting correct** : Les balises doivent être imbriquées correctement.

Un exemple de document XHTML :

```xml
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="fr" lang="fr">
  <head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
    <title>Titre XHTML</title>
  </head>
  <body>
    <h1>Titre en XHTML</h1>
    <p>Ceci est un paragraphe en XHTML.</p>
    <br />
  </body>
</html>
```

## 3. Principales différences entre HTML et XHTML

| Critères             | HTML                                   | XHTML                                 |
|----------------------|----------------------------------------|---------------------------------------|
| **Syntaxe**          | Plus permissif                         | Plus strict (balises fermées, minuscules) |
| **Nesting (imbriquer des balises)** | Non strict                 | Strict                               |
| **Compatibilité**     | Compatible avec des navigateurs plus anciens | Requiert des navigateurs modernes    |
| **Souplesse**        | Plus tolérant face aux erreurs         | Les erreurs syntaxiques ne sont pas tolérées |

## 4. Pourquoi comprendre HTML et XHTML ?

Comprendre **HTML** et **XHTML** permet de créer des documents web robustes et conformes aux normes. Même si HTML5 a supplanté XHTML, les bonnes pratiques imposées par XHTML assurent :
- **Meilleure compatibilité** entre navigateurs.
- **Accessibilité** des pages aux utilisateurs ayant des besoins spécifiques et aux moteurs de recherche.
- **Facilité de maintenance** du code.

## 5. HTML5 et l'évolution

La version actuelle de HTML est **HTML5**, qui simplifie certaines règles et introduit de nouvelles balises (comme `<audio>`, `<video>`). HTML5 supporte aussi des API supplémentaires pour une meilleure interactivité.

Voici un exemple de structure de base en **HTML5** :

```html
<!DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page HTML5</title>
  </head>
  <body>
    <header>
      <h1>Bienvenue sur HTML5</h1>
    </header>
    <section>
      <p>Ceci est une page web utilisant HTML5.</p>
    </section>
  </body>
</html>
```

---

## 6. Conclusion

Comprendre la distinction entre HTML et XHTML est crucial pour maîtriser la création de pages web et pour garantir que les documents sont bien formés et accessibles à tous.