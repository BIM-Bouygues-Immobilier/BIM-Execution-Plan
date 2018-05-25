Vous devrez produire à minima un modèle par bâtiment. Vous êtes ensuite libre de découper votre modèle en plusieurs disciplines en fonction de vos contraintes de modélisations.
Quand on sélectione un objet dans le visioneur IFC, on veut savoir à quel lot il appartient. Par exemple, un mur qui sépart un logement d'un comerce, est à la limite entre ces 2 lots. Il peut aussi bien appartenir au lot commerce qu'au lot logement. Pour cette raison, vous devrer également produir un modèle par lot, afin de bien définir l'appartenence de chaque objet dans chaque modèle, et surtout éviter les doublons. les règles de modélisation sont les suivantes: 

* Paroi horizontale commune : le plancher doit être modélisé dans la maquette du dessous
* Paroi verticale commune : le mur doit être dessiné dans une des deux maquettes (choix arbitraire n’ayant aucune conséquence)

En definitif, vous devrez fourinr un modèle IFC par lot, et par bâtiment. Vous n'êtes cependant pas obliger de produir un modèle natif pour chaque modèles IFC, la modélisation en format natif se fait selon vos prférences. Vous trouverez une [méthode pour isoler les différents lots](#methode) plus bas sur cette page. 

{% if logiciel == "Revit" %}

Manipulation dans Revit:{#methode}
Dupliquer la vue 3D, de telle sorte à avoir un nombre de vue 3D égale au nombre de maquettes. 
Utiliser la fonction "zone de coupe" dans l'onglet "Etendues" des propriété pour isoler le produit dans chaque vue correspondante.

La zone de coupe doit être grossierement placée autour du produit à isoler, puis isoler à la main tous les éléments qui "dépassent".
Voici un exemple de découpage, d'abord le projet complet consituté de deux bâtiments et d'un parking, puis le bâtiment 1 isolé grâce à la méthode décrite précédement.

![decoupageRevit2](/templates/procedures/decoupage-images/decoupageRevit2.PNG)

![decoupageRevit](/templates/procedures/decoupage-images/decoupageRevit.PNG)

{% elif logiciel == "ArchiCAD" %}

Manipulation dans Archicad:{#methode}

{% elif logiciel == "Allplan" %}

Manipulation dans Allplan: {#methode}

{% else %}

{% endif %}

Les modèles sont nommés de la façon suivante :

{% include "/00_Referentiel/NomDesModeles.md"  %}

Une fois vos vues correctement découpées, suivre la méthode d'export en IFC pour exporter vos maquettes en format IFC.