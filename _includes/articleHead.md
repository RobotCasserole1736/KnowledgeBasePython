
{%- assign nextPage = "final" -%}
{%- assign previousPage = "first" -%}

{%- for nextArticle in site.articles-%}
    {%- if nextArticle.name == page.articleAfter -%}
        {%- assign nextPage = nextArticle.url | append: "" -%}
    {%- endif -%}
{%- endfor -%}

{%- for nextArticle in site.articles-%}
    {%- if nextArticle.name == page.articleBefore -%}
        {%- assign previousPage = nextArticle.url | append: "" -%}
    {%- endif -%}
{%- endfor -%}

{%- assign currentTopicURL = page.url -%}

{%- for topics in site.topics -%}
    {%- if topics.name == page.topic -%}
        {%- assign currentTopicURL = topics.url | append: "" -%}
    {%- endif -%}
{%- endfor -%}

### Topic: [{{page.topic}}]({{currentTopicURL}}) | Last updated: {{page.updated}}

{% if previousPage != "first" %}
*Previous article: [{{page.articleBefore | string }}]({{ previousPage | string }})*
{% else %}
*This is the first article on this [topic]({{currentTopicURL}})!*
{%- endif -%}
  ----  
{%- if nextPage != "final" -%}
*Next article: [{{page.articleAfter | string }}]({{ nextPage | string }})*
{%- else -%}
*This is the last article on this [topic]({{currentTopicURL}})!*
{%- endif -%}
