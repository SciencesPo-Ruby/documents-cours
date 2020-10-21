# Ranges

Les ranges sont des éléments itérables (on peut boucler dessus avec ".each") qui permettent de générer facilement une série de valeur, d'une valeur de départ à une valeur d'arrivée.

On les note : (depart..fin)

```ruby
(1..6).each do |i|
    puts i
end
# affiche 1, puis 2, etc jusqu'à 6
```

```ruby
(10..40).each do |i|
    puts i
end
# affiche 10, puis 11, etc jusqu'à 40
```

Cela fonctionne aussi avec les lettres :

```ruby
('a'..'z').each do |i|
    puts i
end
# affiche a, puis b, etc jusqu'à z
```

Une conversion est possible d'un range vers un tableau :

```ruby
range_en_array = ('a'..'z').to_a
array = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
puts range_en_array == array # affiche true
```

Les ranges sont pratiques pour créer facilement des boucles qui s'exécutent un nombre précis de fois.

[Retour à la table des matières](../../../)
