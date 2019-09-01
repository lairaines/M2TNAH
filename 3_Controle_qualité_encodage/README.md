
Le schéma schema_grobid_output.rng a été élaboré pour faciliter la correction manuelle des entrées de catalogue structurées automatiquement par GROBID‑dictionaries. Comme le montre le schéma de la chaîne de traitement est associé au fichier automatiquement struturé par GROBID-dictionaries après la première transformation XSLT.

![alt text](https://github.com/lairaines/M2TNAH/blob/master/Chaine_Traitement_Catalogues.png)

Le schéma contient notamment des règles rédigées en langage Schematron. Elles visent à vérifier deux aspects de l’encodage automatique des catalogues de vente d’autographes par GROBID-dictionaries. 

+ Le premier concerne l’enchaînement de la séquence des composantes de chaque élément <item>. Il s’agit de vérifier la présence, au minimum, d’un numéro de lot (élément <num>), d’un nom d’auteur (élément <name>) et d’une description standardisée (<desc>). 
+ La deuxième règle vérifie que les lots sont numérotés de manière continue. 
  
  
