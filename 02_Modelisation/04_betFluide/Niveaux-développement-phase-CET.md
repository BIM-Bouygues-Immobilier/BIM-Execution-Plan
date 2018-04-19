#Les niveaux de développement par phase: les modèles Fluides 

{% include "../../00_Referentiel/ND-projet.md" %}

> Pour connaitre les recommandations générales de modélisation pour les BET Fluides, cliquez [ici](/02_Modelisation/04_betFluide/modelisation-rvt.md ). 

## Phase APS/Dépôt PC  

Le modèle numérique fluides comprendra les éléments suffisant pour permettre le déroulement de la pré-synthèse technique et architecturale et pour extraire des quantitatifs sommaires.
Tout élément impactant le volume des pièces (hauteurs sous plafond, dimensions des trémies et des locaux techniques, ...) devra, de manière générale, être intégré dans cette phase. 

|[Téléchargez un exemple de modèle CET APS/PC](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/04_betFluide/images/CET_APS.zip) | 
| :---: | 
|[![](/02_Modelisation/04_betFluide/images/FLU_APS.PNG)](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/04_betFluide/images/CET_APS.zip)|

Le modèle Fluides intègre les éléments et les caractéristiques listées ci-après:

* Les principaux locaux techniques avec matérialisation des volumes d'accès/maintenance
* Les verticalités et les sorties de trémie à tous les étages
* La distribution des terminaux chauffage, ventilation et climatisation
* L’implantation et l’encombrement des principaux équipements techniques hors locaux techniques (Ventilo convecteur, UTA, rideaux d'air chaude, ballons d'eau chaude, TD,...) avec matérialisation des aires d'accès/maintenance
* Les gaines aérauliques et hydrauliques principales horizontales sur tous les étages
* Les gaines aérauliques et hydrauliques principales et secondaires sur les étages type et spéciaux \(tels que définis par le MOA\), avec modélisation de l'isolation des gaines et canalisations
* Le cheminement des réseaux gravitaires
* L’implantation des chemins des câbles sur tous les étages
* L’implantation des appareils d’éclairage
* Les accessoires de gaine et de canalisation ne sont pas demandés à ce stade, à l'exception des clapets coupe-feu. 
* La coordination avec les réseaux concessionnaire avec l'implantation des points de connexion \(y compris les équipements associés\) en limite de propriétés/bâtiment
* La modélisation des cheminements des principaux réseaux extérieurs, en coordination avec les réseaux existants

> Les réseaux et les terminaux, même si déconnectés, devront être affectés aux systèmes. 
> Pour la modélisation des équipements, des terminaux et des accessoires, il faudra privilégier l'utilisation de "familles génériques" ou "standard" plutôt que des "familles fournisseurs"
> La modélisation des espaces n'est pas demandées et elle est laissée à discrétion du bureau d'étude, qui pourra les intégrer de façon cohérente avec les pièces du modèle architecte.


##Phase APD
|[Téléchargez un exemple de modèle Fluides APD](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/04_betFluide/images/CVC_APD.zip)|
|:---:|
|[![](/02_Modelisation/04_betFluide/images/FLU_APD.PNG)](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/04_betFluide/images/CVC_APD.zip) |

Le modèle Fluides intègre, entre autre, les éléments et les caractéristiques listées ci-après:
* Le maquettage des tous les locaux techniques, des réseaux aérauliques, hydrauliques, gravitaires, chemins de câble primaires et secondaires sur tous les étages
* Le bouclage en modélisation de tous les systèmes \(=Tous les éléments doivent être connectés\)
* Le positionnement des grilles en faux plafond
* La modélisation des cheminement de l’ensemble des réseaux extérieurs en coordination avec les réseaux existants
* Les principaux accessoires des gaines et canalisatiosn
* Les isolants de gaines et canalisations
* Le renseignement des débits dans les réseaux principaux
* L’implantation des terminaux électriques principaux
* La gestion des réservations primaires

## Phase PRO/DCE

|[Téléchargez un exemple de modèle Fluides PRO/DCE](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/04_betFluide/images/FLU_PRO.zip) | 
| :---: | 
|[![](/02_Modelisation/04_betFluide/images/FLU_PRO.PNG)](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/04_betFluide/images/FLU_PRO.zip)|
|[**Téléchargez un exemple de modèle Electricité PRO/DCE**](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/04_betFluide/images/ELE_PRO.zip)|
|[![](/02_Modelisation/04_betFluide/images/ELE_PRO.PNG)](https://github.com/BIM-Bouygues-Immobilier/BIM-Execution-Plan/raw/master/02_Modelisation/04_betFluide/images/ELE_PRO.zip)|

La modélisation en cette phase a pour objectif celui de fournir la préparation des éléments pour les marchés de travaux.
Le niveau de définition est suffisant pour arrêter l’ensemble des prestations. Toutes les composantes des modèles numériques sont définis, positionnées, repérées et renseignées de manière exhaustive, de façon à permettre une description détaillée de l’ouvrage.
L’organisation des composants est faite en fonction du découpage en lots envisagé pour la consultation des entreprises.
La modélisations doit permettre d’établir un cout prévisionnel des travaux décomposés par corps d’état, sur la base d’un avant-métré.
Le modèle Fluides intègre dans cette phase :
* Le renseignement de l’ensemble du matériel avec les spécifications techniques \(désignation, fonction, …\)
* L’affinement de la modélisation des réseaux, des locaux techniques, des isolants et des accessoires de gaines et de canalisations
* L’implantation de tous les terminaux électriques
* La caractérisation des matériaux des réseaux, des types d'isolants (CF, calorifuge, ...)
* Le renseignement des débits sur tous les réseaux

---

Si vous souhaitez connaitre les niveaux de développement des autres intervenants, vous pouvez consulter:
* Les niveaux de développement des modèles structure [ici](/02_Modelisation/03_betStructure/Niveaux-développement-phase-STR.md)
* Les niveaux de développement des modèles architecte [ici](/02_Modelisation/02_architecte/Niveaux-développement-phase-ARC.md)

---

Image credits [here ](/CREDITS.md)