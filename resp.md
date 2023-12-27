**1.Principe des tests d'hypothèses paramètriques**

De manière très schématique, très intuitive, et trop simplifiée, plusieurs tests statistiques paramétriques se basent sur une équation qui ressemble à ceci :

![image](https://github.com/fahmismaoui/statspic/assets/64672385/70f603b4-7ef3-475e-9d1f-f5ecc284e1a3)

L'erreur type est une mesure de dispersion, dont le calcul dépond du test statistique choisi.

Par la suite, on peut décider si le test est statistiquement significative selon deux manière:

◉ **Méthode de la valeur critique:** 

On evalue si la statistique du test (résultat de l'équation) appartient ou non à un intervalle de confiance. Si cette valeur (souvent noté Tobs) n'appartient pas cet intervalle, on rejète l'hypothèse H0.

◉ **Méthode de la p-valeur:** 

On calcule une probabilité, et on la compare avec un niveau de signification α (classiquement 0.05). Si p-valeur < α, on rejète l'hypothèse H0. 

**NB**: *Il ne faut pas confondre "test statistique" et "statistique du test". En effet, "statistique du test" correspond aux résultat de l'équation du "test statistique".*

**2.Test d'hypothèse et intervalle de confiance**

L'intervalle de confiance dépend du __niveau de signification__ choisi (α) ainsi que de la nature __unilatérale ou bilatérale__ du test. 

Je vais expliquer comment choisir le niveau de signification et le sens de comparaison:

◉ __**Nature unilatérale ou bilatérale**__ : Cela dépond de la direction de comparaison.

◌ _**Test Unilatéral**_ : Évalue une hypothèse dans une seule direction. Par exemple, on veux savoir si proportion(A) > valeur de référence.

◌ _**Test Bilatéral**_ : Évalue une hypothèse dans les deux directions. Par exemple, on veux savoir si proportion(A) ≠ valeur de référence.

◉ __**Niveau de signification α**__ (également appelé Erreur de Type I ou de 1er espèce) : 

C’est le niveau de confiance souhaité. Plus il est petit, plus on est sûr de rejeter l'hypothèse H0. Cependant, une valeur trop faible peut conduire à ne pas détecter une différence réelle (je vais vous donner un exemple juste par la suite). 

Généralement, le niveau de signification α choisi est de 0.05. Mais, α peut être ajusté selon la rigueur souhaitée, comme α = 0.01 (1%) pour un test plus strict ou α = 0.10 (10%) pour un test moins strict.

Par la suite, je vais aborder chaque test à part.


**3.Comparaison d'une proportion à une valeur de référence**

Pour ce test, l'intervalle de confiance [-1.96; 1.96] correspond à un test __bilatéral__ avec un niveau de signification __α = 0.05__.

Pour illustrer comment l’intervalle de confiance dépond des paramètres alpha et de la nature uni/bilatérale du test de comparaison d'une proportion, j’ai créé les visualisations suivantes.
![image](https://github.com/fahmismaoui/statspic/assets/64672385/42fb152e-6c28-4aa9-87fb-b92c2200bc53)

Pour les test




Pour plus d'informations sur les tests statistiques, vous pouvez consulter la référence suivante : 

https://www.math.univ-toulouse.fr/~besse/Wikistat/pdf/st-l-inf-tests.pdf

