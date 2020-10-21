# Le mot-clé Return

Imaginons que l'on a les deux fonctions suivantes :

```ruby
def ajouter(a, b)
    puts a+b
end

def fois_deux(n)
    puts 2*n
end
```

Ces deux fonctions permettent de lancer les commandes suivantes :

```ruby
ajouter(2, 3) # affiche : 5
fois_deux(5) # affiche : 10
```

Or, en informatique, il est souvent utile d'enchaîner des fonctions, par exemple on aimerait pouvoir écrire :

```ruby
fois_deux(ajouter(2, 3))
```

En l'état de nos connaissances, ce n'est pas possible : l'exécution de ce code produit une erreur "nil can't be coerced into Integer'.

En effet, ici, "ajouter(2, 3)" affiche 5 à l'écran, mais ne donne aucun résultat : on dit que c'est une valeur vide, aussi dite "nil" ou "null".

```ruby
resultat = ajouter(2, 3)
puts "Résultat vaut :"
puts resultat # n'affiche rien
```


Pour pouvoir "passer" le résultat produit par une fonction et le stocker ou le réutiliser, on doit utiliser le mot-clé "return".

```ruby
def ajouter(a, b)
    return a+b
end

def fois_deux(n)
    return 2*n
end
```

Si l'on écrit le code de la sorte, l'exécution suivante n'affichera rien :

```ruby
ajouter(2, 3) # n'affiche rien
fois_deux(5) # n'affiche rien
```

En revanche, on peut maintenant enchaîner les fonctions ou même stocker leur résultat :

```ruby
fois_deux(ajouter(2, 3)) # n'affiche rien, mais ne produit pas d'erreur
```

```ruby
resultat = ajouter(2, 3)
puts "Résultat vaut :"
puts resultat # affiche 5 
```

On peut même enchaîner les fonctions, et demander à afficher la valeur produite par cet enchaînement, en utilisant "puts" sur le résultat de la fonction :

```ruby
fois_deux(ajouter(2, 3)) # n'affiche rien
puts fois_deux(ajouter(2, 3)) # affiche 10 (notez la présence du puts)
```

Pour résumer : le mot-clé puts sert à afficher un élément à l'écran, mais ne permet pas de ré-exploiter cet élément.

Pour ré-exploiter des valeurs issues d'une fonction, on utilisera plutôt le mot-clé return.

A partir de maintenant, nous ferons surtout des fonctions dont la fin se terminera par "return", et appellerons puts sur le résultat de la fonction.

```ruby

# Pas recommandé :
def fonction(p1, p2)
    # ... actions ...
    puts res
end
fonction(1, 2)

# Recommandé :
def fonction(p1, p2)
    # ... actions ...
    return res # pas recommandé
end
puts fonction(1, 2)
```

[Retour à la table des matières](../../../)
