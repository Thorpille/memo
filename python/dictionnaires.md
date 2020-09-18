# Les dictionnaires
### Création :
    mon_dictionnaire = {"prenom": "Paul", "profession": "ingénieur"}
    
### Accès :
    mon_dictionnaire["prenom"]        Accès, plante si la clé n'existe pas
    mon_dictionnaire.get("prenom")    Accès, renvoie none ou son deuxième argument si la clé n'éxiste pas

### Modifier une valeur:
    d["prenom"] = "Julie"

### Supprimer une valeur:
    del d["prenom"]

### Divers :
    d.keys()   Renvoie une liste de toutes les clés du dictionnaire d
    d.values() Renvoie une liste de toutes les valeurs du dictionnaire d
    d.items() Renvoie une liste de tupple contenant tout les couples clés/valeurs
    for cle, valeur in dictionnaire.items():
    print(cle, valeur)

Par défaut, une boucle for sur un dictionnaire renvoi les clés
