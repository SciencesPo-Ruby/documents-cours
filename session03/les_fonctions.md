# Session 3 - Les fonctions

## Concept des fonctions

Statistiquement, la création d'un programme informatique vise surtout à automatiser des tâches répétitives.

Un exemple simple pourrait être la création d'un programme destiné à envoyer un message à trois nouveaux élèves de Sciences Po : Emile, Richard, et Frédéric.

Le code pourrait être le suivant :

```ruby
puts "Bonjour Emile, bienvenue à Sciences Po !"
puts "Bonjour Richard, bienvenue à Sciences Po !"
puts "Bonjour Frédéric, bienvenue à Sciences Po !"
```

Supposons maintenant que la direction de la communication souhaite un jour changer le message d'accueil, et le remplacer par `bienvenue à l'IEP de Paris !`. L'équipe informatique devrait alors modifier 3 fois le texte saisi : une fois pour Emile, une fois pour Richard, et une fois pour Frédéric. Or l'informatique vise à éviter toute action répétitive. Il y a donc plus simple.

Pour cela, nous allons créer une fonction, c'est-à-dire une sorte de procédure ou de routine.

Une fonction démarre par le mot-clé `def` et se finit par le mot-clé `end`. La syntaxe est la suivante :

```ruby
def nom_fonction(nom_param1, nom_param2,...)

    # corps fonction

end
```

Une fonction peut lire 0, 1, ou plusieurs paramètres.

```ruby
def fonction_sans_parametre
    # corps fonction
end

def fonction_un_seul_parametre(nom_parametre)
    # corps fonction
end

def fonction_plusieurs_parametres(nom_param1, nom_param2, nom_param3)
    # corps fonction
end
```

Les paramètres d'une fonction permettent d'influencer les actions réalisées dans le corps de celle-ci. Pour simplifier, nous pouvons imaginer une fonction comme une usine de production automobile pouvant produire des véhicules Peugeot et Renault, de couleur bleue ou noire. L'utilisateur disposerait alors d'un panneau de contrôle, avec un levier "marque" pour choisir Peugeot ou Renault, et un levier "couleur" pour choisir "bleue" ou "noire".

Dans ce cas, cette usine représente une fonction `produire_vehicule` qui prend 2 paramètres : `marque` et `couleur`, et qui pourrait ressembler à cela :

```ruby
def produire_vehicule(marque_param, couleur_param)
    puts "Véhicule produit de la marque " + marque_param + " et de couleur " + couleur_param +"."
end

produire_vehicule("peugeot", "bleue") # Affiche : Véhicule produit de la marque peugeot et de couleur bleue.
produire_vehicule("peugeot", "noire") # Affiche : Véhicule produit de la marque peugeot et de couleur noire.
produire_vehicule("renault", "bleue") # Affiche : Véhicule produit de la marque renault et de couleur bleue.
produire_vehicule("renault", "noire") # Affiche : Véhicule produit de la marque renault et de couleur noire.
```

Si l'on reprend le code saisi plus haut sur l'accueil d'étudiants, nous pouvons écrire sous forme de fonction :

```ruby
def accueillir_etudiant(prenom_param)
    puts "Bonjour " + prenom_param + ", bienvenue à Sciences Po !"
end
accueillir_etudiant("Emile") # Affiche : Bonjour Emile, bienvenue à Sciences Po !
accueillir_etudiant("Richard") # Affiche : Bonjour Richard, bienvenue à Sciences Po !
accueillir_etudiant("Frédéric") # Affiche : Bonjour Frédéric, bienvenue à Sciences Po !
```

Et dans le cas où la direction de la communication souhaiterait changer de message, une seule modification suffit pour impacter l'ensemble du projet :

```ruby
def accueillir_etudiant(prenom_param)
    # Remplacement de Sciences Po par IEP de Paris dans le texte
    puts "Bonjour " + prenom_param + ", bienvenue à l'IEP de Paris !"
end
accueillir_etudiant("Emile") # Affiche : Bonjour Emile, bienvenue à l'IEP de Paris !
accueillir_etudiant("Richard") # Affiche : Bonjour Richard, bienvenue à l'IEP de Paris !
accueillir_etudiant("Frédéric") # Affiche : Bonjour Frédéric, bienvenue à l'IEP de Paris !
```

## Comment bien créer ses fonctions ?

Pour bien rédiger une fonction dans un programme, il faut réussir à comprendre toutes les actions "communes" du programme et identifier les éléments "variables".

Dans le cas de l'accueil des étudiants montré plus haut, l'action commune est l'affichage d'un texte contenu un prénom, au format `Bonjour PRENOM, bienvenue à l'IEP de Paris`.

Les actions "communes" de la fonction doivent alors constituer le corps de celle-ci, tandis que les éléments "variables" seront passés comme paramètres.

[Retour à la table des matières](../../../)