**1.Principe des tests d'hypothèses paramètriques**

De manière très schématique, très intuitive, et trop simplifiée, plusieurs tests statistiques paramétriques se basent sur une équation qui ressemble à ceci :

![image](https://github.com/fahmismaoui/statspic/assets/64672385/70f603b4-7ef3-475e-9d1f-f5ecc284e1a3)

L'erreur type est une mesure de dispersion, dont le calcul dépond du test statistique choisi. Par exemple, pour le test de comparaison d'une moyenne à une valeur de référence: 

Erreur type = Ecart-type / racine de n , avec n: nombre d'observations

Par la suite, on peut décider si le test est statistiquement significative selon une des deux méthodes suivantes:

◉ **Méthode de la valeur critique:** 

On evalue si la statistique du test (résultat de l'équation, souvent notée Tobs) appartient ou non à un intervalle de confiance. Les bornes supérieures/inférieures de cet intervalle sont souvent appelées valeurs critiques (Tcrit). Si cette statistique du test (Tobs) n'appartient pas cet intervalle, on rejète l'hypothèse H0. Je vais détailler cet intervalle de confiance dans la section suivante.

◉ **Méthode de la p-valeur:** 

On calcule une probabilité, et on la compare avec un niveau de signification α (classiquement 0.05). Si p-valeur < α, on rejète l'hypothèse H0. 

__**Comment calculer la p-valeur?**__

L'équation qui détermine la p-valeur, en se basant sur la statistique du test (Tobs), est très compliquée. Essentiellement, l'équation se base sur l'inverse de la fonction de distribution cumulative (sans entrer dans les détails). Aujourd'hui, avec les avancées informatiques, l'utilisation de logiciels permet d'effectuer ce calcul complexe et de déterminer la p-valeur de manière rapide et précise.


**NB**: *Il ne faut pas confondre "test statistique" et "statistique du test". En effet, "statistique du test" correspond aux résultat de l'équation du "test statistique".*

**2.Test d'hypothèse et intervalle de confiance**

L'intervalle de confiance dépend du __niveau de signification__ choisi (α) ainsi que de la nature __unilatérale ou bilatérale__ du test. 

Je vais expliquer comment choisir le niveau de signification et le sens de comparaison:

◉ __**Nature unilatérale ou bilatérale**__ : Cela dépond de la direction de comparaison.

◌ _**Test Unilatéral**_ : Évalue une hypothèse dans une seule direction. Par exemple, on veux savoir si proportion(A) > valeur de référence.

A noter, on peut réecrire notre hypothèse sous cette forme: on veux savoir si Tobs > Tcrit (La notion que vous allez trouvez dans le cours)

◌ _**Test Bilatéral**_ : Évalue une hypothèse dans les deux directions. Par exemple, on veux savoir si proportion(A) ≠ valeur de référence.

A noter, si le test est bilatéral, l'intervale de confiance est **symétrique**.

C'est à dire, la valeur absolue de la |Tcrit_borne_inférieure| = |Tcrit_borne_supérieure| (on va la noter en tant que |Tcrit|)

En d'autres termes, on compare la statistique du test (Tobs) avec l'intervalle de confiance -> On vérifie si Tobs ∉ [Tcrit_borne_inférieure; Tcrit_borne_supérieure] -> On vérifie si |Tobs| > |Tcrit| (La notion que vous allez trouvez dans le cours)

*=> DONC, dans les deux cas (test unilatéral/bilatéral), on cherche toujours à savoir si |Tobs| > |Tcrit| pour rejeter l'hypothèse H0.*

◉ __**Niveau de signification α**__ (également appelé Erreur de Type I ou de 1er espèce) : 

C’est le niveau de confiance souhaité. Plus il est petit, plus on est sûr de rejeter l'hypothèse H0. Cependant, une valeur trop faible peut conduire à ne pas détecter une différence réelle (je vais vous donner un exemple juste par la suite). 

Généralement, le niveau de signification α choisi est de 0.05. Mais, α peut être ajusté selon la rigueur souhaitée, comme α = 0.01 (1%) pour un test plus strict ou α = 0.10 (10%) pour un test moins strict.


**Quelques remarques concernant le raisonnement statistique**

Dans le passé, les statisticiens utilisaient des tableaux de conversion pour approximer la Tcrit correspondant à chaque niveau de siginfication α. Puis, on comparait la statistique du test (Tobs) avec cette Tcrit. Un exemple de tableaux de conversion (pour test de student pour 2 échantillons indépendants) est ci-dessous.

![image](https://github.com/fahmismaoui/statspic/assets/64672385/236175e4-806b-405c-9ca3-2330add3dfa2)

Aujourd'hui, avec les avancées informatiques, l'utilisation de logiciels permet d'effectuer ce calcul complexe et de déterminer la p-valeur de manière plus précise et efficace.

Par la suite, je vais aborder chaque test à part.


**3.Comparaison d'une proportion à une valeur de référence**

Pour ce test, l'intervalle de confiance [-1.96; 1.96] correspond à un test __bilatéral__ avec un niveau de signification __α = 0.05__.

Pour illustrer comment l’intervalle de confiance dépond des paramètres alpha et de la nature uni/bilatérale du test de comparaison d'une proportion, j’ai créé les visualisations suivantes.
![image](https://github.com/fahmismaoui/statspic/assets/64672385/42fb152e-6c28-4aa9-87fb-b92c2200bc53)

Pour les test




Pour plus d'informations sur les tests statistiques, vous pouvez consulter la référence suivante : 

https://www.math.univ-toulouse.fr/~besse/Wikistat/pdf/st-l-inf-tests.pdf

