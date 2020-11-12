### [Django](index.html)
# Le fichier url.py

### La syntaxe de base du fichier urlpatterns :
{% highlight python %}
from monapp import views
urlpatterns = [
    path('monlien/', views.mafonction),
]
{% endhighlight %}

### Pour utiliser un fichier différent pour une des app:
{% highlight python %}
from django.urls import path, include  

urlpatterns = [
    path('lien_vers_mon_app/', include('monapp.urls')),
]
{% endhighlight %}
### Pour utiliser des arguments via l'url :
{% highlight python %}
path('mon_app/<str:string_arg>/<int:int_arg>/', views.ma_fonction)
{% endhighlight %}

### Pour récupérer une url via son nom (reverse url):
Lui donner un nom dans urls.py :
{% highlight python %}
urlpatterns = [
    path('users/<str:name>/detail', views.users_detail, name='modele-users-details'),
]
{% endhighlight %}
L'appeller avec eventuellement un ou des paramètres dans le template :
{% highlight python %}
<a href="{% url 'modele-users-details' modele %}">{{ infos.name|title }}</a>
{% endhighlight %}
