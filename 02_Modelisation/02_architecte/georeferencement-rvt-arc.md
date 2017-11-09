# Partage des coordonnées dans Revit

Ce document décrit les procédures pour le partage des coordonnées, des trames et des niveaux.

Les prescriptions ci-dessous sont indicatives, et n’enlèvent pas au prestataire la possibilité de définir des systèmes de coordonnées internes en fonction de la géométrie du bâtiment.

## Coordonnées et orientation du projet

Les modèles géométriques de chaque contributeur doivent faire référence un système commun de coordonnées relatif à la position géographique.

### Partage du point d'origine géomètre à partir d'une maquette revit

1. Insérer le modèle du géomètre en LienRevit d’ « Origine à Origine ».
   ![](/02_Modelisation/02_architecte/images/Coordonnées partagées 01.PNG)
2. Tourner/déplacer le modèle dans la position souhaitée
   ![](/02_Modelisation/02_architecte/images/Coordonnées partagées 02.PNG)
3. Aller dans l’onglet « Gérer » ensuite « Coordonnées » et choisir « Importer les coordonnées »
   ![](/02_Modelisation/02_architecte/images/Coordonnées partagées 03.png)
4. Sélectionner le lien du géomètre
5. Le fichier de travail Revit est alors en coordonnées partagées également.

### Partage du point d'origine géomètre à partir d'un fichier CAD

1. Insérer le fichier du géomètre en LienCAO d'« origine à Origine».  
2. Tourner/déplacer le lien dans l'espace de dessin dans la position souhaitée.
3. Aller dans l’onglet « Gérer » ensuite « Coordonnées » et choisir « Importer les coordonnées »
4. Sélectionner le lien CAO
5. Le fichier de travail Revit est maintenant en coordonnées partagés avec le plan géomètre. 

## Création du fichier de référence

L’architecte est responsable de la création d'un fichier de référence .RVT du projet qui doit être mis en coordonnées partagés avec la méthodologie décrite dans le paragraphe précédent.  
Dans ce fichier Revit XXX\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt, l’architecte crée/copie les quadrillages et les niveaux du projet.  
Par ailleurs, le niveau de référence pour tous les intervenants est le niveau fini, comme décrit dans les [Recommandations de modélisation](/02_Modelisation/00_communs/generalites.md ).  
L’architecte, via la plateforme collaborative, met ensuite à disposition de tous les intervenants du projet ce fichier dans le dossier : DOCUMENTS&gt;00-Programme et base documentaire.  
En cas de demande de déplacement, de changement de nom ou d’ajout de niveaux et nouvelles files par la MOE :

* L’architecte est le partenaire qui a la responsabilité de les intégrer dans le fichier XXX\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt. 
* Ce-dernier sera mis à jour en conséquence et transmis à l’ensemble des intervenants concernés. Chacun des contributeurs BIM a alors la responsabilité de mettre à jour son fichier. 

## Importer et exporter

### Importer des fichiers de référence
Lorsque vous liez/importez un fichier .rvt, .dwg d’un partenaire, il faut le faire en positionnement « Automatique – A l’emplacement partagé ».

| Lier un fichier .dwg |
| :--- |
| ![](/02_Modelisation/02_architecte/images/Coordonnées partagées 06.PNG) |

| Lier un fichier .rvt |
| :--- |
| ![](/02_Modelisation/02_architecte/images/Coordonnées partagées 05.PNG) |

### Exporter des IFC

Pour l’export en format IFC : se référer aux recommandations d'export : [Recommandations d'export](/02_Modelisation/00_communs/export-rvt.md#revit2ifc)



