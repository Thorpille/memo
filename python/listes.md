# Les listes

### Ajout suppression d'éléments :
{% highlight python %}
ma_liste = [1, 2, 3]#           Déclaration + affectation
ma_liste.append(ma_var_a_ajouter)#         ajout d'une seule valeur
ma_liste.extend([1, 2, 3])#           ajout plusieurs valeurs sous forme d'une liste
ma_liste.remove(ma_var_a_sup)#                    Enlève la première occurrence de l'élément indiqué
ma_liste.pop(-1)#    Enlève le dernier élément, renvoie le contenu de l'élément enlevé
ma_liste.clear()#     Vide la liste
{% endhighlight %}

### Info sur la liste :
{% highlight python %}
len(ma_liste)#                            Renvoie le nombre d'éléments
ma_liste.index("truc")#   Renvoie l'index de truc
ma_liste.count("truc")#  Renvoie le nombre d’occurrence de truc
{% endhighlight %}

### Réorganistion de la liste :
{% highlight python %}
ma_liste.sort()#          Range les élément par ordre alphabétique, écrase l'ancienne liste
sorted(ma_liste)#        Renvoie la liste triée par ordre alphabétique
ma_liste.reverse()# inverse l'ordre de la liste et écrase l'ancienne
"-".join(ma_liste)#      Joint les élément de la liste avec - comme séparateur
courses.split(",")#   Découpe la chaine de caractère à chaque , (par défaut coupe aux espaces)
{% endhighlight %}

### Accès aux valeurs
{% highlight python %}
ma_liste[0]#       Accède au premier élément de ma_liste
ma_liste[-1]#     Accède au dernier élément de ma_liste
{% endhighlight %}

### Conversions
{% highlight python %}
list(mon_tuple)#    tuple => liste
tuple(ma_liste)#     liste => tuple
{% endhighlight %}

### Les slices :
{% highlight python %}
ma_liste[0:2]#    Renvoie les deux première valeur de la liste (le deuxième index est exclu)
ma_liste[3:]#      Renvoie les valeurs de la de la quatrième à la dernière
ma_liste[::2]#      Renvoie les éléments par pas de deux (index 0, 2, 4...)
ma_liste[::-1]#    Affiche tout les éléments en commençant par la fin
{% endhighlight %}

### Les compréhensions de liste
{% highlight python %}
liste = [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5]
nombre_positifs = [i for i in liste if i > 0]
nombre_positifs_fois_deux = [i * 2 for i in liste if i > 0]
{% endhighlight %}

### Tupple

Découpe le tupple dans plusieurs variable, l'underscore peut servir à ignorer une valeur
{% highlight python %}
mon_tupple = (Bonjour, vous, coucou)
var1, var2, _ = mon_tupple
{% endhighlight %}
