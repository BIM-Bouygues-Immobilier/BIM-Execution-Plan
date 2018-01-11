# Importer un fichier IFC dans Revit

## Généralités

Ce paragraphe décrit la méthodologie pour l'intégration de fichiers de référence au format IFC dans l'environnement de travail Revit.
Le procès suggéré consiste à convertir le fichier IFC en format Revit pour ensuite l'appeler en lien et travailler de façon plus fluide.

## Conversion du fichier IFC en format Revit

Pour convertir le fichier IFC en format Revit:
* Ouvrir le ficher IFC dans Revit

![](/02_Modelisation/00_communs/images/ImportIFCRVT1.png)

![](/02_Modelisation/00_communs/images/ImportIFCRVT2.PNG)

* Enregistrer sous format Revit le fichier, en choisissant les options souhaités

![](/02_Modelisation/00_communs/images/ImportIFCRVT3.png)

![](/02_Modelisation/00_communs/images/ImportIFCRVT4.PNG)

## Utilisation du fichier converti

Le fichier .rvt crée dans l'étape ci-dessus pourra être utilisé comme lien Revit dans le projet. 
Pour lier ce fichier, il faudra donc aller dans l'onglet "Insérer" et choisir "Lier Revit".
Le fichier à lier devra être sélectionnée, ainsi que l'option de positionnement "Automatique - A l'emplacement partagé". 

![](/02_Modelisation/00_communs/images/ImportIFCRVT5.PNG)

Il est possible que le fichier lié ne soit pas visible dans la vue à cause de la phase de création des objets. Pour régler cela, vous pouvez utiliser l'option d'affectation des phases des liens Revit. 
Pour accéder à cette option, il est nécessaire d'aller dans l'arborescence du projet, de sélectionner le lien à l'aide de la touche droite et de choisir "Propriété du type". 
![](/02_Modelisation/00_communs/images/ImportIFCRVT6.png)

Ensuite, grâce à la propriété de l'affectation des phases, vous pouvez choisir la correspondance des phases entre le modèle hôte et le modèle en lien. 

![](/02_Modelisation/00_communs/images/ImportIFCRVT7.PNG)


