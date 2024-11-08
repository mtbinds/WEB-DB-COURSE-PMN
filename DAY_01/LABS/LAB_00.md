
# TP : Partie 00 - XML

## Objectifs

- Comprendre la structure et l’utilisation des balises en **XML**.
- Apprendre à valider un document **XML** avec une **DTD** et un schéma **XSD**.
- Savoir transformer un document **XML** en **HTML** avec **XSLT**.

## Prérequis

- Connaissances de base en balisage **XML**.
- Un éditeur de texte (comme **Visual Studio Code**, **Sublime Text**, etc.) pour écrire et tester du code **XML**.

---

## Exercice 1 : Création d’un Document XML

### Instructions

1. **Structure de données** : Créez un fichier **XML** nommé `bibliotheque.xml` représentant une bibliothèque contenant plusieurs livres. Chaque livre doit inclure les informations suivantes :
   
   - `titre` (chaîne de caractères)
   - `auteur` (chaîne de caractères)
   - `année` de publication (nombre)
   - `genre` (chaîne de caractères, comme "roman", "poésie", etc.)
   - `prix` avec un attribut `devise` (par exemple, `EUR`, `USD`).

2. **Organisation des données** : Utilisez des éléments imbriqués pour structurer chaque livre dans une balise `<livre>`, à l’intérieur de l’élément racine `<bibliotheque>`.

**Exemple :**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<bibliotheque>
  <livre>
    <titre>Apprendre XML</titre>
    <auteur>Jean Dupont</auteur>
    <annee>2020</annee>
    <genre>informatique</genre>
    <prix devise="EUR">29.99</prix>
  </livre>
  <livre>
    <titre>Les bases de XML</titre>
    <auteur>Marie Durant</auteur>
    <annee>2019</annee>
    <genre>informatique</genre>
    <prix devise="USD">34.50</prix>
  </livre>
</bibliotheque>
```

### Livrable

- Le fichier `bibliotheque.xml` avec une structure correcte et bien formée.

---

## Exercice 2 : Validation avec une DTD (Document Type Definition)

### Instructions

1. **Création d’une DTD interne** : Ajoutez une **DTD** interne à votre document XML (`bibliotheque.xml`) pour définir la structure de votre document. Cette **DTD** doit définir :
   
   - L’élément racine `<bibliotheque>`, contenant un ou plusieurs éléments `<livre>`.
   - Les éléments de chaque livre : `<titre>`, `<auteur>`, `<annee>`, `<genre>`, et `<prix>`.
   - L’attribut `devise` pour `<prix>`.

2. **Intégration de la DTD** : La DTD doit être placée au début du fichier XML.

**Exemple de DTD interne :**

```xml
<!DOCTYPE bibliotheque [
  <!ELEMENT bibliotheque (livre+)>
  <!ELEMENT livre (titre, auteur, annee, genre, prix)>
  <!ELEMENT titre (#PCDATA)>
  <!ELEMENT auteur (#PCDATA)>
  <!ELEMENT annee (#PCDATA)>
  <!ELEMENT genre (#PCDATA)>
  <!ELEMENT prix (#PCDATA)>
  <!ATTLIST prix devise CDATA #REQUIRED>
]>
<bibliotheque>
  <!-- contenu ici -->
</bibliotheque>
```

### Livrable

- Le fichier `bibliotheque.xml` avec la **DTD** intégrée, respectant la structure définie.

---

## Exercice 3 : Validation avec un Schéma XSD (XML Schema Definition)

### Instructions

1. **Création d’un fichier XSD** : Créez un fichier `bibliotheque.xsd` pour valider la structure de `bibliotheque.xml`. Ce schéma doit inclure :
   
   - La définition des éléments `<bibliotheque>` et `<livre>`.
   - Des contraintes sur les types de données, comme le type `xs:string` pour les chaînes de caractères, `xs:integer` pour les années, et `xs:decimal` pour le prix.
   - Un attribut `devise` pour `<prix>`.

2. **Application du schéma** : Modifiez le document XML pour lier le schéma XSD en ajoutant l’attribut `xsi:schemaLocation` dans l’élément racine.

**Exemple de schéma XSD :**

```xml
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="bibliotheque">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="livre" maxOccurs="unbounded">
          <xs:complexType>
            <xs:sequence>
              <xs:element name="titre" type="xs:string"/>
              <xs:element name="auteur" type="xs:string"/>
              <xs:element name="annee" type="xs:integer"/>
              <xs:element name="genre" type="xs:string"/>
              <xs:element name="prix">
                <xs:complexType>
                  <xs:simpleContent>
                    <xs:extension base="xs:decimal">
                      <xs:attribute name="devise" type="xs:string" use="required"/>
                    </xs:extension>
                  </xs:simpleContent>
                </xs:complexType>
              </xs:element>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
```

3. **Validation** : Utilisez un éditeur **XML** ou un outil en ligne pour valider `bibliotheque.xml` avec `bibliotheque.xsd`.

### Livrable

- Le fichier `bibliotheque.xsd` pour valider la structure de `bibliotheque.xml`.

---

## Exercice 4 : Transformation avec XSLT

### Instructions

1. **Création d’un fichier XSLT** : Créez un fichier `bibliotheque.xsl` pour transformer votre document **XML** en une page **HTML** affichant les informations de chaque livre sous forme de liste.

2. **Structure de Transformation** : La transformation doit générer une structure **HTML** contenant :
   
   - Un titre pour la page (`<h1>Bibliothèque</h1>`).
   - Une liste non ordonnée (`<ul>`) avec chaque livre comme élément de liste (`<li>`).
   - Chaque élément de liste doit afficher le `titre` et l’`auteur` du livre, suivis du `prix` avec la devise.

**Exemple de transformation XSLT :**

```xml
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
  <xsl:template match="/bibliotheque">
    <html>
      <body>
        <h1>Bibliothèque</h1>
        <ul>
          <xsl:for-each select="livre">
            <li>
              <strong><xsl:value-of select="titre"/></strong> -
              <xsl:value-of select="auteur"/> :
              <xsl:value-of select="prix"/> <xsl:value-of select="prix/@devise"/>
            </li>
          </xsl:for-each>
        </ul>
      </body>
    </html>
  </xsl:template>
</xsl:stylesheet>
```

3. **Transformation et Visualisation** : Utilisez un éditeur **XML** ou un navigateur compatible pour transformer le document **XML** en **HTML** à l’aide du fichier **XSLT**.

### Livrable

- Le fichier `bibliotheque.xsl` avec le code de transformation.
- Une capture d’écran ou le fichier **HTML** résultant.

---

## Conclusion

Ce **TP** vous a permis d'explorer différentes facettes de **XML**, de la création de documents bien structurés à la validation avec **DTD** et **XSD**, en passant par la transformation en **HTML** via **XSLT**.

---

### Points clés à retenir

- **DTD et XSD** permettent de valider la structure et l'intégrité des données **XML**.
- **XSLT** est un outil puissant pour transformer XML en d’autres formats, comme **HTML**, pour la présentation.
- Une bonne maîtrise de **XML** et de ses outils vous permet de structurer et d’utiliser les données de manière flexible et standardisée.
