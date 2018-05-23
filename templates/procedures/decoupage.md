Vous devrez produire à minima un modèle par bâtiment. Vous êtes ensuite libre de découper votre modèle en plusieurs disciplines en fonction de vos contraintes de modélisations :

{% block lot_decoupage %}{% endblock %}

Vous demanderez alors au BIM Manager la création des modèles correspondants sur la plateforme d’échange bimsync.

{% if logiciel == "Revit" %}

Découpage des modèles :Mise au point du principe de découpage des modèles :
	* Revit
	* ArchiCAD
	* Allplan

Principe général: A partir d'un modèle natif, exporter un ou plusieurs fichier IFC, un par type de produit. On découpe les export par bâtiment et par produit

Manipulation dans Revit :
Dupliquer la vue 3D, de telle sorte à avoir un nombre de vue 3D égale au nombre de maquettes. 
Utiliser la fonction "zone de coupe" dans l'onglet "Etendues" des propriété pour isoler le produit dans chaque vue correspondante.
Lorsque deux maquettes possèdent des éléments communs, dans le découpage Architecte notamment, il convient de ne pas dupliquer ces éléments dans les deux maquettes concernées.
La règle est la suivante :
	*	Paroi horizontale commune : le plancher doit être modélisé dans la maquette du dessous
	*	Paroi verticale commune : le mur doit être dessiné dans une des deux maquettes (choix arbitraire n’ayant aucune conséquence)
La zone de coupe doit être grossierement placée autour du produit à isoler, puis isoler à la main tous les éléments qui "dépassent".
Voici un exemple de découpage, d'abord le projet complet consituté de deux bâtiments et d'un parking, puis le bâtiment 1 isolé grâce à la méthode décrite précédement.

{% elif logiciel == "ArchiCAD" %}

{% elif logiciel == "Allplan" %}

{% else %}

{% endif %}

Les modèles sont nommés de la façon suivante :

{% include "/00_Referentiel/NomDesModeles.md"  %}

Une fois vos vues correctement découpées, suivre la méthode d'export en IFC pour exporter vos maquettes en format IFC.