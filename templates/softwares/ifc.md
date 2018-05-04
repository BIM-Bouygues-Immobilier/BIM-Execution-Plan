{% extends "/templates/modelisation.md" %}

{# Décrit le format de fichier du logiciel #}
{% block logicel_format %}IFCZip (.ifczip){% endblock %}

{# Décrit la procédure de georeférencement #}
{% block logiciel_geopositionnement %}
{% endblock %}

{# Décrit la procédure d'export en IFC #}
{% block logiciel_export %}

### Généralités

Pour chaque lot, il est nécessaire de déposer un seul fichier, au format IFC2X3, incluant tous les éléments nécessaires à la bonne compréhension du projet pour la phase en cours, et purgé de tous les éléments non nécessaires au sujet en cours.
Avant d'exporter, il est nécessaire de ramener les offset en X et Y dans la fenêtre des paramètres du projet à zéro.

### Renseignement de l'adresse du projet

Les informations suivantes doivent être remplies dans le IfcPostalAdress et associées au IfcBuilding :

| Paramètre | Valeur |
| :--- | :--- |
| Purpose | User defined |
| Description | Type d'intervention \(Rénovation, Nouvelle construction, ...\) |
| User-Defined purpose | Destination \(Bureaux, Logements, Hôtel, ...\) |
| Address line 1 | L'adresse du projet |
| City | La ville du projet |
| Postal code | Le code postal du projet |
| State | La région du projet |
| Country | France |

{% endblock %}