# Examen de Projet NLP

## Objectif du projet

Le projet final de ce [cours](https://github.com/RimeAB/TALA540A-24-25/tree/main) consiste à travailler en groupe pour appliquer les compétences acquises à une tâche concrète en TAL. Vous devrez choisir et analyser un corpus, choisir une tâche et un outil, puis proposer une solution qui sera évaluée selon plusieurs critères.

## Membre du groupe 
- Jeevya AROUN
- Nicolas NGAUV  
- Anissa THEZENAS 

## Sujet du projet 
**🌸 Classification de revues de parfums selon le genre avec SVM 🌸**
- Notre corpus : données de fragrantica.com dont les reviews de parfums et le genre auquel est destiné le parfum (crée par joehusseinmama sur Kaggle)
- Notre tâche :  Classification de revues de parfums selon le genre
- L'algo de classification utilisé : SVM à l'aide de la librairie sklearn

### Usage
- clone git repo
- download raw corpus from joehusseinmama/fragrantica-data on Kaggle 
	- https://www.kaggle.com/datasets/joehusseinmama/fragrantica-data
	- place the file perfumes_table.csv in ../data/raw/
- run classifier.ipynb

### Some info on the raw data
- csv file (724,3 Mo) found on Kaggle (joehusseinmama/fragrantica-data)
- 84144 fragrances in total

- fields : 
	- rating (1 to 5)
	- notes (list)
	- designer
	- reviews (list), some lists are empty
	- description
	- url
	- title (title + gender) ex: "Vanilla Scent Fiorucci for women and men" or "Laura Nina's Nature for women"

### Clean data
- json format
- for each review we have :
	- id
	- text content of the review
	- gender (split on the title)
- words like "for men", "for women", "unisexe" etc. will be masked from reviews to avoid bias
- all classes will have the same nb of reviews
