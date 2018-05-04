# Recommendations de modélisation

* [Généralités](#generalites)
* [Livrables](#livrables)
* [Découpage des modèles](#découpage)
* [Positionnement des modèles](#position)
* [Modélisation des niveaux](#niveaux)
{% block specific_toc %}{% endblock %}
* [Export au format IFC](#export)

## Généralités{#generalites}

L’ensemble des informations décrites ci-dessous devront être présentes dans les modèles déposés sur la plateforme d'échange au format IFC, indépendamment du logiciel de modélisation utilisé.
L'ensemble des études des intervenants devra être réalisé au moyen de modèles numériques.

Chaque Modèle Numérique devra constituer le reflet des études. L’ensemble des informations transmises par les Intervenants, notamment les plans, nomenclatures ou tous autres documents, devra être extrait, dans la mesure du possible, des Modèles Numériques.

Chaque intervenant aura la responsabilité de coordonner ses Modèles Numériques avec ceux développés par les autres intervenants.

{% block lot_specifique_generalites %}{% endblock %}

### Valeurs possibles

Lorsqu’une propriété doit contenir une valeur choisie parmi plusieurs proposées, il est impératif de saisir précisément l’une des valeurs indiquées. Les valeurs autres que celle proposées seront refusées, et l’intervenant devra déposer un nouveau modèle.

## Livrables{#livrables}

Au fur et à mesure de l’avancement des études, les Modèles Numériques seront transmis au Maître d’Ouvrage et partagés avec les autres intervenants. Ces modèles numériques du projet sont livrées sur la plateforme collaborative, suivant les jalons donnés, sous deux formats :

* Au format IFC2x3, en suivant [la procédure d'export](#export)
* Au format natif {% block logicel_format %}{% endblock %}

Les deux formats doivent être produits en même temps afin de garantir leur cohérence au même état de définition du bâtiment.

## Découpage des modèles{#découpage}

Vous devrez produire à minima un modèle par bâtiment. Vous êtes ensuite libre de découper votre modèle en plusieurs disciplines en fonction de vos contraintes de modélisations :

{% block lot_decoupage %}{% endblock %}

Vous demanderez alors au BIM Manager la création des modèles correspondants sur la plateforme d’échange bimsync.

Les modèles sont nommés de la façon suivante :

{% include "/00_Referentiel/NomDesModeles.md"  %}

## Positionnement des modèles{#position}

Les modèles devront être correctement positionnés les uns par rapport aux autres.

{% block logiciel_geopositionnement %}{% endblock %}

## Modélisation des niveaux{#niveaux}

Les modèles déposés contiennent un et un seul niveau \(IfcBuildingStorey\) par étage du projet, afin de permettre le regroupement des éléments du modèle par étage du projet.

Tous les éléments du projet devront être modélisés au bon niveau. A l'exception des verticalités des réseaux, tous les composants seront découpés par niveau. Suivant ce principe, les murs ne pouront pas s'étendre sur plusieurs niveaux.

Aucun niveau supplémentaire ne pourra être modélisé \(niveau brut béton, paliers intermédiaires, …\), mais on utilisera, en fonction du logiciel de modélisation, des décalages par rapport aux niveaux ou plans de référence.

Néanmoins, pour faciliter la modélisation des éléments structurels, il reste possible de ne dessiner que les niveaux bruts en lieu et à la place des niveaux finis.

![Modélisation des niveaux](/02_Modelisation/00_communs/images/Niveaux.PNG)

Les niveaux sont nommés de la façon suivante :

{% include "/00_Referentiel/NomDesNiveaux.md"  %}

{% block lot_specifique_content %}{% endblock %}

## Export au format IFC{#export}

### Généralités

Pour chaque lot, il est nécessaire de déposer un seul fichier, au format IFC2X3, incluant tous les éléments nécessaires à la bonne compréhension du projet pour la phase en cours, et purgé de tous les éléments non nécessaires au sujet en cours.

Les paramètres d'export décrit ci-dessous doivent être réglés une seule fois, puis réutilisés à l'identique pour tout les exports suivants.

{% block logiciel_export %}{% endblock %}