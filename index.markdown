---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
---
<div id="">
  <h3>Comunidad MSXVR</h3>
  <h3>Forum de la comunidad</h3>
  <h3>Codigo</h3>
</div>

{% assign categories = site.documents | where: "category", "primeros_pasos" %}
<h1>Primeros pasos</h1>
<ul>
  {% for document in category.items %}
    <li>
      <h2><a href="{{ document.url }}">{{ document.name }}</a></h2>
      <h3>{{ document.position }}</h3>
    </li>
  {% endfor %}
</ul>

{% assign categories = site.documents | where: "category", "programacion" %}
<h1>Aprende a programar</h1>
<ul>
  {% for document in category.items %}
    <li>
      <h2><a href="{{ document.url }}">{{ document.name }}</a></h2>
      <h3>{{ document.position }}</h3>
    </li>
  {% endfor %}
</ul>

<div id="manuales" style="display:none">
  <div id="pasos">
      <h2>Primeros pasos con el MSXVR</h2>
      <section>
          <a href="">Manual de servicio</a>
          <a href="">Welcome pack</a>
          <a href="">Como realizar una copia de seguridad</a>
      </section>
  </div>

  <div id="programacion">
      <h2>Aprende a programar</h2>
      <section>
          <a href="">Libro de programacion</a>
          <a href="">Curso de programacion en VR-SCRIPT</a>
      </section>                
  </div>

  <div id="tutoriales">
      <h2>Tutoriales MSXVR</h2>
      <section>
          <a href="">Como acceder a la partición boot</a>
          <a href="">Conectarnos al MSXVR por SSH</a>
      </section>
  </div>

  <div id="documentacion">
      <h2>Documentacion MSX</h2>
      <section>
          <a href="">Libro técnico de MSX</a>
      </section>
  </div>
</div>

<a href="documents/introduccion_msxvr.html">Visita el tutorial</a>
