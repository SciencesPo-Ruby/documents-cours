# Session 2 - Structures de données élémentaires

Souvent, l'informatique demande de travailler sur des groupes de données, plutôt que sur des données prises de manière individuelle.

Un exemple est le cas de Sciences Po et des inscriptions pédagogiques : un groupe d'élèves doit élaborer son parcours pédagogique parmi un catalogue comportant un groupe de cours.
Les cours, assemblés dans une structure de données adaptée, peuvent alors être triés, catégorisés, hiérarchisés, ce qui permet aux élèves de faire des choix plus pertinents.

En Ruby, les "groupes" de données les plus classiques, et dont nous aurons besoin dans ce cours, sont au nombre de 2 : les tableaux, et les dictionnaires.

## Les tableaux - Array

Les tableaux sont des assemblages ordonnés, qui permettent de hiérarchiser les données.

Ils consistent à prendre l'ensemble des données souhaitées, et à leur attribuer un numéro unique appelé **index**. Le tableau est alors formé de la suite de ces données, prises dans l'ordre croissant de leur index.

Un tableau, en Ruby, est appelé **Array** et est délimité à partir des caractères `[` et `]`. Les éléments qui le composent sont séparés par une **virgule** `,`.

Attention :
- par convention, l'élément placé en première position du tableau a pour index **0** ;
- l'index est ensuite **incrémenté de 1** pour chaque nouvel objet ajouté au tableau ;
- le tableau vide, qui ne contient aucun élément, est noté **[]**.

Exemples :
- `["premier", "deuxième", "troisième"]` est un tableau de chaînes de caractères, dont "premier" a l'index 0, "deuxième" l'index 1, et "troisième" l'index 2 ;
- `[10, 2]` est un tableau de nombres entiers, dont 10 a l'index 0, 2 l'index 1.


Si on peut construire des tableaux comportant un type unique de données, on peut aussi utiliser des tableaux comportant plusieurs types de données, comme `["a", 2, 3.0]`.

On peut aussi mettre un tableau dans un autre tableau, comme `[[1, 2, 3], [4, 5, 6], [7, 8, 9]]`.

Un tableau dispose lui aussi d'opérations de base :
- addition notée `+` (concaténation de tableaux)
- soustraction notée `-` (suppression d'éléments)
- multiplication notée `*` (pour répéter un tableau)
- union notée `|` (union de plusieurs ensembles)
- intersection notée `&` (intersection de plusieurs ensembles)

On peut également demander à Ruby d'afficher un Array avec la commande "puts" suivie de ce que l'on souhaite afficher. L'affichage se fait alors consécutivement avec chaque élément du tableau.

Exemple :

```ruby
puts [1,2,3] + [4,5]
```


Cette commande affichera consécutivement le contenu du résultat de la concaténation de `[1,2,3]` et `[4,5]` (c'est-à-dire `[1,2,3,4,5]`) de la manière suivante :

```
1
2
3
4
5
```

Exemple :

```ruby
puts [1,2,3] - [1,3]
```

Cette commande affichera [2], de la manière suivante :

```
2
```

Exemple :

```ruby
puts [1,2,3] * 2
```


Cette commande affichera `[1,2,3,1,2,3]` consécutivement, de la manière suivante :

```
1
2
3
1
2
3
```

Exemple :

```ruby
puts [1,2,3] | [3,4,5]
```

Cette commande affichera [1,2,3,4,5] consécutivement, de la manière suivante :

```
1
2
3
4
5
```

Exemple :

```ruby
puts [1,2,3] & [3,4,5]
```

Cette commande affichera [3], de la manière suivante :

```
3
```

Enfin, il est possible d'accéder à un élément d'un Array via les symboles [] : [1,2,3][x] correspond alors au (x+1)ème élément de [1,2,3].

Exemple :

```
puts [1,2,3][1]
```

Cette commande affichera alors le (1+1)ème élément de [1,2,3], soit le 2ème élément, c'est-à-dire l'Integer 2.

## Dictionnaires - Hash

Les dictionnaires sont des assemblages non-ordonnés, qui permettent de ranger les données avec des étiquettes.

Ils consistent à prendre l'ensemble des données souhaitées, nommées **valeurs**, et à leur attribuer un identifiant appelé **clé**. Le dictionnaire est alors formé de l'ensemble de ces clés, et des valeurs associées.

Pour mieux comprendre ce concept, nous pouvons prendre une situation de la vie de tous les jours : cela revient à avoir un immeuble, avec plusieurs appartements. Dans chaque appartement habite une personne. A l'entrée de l'immeuble se trouvent les boîtes aux lettres, qui indiquent chaque fois le nom d'un habitant suivi du numéro de l'appartement où celui-ci réside.

Le nom de chaque habitant est alors une **clé**, tandis que le numéro d'appartement indiqué pour chaque habitant est une **valeur**.

Autre exemple : la table des matières d'une encyclopédie indique une série de mots, avec à chaque fois un numéro de page. Dans ce cas, chaque mot de la table des matières agit comme une **clé**, et chaque numéro de page indiqué est une **valeur**.

Un dictionnaire, en Ruby, est appelé **Hash** et est délimité à partir des caractères `{` et `}`. Les éléments qui le composent sont alors définis à l'aide de clés et de valeurs, dont la correspondance est indiquée à l'aide des caractères `=>`. Ces couples "clé / valeur" sont séparés les uns des autres par des virgules `,`.

Attention : le dictionnaire vide, qui ne contient aucun élément, est noté `{}`.

Exemples :
- `{ "clé1" => "valeur1" }` est un Hash comportant un seul couple, dont la clé1 est associée à la valeur valeur1 ;
- `{ "clé1" => "valeur1", "clé2" => "valeur2" }` est un Hash comportant deux couples, dont la clé clé1 est associée à la valeur valeur1, et dont la clé clé2 est associée à la valeur valeur2 ;
- `{ "Matignon" => "Premier Ministre", "Elysée" => "Président de la République" }` est un Hash comportant deux couples, dont la clé Matignon est associée à la valeur Premier Ministre, et dont la clé Elysée est associée à la valeur Président de la République ;
- `{ "US" => [ "Trump", "Obama", "Bush", "Clinton" ], "FR" => [ "Macron", "Hollande", "Sarkozy", "Chirac" ]` est un Hash comportant deux couples, dont chaque clé contient un Array des 4 derniers présidents du pays qu'elle décrit.

Vous l'aurez compris avec ce dernier exemple : il est possible de mélanger Hash et Array, c'est d'ailleurs très utile pour modéliser des annuaires informatiques (chaque clé correspond à la lettre de l'index de l'annuaire, et les valeurs associées sont un tableau de tous les noms pertinents et triés par ordre alphabétique).

On peut aussi mettre un dictionnaire dans un autre dictionnaire, comme `{ "clé1" => { "clé1a" => "valeur1a" } }`.

Attention : un hash ne dispose pas des opérations de base `+ - * / | &` !

On peut également demander à afficher un Hash avec la commande `puts` suivie de ce que l'on souhaite afficher.

*Note : il faut encercler le Hash avec des parenthèses. l'utilisation des parenthèses ici permet d'expliciter à Ruby ce que l'on souhaite afficher. Autrement, la notation des Hash pouvant vite être complexe, nous rencontrerions ici une erreur, Ruby ne comprenant pas que l'on souhaite afficher l'ensemble du Hash. Ce problème sera résolu lorsque nous aborderons le sujet des variables.*


Exemple :

```ruby
puts ({"clé" => "valeur"})
```

Cette commande affichera `{"clé"=>"valeur"}`.

Enfin, il est possible d'accéder à un élément d'un Hash via les symboles `[]` : `{"clé" => "valeur"}[KEY]` correspond alors à la valeur associée à la clé **KEY**.

Exemple :

```ruby
puts ({"cléA" => "valeurA"}["cléA"])
```

Cette commande affichera alors la valeur associée à la clé cléA, c'est-à-dire valeurA.

[Retour à la table des matières](../../../)