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

### Fonctions d'aggrégations

    SELECT COUNT(service) nbServices FROM employe
Compte le nombre d'entrées non nulle de la colonne service, si (*) compte tout, y compris les lignes composé de NULL 

    SELECT MIN(salaire) FROM employe
    SELECT MAX(nom) FROM employe
Fonctionne aussi bien sur les nombres que sur les chaines de caractères ou les dates

    SELECT SUM(salaire) FROM employe

Calcul de la moyenne :

    SELECT SUM(salaire) / COUNT(*) FROM employe
    SELECT AVG(salaire) FROM employe
    
### Regroupements

    SELECT sexe, AVG(salaire) moyenne FROM employe GROUP BY sexe
Le group by doit étre utilisé sur une colonne selectionné + une fonction d'agrégation

Where/Having
WHERE agit en entrée, avant la création des alias, HAVING agit en sortie
Having:

    SELECT service, AVG(salaire) moyenne
    FROM employe
    GROUP BY service
    HAVING moyenne > 1000

WHERE + HAVING :

    SELECT service, AVG(salaire) moyenne FROM employe WHERE salaire > 12000 GROUP BY service HAVING moyenne > 15000

Ordre des clauses :

    SELECT FROM
    WHERE
    GROUP BY
    HAVING
    ORDER BY
    LIMIT

Jointures :
Jointure interne ( ne selectionne que ceux qui ont une correspondance)

    SELECT employe.nom, employe.prenom, service.nom FROM employe, service WHERE employe.idService = service.idSevice
    SELECT employe.nom, employe.prenom, service.nom FROM employe JOIN service ON employe.idService = service.idService
    SELECT employe.nom, employe.prenom, service.nom FROM employe JOIN service USING(idService) //Si les deux clés sont les memes
    SELECT employe.nom, employe.prenom, service.nom FROM employe NATURAL JOIN service //Si les deux clés sont les memes et qu'il n'y a pas d'autres clés identiques
Dans les jointures internes, l'ordre des tables n'a aucune importance
    
Jointures externes :

    

