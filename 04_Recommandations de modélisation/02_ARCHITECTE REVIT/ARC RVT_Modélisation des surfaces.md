# Modélisation des surfaces dans Revit

L'article suivant présente les recommandations de modélisation des surfaces dans le logiciel Autodesk Revit pour les maquettes numériques architecturales.

Aucune contrainte n'est imposé pour l'utilisation de l'outil "Espace".

## Surface Hors Œuvre Brut \(SHOB\) et Surface de Plancher \(SDP\)

### Généralités

Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) sont calculées en additionnant les différents types de surfaces du projet. De plus, la représentation des surfaces de parkings extérieurs est attendue.

### Décomposition des surfaces

Les surfaces du projet sont décomposées suivant ces valeurs:

| Nom | Description |
| :--- | :--- |
| Façade | Surface correspondante à l’emprise horizontale de la façade \(la SDP est calculée au nu intérieur de la façade\) |
| Gaine Ascenseur Et Escaliers | Surfaces des vides et trémies qui se rattachent aux escaliers et ascenseurs |
| Gaine Technique | Surfaces des vides et trémies qui se rattachent aux gaines techniques |
| 180 | Surfaces d'une hauteur sous plafond inférieure ou égale à 1,80 mètre |
| Parking | Surfaces aménagées en vue du stationnement des véhicules motorisés, hors rampes d'accès et aires de manœuvres |
| Parking Vélo | Surfaces aménagées en vue du stationnement des vélo |
| Circulation | Surfaces des circulations des véhicules et aires de manœuvres |
| Rampe | Surfaces des rampes d’accès des véhicules au parking |
| Allée | Surfaces des allées piétonnes autour du bâtiment |
| Voirie | Surfaces de voirie |
| Espace vert | Surfaces de pelouses, allées, zones plantées, … |
| Local technique | Surfaces des locaux techniques nécessaires au fonctionnement d'un groupe de bâtiments ou d'un immeuble autre qu'une maison individuelle, y compris les locaux de stockage des déchets |
| Cave | Surfaces des caves ou des celliers, annexes des logements, dès lors que ces locaux sont desservis uniquement par une partie commune |
| Palier | Surface des paliers en infrastructure |
| Livraison | Surfaces des aires de livraisons couvertes et fermées |
| Terrasse | Surfaces des balcons, terrasses, loggia, … |
| SDP | Surfaces restantes |

### Modélisation dans Revit

L’ensemble de ces surfaces SHOB/SHON/SDP est représenté à l’aide d’un plan de surface par niveau :

![](/assets/SURFACE_01.PNG)Chaque surface dessinée dans ce plan doit alors avoir les propriétés suivantes :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Commentaire | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement de ces surfaces. Les surfaces en terrasses \(locaux techniques par ex.\) sont marquée « Extérieur » |
| Nom | Façade, Gaine Ascenseur Et Escaliers, Gaine Technique, 180, Parking, Parking Vélo, Circulation, Rampe, Allée, Voirie, Espace vert, Local technique, Cave, Palier, Livraison, Terrasse, SDP | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. |

## Places de parking

### Modélisation dans Revit

Les places de parking sont modélisées à l’aide d’une famille de la catégorie Parking. Les propriétés suivantes sont à compléter :

## Surface Utile Brute Locative \(SUBL\), Surface Utile Brute Bureaux \(SUBB\), Surface Utile Nette \(SUN\) et Surface Nette Bureaux \(SNB\)





