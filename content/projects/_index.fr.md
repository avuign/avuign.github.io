---
title: "Projets"
---

## Machine Learning

### Réseau de neurones from scratch en NumPy

Un perceptron multicouche codé entièrement en NumPy : forward pass, backpropagation et SGD sont implémentés from scratch, sans aucun framework. L'objectif était de comprendre l'atome du deep learning : ce qui se passe exactement quand un réseau apprend. C'est aussi utile d'avoir une implémentation entièrement maîtrisée pour comprendre ce que le framework fait sous le capot quand j'utilise PyTorch. Le même dépôt contient également un CNN construit avec JAX/Flax et Optax à titre de comparaison, atteignant ~95% de précision sur le jeu de test.

**Stack :** Python, NumPy, JAX, Flax, Optax

[GitHub](https://github.com/avuign/MNIST)

---

### Pipeline de distillation de connaissances

Un modèle character-level qui apprend la structure statistique de prénoms anglais et en génère de nouveaux. L'architecture de base est une couche d'embedding suivie d'un MLP. En plus de l'entraînement standard, j'ai implémenté un pipeline de distillation teacher-student : un modèle teacher plus grand est d'abord entraîné, puis un modèle student plus petit est entraîné à reproduire la distribution de sortie du teacher via une loss de divergence KL.

Le modèle student entraîné sur les soft targets a obtenu des performances comparables à un modèle entraîné directement sur les données avec la même architecture, ce qui suggère qu'à cette échelle la distribution de sortie du teacher ne contient pas significativement plus d'information que les hard labels. Une suite naturelle serait de tester sur une architecture plus profonde, où les représentations internes du teacher sont plus riches et où l'écart entre hard et soft targets devrait être plus marqué.

**Stack :** Python, PyTorch

[GitHub](https://github.com/avuign/char_lm)

---

### Transformer language model from scratch

Travail en cours. Je construis un language model de type GPT from scratch en PyTorch. L'objectif est d'implémenter le pipeline complet de bout en bout : tokenization BPE, multi-head attention, pretraining et génération de texte. Complétion prévue : été 2026.

**Stack :** Python, PyTorch

[GitHub](https://github.com/avuign/femto_chatbot)

---

## Recherche en physique

### Pourquoi la gravité émerge-t-elle de matrices ?

Le modèle IKKT ne décrit pas le monde réel, mais c'est précisément là que réside son intérêt. C'est un modèle jouet, suffisamment simple pour être étudié en détail, qui possède une propriété remarquable : un système statistique de matrices en interaction, pas si différent d'un gaz de particules, se réorganise à grand N en une théorie d'espace-temps dynamique obéissant aux équations d'Einstein. La vraie question est : pourquoi ? Qu'est-ce que les interactions ont de particulier pour que cela se produise ?

Un angle d'attaque concret consiste à intégrer une partie de la matrice. On part d'une matrice (N+k) × (N+k) et on intègre sur le bloc N × N, en laissant k entrées intactes. Le résultat est une action effective pour les degrés de liberté restants, qui devrait décrire k D-instantons se propageant dans la géométrie générée par les N autres. On ne peut pas évaluer cette intégrale exactement, mais on peut écrire les équations que cette action effective doit satisfaire. Pour un modèle de matrices générique, ces équations forment une hiérarchie infinie couplée (similaire aux équations de boucle). L'observation clé est que pour les modèles holographiques comme IKKT, la hiérarchie devrait tronquer : dans les bonnes variables, la tour infinie s'effondre en un ensemble fini d'équations qui reproduisent la relativité générale. Comprendre quelle propriété des interactions est responsable de cette troncation est, à mon avis, la question ouverte centrale dans ce domaine.
