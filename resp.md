__**I.Réponse directe aux questions**__

Tout d'abord, il est important de souligner que l'intervalle de confiance n'est pas toujours défini comme [-1.96, 1.96]. L'intervalle de confiance dépend du niveau de signification α, de la nature uni/bilatérale, et, pour certains tests, du degré de liberté. Cet intervalle spécifique [-1.96, 1.96] correspond à un test bilatéral avec un niveau de signification α de 0.05. Cela s'applique notamment aux tests de comparaison de proportion/moyenne à une valeur de référence, de comparaison de deux proportions, et de comparaison de deux moyennes (test de Student pour échantillons appariés/indépendants) lorsque le nombre d'observations est très élevé. 
Cependant, il est essentiel de noter que pour des échantillons avec un nombre d'observations plus faible, l'intervalle de confiance du test de Student aura tendance à être plus large. Dans cette situation, il dépend aussi du degré de liberté (Pour ce test : ddl = n-1).

Le principe général de tous ces tests repose sur la comparaison de la valeur du test statistique (appelé statistique du test ou Tobs) avec une valeur critique (par exemple : Tcrit = 1.96). Si Tobs n'appartient pas à cet intervalle de confiance :

c’est-à-dire Tobs ∉ [-1.96, 1.96]

c’est-à-dire Tobs < -1.96 et Tobs > 1.96

c’est-à-dire |Tobs| > |Tcrit|=1.96

Dans ce cas, on peut rejeter l'hypothèse H0.

Une autre méthode est la détermination d’une probabilité appelée « p-valeur », qu'on va comparer avec le niveau de signification α. À noter qu’on ne peut réaliser ce calcul qu’en utilisant des logiciels, puisque l’équation est complexe.

Ces deux méthodes s’appliquent au test Chi-deux de Pearson. Le principe de ce test repose sur la comparaison des valeurs observées avec des valeurs théoriques attendues si H0 est vrai. Une particularité du test Chi-deux c’est que la Tcrit dépend du niveau de signification α et du degré de liberté qui se calcule de la façon suivante :

Ddl = (r-1)(c-1) ; avec r : nombre de lignes, c : nombre de colonnes

Une fois que l'on connaît le ddl et que l'on a choisi le niveau de signification α, on peut utiliser un tableau de conversion pour déterminer la valeur Tcrit. 
![image](https://github.com/fahmismaoui/statspic/assets/64672385/c5a36aa6-1b2a-4544-a1f0-f91ccfc24e73)


Une fois la valeur Tobs est déterminée en utilisant l’équation du test Chi-deux, on peut comparer Tobs avec Tcrit :
Si Tobs > Tcrit, donc on rejette l’hypothèse H0.

Par exemple, si l'on veut savoir s'il y a une association entre le fait de fumer et le sexe, on va avoir un tableau 2x2 (fumeur/non-fumeur X homme/femme) :

Ddl = (2 * 1) * (2 * 1) = 1

Supposant qu’on a choisi alpha = 0.05, la Tcrit selon le tableau est :

Tcrit = 3.841 (C'est la valeur du test Chi-deux au Ddl de 1, avec alpha = 0.05)

Si notre Tobs > Tcrit = 3.841, on va rejeter l’hypothèse H0, et on va dire qu'il y a une association statistiquement significative entre le fait de fumer et le sexe.

(Ce que nous avons fait ici est la comparaison avec la Tcrit, c'est à dire la comparaison avec la valeur du test Chi-deux au Ddl de 1, avec alpha = 0.05)


__**II.Plus de détails**__

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

L'intervalle de confiance (ou intervalle d'acceptation) dépend du __niveau de signification__ choisi (α) ainsi que de la nature __unilatérale ou bilatérale__ du test. 

Je vais expliquer comment choisir le niveau de signification et la nature uni/bilatérale:

◉ __**Niveau de signification α**__ (également appelé Erreur de Type I ou de 1er espèce) : 

C’est le niveau de confiance souhaité. Plus il est petit, plus on est sûr de rejeter l'hypothèse H0. Cependant, une valeur trop faible peut conduire à ne pas détecter une différence réelle (je vais vous donner un exemple juste par la suite). 

Généralement, le niveau de signification α choisi est de 0.05. Mais, α peut être ajusté selon la rigueur souhaitée, comme α = 0.01 (1%) pour un test plus strict ou α = 0.10 (10%) pour un test moins strict.


◉ __**Nature unilatérale ou bilatérale**__ : Cela dépond de la direction de comparaison.

◌ _**Test Unilatéral**_ : Évalue une hypothèse dans une seule direction. Par exemple, on veux savoir si proportion(A) > valeur de référence.

A noter, la régle de décision dans ce cas est de voir si Tobs > Tcrit.

Dans le cas contraire, si on a voulu savoir si proportion(A) < valeur de référence, la règle de décision serai Tobs < Tcrit.

Pour ne pas compliquer la vie, on peut décider dans les deux situations (proportion(A) > valeur de référence et proportion(A) < valeur de référence) par la règle suivante:

Si |Tobs| > |Tcrit| -> on rejète H0.

◌ _**Test Bilatéral**_ : Évalue une hypothèse dans les deux directions. Par exemple, on veux savoir si proportion(A) ≠ valeur de référence.

A noter, si le test est bilatéral, l'intervale de confiance est **symétrique**.

C'est à dire, la valeur absolue de la |Tcrit_borne_inférieure| = |Tcrit_borne_supérieure| (on va la noter en tant que |Tcrit|)

Exemple: L'intervalle de confiance (d'acceptation) du test Z de comparaison d'une proportion à une valeur de réfèrence qui est **bilatéral** avec un niveau de signification **α = 0.05** est égale à [-1.96, 1.96].

On peut voir que c'est un intervalle symétrique 

|Tcrit_borne_inférieure| = |Tcrit_borne_supérieure|
|-1.96| = |1.96|

Dans ce cas, on veux savoir si Tobs ∉ [-1.96, 1.96] (∉: n'appartient pas à) pour rejeter H0.

c’est-à-dire Tobs < -1.96 et Tobs > 1.96

c’est-à-dire |Tobs| > |Tcrit|=1.96 pour rejeter l'hypothèse H0.

__*=> DONC, dans les deux cas (test unilatéral/bilatéral), on cherche à savoir si |Tobs| > |Tcrit| pour rejeter l'hypothèse H0.*__

_*NB*_

Pour certains tests, comme le test de Student (comparaison de moyennes), l'intervalle de confiance dépond aussi d'un paramètre appelé **degré de liberté (ddl)** (dans le cas du test de Student: ddl = n - 1 , avec n: nombre d'observations).



**Quelques remarques concernant le raisonnement statistique**

Dans le passé, les statisticiens utilisaient des tableaux de conversion pour approximer la Tcrit correspondant à chaque niveau de siginfication α. Puis, on comparait la statistique du test (Tobs) avec cette Tcrit. Un exemple de tableaux de conversion (pour test de student pour 2 échantillons indépendants) est ci-dessous.

![image](https://github.com/fahmismaoui/statspic/assets/64672385/236175e4-806b-405c-9ca3-2330add3dfa2)

Aujourd'hui, avec les avancées informatiques, l'utilisation de logiciels permet d'effectuer ce calcul complexe et de déterminer la p-valeur de manière plus précise et efficace.


**Pourquoi l'intervalle de confiance peut varier entre les tests statistiques**

Sans entrer trop dans les détails, il est crucial de comprendre que les tests statistiques mentionnés ci-dessus reposent sur des lois de distribution spécifiques.

Tout test qui suit une loi de distribution normale (de moyenne 0 et d'écart-type 1, notée N(0,1)), présente les mêmes intervalles de confiance (d'acceptation). Pour expliquer comment cet intervalle de confiance dépend des paramètres alpha et de la nature uni/bilatérale, j’ai créé les visualisations suivantes.

![image](https://github.com/fahmismaoui/statspic/assets/64672385/42fb152e-6c28-4aa9-87fb-b92c2200bc53)


Par exemple, le test Z de proportion se fonde sur la loi de distribution normale. Cela peut vous paraitre bizarre, puisque les proportions se calculent à partir de variables binaires (ex: sexe = homme/femme) qui suivent une loi de distribution binomiale. Cependant, pour simplifier les choses, on peut approximer cette loi binomiale en loi normale, surtout si le nombre d'observations n'est pas faible.

Cependant, le test de comparaison de moyenne (test de Student) se base sur une loi différente : la loi de distribution de Student. L'aspect de la courbe de distribution dans ce cas dépend du degré de liberté (et donc du nombre d'observations, puisque ici ddl=n-1). C'est pourquoi l'intervalle de confiance (d'acceptation) varie en fonction du ddl pour ce test.

Une particularité de la loi de distribution de Student est qu'elle devient très similaire à une loi de distribution normale lorsque n est très élevé, comme indiqué dans la figure suivante.


Dans le tableau de conversion suivant (spécifique pour un test de Student bilatéral), on peut observer que |Tcrit| pour α = 0.05 tend à s'approcher de la valeur 1.96 à mesure que le ddl augmente (n augmente), correspondant à |Tcrit| d'un test qui suit la loi de distribution normale avec une comparaison bilatérale et α = 0.05. Ainsi, avec un nombre élevé d'échantillons, l'intervalle pour le test de Student devient presque équivalent à [-1.96, 1.96].

![image](https://github.com/fahmismaoui/statspic/assets/64672385/7aaa8773-cc68-47f8-aed8-84e28105fb8d)





Par la suite, je vais aborder chaque test à part.


**3.Comparaison d'une proportion à une valeur de référence**

Pour ce test, l'intervalle de confiance [-1.96; 1.96] correspond à un test __bilatéral__ avec un niveau de signification __α = 0.05__.

Pour illustrer comment l’intervalle de confiance dépond des paramètres alpha et de la nature uni/bilatérale du test de comparaison d'une proportion, j’ai créé les visualisations suivantes.
![image](https://github.com/fahmismaoui/statspic/assets/64672385/42fb152e-6c28-4aa9-87fb-b92c2200bc53)






Pour plus d'informations sur les tests statistiques, vous pouvez consulter la référence suivante : 

https://www.math.univ-toulouse.fr/~besse/Wikistat/pdf/st-l-inf-tests.pdf

