## Export au format IFC, à partir de Revit

### Généralités

Ce paragraphe décrit les méthodologies d’export au format IFC demandées par Bouygues Immobilier.

Pour chaque lot, il est nécessaire de déposer un seul fichier, au format IFC2X3, incluant tous les éléments nécessaires à la bonne compréhension du projet pour la phase en cours, et purgé de tous les éléments non nécessaires au sujet en cours.

### Plug-in d’export IFC

Pour export, il est nécessaire d’utiliser la dernière version du plug-in d’export IFC disponible gratuitement sur l’Autodesk App Store. Ce plug-in améliore la qualité de l’export depuis Revit vers le format IFC.

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
| ![](/assets/Export_01.png) |

| Modifier les réglages d’exports: |
| :--- |
| ![](/assets/Export_02.png) |

### Réglages de l’export IFC

Il est demandé d’effectuer les réglages suivants lors de l’export :

| Général  |
| :--- |
| ![](/assets/Export_03.png) |

| Additional contents |
| :--- |
| ![](/assets/Export_04.png) |



| Property Sets \[A modifier\] |
| :--- |
| ![](/assets/Export_05.png) |

| Level of Detail |
| :--- |
| ![](/assets/Export_06.png) |

| Advanced |
| :--- |
| ![](/assets/Export_07.png) |

### NOTA USER PROPERTY SETS ET MAPPING TABLE A RAJOUTER

### Réglages des catégories à exporter

Afin que l'ensemble des catégories Revit modélisées soit exportées, il est nécessaire de modifier les catégories exportée par default en IFC :

![](/assets/Export_08.png)

Pour cela, il faut venir écrire le nom de la catégorie IFC souhaitée en face de la catégorie Revit, comme indiqué ci-dessous :



| Quadrillages = &gt; IfcGrid |
| :--- |
| ![](/assets/Export_09.png) |

| Surfaces =&gt; IfcSpaces |
| :--- |
| ![](/assets/Export_10.png) |

| Volumes = &gt; IfcBuildingElementProxy |
| :--- |
| ![](/assets/Export_11.png) |

| Parking=&gt; IfcSpaces |
| :--- |
| ![](/assets/Export_12.png) |



