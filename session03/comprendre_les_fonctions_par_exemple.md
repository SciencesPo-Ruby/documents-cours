# Session 3 - Comprendre les fonctions par l'exemple

Pour chaque exercice ci-après :
- créer un REPL.it Ruby en cliquant sur [https://repl.it/languages/ruby](https://repl.it/languages/ruby)
- copier / coller le code fourni dans l'exercice
- résoudre l'exercice

Ces exercices doivent être réalisés durant la session hebdomadaire : profitez-en pour poser vos questions si vous bloquez !

## Exercice 1 : l'addition

```ruby
# Compléter le code pour que addition(nombre1, nombre2) affiche la somme de nombre1 et nombre2
def addition(nombre1, nombre2)
    puts VOTRE_REPONSE
end
addition(1, 2) # doit afficher 3
addition(5, 10) # doit afficher 15
```

## Exercice 2 : le carré

```ruby
# Compléter le code pour que carre(nombre) affiche le carré de nombre (c'est-à-dire nombre multiplié par lui-même)
def carre(nombre)
    puts VOTRE_REPONSE
end
carre(5) # doit afficher 25
carre(10) # doit afficher 100
```

## Exercice 3 : le périmètre d'un cercle

```ruby
# Compléter le code ci-après pour que perimetre(rayon) affiche le périmètre d'un cercle ayant pour rayon le paramètre saisi (la formule étant Périmètre = 2 * Pi * Rayon)

# Cette variable contient plusieurs éléments, dont un sera utile pour l'exercice
nombres_utiles = { "pi" => 3.14159, "phi" => 1.618, "e" => 2.718 }

def perimetre(rayon)
    puts 2*VOTRE_REPONSE_1*VOTRE_REPONSE_2
end
perimetre(50) # doit afficher 314.159
perimetre(150) # doit afficher 942.477
```

## Exercice 4 : périmètre moins précis

Je souhaite arrondir la valeur de Pi à `3`. Modifier le code de l'exercice 3 en conséquence. Mettre finalement une valeur plus précise comme `3.14159265359`. Modifier le code et observer les résultats.

[Retour à la table des matières](../../../)