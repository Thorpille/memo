# Manipulation des fichiers

### Fichier .json

Lecture :

    with open(chemin, "r") as f:
        contenu = json.load(f)

Ecriture :

    with open(fichier, "w") as f:
        json.dump(settings, f, indent=4)

### Fichier .txt

Lecture :

    with open(chemin, "r") as f:
        contenu = f.read()

Ecriture:

    with open(chemin, "w", encoding = "utf-8") as f:
        f.write("Bonjour")

    f.readlines()

pour récupérer les lignes du fichier dans une liste, \n inclus

    f.read().splitlines()

pour récupérer les lignes du fichier dans une liste, \n non inclus
