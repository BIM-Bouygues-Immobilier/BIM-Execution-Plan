{% extends "/templates/softwares/revit.md" %}
{% set logiciel = "Revit" %}

{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Votre modèle peut ainsi être séparé en 2 modèles, Voirie/Site et Réseaux, par exemple.{% endblock %}

{# Donne des recommendation de modélisaiton générales propre au lot#}
{% block lot_specifique_generalites %}{% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}
* [Modélisation des équipements VRD](#equipements VRD)
* [Modélisation du mobilier](#mobilier)
* [Modélisation des réseaux](#reseaux)
* [Modélisation de la topographie](#topographie)
* [Modélisation de la végétation](#vegetation)
* [Modélisation de la voirie](#voirie){% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}

### Modélisation des équipements VRD{#equipements VRD}

{% include "/categories/VRD/equipements VRD.md"  %}

### Modélisation du mobilier{#mobilier}

{% include "/categories/VRD/mobilier.md"  %}

### Modélisation des réseaux{#reseaux}

{% include "/categories/VRD/reseaux.md"  %}

### Modélisation de la topographie{#topographie}

{% include "/categories/VRD/topographie.md"  %}

### Modélisation de la végétation{#vegetation}

{% include "/categories/VRD/vegetation.md"  %}

### Modélisation de la voirie{#voirie}

{% include "/categories/VRD/voirie.md"  %}

{% endblock %}