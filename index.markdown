---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
---
<div class="row">
  <div class="box">
    <a href="https://www.youtube.com/c/MSXVRComputer">Canal Youtube</a>
    <p>MSXVR</p>
  </div>
  <div class="box">
    <h3>Chat MSXVR</h3>
    <p>Chat oficial de la comunidad MSXVR</p>
  </div>
  <div class="box">
    <a href="http://msxvr.es/doc/forum/">Forum MSXVR</a>
    <p>Forum oficial de la comunidad MSXVR</p>
  </div>
  <div class="box">
    <h3>Github</h3>
    <p>Repositorio oficial de codigo con ejemplos</p>
  </div>
</div>

<div class="divider">
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
</div>

<div class="divider">
  <h2>Recursos MSX</h2>
</div>

<div class="row">
  <div class="box">
    <h1>Recursos MSX</h1>
    <ul>
        <li>
          <h2><a href="http://www.lavandeira.net/relearning-msx/">Relearning MSX</a></h2>
          <p>Series of articles about developing software for MSX computers</p>
        </li>
        <li>
          <h2><a href="https://books.google.com/books/about/MSX_Made_Simple.html?id=Qo-GDAAAQBAJ">MSX-DOS</a></h2>
        </li>
        <li>
          <h2><a href="https://konamiman.github.io/MSX2-Technical-Handbook/">MSX2 Technical Handbook</a></h2>
        </li>
    </ul>
  </div>
    <div class="box">
    <h1>Utilidades MSX</h1>
    <ul>
        <li>
          <h2><a href="https://books.google.com/books/about/MSX_Made_Simple.html?id=Qo-GDAAAQBAJ">MSX-HUB</a></h2>
          <h2><a href="https://www.louthrax.net/mgr/">Sofarun</a></h2>
          <h2><a href="https://www.msx.org/wiki/MultiMente">MultiNente</a></h2>
        </li>
    </ul>
  </div>
  <div class="box">
    <h1>Libros sobre el MSX</h1>
    <ul>
        <li>
          <h2><a href="https://books.google.com/books/about/MSX_Made_Simple.html?id=Qo-GDAAAQBAJ">MSX Made Simple</a></h2>
        </li>
    </ul>
  </div>
</div>

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