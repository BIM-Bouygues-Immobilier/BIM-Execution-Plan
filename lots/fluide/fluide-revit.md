{% extends "/templates/softwares/revit.md" %}


{# Donne un exemple de découpage pour le lot #}
{% block lot_decoupage %}Votre modèle peut ainsi être séparé en 3 modèles, CVC, plomberie et électricité, par exemple.{% endblock %}

{# Donne des recommendation de modélisaiton générales propre au lot#}
{% block lot_specifique_generalites %}{% endblock %}

{# Ajoute la table des matières pour le lot#}
{% block specific_toc %}
* [Modélisation des CVC](#CVC)
* [Modélisation des unités de production d'eau chaude](#unites de production d'eau chaude)
* [Modélisation des réseaux de chauffage](#reseaux de chauffage)
* [Modélisation des aérothermes convecteurs](#aerothermes convecteurs)
* [Modélisation des extracteurs insuflateurs désemfumage](#extracteurs insuflateurs desemfumage)
* [Modélisation des réseaux de désemfumage](#reseaux de desemfumage)
* [Modélisation des CVF](#VCF)
* [Modélisation des CTA](#CTA)
* [Modélisation des réseaux de ventilation CVC](reseaux de ventilation CVC#)
* [Modélisation des ventilo-convecteurs](#ventilo-convecteurs)
* [Modélisation des bouches de VMC](#bouches de VMC)
* [Modélisation des équipements CVC](#equipements CVC)
* [Modélisation des équipements plomberie](#equipements plomberie)
* [Modélisation des réseaux d'eaux usées](#reseaux d'eau usees)
* [Modélisation des réseaux d'eaux vannes](#reseaux d'eau vannes)
* [Modélisation des pompes](#pompes)
* [Modélisation des accessoires sanitaires](#accessoires sanitaires)
* [Modélisation des colonnes sèches](#colonnes seches)
* [Modélisation des équipements électriques](#equipements electriques)
* [Modélisation des chemins de câbles](#chemin de cable)
* [Modélisation des équipements SSI](#equipements SSI)
* [Modélisation des équipements sûreté sécurité](#equipements-surete-securite)
{% endblock %}

{# Décrit les recommendations de modélisation spécifiques au lot et au logiciel #}
{% block lot_specifique_content %}

### Modélisation des CVC{#CVC}

{% include "/categories/CVC/CVC.md"  %}

### Modélisation des unités de production d'eau chaude{#unites de production d'eau chaude}

{% include "/categories/CVC/unites production eau chaude.md"  %}

### Modélisation des réseaux de chauffage{#reseaux de chauffage}

{% include "/categories/CVC/reseaux de chauffage.md"  %}

### Modélisation des aérothermes convecteurs{#aerothermes convecteurs}

{% include "/categories/CVC/aerothermes convecteurs.md"  %}

### Modélisation des extracteurs insuflateurs désemfumage{#extracteurs insuflateurs desemfumage}

{% include "/categories/CVC/extracteurs insuflateurs desemfumage.md"  %}

### Modélisation des Modélisation des réseaux de désemfumage{#reseaux de desemfumage}

{% include "/categories/CVC/reseaux de desemfumage.md"  %}

### Modélisation des VCF{#VCF}

{% include "/categories/CVC/VCF.md"  %}

### Modélisation des CTA{#CTA}

{% include "/categories/CVC/CTA.md"  %}

### Modélisation des réseaux de ventilation CVC{#reseaux de ventilation CVC}

{% include "/categories/CVC/reseaux de ventilation CVC.md"  %}

### Modélisation des ventilo-convecteurs{#ventilo-convecteurs}

{% include "/categories/CVC/ventilo-convecteurs.md"  %}

### Modélisation des bouches de VMC{#bouches de VMC}

{% include "/categories/CVC/bouches de VMC.md"  %}

### Modélisation des équipements CVC{#equipements CVC}

{% include "/categories/CVC/equipements CVC.md"  %}

### Modélisation des équipements plomberie{#equipements plomberie}

{% include "/categories/plomberie/equipements plomberie.md"  %}

### Modélisation des réseaux d'eaux usées{#reseaux d'eau usees}

{% include "/categories/plomberie/reseaux eaux usees.md"  %}

### Modélisation des réseaux d'eaux vannes{#reseaux d'eaux vannes}

{% include "/categories/plomberie/reseaux eaux vannes.md"  %}

### Modélisation des pompes{#pompes}

{% include "/categories/plomberie/pompes.md"  %}

### Modélisation des accessoires sanitaires{#sanitaires}

{% include "/categories/plomberie/accessoires sanitaires.md"  %}

### Modélisation des colonnes sèches{#colonnes seches}

{% include "/categories/plomberie/colonnes seches.md"  %}

### Modélisation des équipements électriques{#equipements electriques}

{% include "/categories/electricite/equipements electriques.md"  %}

### Modélisation des chemins de câbles{#chemins de cables}

{% include "/categories/electricite/chemins de cables.md"  %}

### Modélisation des équipements SSI{#equipements SSI}

{% include "/categories/SSI/equipements SSI.md"  %}

### Modélisation des équipements sûreté sécurité{#equipements-surete-securite}

{% include "/categories/surete-securite/equipements surete securite.md"  %}

{% endblock %}