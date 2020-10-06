# Liste de modules intéresants

### os :
    os.path.join()                             génère un chemin en concaténant les valeurs qui lui sont passées, gère automatiquement les "/" selon l'os
    os.mkdir()                                  Cré un nouveau dossier
    os.makedirs()                             Crée un nouveau dossier et si besoin ses dossiers parents possibilité d’utiliser l'argument exist_ok = True pour éviter le plantage en cas de dossier déjà présent
    os.path.exists()                           Renvoie True si le dossier existe
    os.removedirs()                          Supprime un dossier, plante si le dossier n'existe pas
    os.path.splitext(machin.txt)        Sépare le nom de fichier de son extension, renvoie une liste ['machin', '.txt']
    os.rename("ancien_nom", "nouveau_nom")


### random :
    random.randint(0, 10)         renvoie un nombre entier entre 0 et 10 inclue
    random.uniform(0, 10)        renvoie un nombre décimale entre 0 et 10
    random.randrange(10)        renvoie un nombre entre 0 et 9 (le 10 est exclue)
    random.randrange(0, 101, 10)        renvoie un nombre entre 0 et 100 (le 101 est exclue) par pas de 10
    
### shutil :
    shutil.move(fichier, dossier)
### datetime

https://strftime.org/
