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
    
WHERE truc != "machaine"
Filtre aussi les valeurs NULL
