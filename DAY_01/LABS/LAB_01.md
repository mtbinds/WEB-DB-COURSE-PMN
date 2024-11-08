
# TP : Partie 01 - JSON

## Objectifs

- Comprendre le concept de **JSON** et son rôle dans le transfert de données.
- Apprendre à structurer et manipuler des données en **JSON**.
- Explorer l'importance de **JSON** dans les échanges de données entre client et serveur.

## Prérequis

- Connaissances de base en **JavaScript** et en manipulation de données.
- Un éditeur de texte (comme **Visual Studio Code**, **Sublime Text**, etc.) et un navigateur ou un environnement de développement (comme **Node.js**) pour les tests.

---

## Exercice 1 : Introduction à JSON

### Instructions

1. **Recherche** : Effectuez des recherches sur **JSON**.
   
   - Qu'est-ce que **JSON** ?
   - À quoi sert **JSON** et pourquoi est-il largement utilisé dans le développement web ?
   
2. **Structure et Types de Données** : Dressez une liste des types de données compatibles avec **JSON** (comme les chaînes, les nombres, les tableaux, etc.) et donnez un exemple pour chacun.

### Livrable

- Rédigez un court résumé (**200-300 mots**) sur **JSON**, son importance dans les échanges de données, et sa syntaxe de base.
- Fournissez également un fichier `.json` contenant un exemple de structure **JSON** qui inclut les différents types de données (chaîne, nombre, booléen, objet, tableau, etc.).

---

## Exercice 2 : Création et Validation de JSON

### Instructions

1. Créez un fichier JSON nommé `personne.json` qui décrit une personne avec les informations suivantes :
   - `nom` (chaîne de caractères)
   - `âge` (nombre)
   - `ville` (chaîne de caractères)
   - `estMarried` (booléen)
   - `enfants` (tableau de chaînes, représentant les prénoms des enfants)
   - `adresse` (objet contenant la `rue` et le `codePostal`)
   
   Exemple d'organisation :

   ```json
   {
     "nom": "Dupont",
     "age": 30,
     "ville": "Paris",
     "estMarried": true,
     "enfants": ["Alice", "Bob"],
     "adresse": {
       "rue": "123 Rue Exemple",
       "codePostal": "75001"
     }
   }
   ```

2. **Validation** : Utilisez un validateur **JSON** en ligne (comme [JSONLint](https://jsonlint.com/)) pour vérifier que votre fichier `personne.json` est valide.

### Livrable

- Soumettez le fichier `personne.json` après validation.
- Écrivez une brève explication (environ **100 mots**) sur l’importance de la validation de **JSON** et les erreurs courantes que vous avez pu rencontrer.

---

## Exercice 3 : Sérialisation et Désérialisation de JSON

### Instructions

1. **Sérialisation et Désérialisation en JavaScript** :
   
   - Créez un fichier **JavaScript** (`app.js`) dans lequel vous :
   
     - Créez un objet en **JavaScript** qui représente une voiture avec les attributs suivants : `marque`, `modele`, `année`, et `propriétaire` (un objet contenant le `nom` et l'`âge`).
     - Sérialisez cet objet en une chaîne **JSON** à l’aide de `JSON.stringify()` et affichez le résultat dans la console.
     - Désérialisez ensuite cette chaîne **JSON** en utilisant `JSON.parse()` pour recréer l'objet, et affichez-le dans la console.

2. **Sérialisation et Désérialisation en Python** (si vous connaissez **Python**) :
   
   - Créez un fichier Python (`app.py`) dans lequel vous effectuez les mêmes étapes en utilisant les fonctions `json.dumps()` et `json.loads()`.

### Livrable

- Soumettez le fichier `app.js` (et `app.py` si applicable) avec les scripts de sérialisation et désérialisation.
- Ajoutez des commentaires dans le code pour expliquer chaque étape du processus.

---

## Exercice 4 : Utilisation de JSON dans une Requête HTTP

### Instructions

1. **Création d'une Requête POST en JavaScript** :
   
   - Utilisez la fonction `fetch` en JavaScript pour envoyer une requête **POST** avec des données **JSON** à une **API de test** (par exemple, https://jsonplaceholder.typicode.com/posts).
   - Les données **JSON** doivent représenter un message avec un `titre`, un `contenu`, et un `auteur`.

   Exemple de code :

   ```javascript
   fetch("https://jsonplaceholder.typicode.com/posts", {
     method: "POST",
     headers: {
       "Content-Type": "application/json"
     },
     body: JSON.stringify({
       titre: "Mon Premier Message",
       contenu: "Ceci est le contenu de mon message.",
       auteur: "Jean Dupont"
     })
   })
   .then(response => response.json())
   .then(data => console.log(data))
   .catch(error => console.error("Erreur :", error));
   ```

2. **Testez et Observez** :
   
   - Exécutez le script dans le navigateur ou un environnement **Node.js** et observez la réponse.
   - Notez la réponse de l'**API** et expliquez comment elle renvoie l'**ID** du message créé.

### Livrable

- Soumettez le fichier `post_request.js` avec le code de la requête **POST**.
- Rédigez un rapport (environ **100 mots**) décrivant les étapes de la requête et l’analyse de la réponse de l’**API**.

---

## Exercice 5 : Transformation d'une Structure Complexe en JSON

### Instructions

1. Créez un fichier **JSON** nommé `projet.json` représentant un projet de développement logiciel. Ce projet devrait inclure :
   
   - `nomDuProjet`
   - `dateDeDebut`
   - `dateDeFin`
   - `membres` (tableau d'objets avec les informations de chaque membre : `nom`, `role`, `email`)
   - `taches` (tableau d'objets avec les informations de chaque tâche : `description`, `responsable` (nom du membre), `status` (valeur de type chaîne : "à faire", "en cours", ou "terminée"))

   Exemple d'organisation :

   ```json
   {
     "nomDuProjet": "Développement Web",
     "dateDeDebut": "2024-01-15",
     "dateDeFin": "2024-06-30",
     "membres": [
       {
         "nom": "Alice Martin",
         "role": "Développeuse",
         "email": "alice.martin@example.com"
       },
       {
         "nom": "Bob Durand",
         "role": "Chef de Projet",
         "email": "bob.durand@example.com"
       }
     ],
     "taches": [
       {
         "description": "Création de la maquette",
         "responsable": "Alice Martin",
         "status": "terminée"
       },
       {
         "description": "Développement Front-End",
         "responsable": "Alice Martin",
         "status": "en cours"
       }
     ]
   }
   ```

2. **Validation et Utilisation** :
   
   - Validez `projet.json` avec un validateur **JSON**.
   - Utilisez le fichier **JSON** pour afficher les informations des tâches dans une page **HTML** en **JavaScript (bonus)**.

### Livrable

- Soumettez le fichier `projet.json`.
- Optionnel : Fournissez le code **JavaScript** permettant de lire et afficher le contenu de `projet.json` dans une page HTML.

---

## Conclusion

Ce **TP** vous a permis de découvrir **JSON**, ses différentes utilisations, et sa manipulation dans les scripts **JavaScript** et **Python**. En maîtrisant **JSON**, vous améliorez vos compétences en développement web, notamment dans l'échange et la manipulation de données entre clients et serveurs.

---

### Points clés à retenir

- **JSON** est un format de données léger et universel pour le transfert de données entre les applications.
- La validation et la compréhension des structures de données **JSON** facilitent la création de données lisibles et utilisables par les machines.
- **JSON** est essentiel pour les **APIs** et la communication entre différents systèmes dans les applications web modernes.