Les planchers sont modélisés à l'aide de l'outil Sol de {{logiciel}}.

Le nom du type du  doit suivre le schéma suivant :

> SOL-_type/description_-_matériaux_-_épaisseur (en cm)_ 

Dans le cas de plancher multicouche, le nom du type se fera suivant la codification et l’ordre suivant  :

> SOL-_type_-_matériaux_-_épaisseur (porteur)_-_matériaux_-_épaisseur (sous face de dalle)_-_matériaux_-_épaisseur (dessus de dalle)_-_épaisseur totale du complexe en cm_

Exemple pour un plancher acoustique :
SOL-DALLE-BETON  20-ISOLANT-8  -CHAPE-5-PARQUET-2-35cm

Attention dans la description des couches, toujours partir du dessous de dalle vers le dessus. Les épaisseurs seront toujours en cm.
Dans le cas de plancher multicouche, le code CCTP devra être entrée pour chaque couche directement dans le matériau.

Les valeurs possibles sont indiquées ci-dessous :

#### Nom des types de planchers

{% include "/00_Referentiel/NomDesPlanchers.md" %}