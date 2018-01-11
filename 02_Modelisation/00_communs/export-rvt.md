# Export au format IFC, à partir de Revit {#revit2ifc}

## Généralités

Ce paragraphe décrit les méthodologies d’export au format IFC demandées par Bouygues Immobilier.

Pour chaque lot, il est nécessaire de déposer un seul fichier, au format IFC2X3, incluant tous les éléments nécessaires à la bonne compréhension du projet pour la phase en cours, et purgé de tous les éléments non nécessaires au sujet en cours.

## Plug-in d’export IFC

Pour l'export, il est nécessaire d’utiliser la dernière version du plug-in d’export IFC disponible gratuitement sur l’Autodesk App Store.  
Ce plug-in améliore la qualité de l’export depuis Revit vers le format IFC.

Ce plug-in est disponible aux adresses suivantes :

| Version du logiciel | Adresse |
| :--- | :--- |
| Revit 2018 | [https://apps.autodesk.com/RVT/en/Detail/Index?id=6193770166503453647&appLang=en&os=Win64](https://apps.autodesk.com/RVT/en/Detail/Index?id=6193770166503453647&appLang=en&os=Win64) |
| Revit 2017 | [https://apps.autodesk.com/RVT/en/Detail/Index?id=1049118595309324136&appLang=en&os=Win64](https://apps.autodesk.com/RVT/en/Detail/Index?id=1049118595309324136&appLang=en&os=Win64) |
| Revit 2016 | [https://apps.autodesk.com/RVT/en/Detail/Index?id=3754730560173591798&appLang=en&os=Win32\_64](https://apps.autodesk.com/RVT/en/Detail/Index?id=3754730560173591798&appLang=en&os=Win32_64) |
| Revit 2015 | [https://apps.autodesk.com/RVT/en/Detail/Index?id=1636561288646603019&appLang=en&os=Win32\_64](https://apps.autodesk.com/RVT/en/Detail/Index?id=1636561288646603019&appLang=en&os=Win32_64 "Plug-in export IFC from Revit 2015") |

## Procédure d’export

Ce plug-in remplace les fonctions d’export IFC classique de Revit :

| Ouvrir l’interface d’export IFC : |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_01.png) |

| Ouvrir l’interface d’export IFC : |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_01.png) |

## Réglages de l’export IFC

Il est demandé d’effectuer les réglages suivants lors de l’export :

| General |
| :---: |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_03.png) |

| Additional contents |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_04.png) |

| Property Sets |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_05.png) |

| Level of Detail |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_06.png) |

| Advanced |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_07.png) |

## Renseignement de l'adresse du projet

Dans l'onglet "General" de la fenêtre d'export IFC, il est également demandé de renseigner les informations liées à l'adresse du projet:![](/02_Modelisation/00_communs/images/Adresse1.PNG)![](/02_Modelisation/00_communs/images/Adresse2.PNG)Les paramètres sont à renseigner de la façon suivante:

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

## Réglages des catégories à exporter

Afin que l'ensemble des catégories Revit modélisées soit exporté, il est nécessaire de modifier les catégories exportées par default en IFC :

![](/02_Modelisation/00_communs/images/export-rvt/Export_08.png)

Pour cela, il faut venir écrire le nom de la catégorie IFC souhaitée en face de la catégorie Revit, comme indiqué ci-dessous :

| Quadrillages = &gt; IfcGrid |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_09.png) |

| Surfaces =&gt; IfcSpaces |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_10.png) |

| Volumes = &gt; IfcBuildingElementProxy |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_11.png) |

| Parking=&gt; IfcBuildingElementProxy & Type = PARKING  |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_12.png) |

| Meuble de rangement=&gt; IfcBuildingElementProxy & Type = PLACARD |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export_13.png) |

# Export au format DWG, à partir de Revit {#revit2dwg}

L’extraction des DWG depuis Revit doit se faire :

* Depuis l’espace papier de Revit, pour le rendu de chaque phase, afin de fournir la version en format .dwg des livrables diffusés en format .pdf
* Depuis les vues de rendu de Revit, en coordonnées partagées, tout le long du projet et pour le rendu de phase:

| Sélectionner "Exporter" &gt; "Format CAO" &gt; "DWG" |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export DWG 1.png) |

| Ouvrir l'interface pour la modification de l'export |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export DWG 2.png) |

| Sélectionner la modalité d'export en coordonnées partagées |
| :--- |
| ![](/02_Modelisation/00_communs/images/export-rvt/Export DWG 3.png) |



