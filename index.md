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
          <p>Demos, tutoriales y otros vídeos para aprender mas sobre tu MSXVR.</p>
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
          <p>Únete al chat de la comunidad de usuarios y desarolladores.</p>
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
          <p>Anuncia o discute cualquier tema relacionado con el MSXVR.</p>
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
          <p>Repositorio oficial con ejemplos de código y utilidades para tu máquina.</p>
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
   <h2>Recursos MSX</h2>
  </div>
  <div class="row">
    <div class="box">
      <h1>Documentación técnica</h1>
      <ul>
          <li>
            <a class="article" href="http://www.lavandeira.net/relearning-msx/">
              <article>
                <h3>Relearning MSX</h3>
                <p>Series de articulos sobre desarrollo de software para el MSX.</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="http://map.grauw.nl/resources/dos2_environment.php">
              <article>
                <h3>MSX-DOS version 2</h3>
                <p>Sistema operativo de disco para ordenadores MSX 2.</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="https://konamiman.github.io/MSX2-Technical-Handbook">
              <article>
                <h3>MSX2 Technical Handbook</h3>
                <p>Manual de referencia del sistema MSX2 publicada por la ASCII Corporation en 1987.</p>
              </article>
            </a>
          </li>
      </ul>
    </div>
      <div class="box">
      <h1>Utilidades MSX</h1>
      <ul>
          <li>
            <a class="article" href="https://books.google.com/books/about/MSX_Made_Simple.html?id=Qo-GDAAAQBAJ">
              <article>
                <h3>MSX-HUB</h3>
                <p>Sistema de gestión de paquetes para el MSX. Descarga y actualiza tu software de MSX directamente desde Internet</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="https://www.louthrax.net/mgr/">
              <article>
                <h3>Sofarun</h3>
                <p>Herramienta para ejecutar imágenes en formato .DSK, .CAS y .ROM.</p>
            </a>
          </li>
          <li>
            <a class="article" href="https://www.msx.org/wiki/MultiMente">
              <article>
                <h3>MultiMente</h3>
                <p>Administrador de archivos para el MSX-DOS 2, basado en FILMTN, el administrador de archivos para MS-DOS.</p>
              </article>
            </a>
          </li>
      </ul>
    </div>
    <div class="box">
      <h1>Libros sobre el MSX</h1>
      <ul>
          <li>
            <a class="article" href="https://books.google.com/books/about/MSX_Made_Simple.html?id=Qo-GDAAAQBAJ">
              <article>
                <h3>MSX Made Simple</h3>
                <p>Aprende MSX Basic y breve introducción al codigo maquina.</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="https://www.amazon.com/dp/1527298094?linkCode=ogi&th=1&psc=1&tag=sofferscom1-20">
              <article>
                <h3>Modern MSX BASIC Game Development</h3>
                <p>Desarrolla juegos retro en MSX Basic usando herramientas modernas.</p>
              </article>
            </a>
          </li>
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
      <h1>Programación de videojuegos</h1>
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

