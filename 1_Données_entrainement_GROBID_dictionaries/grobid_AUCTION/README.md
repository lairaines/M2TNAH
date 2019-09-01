
## Corpus

Le corpus est constitué de numérisations de revues et catalogues produites par Auguste Laverdet, de la *Revue des autographes* de Gabriel Charavay ([data.bnf](http://data.bnf.fr/10429866/gabriel_charavay/)) et d'un catalogue de vente aux enchères édité par l'autre maison Charavay.

## Méthodologie

Les fichiers PDF sont OCRisés avec [Transkribus](https://transkribus.eu). 

Ce modèle est entraîné à partir de 4 types distincts de catalogues. Pour chacun, 15 pages annotées sont disponibles : 10 comme données d'entraînement et 5 comme données d'évaluation. 

Les données d'entraînement et d'évaluation du modèle "auction" sont extraites des publications et catalogues suivants :

+ Gabriel Charavay, *Revue des Autographes*, première série : 25, 35, 50, 80.
+ Gabrielle Charavay *Revue des Autographes*, deuxième série : 24, 56.
+ Auguste Laverdet, *Catalogue de lettres autographes et manuscrits* : 1, 22.
+ Noël Charavay, *Catalogue d’une intéressante collection de lettres autographes…* (14 décembre 1908).

La source des données est indiquée par les acronymes suivants :
+ RDA_1 pour la Revue des Autographes, première série
+ RDA_2 pour la Revue des Autographes, deuxième série 
+ LAV pour les catalogues d'Auguste Laverdet
+ ETI for auction catalogues de Noël Charavay

En accord avec les [préconisations de Grobid⁻Dictionaries](https://github.com/MedKhem/grobid-dictionaries/wiki/How-to-Annotate%3F), les séparateurs typographiques sont étiquetés avec la balise <pc>.
  
Exemple : 

            <entry>
                <num>350</num>
                <pc>.</pc>
                <form>
                    <name>STANISLAS</name>
                    <pc>,</pc>
                    <desc>roi de Pologne N. 1677. M. 1766</desc>
                </form>
                <pc>. -</pc>
                <sense>
                    <subSense>L. aut. sig. à madame de Boufïlers. Lunéville, 5 janvier 1741. 1 page in-4, 10</subSense>
                </sense>
            </entry>
            <pc>»</pc>
            <entry>

## Dossiers
Les données d'entraînement ("corpus") et les données d'évaluation sont disponibles dans le fichier `ToyData`.

## Crédits

GROBID dictionaries est développé par Mohamed Khemakhem ([GitHub](https://github.com/MedKhem)). Plus d'informations sur les technologies GROBID est disponible [ici](https://grobid.readthedocs.io).

## Licence

Concernant `GROBID`, cf. [ici](https://github.com/MedKhem/grobid-dictionaries).

Concernant les jeux de données : CC-BY.  

<a rel="license" href="https://creativecommons.org/licenses/by/2.0"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/2.0/88x31.png" /></a><br />

## Citer ce jeux de données

Lucie Rondeau du Noyer, Simon Gabay, Mohamed Khemakhem, Laurent Romary. 2019. _Training and evaluation data for encoding Manuscript Sales Catalogues with GROBID dictionaries_.

