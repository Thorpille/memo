# Views.py

### Réponse HTTP basique
    def ma_view(request, param1, param2=0):
      body = f"Premier paramètre = {param1}, deuxième paramètre = {param2}"
      return HttpResponse(body)
  
### Réponse avec loader de template
    def git(request):
      context = {'param1': 2020,
                 'string': 'bla bla bla'}
      template = loader.get_template('monapp/template.html')
      return HttpResponse(template.render(context, request))
