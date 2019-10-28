Enjeux et risques du cloud computing
========================

Evaluation : étude de cas en groupe de 5, questions et recommandation

## Objectifs

* Survival kit
* Audit
* Veille
* Analyse critique
* Experiences
* Réseau technique

## Environnement projet

### Etudier le contexte

* Objectifs : savoir d'où ça vient et où ça va
* Financement : family money (< 500 000€, argent familial pour prouver un modèle)
* Modèle économique : modèle impacte l'infrastructure, notamment la manière de vendre (on premise - service)
* Marché
* Clients
* Mesures

### 4 indicateurs

* Vertical
* Maturité du projet
* Capacité d'investissement
* Structure de coût

## Environnement technique

### Contraintes techniques

* Atouts (ressources, données, algorithme, connaissances, métiers, contrats)
* Difficulté
* Pile technique (langage, type de technologie, framework)
* Infrastructure

Rester en veille sur la popularité des langages

### 4 indicateurs

* Ambition
* Maturité technique
* Environnement technique
* Points clefs à sécuriser

## Equipe

### Acteurs

* Périmètres et responsabilité
* Organisation et rôle
* Outils et services

### 4 indicateurs

* Personnes clefs
* Maturité équipe
* Staffing & manques
* Sensibilité & demandes

## Se positioner en tant qu'expert

Passe par la méthodologie et la rigueur

### Forces

* Les avantages compétitifs
* Les compétences
* Qu'est-ce qui est mature

### Faiblesses

* Où cela bloque
* Faille dans le modèle
* Qu'est-ce qui n'est pas couvert

### Opportunités

* Axes d'amélioration
* Gain possible connu ou pas
* Changement possible ?

### Menaces

* Est-ce que l'environnement est hostile ?
* Y'a t'il des risques ?
* Cadre complexe

### Cartographie

Voir slides

### To Do

4 points pour lequel le cloud computing est important :

* Sécurité
* Réseau
* Stockage
* Performance / compute

## Les limites pour définir les enjeux

## Pourquoi le cloud computing ?

### Un peu d'histoire

* Dimension technique : Possibilité d'effectuer un traitement hors de son infrastructure locale
* Dimension fonctionnelle : Exporter ses services / infrastructures ailleurs

La virtualisation est la révolution technologique ayant permis le cloud, en rationalisant et abstrayant les ressouces physiques vers un ordinateur central

Matériel -> Virtualisation -> Conteneurisation -> Applications

### Différents types de cloud

* Cloud public : générique, à l'usage, sans investissement, global; AWS, Google, Azure
* Cloud privé : spécifique, économique, sécurisé, personnalisable; Openstack, VMWare
* Cloud hybride : extensibilité, abstraction, indépendant, qualité / prix; Kubernetes, Terraform

### Usage du cloud computing

##### Positive

* Consommer de l'infrastructure comme un service
* Remplacer de l'investissement initial par des coûts d'exploitation
* Bénéficier d'économie d'échelles
* S'affranchir des problèmes de capacité
* Augmenter l'agilité et les vitesses de déploiement
* Exploiter l'infrastructure efficacement
* Adapter les ressources au besoin, adapter la puissance à l'usage, économiser avec des modèles à l'usage
* Déploier internationalement rapidement

##### Négative

* Confidentialité / Sécurité (RGPD)
* Inconvénients de la centralisation
* Vendor-Locking spécialement avec l'usage de services haut-niveau
* Maitrise du système informatique
* Accès à de hautes performances
* Dépendance à Internet ainsi qu'à tous les vecteurs de disponibilité externe
* Coût du cloud
* Cadre légale / Conditions de services / Pérennité

### Par continent

L'Afrique et l'Asie sont les futurs consommateurs du Cloud, avec des acteurs différents et des cas d'usage différents

### 6 concepts clés

* Disponibilité
* Dimensionnement (horizontale / verticale)
* Performance (réseaux, applicatifs, infrastructure sous-jacent)
* Service à état (privilégie les services sans état (stateless))
* Distribué
* As Code

### 6 concepts économiques

* CAPEX / OPEX
* ROI
* TCO (Coût total de possession), qui intégre matériel, logiciel, consommation, locaux, personnels, formation, ...
* Fixe / Usage
* Self-service
* Contrats

### 6 concepts techniques

* Conteneurs
* Asynchrone
* Tolérance aux pannes
* Cache (CDN, contenu fixe ou contenu dynamique)
* Base de données (relationnel ou non, clé, documents, déconnecté, data-warehouse)
* Sécurité

## Les services du Cloud

### Compute

* Concepts-clefs : Service de Base du Cloud Computing qyu execute une charge applicative dans un environnement virtualisé
* Risques : Vendor-locking, risque de ressources centralisés, perte de connaissance système, qualité variable
* Enjeux : Consommer des ressources à la demande accessible instantanément pour construire une infrastructure disponible et sécurisé
* Perspectives d'avenir : Consommation des ressources sans serveur (Server-Less) au temps d'execution

Tendance à aller vers le Serverless, pas encore de gros framework dans ce domaine mais il existe des Open FaaS.

Consommation stockage : nombre d'I/O à la seconde

Choix de la puissance de Compute nécessite une vraie connaissance et un véritable accompagnement, pour améliorer ses performances, il faut apprendre comment automatiser et optimiser. La doc Amazon est très complète à ce niveau là.

La tendance informatique va vers la consommation à la demande

### Storage

* Concepts-clefs : Service de base du Cloud Computing, qui stocke les données en objet ou en bloc, de manière centralisé ou directement
* Risques : Modèle économique, dépendance application, sécurité
* Enjeux : Disposé d'un espace de stockage illimité sauvegardé, distribué et accessible avec globalement de bonnes performances
* Perspective d'avenir : Site statique et distribution web amélioré par du traitement dynamique sur les Edges

Transforme les problématiques de stockage

Possibilité de stockage de petaoctets de données dans des bandes sans faire les investissements initiaux

Aujourd'hui, il est possible de passer des sites en statique ou pseudo-statique en optimisant et organisant bien les workflows et en effectuant des pré calculations des données

### Database

* Concepts-clefs : Déporter les logiciels de SGBD vers le cloud en bénéficiant des avancés de scaling et de traitement distribué
* Risques : Maitrise des coûts, comptabilité applicative et maintenances / debug
* Enjeux : Utiliser des bases de données adapté aux traitements, volumétrie, contraintes, avec des outils performants
* Perspective d'avenir : Data Lake sur des peta octets de données, requetable hors ligne "non relationnel global", relationnel auto-scalable

### Network

* Concepts-clefs : Connectivité interne / externe, CDN, VPC, Région
* Risques : Domaine qui nécessite une réel expertise mais de plus en plus abstrait  : métrique qui est le plus sur-facturé et qui rapporte aux CSP
* Enjeux : Point stratégique pour lequel les investissements sont forts qui garantisse connectivité, performance et disponibilité de l'accés aux services et données
* Perspective d'avenir : Network as Code, VNF

Le tarif est à la taille de tuyau, on paye rarement le traffic entrant mais bcp le traffic sortant

### Security

* Concepts-clefs : Transposition des techniques de défense dans un périmètre cloud grace à un ensemble de produits / services pour se protéger des malveillances
* Risques : Transformation en commodité alors que c'est un risque qui touche tous les métiers
* Enjeux : Trouver le bon niveau, ne pas faire confiance aveugle dans les configurations, tester, auditer, vérifier
* Perspectives d'avenir :  Utilisation du machine learning et d'outils de recommandation automatique, implication de plus en plus tôt dans les développements (dev-sec-ops)

### Cost management

* Concepts-clefs : aider les consommateurs cloud à effectuer leur transition
* Enjeux : former le directeur financier et l'informer que le coût passe d'un coût d'investissement puis régulier à un coût variable et à la consommation
* Risques : acceptation du changement, de la nouvelle forme de coût
* Perspective d'avenir : les acteurs cloud se tâtent à changer leur méthode de coût pour éviter de tuer des licornes

### IA - Machine Learning

* Concepts-clefs : Mise à disposition de puissance de calculs amélioré par des puces spécifiques pour l'usage d'apprentissage profond ou de services à plus forte valeur ajouté d'IA
* Enjeux : Savoir traiter et tirer des modèles automatiques pour tirer un avantage compétitif dans son métier depuis les données
* Risques : Données privées, Ethiques, Changement social
* Perspectives d'avenir : Généralisation, SaaS spécifique, Intelligence Générale

### Autres

* Migration : des outils qui facilite la migration
* Marketplace : consommation des logiciels as Service (licence à l'usage), capitalisation et partage d'outils
* Metrologie : Centralisation de journaux, système de métrologie et de monitoring, consolidation et traçabilité
* Developer tools