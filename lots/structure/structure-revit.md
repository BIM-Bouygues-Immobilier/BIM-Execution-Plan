{% extends "/templates/softwares/revit.md" %}
{% set logiciel = "Revit" %}

{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Votre modèle peut ainsi être séparé en 2 modèles, Infrastructe et Superstructure, par exemple.{% endblock %}

{# Donne des recommendation de modélisaiton générales propre au lot#}
{% block lot_specifique_generalites %}{% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}* [Plans de surface](#surface)
* [Pièces](#piece)
* [Logements](#logements)
* [Places de parking](#parking)
* [Modélisation des murs](#murs)
* [Placards](#placards){% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}

{% endblock %}