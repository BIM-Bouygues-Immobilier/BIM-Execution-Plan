{% extends "/templates/softwares/archicad.md" %}

{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Votre modèle peut ainsi être séparé en 2 modèles, Façades et Intérieur.{% endblock %}

{# Donne des recommendation de modélisaiton générales propre au lot#}
{% block lot_specifique_generalites %}

De manière générale, dans les modèles Architecte les éléments de structure (dalles, poteaux, poutres, voiles ...) devront être modélisées sur des calques séparés de manière à pouvoir les isoler facilement.
Dans le cas où des intervenants spécifiques pour les lots façade et décoration soient soient présents dans l'équipe, ce principe devra s'appliquer également pour les éléments de façade et de décoration.

{% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}
* [Surface de plancher](#surface)
* [Pièces](#piece)
* [Logements](#logements)
* [Modélisation des places de parking](#parking)
* [Modélisation des Placards](#placards)
* [Modélisation des murs](#murs)
* [Modélisation des poteaux](#poteaux)
* [Modélisation des poutres](#poutres)
* [Modélisation des planchers](#planchers)
* [Modélisation des toitures](#toitures)
* [Modélisation des fenetres](#fenetres)
* [Modélisation des murs rideaux](#murs rideaux)
* [Modélisation des cloisons](#cloisons)
* [Modélisation des plafonds](#plafonds)
* [Modélisation des portes](#portes)
* [Modélisation des brises soleil](#brises soleil)
* [Modélisation des stores](#stores)
* [Modélisation des appareils élévateurs](#appareils élévateurs)
* [Modélisation des escaliers](#escaliers)
* [Modélisation des gardes-corps](#gardes-corps)
* [Modélisation des voiries](#voiries){% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}


### Préparation

Afin de différencier les différentes surfaces du projet, il est nécéssaire de créer deux catégories de zones :

| Code de la Catégorie | Nom Catégorie Zone | Description |
| :--- | :--- | :--- |
| AREA | Area | Cette catégorie permet de modéliser Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) |
| ROOMS | Rooms | Cette catégorie permet de modéliser les locaux |

![](/02_Modelisation/02_architecte/images/CréationDesCatégoriesDeZones.png)

### Modélisation des surfaces de plancher{#surface}

{% include "/categories/architecte/surfaces.md" %}

### Modélisation des pièces{#piece}

{% include "/categories/architecte/pieces.md" %}

### Modélisation des logements{#logements}

Les pièces constituants un logement doivent être regroupées ensembles. Il est nécéssaire d'ajouter les propriétés suivantes aux pièces à l'aide de trois paramètres:

* ZoneName
* ZoneObjectType
* ZoneDescription.

Ces trois paramètres permettent de créer des IfcZones au moment de l'export IFC

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| ZoneName | Voir [« Noms des logements »](#nom_logement) ci-dessous | Cette propriété permet de regrouper les pièces d'un logement.|
| ZoneDescription | Voir [« Typologie des logements »](#typologie_logement) ci-dessous | Cette propriété permet de préciser la typologie du logement (T1, T2, ...).|
| ZoneObjectType | Voir [« Collections »](#collection) ci-dessous  | Cette propriété permet de préciser la collection du logement.|

#### Nom des Logements{#nom_logement}

{% include "/00_Referentiel/NatureDesLogements.md"  %}

#### Typologie des logements{#typologie_logement}

{% include "/00_Referentiel/TypologieDesLogements.md"  %}

#### Collections{#collection}

{% include "/00_Referentiel/Collection.md"  %}

### Modélisation des places de parking{#parking}

Les places de parking sont modélisées à l’aide d’une famille de la catégorie Parking. La propriété suivante est alors à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Commentaire | Un numéro unique | Cette propriété permet d’identifier la places de parking. |

![Parking](/02_Modelisation/02_architecte/images/Parking.PNG)

### Modélisation des façades de placards{#placards}

Les placards doivent être modélisé à l'aide de la famille de placard fournie, disponible [en cliquant ici](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/02_architecte/images/Placard.rfa)

Cette famille de placard, basée sur une ligne, permet de représenter les façades de placards. La profondeur du placard est un paramètre de type.

![Placard](/02_Modelisation/02_architecte/images/Placard.png)

### Modélisation des murs{#murs}

{% include "/categories/architecte/murs.md"  %}

### Modélisation des poteaux{#poteaux}

{% include "/categories/architecte/poteaux.md"  %}

### Modélisation des poutres{#poutres}

{% include "/categories/architecte/poutres.md"  %}

### Modélisation des planchers{#planchers}

{% include "/categories/architecte/planchers.md"  %}

### Modélisation des toitures{#toitures}

{% include "/categories/architecte/toitures.md"  %}

### Modélisation des fenetres{#fenetres}

{% include "/categories/architecte/fenetres.md"  %}

### Modélisation des murs rideaux{#murs rideaux}

{% include "/categories/architecte/murs-rideaux.md"  %}

### Modélisation des cloisons{#cloisons}

{% include "/categories/architecte/cloisons.md"  %}

### Modélisation des plafonds{#plafonds}

{% include "/categories/architecte/plafonds.md"  %}

### Modélisation des portes{#portes}

{% include "/categories/architecte/portes.md"  %}

### Modélisation des brises soleil{#brises soleil}

{% include "/categories/architecte/brises-soleil.md"  %}

### Modélisation des stores{#stores}

{% include "/categories/architecte/stores.md"  %}

### Modélisation des appareils élévateurs{#appareils élévateurs}

{% include "/categories/architecte/appareils-elevateurs.md"  %}

### Modélisation des escaliers{#escaliers}

{% include "/categories/architecte/escaliers.md"  %}

### Modélisation des gardes-corps{#gardes-corps}

{% include "/categories/architecte/stores.md"  %}

### Modélisation des voiries{#voiries}

{% include "/categories/architecte/voiries.md"  %}
{% endblock %}