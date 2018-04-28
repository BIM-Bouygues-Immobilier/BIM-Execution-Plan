{% extends "/templates/modelisation.md" %}

{# Décrit le format de fichier du logiciel #}
{% block logicel_format %}Autodesk Revit (.rvt){% endblock %}

{# Décrit la procédure de georeférencement #}
{% block logiciel_geopositionnement %}
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

### Création du fichier de référence

L’architecte est responsable de la création d'un fichier de référence .RVT du projet qui doit être mis en coordonnées partagés avec la méthodologie décrite dans le paragraphe précédent.
Dans ce fichier Revit XXX\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt, l’architecte crée/copie les quadrillages et les niveaux du projet.
Par ailleurs, le niveau de référence pour tous les intervenants est le niveau fini, comme décrit dans les [Recommandations de modélisation](/02_Modelisation/00_communs/generalites.md ).
L’architecte, via la plateforme collaborative, met ensuite à disposition de tous les intervenants du projet ce fichier dans le dossier : DOCUMENTS00-Programme et base documentaire.
En cas de demande de déplacement, de changement de nom ou d’ajout de niveaux et nouvelles files par la MOE :

* L’architecte est le partenaire qui a la responsabilité de les intégrer dans le fichier XXX\_QUADRILLAGES\_NIVEAUX\_PHASE.rvt.
* Ce-dernier sera mis à jour en conséquence et transmis à l’ensemble des intervenants concernés. Chacun des contributeurs BIM a alors la responsabilité de mettre à jour son fichier.

{% endblock %}

{# Décrit la procédure d'export en IFC #}
{% block logiciel_export %}

### Plug-in d’export IFC

Pour l'export, il est nécessaire d’utiliser la dernière version du plug-in d’export IFC disponible gratuitement sur l’Autodesk App Store.
Ce plug-in améliore la qualité de l’export depuis Revit vers le format IFC.

Ce plug-in est disponible aux adresses suivantes :

| Version du logiciel | Adresse |
| :--- | :--- |
| Revit 2018 | [https://apps.autodesk.com/RVT/en/Detail/Index?id=6193770166503453647&appLang=en&os=Win64](https://apps.autodesk.com/RVT/en/Detail/Index?id=6193770166503453647&appLang=en&os=Win64) |
| Revit 2017 | [https://apps.autodesk.com/RVT/en/Detail/Index?id=1049118595309324136&appLang=en&os=Win64](https://apps.autodesk.com/RVT/en/Detail/Index?id=1049118595309324136&appLang=en&os=Win64) |
| Revit 2016 | [https://apps.autodesk.com/RVT/en/Detail/Index?id=3754730560173591798&appLang=en&os=Win32\_64](https://apps.autodesk.com/RVT/en/Detail/Index?id=3754730560173591798&appLang=en&os=Win32_64) |
| Revit 2015 | [https://apps.autodesk.com/RVT/en/Detail/Index?id=1636561288646603019&appLang=en&os=Win32\_64](https://apps.autodesk.com/RVT/en/Detail/Index?id=1636561288646603019&appLang=en&os=Win32_64 "Plug-in export IFC from Revit 2015") |

### Procédure d’export

Ce plug-in remplace les fonctions d’export IFC classique de Revit :

| Ouvrir l’interface d’export IFC : |
| :--- |
| ![Interface d'export](/02_Modelisation/00_communs/images/export-rvt/Export_01.png) |

### Réglages de l’export IFC

Il est demandé d’effectuer les réglages suivants lors de l’export :

| General |
| :---: |
| ![Général](/02_Modelisation/00_communs/images/export-rvt/Export_03.png) |

| Additional contents |
| :--- |
| ![Additional contents](/02_Modelisation/00_communs/images/export-rvt/Export_04.png) |

| Property Sets |
| :--- |
| ![Property Sets](/02_Modelisation/00_communs/images/export-rvt/Export_05.png) |

| Level of Detail |
| :--- |
| ![Level of Detail](/02_Modelisation/00_communs/images/export-rvt/Export_06.png) |

| Advanced |
| :--- |
| ![Advanced](/02_Modelisation/00_communs/images/export-rvt/Export_07.png) |

### Renseignement de l'adresse du projet

Dans l'onglet "General" de la fenêtre d'export IFC, il est également demandé de renseigner les informations liées à l'adresse du projet:

![Renseignement du projet](/02_Modelisation/00_communs/images/Adresse1.PNG)

![Adresse du projet](/02_Modelisation/00_communs/images/Adresse2.PNG)

Les paramètres sont à renseigner de la façon suivante:

| Paramètre | Valeur |
| :--- | :--- |
| Purpose | User defined |
| Description | Type d'intervention \(Rénovation, Nouvelle construction, ...\) |
| User-Defined purpose | Destination \(Bureaux, Logements, Hôtel, ...\) |
| Address line 1 | L'adresse du projet |
| City | La ville du projet |
| Postal code | Le code postal du projet |
| State | La région du projet |
| Country | France |

### Réglages des catégories à exporter

Afin que l'ensemble des catégories Revit modélisées soit exporté, il est nécessaire de modifier les catégories exportées par default en IFC :

![Catégories](/02_Modelisation/00_communs/images/export-rvt/Export_08.png)

Pour cela, il faut venir écrire le nom de la catégorie IFC souhaitée en face de la catégorie Revit, comme indiqué ci-dessous :

| Quadrillages =  IfcGrid |
| :--- |
| ![Quadrillages](/02_Modelisation/00_communs/images/export-rvt/Export_09.png) |

| Surfaces = IfcSpaces |
| :--- |
| ![Surfaces](/02_Modelisation/00_communs/images/export-rvt/Export_10.png) |

| Volumes =  IfcBuildingElementProxy |
| :--- |
| ![Volumes](/02_Modelisation/00_communs/images/export-rvt/Export_11.png) |

| Parking = IfcBuildingElementProxy & Type = PARKING  |
| :--- |
| ![Parking](/02_Modelisation/00_communs/images/export-rvt/Export_12.png) |

| Meuble de rangement = IfcBuildingElementProxy & Type = PLACARD |
| :--- |
| ![Meuble de rangement](/02_Modelisation/00_communs/images/export-rvt/Export_13.png) |

### Export au format DWG, à partir de Revit {#revit2dwg}

L’extraction des DWG depuis Revit doit se faire :

* Depuis l’espace papier de Revit, pour le rendu de chaque phase, afin de fournir la version en format .dwg des livrables diffusés en format .pdf
* Depuis les vues de rendu de Revit, en coordonnées partagées, tout le long du projet et pour le rendu de phase:

| Sélectionner "Exporter"  "Format CAO"  "DWG" |
| :--- |
| ![Menu](/02_Modelisation/00_communs/images/export-rvt/Export DWG 1.png) |

| Ouvrir l'interface pour la modification de l'export |
| :--- |
| ![Interface d'export](/02_Modelisation/00_communs/images/export-rvt/Export DWG 2.png) |

| Sélectionner la modalité d'export en coordonnées partagées |
| :--- |
| ![Coordonnées paratagées](/02_Modelisation/00_communs/images/export-rvt/Export DWG 3.png) |

{% endblock %}