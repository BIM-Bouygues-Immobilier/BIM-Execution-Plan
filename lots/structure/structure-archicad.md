{% extends "/templates/softwares/archicad.md" %}
{% set logiciel = "ArchiCAD" %}

{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Votre modèle peut ainsi être séparé en 2 modèles, Infrastructe et Superstructure, par exemple.{% endblock %}

{# Donne des recommendation de modélisation générales propre au lot#}
{% block lot_specifique_generalites %}{% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}* [Modélisation des voiles](#murs)
* [Modélisation des planchers](#sols)
* [Modélisation des poteaux](#poteaux)
* [Modélisation des poutres](#poutres)
* [Modélisation des fondations](#fondations)
* [Modélisation des gardes-corps](#gardes-corps)
* [Modélisation des escaliers](#escaliers){% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}

### Modélisation des voiles{#murs}

{% include "/categories/structure/murs.md"  %}

### Modélisation des planchers{#sols}

{% include "/categories/structure/planchers.md"  %}

### Modélisation des poteaux{#poteaux}

{% include "/categories/structure/poteaux.md"  %}

### Modélisation des poutres{#poutres}

{% include "/categories/structure/poutres.md"  %}

### Modélisation des fondations{#fondations}

{% include "/categories/structure/fondations.md"  %}

### Modélisation des gardes-corps{#gardes-corps}

{% include "/categories/structure/gardes-corps.md"  %}

### Modélisation des escaliers{#escaliers}

{% include "/categories/structure/escaliers.md"  %}

{% endblock %}