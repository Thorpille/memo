# Base de données

Connexion :

    conn = sqlite3.connect           Connexion
    c = conn.sursor()                Curseur
    c.execute("Mon code SQL")        Stack Sql
    conn.commit()                    Envoi Sql
    conn.close()                     Fermeture connexion

Création table :

    c.execute("""
    CREATE TABLE IF NOT EXISTS employees(
        prenom text,
        nom text)
    """)

Envoi de donnée :

    d = {"prenom": "Patrick", "nom": "Chirac"}
    c.execute("INSERT INTO employees VALUES (:prenom, :nom)", d)

Récupération de donnée :

    c.execute("SELECT * FROM employes WHERE prenom = 'Pierre'")
    donnees = c.fetchall()
ou
 
    d = {"prenom": "Pierre"}
    c.execute("SELECT * FROM employes WHERE prenom =:a", d)
    donnees = c.fetchall()