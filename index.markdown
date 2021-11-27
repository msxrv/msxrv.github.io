---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
---
{% assign categories = site.documents | group_by: "category" %}
{% for category in categories %}
<h1>Categoria {{ category.name }}
<ul>
  {% for document in category.items %}
    <li>
      <h2><a href="{{ document.url }}">{{ document.name }}</a></h2>
      <h3>{{ document.position }}</h3>
    </li>
  {% endfor %}
</ul>
{% endfor %}
