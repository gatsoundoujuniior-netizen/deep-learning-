# Réseaux de neurones & Deep Learning

Implémentations pas à pas d'algorithmes de deep learning avec **PyTorch**, sous forme de notebooks Jupyter.

L'objectif est d'apprendre en codant : chaque notebook part des bases (tenseurs, gradients) pour aller vers des modèles plus complexes.

## Contenu

| Notebook | Sujet |
|---|---|
| [lab1.ipynb](lab1.ipynb) | Prise en main de PyTorch : tenseurs, formes, GPU (CUDA) |
| [regression.ipynb](regression.ipynb) | Régression linéaire avec `torch.nn` sur des données bruitées |

D'autres algorithmes seront ajoutés au fur et à mesure (réseaux denses, CNN, RNN, etc.).

## Ce qui a été travaillé

### Lab 1 : les bases de PyTorch

- **Tenseurs** : création (`torch.tensor`, `torch.zeros`, `torch.randn`), forme (`shape`) et type des données (`dtype`), conversion en `float32`
- **GPU** : vérification de CUDA et déplacement des tenseurs sur le bon appareil (`cuda` ou `cpu`)
- **Calcul matriciel** : produit de matrices avec l'opérateur `@`
- **Calcul du gradient** : différentiation automatique avec `requires_grad`, `loss.backward()` et `torch.autograd.grad`, sur l'exemple d'une perte `(w*x + b - 10)²`

### Régression linéaire

- **Données synthétiques** : 50 points générés selon `y = 3x + 2`, avec du bruit gaussien
- **Modèle** : une couche `nn.Linear(1, 1)`
- **Entraînement** : 1000 époques avec la perte `MSELoss` et l'optimiseur `Adam` (learning rate 0,01)
- **Évaluation** : affichage de la droite prédite sur les données, courbe de la perte pendant l'entraînement et score **R²** avec `torcheval`

## Installation

Le projet utilise [uv](https://docs.astral.sh/uv/) et Python 3.12.

```bash
git clone https://github.com/<ton-pseudo>/reseaux_de_neuronnes.git
cd reseaux_de_neuronnes
uv sync
```

Installe ensuite les bibliothèques nécessaires :

```bash
uv add torch numpy matplotlib torcheval
```

> Pour utiliser le GPU (NVIDIA), installe la version CUDA de PyTorch en suivant les instructions sur [pytorch.org](https://pytorch.org/get-started/locally/).

Ouvre ensuite un notebook dans VS Code ou Jupyter et sélectionne le kernel `.venv`.

## Technologies

- Python 3.12
- PyTorch
- NumPy
- Matplotlib
- Jupyter
