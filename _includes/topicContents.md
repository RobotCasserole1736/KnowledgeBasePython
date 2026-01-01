<ul>
    {% for article in site.articles %}
        {% if article.topic == page.name and article.articleBefore == "none" %}
            <li> <a href="{{article.url}}">{{article.name}} - ({{article.updated}})</a></li>
            {% assign rootArticle = article %}
        {% endif %}
    {% endfor %}
    
    {% assign articleArray = site.articles | where: "topic", page.name %}

    {% for numbers in articleArray  %} <!-- We should only have to set up as many links as there are articles. -->
        
        {% assign finalArticle = true %}

        {% for article in site.articles %}
            {% if article.name == rootArticle.articleAfter and article.topic == rootArticle.topic %}
                <li> <a href="{{article.url}}">{{article.name}} - ({{article.updated}})</a></li>
                {% assign rootArticle = article %}
                {% assign finalArticle = false %}
                {% break %}
            {% endif %}
        {% endfor %}
        
        {% if finalArticle == true %}
            {% break %}
        {% endif %}

    {% endfor %}
</ul>