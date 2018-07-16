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

#### Configuration du traducteur IFC

Télécharger le traducteur pour l'exportation  : _[Traducteur général Bouygues Immobilier](https://raw.githubusercontent.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/master/templates/softwares/Configuration%20IFC%20Cahier%20des%20Charges%20BIM%20BI.json)_ _(Clic-droit, puis "Enregistrer le lien/la cible sous...")_

Il s'agit d'un projet ArchiCAD vide, contenant le Traducteur général Bouygues Immobilier que vous allez importer dans votre propre projet.
Dans l'interface Traducteurs IFC, cliquer sur l'icône "Importer traducteur de fichier externe" (1), puis dans le dossier de téléchargements, sélectionner le fichier Configuration Cahier des Charges BIM BI (2) que vous venez de télécharger et cliquer sur Ouvrir (3).

![ExportIFCRevit02](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad02.PNG)

Il vous est demandé de choisir quels traducteurs vous souhaitez importer. sélectionner Traducteur général Bouygues Immobilier (4), puis cliquer sur Importer (5).

![ExportIFCRevit03](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad03.PNG)

Le traducteur pour l'exportation Traducteur général Bouygues Immobilier va alors apparaître dans la liste des traducteurs pour l'exportation disponibles (6). Sélectionnez le, et cliquez sur OK (7).

![ExportIFCRevit04](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad04.PNG)

#### Configuration manuelle

_Si vous ne souhaitez pas utiliser la configuration automatique,_ vous pourrez utiliser les réglages décrit ci-dessous :

Dupliquer le traducteur général pour créer un nouveau traducteur. Vous pouvez alors renommer ce nouveau traducteur :

![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad0.PNG)

Les propriétés sont configurables grâces aux 6 paramètres de l'onglet Prédéfinition de conversion (1). Régler ces paramètres en cliquant sur les "..." à droites de l'écran (2)  :

![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad1.PNG)

Chaque paramètre doit être réglé de la façon suivante :

|**Filtre Modèle**|**Correspondance des type**|
| :---: | :---: |
| ![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad2.PNG)| ![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad3.PNG)|
|**Conversion géométrique**|**Correspondance des propriétés**|
|![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad4.PNG)|![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad5.PNG)|
|**Conversion des données**|**Conversion des unités**|
|![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad6.PNG)|![](/02_Modelisation/00_communs/images/export-archicad/ExportIFCArchicad7.PNG)|

Cliquer sur OK pour sauvegarder votre configuration d’export en IFC.

## Export en IFC

Ouvrir une vue ne contenant que les éléments que vous souhaitez exporter \(un seul bâtiment par exemple\) :

![](/02_Modelisation/00_communs/images/export-archicad/ARCHICAD_06.PNG)

Afficher les zones dans la vue 3D afin que ces zones soient exportée

![](/02_Modelisation/00_communs/images/export-archicad/ARCHICAD_07.PNG)   
Cliquer sur enregistrer sous :

![](/02_Modelisation/00_communs/images/export-archicad/ARCHICAD_08.png)
![](/02_Modelisation/00_communs/images/export-archicad/ARCHICAD_09.PNG)

Cliquer sur « Enregistrer »

{% endblock %}