Dans un même projet, s'il y a plusieurs lots à représenter ou plusieurs bâtiments, il est demandé de produire un modèle IFC par lot et par bâtiment. Le but étant de savoir à quel lot et quel bâtiment chaque objet appartient dans le modèle IFC final. Les règles de modélisation pour le découpage sont les suivantes: 

* Paroi horizontale commune : le plancher doit être modélisé dans la maquette du dessous
* Paroi verticale commune : le mur doit être dessiné dans une des deux maquettes (choix arbitraire n’ayant aucune conséquence)

Voici un exemple de découpage pour un bâtiment ayant plusieurs lots, répartis sur chacun un étage:

![decoupageRevitSchema3](/templates/procedures/decoupage-images/decoupageRevitSchema3.png)

En définitif, vous devrez fournir un modèle IFC par lot, et par bâtiment. Vous n'êtes cependant pas obligé de produire un modèle natif pour chaque modèles IFC, la modélisation en format natif se fait selon vos préférences. Vous trouverez une méthode pour isoler les différents lots ci dessous:

{% if logiciel == "Revit" %}

Méthode d'isolation des lots:
Dupliquer la vue 3D, de telle sorte à avoir un nombre de vue 3D égale au nombre de maquettes.
Utiliser la fonction "zone de coupe" dans l'onglet "Etendues" des propriété pour isoler le produit dans chaque vue correspondante.

La zone de coupe doit être grossièrement placée autour du produit à isoler, puis isoler à la main tous les éléments qui "dépassent".
Voici un exemple de découpage, d'abord le projet complet constitué de deux bâtiments et d'un parking, puis le bâtiment 1 isolé grâce à la méthode décrite précédemment.

![decoupageRevit2](/templates/procedures/decoupage-images/decoupageRevit2.PNG)

![decoupageRevit](/templates/procedures/decoupage-images/decoupageRevit.PNG)

{% elif logiciel == "ArchiCAD" %}

Créer une vue par lot et par bâtiment, et y regrouper les éléments que vous souhaitez exporter.

{% elif logiciel == "Allplan" %}

Au début de la conception, créer un claque par lot et par bâtiment. Veiller à bien assigner chaque objet dans le claque correspondant. Ainsi, lors de l'export IFC, vous pourrez choisir les calques à exporter pour chacun des modèles.

{% else %}

{% endif %}

Une fois vos vues correctement préparées, suivre la [méthode d'export en IFC](#export) pour exporter ces vues.