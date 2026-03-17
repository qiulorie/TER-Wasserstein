# TER-Wasserstein
# Projet TER : Optimisation de Mixture Gaussienne par Transport Optimal
##DISCLAIMER: the repo has no commits as the ORIGINAL repo is private, as the teacher wanted. This is only a public copy.
## Description
Ce projet s'inscrit dans le cadre d'un Travail d'Étude et de Recherche (TER). Il explore l'utilisation du transport optimal, et plus précisément de la distance de Wasserstein, pour ajuster et optimiser les paramètres d'une Mixture Gaussienne (GMM) en deux dimensions. 

## Étapes du projet
1. **Génération des données :** Création d'une distribution cible sous forme d'un nuage de points 2D à partir d'une GMM simulée.
2. **Estimation initiale (Algorithme EM) :** Utilisation de l'algorithme Espérance-Maximisation pour ajuster une première GMM sur les données générées et trouver les paramètres de base.
3. **Optimisation des poids :** Ajustement des poids des clusters de la distribution source pour se rapprocher de la cible, en minimisant la distance de Wasserstein via une descente de gradient.
4. **Optimisation des moyennes :** Ajustement des moyennes des clusters à l'aide de l'astuce de reparamétrisation (reparametrization trick) et d'une approche de Monte Carlo pour rendre le processus différentiable.
5. **Optimisation conjointe :** Ajustement global des paramètres (poids, moyennes et covariances) pour minimiser l'écart entre le modèle et la cible.

## Technologies utilisées
- **Python** - **PyTorch** (pour le calcul des gradients et l'optimisation)
- **POT (Python Optimal Transport)** (pour le calcul de la distance de Wasserstein)
- **Scikit-learn** (pour l'algorithme EM via GaussianMixture)
- **NumPy & Matplotlib** (pour la manipulation des tenseurs/tableaux et la visualisation)

## Utilisation
Le code est entièrement contenu dans le notebook `TER_wasserstein.ipynb`. Il suffit d'exécuter les cellules de manière séquentielle pour générer les données, observer l'estimation EM, puis suivre l'évolution de la fonction de perte (loss) lors de l'optimisation des différents paramètres par transport optimal.
