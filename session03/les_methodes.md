# Session 4 - Les méthodes

Ruby permet de lancer des fonctions sur des paramètres, mais dispose également d'une notation liée à ce que l'on appelle la "programmation orientée objet" (POO), que nous verrons un peu plus tard, et qui permet de lancer des fonctions sur des paramètres de manière "plus lisible".

Ces fonctions sont de plus "pré-programmées" dans Ruby, et permettent de faire beaucoup de choses utiles très facilement.

La notation de ces fonctions est :

```ruby
parametre.fonction(parametre_auxiliaire)
```

Lorsque l'on voit cette notation, on parlera de **méthode** (pour des raisons que nous verrons plus tard avec la POO).

La plupart de ces méthodes on un nom lié à la traduction anglaise de l'action réalisée.

Quelques exemples :

```ruby
puts "test".upcase # affiche "TEST"
puts "TEST".downcase # affiche "test"
puts "test".reverse # affiche "tset"
puts [1,2,3].first # affiche 1
puts [1,2,3].last # affiche 3
puts [1,2,3].join("-") # affiche "1-2-3"
puts "Une phrase, avec une virgule".split(",") # affiche "Une phrase" puis " avec une virgule"
```

De plus, certaines de ces méthodes permetent de faire des conversions entre types de caractères. On utilise pour cela la notation :

```ruby
parametre.to_X
```

en remplaçant `X` par la première lettre du type ciblé.

Par exemple :

```
puts 3.to_f # affiche 3.0 (Integer vers Float)
puts 3.0.to_i # affiche 3 (Float vers Integer)
puts "3.0".to_f # affiche 3.0 (String vers Float)
```

Enfin, les méthodes peuvent être chaînées, c'est-à-dire que l'on peut écrire :

```ruby
parametre.methode1.methode2
```

Exemple :

```ruby
puts ["1", "2", "3"].join("").to_i # affiche 123
```

[Retour à la table des matières](../../../)