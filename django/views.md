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
