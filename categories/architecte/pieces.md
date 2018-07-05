#### Généralités

Les Surfaces Habitables (S.H.A.B.) sont calculées à partir de la modélisation des pièces du projet.

L’ensemble des locaux du projet doivent être présents dans la maquette numérique. En plus des locaux « nobles » du programme, cette modélisation doit inclure tous les autres types de locaux, tel que les circulations, les locaux techniques, les gaines techniques, …

Les locaux doivent être représentés et décomposés en locaux fonctionnels (Chambre, Séjour, Hall, …), même si ces locaux appartiennent à un espace physique plus important. Par exemple, un séjour et une cuisine ouverts l'un sur l'autre devront être représentés comme deux locaux distincts.

Les locaux doivent être modélisés depuis le sol fini jusqu’au plafond fini. En l’absence de faux-plafonds, les locaux doivent être modélisés jusqu’à la hauteur libre prévue par le programme. Les locaux doivent être identifiés par leur nom, en suivant les valeurs du tableau ["Nom des pièces"](#Nom_pieces) ci-dessous.

{% if logiciel == "Revit" %}

#### Tableaux de valeurs Revit BI

Avant de modéliser, assurez vous de charger les Tableaux de valeurs Revit BI dans votre protjet. Télécharger les tableaux : [les Tableaux de valeurs Revit BI](https://raw.githubusercontent.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/master/templates/softwares/Configuration%20IFC%20Cahier%20des%20Charges%20BIM%20BI.json) _(Clic-droit, puis "Enregistrer le lien/la cible sous...")_

Pour charger les Tableaux de valeurs Revit BI dans votre projet, aller dans l'onglet Insérer (1), cliquer sur Insérer à partir du fichier, puis sur Insérer des vues à partir du fichier (2).

![Pièces02](/02_Modelisation/02_architecte/images/PiecesRevit02.PNG)

Parcourir l'explorateur de fichiers jusqu'au dossier où est stocké le fichier Tableaux de valeurs Revit BI (3), le sélectionner, puis cliquer sur Ouvrir (4).

![Pièces03](/02_Modelisation/02_architecte/images/PiecesRevit03.PNG)

Dans la nouvelle fenêtre qui s'affiche, sélectionner la ou les nomenclatures proposées (5), puis cliquer sur OK (6).

![Pièces04](/02_Modelisation/02_architecte/images/PiecesRevit04.PNG)

#### Modélisation

Dans Revit, ces locaux doivent être modélisés à l’aide de l’outil Espace (1), situé dans l'onglet Analyser (2) :

![Pièces01](/02_Modelisation/02_architecte/images/PiecesRevit01.PNG)

Lorsqu'une pièce  est modélisée, sélectionner un nom pour le paramètre "Type de la pièce" (3) dans le groupe de paramètres "Données d'identification" (4).

![Pièces05](/02_Modelisation/02_architecte/images/PiecesRevit05.PNG)

Veiller à ne pas renseigner ce paramètre à la main, mais de choisir uniquement parmi les types proposés dans le Tableau de valeurs Revit BI.
Chaque type est associé à un code unique, que nous récupérons et réutilisons dans les export IFC.
Vous trouverez la liste complète des types de pièces dans le tableau ci-dessous : [« Nom des pièces »](#Nom_pieces).

{% elif logiciel == "ArchiCAD" %}

#### Modélisation

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

#### Modélisation

Dans Allplan, ces locaux doivent être modélisé à l’aide de l’outil Pièce.

![PiecesAllplan](/02_Modelisation/02_architecte/images/PiecesAllplan.PNG)

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

Concernant les combles, l'espace dont la hauteur sous plafond est de moins d'1,80m n'est pas pris en compte dans le calcul de la surface. Dans l'image ci dessous, il s'agit de l'espace à l’extérieur des deux droites en pointillés verts.

![Combles1](/02_Modelisation/02_architecte/images/Combles1.PNG)

 Il faut créer une ou plusieurs pièces supplémentaires (avec l'outil Espace), que l'on va nommer Combles, regroupant tous ces espaces dont la hauteur sous plafond est inférieure à 1,80m. Pour cela, utiliser l'outil Séparateur d'espaces.  Enfin, renommer correctement vos pièces. Vous devez avoir une pièce principale, et une ou plusieurs pièces nommées Combles, comme sur l'image ci dessous:

![Combles2](/02_Modelisation/02_architecte/images/Combles2.PNG)

#### Nom des pièces{#Nom_pieces}

Le tableau ci-dessous liste les noms de pièces à utiliser sur l'opération:

{% include "/00_Referentiel/NomDesPieces.md" %}