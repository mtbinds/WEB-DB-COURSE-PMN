# TP : Partie 03 - Feuilles de styles (CSS)

## Objectifs

- Comprendre les concepts de base des feuilles de styles en ***CSS***.
- Apprendre à appliquer des styles ***CSS*** pour améliorer la présentation d'une page web.
- Explorer les différentes manières d'intégrer ***CSS*** dans un document ***HTML***.

## Prérequis

- Connaissance de base en ***HTML***.
- Un éditeur de texte (comme ***Visual Studio Code***, ***Sublime Text***, etc.) et un navigateur web pour les tests.

## Exercice 1 : Introduction au CSS

### Instructions

1. **Recherche** : Effectuez des recherches sur le ***CSS*** et sa fonction dans le développement web.
   
   - Qu'est-ce que le ***CSS*** ?
   - Quelles sont les différences entre le ***CSS***, le ***HTML*** et le ***JavaScript*** ?

2. **Glossaire CSS** : Dressez une liste des termes clés liés au ***CSS*** (ex. sélecteur, propriété, valeur, etc.) et définissez chacun d'eux.

### Livrable

- Rédigez un court résumé (***200-300 mots***) sur le rôle du ***CSS*** dans le développement web, en incluant votre glossaire.

---

## Exercice 2 : Création d'une feuille de styles CSS

### Instructions

1. Créez une nouvelle page HTML avec le contenu suivant :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Site Web</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Bienvenue sur mon site web</h1>
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
2. Créez un fichier CSS (***styles.css***) pour styliser la page. Utilisez au moins ***10 propriétés CSS différentes***. 

- Voici quelques propriétés que vous pourriez utiliser :

  - **Couleurs (color, background-color)**
  - **Polices (font-family, font-size)**
  - **Marges et rembourrages (margin, padding)**
  - **Bordures (border)**
  - **Alignement (text-align)**
  - **Dimensions (width, height)**
  - **Effets de survol (:hover)**

### Livrable

- Soumettez votre fichier HTML (avec le nom ***mon_site.html***) et votre fichier ***CSS*** (avec le nom ***styles.css***).

## Exercice 3 : Utilisation des sélecteurs CSS

### Instructions

1. Dans votre fichier ***styles.css***, appliquez différents types de sélecteurs CSS :
 
 - **Sélecteurs de type :** sélectionnez tous les éléments d’un type (ex. ***h1***, ***p***).
 - **Sélecteurs de classe :** appliquez des styles à des classes spécifiques (ex. ***.important***).
- **Sélecteurs d'identifiant :** appliquez des styles à des éléments spécifiques (ex. ***#section1***).
Sélecteurs de descendant : sélectionnez des éléments en fonction de leur hiérarchie (ex. ***nav*** ***ul*** ***li***).

### Livrable

- Montrez dans votre fichier CSS comment vous avez utilisé chaque type de sélecteur. Assurez-vous que les styles appliqués reflètent les différents types de sélecteurs que vous avez utilisés.

## Exercice 4 : Mise en page avec CSS

### Instructions

1. Utilisez les propriétés de mise en page CSS pour structurer votre page. Essayez d'appliquer les techniques suivantes :

- Utilisation de ***flexbox*** pour aligner des éléments horizontalement ou verticalement.
- Utilisation de ***grid*** pour créer une mise en page complexe.
- Ajustement des éléments à l'aide de float et de clear.
- Ajoutez des commentaires dans votre fichier CSS pour expliquer comment chaque technique est utilisée et l'effet obtenu.

### Livrable

- Soumettez votre fichier CSS mis à jour, en veillant à ce qu'il inclue des mises en page flexibles et des grilles.

## Exercice 5 : Responsive Design

### Instructions

1. Modifiez votre feuille de styles pour qu'elle soit responsive :
2. Utilisez des unités relatives (comme ***em***, ***rem***, ***%***) plutôt que des unités absolues (comme px).
3. Ajoutez des media queries pour adapter la mise en page et les styles en fonction de la taille de l'écran.

- Voici un exemple de media query :

```css
@media (max-width: 600px) {
    body {
        background-color: lightblue;
    }
    h1 {
        font-size: 2em;
    }
}
```
### Livrable

- Soumettez votre fichier CSS mis à jour, en démontrant comment votre page est responsive à l'aide de media queries.

- [Lien pour déposer les rapports et le code - LAB 03](https://classroom.google.com/c/NzI0MzA5NDQ2NTc3?cjc=elqswn3)

## Conclusion

Ce TP vous a permis d'explorer les concepts fondamentaux des feuilles de styles en CSS. Vous avez appris à appliquer des styles, à utiliser des sélecteurs et à créer des mises en page responsives. Ces compétences sont essentielles pour tout développeur web souhaitant créer des sites attrayants et accessibles.

### Points clés à retenir

- Le CSS permet de séparer la présentation et le contenu des pages web.
- L'utilisation de sélecteurs appropriés et de techniques de mise en page est essentielle pour créer des designs attrayants et fonctionnels.
- Le responsive design est crucial pour s'assurer que les sites web s'affichent correctement sur tous les appareils.
