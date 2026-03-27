# SAÉ Apprentissage pour l'IA — BUT SD S6

Projet réalisé dans le cadre de la SAÉ Apprentissage pour l'IA (M. Métivier, IUT de Paris - Rives de Seine).  
Ce projet se découpe en deux études sur des données différentes, avec développement de modèles d'apprentissage profond.

## Auteurs

- Nathan Chan Sing Man
- Camille Franceschin
- Manohy Ratsimba

---

## Structure du projet

```
Winequality-CIFAR10-ML-Project/
├── data/                      # Données brutes (non versionnées)
│   └── winequality-white.csv
├── models/                    # Modèles entraînés .keras (non versionnés)
├── results/                   # Résultats sauvegardés .pickle (non versionnés)
├── notebooks/
│   ├── Winequality_ML.ipynb   # Étude 1 : Prédiction qualité des vins
│   └── CIFAR-10_ML.ipynb      # Étude 2 : Classification CIFAR-10
├── .gitignore
├── requirements.txt
├── README.md
└── livrables/                 # Livrables attendu pour le projet
    ├── Notebook_Winequality.html
    ├── Notebook_CIFAR10.html
    ├── Rapport_Winequality.pdf
    └── Rapport_CIFAR10.pdf
```
## Introduction 
Les réseaux de neurones constituent aujourd’hui l’un des piliers de l’intelligence artificielle. C’est cette technologie qui a rendu possibles les grands modèles de langage (LLM) et les systèmes d’IA que nous connaissons actuellement. Le principe repose sur un apprentissage statistique où l’ordinateur s’appuie sur des données antérieures pour apprendre à classifier, prédire ou encore effectuer des régressions sur des données futures.
Pour ce faire, le but est d’imiter le fonctionnement de l’intelligence humaine à travers des réseaux de neurones profonds, dits profonds car les neurones artificiels sont organisés en plusieurs couches successives où chaque couche prend le résultat de l’ancienne couche pour produire un résultat.

---

## Études

### Étude 1 — Prédiction de la qualité des vins
- **Dataset** : `winequality-white.csv` (P. Cortez et al., 2009)
- **Objectif** : Prédire la qualité d'un vin blanc à partir de ses propriétés physico-chimiques
- **Modèles** : MLP baseline (1 couche cachée, SGD) + MLP avancé (2 couches cachées, Adam, Dropout)
- **Métrique** : MAE (Mean Absolute Error)

### Étude 2 — Classification d'images CIFAR-10
- **Dataset** : CIFAR-10 (via `keras.datasets`)
- **Objectif** : Classifier des images en 10 catégories
- **Modèles** : MLP baseline + CNN avec filtres (3x3) et (5x5) + Data Augmentation
- **Métrique** : Accuracy

---

## Installation

### 1. Cloner le dépôt

```bash
git clone <url-du-repo>
cd Winequality-CIFAR10-ML-Project
```

### 2. Créer et activer l'environnement virtuel

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

### 3. Installer les dépendances

```bash
pip install -r requirements.txt
```


---

## Utilisation

Ouvrir les notebooks : 

1. `notebooks/etude1_vins.ipynb`
2. `notebooks/etude2_cifar10.ipynb`

> ⚠️ Les modèles `.keras` et résultats `.pickle` sont sauvegardés automatiquement dans `models/` et `results/`. Au prochain lancement, ils sont rechargés sans réentraînement.

---

## Dépendances principales

| Bibliothèque | Usage |
|---|---|
| `tensorflow` / `keras` | Construction et entraînement des modèles |
| `numpy` | Manipulation des données |
| `pandas` | Chargement et exploration des données |
| `matplotlib` | Visualisation des résultats |
| `scikit-learn` | Prétraitement (normalisation, split) |

---

## Rendu

- **Date limite** : 27 mars 2026
- **Plateforme** : Moodle
- **Fichiers à rendre** : 2 notebooks + 2 rapports PDF
