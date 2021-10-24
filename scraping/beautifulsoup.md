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

## Naviguer dans le dom
liste les élément contenu dans la sélection :
first_quote.contents
pour récupérer la tatalité de  l'élément parent :
first_quote.parent
Pour récupérer les attributs du parents
first_quote.parent.attrs
.previous_sibling renvoi l'élément précédent au même niveau
.next_sibling renvoi l'élément suivant au même niveau

## Export
{% highlight python %}
with open('mon_chemin/mon_fichier.json', 'w')as f:
            json.dump(ma_liste, f)
            
import pandas as pd
data_pd = pd.DataFrame.from_dict(ma_liste)


data_pd.to_json('monchemin.json')
data_pd.to_csv('monchemin.csv')
{% endhighlight %}
