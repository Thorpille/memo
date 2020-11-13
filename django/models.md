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
{% endhighlight %}

Pour ajouter juste une valeur:
{% highlight python %}
song.lyrics = "Mes paroles"
{% endhighlight %}

Pour sauvegarder :
{% highlight python %}
song.save()
{% endhighlight %}

Pour faire des requétes :

Récupérer la totalité de la liste
{% highlight python %}
Song.objects.all()
{% endhighlight %}

Pour itérer sur les lignes :
{% highlight python %}
for s in MaTable.objects.all():
  print(s.name)
song.objects.filter(un_nombre__gt=10)#     Greater Than
song.objects.exclude(ma_string__exact='truc')
song.objects.exclude(ma_string__exact='truc').filter(un_nombre__gt=200)

for s in MaTable.object.exclude(ma_string__exact='truc').filter(un_nombre__gt=10):
	s.delete()
{% endhighlight %}

Les types de valeurs :
{% highlight python %}
models.CharField(max_length=255)
models.IntegerField(default=0, help_text='Duration in seconds')
models.TextField(blank=True)


{% endhighlight %}


