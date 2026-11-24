# Price-Formation-Analysis
Régression linéaire sur l'immobilier californien (1990) : préparation des données brutes, feature engineering et interprétation des coefficients pour comparer le poids du revenu (median_income) et de la taille des logements (AveRooms).
# 🏠 Price-Formation-Analysis
> Régression linéaire sur l'immobilier californien (1990) : préparation des données brutes, *feature engineering* et interprétation des coefficients pour comparer le poids du revenu (`median_income`) et de la taille des logements (`AveRooms`).

## 🎯 Pourquoi ce projet
Dépasser l'intuition selon laquelle « plus c'est grand, plus c'est cher ». Mon objectif est de quantifier précisément l'impact de chaque caractéristique sur le prix afin de poser des bases solides en régression linéaire avant d'explorer des modèles plus complexes.

## ❓ Problematique
> *« Le revenu médian des habitants d'un quartier pèse-t-il plus lourd que la taille des logements dans la fixation du prix ? »*

## 📊 Jeu de données et choix techniques
J'utilise le dataset **California Housing Prices** (version brute issue de Kaggle).

* **Pourquoi cette source ?** Contrairement à la version pré-nettoyée de Scikit-learn, le fichier brut de Kaggle contient des valeurs manquantes et nécessite de calculer manuellement le nombre moyen de pièces (`AveRooms`). Cela me permet de mettre en pratique le *feature engineering* et le nettoyage sur données réelles.
* **Variables clés :**
  * `median_income` : revenu médian des ménages du district.
  * `housing_median_age` : âge médian des logements.
  * `AveRooms` : nombre moyen de pièces par ménage (calculé via `total_rooms / households`).

## 🔍 Ce que j'ai déjà trouvé (Exploration préliminaire)
En ouvrant les données brutes, deux constats guident mon approche :

1. **Le plafonnement de la cible :** La variable `median_house_value` est bloquée à **500 001 $**. Je devrai traiter ces valeurs pour éviter de biaiser la régression.
2. **La corrélation revenu/prix :** Une première visualisation rapide montre que les quartiers à haut revenu ont des prix systématiquement plus élevés, suggérant que le facteur socio-économique est déterminant.

## 📦 Mes livrables concrets
Pour démontrer ma maîtrise technique et analytique, ce dépôt contient :

1. **Le Notebook de Diagnostic (`notebooks/`) :** Un code Python commenté montrant comment j'ai traité les valeurs manquantes (`total_bedrooms`), calculé les nouvelles variables (`AveRooms`) et isolé les valeurs plafonnées.
2. **Le Graphique Comparatif (`reports/`) :** Une visualisation superposant deux droites de régression (*Revenu vs Prix* et *Pièces vs Prix*) pour identifier visuellement quel facteur a l'impact le plus fort.
3. **La Note de Synthèse (`reports/`) :** Une conclusion chiffrée indiquant le poids exact de chaque variable, accompagnée d'une analyse honnête des limites du modèle linéaire.

## ⚙️ Installation et exécution

1. **Cloner le dépôt :**
   git clone https://github.com/Tresorkitwanda00/Price-Formation-Analysis.git
2. pip install -r requirements.txt
3. jupyter lab

   git clone [ton-lien-github]
   cd Price-Formation-Analysis
