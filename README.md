# 🎮 Prédiction des Ventes de Jeux Vidéo

Ce projet vise à analyser les ventes mondiales de jeux vidéo à partir du dataset VGChartz 2024.

**Objectif** : Prédire les ventes totales d'un jeu en fonction de sa plateforme, son genre et son éditeur.

**Dataset** : vgchartz-2024.csv — données de ventes mondiales de jeux vidéo.

---

## 📊 Insights clés

En regardant les ventes totales par éditeur, c'est **Activision** qui domine en volume global. 
Le genre **Sport** arrive en tête des ventes mondiales par catégorie. 
Et côté plateforme, **PlayStation** est la famille de consoles qui génère le plus de ventes au niveau mondial.

![Visualisation globale](https://github.com/landrykiki0/Predictions-ventes-Data-Machine-Learning-/blob/5ccc4a61bca793751cfe7f0e3ee04f5d00f53e8a/Visualisation%20Power%20BI.png)

On se dirait donc que pour faire le plus de ventes, il serait plus simple de sortir un jeu de sport, sur PlayStation et édité par Activision. 
Cependant, cette analyse était globale . Activision domine peut-être juste parce qu'ils ont édité beaucoup de jeux. 
C'est exactement pour gagner ce temps qu'on entraîne un modèle prédictif.

---

## 🤖 Modélisation

**Algorithme** : Random Forest Regressor (scikit-learn)  
**Split** : 85% entraînement / 15% test  
**Encodage** : One-hot encoding sur genre, plateforme et éditeur

**Résultats :**

| Métrique | Score |
|---|---|
| RMSE | 0.41 M copies |
| MAE | 0.28 M copies |
| MAPE | 89.8% |

Le MAPE élevé est attendu sur ce type de données — les ventes varient de quelques milliers à plusieurs millions selon les jeux, ce qui rend la prédiction proportionnelle difficile sur les petits titres.

---

## 🧪 Test concret

J'ai simulé deux jeux de genre Action sur PlayStation, l'un édité par Rockstar Games et l'autre par Activision.

- **Action / Rockstar Games / PlayStation** → estimé à **5.7 millions** de ventes
- **Action / Activision / PlayStation** → estimé à **0.6 millions** de ventes

Notre doute sur la domination d'Activision était donc fondé — dans le domaine de l'action sur PlayStation, Rockstar Games performe bien mieux en termes de ventes.

---

## 🛠️ Stack technique

- **Python** — langage principal
- **Pandas** — manipulation et nettoyage des données
- **NumPy** — calculs numériques
- **Matplotlib / Seaborn** — visualisation des données
- **Scikit-learn** — modélisation et évaluation (Random Forest Regressor)
- **Power BI** — dashboards interactifs

---

## 🚀 Lancer le projet
1. Clone le repo
2. Ouvre le notebook dans Jupyter ou directement sur Google Colab.
