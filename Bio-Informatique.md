Bio-Informatique
========================

Métiers de la bioinformatique :

1. Analyse de données (Aide au diagnostique, ML, Stockage, Big Data)
2. Traitement de données
3. Modélisation
4. Développement logiciel
5. Gestion de projet

En biologie, on étudie des objets de l'ordre du micro et nanomètre

## Energie et liaison du vivant

Le vivant est basé sur des biomolécules

Comme tout objet, le vivant est soumis aux règles physiques. C'est un moteur du développement et de la complexification des organismes.

Energie cinétique -> energie du mouvement

Energie potentielle -> energie stockée

Liaison covalente : partage d'électron (intramoléculaire)

Liaison électrostatique entre atomes de charges opposées

Liaison hydrogène H de l'eau + autre atome

## Thermodynamique

Les lois régissant la faisabilité des réactions chimiques

1. Conservation de l'énergie, Un système fermé ne peut pas créer ou détruire de l'énergie
2. Accroissement du désordre, Augmentation de l'entropie

Réaction chimique : réactifs <=> produits

Changement d'enthalpie : $\delta$G = G_produits - G_réactifs

Réaction endothermique : consomme de l'énergie

Réaction exothermique : libére de l'énergie

Si $\delta$G < 0, réactifs -> produits, endothermique

Si $\delta$G > 0, réactifs <- produits, exothermique

## Les bases du vivant

### ADN

ADN : Acide DesoxyriboNucléique

L'ADN ne crée pas les proteines directement, elle passe par l'ARN via la transcription avant d'effectuer la traduction pour générer les proteines

Alphabet ADN = {A, T, G, C}

* A : Adenine
* G : Guanine
* T : Thymine
* C : Cytosine

La molécule d'ADN n'est pas symétrique, la polymerisation s'effectue uniquement dans un sens, en fonction des carbones 5' (phosphate) et 3' (hydroxyl)

Les bases ADN sont complémentaires 2 à 2 : Adenine <-> Thymine et Cytosine <-> Guanine

### ARN

ARN : Acide RiboNucléique

4 majeures fonctions de l'ARN :

1. mRNA
2. rRNA
3. tRNA
4. tmRNA

Structure de l'ARN est non plate et multiple. Il existe des algorithmes pour déduire la forme d'une ARN

### Transcription

Changement de base simple en informatique

En biologie, plus complexe

### Acide aminé et proteine

Toujours composé d'un groupe amine et d'un groupe carboxyle et d'un side chaine qui détermine son type d'acide aminé

Trois type d'acide : 

1. Hydrophobe
2. Hydrophile
3. Chargé

Plus petit acide aminé : Glycine

Une protéine est un structure composé d'acides aminés, regroupé en hélice alpha, en feuillet bêta, combiné en structure tertiaire puis en association de protéines

Les proteines effectuent des réactions lors des changements de conformation

### Cellule

Paroi cellulaire : bicouche lipidique, sépare milieu intérieur (cytoplasme) et milieu extérieur

Membrane fluide : autorise le déplacement latéral de proteines

Imperméable aux larges molécules

Le passage peut être autorisé à l'aide de canaux spécifiques liés à des protéines spécialisées : aquaporine, canal ionique

Les transporteurs actifs permettent de transporter des molécules contre le gradient

Les cellules eukaryotes possédent des organelles (sous-compartiment) tel que le noyau ou la mitochondria, maintenue par les filaments le long de la cellule

## Température et énergie

**Loi des gaz parfaits**: _PV_ = _nRT_

Donc _T_ $\arrow_up$ => _P_ $\arrow_up$

## Rappel cours 1

Protéine : polypetide, séquence d'acide aminés

ADN -> ARN pré-mature : transcription

ARN pré-mature -> ARN mature : epissage

ARN mature -> Protéine : traduction

ARN mature : Codon start -> Coding Sequence -> Codon stop

### Modification allostérique

On change la forme de la protéine afin d'être active ou inactive

### Cycle de la respiration cellulaire

La glycolyse permet la respiration cellulaire, via le cycle TCA (Krebs cycle)

## Séquençage de l'ADN

Séquençage : lire les séquences ADN d'une cellule

Séquençage de Sanger : 1977, 1ère méthode

1. On extrait puis amplifie un fragment d'ADN après avoir stopper la polymérisation
2. On etiquete chaque sous-séquence
3. On reconstruit la séquence

A partir des années 2000, on a réussi à déduire l'ensemble du génome humain. Seul 2% du génome humain sont des séquences codantes.

### Contraintes sur les séquences protéiques

**Domain protéique :** un fragment auto-stabilisé est indentifé par un motif charactéristique et une fonction précise

**Séquences homologues :** séquences possédant une origine évolutionnaire commune

But : 
1. Evaluer si deux séquences sont homologues
2. Trouver les zones à conserver via l'alignement de séquences

#### Distance de Hamming

x = x1 ... x|x|, y = y1 ... y|y| deux séquences de taille m

1a, b = {1 si a != b, 0 sinon}

### Mutation de l'ADN

* Substitution
* Glissement de brin
	* Insertion
	* Suppression

#### Distance de Levensthein

Permet de gérer les chaînes de taille différentes

##### Amélioration via la programmation dynamique

Découper le problème en sous-problème redondants.

On passe par une matrice pour la distance de Levensthein.