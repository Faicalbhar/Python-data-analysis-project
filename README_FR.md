# 📊 Analyse de Prêts Bancaires - Projet Data Science

## 📋 Table des Matières
1. [Présentation du Projet](#-présentation-du-projet)
2. [Objectifs](#-objectifs)
3. [Données Utilisées](#-données-utilisées)
4. [Méthodologie](#-méthodologie)
5. [Technologies Utilisées](#-technologies-utilisées)
6. [Installation](#-installation)
7. [Utilisation](#-utilisation)
8. [Résultats et Visualisations](#-résultats-et-visualisations)
9. [Structure du Projet](#-structure-du-projet)
10. [Auteur](#-auteur)

## 🎯 Présentation du Projet
Ce projet d'analyse de données porte sur l'étude d'un portefeuille de prêts bancaires. L'objectif est d'analyser les tendances, les risques et les performances des prêts accordés, en mettant en évidence des indicateurs clés pour la prise de décision.

## 🎯 Objectifs
- Analyser la distribution des prêts par différentes variables (durée, montant, taux d'intérêt, etc.)
- Évaluer la qualité du portefeuille (bons vs mauvais prêts)
- Identifier les facteurs influençant le remboursement des prêts
- Fournir des visualisations claires pour la prise de décision
- Démontrer des compétences en analyse de données avec Python

## 📊 Données Utilisées
Le jeu de données contient des informations sur 38 576 prêts avec les variables clés suivantes :
- **Données démographiques** : État, type de demande
- **Informations sur l'emprunteur** : Revenu annuel, score DTI (Debt-to-Income), ancienneté dans l'emploi
- **Détails du prêt** : Montant, taux d'intérêt, durée, échéance mensuelle
- **Statut du prêt** : En cours, remboursé, défaut de paiement
- **Historique de paiement** : Dernier paiement, prochaine échéance

## 🔍 Méthodologie
1. **Nettoyage des données** : Gestion des valeurs manquantes et formatage des variables
2. **Analyse exploratoire** : Statistiques descriptives et identification des tendances
3. **Visualisation** : Création de graphiques pour représenter les insights clés
4. **Analyse des performances** : Évaluation des indicateurs de performance clés (KPIs)

## 💻 Technologies Utilisées
- **Langage** : Python 3.8+
- **Bibliothèques principales** :
  - Pandas pour la manipulation des données
  - NumPy pour les calculs numériques
  - Matplotlib et Seaborn pour la visualisation
  - Plotly pour des graphiques interactifs
  - Jupyter Notebook pour l'analyse interactive

## 🛠️ Installation
1. Cloner le dépôt :
   ```bash
   git clone https://github.com/Faicalbhar/Python-data-analysis-project.git
   cd Python-data-analysis-project
   ```

2. Créer un environnement virtuel (recommandé) :
   ```bash
   python -m venv venv
   # Sur Windows :
   .\venv\Scripts\activate
   # Sur macOS/Linux :
   source venv/bin/activate
   ```

3. Installer les dépendances :
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Utilisation
1. Placer le fichier de données `financial_loan_data_excel.xlsx` dans un dossier `data/`
2. Lancer Jupyter Notebook :
   ```bash
   jupyter notebook
   ```
3. Ouvrir `Bank Loan Project.ipynb`
4. Exécuter les cellules dans l'ordre pour reproduire l'analyse

## 📈 Résultats et Visualisations

### 1. Vue d'ensemble du portefeuille
- **Montant total des prêts accordés** : 435,76 M$
- **Nombre total de prêts** : 38 576
- **Taux d'intérêt moyen** : 12,05%
- **Ratio DTI (Dette/Revenu) moyen** : 13,33%

### 2. Qualité du portefeuille
- **Prêts sains (remboursés ou en cours)** : 86,18%
- **Prêts à risque (défaut de paiement)** : 13,82%
- **Montant total reçu** : 473,07 M$

### 3. Analyses clés
- **Tendances mensuelles** des prêts accordés et remboursés
- Répartition géographique des prêts par État
- Analyse par durée de prêt (36 ou 60 mois)
- Impact de la situation professionnelle sur le remboursement
- Répartition par objet de prêt (consommation, rénovation, etc.)

## 📁 Structure du Projet
```
Python-data-analysis-project/
├── Bank Loan Project.ipynb  # Notebook d'analyse principal
├── README.md                # Documentation en anglais
├── README_FR.md             # Documentation en français
├── requirements.txt         # Dépendances Python
└── .gitignore              # Fichiers à ignorer par Git
```

