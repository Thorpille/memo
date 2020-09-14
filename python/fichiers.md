# Manipulation des fichiers

### Fichier .txt

Lecture :

    with open(chemin, "r") as f:
        contenu = f.read()

Ecriture:

    with open(chemin, "w") as f:
        f.write("Bonjour")

### Fichier .json

Lecture :

    with open(chemin, "r") as f:
        contenu = json.load(f)

Ecriture :

    with open(fichier, "w") as f:
        json.dump(settings, f, indent=4)
