### [Django](index.md)
# Liste des commande liées au fichier manage.py

### Création d'un projet
{% highlight Batchfile %}
pip install Django  
django-admin startproject monprojet .       // le point sert à ne pas créer de sous dossier
{ % endhighlight %}


### Création d'une app
{% highlight Batchfile %}
python manage.py startapp <mon_app>
{ % endhighlight %}

Dans settings, l'ajouter dans les apps installés.  
Ajouter la fonction dans le views.py de l'app.  
Importer la views et gérer l'URL dans le urls.py du projet


### Lancer le serveur :
{% highlight Batchfile %}
python manage.py runserver
{ % endhighlight %}

### Créer un superuser
