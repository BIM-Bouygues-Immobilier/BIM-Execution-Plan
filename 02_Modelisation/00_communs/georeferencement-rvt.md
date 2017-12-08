# Partage des coordonnées dans Revit

Ce document décrit les procédures pour le partage des coordonnées, des trames et des niveaux.

Les prescriptions ci-dessous sont indicatives, et n’enlèvent pas au prestataire la possibilité de définir des systèmes de coordonnées internes en fonction de la géométrie du bâtiment.

## Coordonnées et orientation du projet

Les modèles géométriques de chaque contributeur doivent faire référence un système commun de coordonnées relatif à la position géographique.

> Avertissement : On ne déplacera *jamais* le point topographique ou le point de base du projet à la main

### Partage du point d'origine

La procédure suivante permet de réccupérer le système de coordonnées du modèle de référence (modèle du site ou modèle architecte). Cette procédure n'est à faire qu'une seule fois, au démarrage du projet.

* Etape 1 : Liez le modèle de référence (modèle du site ou modèle architecte) en Lien Revit « Automatique - Origine à Origine ». Si le modèle est corectement placé, passez directement à l'étape 4.

|Lien "Origine à Origine" | Modèle de référence lié | 
| :---: | :---: |
|![](/02_Modelisation/00_communs/images/georeferencement/Lier_le_modèle_de_reference_Origine_origine.png)  |![](/02_Modelisation/00_communs/images/georeferencement/modele_reference_positionne.png)  |

* Etape 2 : Si le modèle de référence n'est pas correctement placé, supprimez le lien, liez-le de nouveau en Lien Revit « Automatique - Centre à Centre » et passez à l'étape 3.

|Lien "Centre à Centre" | Modèle de référence lié | 
| :---: | :---: |
|![](/02_Modelisation/00_communs/images/georeferencement/Lier_le_modèle_de_reference_Centre_centre.png)  |![](/02_Modelisation/00_communs/images/georeferencement/Modele_Reference.png)  |

* Etape 3 : Déplacer et tourner manuelement ce modèle de référence lié dans la position souhaitée, en plan et en élévation.

|Déplacement et rotation en plan | Déplacement en élévation | 
| :---: | :---: |
|![](/02_Modelisation/00_communs/images/georeferencement/deplacement_plan.png)  |![](/02_Modelisation/00_communs/images/georeferencement/deplacement_elevation.png)  |

* Etape 4 : Dans l'onglet "Gérer" (1), sélectionner "Coordonnées" (2) puis "Importer les coordonnées" (3). Cliquez alors sur le modèle de référence lié (4).

![](/02_Modelisation/00_communs/images/georeferencement/importer_coordonnees.png) 

Le système de coordonnées partagées du modèle de référence est maintenant importé dans votre modèle.

## Lier et exporter

### Lier des modèles

Dorénavant, lorsque vous liez/importez un fichier .rvt ou .dwg provenant d’un partenaire, il faut le faire en positionnement « Automatique – A l’emplacement partagé ».

| Lier un fichier .dwg | Lier un fichier .rvt |
| :--- |:--- |
| ![](/02_Modelisation/02_architecte/images/Coordonnées partagées 06.PNG) |![](/02_Modelisation/02_architecte/images/Coordonnées partagées 05.PNG) |

### Exporter des IFC 

Pour l’export en format IFC, se référer aux recommandations d'export : [Recommandations d'export](/02_Modelisation/00_communs/export-rvt.md#revit2ifc)




