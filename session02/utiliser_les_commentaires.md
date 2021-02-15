# Session 3 - Utiliser les commentaires

Avec l'arrivée des variables, nous allons rapidement écrire du code un peu plus complexe. Progressivement, il sera plus difficile de nous relire et de comprendre ce que nous avions tapé.

Pour faciliter la relecture, nous utiliserons un type de données appelé "commentaires".

Les commentaires ont la particularité de ne pas être "lus" ou "interprétés" par l'ordinateur : leur seule utilité est d'aider l'humain à se relire.

Un commentaire est indiqué à l'aide du symbole `#` suivi du contenu du commentaire.

Reprenons le code précédent avec le compteur :

```ruby
compteur = 1
compteur = compteur + 1
compteur = compteur + 1
compteur = compteur + 1
puts compteur
```

Si l'on ajoute des commentaires afin d'en faciliter la lisibilité, nous pourrions écrire le code suivant :

```ruby
compteur = 1 # compteur vaut 1
compteur = compteur + 1 # compteur vaut 2
compteur = compteur + 1 # compteur vaut 3
compteur = compteur + 1 # compteur vaut 4
puts compteur # affiche 4
```

Les commentaires sont donc très utiles d'une part pour des débutants, mais aussi pour travailler en équipe et faciliter la relecture mutuelle du code.

[Retour à la table des matières](../../../)