# Partage des coordonnées dans Revit

Ce document décrit les procédures pour le partage des coordonnées, des trames et des niveaux.

Les prescriptions ci-dessous sont indicatives, et n’enlèvent pas au prestataire la possibilité de définir des systèmes de coordonnées internes en fonction de la géométrie du bâtiment.

## Coordonnées et orientation du projet

Les modèles géométriques de chaque contributeur doivent faire référence un système commun de coordonnées relatif à la position géographique.

### Partage du point d'origine géomètre à partir d'un fichier CAD

### Partage du point d'origine géomètre à partir d'une maquette revit

1. Insérer le modèle du géomètre en LienRevit d’ « Origine à Origine ».
![](/02_Modelisation/02_architecte/images/Coordonnées partagées 01.PNG)
2. Tourner/déplacer le modèle dans la position souhaitée
4. Aller dans l’onglet « gérer » ensuite « coordonnées » et choisir « importer les coordonnées »
5. Sélectionner le lien IE\_AFFAIRE\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt
6. Le fichier de travail Revit est alors en coordonnées partagées également.

## Importer et exporter

### Importer des fichiers de référence

Dorénavant, lorsque vous liez/importez un fichier .rvt, .dwg d’un partenaire, il faut le faire en positionnement « Automatique – A l’emplacement partagé ».

### Exporter des IFC et extraire des DWG

* Pour l’export en format IFC : se référer aux recommandations d'export : [Recommandations d'export](/02_Modelisation/00_communs/export-rvt.md#revit2ifc)

* Pour l’extraction des livrables en format dwg : se référer aux recommandations d'export : [Recommandations d'export](/02_Modelisation/00_communs/export-rvt.md#revit2dwg)



