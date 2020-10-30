## Calcul de Pi

A partir des éléments de hasard vus dans l'exercice Juste Prix, nous pouvons aussi calculer des valeurs intéressantes comme Pi.

Cette méthode s'appelle la méthode de Monte Carlo : https://www.youtube.com/watch?v=t1X1Agp1CWA.

En effet, considérons les éléments suivants :
- soit un ensemble de 1000 fléchettes, lancées au hasard dans un carré de 1 par 1 ;
- soit la formule permettant de calculer combien de fléchettes sont dans le cercle circonscrit au carré de 1 par 1.

Alors nous pouvons calculer le nombre de fléchettes dans le cercle, au regard du nombre de fléchettes tirées. Ce ratio nous permet directement de calculer Pi.

En effet :
- aire du cercle = pi * rayon * rayon ;
- aire du carré = cote * cote ;
- et si le cercle est circonscrit au carré, alors rayon = cote / 2.

Donc nous avons :
- aire du cercle = pi * cote / 2 * cote / 2 ;
- aire du carré = cote * cote.

Et, pour un nombre de fléchettes très grand, nous avons la relation : aire du cercle / aire du carré = nombre de fléchettes dans le cercle / nombre de fléchettes lancées au total.

D'où : pi * cote / 2 * cote / 2 / cote / cote = nombre de fléchettes dans le cercle / nombre de fléchettes lancées au total.

Ou, de manière simplifiée, pour un nombre très grand de fléchettes : pi = 4 * nombre de fléchettes dans le cercle / nombre de fléchettes lancées au total.

A partir de ces élements, calculer une valeur de Pi approchée. A vous de jouer ! (en session de cours)

[Retour à la table des matières](../../../)
