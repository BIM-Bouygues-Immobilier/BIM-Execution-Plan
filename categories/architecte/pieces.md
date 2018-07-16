#### Généralités

Les Surfaces Habitables (S.H.A.B.) sont calculées à partir de la modélisation des pièces du projet.

L’ensemble des locaux du projet doivent être présents dans la maquette numérique. En plus des locaux « nobles » du programme, cette modélisation doit inclure tous les autres types de locaux, tel que les circulations, les locaux techniques, les gaines techniques, …

Les locaux doivent être représentés et décomposés en locaux fonctionnels (Chambre, Séjour, Hall, …), même si ces locaux appartiennent à un espace physique plus important. Par exemple, un séjour et une cuisine ouverts l'un sur l'autre devront être représentés comme deux locaux distincts.

Les locaux doivent être modélisés depuis le sol fini jusqu’au plafond fini. En l’absence de faux-plafonds, les locaux doivent être modélisés jusqu’à la hauteur libre prévue par le programme. Les locaux doivent être identifiés par leur nom, en suivant les valeurs du tableau ["Nom des pièces"](#Nom_pieces) ci-dessous.

{% if logiciel == "Revit" %}

#### Tableaux de valeurs Revit Bouygues Immobilier

Avant de modéliser, assurez vous de charger les Tableaux de valeurs Revit Bouygues Immobilier dans votre protjet. Télécharger les tableaux : _[Tableaux de valeurs Revit Bouygues Immobilier](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/blob/master/templates/softwares/revit/Tableaux%20de%20valeurs%20Revit%20Bougyes%20Immobilier.rvt?raw=true)_

Pour charger les Tableaux de valeurs Revit Bouygues Immobilier dans votre projet, aller dans l'onglet Insérer (1), cliquer sur Insérer à partir du fichier, puis sur Insérer des vues à partir du fichier (2).

![Pièces02](/02_Modelisation/02_architecte/images/PiecesRevit02.PNG)

Parcourir l'explorateur de fichiers jusqu'au dossier où est stocké le fichier Tableaux de valeurs Revit Bouygues Immobilier (3), le sélectionner, puis cliquer sur Ouvrir (4).

![Pièces03](/02_Modelisation/02_architecte/images/PiecesRevit03.PNG)

Dans la nouvelle fenêtre qui s'affiche, sélectionner toutes les nomenclatures proposées (5), puis cliquer sur OK (6).

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

#### Réglages et imports préliminaires

Avant de modéliser, assurez vous d'avoir:

* Importé le Traducteur général Bouygues Immobilier comme traducteur IFC, ou fait la configuration manuellement comme demandé (voir [Procédure d'export en IFC](#export))
* Importé le paramètre "Type de la pièce". Pour cela, aller dans l'onglet Option (1), puis ouvrir le Gestionaire de propriétés (2)

![Pièces06](/02_Modelisation/02_architecte/images/PiecesArchicad01.png)

Après avoir téléchargé le fichier _[Propriété ArchiCAD Type de pièce](https://raw.githubusercontent.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/master/templates/softwares/archicad/Propri%C3%A9t%C3%A9%20ArchiCAD%20Type%20de%20pi%C3%A8ce.xml)_  _(Clic-droit, puis "Enregistrer le lien/la cible sous...")_ cliquer sur Importer (3), puis dans le dossier de téléchargements, sélectionner le fichier "Propriété ArchiCAD Type de pièce" (4) que vous venez de télécharger et cliquer sur Ouvrir (5). 

![Pièces07](/02_Modelisation/02_architecte/images/PiecesArchicad02.png)

La nouvelle propriété sera disposible dans la liste des propriété de zone (6). cliquer enfin sur OK pour valider l'importation (8).

![Pièces08](/02_Modelisation/02_architecte/images/PiecesArchicad03.png)

#### Modélisation

Dans ArchiCAD, ces locaux doivent être modélisé à l’aide de l’outil Zone :

![Pièces09](/02_Modelisation/02_architecte/images/Zones.png)

Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Type de la pièce | Voir [« Nom des pièces »](#Nom_pieces) | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Hauteur | Hauteur libre \(en m\) | Cette propriété permet d’indiquer la hauteur libre dans le local.|

Pour nommer chaque pièce et renseigner son type, se référer au tableau [Nom des pièces](#Nom_pieces). Ouvrir les options de la zone (sélectioner la zone, clique droit puis sur Options zones sélectionnées (1)), indiquer le nom de la pièce dans la case Nom (2) et le numéro de la pièce dans la case N° (3). Pour la hauteur de la pièces, utiliser les cases juste en dessous (4) pour la configurer comme souhaité.
Pour renseigner le paramètre Type de la pièce, aller dans l'onglet Classification et propriétés (5), puis le sous onglet Zone et indiquer manuellement le code à trois lettre correspondant au type de la pièce (6).

![Pièces10](/02_Modelisation/02_architecte/images/PiecesArchicad04.png)

{% elif logiciel == "Allplan" %}

#### Réglages préliminaires

Avant de modéliser, assurez-vous d'avoir créé l'attribut Code_Bouygues_Immobilier. Lors de la création de la première pièce, la sélectionner, cliquer droit dessus, puis sur Modifier des attributs (1). Cliquer ensuite sur Assigner un nouvel attribut (2).

![PiecesAllplan01](/02_Modelisation/02_architecte/images/PiecesAllplan01.png)

Dans la fenêtre qui s'ouvre, sélectionner l'onglet Utilisateur (3). Pour créer un nouvel attribut, cliquer sur l'icône du milieu en haut à droite (4), puis dans la nouvelle fenêtre qui s'ouvre, remplir les information comme indiqué (5). Soyez _très_ vigilant au nom de l'attribut, il doit précisément être "Code_Bouygues_Immobilier", ne pas hésiter à le copier-coller. Cliquer sur OK (6), puis l'attribut sera ajouté à la liste des attributs disponibles (7). Cliquer enfin sur OK (8) pour que l'attribut soit ajouté aux attributs de la pièce (9).

![PiecesAllplan02](/02_Modelisation/02_architecte/images/PiecesAllplan02.png)

![PiecesAllplan03](/02_Modelisation/02_architecte/images/PiecesAllplan03.png)

Vous devrez ajouter l'attribut Code_Bouygues_Immobilier manuellement à chaque fois que vous créez une nouvelle pièce; vous pouvez également utiliser la fonction Reprendre les propriétés (10), en cliquant sur une pièce précédemment crée. Cette nouvelle pièce disposera automatiquement de l'attribut Code_Bouygues_Immobilier parmi sa liste d'attributs.

![PiecesAllplan04](/02_Modelisation/02_architecte/images/PiecesAllplan04.png)

#### Modélisation

Dans Allplan, ces locaux doivent être modélisés à l’aide de l’outil Pièce.

![PiecesAllplan](/02_Modelisation/02_architecte/images/PiecesAllplan.PNG)

Les attributs suivants sont à compléter :

| Attribut | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Code_Bouygues_Immobilier | Voir [« Nom des pièces »](#Nom_pieces) ci-dessous | Cet attribut indique le type de local, suivant la décomposition décrite ci-dessus. |
| Hauteur | Hauteur libre \(en m\) | Cet attribut permet d’indiquer la hauteur libre dans le local.|

Lors de la création de chaque pièce, renseigner manuellement l'attribut Code_Bouygues_Immobilier (1), avec le code correspondant à la fonction de la pièce. Pour cela, se référer au tableau [Nom des pièces](#Nom_pieces) où sont listés les codes des pièces.

![PiecesAllplan05](/02_Modelisation/02_architecte/images/PiecesAllplan05.png)

{% else %}

{% endif %}

#### Pièces sous 1,80 m

Concernant les combles, l'espace dont la hauteur sous plafond est de moins d'1,80m n'est pas pris en compte dans le calcul de la surface. Dans l'image ci dessous, il s'agit de l'espace à l’extérieur des deux droites en pointillés verts.

![Combles1](/02_Modelisation/02_architecte/images/Combles1.PNG)

 Il faut créer une ou plusieurs pièces supplémentaires (avec l'outil Espace), que l'on va nommer Combles, regroupant tous ces espaces dont la hauteur sous plafond est inférieure à 1,80m. Pour cela, utiliser l'outil Séparateur d'espaces.  Enfin, renommer correctement les pièces. Vous devez avoir une pièce principale, et une ou plusieurs pièces nommées Combles, comme sur l'image ci dessous:

![Combles2](/02_Modelisation/02_architecte/images/Combles2.PNG)

#### Nom des pièces{#Nom_pieces}

Le tableau ci-dessous liste les noms de pièces à utiliser sur l'opération:

{% include "/00_Referentiel/NomDesPieces.md" %}