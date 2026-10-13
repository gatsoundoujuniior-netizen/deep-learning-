# Réseaux de neurones & Deep Learning

Implémentations pas à pas d'algorithmes de deep learning avec **PyTorch**, sous forme de notebooks Jupyter.

L'objectif est d'apprendre en codant : chaque notebook part des bases (tenseurs, gradients) pour aller vers des modèles plus complexes.

## Contenu

| Notebook | Sujet |
|---|---|
| [lab1.ipynb](lab1.ipynb) | Prise en main de PyTorch : tenseurs, formes, GPU (CUDA) |
| [regression.ipynb](regression.ipynb) | Régression linéaire avec `torch.nn` sur des données bruitées |

D'autres algorithmes seront ajoutés au fur et à mesure (réseaux denses, CNN, RNN, etc.).

## Installation

Le projet utilise [uv](https://docs.astral.sh/uv/) et Python 3.12.

```bash
git clone https://github.com/<ton-pseudo>/reseaux_de_neuronnes.git
cd reseaux_de_neuronnes
uv sync
```

Ouvre ensuite un notebook dans VS Code ou Jupyter et sélectionne le kernel `.venv`.

## Technologies

- Python 3.12
- PyTorch
- NumPy
- Matplotlib
- Jupyter
