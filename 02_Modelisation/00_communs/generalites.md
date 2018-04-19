# Généralités

L’ensemble des informations décrites ci-dessous devront être présentes dans les modèles déposés sur la plateforme d'échange au format IFC, indépendamment du logiciel de modélisation utilisé.
L'ensemble des études des intervenants devra être réalisé au moyen de modèles numériques. 

Au fur et à mesure de l’avancement des études, les Modèles Numériques seront transmis au Maître d’Ouvrage et partagés avec les autres intervenants. Ces transmissions des modèles numériques s’effectueront cumulativement au format IFC, ainsi qu’au format natif. 
Pour connaitre le paramétrage pour l'export IFC voir: [Revit](/02_Modelisation/00_communs/export-rvt.md ) ou [Archicad](/02_Modelisation/00_communs/export-archicad.md ) ou [Allplan](/02_Modelisation/00_communs/export-allplan.md )

Chaque Modèle Numérique devra constituer le reflet des études. L’ensemble des informations transmises par les Intervenants, notamment les plans, nomenclatures ou tous autres documents, devra être extrait, dans la mesure du possible, des Modèles Numériques. 

Chaque intervenant aura la responsabilité de coordonner ses Modèles Numériques avec ceux développés par les autres intervenants.

##Livrables

Les modèles numériques du projet sont livrées sur la plateforme, suivant les jalons donnés, sous deux formats :

* Au format IFC2x3, en suivant la procédure d'export pour [Revit](/02_Modelisation/00_communs/export-rvt.md), pour [ArchiCAD](/02_Modelisation/00_communs/export-archicad.md) et pour [Allplan](/02_Modelisation/00_communs/export-allplan.md )
* Au format natif du logiciel utilisé pour la modélisation. Il sera purgé et seuls les éléments propres au projet seront conservés. 

Les deux formats doivent être produits en même temps afin de garantir leur cohérence au même état de définition du bâtiment.

## Découpage

Chaque intervenant produit à minima un modèle par bâtiment et il est ensuite libre de découper son modèle en plusieurs disciplines en fonction de ses contraintes de modélisations. 
Par exemple: 
* Un modèle Fluides peut ainsi être séparé en 3 modèles distincts, Climatisation, Plomberie et Electricité. 
* Un modèle Architecte peut être séparé en 2 modèles, Façades et Intérieur.

L'intervenant demandera alors au BIM Manager la création des modèles correspondants sur la plateforme d’échange Bimsync.

Les modèles sont nommés de la façon suivante : CODE DISCIPLINE - CODE BATIMENT

{% include "../../00_Referentiel/NomDesModeles.md"  %}

## Niveaux

Les modèles déposés contiennent un et un seul niveau \(IfcBuildingStorey\) par étage du projet, afin de permettre le regroupement des éléments du modèle par étage du projet.

Tous les éléments du projet devront être modélisés au bon niveau. A l'exception des verticalités des réseaux, tous les composants seront découpés par niveau \(donc par exemple pas de voiles sur plusieurs niveaux\).

Aucun niveau supplémentaire devra être modélisé \(niveau brut béton, paliers intermédiaires, …\), mais on utilisera, en fonction du logiciel de modélisation, des décalages par rapport aux niveaux ou plans de référence.

Néanmoins, pour faciliter la modélisation des éléments structurels, il reste possible de ne dessiner que les niveaux bruts en lieu et à la place des niveaux finis.

![](/02_Modelisation/00_communs/images/Niveaux.PNG)

Les niveaux sont nommés de la façon suivante : 

{% include "../../00_Referentiel/NomDesNiveaux.md"  %}

## Valeurs possibles

Lorsqu’une propriété doit contenir une valeur parmi plusieurs proposées, il est impératif de saisir précisément l’une des valeurs indiquées. Les valeurs autres que celle proposées seront refusées, et l’intervenant devra déposer un nouveau modèle.

