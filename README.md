**- Projet de Classification Automatique de Produits pour "Les Bonnes Affaires"**
*Contexte*
La startup Les Bonnes Affaires est une marketplace en ligne où des particuliers peuvent vendre leurs produits en postant une description, une photo, et en choisissant une catégorie. Cependant, cette approche manuelle s'avère peu fiable, avec de nombreux produits mal classés. Pour améliorer cette situation, la direction souhaite automatiser la classification des produits en s’appuyant sur le pôle Data.

Vous, en tant que Data Scientist, avez été chargé de réaliser une preuve de concept (PoC) pour évaluer la faisabilité d'un modèle de classification automatique basé sur les descriptions textuelles et les images des produits. Ce PoC permettra d’évaluer la précision d’un modèle multi-inputs combinant NLP et vision par ordinateur.

**Objectifs**
*Étape 1 :* Développer un modèle de classification basé sur le texte des descriptions des produits. Utiliser un modèle de NLP tel qu'un transformer.
*Étape 2 :* Développer un modèle basé uniquement sur les images des produits, en utilisant un réseau de neurones convolutifs (ConvNet) pré-entraîné sur ImageNet (EfficientNet, VGG, Inception, etc.).
*Étape 3 :* Combiner les deux modèles en une architecture multi-inputs, permettant de capturer simultanément les informations textuelles et visuelles.
Chaque approche sera évaluée individuellement en termes de précision et de temps d’entraînement.

**Architecture Multi-Inputs**
Une architecture multi-inputs utilise plusieurs sources d’information pour des prédictions plus précises. Dans ce projet, nous combinons :

Un modèle NLP (par exemple, un transformer) pour traiter les descriptions textuelles des produits.
Un modèle ConvNet pour analyser les images.
Les couches softmax de chaque modèle sont retirées, et les vecteurs de caractéristiques générés sont concaténés en une représentation unifiée. Cette combinaison permet de capturer les informations des descriptions et des images, améliorant ainsi la précision de la prédiction de catégorie.

**Données**
L’échantillon de données fourni pour ce projet comprend :

1050 articles avec descriptions textuelles et images.
Données d'entraînement limitées pour réduire les coûts de calcul et accélérer le processus d'entraînement.
Remarque : Les métriques de précision et le temps d'entraînement peuvent varier en fonction du random_state. Un fine-tuning modéré est conseillé, étant donné la taille réduite de l'échantillon.

**Outils Recommandés**
Notebook Colab (ou un équivalent) pour un environnement flexible et partageable.
Keras pour le développement des algorithmes, avec une préférence pour le transfer learning pour optimiser l’entraînement.
Instructions de Mise en Production
Si le modèle s’avère concluant, voici quelques étapes pour sa mise en production :

*Architecture :* Entraîner un modèle multi-inputs sur un jeu de données plus volumineux pour obtenir une meilleure robustesse.
*Outils :* Utiliser un environnement de production plus optimisé, tel que TensorFlow Serving, pour déployer le modèle.
*Scalabilité :* Prévoir une infrastructure permettant le scaling horizontal pour gérer de grands volumes de données.
**Bonus**
Développer une API pour faciliter l’intégration de ce modèle dans le produit final.

**Livrables**
Notebook commenté détaillant chaque étape du projet, du preprocessing au modèle multi-inputs final.
[Optionnel] API pour intégrer le modèle dans un pipeline de production.
**Modalités**
Travail en solo ou en binôme
**Outils :** Libre choix d’outils, mais la correction sera faite avec Keras.
**Durée estimée :** 4 jours
Ce projet permettra de valider la faisabilité d’une solution de classification automatique pour Les Bonnes Affaires, en s'appuyant sur des techniques modernes de NLP et de vision par ordinateur.