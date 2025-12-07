---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---

# Welcome to the Recipe Book!

Here we hope to hose some cool guides for our software and links to wikis for software we use, designed to be friendly to new students and teams.

Here's a list of our site's contents:

<ul>
  {% for topic in site.topics %}
    <li>
        <h2><a href="{{ topic.url }}">{{ topic.name }}</a></h2>
        <p>{{ topic.desc }}</p>
        <ul>{{ topic.content | markdownify }}</ul>
    </li>
  {% endfor %}
</ul>