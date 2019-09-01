
Ce dépôt Github réunit le mémoire et une partie des livrables techniques que j'ai réalisés pendant un stage de quatre mois à l'Institut de littérature française de l'Université de Neuchâtel. 

L'enjeu de mon stage était de proposer une **chaîne de traitement** complète, efficace et automatique permettant le **passage d'un corpus numérisé de catalogues** de vente d'autographes de la deuxième moitié du XIXe siècle **à une base de données** aisément accessible et interrogeable.

Le mémoire consultable sur ce dépôt décrit notamment les aspects techniques du travail effectué au cours de mon stage. Il détaille et évalue les outils numériques sélectionnés et mis en œuvre à chaque étape : reconnaissance automatique du texte grâce à Transkribus, structuration automatique des données grâce à GROBID-dictionaries, mise en place de transformations XSLT et d'associations avec des schémas pour assurer la correction manuelle des fichiers et leur intégration au projet e-ditiones. Il démontre en particulier la pertinence et l'adaptabilité du logiciel GROBID‑dictionaries pour le traitement de ressources non lexicales mais de forme encyclopédique.

Au cours de ce stage, j'ai :
+ produit quatre jeux de données (un général et trois spécifiques) pour entraîner GROBID-dictionaries et srtucturer automatiquement des catalogues de vente à la mise en page variée (**dossier 1**).
+ encodé, grâce à ces modèles, plus de 70 catalogues de vente d'autographes (**dossier 2**).
+ conçu un schéma Relax NG qui permet de corriger efficacement les fichiers structurés automatiquement par GROBID-dictionaries (**dossier 3**).
+ conçu un schéma général et une documentation s'appliquant à l'ensemble du projet e-ditiones (**dossier 4**).

Une application de publication de ces catalogues en ligne a par ailleurs été développée grâce au système eXist-db.

