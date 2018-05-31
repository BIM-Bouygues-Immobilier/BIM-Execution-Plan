{% extends "/templates/modelisation.md" %}
{% set logiciel = "Revit" %}

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

#### Configuration de l'export

Télécharger la configuration d'export : [Configuration Cahier des Charges BIM BI](https://raw.githubusercontent.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/master/templates/softwares/Configuration%20IFC%20Cahier%20des%20Charges%20BIM%20BI.json) _(Clic-droit, puis "Enregistrer le lien/la cible sous...")_

Dans l'interface d'export IFC, cliquer sur l'icône "Importer Configuration" (1), puis dans le dossier de téléchargements, sélectionner le fichier Configuration Cahier des Charges BIM BI (2) que vous venez de télécharger et cliquer sur Ouvrir (3).

![ExportIFCRevit6](/02_Modelisation/00_communs/images/export-rvt/ExportIFCRevit8.PNG)

La Configuration Cahier des Charges BIM BI va alors apparaître dans la liste des configurations disponibles (4). Sélectionnez la, et cliquez sur OK (5).

![ExportIFCRevit6](/02_Modelisation/00_communs/images/export-rvt/ExportIFCRevit9.PNG)

#### Configuration manuelle

_Si vous ne souhaitez pas utiliser la configuration automatique,_ vous pourrez utiliser les réglages décrit ci-dessous :

Pour configurer manuellement l'export IFC, cliquer sur "Modifier réglages", la fenêtre de configuration de l'export va s'ouvrir. Il est recomandé de créer une nouvelle configuration. Pour cela, cliquer sur l'icône "Créer un nouveau régalge" en bas à gauche de la fenêtre, renseigner le nom de la configuration (par exemple, Configuration Cahier des Charges BIM BI), puis régler les paramètres de la façon suivante:

| Général |
| :--- |
| ![Général](/02_Modelisation/00_communs/images/export-rvt/ExportIFCRevit.PNG) |

| Contenu additionnel |
| :--- |
| ![Additional contents](/02_Modelisation/00_communs/images/export-rvt/ExportIFCRevit2.PNG) |

| Export jeux de propriétés |
| :--- |
| ![Property Sets](/02_Modelisation/00_communs/images/export-rvt/ExportIFCRevit3.PNG) |

| Niveau de détail |
| :--- |
| ![Level of Detail](/02_Modelisation/00_communs/images/export-rvt/ExportIFCRevit4.PNG) |

| Avancé |
| :--- |
| ![Advanced](/02_Modelisation/00_communs/images/export-rvt/ExportIFCRevit5.PNG) |

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

### Noms des modèles IFC

Les modèles IFC sont nommés de la façon suivante :
_CODE PROJET_-_CODE DISCIPLINE_-_CODE ILOT_-_CODE OUVRAGE_-_CODE PRODUIT_-_CODE PHASE_

Pour définir chaque code, se référer aux règles de nomenclatures qui suivent: 

#### Code Projet

Il s'agit du code du projet, attribué par Bouygues Immobilier en début de projet, qui restera le même jusqu'à la fin.

#### Code Discipline

| **Nom Discipline** | **Description** | **Code Discipline** |
| :--- | :--- | :--- |
| Bâtiment | Tout ouvrage unique construit | BAT |
| BIM Manager | Assemblage de maquettes | ASS |
| Géomètre | Maquette du site existant | SIT |
| Architecte | Travaux des architectes | ARC |
| Structure | Structure par bâtiment | STR |
| Fluides | Ventilation | CVC |
| Fluides | Plomberie | PLO |
| Électricité | Électricité | ELE |
| Sécurité incendie | Sécurité incendie | SSI |
| VRD | Réseaux, Voirie | VRD |
| Paysage | Aménagement et végétaux | PAY |
| Mobilier | Ensemble des mobiliers | MOB |

#### Code Ilot

| **Nom Ilot** | **Description** | **Code Ilot** |
| :--- | :--- | :--- |
| Ilot | Tout ensemble d’ouvrages communs | ILOT |

Dans le cas où il existe plusieurs îlots, le code îlot est implémenté de la manière suivante ILOT A, ILOT B,….


#### Code Ouvrage

| **Nom Ouvrage** | **Description** | **Code Ouvrage** |
| :--- | :--- | :--- |
| Bâtiment | Tout ouvrage unique construit | BAT |

Dans le cas où il existe plusieurs bâtiments, le code ouvrage est implémenté de la manière suivante BAT01, BAT02,…

#### Code Nature Poduit

| **Nom Famille Produit** | **Code Famille Produit** | **Nom Nature Produit** | **Code Nature Produit** |
| :--- | :--- | :--- | :--- |
| Logement | LOG | Maison individuelle | MIG |
| Logement | LOG | Maison jumelée | MJG |
| Logement | LOG | Maison en bande | MBG |
| Logement | LOG | Appartement | APT |
| Logement | LOG | Intermédiaire | INT |
| Logement | LOG | Social | SOC |
| Logement | LOG | Lots à bâtir | LOB |
| Logement | LOG | Résidence service | RES |
| Logement | LOG | Résidence étudiante | REE |
| Tertiaire | TER | Bureaux | BUR |
| Tertiaire | TER | Commerce | COM |
| Tertiaire | TER | Hôtel | HOT |
| Tertiaire | TER | Restaurant | RES |
| Tertiaire | TER | Restaurant Inter-Entreprises | RIE |
| Tertiaire | TER | Equipement culturel | ECU |
| Tertiaire | TER | Equipement petite enfance | EPE |
| Accessoire | ACC | Parking | PAR |

Dans le cas où il existe plusieurs zones de même nature de produit pour un même bâtiment, le code nature de produit est implémenté de la manière suivante APT01, APT02,…., COM01, COM02,…

#### Code Phase

Le découpage temporel d’une opération se base sur 10 phases bien distinctes.

| **Nom Phase** | **Description** | **Code Phase** |
| :--- | :--- | :--- |
| Etude Capacitaire | Correspond à une phase de modélisation  | ECA |
| Esquisse | prérequis de l'optimisation capacitaire | ESQ |
| Avant-Projet Sommaire | Correspond à la phase Faisabilité | APS |
| Avant-Projet Détaillé | Correspond à une phase de modélisation prérequis de l'optimisation de la Conception sommaire | APD |
| Lancement Commercial | Correspond à une phase de modélisation prérequis de l'optimisation de la Conception détaillée | LCO |
| Projet | Correspond à une phase de modélisation prérequis de la commercialisation | PRO |
| Appel d'Offres | Correspond à la phase Projet | AO |
| Exécution | Correspond à une phase de modélisation intégrant les corrections et variantes éventuelles | EXE |
| Livraison | Correspond à la phase Exécution des travaux | LIV |
| Exploitation | Correspond à la phase de gestion de la qualité | EXPL |

**Note :** Il est interdit de créer de nouveaux codes sans l’autorisation du BIM Manager de la MOA.

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