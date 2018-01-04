# Renseignement des informations du projet

Les informations du projet doivent être renseigné dans le logiciel Allplan au démarrage du projet selon la méthode suivante. 

* Dans l'espace de mise en page des plans, sélectionner la commande "Ouvrir sur la base du projet: plans" (1) et ensuite ouvrir les "Attributs du plan et du projet".

![](/02_Modelisation/00_communs/images/Info projet Allplan 2.png)

* Ouvrir les attributs du projet
![](/02_Modelisation/00_communs/images/Info projet Allplan 3.PNG)

NOTA les propriétés renseignées sortent dans un IfcPropertySet "attribus projet" du IfcOwnerHistory



---

Pour savoir comment exporter en IFC depuis Allplan, veuillez consulter [Exporter en IFC depuis Allplan](/02_Modelisation/00_communs/export-allplan.md)


En IFC:

IfcProject.Name = Numéro du projet, tel que indiqué sur Bimsync

IfcProject.LongName = Nom du projet tel que indiqué sur Bimsync

IfcProject.Phase = Phase du projet

IfcAddress.Description=Type de projet

IfcAddress.UserDefinedPurpose=Destination du projet

IfcPostalAddress.AddressLines=Adresse du projet \(numéro et rue\)

IfcPostalAddress.Town=la ville du projet

IfcPostalAddress.Region = La région du projet

IfcPostalAddress.PostalCode= Le code postal

IfcPostalAddress.Country = La nation du projet







