---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
---
<div class="section">
  <div class="row">
    <div class="box-links">
      <div>
        <img width="30px" src="assets/img/github.png">
      </div>
      <div>
        <a href="https://www.youtube.com/c/MSXVRComputer">Canal Youtube</a>
        <p>Tutoriales, para tu MSXVR</p>
      </div>
    </div>
    <div class="box-links">
      <a href="https://www.guilded.gg/i/pPAaqQaE">Guilded</a>
      <p>Chat de la comunidad</p>
    </div>
    <div class="box-links">
      <a href="http://msxvr.es/doc/forum/">Forum MSXVR</a>
      <p>Anuncia o discute cualquier tema relacionado con el MSXVR</p>
    </div>
    <div class="box-links">
      <a href="https://github.com/msxvr">Github</a>
      <p>Repositorio oficial de codigo con ejemplos</p>
    </div>
  </div>
</div>

<div class="section">
  <div class="section-header">
    <h2>Todo sobre el MSXVR</h2>
  </div>
  <div class="row">
    <div class="box">
      <h1>Primeros pasos</h1>
      <ul>
      {% assign primeros_pasos = site.documents | where: "category", "primeros_pasos" %}
        {% for document in primeros_pasos %}
          <li>
            <a href="{{ document.url }}">{{ document.name }}</a>
            <h3>{{ document.position }}</h3>
          </li>
        {% endfor %}
      </ul>
    </div>

    <div class="box">
      <h1>Aprende a programar</h1>
      <ul>
        {% assign programacion = site.documents | where: "category", "programming" %}
        {% for document in programacion %}
          <li>
            <a href="{{ document.url }}">{{ document.name }}</a>
            <h3>{{ document.position }}</h3>
          </li>
        {% endfor %}
      </ul>
    </div>

    <div class="box">
      <h1>Tutoriales</h1>
      <ul>
        {% assign tutoriales = site.documents | where: "category", "tutoriales" %}
        {% for tutorial in tutoriales %}
          <li>
            <a href="{{ tutorial.url }}">{{ tutorial.name }}</a>
            <h3>{{ tutorial.position }}</h3>
          </li>
        {% endfor %}
      </ul>
    </div>
  </div>
</div>

<div class="section">
  <div class="section-header">
   <h2>Recursos MSX</h2>
  </div>
  <div class="row">
    <div class="box">
      <h1>Recursos MSX</h1>
      <ul>
          <li>
            <a href="http://www.lavandeira.net/relearning-msx/">Relearning MSX</a>
            <p>Series of articles about developing software for MSX computers</p>
          </li>
          <li>
            <a href="https://books.google.com/books/about/MSX_Made_Simple.html?id=Qo-GDAAAQBAJ">MSX-DOS</a>
          </li>
          <li>
            <a href="https://konamiman.github.io/MSX2-Technical-Handbook/">MSX2 Technical Handbook</a>
          </li>
      </ul>
    </div>
      <div class="box">
      <h1>Utilidades MSX</h1>
      <ul>
          <li>
            <a href="https://books.google.com/books/about/MSX_Made_Simple.html?id=Qo-GDAAAQBAJ">MSX-HUB</a>
          </li>
          <li>
            <a href="https://www.louthrax.net/mgr/">Sofarun</a>
          </li>
          <li>
            <a href="https://www.msx.org/wiki/MultiMente">Multi Mente</a>
          </li>
      </ul>
    </div>
    <div class="box">
      <h1>Libros sobre el MSX</h1>
      <ul>
          <li>
            <a href="https://books.google.com/books/about/MSX_Made_Simple.html?id=Qo-GDAAAQBAJ">MSX Made Simple</a>
          </li>
      </ul>
    </div>
  </div>
</div>