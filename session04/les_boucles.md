# Session 4 - Les boucles

L'informatique visant à automatiser des actions, nous avons régulièrement besoin de répéter la même action sur une série d'éléments.

Cela peut consister par exemple à calculer les résultats académiques sur l'ensemble des étudiants, ou envoyer un email individuels à chaque étudiant, etc.

Dans ce cas, l'approche consiste généralement à :
- définir une fonction qui permettra de traiter l'opération de manière atomique (par exemple "calculer les résultats d'un étudiant") ;
- répéter autant de fois que nécessaire l'appel à la fonction atomique, sur l'ensemble des éléments à traiter (ici, l'ensemble des étudiants).

Pour réaliser ces "répétitions", on utilise ce que l'on appelle des "boucles".

En Ruby, nous aurons besoin de deux types de boucles :
- les boucles conditionnelles ;
- les boucles itératives.

## Les boucles conditionnelles

Une boucle conditionnelle repose sur un booléen : cette boucle se répète **TANT QUE** que le booléen utilisé vaut **true**.

Autrement dit, cela consiste à formuler la répétition de la manière suivante :

```
Tant que CONDITION EST VRAIE
    Action à répéter
Fin
```

En Ruby, on notera :

```ruby
while ( test_logique ) do
   # Actions à répéter tant que test_logique est à true
   # ...
end
```

Cela permet de réduire le code nécessaire pour réaliser une opération.

Par exemple, pour afficher tous les nombres de 1 à 10, on peut écrire :

```ruby
puts 1
puts 2
puts 3
puts 4
puts 5
puts 6
puts 7
puts 8
puts 9
puts 10
```

ou de manière plus efficace :

```ruby
i = 1 # on définit une variable i
while ( i <= 10 ) do # tant que la valeur de i est inférieure ou égale à 10...
  puts i # on affiche i
  i = i + 1 # on augmente la valeur de i de 1 : on dit que l'on "incrémente" i de 1
end
```

## Les boucles itératives

Une boucle itérative repose, contrairement boucles conditionnelles, sur un ensemble de données : une boucle itérative permet alors de "parcourir" cet ensemble de données, de son premier élément à son dernier élément.

Autrement dit, cela consiste à formuler la répétition de la manière suivante :

```
Pour chaque élément dans ENSEMBLE PARCOURU
    Action à répéter
Fin
```

```ruby
# Si ensemble_a_parcourir est l'ensemble de donneés sur lequel on souhaite boucler, on notera :
ensemble_a_parcourir.each do | element_lu |
    # Actions à réaliser sur l'élément lu
    # ...
end
```

Attention : la notation est particulièrement complexe pour des profils n'ayant jamais fait de programmation informatique !

Il faut lire le code ci-dessus de la manière suivante :

```
Pour chaque élément dans ensemble_a_parcourir
    Je lis un élément, que j'appelle element_lu
    J'exécute les actions sur element_lu
    Je passe à l'élément suivant
Fin
```

Exemple :

```ruby
# Le code suivant affiche 1, puis 2, puis 3, puis 4, puis 5
[1,2,3,4,5].each do | element_lu |
    puts element_lu
end
```

Etape par étape :

```
1. Considérer un Array contenant les entiers de 1 à 5 ;
2. Boucler sur chaque élément de cet Array ;
3. A chaque tour de boucle :
    - remplacer la variable entre "| ... |", ici "element_lu", par une valeur de l'Array ;
    - exécuter la commande puts element_lu ;
    - passer à la valeur suivante.
4. Lorsque tout l'Array a été parcouru, la boucle est finie.
```

[Retour à la table des matières](../../../)