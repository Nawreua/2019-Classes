Cloud computing
============

## Cloud ?

* Definition - Key features - Types - Examples
* Technologies ?

## Benefits ?

* User view ? Business perspective ? From IT perpective ?

## Definition

Cloud computing is a delivery model for technology-enabled services that provides **on-demand** access via a **network** to an **elastic** pool of **shared** computing assets that can be rapidly _provisioned and released with minimal service provider interaction_.

## Cloud key features

* On-demand
* Network access
* Pay-per-user
* Elastic
* Shared
* Scalable

## C-offers : Three Pillars

* Saas
* Paas
* Iaas

It's all about Granularity and Packaging

## Three types of cloud

* Public : Applications non sensitive, low costs
* Private : Strategic Applications
* Hybrid : Combination Public/Private

![Cloud_computing](file://media/387423046.png)

> *On-demand self-service*. A consumer can unilaterally provision computing capabilities, such as server time and network storage, as needed automatically without requiring human interaction with each service provider.

> *Broad network access*. Capabilities are available over the network and accessed through standard mechanisms that promote use by heterogeneous thin or thick client platforms (e.g., mobile phones, tablets, laptops, and workstations).

> *Resource pooling*. The provider's computing resources are pooled to serve multiple consumers using a multi-tenant model, with different physical and virtual resources dynamically assigned and reassigned according to consumer demand. 

> *Rapid elasticity*. Capabilities can be elastically provisioned and released, in some cases automatically, to scale rapidly outward and inward commensurate with demand. To the consumer, the capabilities available for provisioning often appear unlimited and can be appropriated in any quantity at any time.

> *Measured service*. Cloud systems automatically control and optimize resource use by leveraging a metering capability at some level of abstraction appropriate to the type of service (e.g., storage, processing, bandwidth, and active user accounts). Resource usage can be monitored, controlled, and reported, providing transparency for both the provider and consumer of the utilized service.

— National Institute of Standards and Technology

## Interview Avec Chewie

### 1

1. Tech: Cloud démocratisation de la virtualisatio, , capactié à outsourcer les besoins pour deploy, permet de se passer des besoins du "bas", exemple deploy une application, consommer sans installer. Enabler pour pratiques impossibles avant, introduction du devops, extension de l'infra agile, Manifeste agile 2001, 1993 début idée, 2012, début devops => infra dans la loop, Cloud enabler agilité dans l'infrastructure
2. Business: pyramide éclaté, capacité relation commercial à chaque niveau, Saas -> Paas -> Iaas -> data center, impact sécurité: modéle français: SS2I, louage de talents, Amazon: **shared responsiblity model** , Iaas : Amazon WS, Azure, Google (un peu) quasiment à cause du SLA mais sur les couches plus, concurrences possibles

### 2

Ajd, découpa un peu plus flou, (Iaas+): Iaas au début, virtu machines + réseau, Iaas+: Iaas + Saas, DBaas techniquement Paas mais ajd Iaas+

### 3

Iaas, Paas, Saas, Iaas+

### 4

Acteurs Iaas: AWS, + grosse part de marché en terme de Iaas, concurrence plus au niveau offre commerciale, Azure pas ouf, OpenStack *opensource*, produit ou service, généralement pas conseillé en produit, ou revendu en service, mais pas fonctionné surtout en France avec échec cloud souverain, acteurs français Iaas: OVH et Scaleware, in-house, interne Openstack mais Iaas figé de manière générale

KAM: Key Account Manager, mec de la boîte chez le client

Paas: Au début détection language et différenciation sau niveau offre language mais docker a changé la donne, Paas => Caas (container), DockerSwarm, Mezos et Kubernetes en cluster et orchestrateur de container, cristalisé en termes de produits, surtout Kube, Kaas maintenant en Paas

Saas: variation

offres figés maintenant

### 5

Cloud computing: compute network storage

Cloud smartphone: storage

### 6

On premise, ce n'est plus à moi de le gérer, avis perso: ne pas devenir le bac à sable d'AWS

Mais AWS est une solution facile pour gérer le problème en tant que consultant

Data center aura sa place pour des raisons légales, exemple: données médicales ou des grosses puissances de calculs

Y rester parce que acheter: NON

Ou mixer en cas de pics de calculs: solution hybride, latence la plus faible requise

Hybridation: gros endgame cloud

### 7

Avantages: Rentabilité, Sécurité

Incovénients: Données sensibles, Vendor locking (Infrastructure as code), Exemple: Heroku

Capital expensise: prix ponctuelle: Capex

Operational expensies: prix continue: Opex

### 8

RGPD, mais responsabilité client pas fournisseur

PCI-DSS, réglementation carte bleue, stockage carte bleue, offre Saas permettant de répondre à ce problème

Contrat entre end-user et boîte

### 9

Shared responsability model, risque de leaks de credentials: Faille n°1 mais faille client, plus confiance à AWS pour la sécurité, le cloud a gagné, suffisament sécurisé, recommendation: chiffrer les données stockées

### 10

1. Coder n'est pas le même, changement de design, **12 factors**: heroku, à chercher !!!, best practice devops, Architecture: n services répliqués, à tout moment, mort et renaissance ailleurs, Service: Cloud Ready App, accompagnement du changement cloud
2. Evolution techno pour finalité de changement organisationnelle, but du cloud: Changer son organisation, déployement, communication entre service, demande + grande autonomie entre les services, demande un individu spécialisé et nécessite compétence ops
3. Avoir des compétences devops, **Terraform**, produit d'automisation Iaas, devisation de l'infrastructure, versionner, même standard que sur le dev, **Ansible**, automatisation de VM

### Exemple du CRI

Raison de non-changement, raison pédagogique: les gens doivent apprendre à gérer de l'infrastructure

## Sources

[Cloud Computing : Nouveaux modèles, *Syntec numérique*](https://syntec-numerique.fr/sites/default/files/Documents/20120328-Infra-livreblanc-cloud-computing-nouveaux-modeles.pdf)

[Best Practice In The Cloud An Introduction, *ITIL*](https://www.axelos.com/case-studies-and-white-papers/best-practice-in-the-cloud-white-paper)

[White Paper Octo, Culture Devops Vol.01](https://www.octo.com/fr/publications/30-culture-devops-vol-01)

[The Twelve-Factor App](https://12factor.net/)
