# Modélisation

L'article suivant présente les recommandations de modélisation pour différentes catégories d'éléments dans Revit. Ces recommandations permettent de produire les informations nécéssaires à la réalisation des [cas d'usages BIM de Bouygues Immobilier](/01_CasUsages/README.md).

Ces recommendations couvrent les éléments suivants:
* [Plans de surface](#surface)
* [Pièces](#piece){% if book.bu == "logement" %}
* [Logements](#logements){% endif %}
* [Places de parking](#parking) {% if book.bu == "logement" %}
* [Placards](#placards){% endif %}
{% if book.bu == "logement" %} {% else %} 

De manière générale, dans les modèles Architecte les éléments de structure (dalles, poteaux, poutres, voiles ...) devront être modélisées sur un sous-projet à part de manière à pouvoir les isoler facilement. 
Dans le cas où des intervenants spécifiques pour les lots façade et décoration soient soient présents dans l'équipe, de principe devra s'appliquer également pour les éléments de façade et de décoration. 

{% endif %}

## Modélisation des plans de surfaces{#surface}

### Généralités

Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) sont calculées en additionnant les différents types de surfaces du projet. De plus, la représentation des surfaces de parkings extérieurs est attendue.

### Modélisation

L’ensemble de ces surfaces SHOB/SHON/SDP est représenté à l’aide d’un plan de surface par niveau :

![](/02_Modelisation/02_architecte/images/SURFACE_01.PNG)

Les surfaces modélisées doivent couvrir l'ensemble de l'emprise du projet, à tout les niveaux. Le niveau N00 (Rez-De-Chaussé) doit également contenir les surfaces extérieures au bâtiment lui-même (VRD, parking extérieur, ...).

Chaque surface dessinée dans ces plans doit avoir les propriétés suivantes :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Nom | Voir [« Noms des surfaces »](#nom_surface) ci-dessous | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. |
| Commentaire | Voir [« Types de surfaces »](#types_surface) ci-dessous| Cette propriété indique la destination des surfaces réalisées. |

Si un même niveau contient des surfaces ayant des usages différents (par exemple, surface de plancher de commerce et de logement), chaque usage doit être réprésenté par une surface.

### Exemples

#### Niveau de parking

![](/02_Modelisation/02_architecte/images/Surfaces_ExempleNiveauParking.png)

#### Niveau courant

![](/02_Modelisation/02_architecte/images/Surfaces_ExempleNiveauCourant.png)

### Noms des surfaces{#nom_surface}

{% include "../../00_Referentiel/NomDesSurfaces.md"  %}

### Types de surface{#types_surface}

{% include "../../00_Referentiel/NomDesProduits.md"  %}

## Modélisation des pièces{#piece}

### Généralités

Les {% if book.bu == "logement" %}Surfaces Habitables (S.H.A.B.){% else %}Surfaces Utiles Brutes Locatives \(SUBL\), Surfaces Utiles Brutes Bureaux \(SUBB\), Surfaces Utiles Nettes \(SUN\) et Surfaces Nettes Bureaux \(SNB\){% endif %} sont calculées à partir de la modélisation des pièces du projet.

L’ensemble des locaux du projet doivent être présents dans la maquette numérique. En plus des locaux « nobles » du programme, cette modélisation doit inclure tous les autres types de locaux, tel que les circulations, les locaux techniques, les gaines techniques, …

Les locaux doivent être représentés et décomposés en locaux fonctionnels {% if book.bu == "logement" %}\(Chambre, Séjour, Hall, …\){% else %}\(Bureau, Salle de Réunion, Hall, …\){% endif %}, même si ces locaux appartiennent à un espace physique plus important. Par exemple, {% if book.bu == "logement" %}un séjour et une cuisine{% else %}un hall et une cafétéria{% endif %} ouverts l'un sur l'autre devront être représentés comme deux locaux distincts.

Les locaux doivent être modélisés depuis le sol fini jusqu’au plafond fini. En l’absence de faux-plafonds, les locaux doivent être modélisés jusqu’à la hauteur libre prévue par le programme. Les locaux doivent être identifiés par leur nom, en suivant les valeurs du tableau "Nom des pièces" ci-dessous.

### Modélisation

Dans Revit, ces locaux doivent être modélisé à l’aide de l’outil Pièce :

![](/02_Modelisation/02_architecte/images/SURFACE_02.PNG)

Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Nom | Voir [« Nom des pièces »](#Nom_pieces) ci-dessous | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Commentaire | Voir [« Destination des pièces »](#destination_piece) ci-dessous| Cette propriété indique la destination des pièces réalisées. |
| Décalage limite | Hauteur libre \(en m\) | Cette propriété permet d’indiquer la hauteur libre dans le local. Les propriétés « Niveau » et « Limite supérieure » doivent donc également avoir la même valeur. |
{% if book.bu == "logement" %}

On completera également le revêtement de sol :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Finition du sol | Voir [« Revêtements de sols »](#revêtements_sols) ci-dessous | Cette propriété indique le type de revêtement de sol dans la pièce. |
{% endif %}

### Exemple

{% if book.bu == "logement" %}
![](/02_Modelisation/02_architecte/images/pieces_proprietes_logement.png)
{% else %}
![](/02_Modelisation/02_architecte/images/pieces_proprietes_IE.png)
{% endif %}

### Pièces sous 1,80 m

On découpe la pièce en séparant les espaces sous 1,80 m. On appele ces espaces "COMBLE".

### Nom des pièces{#Nom_pieces}
Le tableau ci-dessous liste les noms de pièces à utiliser sur l'operation:

{% include "../../00_Referentiel/NomDesPieces.md" %}

{% if book.bu == "logement" %}

### Revêtements de sols{#revêtements_sols}

{% endif %}

{% include "../../00_Referentiel/TypesDeRevetements.md" %}

### Destination des pièces{#destination_piece}
Le tableau ci-dessous liste les destinations possible pour une pièces:

{% include "../../00_Referentiel/NomDesProduits.md" %}

{% if book.bu == "logement" %}

## Logements{#logements}

### Généralités

Les pièces constituants un logement doivent être regroupées ensembles.

### Modélisation

Il est nécéssaire d'ajouter les propriétés suivantes aux pièces à l'aide de trois paramètres partagés, ZoneName, ZoneObjectType et ZoneDescription. Ces trois paramètres permettent de créer des IfcZones au moment de l'export IFC

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| ZoneName | Voir [« Noms des logements »](#nom_logement) ci-dessous | Cette propriété permet de regrouper les pièces d'un logement.|
| ZoneDescription | Voir [« Typologie des logements »](#typologie_logement) ci-dessous | Cette propriété permet de préciser la typologie du logement (T1, T2, ...).|
| ZoneObjectType | Voir [« Collections »](#collection) ci-dessous  | Cette propriété permet de préciser la collection du logement.|

### Exemple

![](/02_Modelisation/02_architecte/images/zones_proprietes_logement.png)

![](/02_Modelisation/02_architecte/images/RegroupementEnLogements.png)

### Nom des Logements{#nom_logement}

{% endif %}
{% include "/00_Referentiel/NomDesLogements.md"  %}
{% if book.bu == "logement" %}
### Typologie des logements{#typologie_logement}
{% endif %}
{% include "/00_Referentiel/TypologieDesLogements.md"  %}
{% if book.bu == "logement" %}
### Collections{#collection}
{% endif %}
{% include "/00_Referentiel/Collection.md"  %}

## Modélisation des places de parking{#parking}

Les places de parking sont modélisées à l’aide d’une famille de la catégorie Parking (Par exemple, la famille "Place de parking.rfa" incluse avec Revit). La propriété suivante est alors à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Commentaire | Un numéro unique | Cette propriété permet d’identifier la places de parking. |

![](/02_Modelisation/02_architecte/images/Parking.PNG)

{% if book.bu == "logement retiré" %}

## Modélisation des murs

Les propriétés suivantes sont à compléter pour tout les types de murs :

![](/02_Modelisation/02_architecte/images/TypeDeMur.png)

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Nom du type | Voir « Nom des murs »  |  |
| Keynote | Suivant fichier texte joint | Cette propriété permet d'identifier le mur dans le CCTP. |

{% include "../../00_Referentiel/NomDesMurs.md" %}

{% endif %}

{% if book.bu == "logement" %}

## Modélisation des façades de placards{#placards}

Les placards doivent être modélisé à l'aide de la famille de placard fournie, disponible [en cliquant ici](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/02_architecte/images/Placard.rfa)

Cette famille de placard, basée sur une ligne, permet de représenter les façades de placards. La profondeur du placard est un paramètre de type.

![](/02_Modelisation/02_architecte/images/Placard.png)

{% endif %}