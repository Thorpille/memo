# Manipulation des fichiers

### Fichier .json

Lecture :
{% highlight python %}
with open(chemin, "r") as f:
    contenu = json.load(f)
{% endhighlight %}

Ecriture :
{% highlight python %}
with open(fichier, "w") as f:
    json.dump(settings, f, indent=4)
{% endhighlight %}


### Fichier .txt

Lecture :
{% highlight python %}
with open(chemin, "r") as f:
    contenu = f.read()
{% endhighlight %}

Ecriture:
{% highlight python %}
with open(chemin, "w", encoding = "utf-8") as f:
    f.write("Bonjour")

    f.readlines()
{% endhighlight %}
pour récupérer les lignes du fichier dans une liste, \n inclus
{% highlight python %}
f.read().splitlines()
{% endhighlight %}
pour récupérer les lignes du fichier dans une liste, \n non inclus
