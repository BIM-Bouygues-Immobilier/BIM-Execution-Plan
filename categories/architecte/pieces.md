#### Généralités

Les Surfaces Habitables (S.H.A.B.) sont calculées à partir de la modélisation des pièces du projet.

L’ensemble des locaux du projet doivent être présents dans la maquette numérique. En plus des locaux « nobles » du programme, cette modélisation doit inclure tous les autres types de locaux, tel que les circulations, les locaux techniques, les gaines techniques, …

Les locaux doivent être représentés et décomposés en locaux fonctionnels (Chambre, Séjour, Hall, …), même si ces locaux appartiennent à un espace physique plus important. Par exemple, un séjour et une cuisine ouverts l'un sur l'autre devront être représentés comme deux locaux distincts.

Les locaux doivent être modélisés depuis le sol fini jusqu’au plafond fini. En l’absence de faux-plafonds, les locaux doivent être modélisés jusqu’à la hauteur libre prévue par le programme. Les locaux doivent être identifiés par leur nom, en suivant les valeurs du tableau ["Nom des pièces"](#Nom_pieces) ci-dessous.

#### Modélisation

{% if logiciel == "Revit" %}

Dans Revit, ces locaux doivent être modélisé à l’aide de l’outil Pièce :

![Pièces](/02_Modelisation/02_architecte/images/SURFACE_02.PNG)

Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Nom | Voir [« Nom des pièces »](#Nom_pieces) ci-dessous | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Commentaire | Voir [« Destination des pièces »](#destination_piece) ci-dessous| Cette propriété indique la destination des pièces réalisées. |
| Décalage limite | Hauteur libre \(en m\) | Cette propriété permet d’indiquer la hauteur libre dans le local. Les propriétés « Niveau » et « Limite supérieure » doivent donc également avoir la même valeur. |

On completera également le revêtement de sol :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Finition du sol | Voir [« Revêtements de sols »](#revêtements_sols) ci-dessous | Cette propriété indique le type de revêtement de sol dans la pièce. |

#### Exemple

![Propriétés des pièces](/02_Modelisation/02_architecte/images/pieces_proprietes_logement.png)

{% elif logiciel == "ArchiCAD" %}

Dans ArchiCAD, ces locaux doivent être modélisé à l’aide de l’outil Zone :

![](/02_Modelisation/02_architecte/images/Zones.png)

Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Catégorie de Zone | Rooms| Toutes les zones sont dans la catégorie Rooms |
| Nom | Voir « Nom des pièces » | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Hauteur | Hauteur libre \(en m\) | Cette propriété permet d’indiquer la hauteur libre dans le local.|

#### Zones

Afin de regrouper ces pièces, il est nécéssaire d'ajouter les propriétés suivantes à l'aide d'un paramètre partagé :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| ZoneDescription | Voir « Nom des zones » | Cette propriété permet de regrouper plusiseurs pièces en une seule zone, par exemple un appartement. Ce paramètre peut n'être saisi qu'une seule fois par zone. |
| ZoneName | Un numéro unique | Cette propriété permet d'identifier la zone.|
{% include "../../00_Referentiel/NomDesZones.md"  %}

{% include "/00_Referentiel/NomDesProduits.md" %}

{% elif logiciel == "Allplan" %}

Dans Allplan, ces locaux doivent être modélisé à l’aide de l’outil Pièce.

Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Fonction | Voir [« Nom des pièces »](#Nom_pieces) ci-dessous | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Description | Voir [« Destination des pièces »](#destination_piece) ci-dessous| Cette propriété indique la destination des pièces réalisées. |

On completera également le revêtement de sol :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Finition du sol | Voir [« Revêtements de sols »](#revêtements_sols) ci-dessous | Cette propriété indique le type de revêtement de sol dans la pièce. |

#### Exemple

![Propriétés des pièces](/02_Modelisation/02_architecte/images/ROOM1.PNG)

{% else %}

{% endif %}

#### Pièces sous 1,80 m

On découpe la pièce en séparant les espaces sous 1,80 m. On appele ces espaces "COMBLE".

#### Nom des pièces{#Nom_pieces}

Le tableau ci-dessous liste les noms de pièces à utiliser sur l'operation:

{% include "/00_Referentiel/NomDesPieces.md" %}

#### Revêtements de sols{#revêtements_sols}

{% include "/00_Referentiel/TypesDeRevetements.md" %}

#### Destination des pièces{#destination_piece}

Le tableau ci-dessous liste les destinations possible pour une pièces:

{% include "/00_Referentiel/NomDesProduits.md" %}

