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

### Séquençage multiple

On effectue un alignement par paires puis on aligne ensuite les différents alignements entre eux. Il faut cependant faire attention à l'arbre guide.

## Cellule Eukaryote

Une cellule eukaryote a besoin de qqs heures tandis qu'une cellule prokaryote a en général besoin de qqs minutes.

Les cellules eukaryotes et prokaryotes possèdent tous deux des ribosomes (ARN ribosomiques), qui transforment des ARN messagers pour les transfomer en protéines.

Les eukaryotes ont des réticulum endoplasmique, auxquels s'accrochent des ribosomes, notamment le réticulum rugeux, qui ont des ribosomes injectant des protéines dans le réticulum, lui permettant de servir de poste pour les protéines.

Le golgi sert lui aussi à livrer des protéines dans la cellule lorsqu'elle en a besoin.

La cellule est encadrée par une membrane et possède un noyau en son sein. Les mitochondries à l'intérieur de la cellule produisent l'énergie de la cellule.

Enfin, la cellule eukaryote posséde du lysosome, qui recycle les protéines utilisées à l'aide d'un pH faible, et du peroxisome qui capture tous les élèments toxiques pour la cellule pour les rejeter.

Le nucleolus, contenu dans le noyau, contient l'ADN servant à coder les ARN ribosomiques.

## BLAST

Le développement de l'algo BLAST s'est fait en même temps que le développement de la Base de données Genbank, contenant des séquences avec des annotations et des données bibliographiques, ainsi que sa provenance.

[Blast Website](https://blast.ncbi.nlm.nih.gov/Blast.cgi)

[Eterna Game](https://eternagame.org/game/puzzle/6502927/)

## Métagénomique

A partir d'échantillon d'eau prélevée en pleine mer, on cherche sur BLAST les traces de ribosomes ARN 16S pour identifier efficacement les différentes espèces ou famille d'espèces présentes dans l'échantillon.

## Cellules du corps humain

Le foetus posséde à l'origine des cellules souches généralistes qui vont se spécialiser. Dans le corps humain, les cellules sont différenciées et ont chacun leur propre rôle.

On peut dédifférencier des cellules pour les transformer en cellule plus généraliste et ainsi les redifférencier.

En fonction de la phase du cycle cellulaire, l'ADN change de forme.

Dans le noyau, l'ADN est divisé en territoire chromosomiques.

## Mailing list

[Mailing list pour des offres en bio-informatique](www.sfbi.fr)

## Instituts de recherche médicale à Paris

* Institut Curie
* Institut Pasteur
* Institut du cerveau et de la moelle

## Rappels

La glycolyse est le processus qui transforme le glucose en pyruvate.

Le pyruvate est transformé en acetyl-coa, afin d'activer le cycle de Krebs, produisant du NADH et du FADH2, en suivant le principe de la TCA.

Les enzymes sont des protéines catalyseurs, servant à enclencher des réactions chimiques.

Les ribosomes, composés d'ARN ribosomiques et de protéines, sert à la traduction d'ARN messager en protéines.

Ces protéines, composés d'acides aminés, sont produites ou recyclées, à l'aide des lysosomes.

## Déformation génétique

Les gènes peuvent se chevaucher.

La consanguinité entraine plus d'alléles récessif et des maladies génétiques.

Comprendre l'origine des maladies ne permet pas de trouver nécessairement un traitement. La déformation se trouve dans toutes les cellules du corps et traiter l'ensemble des cellules devient très compliqué.)

Pour identifier l'emplacement de la maladie, il faut prendre un groupe malade et un groupe sain. En comparant tout le génome ou juste une partie du génome, si une différence de position se retrouve plus, on peut identifier une coréllation.

## Pathogène

**Agent pathogène :** facteur capable d'engendrer une lésion ou de causer une maladie (processus morbide) chez les animaux ou les plantes

* Bactéries
* Parasites
* Mycètes
* Virus
* Prions

### Bactérie

Une bactérie n'est pas toujours pathogène mais elle peut devenir pathogène, en se transformant au contact d'un ADN, en se transductant lorsqu'un virus bactériophage la dévore ou enfin en se conjuguant avec un plasmide.

### Virus

Les virus ne sont pas dans l'arbre du vivant. Son but est de se multiplier et de survivre. Les virus cherchent à s'accrocher à des récepteurs ou à des membranes cibles. Il va checher à encoder dans la cellule cible à s'auto-répliquer en répliquant des ARN messagers pour produire des protéines cibles. Un virus peut être sous de multiple forme : capsyde (enveloppe), membranes, etc...

1. Pénétrer dans l'organisme (plaie, etc...)
2. Pénétrer dans des cellules hôtes, en fonction des récepteurs
3. Pénétrer dans le cytoplasme si besoin
4. Pénétrer dans le noyau
5. Insérer son matériel génétique (ADN) dans le génome de la cellule

Les virus n'affectent pas que les cellules eukaryotes. Exemple : les phages, virus bactériophages

Les virus n'ont pas de processus de correction d'erreur et mutent très vite. Cela rend leur traitement complexe.

### Système immunitaire

Les cellules T et B sont remplis de réticulum endoplasmiques afin de maximiser la production d'acide cytotoxique.