{% extends "/templates/softwares/allplan.md" %}


{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Vous pouvez par exemple séparer votre modèle en deux, Réseaux et Mobiliers{% endblock %}

{# Donne des recommendation de modélisation générales propre au lot#}
{% block lot_specifique_generalites %}
## Assignation des catégories

Tous les objets du modèle devront être modélisés avec des familles qui soient affectées à une catégorie {{logiciel}} cohérente avec la fonction de l'élément même: 

* Equipements électriques
* Equipements de génie climatique et de plomberie
* Terminaux horizontaux et verticaux
* Accessoires de gaine et de canalisation
* Equipements sanitaires 
* Equipements spécialisés
* Mobilier

Aucun objet ne devra être modélisé en "Modèle Générique".

### Positionnement des attentes

Pour fluidifier les échanges avec le BET Fluides, il est conseillé de matérialiser via, par exemple, des éléments d'annotations visibles au moins dans les vues en plan, les éléments suivants:
* Attentes EFS, ECS, EFAdoucie
* Siphon de sol
* Attentes évacuation EUG
* Attentes évacuation EU
* Hottes
* Attentes évacuation chambres froides
* ...

Ces éléments pourront être soit intégrés dans des familles soit faire objet de familles spécifiques et être positionnés dans un sous-projet à part. 
{% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}
* [Modélisation des réseaux](#reseaux){% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}
## Modélisation des réseaux{#reseaux}

{% include "/categories/plomberie/reseaux.md" %}
{% endblock %}