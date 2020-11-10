# Templates

### Sytaxe de  base
    {{ ma_variable }}
    {# mon commentaire #} ou {% comment %} Commentaire sur lignes {% endcomment %}
    Pour accédes à la première valeur de la clé d'un dictionnaire : {{ picture.categories.0 }}
    
    
    
    
### Tags et filtres :
#### Tags:
{% highlight python %}  
{% if condition %} ... {% endif %}  
{% for i in truc %} ... {% endfor %}  
print('rt')  
{% endhighlight %}

#### Pour basculer d'une valeur à l'autre à chaque appel :
    {% cycle '#80e27e' '#087f23' as rowcolors %}
    {% cycle rowcolors %}
    {{ rowcolors }} pour récupérer la dernière valeur utilisée

#### Filtres:
    {{ name|length }}
    {{ name|default:"Empty"}}
    {{ name|lower|truncatewords:5 }}
    {{ page_title|title }}
    {{ var_contenant_du_html|safe }} pour que le html ne soit pas échappé
    {{ var_contenant_du_html|safe|striptags }} pour supprimer les balises html
    {{ ma_liste|join: ', ' }}
