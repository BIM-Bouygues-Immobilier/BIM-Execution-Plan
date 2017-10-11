# Modélisation des surfaces dans Revit

L'article suivant présente les recommandations de modélisation des surfaces dans le logiciel Autodesk Revit pour les maquettes numériques architecturales.

Aucune contrainte n'est imposé pour l'utilisation de l'outil "Espace".

## Surface Hors Œuvre Brut \(SHOB\) et Surface de Plancher \(SDP\)

### Généralités

Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) sont calculées en additionnant les différents types de surfaces du projet. De plus, la représentation des surfaces de parkings extérieurs est attendue.

### Décomposition des surfaces

Les surfaces du projet sont décomposées suivant ces valeurs:

{% include "../../00_Referentiel/NomDesSurfaces_Logement.md" %}

### Modélisation dans Revit

L’ensemble de ces surfaces SHOB/SHON/SDP est représenté à l’aide d’un plan de surface par niveau :

![](/02_Modelisation/02_architecte/images/SURFACE_01.PNG)Chaque surface dessinée dans ce plan doit alors avoir les propriétés suivantes :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Commentaire | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement de ces surfaces. Les surfaces en terrasses \(locaux techniques par ex.\) sont marquée « Extérieur » |
| Nom | Façade, Gaine Ascenseur Et Escaliers, Gaine Technique, 180, Parking, Parking Vélo, Circulation, Rampe, Allée, Voirie, Espace vert, Local technique, Cave, Palier, Livraison, Terrasse, SDP | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. |

## Places de parking

### Modélisation dans Revit

Les places de parking sont modélisées à l’aide d’une famille de la catégorie Parking. Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Commentaire | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement des places de parking. |

## Surface Utile Brute Locative \(SUBL\), Surface Utile Brute Bureaux \(SUBB\), Surface Utile Nette \(SUN\) et Surface Nette Bureaux \(SNB\)

### Généralités

Les Surfaces Utiles Brutes Locatives \(SUBL\), Surfaces Utiles Brutes Bureaux \(SUBB\), Surfaces Utiles Nettes \(SUN\) et Surfaces Nettes Bureaux \(SNB\) sont calculées à partir de la modélisation des locaux du projet.

L’ensemble des locaux du projet doivent être présents dans la maquette numérique. En plus des locaux « nobles » du programme, cette modélisation doit inclure tous les autres types de locaux, tel que les circulations, les locaux techniques, les gaines techniques, …

Les locaux doivent être représentés et décomposés en locaux fonctionnels \(Bureau, Salle de Réunion, Hall, …\), même si ces locaux appartiennent à un espace physique plus important. Par exemple, un hall et une cafétéria partageant le même espace physique devront être représentés comme deux locaux distincts.

Les locaux doivent être modélisés depuis le sol fini jusqu’au plafond fini. En l’absence de faux-plafonds, les locaux doivent être modélisés jusqu’à la hauteur libre prévue par le programme. Les locaux doivent être identifiés par leur nom, en suivant les valeurs du tableau VI.2 Décomposition des locaux.

### Décompositions des locaux

{% include "../../00_Referentiel/NomDesPieces_Logement.md" %}

### Modélisation dans Revit

Dans Revit, ces locaux doivent être modélisé à l’aide de l’outil Pièce :

![](/02_Modelisation/02_architecte/images/SURFACE_02.PNG)Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Commentaire | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement de ces surfaces. Les surfaces en terrasses \(locaux techniques par ex. sont marquée « Extérieur ». |
| Nom | Voir « Décompositions des locaux » | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Décalage limite | Hauteur libre \(en m\) | Cette propriété permet d’indiquer la hauteur libre dans le local. Les propriétés « Niveau » et « Limite supérieure » doivent donc également avoir la même valeur. |

