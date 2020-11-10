### [Django](index.html)
# Templates

### Sytaxe de  base
{% highlight liquid %}{% raw %}
{{ ma_variable }}
{# mon commentaire #} ou {% comment %} Commentaire sur lignes {% endcomment %}
Pour accédes à la première valeur de la clé d'un dictionnaire : {{ picture.categories.0 }}
{% endraw %}{% endhighlight %}

### L'héritage de template :

Dans le template parent, les blocs à surcharger sont définis par :
{% highlight liquid %}{% raw %}
{% block mon_bloc %} contenu de base {% endblock %}
{% endraw %}{% endhighlight %}

Dans le template parent : 
{% highlight liquid %}{% raw %}
{% extends "monapp/base.html" %}

{% block mon_block %} Mon nouveau contenu {%endblock mon_block %} le nom du bloc dans le tag de fin est optionnel mais peut améliorer la lisibilité
{{ block.super }} pour récupérer le contenu du bloc parent
{% endraw %}{% endhighlight %}

### Les ressources statiques :

Dans le template, chargé le module statique :
{% highlight liquid %}{% raw %}
{% load static %}
{% endraw %}{% endhighlight %}

Pour appeler les ressources :
{% highlight liquid %}{% raw %}
{% static 'apptwo/css/style.css' %}
{% endraw %}{% endhighlight %}

pour concaténer des valeurs:
{% highlight liquid %}{% raw %}
{% with 'apptwo/'|add:picture.filename as filepath %}   {% endwith %}
{% endraw %}{% endhighlight %}

Pour inclure un template dans un autre template :
{% highlight liquid %}{% raw %}
{% include "peoplebook/block_user_details.html %}
{% endraw %}{% endhighlight %}





### Tags et filtres :

#### Tags:
{% highlight liquid %}{% raw %}
{% if condition %} ... {% endif %}  
{% for i in truc %} ... {% endfor %}  
    print('rt')  
{% endraw %}{% endhighlight %}

#### Pour basculer d'une valeur à l'autre à chaque appel :
{% highlight liquid %}{% raw %}
{% cycle '#80e27e' '#087f23' as rowcolors %}
{% cycle rowcolors %}
{{ rowcolors }} pour récupérer la dernière valeur utilisée
{% endraw %}{% endhighlight %}


#### Filtres:
{% highlight liquid %}{% raw %}
{{ name|length }}
{{ name|default:"Empty"}}
{{ name|lower|truncatewords:5 }}
{{ page_title|title }}
{{ var_contenant_du_html|safe }} pour que le html ne soit pas échappé
{{ var_contenant_du_html|safe|striptags }} pour supprimer les balises html
{{ ma_liste|join: ', ' }}
{% endraw %}{% endhighlight %}
