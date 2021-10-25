### [Scraping](index.md)

## Base :
{% highlight python %} 
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
