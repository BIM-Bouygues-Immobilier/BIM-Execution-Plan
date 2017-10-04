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

&lt;!--

/\* Font Definitions \*/

@font-face

```
{font-family:"Cambria Math";

panose-1:2 4 5 3 5 4 6 3 2 4;

mso-font-charset:1;

mso-generic-font-family:roman;

mso-font-pitch:variable;

mso-font-signature:0 0 0 0 0 0;}
```

@font-face

```
{font-family:"Trebuchet MS";

panose-1:2 11 6 3 2 2 2 2 2 4;

mso-font-charset:0;

mso-generic-font-family:swiss;

mso-font-pitch:variable;

mso-font-signature:1671 0 0 0 159 0;}
```

/\* Style Definitions \*/

p.MsoNormal, li.MsoNormal, div.MsoNormal

```
{mso-style-unhide:no;

mso-style-qformat:yes;

mso-style-parent:"";

margin:0cm;

margin-bottom:.0001pt;

mso-pagination:widow-orphan;

font-size:10.0pt;

mso-bidi-font-size:12.0pt;

font-family:"Trebuchet MS",sans-serif;

mso-fareast-font-family:"Times New Roman";

mso-bidi-font-family:"Times New Roman";

color:\#0B2D77;}
```

.MsoChpDefault

```
{mso-style-type:export-only;

mso-default-props:yes;

font-size:10.0pt;

mso-ansi-font-size:10.0pt;

mso-bidi-font-size:10.0pt;}
```

@page WordSection1

```
{size:612.0pt 792.0pt;

margin:70.85pt 70.85pt 70.85pt 70.85pt;

mso-header-margin:36.0pt;

mso-footer-margin:36.0pt;

mso-paper-source:0;}
```

div.WordSection1

```
{page:WordSection1;}
```

--&gt;

| **Eléments de construction** |  |
| :--- | :--- |
|  | TERRASSES |
|  | GAINES ASCENSEURS ET ESCALIERS |
|  | GAINES TECHNIQUES |
| **Partie Communes Nobles** |  |
|  | HALL |
|  | SALLE DE RESTAURANT ET DISTRIBUTION |
|  | CUISINES |
|  | CAFETERIA |
|  | SANITAIRES SGX |
|  | AUDITORIUM / SALLE POLYVALENTE |
|  | FITNESS |
|  | PALIERS D'ETAGES |
|  | PALIERS D'ESCALIERS |
|  | CIRCULATIONS COMMUNES |
| **Parties Privatives** |  |
|  | LOCAUX ET ARMOIRES TECHNIQUES UTILISATEURS |
|  | CIRCULATIONS DE BUREAUX |
|  | SANITAIRES PRIVATIFS |
|  | LOCAUX MENAGES D'ETAGES |
|  | TISANERIES |
|  | LOCAUX BRASSAGE |
|  | SALLES DE REUNIONS |
|  | ZONES DE SURCHARGES RENFORCEES |
|  | SURFACES BUREAUX |
| **Back of house** |  |
|  | ARCHIVES CENTRALES |
|  | LOCAUX DIVERS COMMUNS |
|  | LOCAUX VESTIAIRES VELO |
|  | LOCAUX DECHETS |
|  | LOCAUX TECHNIQUES |
| **Stationnement** |  |
|  | PARKING VOITURES ET DEUX MOTORISES |
|  | LOCAUX VELO PARKING |
|  | PALIERS INFRA |
|  | AIRES DE LIVRAISONS COUVERTES ET FERMEES |

### Modélisation dans Revit

Dans Revit, ces locaux doivent être modélisé à l’aide de l’outil Pièce :

![](/assets/SURFACE_02.PNG)Les propriétés suivantes sont à compléter :

| Propriété | Valeurs possibles | Explication |
| :--- | :--- | :--- |
| Commentaire | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement de ces surfaces. Les surfaces en terrasses \(locaux techniques par ex. sont marquée « Extérieur ». |
| Nom | Voir « Décompositions des locaux » | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. |
| Décalage limite | Hauteur libre \(en m\) | Cette propriété permet d’indiquer la hauteur libre dans le local. Les propriétés « Niveau » et « Limite supérieure » doivent donc également avoir la même valeur. |



