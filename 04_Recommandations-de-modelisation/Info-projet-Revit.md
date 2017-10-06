# Renseignement des informations du projet

Les informations du modèle Revit \(Onglet "Gérer"&gt;"Informations du projet"\) doivent être renseignées en suivant ces indications:

![](/assets/Info projet.png)

| _Nom de la propriété_ | _Valeur_ |
| :--- | :--- |
| Etat du projet | Correspond à la phase en cours, à choisir parmi: les valeurs ESQ, APS-PC, LCO, DCE, EXE, LIV |
| Nom du projet | Le nom du projet en cours |
| Nom du client | Bouygues Immobilier |
| Adresse du projet | L'adresse du projet |
| Nom du projet | Le nom du projet, tel que défini dans le projet Bimsync |
| Numéro de projet | Le numéro du projet, tel que défini dans le projet Bimsync |

Il est requis que le propriétés attachées au IfcBuilding des IFC extraits depuis les modèles en format natif respectent les indications suivantes. Veuillez trouver \[ICI\] les fichiers texte à importer lorsque vous allez exporter votre IFC depuis Revit afin de suivre les correspondances suivantes. 

| PropertySet | Property | Valeurs possibles | Explication |
| :--- | :--- | :--- | :--- |
| Pset\_BuildingCommon | BuildingID | Texte | Le numéro du projet |
|  | OccupancyType | Bureaux, logements, hôtel, commerces, ... | La destination |
|  | GrossPlannedArea | Numéro \(Surface\) | La surface programme |
|  | NumberOfStoreys | Numéro | Le nombre d'étages |
|  | YearOfConstruction | Texte | L'année de construction/livraison du projet |
| Pset\_ProjectCommon | ConstructionMode | Rénovation, Nouvelle construction | Le type de projet |

| Entity | Property | Valeurs possibles | Explication |
| :--- | :--- | :--- | :--- |
| IfcBuilding | IfcBuilding.Name | Texte | Le numéro du projet |
|  | IfcBuilding.LongName | Texte | Le nom du projet en cours |
|  | IfcBuilding.BuildingAddress | Texte | L'adresse postal du projet |
| IfcProject | IfcProject.Phase | ESQ, APS-PC, LCO, DCE, EXE, LIV | La phase du projet |
| IfcPostalAddress | IfcPostalAddress.Country | Texte | La nation du projet, en langue française \(Ex. France, Royaume-Uni, Espagne, ...\) |
|  | IfcPostalAddress.Region | Texte | La région du projet \(Ex. Ile-de-France |
|  | IfcPostalAddress.Town | Texte | La ville du projet |
|  | IfcPostalAddress.PostalCode | Texte | Le code postale du projet |
|  | IfcPostalAddress.AddressLines | Texte | L'adresse du projet sous forme: numéro, rue/place/avenue/... nom |

---

Pour savoir comment exporter en IFC depuis Revit, veuillez consulter \[Cfr. [Exporter en IFC depuis Revit](/04_Recommandations-de-modelisation/Export-depuis-Revit.md)\]

