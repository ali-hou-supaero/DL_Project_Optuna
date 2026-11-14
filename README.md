# Optuna — Optimisation automatique des hyperparamètres

Démonstration pédagogique par **Ali Houssenaly**, préparée dans le cadre de la SDD à SUPAERO, montrant comment Optuna sélectionne des modèles et optimise leurs hyperparamètres.

## Démonstrations

1. **Machine learning classique sur Fashion-MNIST** : sélection entre SVC, Random Forest et Gradient Boosting, avec un objectif d’accuracy.
2. **Réseaux de neurones sur Fashion-MNIST** : optimisation de l’architecture d’un réseau feedforward, du dropout, de l’optimiseur et du taux d’apprentissage.
3. **Extension au hackathon heart-risk** : optimisation de CatBoost avec un objectif F1.

Le [notebook](demo_code.ipynb) implémente les études Optuna, les espaces de recherche et leur visualisation. Les résultats numériques enregistrés et les comparaisons au classement sont des observations historiques, et non des benchmarks réexécutés indépendamment.

## Contenu

- [demo_code.ipynb](demo_code.ipynb) — démonstration complète.
- [Présentation](DL_Project_Optuna_Presentation.pdf) — diapositives associées.
- [Article Optuna](optuna_paper.pdf) — document de référence, dont le crédit revient à ses auteurs.

## Installation et données

Utiliser Jupyter avec Python, Optuna, scikit-learn, NumPy, pandas, PyTorch, torchvision et CatBoost. Le notebook importe également les modules d’intégration CatBoost et de visualisation d’Optuna ; installer les dépendances compatibles avec la version d’Optuna choisie. Les versions des dépendances ne sont pas verrouillées dans ce dépôt.

Fashion-MNIST nécessite un accès aux données et leur téléchargement. Pour la troisième démonstration, télécharger les données originales du hackathon depuis le [dossier Google Drive partagé](https://drive.google.com/drive/folders/106h8NLhxBq4la_aS8UOWMZ1iu9fthQ5i?usp=drive_link). L’accès à ce dossier externe n’a pas été vérifié.

Placer les fichiers comme suit :

```text
DL_Project_Optuna/
├── demo_code.ipynb
├── DL_Project_Optuna_Presentation.pdf
├── optuna_paper.pdf
└── mini-hackathon-data/
    ├── train.csv
    └── test.csv
```

Lancer Jupyter depuis la racine du dépôt et exécuter les cellules dans l’ordre. Vérifier le nombre d’essais avant de lancer une étude : la durée dépend du matériel, des données et de l’espace de recherche. La troisième partie nécessite les données supplémentaires du hackathon.

## Reproductibilité et périmètre

Il s’agit d’une démonstration pédagogique plutôt que d’un service d’optimisation en production. Aucun test automatisé ni environnement verrouillé et vérifié n’est fourni. Pour prolonger les expériences, séparer l’entraînement, la sélection des hyperparamètres et l’évaluation finale sur le jeu de test.
