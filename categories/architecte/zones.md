#### Réglages préliminaires 

Les pièces constituants un logement doivent être regroupées ensembles. Il est nécéssaire d'ajouter les propriétés suivantes aux pièces à l'aide de trois paramètres du projet :

* Nature
* Typologie
* Collection

Ces trois paramètres permettent de créer des IfcZones au moment de l'export IFC

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Nature | Voir [« Nature des lots »](#nature_logement) ci-dessous | Cette propriété permet de définir la nature du lot|
| Typologie | Voir [« Typologie des lots »](#typologie_logement) ci-dessous | Cette propriété permet de préciser la typologie du lot (T1, T2, ...).|
| Collection | Voir [« Collections »](#collection) ci-dessous  | Cette propriété permet de préciser la collection du lot.|

Ces propriétés doivent être renseignées à la main, en y inscrivant le code correspondant.

#### modélisation

Pour regrouper les pièces en zone, utiliser l'outil Zone (1). 

![ZonesRevit01](/02_Modelisation/02_architecte/images/ZonesRevit01.PNG)

Assurez-vous d'avoir ajouté toutes les pièces du logement dans la zones, grâce à la fonctionnalité Ajouter un espace (2), puis cliquer sur Finir la modification de la zone (3). Enfin, renseinger les 3 proprités de la zone décrites précédement avec les codes correspondants (4). Pour cela, se référer aux _[tableaux ci-dessous](#nature_logement):_

![ZonesRevit02](/02_Modelisation/02_architecte/images/ZonesRevit02.PNG)

##### Nature des Lots{#nature_logement}

{% include "/00_Referentiel/NatureDesLogements.md"  %}

##### Typologie des lots{#typologie_logement}

{% include "/00_Referentiel/TypologieDesLogements.md"  %}

##### Collections{#collection}

{% include "/00_Referentiel/Collection.md"  %}