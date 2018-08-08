{% if logiciel == "Revit" %}

Les placards doivent être modélisés à l'aide des familles de placard fournies : vous pouvez utiliser la famille [Placard Portes Pivotantes](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/02_Modelisation/02_architecte/images/Placard%20Portes%20Pivotantes.rfa?raw=true) , et la famille [Placard Portes Coulissantes](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/02_Modelisation/02_architecte/images/Placard%20Portes%20Coulissantes.rfa?raw=true). Elle sont disponibles parmis les familles de Composant de Revit.

Ces familles de placard permettent de représenter les portes de placards. Les dimensions de ces portes peuvent être adaptées en fonction de la taille du placard. Elle se placent comme les murs, en cliquant à une extrimité, puis l'autre. Vous pouvez régler les dimensions à l'aides des paramètres partagés fournis avec la famille. Veiller à bien régler la profondeur du placard.

![Placard](/02_Modelisation/02_architecte/images/PlacardRevit01.PNG)

{% elif logiciel == "ArchiCAD" %}

WIP

{% elif logiciel == "Allplan" %}

TO DO

{% endif %}