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
