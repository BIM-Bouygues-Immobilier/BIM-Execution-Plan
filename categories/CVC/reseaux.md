Les réseaux de climatisation, de ventilation et de desenfumage sont modélisés à l'aide de l'outil Gaine de {{logiciel}}.

### Nom des systèmes

L'ensemble des gaines, raccord de gaines et accessoires de gaines doivent faire partie d'un système.

Le nom du type de réseaux de desemfumage doit suivre le schéma suivant :

> CVC-DES-RES-_CODE ELEMENT_

Le nom du type du réseau de ventilation CVC  doit suivre le schéma suivant :

> CVC-VEN-RES-_CODE ELEMENT_

{% include "/00_Referentiel/CVC/NomDesReseauxDeVentilationCVC.md" %}

### Couleur des systèmes

Afin de les visualiser, chaque type de système de réseaux technique \(gaine et canalisation\) doit avoir sa propre couleur. Les couleurs ne sont pas imposées, mais chaque type de système doit être clairement identifiable par sa couleur.

Afin d’assigner à chaque système sa couleur, il est nécessaire d’ajouter un matériau à chaque type de système. Pour cela, ouvrir les propriétés du type de système en faisant un clic-droit sur le type de système dans l’arborescence du projet \(1\). Cliquer ensuite sur « … » \(2\) en face de « Matériau » afin de sélectionner un matériau pour le système :

![](/02_Modelisation/04_betFluide/images/MEP_01.PNG)

Dans le navigateur de matériaux, cliquer sur « Créer un matériau » \(1\) pour créer un nouveau matériau. Dans l’onglet « Graphique » \(2\), régler la couleur d’Ombrage \(3\) pour sélectionner la couleur du type de système \(ici rouge\). Cliquer sur OK \(4\) pour valider votre choix.

![](/02_Modelisation/04_betFluide/images/MEP_02.PNG)Cette procédure doit être répétée pour chaque système de gaine et de canalisation.