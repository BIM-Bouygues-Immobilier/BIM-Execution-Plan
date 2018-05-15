{% extends "/templates/softwares/revit.md" %}


{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Votre modèle peut ainsi être séparé en 2 modèles, Voirie et Jardin, par exemple.{% endblock %}

{# Donne des recommendation de modélisaiton générales propre au lot#}
{% block lot_specifique_generalites %}
* [Modélisation des site](#sites)
* [Modélisation des sols](#sols)
* [Modélisation des équipements spécialisés](#equipements sepcialises)
* [Modélisation des parkings](#parkings)
* [Modélisation du mobilier](#mobilier)
* [Modélisation des plantes](#plantes){% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}
### Modélisation des sites{#sites}

{% include "/categories/paysagiste/sites.md"  %}

### Modélisation des sols{#sols}

{% include "/categories/paysagiste/sols.md"  %}

### Modélisation des équipements spécialisés{#equipements specialises}

{% include "/categories/paysagiste/equipements specialises.md"  %}

### Modélisation des parkings{#parkings}

{% include "/categories/paysagiste/parkings.md"  %}

### Modélisation du mobilier{#mobilier}

{% include "/categories/paysagiste/mobilier.md"  %}

### Modélisation des plantes{#plantes}

{% include "/categories/paysagiste/plantes.md"  %}

{% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}


{% endblock %} 