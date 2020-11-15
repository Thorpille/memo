### [Django](index.html)
# Views.py

## Les basiques :

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

## Utiliser les models dans les views

{% highlight python %}from monapp.model import MaTable{% endhighlight %}

### Lecture :
{% highlight python %}
def lecture(request):
	liste =  [] 
	for m in MaTable.objects.all():
		names.append(m.nom)
	
body = '<br/>'.join(liste)
return HttpResponse(body)
{% endhighlight %}
### Ecriture :
{% highlight python %}
def ecriture(request, nom, prenom):
	membre = MaTable(nom=nom, prenom=prenom)
	membre.save()
	return HttpResponse("Enregistrement OK")
{% endhighlight %}  
   
