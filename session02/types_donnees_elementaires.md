# Session 2 - Types de données élémentaires

Dans le cadre de ce cours, nous utiliserons régulièrement les types de données suivants, que nous appellerons "types de données élémentaires" :
- nombres entiers (Integer) ;
- nombres décimaux (Float) ;
- chaînes de caractères (String).

## Les nombres entiers - Integer

Les nombres entiers sont écrits avec les chiffres qui les composent.

Exemples : `2`, `3`, `4`, `5`, `42`, `100`.

Ils sont appelés **Integer** en Ruby.

Un Integer peut être utilisé avec les opérations mathématiques suivantes :
- addition notée `+`
- soustraction notée `-`
- multiplication notée `*`
- division notée `/`

On peut également demander à Ruby d'afficher un Integer avec la commande `puts` suivie de ce que l'on souhaite afficher.

Exemple :

```ruby
puts 100
```

Cette commande affichera 100 à l'écran.

On peut aussi demander à Ruby d'afficher le résultat d'une opération mathématique, avec la commande `puts` suivie de l'opération.

Exemple :

```ruby
puts 2+2
```

Cette commande affichera le résultat de l'opération 2+2 c'est-à-dire 4 à l'écran.

## Les nombres décimaux - Float

Les nombres flottants / décimaux sont écrits avec les chiffres qui les composent, et un point pour séparer la partie entière de la partie décimale.

Dans le cas où la partie décimale est nulle, il faut tout de même écrire `.0` après la partie entière.

Exemples : `2.0`, `3.14`, `4.15`, `100.001`

Ces nombres sont appelés **Float** en Ruby.

Un Float peut être utilisé avec les opérations mathématiques suivantes :
- addition notée `+`
- soustraction notée `-`
- multiplication notée `*`
- division notée `/`

On peut également demander à afficher un Float avec la commande `puts` suivie d'un nombre flottant ou d'une opération.

Exemples :

```ruby
puts 15.7
```

Cette commande affichera 15.7 à l'écran.

```ruby
puts 10.0+2.0
```

Cette commande affichera le résultat de l'opération 10.0 + 2.0 c'est-à-dire 12.0 à l'écran.

## Chaînes de caractères - String

En informatique, on décrira du texte par une série de caractères, c'est-à-dire une chaîne de caractères.

En Ruby, les chaînes de caractères sont écrites avec les caractères qui les composent, et doivent impérativement être délimitées par des guillements doubles `"` ou guillements simples `'`. La différence entre les deux types de guillemets est décrite dans des ouvrages avancés sur Ruby, situés dans la FAQ du cours.

Pour la suite de ce cours, nous privilégierons l'utilisation des guillemets doubles `"`.

Exemples : `"abc"`, `"SciencesPo"`, `"Bienvenue dans ce cours !"`

Les chaînes de caractères sont appelées **String** en Ruby.

Une String peut être utilisée avec les opérations suivantes :
- addition notée `+` (concaténation de chaînes)
- multiplication notée `*` (pour répéter une chaîne)

On peut également demander à afficher une String avec la commande "puts" suivie de ce que l'on souhaite afficher.

Exemples :

```ruby
puts "Bonjour Sciences Po !"
```

Cette commande affichera Bonjour Sciences Po ! à l'écran.

```ruby
puts "abc"+"def"
```

Cette commande affichera le résultat de la concaténation de abc et de def, c'est-à-dire abcdef à l'écran.

```ruby
puts "abc"*3
```

Cette commande affichera le résultat de la multiplication de abc par 3, c'est-à-dire abcabcabc à lécran.

Enfin, il est possible d'accéder à un élément d'une String via les symboles `[]` : `"abc"[x]` correspond alors au (x+1)ème élément de "abc".

Exemple :

```ruby
puts "SciencesPo"[0]
```

Cette commande affichera alors le (0+1)ème élément de SciencesPo, soit le 1er élément, c'est-à-dire la lettre S.

[Retour à la table des matières](../../../)
