# Modélisation du lot Ascenseur dans le logiciel Revit

## Modélisation des réseaux

Afin de les visualiser, chaque type de système de réseaux technique \(gaine et canalisation\) doit avoir sa propre couleur. Les couleurs ne sont pas imposées, mais chaque type de système doit être clairement identifiable par sa couleur.

### Couleur des systèmes

Afin d’assigner à chaque système sa couleur, il est nécessaire d’ajouter un matériau à chaque type de système. Pour cela, ouvrir les propriétés du type de système en faisant un clic-droit sur le type de système dans l’arborescence du projet \(1\). Cliquer ensuite sur « … » \(2\) en face de « Matériau » afin de sélectionner un matériau pour le système :

![](/02_Modelisation/04_betFluide/images/MEP_01.PNG)

Dans le navigateur de matériaux, cliquer sur « Créer un matériau » \(1\) pour créer un nouveau matériau. Dans l’onglet « Graphique » \(2\), régler la couleur d’Ombrage \(3\) pour sélectionner la couleur du type de système \(ici rouge\). Cliquer sur OK \(4\) pour valider votre choix.

![](/02_Modelisation/04_betFluide/images/MEP_02.PNG)Cette procédure doit être répétée pour chaque système de gaine et de canalisation.

### Assignation des catégories

Les éléments suivants doivent être modélisés avec des familles qui soient affectées à une catégorie Revit cohérente avec la fonction de l'élément même: 

* Equipements électriques
* Equipements de génie climatique et de plomberie
* Terminaux horizontaux et verticaux
* Accessoires de gaine et de canalisation
* Equipements spécialisés


Aucun objet ne doit être modélisé en "Modèle Générique". 

---

Image credits [here ](/CREDITS.md)









