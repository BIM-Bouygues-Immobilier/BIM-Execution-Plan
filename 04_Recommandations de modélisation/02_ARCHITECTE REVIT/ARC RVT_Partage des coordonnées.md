# Partager les coordonnées dans Revit

Ce document décrit les procédures pour le partage des coordonnées, des trames et des niveaux.

Les prescriptions ci-dessous sont indicatives, et n’enlèvent pas au prestataire la possibilité de définir des systèmes de coordonnées internes en fonction de la géométrie du bâtiment.

## Coordonnées et orientation du projet

Les modèles géométriques de chaque contributeur doivent faire référence un système commun de coordonnées relatif à la position géographique.

L’architecte récupère la position du point topographique du projet par rapport à celui qui est définit par le géomètre.

### Coordonner sa maquette avec le géomètre

Afin de récupérer le point d’origine du géomètre dans le modèle architecturale, il est conseillé de suivre les procédure suivante, en fonction des documents fournis par le géomètre :

#### Coordination avec un plan géomètre format CAO

1. Dans le fichier de travail, sélectionner l’onglet insérer, puis « LierCAO » le plan géomètre, en choisissant l’option « Centre à Centre ».

\[Image écran avec le bouton d’insertion et l’option centre à centre\]

1. Sélectionner le plan importé, puis le placer à l’aide des commande « déplacement » et « pivotement » dans la position souhaité dans l’environnement de travail. 

Il est conseillé de positionner le plan géomètre de façon à l’adapter aux quadrillages définis pour le projet \(i.e. on laisse les quadrillages en positon - idéalement orthogonales à l’espace de travail » , et on cale l’environnement par apport à ceux-là\).

\[Plusieurs images par étapes qui montrent le déplacement et la rotation\]

1. Une fois déplacé dans la position correcte, aller sur l’onglet « gérer » ensuite « coordonnées » et « importer les coordonnées ».

\[images de la procédure\]

1. Les coordonnées du plan ont été donc importé. Le modèle et le plan partages le même système de coordonnées.

\[image avec les propriétés du plan\]

1. Vérifier que le point d’origine du projet \(cercle\) s’est bien dissocié du point d’origine topographie \(triangle\). 

\[image\]

1. Sélectionner le point d’origine du projet \(cercle\).

2. Renseigner le champ Elev. avec la valeur référentiel \(par exemple, ngf\) du point 0 projet : par exemple, si le point 0 projet correspond à la cote ngf 50.00, sur le champ Elev. , écrire 50.00.

\[image\]

#### Coordination avec une maquette géomètre

1. Insérer le modèle géomètre en LienRevit avec l’option « centre à centre » 

\[image\]

1. Positionner le lien \(déplacement + rotation\) dans la position souhaité dans l’espace de travail.

1. Aller dans l’onglet « gérer » ensuite « coordonnées » et choisir « importer les coordonnées »

2. Sélectionner le lien géomètre.

3. Le deuxième fichier Revit est alors en coordonnées partagées également.

### Les niveaux altimétriques et les trames

L’architecte est responsable de la création du fichier IE\_AFFAIRE\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt qui sera mis en coordonnées partagés avec la procédure indiquée dans II.2.1 PARTAGE DU POINT D’ORIGINE ;

Dans le fichier Revit IE\_AFFAIRE\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt en coordonnées partagées \(voir étapes précédentes\), l’Architecte crée les quadrillages et les niveaux souhaités.

Par ailleurs, le niveau de référence pour tous les intervenants est le niveau fini. \[Voir Annexe 2 - Recommandations de modélisation\]

L’architecte, via la plateforme collaborative, met ensuite à disposition de tous les intervenants du projet ce fichier  dans le dossier :

DOCUMENTS&gt;00-Programme et base documentaire.

En cas de demande de déplacement, de changement de nom ou d’ajout de niveaux et nouvelles files par la MOE :

* L’architecte est le partenaire qui a la responsabilité de les intégrer dans le fichier IE\_AFFAIRE\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt.

* Ce-dernier sera mis à jour en conséquence et transmis à l’ensemble des intervenants concernés. Chacun des coordinateurs BIM a alors la responsabilité de mettre à jour son fichier

\[voir II.3.2 partage des quadrillages et des niveaux\]

## Importer et exporter

#### Importer des fichiers en référence

Dorénavant, lorsque vous liez/importez un fichier .rvt, .dwg d’un partenaire, il faut le faire en positionnement – « Automatique – A l’emplacement partagé ».

#### Exporter des IFC et extraire des DWG

* Pour l’export en format IFC : se référer à l’ « Annexe 3 - Recommandations d'export».

* Pour l’extraction des livrables en format dwg : se référer à l’ « Annexe 3 - Recommandations d'export».



