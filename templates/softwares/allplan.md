{% extends "/templates/modelisation.md" %}
{% set logiciel = "Allplan" %}

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

Pour pouvoir exporter le projet en format IFC2X3:

* Aller dans le browser de projet et sélectionner la commande "Exporter" et ensuite "Exportation des données IFC 2X3":

![EXP1](/02_Modelisation/00_communs/images/EXP1.png)

* Choisir les calques dont on souhaite faire l'export dans l'interface "Choix calque", qui montre la base du projet complète:

![EXP2](/02_Modelisation/00_communs/images/EXP2.PNG)

* Remplir le chemin d'export et le nom du fichier et vérifier que dans le type de fichier, l'option "Fichiers IFC 2X3 (*.ifc) est bien sélectionnée.
Si nécessaire, il est possible d'accèder aux paramètres supplémentaires d'export.

![EXP3](/02_Modelisation/00_communs/images/EXP3.PNG)

### Réglages de l’export IFC

#### Configuration de l'export

Télécharger la configuration d'export : [Paramètres import export IFC BI](https://raw.githubusercontent.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/master/templates/softwares/Configuration%20IFC%20Cahier%20des%20Charges%20BIM%20BI.json) _(Clic-droit, puis "Enregistrer le lien/la cible sous...")_

Dans l'interface de paramètres avancés, cliquer sur l'icône "Rechercher" (1), puis dans le dossier de téléchargements, sélectionner le fichier Paramètres import export IFC BI (2) que vous venez de télécharger et cliquer sur Ouvrir (3).
Paramètre import export IFC BI va alors apparaître dans la liste des Favoris disponibles (4). Sélectionnez le, et cliquez sur OK (5).

![ExportIFCRevit6](/02_Modelisation/00_communs/images/export-allplan/ParametresIFCAllplan01.PNG)

#### Configuration manuelle

_Si vous ne souhaitez pas utiliser la configuration automatique,_ vous pourrez utiliser les réglages décrit ci-dessous :

Pour configurer manuellement l'export IFC, cliquer sur "Paramètres", la fenêtre de paramètres d'import et d'export va s'ouvrir. Régler les paramètres de la façon suivante:

![ExportIFCRevit6](/02_Modelisation/00_communs/images/export-allplan/ParametresIFCAllplan1.PNG)

{% endblock %}