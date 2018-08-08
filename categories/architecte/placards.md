{% if logiciel == "Revit" %}

Les placards doivent être modélisés à l'aide des familles de placard fournies : vous pouvez utiliser la famille _[Placard Portes Pivotantes.rfa](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/02_Modelisation/02_architecte/images/Placard%20Portes%20Pivotantes.rfa?raw=true)_ , et la famille _[Placard Portes Coulissantes.rfa](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/02_Modelisation/02_architecte/images/Placard%20Portes%20Coulissantes.rfa?raw=true)_. Elle sont disponibles parmis les familles de Composant de Revit.

Ces familles de placard permettent de représenter les portes de placards. Les dimensions de ces portes peuvent être adaptées en fonction de la taille du placard. Elles se placent comme les murs, en cliquant à une extrémité, puis l'autre. Vous pouvez régler les dimensions à l'aides des paramètres partagés fournis avec la famille. Veiller à bien régler la profondeur du placard.

![Placard](/02_Modelisation/02_architecte/images/PlacardRevit01.PNG)

{% elif logiciel == "ArchiCAD" %}

Les portes des placards sont modélisées à l'aide de l'outil Objet (1). Il faut tout d'abord télécharger les portes de placards que nos avons modélisé : _[Placard Portes Coulissantes.gsm](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/02_Modelisation/02_architecte/images/Placard%20Portes%20Coulissantes.gsm?raw=true)_ et _[Placard Portes Pivotantes.gsm](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/02_Modelisation/02_architecte/images/Placard%20Portes%20Pivotantes.gsm?raw=true)_, puis les charger dans votre projet. Pour cela, aller dans le Gestionaire de bibliothèque (2) et cliquer sur Ajouter de nouveaux fichiers au dossier selectionné (3). Aller ensuite dans le dossier de téléchargement, sélectionner les 2 fichiers Placards Portes Coulissantes/Pivotantes (4), et cliquer sur Ouvrir (5). Une fois les fichiers ajoutés à la Bibliothèque emboitée (6), cliquer sur OK (7).

![PlacardArchicad01](/02_Modelisation/02_architecte/images/PlacardArchicad01.PNG)

Pour ajouter des portes de placards à votre maquette, cliquer sur l'outil Objet (8), puis sur l'icône en forme de chaise (9). Dans la fenêtre que s'ouvre, sélectionner la bibliothèque emboitée (10), la porte de placard à ajouter à la maquette (11), puis cliquer sur OK (12). Enfin, cliquer à l'endroit de la maquette où elle doit être positionnée.
![PlacardArchicad02](/02_Modelisation/02_architecte/images/PlacardArchicad02.PNG)

La dimension des portes peut être ajustée à l'aide des paramètres de l'objet. Cliquer droit sur la place, puis sur Options Objets sélectionnés (13); les dimensions peuvent être changées dans l'onglet Prévisualisation et position (14). vous pouvez également utiliser la fonction Déplacer les noeuds. 

![PlacardArchicad03](/02_Modelisation/02_architecte/images/PlacardArchicad03.PNG)

{% elif logiciel == "Allplan" %}

TO DO

{% endif %}