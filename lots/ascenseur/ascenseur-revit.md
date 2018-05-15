{% extends "/templates/softwares/revit.md" %}
{% set logiciel = "Revit" %}

{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Votre modèle sera unique, étant donné que le sujet qui vous concerne est composé des cages d'ascenseurs et les ascenseurs eux mêmes.{% endblock %}

{# Donne des recommendation de modélisaiton générales propre au lot#}
{% block lot_specifique_generalites %}{% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}
* [Modélisation des cages d'ascenseurs](#cages-ascenseurs)
* [Modélisation des ascenseurs](#ascenseurs){% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}
### Modélisation des cages d'ascenseurs{#cages-ascenseurs}

{% include "/categories/ascenseurs/cages-ascenseurs.md"  %}

### Modélisation des ascenseurs{#ascenseurs}

{% include "/categories/ascenseurs/ascenseurs.md"  %}
{% endblock %}