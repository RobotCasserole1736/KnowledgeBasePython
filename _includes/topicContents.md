<ul>
  {% for article in site.articles %}
    {% if article.subject == page.name %}
        <li> <a href="{{article.url}}">{{article.name}} - ({{article.updated}})</a></li>
    {%endif %}
  {% endfor %}
</ul>