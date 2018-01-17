# Positionner son projet dans Allplan

Les modèles géométriques de chaque contributeur doivent faire référence un système commun de coordonnées relatif à la position géographique.  
Au démarrage du projet il faudra donc suivre la procédure suivante pour qu'une compilation et une visualisation du projet dans son ensemble soient possibles.

## Orientation du Nord

Lorsqu'on démarre un projet Allplan, le nord du projet correspond par défaut au haut de la vue de travail en plan. Il faudra donc implanter en conséquence son bâtiment en plan en tenant compte de la position du Nord Allplan.

Pour faciliter la modélisation, il sera ensuite possible de tourner les vues de travail en saisissant l'angle souhaité dans les paramètres du projet "Ange du projet pour faire pivoter la vue en plan".

![](/02_Modelisation/00_communs/images/ALLPLAN-ROTATE.PNG)

Ce paramètre modifie la visualisation en plan du projet, sans en changer l'orientation.

L'orientation du curseur dans les vues en plan pourra être éventuellement modifiée directement dans les propriétés de l'espace de travail.

## Définition des niveaux

La définition du modèle pour la gestion des plans de référence du projet devra se faire par rapport à l'altimétrie du site, en définissant donc le niveau du RDC \(qui correspondra au +/-0 projet\) en NGF.

Pour faire cela, il faudra renseigner la cote du niveau RDC dans la fenêtre des paramètres du projet "Coordonnées Offset" Z. 

![](/assets/offset.jpg)

## Position du zéro projet et des quadrillages

Avant d'implanter le projet en plan, il est tout d'abord conseillé d'identifier l'origine du système des coordonnées Allplan.   
Ce point devra **impérativement** correspondre à l'origine du modèle numérique géomètre, si disponible, ou bien au relevé géomètre en format Autocad \(0,0,0 UCS général\).

![](/02_Modelisation/00_communs/images/ALLPLAN-GRID.PNG)

L'implantation des quadrillages de projet se fera donc dans la parcelle par rapport à ce point de repère et un point "zéro projet" sera identifié à l'intersection de deux files perpendiculaires de la grille.

L'origine du projet pourra éventuellement être déplacée dans le "zéro projet" pour faciliter la modélisation dans la fenêtre des propriétés du projet, dans le paramétrage offset X et Y. 

> Tout offset projet en X et Y devra être ramenée à zéro avant d'exporter en IFC.


