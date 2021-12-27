---
title: Search
layout: search
---
<script>
  window.store = {
    {% for doc in site.documents %}
      "{{ doc.url | slugify }}": {
        "title": "{{ doc.titulo | xml_escape }}",
        "author": "{{ doc.autor | xml_escape }}",
        "category": "{{ doc.categoria | xml_escape }}",
        "content": {{ doc.content | strip_html | strip_newlines | jsonify }},
        "url": "{{ doc.url | xml_escape }}"
      }
      {% unless forloop.last %},{% endunless %}
    {% endfor %}
  };
</script>