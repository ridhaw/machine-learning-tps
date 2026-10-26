# Machine learning, deep learning et data mining — travaux pratiques

Notebooks Python réalisés sur Google Colab pendant mon cursus universitaire : vision par
ordinateur, analyse de données, apprentissage supervisé et non supervisé, réseaux de
neurones et graphes.

## Sommaire

| # | Notebook | Thème | Points clés |
|---|---|---|---|
| 01 | [Traitement d'image avec OpenCV](notebooks/01_vision_traitement_image_opencv.ipynb) | Vision | Lecture d'image, dimensions, canaux, nombre de pixels |
| 02 | [Analyse du dataset Heart Disease](notebooks/02_analyse_donnees_heart_disease.ipynb) | Analyse de données | Statistiques descriptives, équilibre des classes, valeurs manquantes et invalides, analyses groupées |
| 03 | [Visualisation et prétraitement — Titanic](notebooks/03_visualisation_et_pretraitement.ipynb) | Data mining | Visualisation, nettoyage, règles d'association (Apriori) |
| 04 | [Arbre de décision — Iris](notebooks/04_arbre_de_decision_iris.ipynb) | Supervisé | Split 70/30, visualisation de l'arbre, rapport de classification, matrice de confusion — accuracy 100 % en test (45 échantillons) |
| 05 | [Clustering K-Means — Iris](notebooks/05_clustering_kmeans_iris.ipynb) | Non supervisé | Exploration, normalisation, choix de k, comparaison aux vraies classes — jusqu'à 89,3 % de correspondance |
| 06 | [Classification d'images par KNN](notebooks/06_classification_images_knn.ipynb) | Vision / supervisé | Chargement d'images, préparation, KNN — 63,3 % → 66,7 % après préparation |
| 07 | [Autoencodeurs — détection de spam](notebooks/07_autoencodeurs_detection_spam.ipynb) | Deep learning | TF-IDF, autoencodeurs simple, profond et empilé, comparaison des MSE, classification MLP sur les représentations compressées |
| 08 | [Graphes avec NetworkX](notebooks/08_graphes_networkx.ipynb) | Algorithmique | Construction et dessin de graphes |

## Stack

Python · pandas · NumPy · scikit-learn · TensorFlow / Keras · OpenCV · matplotlib ·
seaborn · SciPy · NetworkX · apyori

## Exécuter

Les notebooks ont été écrits pour Google Colab : ils montent Google Drive
(`drive.mount('/content/drive')`) et lisent les données depuis `/content/drive/MyDrive/...`.
Pour les lancer ailleurs, remplacer ces chemins par l'emplacement local des datasets
(Iris, Titanic, Heart Disease Cleveland, SMS Spam). Les datasets ne sont pas inclus.

```bash
pip install -r requirements.txt
jupyter notebook notebooks/
```

## À noter

Dans le TP 07, la dernière étape (classification MLP sur les représentations compressées)
échoue à l'évaluation : `classification_report` reçoit une seule classe alors que deux
noms de classes sont attendus. Elle reste à corriger.
