
### Last updated: {{page.updated}}

{% assign link = "final" %}

{% for nextArticle in site.articles%}
    {% if nextArticle.name == page.articleAfter %}
        {% assign link = nextArticle.url | append: "" %}
    {% endif %}
{% endfor %}

{% if link != "final" %}
### Next article: [{{page.articleAfter | string }}]({{ link | string }})
{% else %}
### Welp! Looks like this is the last article on this subject!
{% endif s%}
