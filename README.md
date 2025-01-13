# churn_prediction

Analyse et prédiction des résiliations client (**churn**) dans le secteur des télécommunications. Ce projet vise à explorer les données pour identifier les facteurs influençant le churn et à développer des modèles prédictifs fiables pour améliorer la fidélisation des clients.

---

##  Objectifs du projet

- **Analyse des données** :
  - Identifier les variables clés influençant le churn.
  - Comprendre les caractéristiques des clients susceptibles de résilier leur abonnement.
- **Modélisation prédictive** :
  - Développer des modèles baseline pour prédire le churn.
  - Comparer et évaluer plusieurs algorithmes de machine learning.
  - Prioriser les modèles en fonction de leur capacité à minimiser les faux négatifs (détection des clients à risque).

---

##  Approche adoptée

### 1. **Exploration des données (EDA)**
- Analyse des distributions des variables clés (tenure, charges mensuelles, services utilisés, etc.).
- Gestion des valeurs manquantes et encodage des variables catégoriques.
- Visualisations pour mieux comprendre les relations entre les variables et le churn.

### 2. **Modélisation baseline**
- Mise en place de trois modèles baseline :
  - **Régression Logistique** : Modèle simple, efficace et interprétable.
  - **MLP (Multilayer Perceptron)** : Réseau de neurones pour capturer des relations complexes.
  - **Forêt Aléatoire** : Modèle robuste pour les données tabulaires.

- **Hyperparamètres optimisés** : Ajustement léger pour chaque modèle afin d'améliorer les performances sans perdre en simplicité.

### 3. **Évaluation des performances**
- Utilisation des métriques clés :
  - **Matrice de confusion** : Analyse des faux négatifs et faux positifs.
  - **Précision**, **Rappel**, **F1-score**, et **AUC** : Comparaison des performances entre modèles.
- Priorisation des modèles en fonction de la minimisation des faux négatifs.

---

##  Technologies utilisées

### Langages et Bibliothèques
- **Python** : Langage principal pour toutes les étapes du projet.
- **Bibliothèques** :
  - `NumPy`, `Pandas` : Préparation et analyse des données.
  - `Matplotlib`, `Seaborn` : Création de visualisations claires et informatives.
  - `Scikit-learn` : Implémentation des modèles de machine learning.
  - `TensorFlow` : Construction et entraînement du MLP.

---

##  Résultats et décision finale

- **Modèles baseline** :
  - Les résultats obtenus avec les modèles baseline sont encourageants et montrent leur potentiel pour détecter les clients à risque.
  - La **Régression Logistique** et le **MLP** ont des performances très proches, mais la Régression Logistique est privilégiée pour sa **simplicité** et sa capacité à minimiser efficacement les faux négatifs.

- **Modèle sélectionné** :
  - La **Régression Logistique** est retenue comme base pour les itérations futures, offrant un bon compromis entre performance, interprétabilité et facilité de déploiement.

---

##  Structure du projet

- `churn_prediction_model.ipynb` : Notebook principal contenant la modélisation et l'évaluation.
- `data_description.txt` : Description des colonnes et des données utilisées.
- `README.md` : Présentation générale du projet.
- `WA_Fn-UseC_-Telco-Customer-Churn.csv` : Fichier de données utilisé pour l'analyse.

---

## Prochaines étapes

Si le projet devait être approfondi, les pistes d'amélioration suivantes pourraient être envisagées :

1. **Tuning des hyperparamètres** :
   - Réaliser un ajustement plus précis des hyperparamètres pour chaque modèle afin d'optimiser les performances.

2. **Feature engineering** :
   - Travailler les features pour extraire des informations plus pertinentes ou créer de nouvelles variables explicatives.

3. **Déploiement** :
   - Mettre en place un pipeline complet pour intégrer les prédictions dans un environnement de production.
   - Développer une interface simple pour tester les modèles avec de nouvelles données.