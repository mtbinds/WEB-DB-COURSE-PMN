
# Partie 01 - JSON

## 1. Introduction

**JSON (JavaScript Object Notation)** est un format de données textuel et léger, utilisé pour échanger des données de manière structurée. **JSON** est très populaire pour les échanges de données entre un serveur et un client. Ce format, bien que dérivé de la syntaxe JavaScript, est pris en charge par de nombreux langages de programmation, notamment **Python**, **Java**, **PHP**, et bien d’autres.

Les fichiers **JSON** utilisent l’extension `.json` et sont facilement compréhensibles par les humains grâce à leur syntaxe simple et concise.

## 2. Structure de JSON

La structure **JSON** repose sur deux types de structures principales :

- **Objets** : définis par des paires clé/valeur.
- **Tableaux** : une liste ordonnée de valeurs.

### 2.1 Objets JSON

Un **objet JSON** est une collection de paires clé/valeur. Les clés doivent être des chaînes de caractères (strings) entre guillemets doubles, tandis que les valeurs peuvent être de plusieurs types : chaînes, nombres, booléens, objets, tableaux ou `null`. Les objets sont définis par des accolades `{}`.

**Exemple d’un objet JSON :**

```json
{
  "nom": "Dupont",
  "age": 30,
  "ville": "Paris",
  "enfants": ["Alice", "Bob"],
  "isMarried": true
}
```

### 2.2 Tableaux JSON

Un **tableau JSON** est une liste ordonnée de valeurs, définie par des crochets `[]`. Un tableau peut contenir des chaînes, des nombres, des booléens, des objets ou même d’autres tableaux.

**Exemple d’un tableau JSON :**

```json
[
  {
    "nom": "Alice",
    "age": 25
  },
  {
    "nom": "Bob",
    "age": 28
  }
]
```

Dans cet exemple, le tableau contient deux objets représentant chacun une personne avec un nom et un âge.

### 2.3 Types de données JSON

**JSON** prend en charge plusieurs types de données :

- **String** : Texte entre guillemets doubles, comme `"Paris"`.
- **Number** : Entiers ou nombres à virgule flottante, comme `30` ou `3.14`.
- **Boolean** : Valeurs booléennes, `true` ou `false`.
- **null** : Valeur représentant une absence ou un vide.
- **Object** : Collection de paires clé/valeur entre accolades `{...}`.
- **Array** : Liste ordonnée de valeurs entre crochets `[...]`.

### 2.4 Syntaxe JSON

La syntaxe **JSON** suit des règles strictes pour garantir la compatibilité et la lisibilité.

1. Les **clés** doivent être entourées de guillemets doubles `"` (contrairement à **JavaScript**).
2. Les valeurs des paires clé/valeur doivent être séparées par deux-points `:`.
3. Les paires clé/valeur doivent être séparées par des virgules `,`.
4. **Pas de commentaires** : **JSON** ne supporte pas les commentaires.

**Exemple de fichier JSON valide :**

```json
{
  "nom": "Dupont",
  "age": 30,
  "ville": "Paris",
  "enfants": ["Alice", "Bob"],
  "isMarried": true,
  "adresse": {
    "rue": "123 Rue Exemple",
    "codePostal": "75001"
  }
}
```

## 3. Manipulation de JSON

### 3.1 Sérialisation et Désérialisation

**Sérialisation** signifie convertir un objet de données en une chaîne **JSON**. **Désérialisation** est l’opération inverse : convertir une chaîne **JSON** en un objet de données utilisable.

- En **JavaScript** : `JSON.stringify()` pour sérialiser et `JSON.parse()` pour désérialiser.

  ```javascript
  let objet = { nom: "Dupont", age: 30 };
  let json = JSON.stringify(objet);
  let objetDeNouveau = JSON.parse(json);
  ```

- En **Python** : `json.dumps()` pour sérialiser et `json.loads()` pour désérialiser.

  ```python
  import json
  
  data = {"nom": "Dupont", "age": 30}
  json_string = json.dumps(data)
  data_de_nouveau = json.loads(json_string)
  ```

### 3.2 Utilisation dans les requêtes HTTP

**JSON** est couramment utilisé pour transférer des données dans les applications web via des requêtes **HTTP (HyperText Transfer Protocol)**. Lorsqu’un client envoie des données à un serveur, elles sont souvent encodées en **JSON**.

Exemple de requête **JavaScript (fetch API)** :

```javascript
fetch("https://api.example.com/utilisateur", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ nom: "Dupont", age: 30 })
})
.then(response => response.json())
.then(data => console.log(data));
```

## 4. Exemples d'Utilisation de JSON

**JSON** est utilisé dans divers cas :

1. **APIs** : Les **API RESTful** utilisent **JSON** pour échanger des données entre serveurs et clients.
2. **Configuration** : **JSON** est souvent utilisé pour les fichiers de configuration car il est facile à lire et modifier.
3. **Bases de données NoSQL** : Certaines bases de données, comme **MongoDB**, utilisent des documents **JSON**.

## 5. Meilleures Pratiques pour JSON

Voici des conseils pour travailler efficacement avec **JSON** :

1. **Validez votre JSON** : Utilisez des validateurs pour détecter les erreurs de syntaxe.
2. **Clés cohérentes** : Utilisez une convention pour les noms de clés (ex. camelCase).
3. **Évitez les structures trop complexes** pour faciliter la lisibilité et le traitement.
4. **Minifiez en production** : Supprimez les espaces et sauts de ligne pour alléger la taille des données.

## 6. JSON vs XML

| Caractéristiques         | JSON                                | XML                                 |
|--------------------------|-------------------------------------|-------------------------------------|
| **Lisibilité**           | Plus lisible pour les humains       | Plus complexe                      |
| **Taille**               | Moins volumineux                    | Plus volumineux                    |
| **Compatibilité**        | Directement utilisable en JavaScript | Parsing nécessaire                 |
| **Structures de données**| Basé sur objets et tableaux         | Basé sur éléments imbriqués        |

## 7. Exemple JSON Complet

```json
{
  "utilisateur": {
    "nom": "Dupont",
    "prenom": "Jean",
    "age": 30,
    "email": "jean.dupont@example.com",
    "adresse": {
      "rue": "123 Rue Exemple",
      "ville": "Paris",
      "codePostal": "75001"
    },
    "competences": ["JavaScript", "Python", "HTML", "CSS"],
    "experience": [
      {
        "poste": "Développeur Front-End",
        "entreprise": "WebSolutions",
        "duree": "2 ans"
      },
      {
        "poste": "Développeur Back-End",
        "entreprise": "CodeFactory",
        "duree": "3 ans"
      }
    ],
    "actif": true
  }
}
```

## 8. Conclusion

**JSON** est essentiel pour le développement web, facilitant les échanges de données de manière légère et efficace. Une bonne maîtrise de **JSON** permet de travailler avec des **APIs**, des configurations d’applications et des bases de données modernes.