# Jeu du Juste Prix

Nous allons maintenant faire un jeu relativement simple : le jeu du Juste Prix.

Concrètement, les règles sont :
- l'ordinateur choisit un prix au hasard entre 1 et 1000 euros
- le joueur doit deviner le prix
- le joueur saisit un prix par tour
- l'ordinateur dit si c'est plus grand, ou plus petit, ou trouvé
- si c'est trouvé, c'est gagné
- si c'est trop grand ou trop petit, le joueur perd une vie
- le joueur démarre avec 5 vies

Pour gérer le choix du prix au hasard, nous utiliserons les éléments ci-après.

## Gérer le hasard

Afin de faire des projets basiques et ludiques, nous demanderons souvent à l'ordinateur de générer des éléments "au hasard".

Ruby dispose pour cela d'une fonction nommée rand et qui permet de tirer un nombre au hasard.

Cette section montre comment utiliser cette fonction.

Tirer un Float entre 0.0 et 1.0 :

```ruby
rand() # vaut un Float au hasard entre 0.0 et 1.0
```

Tirer un Float entre -5.0 et 5.0 :

```ruby
rand(-5.0..5.0) # vaut un Float au hasard entre -5.0 et 5.0
```

Tirer un Integer entre -10 et 10 :

```ruby
rand(-10..10) # vaut un Integer au hasard entre -10 et 10
```

## Création du jeu

Le jeu va avoir :
- des conditions initiales :
    - l'ordinateur tire un nombre entre 1 et 1000
    - le joueur a 5 vies
    - un booléen indiquant la victoire (mis par défaut à false)
- une boucle principale de jeu, qui s'exécute tant que le jeu n'est pas fini
- les conditions de fin du jeu sont :
    - soit le joueur a perdu (plus de vie)
    - soit le joueur a gagné
- un tour de jeu, exécuté dans la boucle principale :
    - le joueur choisit un nombre
    - l'ordinateur dit si c'est plus ou moins que le nombre tiré
    - si c'est gagné, l'ordinateur met à jour le booléen de victoire (passagee à true)
    - si c'est perdu, l'ordinateur retire une vie au joueur

A vous de jouer ! (en session de cours)


[Retour à la table des matières](../../../)
