# Test technique Datapool

## Question 1
En shell, charger les fichiers *file_1.csv* et *file_2.csv* à la racine du bucket GCS `gs://auchan-itcorp-dev_dc_fallou/`.

## Question 2
Créer un fichier *main.py* qui permet de réaliser les actions suivantes :

### Question 2.1
Chargement du fichier *file_1.csv* depuis GCS vers BigQuery. Le fichier sera à charger dans le projet `auchan-itcorp-dev` dans le dataset `test_fallou`, dans une table qu'il faudra nommer `store` et dont le schéma sera auto-généré.

### Question 2.2
Chargement du fichier *file_2.csv* depuis GCS vers BigQuery. Le fichier sera à charger dans le projet `auchan-itcorp-dev` dans le dataset `test_fallou`, dans une table qu'il faudra nommer `turnover` et dont le schéma respectera les spécifications ci-dessous :
   - 1er champ : 
     - Nom : mag
     - Type : string
   - 2ème champ :
     - Nom : ca
     - Type : integer
   - 3ème champ :
     - Nom : ca_date
     - Type: date

## Question 3
En se basant sur les tables `store` et `turnover` :
### Question 3.1
Exécuter une requête permettant d'afficher le total du chiffre d'affaires du 2 avril 2021 pour les magasins du Nord. Sauvegarder le resultat dans une table qu'on nommera `total_turnover`, dans le dataset `test_fallou`.

### Question 3.2
Exécuter une requête permettant d'afficher :
- l'ID du ou des magasin(s) ayant fait le plus grand total de chiffre d'affaires parmi les magasins du Nord.
- le total de chiffre d'affaires de ce(s) magasin(s).

### Question 3.3
Exécuter une requête permettant d'afficher une ligne pour chaque région. Chaque ligne comportera :
- la région.
- le nom du magasin avec le record du plus grand chiffre d'affaires sur une journée dans cette région.
- le montant du chiffre d'affaires engrangé par ce magasin sur cette journée record.
