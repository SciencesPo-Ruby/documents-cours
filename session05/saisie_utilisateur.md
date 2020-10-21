# Demander une saisie utilisateur

Pour rendre nos programmes interactifs, nous allons pouvoir demander à l'utilisateur de saisir des données.

En l'absence d'interface web, cela passe par le mot-clé gets.

```ruby
puts "Saisir votre prénom :"

prenom = gets # va demander à l'utilisateur de faire une saisie, et en stocker le résultat dans prenom

puts "Bonjour " + prenom + " !"
```

Petit problème : en l'état, si l'utilisateur tape par erreur des espaces en trop avant ou à la fin de son prénom, ces espaces seront pris en compte.

Nous allons donc utiliser une méthode nommée strip﻿ qui permet, pour une String, d'en retirer les espaces en trop situés au début et à la fin.

```ruby
puts "Saisir votre prénom :"

prenom = gets.strip # demande une saisie utilisateur, retire les espaces en trop, et stocke le tout dans prenom

puts "Bonjour " + prenom + " !"
```

On utilisera ainsi gets.strip pour la saisie, dans la mesure du possible.

[Retour à la table des matières](../../../)
