Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) sont calculées en additionnant les différents types de surfaces du projet. De plus, la représentation des surfaces de parkings extérieurs est attendue.

{% if logiciel == "Revit" %}

####Préparation

Avant la création d'un plan de surfaces, créer un type de plan de surfaces (l'appeler BI par exemple (1) ), et s'assurer que tous les plans de surfaces crées soient de ce type. Pour créer un nouveau type de plan de surfaces, utiliser la fonctionalité Calculs des surfaces et des volumes dans l'onglet Pièces et surfaces (2), puis cliquer sur Nouveau (3) comme dans l'image suivante: 

![Plan de surface](/02_Modelisation/02_architecte/images/SURFACE_03.PNG)

{% endif %}

#### Modélisation

{% if logiciel == "Revit" %}

L’ensemble de ces surfaces SHOB/SHON/SDP est représenté à l’aide d’un unique plan de surface par niveau :

![Plan de surface](/02_Modelisation/02_architecte/images/SURFACE_01.PNG)

Les surfaces modélisées doivent couvrir l'ensemble de l'emprise du projet, à tout les niveaux. Le niveau N00 (Rez-De-Chaussé) doit également contenir les surfaces extérieures au bâtiment lui-même (VRD, parking extérieur, ...).

Chaque surface dessinée dans ces plans doit avoir les propriétés suivantes :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Nom | Voir [« Noms des surfaces »](#nom_surface) ci-dessous | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. |
| Commentaire | Voir [« Types de surfaces »](#types_surface) ci-dessous| Cette propriété indique la destination des surfaces réalisées. |

Si un même niveau contient des surfaces ayant des usages différents (par exemple, surface de plancher de commerce et de logement), chaque usage doit être réprésenté par une surface distincte.

{% elif logiciel == "ArchiCAD" %}

L’ensemble de ces surfaces SHOB/SHON/SDP est modélisé à l’aide de l'outil Zone :

![](/02_Modelisation/02_architecte/images/Zones.png)

Chaque Zone dessinée doit alors avoir les propriétés suivantes :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Catégorie de Zone | Area | Toutes les zones sont dans la catégorie Area |
| Nom | Voir "Noms des surfaces" ci-dessous | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. |

La propriété « Description » est accessible en faisant un clic-droit sur une zone sélectionnée (1), puis « Options Zones sélectionnées » (2), puis « Gérer propriétés IFC... » (3), puis en cochant « Description » (4). La propriété est alors disponible dans « Options Zones sélectionnées » (5):

![](/02_Modelisation/02_architecte/images/Description.png)

{% elif logiciel == "Allplan" %}

Des objets "Pièces" devront être modélisés spécifiquement pour permettre ce calcul.

Les pièces modélisées doivent couvrir l'ensemble de l'emprise du projet, à tout les niveaux. Le niveau N00 (Rez-De-Chaussé) doit également contenir les surfaces extérieures au bâtiment lui-même (VRD, parking extérieur, ...).

Chaque surface dessinée dans ces plans doit avoir les propriétés suivantes :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Fonction | Voir [« Noms des surfaces »](#nom_surface) ci-dessous | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. |
| Description | Voir [« Types de surfaces »](#types_surface) ci-dessous| Cette propriété indique la destination des surfaces réalisées. |

Si un même niveau contient des surfaces ayant des usages différents (par exemple, surface de plancher de commerce et de logement), chaque usage doit être réprésenté par une surface distincte.

Le renseignement de la destination des pièces devra se faire dans la propriété IFC "Description" :
* Pour assigner cette propriété aux pièces du projet, aller dans l'interface "Attributs" dans la palette des propriétés de la pièce, dans le champs "Attributs généraux". 
* Cliquer ensuite sur l'option "Assigner un nouvel attributs" pour accéder à la palette "Définir et assigner des attributs" :
![](/02_Modelisation/02_architecte/images/ROOM2.PNG)
* Aller dans les groupe des attributs "IFC" et choisir l'attribut "Description"
![](/02_Modelisation/02_architecte/images/ROOM3.PNG)
* Remplir enfin le paramètre avec la valeur correcte parmi celles listées ci-dessous :
![](/02_Modelisation/02_architecte/images/ROOM4.PNG)

{% else %}

{% endif %}

#### Exemples

##### Niveau de parking

![Niveau de parking](/02_Modelisation/02_architecte/images/Surfaces_ExempleNiveauParking.png)

##### Niveau courant

![Niveau courant](/02_Modelisation/02_architecte/images/Surfaces_ExempleNiveauCourant.png)

Les surfaces doivent être nommée de la façon suivante : 

#### Noms des surfaces{#nom_surface}

{% include "/00_Referentiel/NomDesSurfaces.md"  %}

#### Types de surface{#types_surface}

{% include "/00_Referentiel/NomDesProduits.md" %}