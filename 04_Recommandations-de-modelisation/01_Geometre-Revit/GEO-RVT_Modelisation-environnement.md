# Modélisation de l'environnement

## Introduction

Ce document décrit les éléments attendus pour la modélisation de l’environnement du projet de construction.

Les prescriptions ci-dessous sont indicatives, et n’enlèvent pas au prestataire la responsabilité de modéliser l’ensemble des éléments nécessaires à la bonne compréhension de l’environnement du projet de construction.

Les exemples sont présentés dans le logiciel Revit, mais sont adaptables à différent logiciels de modélisation numérique du bâtiment.

Le modèle sera livré au format IFC 2X3, accompagné du modèle au format natif. L’export en IFC doit suivre les recommandations de la note jointe « Recommandations de modélisation et d'export».

## Implantation et orientation

### Généralités

Le modèle de l’environnement sert de référence aux autres modèles, et établi donc le point de base du projet.

Néanmoins, si un ou plusieurs modèles existent déjà pour le projet, la modélisation de l’environnement prendra en compte la position des modèles existants afin d’éviter que ces modèles aient besoin d’être modifiés.

Ce modèle contient également la modélisation en volume des différentes limites du terrain \(limite de propriété, limite de parcelle cadastrale, emprises des cours communes, Espaces Verts Intérieurs Protégé, …\)

### Modélisation dans Revit

Les limites du terrains sont modélisées en plan à l’aide de l’outil « Limite de propriété » de Revit.  
![](/assets/GEOMETRE_ENV_01.PNG)  
Les limites de terrain sont ensuite modélisées en 3 dimensions à l’aide de l’outil « Volume in situ » de Revit. Ce volume prend le nom de la limite modélisée :  
![](/assets/GEOMETRE_ENV_02.PNG)

Le point topographique de Revit est placé à un emplacement caractéristique de la limite de lot afin de constituer le point de référence du projet.![](/assets/GEOMETRE_ENV_03.png)

\[Cfr [Partage des coordonnées](/04_Recommandations-de-modelisation/01_Geometre-Revit/GEO-RVT_Partage-des-coordonnées.md)\]

## Modélisation du plan de masse

### Généralités

Le modèle de l’environnement du projet doit notamment représenter les éléments suivants :

* Une modélisation du terrain comprenant les altitudes des points caractéristiques \(terrain naturel, regards, changement de pente, …\)
* Une modélisation de l’alignement et de la largeur des voies, ainsi que leurs éléments caractéristiques \(bateaux, bordures de trottoir, emplacement de stationnement, …\)
* Une modélisation des éléments de VRD, notamment, mobilier urbain, bornes incendies, bouches d’égouts, luminaires, poteaux électriques …
* La modélisation de la végétation \(Arbres et arbustes principaux, surfaces de pelouses, allées, terrasses plantées,…\)
* La modélisation en volume des constructions environnantes \(emprise au sol, hauteur, forme de la toiture, excroissances principales et significatives\)



