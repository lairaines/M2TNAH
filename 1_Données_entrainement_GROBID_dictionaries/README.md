
Dans ce sous-répertoire se trouve un choix raisonné des données d'entraînement et d'évaluation que j'ai produites au cours de mon stage à l'UniNe.

## Utiliser GROBID-dictionaries pour encoder des catalogues de vente d'autographes

GROBID-dictionaries est un logiciel reposant sur l'apprentissage supervisé et permettant l'encodage automatique au format XML-TEI de ressources lexicales ou de forme encyclopédique.

Les étapes pour installer GROBID-dictionaries, créer de nouveaux modèles ou entraîner des modèles préexistants afin de traiter des docuements sont disponibles [ici](https://github.com/MedKhem/grobid-dictionaries/wiki/Docker_Instructions9).

## Développement d'un modèle général grobid_CAT

L'un des objectifs de mon stage était de déterminer s'il était plus efficace de développer des modèles spécifiques de la mise en page de chaque catalogue de vente ou de produire un modèle général pour tous les types de catalogues.

Les données d'entraînement et d'évaluation du modèle générale sont extraites des publications et catalogues suivants :
+ Gabriel Charavay, _Revue des Autographes_, première série : 25, 35, 50, 80.
+ Gabrielle Charavay _Revue des Autographes_, deuxième série : 24, 56.
+ Auguste Laverdet, _Catalogue de lettres autographes et manuscrits_ : 1, 22.
+ Noël Charavay, _Catalogue d’une intéressante collection de lettres autographes…_ (14 décembre 1908).
	
Ce modèle général donne des résultats satisfaisants pour tous les types de catalogues de vente susceptibles d'être traités (prix marqués ou vente aux enchères. J'ai cependant constaté que dans le cas précis de mon stage, restreindre à certains niveaux les données d'entraînement permettait d'obtenir des résultats encore plus exacts et diminuait le temps de correction manuelle de chaque catalogue.

Le choix du jeu de données avec lequel GROBID-dictionaries est entraîné dépend donc de la mise en page de la série de catalogues à traiter.

## Quand choisir le jeu de données grobid_RDA_LAD?

**Lorsqu'on traite des catalogues à prix marqués qui ont la même mise en page que la _Revue des autographes_ (voir ci-dessous), GROBID dictionaries doit être entraîné avec le jeu de données grobid_RDA_LAD.**

<br/>![alt text](https://github.com/e-ditiones/GROBID/blob/master/RDA_LAD.png)
_Revue des autographes, Gabriel Charavay. (Première série N°42, Décembre 1874)_

<br/>À tous les niveaux, le jeu de données contient des données extraites de divers numéros de _Revue des Autographes_ (25, 35, 50, 80 de la première série / 24, 56 de la deuxième).

## Quand choisir le jeu de données set grobid_OTHER_FIXED_PRICES?

**Lorsqu'on traite des catalogues à prix marqués dont la mise en page n'est pas aussi structuré que la _Revue des autographes_ (voir ci-dessous), GROBID dictionaries doit être entraîné avec le jeu de données grobid_OTHER_FIXED_PRICES.**

<br/>![alt text](https://github.com/e-ditiones/GROBID/blob/master/OTHER_FIXED_PRICES.png)
_Catalogue de lettres autographes et manuscrits, Auguste Laverdet (N°1, Avril 1856.)_

<br/>Le jeu de données contient au niveau "dictionary body segmentation" des données issues des catalogues à prix marqués d'Auguste Laverdet (numéro 1 and issue 22). Aux niveaux inférieurs, il contient les mêmes données que le modèle général.

## Quand choisir le jeu de données grobid_AUCTION?

**Lorsqu'on traite des catalogues de vente aux enchères sans indication de prix (voir ci-dessous), GROBID dictionaries doit être entraîné avec le jeu de données grobid_AUCTION.**

<br/>![alt text](https://github.com/e-ditiones/GROBID/blob/master/AUCTION.png)
_Catalogue d’une intéressante collection de lettres autographes…, Noël Charavay (Décembre, 14th 1908)_

<br/>Le jeu de données contient au niveau "dictionary body segmentation" des données issues d'un catalogue de vente produit par Noël Charavay pour une vente aux enchères (14 décembre 1908). Aux niveaux inférieurs, il contient les mêmes données que le modèle général.

## Crédits

GROBID dictionaries est développé par Mohamed Khemakhem ([GitHub](https://github.com/MedKhem)). Plus d'informations sur les technologies GROBID est disponible [ici](https://grobid.readthedocs.io).

## License

Concernant `GROBID`, cf. [ici](https://github.com/MedKhem/grobid-dictionaries).

Concernant les jeux de données : CC-BY.  

<a rel="license" href="https://creativecommons.org/licenses/by/2.0"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/2.0/88x31.png" /></a><br />

## Citer ces jeux de données

Lucie Rondeau du Noyer, Simon Gabay, Mohamed Khemakhem, Laurent Romary. 2019. _Training and evaluation data for encoding Manuscript Sales Catalogues with GROBID dictionaries_.


