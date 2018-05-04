{% extends "/templates/modelisation.md" %}

{# Décrit le format de fichier du logiciel #}
{% block logicel_format %}IFCZip (.ifczip){% endblock %}

{# Décrit la procédure de georeférencement #}
{% block logiciel_geopositionnement %}
{% endblock %}

{# Décrit la procédure d'export en IFC #}
{% block logiciel_export %}

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