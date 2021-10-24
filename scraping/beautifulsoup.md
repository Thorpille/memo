### [Scraping](index.md)

[Lien doc officielle](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)

## Intro :
{% highlight python %} 
import requests
from bs4 import BeautifulSoup
page = requests.get("http://github.com")

if page.status_code == 200:
    parsed_page = BeautifulSoup(page.content, 'lxml')
{% endhighlight %}

## Selecteurs HTML
{% highlight python %}
parsed_page.title
parsed_page.h1.name
parsed_page.find('li', {'class':'next'})
parsed_page.find_all('a')
top_ten_tags = parsed_page.find('div',{'class':'col-md-4 tags-box'}).find_all('a',{'class':'tag'})
{% endhighlight %}

{% highlight python %}tag.string{% endhighlight %} pour récupérer le texte entre les balises (non encapsulées)
{% highlight python %}h1.get_text{% endhighlight %} pour récupérer le texte entre les balises, meme en cas de balises encapsulées
{% highlight python %}tag.attrs{% endhighlight %} pour récupérer tous les attributs sous forme de dictionnaire


## Selecteurs CSS
{% highlight python %}
parsed_page.select("title")
pardes_page.select("h1 a"){% endhighlight %} selectionne le sous élément a présent à l'intérieur du h1 {% highlight python %}
parsed_page.select(".tag")
parsed_page.select("a[href='/tag/be-yourself/page/1/']")
{% endhighlight %}
