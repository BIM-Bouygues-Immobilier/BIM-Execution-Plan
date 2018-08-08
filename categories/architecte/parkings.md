{% if logiciel == "Revit" %}

Les places de parking sont modélisées à l'aide de la famille suivante : _[Place Parking Interieur Standard](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/02_Modelisation/02_architecte/images/Place%20Parking%20Interieur%20Standard.rfa?raw=true)
Télécharger la famille, puis la charger dans votre projet.Il y à deux types de places (Standard et PMR), et la dimension des places peut être ajustée à l'aide des paramètres de la famille.

![ParkingRevit](/02_Modelisation/02_architecte/images/ParkingRevit.PNG)

{% elif logiciel == "ArchiCAD" %}

Les places de parkings sont modélisées à l'aide de l'outil Objet (1). Il faut tout d'abord télécharger les places de parkings que nos avons modélisé : _[Place Parking Interieur Standard](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/02_Modelisation/02_architecte/images/Place%20Parking%20Interieur%20Standard.gsm?raw=true)_ et _[Place Parking Interieur PMR](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/02_Modelisation/02_architecte/images/Place%20Parking%20Interieur%20PMR.gsm?raw=true)_, puis les charger dans votre projet. Pour cela, aller dans le Gestionaire de bibliothèque (2) et cliquer sur Ajouter de nouveaux fichiers au dossier selectionné (3). Aller ensuite dans le dossier de téléchargement, sélectionner les 2 fichiers Places de parking (4), et cliquer sur Ouvrir (5). Une fois les fichiers ajoutés à la Bibliothèque emboitée (6), cliquer sur OK (7).

![ParkingArchicad01](/02_Modelisation/02_architecte/images/ParkingArchicad01.PNG)

Pour ajouter des places de parking à votre maquette, cliquer sur l'outil Objet (8), puis sur l'icône en forme de chaise (9). Dans la fenêtre que s'ouvre, sélectionner la bibliothèque emboitée (10), la place de parking à ajouter à la maquette (11), puis cliquer sur OK (12). Enfin, cliquer à l'endroit de la maquette où doit être positionnée la place de parking.

![ParkingArchicad02](/02_Modelisation/02_architecte/images/ParkingArchicad02.PNG)

la dimension des places peut être ajustée à l'aide des paramètres de l'objet. Cliquer droit sur la place, puis sur Opitions Objets sélectionnés (13); les dimensions peuvent être changée dans l'onglet Prévisualisation et position (14). vous pouvez également utiliser la fonction Déplacer les noeuds. 

![ParkingArchicad03](/02_Modelisation/02_architecte/images/ParkingArchicad03.PNG)

{% elif logiciel == "Allplan" %}

{% endif %}
