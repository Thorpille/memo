# Liste des commande liées au fichier manage.py

### Création d'un projet
    pip install Django  
    django-admin startproject monprojet .       // le point sert à ne pas créer de sous dossier


### Création d'une app
    python manage.py startapp <mon_app>
Dans settings, l'ajouter dans les apps installés.  
Ajouter la fonction dans le views.py de l'app.  
Importer la views et gérer l'URL dans le urls.py du projet


### Lancer le serveur :
    python manage.py runserver


### Créer un superuser
