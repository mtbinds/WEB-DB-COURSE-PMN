# TP : Partie 02 - Balises Sémantiques en HTML5

## Objectifs

- Comprendre le concept de balises sémantiques en ***HTML5***.
- Apprendre à utiliser correctement les balises sémantiques pour structurer un document ***HTML***.
- Explorer l'impact des balises sémantiques sur l'accessibilité et le référencement (***SEO***).

## Prérequis

- Connaissance de base en ***HTML*** et ***CSS***.
- Un éditeur de texte (comme ***Visual Studio Code***, ***Sublime Text***, etc.) et un navigateur web pour les tests.

## Exercice 1 : Introduction aux balises sémantiques

### Instructions

1. **Recherche** : Effectuez des recherches sur les balises sémantiques en ***HTML5***.
   
   - Qu'est-ce qu'une balise sémantique ?
   - Pourquoi est-il important d'utiliser des balises sémantiques ?

2. **Liste des balises** : Dressez une liste des balises sémantiques couramment utilisées en ***HTML5*** et de leur signification.

### Livrable

- Rédigez un court résumé (***200-300 mots***) sur les balises sémantiques en ***HTML5*** et leur importance. Incluez la liste des balises sémantiques que vous avez trouvées.

---

## Exercice 2 : Création d'une page web sémantique

### Instructions

1. Créez une nouvelle page HTML et utilisez les balises sémantiques appropriées pour structurer le contenu. Voici un exemple de structure que vous pouvez suivre :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Article Sémantique</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Titre Principal de l'Article</h1>
        <nav>
            <ul>
                <li><a href="#section1">Section 1</a></li>
                <li><a href="#section2">Section 2</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <article>
            <section id="section1">
                <h2>Titre de la Section 1</h2>
                <p>Voici un paragraphe de contenu pour la section 1.</p>
            </section>
            <section id="section2">
                <h2>Titre de la Section 2</h2>
                <p>Voici un paragraphe de contenu pour la section 2.</p>
            </section>
        </article>
    </main>
    
    <aside>
        <h3>Informations Complémentaires</h3>
        <p>Ceci est une barre latérale avec des informations supplémentaires.</p>
    </aside>
    
    <footer>
        <p>&copy; 2024 Mon Site Web. Tous droits réservés.</p>
    </footer>
</body>
</html>
```
2. Assurez-vous d'utiliser les balises sémantiques appropriées, telles que `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, et `<footer>`.

### Livrable

- Soumettez votre fichier HTML (avec le nom ***article-semantique.html***) ainsi qu'un fichier CSS (optionnel) pour le style.

## Exercice 3 : Évaluation de l'accessibilité

### Instructions

1. Utilisez des outils d'évaluation d'accessibilité (comme l'outil d'accessibilité de ***Google Chrome*** ou des outils en ligne comme ***WAVE***) pour analyser votre page web créée dans l'exercice précédent.
2. Notez les recommandations d'amélioration fournies par ces outils.

### Livrable

- Rédigez un rapport d'environ ***200 mots*** sur l'accessibilité de votre page web et les modifications que vous pourriez apporter pour l'améliorer.
  
## Exercice 4 : Impact sur le référencement (SEO)

### Instructions

Recherchez comment l'utilisation de balises sémantiques peut affecter le référencement d'un site web.

- Quels sont les avantages de l'utilisation de balises sémantiques pour le SEO ?
- Comment les moteurs de recherche utilisent-ils ces balises pour indexer le contenu ?
- Créez une courte présentation (***5-10 diapositives***) sur le rôle des balises sémantiques dans le SEO, en incluant des exemples.

### Livrable

- Soumettez votre présentation sous format ***PDF*** ou ***PowerPoint***.

## Conclusion

Ce TP vous a permis d'explorer les balises sémantiques en ***HTML5***, leur utilisation, et leur impact sur l'accessibilité et le référencement. En intégrant ces pratiques dans votre développement web, vous contribuez à créer des sites plus accessibles et mieux indexés.


### Points clés à retenir

- Les balises sémantiques fournissent un sens clair au contenu, améliorant ainsi l'accessibilité et le ***SEO***.
- L'utilisation correcte des balises sémantiques facilite le travail des moteurs de recherche et des technologies d'assistance.
