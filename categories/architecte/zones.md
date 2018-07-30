{% if logiciel == "Revit" %}

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

{% elif logiciel == "ArchiCAD" %}

Les Zones, au sens assemblage de pièces, n'existent pas dans ArchiCAD en tant que tel; les pièces conçues avec l'outils zones ne peuvent pas être regroupées. Pour faire apparaître des ifcZones dans l'export IFC, il faut les créer lors du découpage en lots du projet (voir [Découpage](#découpage)). Lorsque ce découpage est effectué, ajouter à chaque ifcZones (correspondant à chacun des logements) les 3 propriétés suivantes, en les mettant dans le Pset BI_Parameters (1) :

* Nature
* Typologie
* Collection

Pour cela, dans la fenêtre Gestionaire de projet IFC, cliquer sur Nouveau... (2), renseigner les différentes informations du nouveau paramètre (3), puis cliquer sur OK (4).
Pour chacun des logements, renseigner son nom (5) et la valeur de chaque propriété (6) à la main, en se référant aux _[tableaux ci-dessous](#nature_logement):_
Soyez _très_ vigilant au nom de chaque paramètre et codes, il est impératif qu'ils soient bien orthographiés (majuscules, tirets...). Ne pas hésiter à utiliser la fonction copier-coller.

![ZonesArchiCAD01](/02_Modelisation/02_architecte/images/ZonesArchiCAD01.PNG)

{% elif logiciel == "Allplan" %}

Les pièces constituants un logement doivent être regroupées ensembles. Pour cela, il faut créer un attribut pour les pièces, que vous aller nommer Numéro_du_Logement (1). Puis, renseigner manuelement cet attribut pour chaque pièce avec le numéro de logement correspondant (2).  

![ZonesAallplan01](/02_Modelisation/02_architecte/images/ZonesAllplan01.PNG)

Vous devez de même ajouter les 3 attributs suivants aux pièces, et en renseigner manuelement les valeurs : 

* Nature
* Typologie
* Collection

 Pour cela, se référer aux _[tableaux ci-dessous](#nature_logement):_

{% endif %}

##### Nature des Lots{#nature_logement}

{% include "/00_Referentiel/NatureDesLogements.md"  %}

##### Typologie des lots{#typologie_logement}

{% include "/00_Referentiel/TypologieDesLogements.md"  %}

##### Collections{#collection}

{% include "/00_Referentiel/Collection.md"  %}