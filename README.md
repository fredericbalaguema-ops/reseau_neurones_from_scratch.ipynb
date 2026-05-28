# Réseau de Neurones Multicouche — From Scratch

![Python](https://img.shields.io/badge/Python-3.10-blue)
![NumPy](https://img.shields.io/badge/NumPy-only-orange)
![MIT License](https://img.shields.io/badge/License-MIT-green)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1WU8zWtLvovyLx6jfZO7kj4AhrAPMRNMG?usp=sharing)
[![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20BEFF)](https://www.kaggle.com/code/fredericbalaguema/reseau-neurones-from-scratch)

> **Stage MI3 — Thème 9 | FAST Natitingou | Laboratoire IA CAEB / Fondation VALLET | 2025-2026**  
> Étudiant : **Frédéric BALAGUEMA**

---

## Description

Ce projet implémente un réseau de neurones multicouche (MLP) en **NumPy pur**, sans aucun framework de deep learning (pas de TensorFlow, pas de PyTorch). Il couvre l'intégralité du pipeline d'apprentissage : propagation avant, rétropropagation du gradient (backpropagation), descente de gradient stochastique (SGD) et initialisation Xavier.

Le réseau est appliqué à trois problèmes de classification de complexité croissante : **Iris** (données tabulaires), **MNIST** (images de chiffres) et **CIFAR-10** (photos couleur). Une extension introduit les réseaux convolutifs (CNN) avec Keras pour illustrer les limites du MLP sur des images complexes.

---

## Résultats obtenus

| Dataset | Modèle | Accuracy TEST |
|---------|--------|--------------|
| Iris | MLP from scratch (NumPy) | **96.7%** |
| Iris | MLPClassifier scikit-learn | **96.7%** |
| MNIST | MLP from scratch (NumPy) | **91.9%** |
| MNIST | MLPClassifier scikit-learn | **95.9%** |
| CIFAR-10 | MLP from scratch (NumPy) | **33.8%** |
| CIFAR-10 | CNN Keras | **67.7%** |

**Gradient check validé :** différence relative = 6.57 × 10⁻¹¹ (backpropagation mathématiquement exacte)

---

## Contenu du notebook

- **Partie 1** — Implémentation MLP from scratch (classification Iris)
- **Partie 2** — Comparaison avec `MLPClassifier` de scikit-learn
- **Partie 3** — Analyse des hyperparamètres (learning rate, architecture, underfitting/overfitting)
- **Partie 4** — Application à MNIST : MLP from scratch vs scikit-learn
- **Partie 5** — CIFAR-10 : limites du MLP et introduction aux CNN
- **Partie 6** — CNN avec Keras sur CIFAR-10

---

## Architecture implémentée

```
Fonctions from scratch (NumPy uniquement) :
  sigmoid, relu, softmax + dérivées
  initialize_parameters  (initialisation Xavier/He)
  forward_propagation    (avec cache pour backprop)
  compute_loss           (cross-entropy binaire et multi-classes)
  backward_propagation   (backprop complète)
  update_parameters      (SGD)
  model                  (boucle d'entraînement)
  predict, compute_accuracy
```

---

## Installation

```bash
pip install -r requirements.txt
```

Ou exécuter directement en ligne :

| Plateforme | Lien |
|-----------|------|
| Google Colab | [Ouvrir dans Colab](https://colab.research.google.com/drive/1WU8zWtLvovyLx6jfZO7kj4AhrAPMRNMG?usp=sharing) |
| Kaggle | [Voir sur Kaggle](https://www.kaggle.com/code/fredericbalaguema/reseau-neurones-from-scratch) |

---

## Structure du dépôt

```
reseau_neurones_from_scratch.ipynb   ← notebook principal
requirements.txt                      ← dépendances
README.md
figures/
  courbe_loss_accuracy.png
  comparaison_from_scratch_vs_sklearn.png
  analyse_learning_rate.png
  analyse_architecture.png
  underfitting_overfitting.png
  mnist_exemples.png
  mnist_resultats.png
  mnist_erreurs.png
  cifar10_exemples.png
  cnn_vs_mlp_cifar10.png
  cnn_predictions.png
```

---

## Technologies utilisées

- **Python 3.10**
- **NumPy** — calculs matriciels (MLP from scratch)
- **Matplotlib / Seaborn** — visualisations
- **scikit-learn** — comparaison et preprocessing
- **TensorFlow / Keras** — CNN (extension)
- **Jupyter Notebook** — environnement de développement

---

## Auteur

**Frédéric BALAGUEMA**  
Étudiant MI3 — FAST Natitingou  
📧 fredericbalaguema@gmail.com  
🌐 [GitHub](https://github.com/Fredericbalaguema-Ops)  
📊 [Kaggle](https://www.kaggle.com/fredericbalaguema)

---

## Licence

MIT License — voir le fichier `LICENSE`
