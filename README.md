# Version 4.0 du référentiel général d'amélioration de l'accessibilité (RGAA v4.0)

Ce dépôt contient les __fichiers de référence__ de la version 4.0 du RGAA

Le RGAA 4.0 est mis à disposition sous plusieurs formats :
* un document téléchargeable en format ODT et en format PDF,
* une version HTML disponible uniquement en ligne et publiée sur le site web de la Direction interministérielle du numérique (DINUM).

__À noter__ : le site web de la DINUM met à disposition le RGAA pour la version _en cours_. Les fichiers de référence des versions antérieures du RGAA sont disponibles dans Github.

## Documents téléchargeables du RGAA 4.0
* ### Fichier RGAA-v4.0.odt
Le fichier `RGAA-v4.0.odt` représente la version 4.0 de référence du RGAA en format ODT.

* ### Fichier RGAA-v4.0.pdf
Le fichier `RGAA-v4.0.pdf` représente la version 4.0 de référence du RGAA en format PDF. Il résulte d'une conversion du fichier ODT en format PDF.

* ### Fichier rgaa4.0.modele-de-grille-d-audit.ods
Le fichier `rgaa4.0.modele-de-grille-d-audit.ods` fournit un modèle de grille de vérification des critères du RGAA 4.0 sur un échantillon de pages pour la réalisation d'une inspection d'accessibilité numérique (_audit_).

* ### Fichier rgaa4-2019-modele-rapport-audit.odt
Le fichier `rgaa4-2019-modele-rapport-audit.odt` fournit un modèle de rapport de résultats d'une inspection d'accessibilité numérique (_audit_) en format ODT.

* ### Fichier rgaa4-2019-modele-rapport-audit.pdf
Le fichier `rgaa4-2019-modele-rapport-audit.pdt` fournit un modèle de rapport de résultats d'une inspection d'accessibilité numérique (_audit_) en format PDF. Il résulte d'une conversion du fichier ODT en format PDF.

* ### Fichier rgaa4-2019-exemple-declaration.odt
Le fichier `rgaa4-2019-exemple-declaration.odt` fournit un exemple pour la rédaction d'une déclaration d'accessibilité en format ODT.

* ### Fichier rgaa4-2019-exemple-declaration.pdf
Le fichier `rgaa4-2019-exemple-declaration.pdf` fournit un exemple pour la rédaction d'une déclaration d'accessibilité en format PDF. Il résulte d'une conversion du fichier ODT en format PDF.

*****************

## Version en ligne du RGAA 4.0

La version en ligne du RGAA est constituée d'un ensemble de pages HTML publiées sur le site de la DINUM dans la rubrique `Publications\rgaa_accessibilité` :
* Accueil
* _version HTML du RGAA 4.0_
* Kit d'audit
* Méthodologie de test
* Documentation
* Questions
* Notes de révision

## Version HTML du RGAA 4.0

La version HTML du RGAA 4.0 est constituée des pages HTML suivantes :
* Obligations d'accessibilité
* Méthode technique
  * Critères et tests
  * Glossaire
  * Environnement de test
  * Références
  * Licence

Les pages HTML `Accueil`, `Obligations d'accessibilité`, `Méthode technique`, `Kit d'audit`, `Méthodologie de test`, `Documentation`, `Questions` et `Notes de révision` sont générées à partir de fichiers en format Markdown (md).

Les pages HTML `Critères et tests` sont générées à partir du fichier `criteres.json` au format JSON.
Les pages HTML `Glossaire`, `Environnement de test`, `Références` et `Licence` sont générées à partir du fichier `glossaire.json` au format JSON.

## Package RGAA 4 initial version web

* ### Fichier package RGAA 4 initial version web.zip

Le fichier `package RGAA 4 initial version web.zip` contient les fichiers suivants

| NOM du fichier    | OBJET du fichier |
|:------------------|:-------|
|accueil.md        | pour la page d'accueil de la publication du RGAA sur le site de la DINUM incluant le sommaire de navigation
|**_criteres.json_**     | pour les pages HTML des critères et tests du RGAA 4
|**_glossaire.json_**    | pour les autres pages HTML du RGAA 4
|criteres.html     | pour gérer un filtre d'affichage des critères du RGAA sur le site de la DINUM
|documentation.md  | pour la page de documentation du RGAA sur le site de la DINUM
|kit.md            | pour la page du kit d'audit du RGAA sur le site de la DINUM
|methode.md        | pour la page d'introduction de la méthode technique du RGAA sur le site de la DINUM
|methodologie.md   | pour la page de méthodologie de tests du RGAA sur le site de la DINUM
|notes-revision.md | pour la page des notes de révision du RGAA 3 2017 vers le RGAA 4 sur le site de la DINUM
|obligations.md    | pour les pages de règles de mise en œuvre des obligations en matière d'accessibilité numérique du RGAA sur le site de la DINUM
|questions.md       | pour la page questions du RGAA sur le site de la DINUM

* ### Fichier criteres.json

Le fichier `criteres.json` contient la liste des 106 critères du RGAA 4.0 regroupés par thématiques. 

Chaque critère RGAA contient les informations suivantes :

* Numéro ;
* Titre ;
* Liste des tests associés, certains tests pouvant contenir eux-mêmes une liste de conditions d'application ;
* Section note technique (optionnelle) ;
* Section cas particuliers (optionnelle) ;
* Section références divisée en deux parties :
  * Références aux critères WCAG associés ;
  * Références aux techniques WCAG associées.

* ### Fichier glossaire.json

Le fichier `glossaire.json` contient les entrées de glossaire utilisées dans le fichier `criteres.json`.

Ces entrées sont regroupées par ordre alphabétique à la manière d'un abécédaire.

Chaque entrée de glossaire contient un ou plusieurs paragraphes explicatifs qui peuvent être assortis de liens et d'exemples.

#### Structure des contenus des fichiers JSON

Il est à noter que pour le fichier `criteres.json` :

* La propriété `tests` a pour contenu un objet qui regroupe l'ensemble des tests du critère.
* Chaque test est référencé directement par son numéro (`1`, par exemple) et a pour valeur : 
  * Soit une chaîne de caractères lorsque le test ne possède pas de conditions;
  * Soit un tableau de chaînes de caractères lorsqu'il possède des condtions. Dans ce cas, le premier élément du tableau correspond à l'intitulé du test et les éléments suivants aux conditions associées.
* Les sections `technicalNote` et `particularCases` ont pour valeur un tableau avec pour éléments :
  * Soit une chaîne de caractères correspondant à l'équivalent d'un paragraphe;
  * Soit un objet avec pour contenu une propriété `ol` ou `ul` correspondant à l'équivalent d'une liste ordonnée ou non ordonnée et ayant pour valeur un tableau contenant soit une chaîne de caractères, soit un objet avec pour contenu une propriété `ol` ou `ul` correspondant alors à un tableau imbriqué.

Il est à noter que pour le fichier `glossaire.json` :

* La description de l'entrée de glossaire est référencée par une propriété `dd` qui a pour valeur un tableau avec pour éléments :
  * Soit une chaîne de caractères correspondant à l'équivalent d'un paragraphe;
  * Soit un objet avec pour contenu une propriété `ol` ou `ul` correspondant à l'équivalent d'une liste ordonnée ou non ordonnée et ayant pour valeur un tableau contenant soit une chaîne de caractères, soit un objet avec pour contenu une propriété `ol` ou `ul` correspondant alors à un tableau imbriqué.

De manière générale, le contenu de certaines propriétés JSON contient un balisage interne en markdown :
* Les liens qu'ils soient internes ou externes; par exemple, le renvoi vers un critère du fichier `criteres.json` est représenté ainsi : `[critère 9.1](#crit-9-1)`.
* L'indication d'un terme ou d'une instruction relevant d'un langage informatique est signalée au moyen du délimiteur accent grave (`).

## Licence

Le contenu de ce dépôt est publié sous [licence Ouverte 2.0](LICENSE.md).
