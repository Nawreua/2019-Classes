Approche Consulting des Métiers de la Data
==============================

## Introduction

Alain Fajner

* 4 modules de 3h
* Des cas pratiques (SQL)
* Evaluation finale => Soutenance

### Qu'est-ce que la "data" ?

**_Donnée:_** Description élémentaire d'une réalité. Ex: observatio, mesure. Elle est partout. Actif stratégique de l'entreprise. Couche emotionnelle par rapport à de l'info brute.

### Perception des données

* Utilisation éthique des données est bien perçue par chaque citoyen
* De nouvelles règles, contraintes et moyens de protection de la vie privée sont apparues (GDPR, ...)
* Transgressions éthiques sont faciles à effectuer (morales machines, ...)
* Utilisation des données peut donner lieu à des choix éthiques
* Analyser utilisation des données amène à définir la stratégie data, la qualité des données, la confiance en la donnée et la sécurité

### Entreprises centrées data

Les entreprises centrées sur la data superforment car elles ont un meilleur partage de la connaissance, elles ont une meilleur organisation collaborative, ont une culture de l'innovation et de la créativité.

Productivité plus élevée, profitabilité plus élevée et une meilleure valeur marché => 50% plus élevée.

**On va parler de la mise en commun des différentes informations.**

### Types de données

* Données structurées
	* Structure figé
* Données semi-structurées
	* Information de type clé
* Données non structurées
	* Donnée à l'état brute
	* On connait pas la valeur

| BI classique | Big Data |
|---|---|
| Donnée structurée | Donnée non structurée |
| Donnée semi-structurée | Donnée semi-structurée |

## Business Intelligence

* 1958 : Hans Peter Luhn, chercheur chez IBM, 1er à parler de BI : *Capacité à appréhender les relations entre des faits présentés afin de guider les actions vers un but désiré*
* 1970 -> 1990: Reporting
* Depuis 1990: Entrepôts de données
	* Données historisées, croisées et préparées
	* Outils diffusés plus largement
	* Sens décisionnel -> Transactionnel
	* Structuration de la donnée, modélisation spécifique

| Département | Processus métier | KPI |
|---|---|---|
| Logistique | Acheminer, transporter | Taux de retour, Délai moyen |
| Achats | Acheter | Delais commandes / livraison |
| RH | Recruter, former | Turnover, Age moyen |
| Gestion, finance | Gérer, facturer | CA, résultat net, Montant impayé |
| Commercial, ventes | Vendre, gérer le client | Panier moyen, Churn, Avancement |
| Marketing | Promouvoir | ROI campagne marketing, Coût acquisition d'un nouveau client |

|  | Opérationnel | Décisionnel |
|---|---|---|
| Objectif | Gérer les transactions des processus métiers | Analyser et prendre les décisions stratégiques et/ou tactiques |
| Moyen | Processus métier | Axes d'analyses et indicateurs |
| Synchronisation | Temps réel | Asynchrone |
| Horizon temporel | Habituellement court terme, afin de compléter les processus métier | Moyen ou long terme |
| Stabilité des besoins | Stables | Evolution constante, requêtes à la demande |
| Données | Données transactionnelles brutes | Données contrôlées, qualifiées, agrégées et historisées |

## Architecture classique d'un Datawarehouse: données

Sources -> | Acquisition -> Socle -> Accés | -> Restitution

Méta-Data (Audit, lineage) chapote le corps

### Sources:
* Sources structurées
* Fichiers externes
* Fichiers plats
* File JMS
* Puits de données

### Acquisition:
* Données structurées
* Table en DB

### Socle:
* Master Data
* Reference Data
* Transaction Data
* Table en DB modéle spécifique ou générique

### Accés:
* Structures logiques
* Vue en DB

### Restitution:
* Reporting
* Data visualization
* OLAP
* Ad hoc
* Data mining

## Différents types de données

* Données transactionnelles: données portant des informations quantitatives
* Données de référence: données très stable n'évoluant que rarement
* Méta-data
* Données maîtres: master data

### Test de connaissances

| Donnée | Type |
|---|---|
| Ligne de commande d'achats | Transactionnelles |
| Civilité | Master Data |
| Ligne de facture | Transactionnelles |
| Clients | Master Data |
| Tickets de caisse | Transactionnelles |
| Relèves de compteurs | Transactionnelles |
| Pays | Données de référence |
| Codes postaux | Données de référence |
| Produits | Données de référence |

## Approche consulting

### Par où je commence ?

1. Récupérer les besoins de restitution
2. Confronter les besoins de restitution aux données fournies par le système

### Présentation des données

Les données sont _le plus souvent_, le plus facilement exploitables par des outils de BI et avec la meilleure performance lorsqu'elles représentées sous de forme de modélisation relationnelle (3NF).

#### 3NF

##### Avantages

* Facile à modéliser
* Evolutivité
* Répond à toutes les questions possibles

##### Inconvénients

* Lisibilité réduite
* Peu performant quand utilisé sur des matériels non dédiés
* Requêtage complexe

#### Cas pratique

* Société électronique
* Vente en magasin uniquement
* Magasins partout dans le monde

#### Modéle en étoile

* Table centrale dite de faits, contenant des mesures
* Table de dimension référencée par le table de faits

![stardb](file://media/338810750.png)

**On va dénormaliser, mais concentrez-vous sur la volumétrie de la table de faits.**

##### Avantages

* Meilleur lisibilité surtout par les métiers
* Performance optimale
* Requêtage facilité

##### Inconvénients

* Evolutivité réduite
* Modélisation plus complexe que la modélisation relationnelle
* Modélisation guidée par des besoins prédictibles

##### Modéle en étoiles vs Modéle en flocons

* Modéle en étoile
	* Répétition des dimensions (noms)
	* Conceptuellement dérangeant
	* Mise à jour d'un nom
* Modéle en flocons
	* Place en mémoire

## Les données manipulées par un système décisionnel

### Dimensions conformes

Un des moyens est d'effectuer des analyses croisées est d'utiliser des dimensions "conformes" => la dimension est définie de manière unique dans tout le système (à minima, mm granularité)

### Livrables liés à la modélisation

* Modèles de données logiques => livrable de phase conception
	* Doivent être approuvés par le client
	* Important impliquer client dès le début du travail sur le modèle
	* Traduction physique du modèle logique est de la responsabilité de la sociéte responsable de l'intégration. Souvent défini dans le SLA: délais d'alimentation, sauvegardes, délai de réponse d'une requête

### Stockage

*Appliance*: Matériel dédié pour une tâche donnée

1. Bases de données traditionnelles: Ces bases de données ne sont pas faites à l'origine pour répondre à des besoins décisionnels et nécessitent l'utilisation de modèles en étoiles, d'agrégats,... pour des raisons de perfomance
	* Oracle
	* DB2
	* Microsoft SQL Server
2. Appliances décisionnelles: systèmes logiciels et matières construits spécifiquement pour le décisionnelle
3. Cloud: privé, public, managé

#### Centre de gravité des données

* Le centre de gravité des données est le lieu de stockage le plus naturel des données d'un point de vue économique
* Historiquement, la gravité des données analytiques a été très proche des data centers d'entreprise
* Comme les données utilisées dans les écosystèmes analytiques proviennent de plus en plus des sources externes, on observe un déplacement de la gravité des données d'un stockage on-premise à un stockage off-premise
* Dans de nombreux cas, il est impossible de copier la totalité d'une source de données externe dans un entrepôt d'entreprise
* Les sytèmes opérationnels transitent vers le cloud et les entrepôts analytiques commencent à suivre.

#### Appliances décisionnelles

* Système logiciel et matériel construit spécifiquement
* Systèmes massivement parallèles
* Différents support de stockage en fonction de l'utilisation des données
* Modélisation relationnelle peut être suffisante
* Etat de l'art: Teradata, IBM Netezza, ...

Données froides: données peu utilisés, peut être mise sur HDD

Données chaudes: données fréquement utilisés, peut être mise sur SSD

#### Cloud: caractéristique des service

1. A la demande et en self-service -> facile et rapide à utiliser
2. Large accès au réseau -> Accès via Internet (ou connexion directe)
3. Mise en commun de ressources -> Environnement partagé (sécurité/séparation virtuelle)
4. Elasticité rapide -> Augmente ou diminue rapidement (sans limite de capacité)
5. Service mesuré -> Paiement en fonction de l'anticipation ou à la consommation (sans engagement en amont)

* Les prix et les niveaux de service sont standards - pas personnalisé par rapport à chaque client
* Des réductions importantes sont accordées en fonction des engagements

Le marché évolue d'un modèle Capex à un modèle Opex

##### Trois principaux types de Cloud

1. Cloud managé
2. Cloud privé
3. Cloud public

##### Impacts réseaux du Cloud

* LAN friendly != WAN friendly, temps de latence sont les ennemis, TCP/IP garantit la livraison des paquets ce qui ralentit le réseau
* Minimiser les temps de latence en choisissant la localisation Cloud la plus proche
* Minimiser les mouvements de données via le réseau
* Maximiser la taille de buffer des données des applications
* Essayer des tailles de paquets différentes

##### Avis entreprises

90 % des clients en mode Cloud Hybride en 2020

85 % cherchent à acheter "As a service" OPEX vs CAPEX

40 % Traitements exécutés sur un Cloud Public en 2020

### Datamart

Sous-ensemble des données du DataWarehouse couvrant un domaine métier précis. Il est constitué d'une ou plusieurs étoiles et peut être logique ou physique.

Il peut présenter des données agrégées ou non.

### Cubes

**OLAP**: On Line Analytic Processing (par opposition à **OLTP**, On Line Transaction Processing)

Aggrégats non standards

Etat de l'art: Microsoft SSAS, IBM Cognos

#### Différents types d'OLAP

* MOLAP: Multidimensionnal OLAP
* ROLAP: Relationnal OLAP
* HOLAP: Hybrid OLAP
* DOLAP: Desktop OLAP

### Couche sémantique

Les outils de restitution se basent rarement directement sur les tables de base de données -> ils se basent sur la couche sémantique

### Restitution des données

Restitution:

* Reporting -> reporting statique
* Ad-hoc -> reporting interactif
* Dashboard

### Principes de constructions du DataWarehouse

* Un DataWarehouse est évolutif, je ne mets dans un datawarehouse industriel que ce qui m'est utile et répond à mes besoins implicites ou explicites
* Ceci n'est pas vrai pour le BigData ou l'exploratoire

### Vacation

* Flux de données ayant une cohérence fonctionnelle et temporelle entre elles des systèmes sources vers la zone d'accès de l'entrepôt de données
* Une vacation a une périodicité (quotidienne, hebdomadaire, mensuelle, ...)
* Elle véhicule une date fonctionnelle

### ETL (Extract Transform Load)

* Outil utilisé pour effectuer des traitements en masse sur des données
	* Traitements DataWarehouse
	* Traitements de migration de données
* Il existe 3 types d'outils ETL
	* moteur
	* In-Database
	* Générateurs de code
* Exemples: Informatica PowerCenter, IBM Datastage

### Stratégie de rejets fonctionnels / recyclages

* Bien définir la stratégie au moment de la conception
* Les données rejetées sont les données qui ne respectent pas l'intégrité référentielle

### Mécanisme de rejet / recyclage

* Une table de rejet à l'image de la table source dans la zone d'acquisition ou une partition de la table source

### Principe d'alimentation des structures dimensionnelles

* Les tables de dimensions s'alimentent de manière classique (ajout, mise à jour)
* Généralement pas de suppression dans les tables de dimension (des faits peuvent porter dessus même si très anciens)
* Les tables de faits ne s'alimentent généralement qu'en ajout
	* Remplacement d'un montant de facture par un autre -> on passe une facture avec un montant négatif et on ajoute la nouvelle facture

### Dimensions à évolution lente (SCD)

Trois types:

1. On remplace l'ancienne valeur par la nouvelle, pas d'historisation
2. On historise à chaque changement. Généralement, on ajoute trois champs: "date début de validité", "date fin de validité" et "valeur courante", exemple : ![Exemple type 2 SCD](file://media/1657239972.png)
3. On ajoute une colonne ancienne puissance

## Exercice pour le 27/05

* Modèle: ![Marketing Laboratoire](file://media/717354015.png)
* Historisation pour: Médecin -> Pays
* Dénomination locale vs internationale: Table médicament contient la dénomination internationale et table marque pour les dénominations internationale avec une référence vers le médicament avec la dénomination unique voulue.

## Qualité de données, Master Data Management et Déroulement d'un projet Data

### Qualité de données

"The degree to which _data can be a trusted source_ for any and/or all intented uses in operations, decision making and planning."

#### D'où viennent les problèmes de qualité de données ?

Au fil du temps, les données ont tendance à se détériorer dans le système d'information ce qui engendre des informations incorrectes, périmées, manquantes ou en doublons.

#### Impact de la mauvaise qualité de donnée

* Système opérationnel
	* Non facturation de certains clients
	* Migration difficile
	* Fusions/consolidations d'applications
* Système décisionnel
	* Impossibilité de rapprocher certaines données
	* Différence de résultat suivant les DataMarts

#### Six critères de mesure de la qualité des données

* Complétude
* Conformité
* Consistance
* Précision
* Duplication
* Intégrité

#### La qualité de données, un processus itératif

1. Analyse des sources
2. Détection des incohérences
3. Spécification des règles, des indicateurs de qualimétrie
4. Implémentation des règles
5. 
6. 

#### Outillage de la gestion de la qualité de données

* Data profiling
* Data cleansing
* Data monitoring

## Big data

Le développement et l'adoption des produits est de plus en plus rapide, téléphone : 50 ans, Pokémon Go: 19 jours

En 60 secondes:
	* 694 444 hours watched Netflix
	* 2,1 Million Snap created
	* 4,5 Million Video Youtube viewed

**Consumer journey**:

* Then: Stimulus -> Shelf -> Experience
* Now: Stimulus -> Zero Moment of Truth (Review, Ratings, Search, ...) -> Shelf -> Experience -> Next customer's ZMOT

> Digital is the main reason just over half of companies on the Fortune 500 have disappeared since the year 2000

Pierre Nanternne, CEO of Accenture

L'IoT est partout autour de nous: 50 milliards d'objets connectés d'ici 2020

Comment extraire de la valeur de cet énorme volume de données de différentes natures et qui évoluent très vite ?

### Qu'est-ce que la Big Data ?

C'est une évolution de la data, l'objectif est d'analyser les données pour prendre des décisions, comme le décisionnel classique, mais cela ajoute de la profondeur et de nouveaux types d'analyse.

Big Data: Exaoctets, réseaux sociaux, user generated content, visites web, sentiments, e-mail, graphes, chemins, voix, texte

Sans big data: Vue Client classique, Avec Big Data: Vue Client Etendue

### BI Traditionnelle VS Exploration Big Data

Le métier détermine les questions à poser =BI Traditionnelle (Analyse structurée et réitérable)> L'IT structure les données pour répondre à ces questions

L'IT fournit une plateforme pour stocker, approfondir et analyser toutes les sources données =Big Data Analytics> Le métier explore les données pour trouver les questions intéressantes à poser

### Un nouveau processus: la découverte

* Connaissance orientée-données
	* Visualisation de grosses masses de données
	* Analyse de séries temporelles
* Expérimentations orientée-hypothéses

### Acquisition des données

La donnée est soit structurée dans un entrepôt de données (schema-on-load), soit non-structurée généralement dans un data-lake (schema-on-read), soit semi-structurée (une clé permettant d'y accéder)

### Data Lake

Une collection de conteneurs de données long terme qui capturent, affinent et explorent toutes formes de données brutes, supportés par des technologies à faible coût, sur lesquels des applications aval peuvent se reposer.

Technologies: Hadoop, S3, Cassandra, HBase

C'est pas un entrepôt unique, ni le seul système qui alimente l'entrepôt de données. Ce n'est non plus un lieu d'archivage de données, ni un tableau de bord ou un DataMart.

### JSON

Délai d'ajout de nouvelles données aux data lake est plus rapide avec des données JSON

### Préparation des données

Fonctions de transformation de voix en texte, fonctions d'analyse des logs Apache

### Stockage en graphes

Analyse de chemins (path analytics), pour analyser des données en graphes

## Intelligence Artificielle

Test de Turing

Resurgence des techniques d'IA: CPU + GPU

* Des avancées significatives dans les capacités matérielles
* Le volume de données apportées par Big Data + IoT
* Des avancées rapides dans la recherche et dans les applications qui utilisent des réseaux de neurones

Quelques usages:

* Reconnaissance de parole
* Planification et ordonnancement autonome
* Prévisions financières
* Detection des spams
* Planification logistique
* Robotique
* Traduction automatique
* Système de questions - réponses (ChatBot)
* Prévisions de ventes

### Machine Learning

* Apprentissage supervisé quand il existe une variable y dans les données connues, faire attention à la régression
* Apprentissage non-supervisé, on utilise K-means
* Analyse multi-genre: intérêt de combiner plusieurs sources de données et plusieurs types d'analyses

### Visualisation de données (Dataviz)

Les visualisations classiques ne suffisent plus: comportements (séquences chemins & motifs), nuage de mots, toile, etc..

## Exercice

Vous êtes une ESN spécialisé dans la Data.

Mercredi 10 Juillet de 18h à 21h

T0 = 17/06/19

3: un rôle par personne

Questions au plus tard 24/06/19, à alain.fajner@epita.net

Toutes les réponses : 31/06/19

25 minutes par présentation, devant une personne de l'IT et une personne métier

Structure:

1. Introduction/Contexte
2. Compréhension des besoins
3. Présentation de la solution proposée
4. Organisation proposée
	1. Approche projet / livrables
	2. Planning
	3. Equipe projet
5. Charge avec détail par phrase
6. Proposition de valeur
7. Références ESN dans domaine similaire