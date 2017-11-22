# Définir les coordonnées du fichier géomètre

Les prescriptions ci-dessous sont indicatives, et n’enlèvent pas au prestataire la possibilité de définir des systèmes de coordonnées internes en fonction de la géométrie du bâtiment.

## Implantation et orientation

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
