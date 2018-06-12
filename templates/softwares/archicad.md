{% extends "/templates/modelisation.md" %}
{% set logiciel = "ArchiCAD" %}

{# Décrit le format de fichier du logiciel #}
{% block logicel_format %}AllPlan (.prj.zip){% endblock %}

{# Décrit la procédure de georeférencement #}
{% block logiciel_geopositionnement %}
{% endblock %}

{# Décrit la procédure d'export en IFC #}
{% block logiciel_export %}

### Généralités

Pour chaque lot, il est nécessaire de déposer un seul fichier, au format IFC2X3, incluant tous les éléments nécessaires à la bonne compréhension du projet pour la phase en cours, et purgé de tous les éléments non nécessaires au sujet en cours.
Avant d'exporter, il est nécessaire de ramener les offset en X et Y dans la fenêtre des paramètres du projet à zéro.

### Procédure d’export

Ouvrir « Configuration de traduction IFC » pour créer une nouvelle configuration d’export en IFC

![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad.PNG)

Dupliquer le traducteur général pour créer un nouveau traducteur. Vous pouvez alors renommer ce nouveau traducteur :

![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad0.PNG)

Les propriétés sont configurables grâces aux 6 paramètres de l'onglet Prédéfinition de conversion (1). Régler ces paramètres en cliquant sur les "..." à droites de chaque paramètre (2)  :

![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad1.PNG)

Chaque paramètre doit être réglé de la façon suivante : 

![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad2.PNG)
![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad3.PNG)
![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad4.PNG)
![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad5.PNG)
![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad6.PNG)
![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad7.PNG)

Cliquer sur enregistrer réglages et fermer pour sauvegarder votre configuration d’export en IFC.

## Export en IFC

Ouvrer une vue ne contenant que les éléments que vous souhaitez exporter \(un seul bâtiment par exemple\) :

![](/02_Modelisation/00_communs/images/export-archicad/ARCHICAD_06.PNG)

Afficher les zones dans la vue 3D afin que ces zones soient exportée

![](/02_Modelisation/00_communs/images/export-archicad/ARCHICAD_07.PNG)   
Cliquer sur enregistrer sous :

![](/02_Modelisation/00_communs/images/export-archicad/ARCHICAD_08.png)
![](/02_Modelisation/00_communs/images/export-archicad/ARCHICAD_09.PNG)

Cliquer sur « Enregistrer »

{% endblock %}