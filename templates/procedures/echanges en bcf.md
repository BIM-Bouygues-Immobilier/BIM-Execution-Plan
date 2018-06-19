### Echanges en format BCF 

Pour échanger en utilisant le format BCF, 4 manipulations sont nécessaires: l'export du fichier BCF depuis bimsync, puis l'export de ce fichier dans un logiciel de modélisation (Revit, ArchiCAD ou Allplan), et faire le chemin inverse une fois les modifications apportées.

#### Export depuis bimsync en format BCFZIP

Cliquer sur l'onglet Sujet (1), et ouvrir la listes des sujets contenant le sujet que vous voulez exporter en format BCF (2).

![ExportBCFRevit01](/02_Modelisation/00_communs/images/export-bcf/ExportBCFRevit01.PNG)

Cliquer ensuite sur l'icône "..." (3), puis sur "Exporter la liste des sujets" (4). Vous pouvez également choisir l'option "Exporter les sujets filtrés" (5), en ayant choisi des filtres vous convenant au préalable.

![ExportBCFRevit02](/02_Modelisation/00_communs/images/export-bcf/ExportBCFRevit02.PNG)

Bimsync vous indique que l'exportation a commencé, cliquer sur "voir l'état d'avancement" (6).

![ExportBCFRevit03](/02_Modelisation/00_communs/images/export-bcf/ExportBCFRevit03.PNG)

Une fois l'exportation terminée, cliquer sur l'icône flèche pour télécharger (7) le fichier BFC de la liste des sujets exportés. Vous trouverez ce fichier dans votre dossier de téléchargement (8) en format BCFZIP.

![ExportBCFRevit04](/02_Modelisation/00_communs/images/export-bcf/ExportBCFRevit04.PNG)

{% if logiciel == "Revit" %}

#### Import d'un fichier BCFZIP dans Revit

Pour pouvoir manipuler le format BCF dans Revit, il faut passer par l'intermédiaire d'un plugin (par exemple, BIMcollab) qui doit être téléchargé puis installé sur votre poste. Dans le cas de BIMcollab, il faut se créer un compte, et l'activer avant de pouvoir ouvrir utiliser le BCF Manager, qui est l'interface permettant de manipuler les fichiers BCF. 

Une fois passé tous ces impératifs, aller dans l'onglet nouvellement créé BIMcollab (1), puis  cliquer sur BCF Manager (2) pour ouvrir l'interface, qui va alors apparaitre à droite de l'écran (3)

![importBCFRevit01](/02_Modelisation/00_communs/images/import-bcf/ImportBCFRevit01.PNG)

Pour ouvrir un fichier au format BCFZIP dans le BCF Manager, cliquer sur l'icône "Importer un fichier BCF (4), puis naviguer jusque dans votre dossier de téléchargement (5), sélectioner le fichier précédemment téléchargé et cliquer sur Ouvrir (6).

![importBCFRevit02](/02_Modelisation/00_communs/images/import-bcf/ImportBCFRevit02.PNG)

La listes des sujet va alors apparaitre dans la fenêtre BCF Manager sous forme d'une liste d'images numérotées. Cliquer sur l'image de votre sujet pour le modifier (7), et double cliquer pour ouvrir la vue correspondante dans la maquette Revit (8).

![importBCFRevit03](/02_Modelisation/00_communs/images/import-bcf/ImportBCFRevit03.PNG)

Les commentaires sont visibles en bas de la fenêtre du BCF Manager, cliquer sur le "+" (9) pour en ajouter un nouveau. Ecrire le commentaire dans la zone prévu à cet effet, changer l'image si besoin grâce aux outils sur la droite (10), puis valider en cliquant sur "Sauvegarder" (11). Ce nouveau commentaire sera ajouté à la liste des commentaires, ainsi que le nom de son auteur et sa date de création.

![importBCFRevit04](/02_Modelisation/00_communs/images/import-bcf/ImportBCFRevit04.PNG)