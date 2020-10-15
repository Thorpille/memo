# Le langage SQL

    SELECT table1, table2 FROM base


Affichage des données sans doublon :

    SELECT DISTINCT table1, table2
    

Limitation du nombre de réponse (nombre) ou (index, nombre):

    Select table From base LIMIT 2, 1
    
Filtre :

    SELECT table FROM base WHERE nom = "Durand
    
Null

    SELECT table FROM base WHERE service IS NULL
    SELECT table FROM base WHERE service IS NOT NULL
    SELECT prenom FROM employe WHERE ISNULL(service)
    SELECT prenom FROM employe WHERE NOT ISNULL(service)
    
    WHERE truc != "machine"
Filtre aussi les valeurs NULL

    SELECT table FROM BASE WHERE salaire BETWEEN 10000 AND 15000
Les valeurs indiquées sont comprises

    SELECT table FROM BASE WHERE salaire BETWEEN 10000 AND 15000
    
Pour chercher une ou des valeurs exacts :

    SELECT table FROM base WHERE salaire IN (10000, 20000)
    
    SELECT nom, prenom FROM table WHERE nom LIKE 'D%'
Renvoi tout les noms commencant par un D

    SELECT nom, prenom FROM table WHERE nom LIKE 'D____'
REnvoi les nom, prenom des noms commencant par un D suivi de 4 lettres

    -- Un petit commentaire après deux tirets (ou /*puis */)
    
Opérateurs logiques :

    AND
    OR
    IS NOT NULL
    SELECT CONCAT(nom, ' ', prenom) FROM employe

Alias de colonne:

    SELECT CONCAT(nom, ' ', prenom) AS nomComplet FROM employe
    SELECT CONCAT(nom, ' ', prenom) nomComplet FROM employe

WHERE executée au moment de l'entrée dans la requéte, avant la création des alias

    SELECT CONCAT(nom, ' ', prenom) AS nomComplet FROM employe Having nomComplet LIKE 'DU%'
    
Having , tri effectué après la création des alias

    Order BY nom, prenom ordre croissant sur le nom puis le prenom
    ORDER BY nom DESC oredre décroissant
    
