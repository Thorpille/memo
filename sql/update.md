
    UPDATE employe
    SET salaire = salaire * 1.1
    WHERE idEmploye = 6
    
    UPDATE employe
    SET salaire = 15000, idService = 3, sexe = 'M'
    WHERE idEmploye = 7
    
    UPDATE employe e
    JOIN service s
    USING (idService)
    set e.salaire = 25000, s.nom = 'Achats en gros'
    WHERE e.idEmploye = 7
