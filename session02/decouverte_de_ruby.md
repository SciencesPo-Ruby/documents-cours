# Session 2 - Découverte de Ruby

## A propos de Ruby

Ruby est un langage de programmation créé en 1995 par Yukihiro Matsumoto, qui repose sur de grands principes de simplicité permettant de concevoir rapidement et en peu de code des logiciels complets.

Ruby est un langage idéal pour débuter en programmation informatique :
- il est peu "verbeux", c'est-à-dire qu'il faut en général rédiger peu de code pour effectuer une opération donnée ;
- il dispose d'une courbe d'apprentissage "plate", c'est-à-dire qu'il faut peu de temps pour en assimiler les bases ;
- il repose sur une syntaxe "simple" et "haut-niveau", c'est-à-dire qu'un humain ayant des bases en programmation informatique mais aucune connaissance préalable en Ruby pourra assez facilement deviner le comportement d'un programme rédigé en Ruby dès la première lecture ;
- la communauté mondiale utilisant Ruby a créé de nombreuses "bibliothèques", appelées "gems", pour l'essentiel des besoins d'un programmeur, c'est-à-dire qu'il existe des solutions clé-en-main pour presque tous les problèmes qui peuvent se poser à un développeur débutant.

Pour illustrer ces idées, on dit que Ruby est un langage "transparent" : la syntaxe, c'est-à-dire la manière d'écrire le programme, permet de facilement comprendre ce que celui-ci réalise, et facilite la rédaction de programmes "élégants" même pour des débutants.

Cependant, Ruby comporte aussi des inconvénients :
- étant un langage haut-niveau, il est moins performant que des langages comme C / C++ ;
- Ruby est un langage récent et peu enseigné dans les écoles d'informatique, contrairement à d'autres langages comme C++ / PHP.

## Quelques exemples d'utilisation de Ruby dans un environnement professionnel

Ruby est particulièrement utilisé dans le milieu de la sécurité informatique en raison du [cadriciel](https://fr.wikipedia.org/wiki/Framework) [Metasploit](https://www.metasploit.com/).

Ruby est aussi utilisé dans la construction de sites Internet, avec 9gag, Airbnb, Hulu, Bloomberg, Github, Kickstarter, Crunchbase, Groupon, Basecamp, JobTeaser, Cyberwatch...

## De la notion de "type de données"

L'informatique repose sur le traitement de l'information (d'où le nom de "système d'informations" pour décrire l'ensemble des ressources informatiques d'une entreprise).

Or, pour traiter une information, il faut en connaître la nature : s'agit-il d'une chaîne de caractères ? d'un nombre entier ? d'un nombre flottant (décimal) ?

Si on ne connaît pas la nature d'une information, on devient vite perdu, et la machine aussi.

Pour illustrer cela, on peut penser à la situation suivante : si l'on demande à quelqu'un de trier des livres sans aucune information supplémentaire, cela donnera des résultats très variables. Le tri peut en effet être réalisé par taille, par ordre alphabétique croissant des titres, par ordre alphabétique croissant des noms de famille des auteurs, par genre, etc. 

De la même manière, un ordinateur n'aura un comportement prédictible que si l'on définit exactement les ordres attendus et le type de données que l'ordinateur manipule.

Pour illustrer cela en informatique, par défaut, diviser un nombre entier par un autre nombre entier donnera un nombre entier, tandis que diviser un nombre décimal par un autre nombre décimal donnera un nombre décimal.

Ainsi, la même opération de division aura un résultat différent entre **10 divisé par 3** (3) et **10.0 divisé par 3.0** (3.333333333333333).

La nature d'une information, d'une donnée informatique, est appelée "type". Chaque type dispose alors d'opérations de base, permettant d'effectuer des opérations classiques : addition / soustraction / multiplication / division de nombres entiers, concaténation de chaînes de caractères, etc.

Cette notion est donc très importante pour la suite du cours : en effet, si on peut réaliser des opérations basiques sur deux données du même type, cela n'est pas possible sur deux données de type différent.
Autrement dit, si on peut ajouter 2 pommes avec 2 pommes (cela fait 4 pommes), on ne peut pas ajouter 2 pommes avec 2 oranges. Et c'est ici la même idée avec les Integer, les Float, les String que nous allons étudier.

[Retour à la table des matières](../../../)
