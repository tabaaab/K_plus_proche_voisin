![image](https://g.top4top.io/p_19435g1c11.jpg)

Realisé par : TABAA Abdelkader / M1 info ISIMA


### Introduction

Le K-plus proche voisin est un algorithme d'apprentissage automatique supervisé.

### Énoncé du problème

Étant donné certains points de données étiquetés, nous devons classer un nouveau point de données en fonction de ses plus proches voisins.

**Exemple utilisé ici**

Nous disposons des données d'une grande entreprise de réseaux sociaux qui a réalisé des sondages sur le langage de programmation préféré des utilisateurs. Les utilisateurs appartiennent à un groupe de grandes villes. Maintenant, le vice-président de l'engagement communautaire veut que vous prédisiez le langage de programmation préféré pour les villes qui n'ont pas participé à l'enquête.

### Intuition

* Dans kNN, k est le nombre de voisins que vous évaluerez pour décider à quel groupe appartient un nouveau point de données ?
* La valeur de k est décidée en traçant le taux d'erreur en fonction des différentes valeurs de k.
* Une fois que la valeur de k est fixée, nous prenons les k voisins les plus proches du point de données.
* La mesure de la distance entre les points de données peut être calculée en utilisant la "distance euclidienne" ou la "distance de Manhattan".
* Une fois que nous avons calculé la distance de tous les k neigbors les plus proches, nous recherchons la majorité des étiquettes dans les neigbots.
* Le point de données est assigné au groupe qui a le nombre maximum de neigbots.

### Choix de la valeur K
* Tout d'abord, diviser l'ensemble des données en un ensemble de formation et un ensemble de test. 
* Appliquer l'algorithme KNN à l'ensemble d'entraînement et le valider avec l'ensemble de test.
* Supposons que vous ayez un ensemble d'entraînement `xtrain` et un ensemble de test `xtest`.
* Maintenant, créez le modèle avec la valeur `k` 1` et prédisez avec les données de l'ensemble de test. 
* Vérifiez la précision et les autres paramètres, puis répétez le même processus en augmentant la valeur de k de 1 à chaque fois.


### Note

* kNN est impacté par les `Ensembles de données déséquilibrés`. 
Supposons qu'il y ait `m` instances de **classe 1** et `n` instances de **classe 2** où `n << m`. 
Dans le cas où `k > n`, cela peut conduire à compter plus d'instances de m et donc avoir un impact sur l'élection majoritaire. 
donc cela aura un impact sur l'élection de la majorité dans les k plus proches voisins.

* kNN est également très sensible aux "valeurs aberrantes".


