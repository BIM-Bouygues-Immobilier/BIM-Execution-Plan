{% extends "/templates/softwares/archicad.md" %}

{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Vous pouvez par exemple séparer votre modèle en deux, Décoration et Mobiliers{% endblock %}

{# Donne des recommendation de modélisation générales propre au lot#}
{% block lot_specifique_generalites %}
### Assignation des catégories

Tous les objets du modèle devront être modélisés avec des familles qui soient affectées à une catégorie {{logiciel}} cohérente avec la fonction de l'élément même: 

* Luminaires
* Terminaux horizontaux et verticaux
* Mobilier
* Equipements spécialisés
* Murs, sols, plafonds

Aucun objet ne devra être modélisé en "Modèle Générique". 

### Utilisation des références 

De manière générale, dans les modèles Décorateur les éléments de structure (dalles, poteaux, voiles ...), d'architecture (cloisons, plafonds, ...) éventuellement importés comme référence de dessin, devront être positionnées sur un sous-projet à part de manière à pouvoir les isoler facilement. 
Ce principe s'appliquera aussi aux terminaux horizontaux et verticaux (luminaires, trappes ...) qui seront en interface avec les lots techniques. 

### Modélisation avec les masses volumétriques

Les masses volumétriques qui seront éventuellement utilisé comme support à la modélisation (par exemple pour des murs avec des formes libres), devront être supprimés avant l'export et la diffusion des modèles, afin de ne pas gêner la modélisation des autres intervenants. 
{% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}{% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}

{% endblock %}