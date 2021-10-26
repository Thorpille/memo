### [Scraping](index.md)

## Base :
{% highlight python %} 
/text pour récupérer le contenu
result = {
  'titre': response.xpath('//head/title/text()').get()
        }

        yield result
{% endhighlight %}
{% highlight python %} 
result = {
  'liens': response.xpath('//a/text()').getall()
        }

        yield result
{% endhighlight %}

Pour chercher un attribut role=alert :

{% highlight python %}'alerte': response.xpath('//div[@role="alert"]/text').get(){% endhighlight %}

Ajout d'un point au début des expressions rellatives xpath
{% highlight python %} 
book_bloc = response.xpath('//li[@class="col-xs-6 col-sm-4 col-md-3 col-lg-3"]')[0]
        title = book_bloc.xpath('.//h3/a/text()').get()
        {% endhighlight %}

Pour récupérer la valeur d'un attribut :
{% highlight python %} 
'book_url': book_bloc.xpath('//h3/a/@href').get()
{% endhighlight %}

### Les filtres

Pour filtrer les urls contenant "/category":

{% highlight python %} //a[contains(@href,'/category')]{% endhighlight %}

Pour filtrer les balises dans lesquelles le textes contient "the"
{% highlight python %}
books = response.xpath("//h3[contains(.//text(), 'the')]")
        text_books = books.xpath('.//text()').getall()
{% endhighlight %}

Nettoyer le texte avec normalize-space
{% highlight python %}
text_category = category_bloc.xpath('normalize-space(.//a/text())').getall()
{% endhighlight %}

***Naviguer dans le dom


