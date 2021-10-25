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
