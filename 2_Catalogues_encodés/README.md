
## Catalogues numérotés de 1 à 6

Une première partie de mon stage était destinée à proposer un modèle d'encodage pouvant s'appliquer au plus grande nombre catalogues de vente de manuscrits et d'autographes. À titre d'essai, j'ai donc encodé à l'aide de GROBID-dictionaries un ensemble de catalogues diversifiés : vente aux enchères et prix marqués, différentes maisons d'éditions. Ces fichiers ont été utilisés pour générer la documentation (sous forme d'ODD) du projet e-ditiones ainsi que son schéma général. 

## Catalogues numérotés à 18 à 88

Une fois la chaîne de traitement des catalogues mise au point (cf. schéma ci-dessous), j'ai produit un corpus cohérent de catalogues en traitant les numéros 19 à 95 de la *Revue des Autographes* de Gabriel puis d'Eugène Charavay (à l'exception des numéros qui ne comprenait aucune liste d'autographes : 20, 42, 46, 47). Ce corpus a servi à peupler mon application de visualisation des catalogues. 

![alt text](https://github.com/lairaines/M2TNAH/blob/master/Chaine_Traitement_Catalogues.png)

## Transformations XSLT

Après leur structuration automatique *via* l'interface graphique de GROBID-dictionaries, les catalogues sont deux fois transformés à l'aide deux feuilles XSL. 
+ La première permet dote le catalogue d'un teiHeader conforme aux recommandations générales de la TEI et remplace les balises lexicographiques utilisées par GROBID-dictionaries par des balises plus adoptées à l'encodage des catalogues de vente. 
+ La deuxième numérote automatiquement tous les items présents dans un même catalogue.

## Retrouver un catalogue

Le fichier Liste_catalogues.tsv donne la correspondance entre les noms de fichier utilisés dans le cadre du fichier e-ditiones et les titres et numéros d'origine des catalogues traités automatiquement.
