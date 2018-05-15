{% extends "/templates/softwares/allplan.md" %}

{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Votre modèle peut ainsi être séparé en 2 modèles, Infrastructure et Equipements, par exemple.{% endblock %}

{# Donne des recommendation de modélisaiton générales propre au lot#}
{% block lot_specifique_generalites %}{% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}
* [Implantation et orientation](#implantation)
* [Modélisation de l'existant](#existant)
* [Modélisation de l'environnement](#environnement){% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}
## Implantation et orientation{#implantation}

### Généralités

Le modèle de l’environnement sert de référence aux autres modèles, et établi donc le point de base du projet.

Néanmoins, si un ou plusieurs modèles existent déjà pour le projet, la modélisation de l’environnement prendra en compte la position des modèles existants afin d’éviter que ces modèles aient besoin d’être modifiés.

Ce modèle contient également la modélisation en volume des différentes limites du terrain \(limite de propriété, limite de parcelle cadastrale, emprises des cours communes, Espaces Verts Intérieurs Protégé, …\)

### Modélisation dans Revit

Les limites du terrains sont modélisées en plan à l’aide de l’outil « Limite de propriété » de Revit.
![](/02_Modelisation/01_geometre/images/GEOMETRE_ENV_01.PNG)  
Les limites de terrain sont ensuite modélisées en 3 dimensions à l’aide de l’outil « Volume in situ » de Revit. Ce volume prend le nom de la limite modélisée :  
![](/02_Modelisation/01_geometre/images/GEOMETRE_ENV_02.PNG)

Le point topographique de Revit est placé soit à un emplacement caractéristique de la limite de lot soit en fonction des points matérialisés du système RGF93 afin de constituer le point de référence du projet.

![](/02_Modelisation/01_geometre/images/GEOMETRE_ENV_03.png)

\[Cf. [Partage des coordonnées](/02_Modelisation/00_communs/georeferencement-rvt.md)\]

## Modélisation de l'existant{#existant}

Dans le cas d’un projet de réhabilitation, le modèle du bâtiment existant doit intégrer les éléments suivants :

### Avant curage{#avant}

#### Façades

La modélisation toute hauteur des façades comprendra les ouvertures, les garde-corps, les fenêtres, les bandeaux, les masses d’ornementation et tout autre élément de façade nécessaire à la compréhension du bâtiment et à l’intervention de réhabilitation.
Toutes les altimétries doivent être rattachées au Nivellement Général de France (ou NVP si Paris)

#### Intérieurs

La modélisation de la volumétrie intérieure du bâtiment comporte l’indication de l’ensemble des locaux et notamment :

* Les murs de structure bâtiment (sans indication de cloison légères), poteaux et murs de refend,
* Planchers 
* Les trémies d’escaliers avec leur emmarchement, ascenseurs et gaines
* Les ouvertures (portes avec leur sens d’ouverture, fenêtres, porte-fenêtre,…)
* La poutraison apparente principale
* Les plafonds, afin de pouvoir identifier les plenum de plafond et plancher, les hauteurs sous plafonds et faux plafonds, les zones d’une hauteur à 1,80 mètre
* Les soffites, vasistas, lanterneaux, brisis des étages mansardés, installations fixes, …
* Les épaisseurs de plancher
* Les emplacement des parkings avec indication de leur longueur, largeur, hauteur

#### Toiture-terrasse

La modélisation des toiture-terrasse avec représentation:

* L’altitude des points caractéristiques,
* Sorties diverses en toiture (ventilations, aérations, siphon de sol, …),
* Souches de cheminées et de ventilations,
* Emprise des éléments techniques en toiture,
* Les sens des pentes, nature des matériaux de couverture, acrotères, joints de dilatation, 
* Les édicules

#### Locaux

Les locaux du bâtiment devront être reconnaissables sur le modèle, ainsi que leur destination/usage apparente.
Pour savoir comment modéliser les locaux sur un modèle numérique allez voir :

* [Pour tous les autres logiciels](/02_Modelisation/02_architecte/modelisation-ifc-arc.md )

La modélisation des locaux est finalisée au calcul des surfaces de plancher existantes. 

### Après curage{#apres}

Le modèle doit faire apparaitre :

* Les murs de structure, poteaux et murs de refend
* Les niveaux et épaisseurs de dalles 
* Epaisseur des murs, largeurs des baies en tableau
* Les déformation de dalles et poutraison (le cas échéant) seront mises en évidence

## Modélisation de l'environnement{#environnement}

Ce article décrit les éléments attendus pour la modélisation de l’environnement du projet de construction.

> Les prescriptions ci-dessous sont indicatives, et n’enlèvent pas au prestataire la responsabilité de modéliser l’ensemble des éléments nécessaires à la bonne compréhension de l’environnement du projet de construction.

### Modélisation du plan de masse

Le modèle de l’environnement du projet doit notamment représenter les éléments suivants :

* Une modélisation du terrain comprenant les altitudes des points caractéristiques (terrain naturel, regards, changement de pente, seuils, plaques, …) sur la base d’un nivellement de la propriété rattaché au NGF (ou NVP si spécifiquement demandé),
* Une modélisation des espaces minéraux avec l’alignement et de la largeur des voies et des chaussées, ainsi que leurs éléments caractéristiques (bateaux, bordures de trottoir, emplacement de stationnement, bancs, poubelles, , abribus, station de taxis, clôtures, portails, lampadaires, candélabres, feux routières, … )
* Une modélisation des éléments de VRD, notamment, mobilier urbain, bornes incendies, bouches d’égouts, luminaires, poteaux électriques …
* La modélisation des espaces végétaux \(Arbres et arbustes principaux, surfaces de pelouses, allées, terrasses plantées,…\)
* Les éléments hydrographiques
* Les limites séparatives et les limites des parcelles cadastrales
* Les murs séparatifs (mitoyen, privatif, …) avec indication de leur nature et des matériaux apparents
* La modélisation en volume des constructions environnantes \(emprise au sol, hauteur, forme de la toiture, excroissances principales et significatives\)

![](/02_Modelisation/01_geometre/images/Site.PNG)

### Immeubles voisins

S’ils existent des conventions de cours communes avec des bâtiments voisins, il sera nécessaire d’intégrer dans le modèle les éléments suivants, afin de pouvoir comprendre les coupes gabarits des bâtiments existants sur les propriétés riveraines :
*  Une modélisation pour l’élaboration des coupes-gabarits nécessaires à la vérification des prospects des bâtiments en vis-à-vis. 
*  L’indication des points altimétriques caractéristiques rattachés au NGF pour chaque portion de façade considérée, à savoir les altitudes : 
  *  Des premiers planchers éclairés par une vue principale
  *  Des acrotères
  *  Des éventuels retraits
*  L'emprise maximale des surplombs et des sous-sols
*  L’indication des voies, des caniveaux et des niveaux des seuils 

{% endblock %}