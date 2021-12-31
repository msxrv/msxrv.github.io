---
---
<div class="section">
  <div class="row">
    <div class="box-links">
      <div class="msxvr-link">
        <div class="msxvr-link-logo">
          <figure class="image is-64x64">
            <img src="assets/img/youtube-logo-2431.png">
          </figure>
        </div>
        <div class="msxvr-link-description">
          <a href="https://www.youtube.com/c/MSXVRComputer">Canal Youtube</a>
          <p>Demos, tutoriales y otros videos para aprender mas sobre tu MSXVR</p>
        </div>
      </div>
    </div>
    <div class="box-links">
      <div class="msxvr-link">
        <div class="msxvr-link-logo">
          <figure class="image is-64x64">
            <img src="assets/img/guilded-logo-reco.png">
          </figure>
        </div>
        <div class="msxvr-link-description">
          <a href="https://www.guilded.gg/i/pPAaqQaE">Guilded</a>
          <p>Unete al chat de la comunidad de usuarios y desarolladores</p>
        </div>
      </div>
    </div>
    <div class="box-links">
      <div class="msxvr-link">
        <div class="msxvr-link-logo">
          <figure class="image is-64x64">
            <img src="assets/img/forum-icon-23.jpeg">
          </figure>
        </div>
        <div class="msxvr-link-description">
          <a href="http://msxvr.es/doc/forum/">Forum MSXVR</a>
          <p>Anuncia o discute cualquier tema relacionado con el MSXVR</p>
        </div>
      </div>
    </div>
    <div class="box-links">
      <div class="msxvr-link">
        <div class="msxvr-link-logo">
          <figure class="image is-64x64">
            <img src="assets/img/GitHub-Mark-64px.png">
          </figure>
        </div>
        <div class="msxvr-link-description">
          <a href="https://github.com/msxvr">Github</a>
          <p>Repositorio oficial con ejemplos de codigo y utilidades para tu maquina</p>
        </div>
      </div>
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
      {% assign primeros_pasos = site.documents | where: "categoria", "primeros_pasos" %}
        {% for doc in primeros_pasos %}
          <li>
            <a class="article" href="{{ doc.url }}">
              <article>
                <h3>{{ doc.titulo }}</h3>
                <p>{{ doc.descripcion }}</p>
              </article>
            </a>
          </li>
        {% endfor %}
      </ul>
    </div>

    <div class="box">
      <h1>Aprende a programar</h1>
      <ul>
        {% assign programacion = site.documents | where: "categoria", "programming" %}
        {% for doc in programacion %}
          <li>
            <a class="article" href="{{ doc.url }}">
              <article>
                <h3>{{ doc.titulo }}</h3>
                <p>{{ doc.descripcion }}</p>
              </article>
            </a>
          </li>
        {% endfor %}
      </ul>
    </div>

    <div class="box">
      <h1>Tutoriales</h1>
      <ul>
        {% assign tutoriales = site.documents | where: "categoria", "tutoriales" %}
        {% for doc in tutoriales %}
          <li>
            <a class="article" href="{{ doc.url }}">
              <article>
                <h3>{{ doc.titulo }}</h3>
                <p>{{ doc.descripcion }}</p>
              </article>
            </a>
          </li>
        {% endfor %}
      </ul>
    </div>
  </div>
</div>

<div class="section">
  <div class="section-header">
   <h2>Otros recursos</h2>
  </div>
  <div class="row">
    <div class="box">
      <h1>Programacion de videojuegos</h1>
      <ul>
          <li>
            <a class="article" href="https://www.youtube.com/playlist?list=PL_xRyXins848jkwC9Coy7B4N5XTOnQZzz">
              <article>
                <h3>Intro to Game Programming (C++)</h3>
                <p>Curso de programacion de videojuegos en YouTube por la Memorial University</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="https://profesorretroman.com">
              <article>
                <h3>Programación de Videojuegos en Ensamblador Z80</h3>
                <p>Clases impartidas en la Universidad de Alicante, así como los retos y desafíos propuestos.</p>
              </article>
            </a>
          </li>
      </ul>
  </div>
</div>

