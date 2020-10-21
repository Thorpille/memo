

### Syntaxe positionnel :

    INSERT INTO employe
    VALUES (DEFAULT, 2, 'Legrand', 'Sam', 'M', 1800, '2019-07-13')
    
DEFAULT = NULL
    
###Syntaxe nommée :

    INSERT INTO employe (nom, prenom)
    VALUES('Lefranc', 'GUY')
    
###Insertion par selection :

    INSERT INTO employe (nom, prenom)
    SELECT nom, prenom FROM directeur
    
Possibilité aussi d'insérer des données avec SET dans MYSQL mais commande non standard
