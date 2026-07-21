# Résolution d'une EDP elliptique par éléments finis

Résolution numérique de l'équation `-Δu = f` (puis `-Δu + c0·u = f`) sur le domaine `]0,1[×]0,1[`, par la méthode des éléments finis P1/Q1, avec conditions aux limites de Dirichlet et Neumann.

## Contenu

Le projet est un notebook unique (`projet.ipynb`), organisé en parties progressives :

1. **Maillage triangulaire et conditions de Dirichlet** — matrice de raideur élémentaire P1 sur un maillage de triangles, assemblage du système linéaire, résolution avec conditions de Dirichlet homogènes.
2. **Maillage mixte et conditions de Neumann** — extension à un maillage combinant triangles et quadrangles (éléments Q1), ajout des conditions de Neumann sur une partie du bord.
3. **Complément : terme supplémentaire c0·u** — formulation variationnelle et résolution de `-Δu + c0·u = f`, avec construction d'une matrice de masse élémentaire en complément de la matrice de raideur.

Chaque partie contient les fonctions de calcul (matrices élémentaires, assemblage), la résolution du système linéaire (scipy.sparse), et la visualisation de la solution sur le maillage.

## Installation

git clone <url-du-repo>
cd EDP_HARAKA_FADEL
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

Testé avec Python 3.14.

## Exécution

Ouvrir `projet.ipynb` dans Jupyter ou VS Code, sélectionner l'environnement `.venv` comme kernel, puis exécuter les cellules dans l'ordre (Run All).

jupyter notebook projet.ipynb

## Auteurs

Hiba HARAKA & Salma FADEL — ENSEEIHT (N7/INP Toulouse)
