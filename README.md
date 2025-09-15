# Analyse et détecttion des trues et fake news
Ensemble de traitement du langage naturel permettant de deviner la véracité d'un poste sur twitter

Dataset : fake-and-real-news-dataset
Auteur : NONO KAKEU Andy
Date : 12 septembre 2025

Objectif : l'objectif du projet de se servir de ses connaissances en traitement de language pour prédire la véracité d'un poste sur X(twitter). Pour cela, j'ai développé 2 modèle de machine learning, Naive Bayes et SVM. J'ai ensuite fait une étude comparative pour comprarer la puissance des modèles et leurs utlilitées dans la résolution du problème.

Naive Bayes :
Le modèle a correctement classé 4383 fake news et 3936 vraies nouvelles.
●	En revanche, il a commis 309 erreurs en classant des fake news comme vraies, et 348 erreurs inverses.
●	Le nombre total d’erreurs est donc de 657, ce qui est relativement élevé.
●	Cela montre que le modèle a du mal à bien séparer les deux classes, notamment lorsqu’un article possède des caractéristiques proches des deux types de contenus.
Interprétation :
Naive Bayes repose sur une hypothèse forte d’indépendance entre les mots, ce qui est rarement vérifié dans le langage naturel. Cela peut expliquer pourquoi le modèle fait encore de nombreuses confusions dans les cas où les textes sont ambigus ou partagent un vocabulaire similaire.

SVM :
Le modèle a correctement classé 4641 fake news et 4241 vraies nouvelles, soit un total de 8882 prédictions correctes.
●	Il n’a commis que 94 erreurs au total (51 en fake et 43 en True dans chaque classe).
●	Ces résultats indiquent une très forte capacité de généralisation, avec des performances quasi parfaites sur les données de test.
 Interprétation :
Le SVM (Support Vector Machine) est particulièrement bien adapté aux données textuelles transformées via TF-IDF, car il gère très bien les espaces de grande dimension et cherche à maximiser la marge de séparation entre les classes. Cela lui permet d’être beaucoup plus précis, même sur des données complexes ou déséquilibrées.

Conclusion comparative finale :
●	Le SVM est nettement plus performant que Naive Bayes.
●	Il réalise 7 fois moins d’erreurs, avec une précision bien meilleure pour les deux classes.
●	Cela s’explique notamment par le fait que le SVM ne repose pas sur des hypothèses probabilistes simplifiées, et peut donc capturer des frontières de décision plus complexe.

