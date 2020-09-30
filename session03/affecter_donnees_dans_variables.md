# Session 3 - Affecter des données dans des variables

Dans les 2 sessions précédentes, chaque opération saisie en Ruby n'était qu'à usage unique.

Ainsi, si l'on souhaitait calculer l'union de deux tableaux, puis calculer l'intersection de ce résultat avec un troisième tableau, nous aurions été limité au code suivant :

```ruby
puts "Union de deux tableaux [1, 2, 3] et [3, 4, 5]"
puts [1, 2, 3] | [3, 4, 5]
puts "Reprise du résultat et calcul de l'intersection avec [1, 5]"
puts ([1, 2, 3] | [3, 4, 5]) & [1, 5]
```

Cela n'est pas pratique, surtout si les opérations à réutiliser sont longues à calculer (par exemple lorsque l'on cherche à obtenir un valeur très précise du nombre Pi).

Ruby fournit en conséquence un système qui permet de stocker des valeurs dans la mémoire de l'ordinateur, via ce que l'on appelle des "variables".

Les variables sont comme les tiroirs d'un meuble, où l'on peut stocker des données et lire des données, avec en plus la possibilité de mettre une étiquette sur ces tiroirs de sorte à savoir immédiatement ce qu'ils contiennent.

Pour stocker des données dans une variable, nous utiliserons la syntaxe `nom_variable = VALEUR`. Il faut alors lire que Ruby stockera dans la variable `nom_variable` le contenu `VALEUR`.

Par convention, pour le reste du cours, nous utiliserons des noms de variables écrits en lettres minuscules, en évitant tout accent, et en remplaçant les tirets ou espaces par des `_` (convention [Snake case](https://fr.wikipedia.org/wiki/Snake_case)).

L'action de **stocker des données dans une variable** s'appelle une **"affectation de données"**.

Quelques exemples d'affectations :

```ruby
entier = 1
flottant = 2.3
chaine = "Sciences Po"
tableau = [1, 2, 3]
dict = {"cle" => 99}
```

Une fois qu'une **variable reçoit des données**, on dit qu'elle est **"définie"**. Nous pouvons à tout moment accéder à son contenu en tapant simplement le nom de cette variable. Par exemple, le code ci-après stocke 5 dans la variable `entier`, puis demande à afficher le contenu de `entier`. Ce code affichera donc "5" à l'écran.

```ruby
entier = 5
puts entier
```

Par ailleurs, une variable peut stocker le résultat d'opérations, par exemple pour refaire l'exercice sur l'union et l'intersection de deux tableaux, nous pourrions écrire le code ci-après :

```ruby
puts "Union de deux tableaux [1, 2, 3] et [3, 4, 5]"
union_tableaux = [1, 2, 3] | [3, 4, 5]
puts union_tableaux
puts "Reprise du résultat et calcul de l'intersection avec [1, 5]"
intersection = union_tableaux & [1, 5]
puts intersection
```

Enfin, une variable peut stocker le résultat d'opérations réalisées sur elle-même. Cela est particulièrement utile lorsque l'on veut faire un compteur, dont la valeur augmentera régulièrement de 1 : on dit alors que l'on "incrémente" la variable de 1. Par exemple, le code ci-après affichera 4 à l'écran.

```ruby
compteur = 1
compteur = compteur + 1
compteur = compteur + 1
compteur = compteur + 1
puts compteur
```

[Retour à la table des matières](../../../)