# Session 4 - Les structures conditionnelles

Pour exécuter du code en fonction d'une valeur booléenne, Ruby fournit des structures dites "structures conditionnelles".

Elles reposent sur les mots-clés :
- **if** (si) ;
- **else** (sinon) ;
- **elsif** (sinon si) ;
- **end** (fin).

Ces mots-clés vont servir à rédiger du code visant à remplir l'objectif suivant :

```
Si CONDITION 1 EST VRAIE
    Action 1
Sinon, si CONDITION 2 EST VRAIE
    Action 2
Sinon
    Action 3
Fin
```

On note ainsi :

```ruby
if ( test_logique )
   # Partie du code qui s'exécute si test_logique vaut true
else
   # Partie du code qui s'exécute si test_logique vaut false
end
```

Par exemple pour un radar de vitesse :

```ruby
def verbaliser(vitesse_param)
   reference = 80 # vitesse limite en km/h

   if ( vitesse_param > reference )
      puts "Vitesse trop importante !"
   else
      puts "Vitesse OK."
   end
end
verbaliser(100) # "Vitesse trop importante !"
verbaliser(70) # "Vitesse OK."
verbaliser(80) # "Vitesse OK."
```

ou encore :

```ruby
if ( test_logique_1 )
   # Partie du code qui s'exécute si test_logique_1 vaut true
elsif ( test_logique_2 )
   # Partie du code qui s'exécute si test_logique_1 vaut false, et si test_logique_2 vaut true
else
   # Partie du code qui s'exécute sinon
end
```

avec par exemple :

```ruby
def verbaliser(vitesse_param)
   reference = 80 # vitesse limite en km/h

   if ( vitesse_param > reference )
      puts "Vitesse trop importante !"
   elsif ( vitesse_param == reference )
      puts "Vitesse limite atteinte !"
   else
      puts "Vitesse OK."
   end
end
verbaliser(100) # "Vitesse trop importante !"
verbaliser(70) # "Vitesse OK."
verbaliser(80) # "Vitesse limite atteinte !"
```

[Retour à la table des matières](../../../)