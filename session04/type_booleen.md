# Session 4 - Le type Booléen

L'informatique permet d'automatiser beaucoup de choses, et dépend régulièrement de certaines conditions :
- l'utilisateur est-il connecté ?
- la valeur saisie est-elle bien valide ?

Un humain répond à ces questions sous la forme "oui ou non". Une machine traite ces questions à l'aide de conditions, qui peuvent être vraies ou fausses.

Dans ce cadre, Ruby introduit un type de donnée complémentaire, nommé "Booléen", ou **Boolean**" n anglais (cf [Algèbre de Boole](https://fr.wikipedia.org/wiki/Alg%C3%A8bre_de_Boole_(logique))).

Le type Boolean peut prendre 2 valeurs :
- **true**, c'est-à-dire la valeur "vraie" ;
- **false**, c'est-à-dire la valeur "fausse".

Ces valeurs **true** et **false** vont nous permettre d'effectuer des actions conditionnelles, c'est-à-dire qui auront des comportements différents suivant la valeur du booléen fourni.

Le type booléen permet d'introduire les opérations suivantes :

```ruby
a > b # vaut true si a est strictement supérieur à b, vaut false sinon
a >= b # vaut true si a est supérieur ou égal à b, vaut false sinon
a < b # vaut true si a est strictement inférieur à b, vaut false sinon
a <= b # vaut true si a est inférieur ou égal à b, vaut false sinon
a == b # vaut true si a est égal à b, vaut false sinon
!a # vaut l'opposé de a, c'est-à-dire que cela vaut true si a est false, et cela vaut false si a est true
```

Quelques exercices pour s'entraîner :

```ruby
# Quels sont les résultats des opérations suivantes ?

# Opération 1
50 > 30

# Opération 2
50 >= 50

# Opération 3
30 < 30

# Opération 4
(50 - 30) == (100 - 80)

# Opération 5
!(50 >= 50)
```


[Retour à la table des matières](../../../)