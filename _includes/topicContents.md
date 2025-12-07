<ul>
  {% for article in site.articles %}
    {% if article.subject == page.name and article.articleBefore == "none" %}
        <li> <a href="{{article.url}}">{{article.name}} - ({{article.updated}})</a></li>

        {% if article.articleAfter != "none" %}
            {% for numbers in (1..999) %} <!-- this is meant to serve as a while loop with the if statement containing a break for this loop being the condition -->
                {% assign endloop = false %}
                {% for nextArticle in site.articles %}
                    {% if nextArticle.name == article.articleAfter %}
                        <li> <a href="{{nextArticle.url}}">{{nextArticle.name}} - ({{nextArticle.updated}})</a></li>
                        {% if nextArticle.articleAfter == "none" %}
                            {% assign endloop = true %}
                        {% endif %}
                        {% break %}
                    {% endif %}
                {% endfor %}
            
            {% if endloop == true %}
                {% break %}
            {% endif %}

            {% endfor %}
        {% endif %}

    {%endif %}
  {% endfor %}
</ul>