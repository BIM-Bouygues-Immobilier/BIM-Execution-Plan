Vous devrez produire à minima un modèle par bâtiment. Vous êtes ensuite libre de découper votre modèle en plusieurs disciplines en fonction de vos contraintes de modélisations :

{% block lot_decoupage %}{% endblock %}

Vous demanderez alors au BIM Manager la création des modèles correspondants sur la plateforme d’échange bimsync.

{% if logiciel == "Revit" %}

Découpage des modèles :Mise au point du principe de découpage des modèles :
	*  Revit
	* ArchiCAD
	* Allplan

Principe général :A partir d'un modèle natif, exporter un ou plusieurs fichier IFC, un par type de produitOn découpe les export par bâtiment et par produit

Manipulation dans Revit :

{% elif logiciel == "ArchiCAD" %}

{% elif logiciel == "Allplan" %}

{% else %}

{% endif %}

Les modèles sont nommés de la façon suivante :

{% include "/00_Referentiel/NomDesModeles.md"  %}

