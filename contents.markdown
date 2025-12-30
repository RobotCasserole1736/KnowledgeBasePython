---
layout: page
name: contents
permalink: /contents/
---

<ul>
  {% for topic in site.topics %}
    <li>
        <h2><a href="{{ topic.url }}">{{ topic.name }}</a></h2>
        <p>{{ topic.desc }}</p>
        <ul>{{ topic.content | markdownify }}</ul>
    </li>
  {% endfor %}
</ul>