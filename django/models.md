### [Django](index.html)
### Models.py

Une Class = une table  
Un attribut = une colonne

Chaque class hérite de models.Model :
{% highlight python %}
Class song(models.Model)
{% endhighlight %}

Chaque attribut doit étre déterminé par ses caractéristiques:
{% highlight python %}
name = models.Charfield(max_length = 255, default='No Name')
duration = models.IntegerField(default=0, help_text="Duration in seconds")
lyrics = models.TextField(blank=True)
{% endhighlight %}

Si une colonne id ou pk(primary key) n'est pas défini, Django en crée automatiquement une


Pour enregistrer des données :

{% highlight python %}
from appone.models import Song
song = Song(name = 'Nuages', duration='211', lyrics='')
song.save()
{% endhighlight %}

Pour ajouter juste une valeur:
{% highlight python %}
song.lyrics = "Mes paroles"
{% endhighlight %}

Pour faire des requétes :

Récupérer la totalité de la liste
{% highlight python %}
Song.objects.all()
{% endhighlight %}

Pour itérer sur les lignes :
{% highlight python %}
for s in Song.objects.all():
  print(s.name)
song.objects.filter(duration__gt=200)#     Greater Than
song.objects.exclude(lyrics__exact='')
song.object.exclude(lyrics__exact='').filter(duration__gt=200)

for s in song.object.exclude(lyrics__exact='').filter(duration__gt=200):
	s.delete()
{% endhighlight %}

Les clés étrangères (foreign keys)
