# Test technique Datapool

En shell, chargez les fichiers file_1.csv et file_2.csv à la racine du bucket GCS g://auchan-itcorp-dev_dc_fallou/

Créez un fichier main.py qui executera les actions suivantes:

1. Chargement du fichier file_1.csv sur bigquery.
le fichier est situé sur 
projet: auchan-itcorp-dev
dataset: test_fallou
schema: auto
nom de la table: table_1 (la table n'existe pas)

2. Chargement du fichier file_2.csv sur bigquery.
le fichier est situé sur 
projet: auchan-itcorp-dev
dataset: test_fallou
schema:
- champ 1: 
    -   name: mag
    -   type: string
- champ 2:
    -   name: ca
    -   type: integer
- champ 3:
    -   name: ca_date
    -   type: date

nom de la table: table_2 (la table n'existe pas)

3. Exécution, en se basant sur table_1 et table_2, d'une requête permetant de trouver le magasin auchan qui à le plus gros chiffre d'affaire dans le Nord.
Sauvegarder le resultat dans une table table_3 dans le dataset test_fallou

