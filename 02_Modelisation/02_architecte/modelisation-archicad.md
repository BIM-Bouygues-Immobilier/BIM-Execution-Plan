# Modélisation

L'article suivant présente les recommandations de modélisation pour différentes catégories d'éléments dans ArchiCAD. Ces recommendations permettent de produire les informations nécéssaires à la réalisation des [cas d'usages BIM de Bouygues Immobilier](/01_CasUsages/README.md).

Ces recommendations couvrent les éléments suivants:
* [Surface de plancher](#surface)
* [Locaux](#piece)
* [Places de parking](#parking)

## Préparation

Afin de différencier les différentes surfaces du projet, il est nécéssaire de créer deux catégories de zones :

| Code de la Catégorie | Nom Catégorie Zone | Description |
| :--- | :--- | :--- |
| AREA | Area | Cette catégorie permet de modéliser Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) |
| ROOMS | Rooms | Cette catégorie permet de modéliser les locaux |

![](/02_Modelisation/02_architecte/images/CréationDesCatégoriesDeZones.png)

## Modélisation des surfaces de plancher{#surface}

### Généralités

Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) sont calculées en additionnant les différents types de surfaces du projet. De plus, la représentation des surfaces de parkings extérieurs est attendue.

### Modélisation

L’ensemble de ces surfaces SHOB/SHON/SDP est modélisé à l’aide de l'outil Zone :

![](/02_Modelisation/02_architecte/images/Zones.png)

Chaque Zone dessinée doit alors avoir les propriétés suivantes :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Catégorie de Zone | Area | Toutes les zones sont dans la catégorie Area |
| Nom | Voir "Noms des surfaces" ci-dessous | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. |

La propriété « Description » est accessible en faisant un clic-droit sur une zone sélectionnée (1), puis « Options Zones sélectionnées » (2), puis « Gérer propriétés IFC... » (3), puis en cochant « Description » (4). La propriété est alors disponible dans « Options Zones sélectionnées » (5):

![](/02_Modelisation/02_architecte/images/Description.png)

### Noms des surfaces

{% include "../../00_Referentiel/NomDesSurfaces.md"  %}


## Modélisation des pièces{#piece}

### Généralités

Les Surfaces Utiles Brutes Locatives \(SUBL\), Surfaces Utiles Brutes Bureaux \(SUBB\), Surfaces Utiles Nettes \(SUN\) et Surfaces Nettes Bureaux \(SNB\) sont calculées à partir de la modélisation des locaux du projet.

L’ensemble des locaux du projet doivent être présents dans la maquette numérique. En plus des locaux « nobles » du programme, cette modélisation doit inclure tous les autres types de locaux, tel que les circulations, les locaux techniques, les gaines techniques, …

Les locaux doivent être représentés et décomposés en locaux fonctionnels \(Bureau, Salle de Réunion, Hall, …\), même si ces locaux appartiennent à un espace physique plus important. Par exemple, un hall et une circulation partageant le même espace physique devront être représentés comme deux locaux distincts.

Les locaux doivent être modélisés depuis le sol fini jusqu’au plafond fini. En l’absence de faux-plafonds, les locaux doivent être modélisés jusqu’à la hauteur libre prévue par le programme. Les locaux doivent être identifiés par leur nom, en suivant les valeurs du tableau "Nom des pièces" ci-dessous.

### Modélisation

Dans ArchiCAD, ces locaux doivent être modélisé à l’aide de l’outil Zone :

![](/02_Modelisation/02_architecte/images/Zones.png)

Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Catégorie de Zone | Rooms| Toutes les zones sont dans la catégorie Rooms |
| Nom | Voir « Nom des pièces » | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Hauteur | Hauteur libre \(en m\) | Cette propriété permet d’indiquer la hauteur libre dans le local.|

{% if book.bu == "logement" %}
### Zones

Afin de regrouper ces pièces, il est nécéssaire d'ajouter les propriétés suivantes à l'aide d'un paramètre partagé :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| ZoneDescription | Voir « Nom des zones » | Cette propriété permet de regrouper plusiseurs pièces en une seule zone, par exemple un appartement. Ce paramètre peut n'être saisi qu'une seule fois par zone. |
| ZoneName | Un numéro unique | Cette propriété permet d'identifier la zone.|

{% endif %}

{% include "../../00_Referentiel/NomDesZones.md"  %}

### Nom des pièces

{% include "../../00_Referentiel/NomDesPieces.md" %}

## Modélisation des places de parking{#parking}

### Modélisation

Les places de parking sont modélisées à l’aide de l'objet Parking. Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Description| Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement des places de parking. |