# Recommandations de modélisation dans Allplan

L'article suivant présente les recommandations de modélisation pour différentes catégories d'éléments dans Allplan. Ces recommandations permettent de produire les informations nécéssaires à la réalisation des [cas d'usages BIM de Bouygues Immobilier](/01_CasUsages/README.md).

## Modélisation des pièces

Dans Allplan, l'objet "Pièce" devra être utilisé pour créer deux jeux de modélisation:
* [Un jeu de pièces pour le calcul des surfaces utiles](#Utile), en précisant la décomposition des surfaces des fonctions des locaux. 
* [Un jeu de pièces pour le calcul de la surface de plancher](#SDP), en dessinant les différents types de surfaces du projet

La modélisation des pièces se fait à l’aide de l’outil "Pièce", qui se trouve dans la palette "Architecture_Revêtement", onglet "Métrées: pièces, surfaces, étages" :

![](/02_Modelisation/02_architecte/images/ROOM6.PNG)

### ... pour le calcul des surfaces utiles {#Utile}

Les Surfaces Utiles Brutes Locatives \(SUBL\), Surfaces Utiles Brutes Bureaux \(SUBB\), Surfaces Utiles Nettes \(SUN\) et Surfaces Nettes Bureaux \(SNB\) sont donc calculées à partir d'un jeu de modélisation de pièces à part, dans le quel chaque local du projet sera présent. 

En plus des locaux « nobles » du programme, cette modélisation doit inclure tous les autres types de locaux, tel que les circulations, les locaux techniques, les gaines techniques, …

Les locaux doivent être représentés et décomposés en locaux fonctionnels \(Bureau, Salle de Réunion, Hall, …\), même si ces locaux appartiennent à un espace physique plus important. Par exemple, un hall et une cafétéria partageant le même espace physique devront être représentés comme deux locaux distincts.

> Les locaux doivent être modélisés depuis le sol fini jusqu’au plafond fini. En l’absence de faux-plafonds, les locaux doivent être modélisés jusqu’à la hauteur libre prévue par le programme. 
La hauteur de l'objet pièce devra être paramétrée correctement dans l'interface des propriétés afin de représenter la volumétrie intérieure de la pièce. 

Les propriétés suivantes sont ensuite à compléter:
* Nom de la pièce, qui indique le type de local selon la décomposition décrite [ci-dessous](#nom)
* Destination de la pièce, qui indique la destination des pièces réalisées, selon décomposition proposée [ci-dessous](#destination)

#### Nom des pièces {#nom}

Le nom des pièces devra être associé à la propriété "Fonction" et, si une numérotation des pièces est mise en place, cela devra être associée à la propriété "Désignation/Qualité".
![](/02_Modelisation/02_architecte/images/ROOM1.PNG)

Le nom de la pièce sera obligatoirement choisi parmi la liste suivante:

{% include "../../00_Referentiel/NomDesSurfaces.md"  %}

#### Destination des pièces {#destination}

Le renseignement de la destination des pièces devra se faire dans la propriété IFC "Description":
* Pour assigner cette propriété aux pièces du projet, aller dans l'interface "Attributs" dans la palette des propriétés de la pièce, dans le champs "Attributs généraux". 
* Cliquer ensuite sur l'option "Assigner un nouvel attributs" pour accéder à la palette "Définir et assigner des attributs":
![](/02_Modelisation/02_architecte/images/ROOM2.PNG)
* Aller dans les groupe des attributs "IFC" et choisir l'attribut "Description"
![](/02_Modelisation/02_architecte/images/ROOM3.PNG)
* Remplir enfin le paramètre avec la valeur correcte parmi celles listées ci-dessous:
![](/02_Modelisation/02_architecte/images/ROOM4.PNG)


{% include "../../00_Referentiel/NomDesProduits.md"  %}

### ... et pour le calcul de la SDP {#SDP}

Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) sont calculées en additionnant les différents types de surfaces du projet. 
Des objets "Pièces" devront être modélisés spécifiquement pour permettre ce calcul. 

Contrairement aux pièces qui représentent les locaux, le nom des pièces pour le calcul des surfaces associé à la propriété "Fonction" devra être choisi parmi la liste suivante:

{% include "../../00_Referentiel/NomDesSurfaces.md"  %}

Le renseignement de la destination de la surface suivra le même logique décrite pour les [locaux](#destination)

Le plan suivant montre un exemple de la modélisation des pièces finalisée au calcul de la SDP:

![](/02_Modelisation/02_architecte/images/Surfaces_ExempleNiveauCourant.png)


















