
## Description
Ce projet implémente un réseau de neurones multicouche (MLP) en **NumPy pur**, avec backpropagation, descente de gradient stochastique et fonctions d'activation ReLU, sigmoïde et softmax. Il inclut également une comparaison des performances avec `scikit-learn`, une optimisation des hyperparamètres, ainsi qu'une application aux jeux de données MNIST et CIFAR-10. La dernière partie introduit les réseaux de neurones convolutifs (CNN) avec Keras pour illustrer leurs avantages sur des données images complexes.

## Contenu du notebook
- **Partie 1** – Implémentation d’un MLP from scratch (classification sur Iris)
- **Partie 2** – Comparaison avec `MLPClassifier` de `scikit-learn`
- **Partie 3** – Optimisation des hyperparamètres (taux d’apprentissage, architecture)
- **Partie 4** – Application à MNIST : MLP from scratch vs `scikit-learn`
- **Partie 5** – CIFAR-10 : limites du MLP et introduction aux CNN
- **Partie 6** – Implémentation d’un CNN simple avec Keras

## Installation
Pour exécuter le notebook en local, vous aurez besoin des bibliothèques suivantes :

```bash
pip install -r requirements.txt