### [Django](index.html)
# Views.py

### Réponse HTTP basique :
{% highlight python %}
def ma_view(request, param1, param2=0):
    body = f"Premier paramètre = {param1}, deuxième paramètre = {param2}"
return HttpResponse(body)
{% endhighlight %}
  
### Réponse avec loader de template :
{% highlight python %}
def ma_view(request):
context = {'param1': 2020,
           'string': 'bla bla bla'}
template = loader.get_template('monapp/template.html')
return HttpResponse(template.render(context, request))
{% endhighlight %}

### Utiliser les models dans les views

from appone.model import Song

 # Lecture :

def song_list(request):
 names =  [] 
for s in Song.objects.all():
	names.append(s.name)
	
body = '<br/>.join(names)
return HttpResponse(body)

# Ecriture :
def songs_add(request, song_name, duration):
	song = Song(name=song_name, duration=duration
	song.save()
	return HttpResponse("Enregistrement OK")
    
   
