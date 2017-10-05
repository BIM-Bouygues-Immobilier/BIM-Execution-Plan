# Partage des coordonnées dans Revit

Ce document décrit les procédures pour le partage des coordonnées, des trames et des niveaux.

Les prescriptions ci-dessous sont indicatives, et n’enlèvent pas au prestataire la possibilité de définir des systèmes de coordonnées internes en fonction de la géométrie du bâtiment.

## Coordonnées et orientation du projet

Les modèles géométriques de chaque contributeur doivent faire référence un système commun de coordonnées relatif à la position géographique.

### Partage du point d'origine

1. Insérer le modèle de référence IE\_AFFAIRE\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt. en LienRevit d’ « Origine à Origine ».

2. Tourner/déplacer le modèle dans la position souhaitée

3. Aller dans l’onglet « gérer » ensuite « coordonnées » et choisir « importer les coordonnées »

4. Sélectionner le lien IE\_AFFAIRE\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt.

5. Le fichier de travail Revit est alors en coordonnées partagées également.

## Importer et exporter

### Importer des fichiers de référence

Dorénavant, lorsque vous liez/importez un fichier .rvt, .dwg d’un partenaire, il faut le faire en positionnement « Automatique – A l’emplacement partagé ».

### Exporter des IFC et extraire des DWG

* Pour l’export en format IFC : se référer aux recommandations d'export \[Cfr. [Recommandations d'export](/04_Recommandations-de-modelisation/Export-depuis-Revit.md)\]

* Pour l’extraction des livrables en format dwg : se référer aux recommandations d'export \[Cfr. [Recommandations d'export](/04_Recommandations-de-modelisation/Export-depuis-Revit.md)\]



