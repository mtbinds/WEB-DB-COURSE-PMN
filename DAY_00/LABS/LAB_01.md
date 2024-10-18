# TP : Partie 01 - Problématique des Moteurs de Rendu

## Objectifs

- Comprendre le fonctionnement des moteurs de rendu.
- Identifier les problèmes de compatibilité entre différents navigateurs.
- Analyser l'impact des moteurs de rendu sur l'affichage des pages web.

## Prérequis

- Connaissance de base en ***HTML***, ***CSS*** et ***JavaScript***.
- Avoir accès à plusieurs navigateurs (***Chrome***, ***Firefox***, ***Safari***, ***Edge***).

## Exercice 1 : Compréhension des moteurs de rendu

### Instructions

- **Recherche** : Recherchez et lisez des articles ou des ressources sur le fonctionnement des moteurs de rendu (par exemple, ***Blink***, ***Gecko***, ***WebKit***).

   - Que sont les moteurs de rendu et quel est leur rôle ?
   - Quelles étapes suivent-ils pour rendre une page web ?
   - Quelles sont les différences majeures entre les moteurs de rendu utilisés par les différents navigateurs ?

### Livrable

- Rédigez un court résumé de ***200-300 mots*** expliquant le rôle des moteurs de rendu et les principales différences entre eux. 

---

## Exercice 2 : Analyse de compatibilité

### Instructions

1. Créez une page web simple avec un code HTML et CSS qui utilise des fonctionnalités avancées de CSS (comme les grilles, flexbox, ou les animations CSS). Voici un exemple de structure simple :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Test de compatibilité CSS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Test de Compatibilité des Moteurs de Rendu</h1>
    </header>
    <main>
        <section>
            <h2>Mes Animations CSS</h2>
            <div class="box"></div>
        </section>
    </main>
</body>
</html>
```
```css
body {
    font-family: Arial, sans-serif;
}

.box {
    width: 100px;
    height: 100px;
    background-color: blue;
    animation: move 3s infinite alternate;
}

@keyframes move {
    from {
        transform: translateX(0);
    }
    to {
        transform: translateX(200px);
    }
}
```

2. Testez cette page dans différents navigateurs (***Chrome***, ***Firefox***, ***Safari***, ***Edge***).
3. Notez les différences dans le rendu des animations ou d'autres fonctionnalités CSS que vous avez utilisées.

### Livrable

- Rédigez un rapport comparatif d'environ ***300 mots*** sur le rendu de votre page web dans différents navigateurs. Incluez les éléments suivants :
  - Ce qui a bien fonctionné.
  - Ce qui n'a pas fonctionné ou a rendu différemment.
  - Des captures d'écran des résultats dans chaque navigateur (si possible).

## Exercice 3 : Détection des problèmes de rendu

### Instructions

1. Créez une page HTML qui utilise des balises HTML et CSS obsolètes ou des styles qui ne sont pas bien pris en charge par tous les navigateurs.

- Par exemple, utilisez des propriétés CSS qui sont en cours de dépréciation ou des balises HTML comme `<marquee>` ou `<blink>`.

2. Ajoutez des styles supplémentaires pour voir comment ces anciens éléments sont rendus.

- Exemple de code

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Test des Balises Obsolètes</title>
    <style>
        marquee {
            color: red;
            font-size: 24px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Test de Balises Obsolètes</h1>
    </header>
    <main>
        <section>
            <marquee>Ceci est un texte défilant !</marquee>
        </section>
    </main>
</body>
</html>
```
3. Testez cette page dans différents navigateurs et observez comment ils gèrent les balises obsolètes.

### Livrable

- Rédigez un court rapport d'environ ***200 mots*** sur vos observations concernant les balises obsolètes dans chaque navigateur. Incluez :
  
  - Quel navigateur a le mieux géré ces balises ?
  - Quel navigateur a montré des erreurs ou un rendu inattendu ?

- [Lien pour déposer le rapport - LAB 01](https://classroom.google.com/c/NzI0MzA5NDQ2NTc3?cjc=elqswn3)

## Exercice 4 : Utilisation des outils de développement

### Instructions

1. Ouvrez votre page web dans différents navigateurs.
2. Utilisez les outils de développement ***(DevTools)*** pour examiner les éléments de votre page, les styles appliqués, et les éventuelles erreurs de console.
3. Analysez les ressources chargées (***images***, ***fichiers CSS***, ***JavaScript***) et leur impact sur le rendu.

### Livrable

- Réalisez une capture d'écran de chaque ***DevTool*** montrant le rendu de votre page.
- Rédigez un court commentaire (***100-200 mots***) sur ce que vous avez appris en utilisant les outils de développement, notamment :

  - Les erreurs ou avertissements trouvés dans la console.
  - Les performances de chargement et leur impact sur le rendu.

## Conclusion

Ce TP vous a permis de comprendre la problématique des moteurs de rendu, d’analyser les différences de rendu entre les navigateurs et d'explorer comment les choix de balisage et de styles peuvent affecter l'affichage des pages web. N'hésitez pas à approfondir vos connaissances en testant davantage de fonctionnalités et en explorant de nouveaux outils.

### Points clés à retenir

- Les moteurs de rendu sont essentiels pour le traitement et l'affichage des pages web.
- Les différences entre les navigateurs peuvent affecter la manière dont une page est affichée.
- L'utilisation d'outils de développement permet d'analyser et de déboguer les problèmes de rendu.

