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
| Commentaire | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement de ces surfaces. Les surfaces en terrasses \(locaux techniques par ex.\) sont marquée « Extérieur » |
| Nom | Voir "Noms des surfaces" ci-dessous | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. |

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
| Commentaire | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement de ces surfaces. Les surfaces en terrasses \(locaux techniques par ex. sont marquée « Extérieur ». |
| Nom | Voir « Nom des pièces » | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Décalage limite | Hauteur libre \(en m\) | Cette propriété permet d’indiquer la hauteur libre dans le local. Les propriétés « Niveau » et « Limite supérieure » doivent donc également avoir la même valeur. |

{% if book.bu == "logement" %}
### Zones

Afin de regrouper ces pièces en zones, il est nécéssaire d'ajouter les propriétés suivantes à l'aide d'un paramètre partagé :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| ZoneDescription | Voir « Nom des zones » | Cette propriété permet de regrouper plusiseurs pièces en une seule zone, par exemple un appartement. Ce paramètre peut n'être saisi qu'une seule fois par zone. |
| ZoneName | Un numéro unique | Cette propriété permet d'identifier la zone.|

{% endif %}

{% include "../../00_Referentiel/NomDesZones.md"  %}

### Nom des pièces

{% include "../../00_Referentiel/NomDesPieces.md" %}

## Modélisation des places de parking{#parking}

### Modélisation dans Revit

Les places de parking sont modélisées à l’aide d’une famille de la catégorie Parking. Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Commentaire | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement des places de parking. |