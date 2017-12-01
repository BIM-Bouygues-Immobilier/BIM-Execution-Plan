# Modélisation

L'article suivant présente les recommandations de modélisation pour différentes catégories d'éléments dans Revit. Ces recommendations permettent de produire les informations nécéssaires à la réalisation des [cas d'usages BIM de Bouygues Immobilier](/01_CasUsages/README.md).

Ces recommendations couvrent les éléments suivants:
* [Plans de surface](#surface)
* [Pièces](#piece)
* [Places de parking](#parking)

## Modélisation des plans de surfaces{#surface}

### Généralités

Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) sont calculées en additionnant les différents types de surfaces du projet. De plus, la représentation des surfaces de parkings extérieurs est attendue.

### Modélisation

L’ensemble de ces surfaces SHOB/SHON/SDP est représenté à l’aide d’un plan de surface par niveau :

![](/02_Modelisation/02_architecte/images/SURFACE_01.PNG)

Chaque surface dessinée dans ce plan doit alors avoir les propriétés suivantes :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Nom | Voir "Noms des surfaces" ci-dessous | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. |

### Exemples

#### Niveau de parking

![](/02_Modelisation/02_architecte/images/Surfaces_ExempleNiveauParking.png)

#### Niveau courant

![](/02_Modelisation/02_architecte/images/Surfaces_ExempleNiveauCourant.png)

### Noms des surfaces

{% include "../../00_Referentiel/NomDesSurfaces.md"  %}


## Modélisation des pièces{#piece}

### Généralités

Les Surfaces Utiles Brutes Locatives \(SUBL\), Surfaces Utiles Brutes Bureaux \(SUBB\), Surfaces Utiles Nettes \(SUN\) et Surfaces Nettes Bureaux \(SNB\) sont calculées à partir de la modélisation des pièces du projet.

L’ensemble des locaux du projet doivent être présents dans la maquette numérique. En plus des locaux « nobles » du programme, cette modélisation doit inclure tous les autres types de locaux, tel que les circulations, les locaux techniques, les gaines techniques, …

Les locaux doivent être représentés et décomposés en locaux fonctionnels \(Bureau, Salle de Réunion, Hall, …\), même si ces locaux appartiennent à un espace physique plus important. Par exemple, un hall et une cafétéria partageant le même espace physique devront être représentés comme deux locaux distincts.

Les locaux doivent être modélisés depuis le sol fini jusqu’au plafond fini. En l’absence de faux-plafonds, les locaux doivent être modélisés jusqu’à la hauteur libre prévue par le programme. Les locaux doivent être identifiés par leur nom, en suivant les valeurs du tableau "Nom des pièces" ci-dessous.

### Modélisation

Dans Revit, ces locaux doivent être modélisé à l’aide de l’outil Pièce :

![](/02_Modelisation/02_architecte/images/SURFACE_02.PNG)

Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Nom | Voir « Nom des pièces » | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Décalage limite | Hauteur libre \(en m\) | Cette propriété permet d’indiquer la hauteur libre dans le local. Les propriétés « Niveau » et « Limite supérieure » doivent donc également avoir la même valeur. |

### Nom des pièces
Le tableau ci-dessous liste les noms de pièces à utiliser sur l'operation:

{% include "../../00_Referentiel/NomDesPieces.md" %}

{% if book.bu == "logement" %}
### Logements

Les pièces d'un logement doivent être regroupées ensembles. Pour cela, il est nécéssaire d'ajouter les propriétés suivantes à l'aide de deux paramètres partagés :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| ZoneName | Le numéro du logements (unique) | Cette propriété permet de regrouper les pièces d'un logement.|
| ZoneDescription | Voir « Typologie des logements » | Cette propriété permet de préciser la typologie du logement (T1, T2, ...).|

![](/02_Modelisation/02_architecte/images/RegroupementEnLogements.png)

{% include "../../00_Referentiel/TypologieDesLogements.md"  %}

{% endif %}

## Modélisation des places de parking{#parking}

### Modélisation dans Revit

Les places de parking sont modélisées à l’aide d’une famille de la catégorie Parking. Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Commentaire | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement des places de parking. |

{% if book.bu == "logement" %}
## Modélisation des murs

Les propriétés suivantes sont à compléter pour tout les types de murs :

![](/02_Modelisation/02_architecte/images/TypeDeMur.png)

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Nom du type | Voir « Nom des murs »  |  |
| Keynote | Suivant fichier texte joint | Cette propriété permet d'identifier le mur dans le CCTP. |

{% include "../../00_Referentiel/NomDesMurs.md" %}
{% endif %}