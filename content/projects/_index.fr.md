---
title: "Projets"
---

## Machine Learning

### Modèle de langage Transformer de zéro

Un Transformer au niveau des mots, entraîné sur Shakespeare, construit de zéro en PyTorch. Le modèle implémente l'attention multi-têtes, l'encodage positionnel, les connexions résiduelles et la LayerNorm. La tokenisation, la boucle d'entraînement et la génération de texte sont entièrement écrites à la main. Entraîné sur CPU.

**Stack :** Python, PyTorch

[GitHub](https://github.com/avuign/femto_chatbot)

---

### Modèle de langage caractère par caractère avec distillation

Un modèle au niveau des caractères qui apprend la structure statistique de prénoms anglais et en génère de nouveaux. L'architecture de base est une couche d'embedding suivie d'un MLP. En plus de l'entraînement standard, j'ai implémenté un pipeline de distillation teacher-student : un modèle teacher plus grand est entraîné en premier, puis un modèle student plus petit est entraîné à reproduire la distribution de sortie du teacher via une loss de divergence KL.

**Stack :** Python, PyTorch

[GitHub](https://github.com/avuign/char_lm)

---

### Classification de chiffres MNIST

Deux implémentations de classification de chiffres sur MNIST, dans le même dépôt. La première est un perceptron multicouche codé entièrement en NumPy : passe forward, rétropropagation et SGD sont implémentés from scratch, sans aucun framework. La seconde est un réseau de neurones convolutif construit avec JAX/Flax et Optax, atteignant ~95% de précision sur le jeu de test.

**Stack :** Python, NumPy, JAX, Flax, Optax

[GitHub](https://github.com/avuign/MNIST)

---

## Recherche en physique

### Pourquoi la gravité émerge-t-elle de matrices ?

Le modèle IKKT ne décrit pas le monde réel, mais c'est un modèle suffisamment simple pour être étudié en détail, qui exhibe une propriété remarquable : un système statistique de matrices en interaction, quelque chose qui n'est pas si différent d'un gaz de particules, se réorganise à grand N en une théorie de l'espace-temps dynamique obéissant aux équations d'Einstein. La vraie question est : pourquoi. Qu'est-ce que les interactions ont de particulier pour que cela se produise ?

Un angle d'attaque concret consiste à intégrer une partie de la matrice. On part d'une matrice (N+k) × (N+k) et on intègre le bloc N × N, en laissant k entrées non intégrées. Le résultat est une action effective pour les degrés de liberté restants, qui devrait décrire k D-instantons se propageant dans la géométrie engendrée par les N autres. On ne peut pas évaluer cette intégrale exactement, mais on peut écrire les équations que cette action effective doit satisfaire. Pour un modèle matriciel générique, ces équations forment une hiérarchie infinie couplée (similaire aux équations de boucle). L'observation clé est que pour les modèles holographiques comme IKKT, la hiérarchie devrait tronquer : dans les bonnes variables, la tour infinie se réduit à un ensemble fini d'équations qui reproduisent la relativité générale. Comprendre quelle propriété des interactions est responsable de cette troncation est, à mon avis, la question ouverte centrale dans ce domaine.
