# 🌸 Projet NLP - Classification de Revues de Parfums 🌸

## 📝 Objectif du Projet

Ce projet s'inscrit dans le cadre du cours de **Traitement Automatique des Langues et Applications (TALA540A)**. Le but est d'appliquer les compétences acquises en NLP (Natural Language Processing) à une tâche concrète en développant un modèle de classification des revues de parfums selon le genre de fragrance. 

➡️ Lien vers le [cours](https://github.com/RimeAB/TALA540A-24-25/tree/main).

## 👥 Membres du Groupe
- Jeevya AROUN
- Nicolas NGAUV  
- Anissa THEZENAS 

---

## 🌸 Sujet du Projet 
**Classification de revues de parfums selon le genre avec Support Vector Machine (SVM)**

### 📂 Corpus Utilisé
Notre corpus de données provient de [Fragrantica](https://www.kaggle.com/datasets/joehusseinmama/fragrantica-data), un site de référence pour les parfums, contenant des avis, descriptions et informations sur diverses fragrances. Ces données ont été partagées sur Kaggle par l'utilisateur *joehusseinmama*.

### 🎯 Tâche
La tâche consiste à classifier les avis de parfums en fonction du genre auquel le parfum est destiné : masculin, féminin ou unisexe. Ce projet utilise un algorithme de Support Vector Machine (SVM) pour cette tâche, mis en œuvre via la bibliothèque `sklearn`.

---

## ⚙️ Installation et Préparation

1. **Clonez** ce dépôt en local :
   ```bash
   git clone <url_du_repo>

2. **Téléchargez le corpus brut** depuis Kaggle :
   - Rendez-vous sur la page [Fragrantica Data sur Kaggle](https://www.kaggle.com/datasets/joehusseinmama/fragrantica-data).
   - Téléchargez le fichier `perfumes_table.csv`.
   - Placez le fichier téléchargé dans le dossier `../data/raw/`.

3. **Exécutez le Notebook de classification** :
   - Ouvrez le fichier `classifier.ipynb` dans Jupyter Notebook.
   - Exécutez les cellules une par une pour lancer le processus de prétraitement, l'entraînement du modèle et l'évaluation des résultats.

---

## 🗃️ Informations sur les Données

### Données Brutes
- **Fichier** : `perfumes_table.csv` (taille : 724,3 Mo).
- **Nombre total de parfums** : 84 144.
- **Champs** : 
  - `rating` : Note donnée au parfum (de 1 à 5).
  - `notes` : Liste des notes du parfum.
  - `designer` : Nom du créateur de la fragrance.
  - `reviews` : Liste des avis sur le parfum (certaines listes peuvent être vides).
  - `description` : Description textuelle du parfum.
  - `url` : Lien vers la page du parfum sur Fragrantica.
  - `title` : Nom complet du parfum incluant le genre (ex. : "Vanilla Scent Fiorucci for women and men").

### Données Nettoyées
Après prétraitement, les données sont stockées en format JSON, avec les informations suivantes pour chaque revue :
- `id` : Identifiant unique de la revue.
- `content` : Contenu textuel de la revue en soit les commentaires.
- `gender` : Genre associé au parfum.

**Prétraitement des Données** :
- Les termes indiquant le genre, comme "for men", "for women" et "unisexe", sont masqués pour éviter les biais de classification.
- Les classes sont équilibrées pour garantir un nombre équivalent de revues pour chaque catégorie de genre.

---

## 🏆 Utilisation de Kaggle

### Pourquoi Kaggle ?
Nous avons initialement envisagé de créer notre propre jeu de données en réalisant un script de scraping sur le site Fragrantica. Cependant, l’accès aux commentaires des utilisateurs n'était pas possible, ce qui nous a conduit à utiliser Kaggle pour obtenir un jeu de données pertinent. Cela nous a permis de concentrer nos efforts sur le traitement et l’analyse des données.

### Avantages de Kaggle dans les Projets NLP
Kaggle propose de nombreux jeux de données annotés et de ressources utiles, réduisant le temps nécessaire à la collecte des données et nous permettant de nous concentrer sur l'entraînement et l'optimisation de notre modèle NLP.

---

## 🔧 Technologies et Librairies Utilisées

- **Python** : Langage principal utilisé pour le développement du projet.
- **Pandas** : Bibliothèque utilisée pour la manipulation et le prétraitement des données.
- **Scikit-Learn (sklearn)** : Utilisé pour le modèle de classification SVM.
- **Jupyter Notebook** : Environnement pour l'écriture, l'exécution du code et la visualisation des résultats.

---

## 📊 Structure du Projet

### Fichiers Principaux
- `classifier.ipynb` : Contient le code pour l'entraînement et l'évaluation du modèle SVM.
- `readme.md` : Documentation du projet.
- `Project.ipynb` : Notebook additionnel pour les explorations et les analyses supplémentaires.

### Dossier de Données
- **Données Brutes** : Le fichier `perfumes_table.csv` doit être placé dans `../data/raw/`.
- **Données Nettoyées** : Les données nettoyées sont sauvegardées au format JSON pour l’entraînement.

---

## 🚀 Exécution et Résultats

Pour exécuter le projet :
1. Ouvrez le Notebook `classifier.ipynb`.
2. Suivez les étapes de prétraitement, d’entraînement et de validation pour construire et évaluer le modèle.
3. Les résultats finaux incluront des métriques de performance pour évaluer l'efficacité de la classification des genres de parfums.

---

## 💡 Résumé des Résultats

Le modèle SVM montre des résultats prometteurs pour la classification des genres de parfums en fonction des revues. Grâce à un prétraitement minutieux et à l'équilibrage des classes, le modèle est robuste et performant dans cette tâche de classification.

---

## 📚 Références et Ressources
- **Kaggle Dataset** : [Fragrantica Data](https://www.kaggle.com/datasets/joehusseinmama/fragrantica-data).
- **Documentation Scikit-Learn** : [SVM - sklearn](https://scikit-learn.org/stable/modules/svm.html).

---

Merci d'avoir exploré ce projet ! 😊 Nous espérons que ce travail offre des perspectives intéressantes pour les applications du NLP dans le domaine des avis et des descriptions de produits.