Projet Challenge Rakuten 
==============================


Installation des paquets sous Windows (avec support GPU)
------------

###  1. Pour les modèles baseline et Tensorflow : 


Pour installer les requirements avec Windows et pour pouvoir utiliser la puissance de calcul de votre GPU, voici la démarche à suivre :

Créer un environnement avec conda :
```
conda create --name rakuten_project_tf python=3.10
```

Installer les packages CUDA et CuDNN compatibles avec Windows pour le support GPU pour Tensorflow :
```
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
```

Installer tous les paquets nécessaires :
```
pip install --upgrade pip
pip install -r requirements.txt
```

### 2. Pour les modèles Pytorch : 

Pour installer les requirements avec Windows et pour pouvoir utiliser la puissance de calcul de votre GPU, voici la démarche à suivre :

Créer un environnement avec conda :
```
conda create --name rakuten_project_torch python=3.10
```

Installer les packages compatibles avec Windows pour le support GPU pour Torch :
```
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
conda install -c conda-forge accelerate
```

Installer tous les paquets nécessaires :
```
pip install --upgrade pip
pip install -r requirements_torch.txt
```



# Classification de produits

Ce projet a pour objectif de classifier des produits en 27 catégories en utilisant une photo et une description texte provenant d'un site de vente d'objets en ligne. Pour ce faire, nous disposons d'un dataset de 80 000 images accompagné de leurs descriptions textuelles.

### Les étapes

1. **Analyse du Dataset** : 
   - Examiner la structure des données.
   - Échantillonnage des données.

2. **Entraînement de Modèles de Machine Learning** : 
   - Entraîner plusieurs modèles de machine learning.
   - Comparer ces modèles avec un modèle de référence (baseline).
   - Appliquer des techniques de prétraitement :
     - Filtres d'images avec OpenCV.
     - Vectorisation du texte avec NLTK.
   - Utiliser des techniques de réduction de dimensions pour améliorer les performances des modèles.

3. **Équilibrage des Données** :
   - Utiliser des techniques d'undersampling et d'oversampling.

4. **Utilisation du Deep Learning et des Transformers** :
   - Expérimenter avec plusieurs modèles de deep learning.
   - Utiliser des transformers pour améliorer les résultats.

## Notebooks Utilisés

Voici la liste des notebooks utilisés dans ce projet :

1. **preprocessing.ipynb** : Prétraitement des données.
2. **resize_sort_images.ipynb** : Redimensionnement et tri des images.
3. **baseline_models_general.ipynb** : Modèles de référence généraux.
4. **baseline_models_images_filters.ipynb** : Modèles de référence avec filtres d'images.
5. **tensorflow_models_images.ipynb** : Modèles TensorFlow pour les images.
6. **tensorflow_models_text.ipynb** : Modèles TensorFlow pour le texte.












