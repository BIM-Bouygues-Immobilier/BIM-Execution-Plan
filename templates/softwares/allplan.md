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
Pour savoir comment différencier ces éléments, se référer au paragraphe [Découpage des modèles](#découpage).
Avant d'exporter, il est nécessaire de ramener les offset en X et Y dans la fenêtre des paramètres du projet à zéro.

### Procédure d’export

Pour pouvoir exporter le projet en format IFC2X3:

* Aller dans l'onglet Fichier et sélectionner la commande "Exporter" et ensuite "Exportation des données IFC...":

![EXP1](/02_Modelisation/00_communs/images/EXP1.png)

* Choisir les calques dont on souhaite faire l'export dans l'interface "Choix calque", qui montre la base du projet complète:

![EXP2](/02_Modelisation/00_communs/images/EXP2.PNG)

* Remplir le chemin d'export et le nom du fichier et vérifier que dans le type de fichier, l'option "Fichiers IFC 2X3 (*.ifc) est bien sélectionnée.
Si nécessaire, il est possible d'accèder aux paramètres supplémentaires d'export.

![EXP3](/02_Modelisation/00_communs/images/EXP3.PNG)

### Réglages de l’export IFC

#### Configuration de l'export

Télécharger la configuration d'export : _[Paramètres import export IFC Bouygues Immobilier](https://raw.githubusercontent.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/master/templates/softwares/allplan/Param%C3%A8tres%20import%20export%20IFC%20Bouygues%20Immobilier.nth)_ _(Clic-droit, puis "Enregistrer le lien/la cible sous...")_

Dans l'interface de paramètres avancés, cliquer sur l'icône "Rechercher" (1), puis dans le dossier de téléchargements, sélectionner le fichier Paramètres import export IFC Bouygues Immobilier (2) que vous venez de télécharger et cliquer sur Ouvrir (3).
Paramètres import export IFC Bouygues Immobilier va alors apparaître dans la liste des Favoris disponibles (4). Sélectionnez le, et cliquez sur OK (5).

![ExportIFCAllplan01](/02_Modelisation/00_communs/images/export-allplan/ParametresIFCAllplan01.PNG)

#### Configuration manuelle

_Si vous ne souhaitez pas utiliser la configuration automatique,_ vous pourrez utiliser les réglages décrit ci-dessous :

Pour configurer manuellement l'export IFC, cliquer sur "Paramètres", la fenêtre de paramètres d'import et d'export va s'ouvrir. Régler les paramètres de la façon suivante:

![ExportIFCAllplan02](/02_Modelisation/00_communs/images/export-allplan/ParametresIFCAllplan1.PNG)

### Configuration du dossier d'exportation des paramètres IFC

Pour que les attributs Allplan soient correctement reliés aux paramètres IFC lors de l'export, il faut ajouter un fichier texte à un endroit précis dans les dossier d'Allplan. Commencer par télécharger le fichier texte en question : _[User_PropertyMap_Allplan_TO_Ifc2x3.cfg](https://raw.githubusercontent.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/master/templates/softwares/allplan/User_PropertyMap_Allplan_TO_Ifc2x3.cfg)_ _(Clic-droit, puis "Enregistrer le lien/la cible sous...")_
Ouvrir ensuite l'application Allmenu 2018 (Allmenu 2017 pour une version Allplan 2017, etc), aller dans l'onglet Maintenance, puis cliquer sur Explorateur Windows, et enfin sur Documents CAO personnalisés (USR).

![ExportIFCAllplan03](/02_Modelisation/00_communs/images/export-allplan/ParametresIFCAllplan03.PNG)

Un dossier nommé Local va s'ouvrir, c'est ici que vous devez copier le fichier User_PropertyMap_Allplan_TO_Ifc2x3.cfg (1). Veiller à ne pas éditer ce fichier texte, ni son contenu, ni son nom.

![ExportIFCAllplan04](/02_Modelisation/00_communs/images/export-allplan/ParametresIFCAllplan04.PNG)

{% endblock %}