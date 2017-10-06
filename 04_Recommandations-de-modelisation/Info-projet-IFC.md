# Renseignement des informations de projet

Il est requis que le propriétés attachées au IfcBuilding des IFC extraits depuis les modèles en format natif respectent les indications suivantes:

| PropertySet | Property | Valeurs possibles | Explication |
| :--- | :--- | :--- | :--- |
| Pset\_BuildingCommon | BuildingID | Texte | Le numéro du projet |
|  | OccupancyType | Bureaux, logements, hôtel, commerces,  | La destination  |
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
| IfcPostalAddress | IfcPostalAddress.Country | Texte | La nation du projet, en langue française \(Ex. France, Royaume-Uni, Espagne, ...\)  |
|  | IfcPostalAddress.Region | Texte | La région du projet \(Ex. Ile-de-France |
|  | IfcPostalAddress.Town | Texte | La ville du projet |
|  | IfcPostalAddress.PostalCode | Texte | Le code postale du projet |
|  | IfcPostalAddress.AddressLines | Texte | L'adresse du projet sous forme: numéro, rue/place/avenue/... nom  |



