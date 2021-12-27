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
   <h2>Recursos MSX</h2>
  </div>
  <div class="row">
    <div class="box">
      <h1>Documentacion tecnica</h1>
      <ul>
          <li>
            <a class="article" href="http://www.lavandeira.net/relearning-msx">
              <article>
                <h3>Relearning MSX</h3>
                <p>Series of articles about developing software for MSX computers</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="http://map.grauw.nl/resources/dos2_environment.php">
              <article>
                <h3>MSX-DOS version 2</h3>
                <p>The advanced disk operating system for MSX 2 computers.</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="https://konamiman.github.io/MSX2-Technical-Handbook">
              <article>
                <h3>MSX2 Technical Handbook</h3>
                <p>This is the (almost) full reference of the MSX2 system as published by ASCII Corporation in 1987.</p>
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
                <p>Package manager for your MSX computer. Download software directy from the internet. Upgrade software when a new version is released ...</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="https://www.louthrax.net/mgr/">
              <article>
                <h3>Sofarun</h3>
                <p>MSX tool designed to run disk (.DSK), cassette (.CAS) and cartridge (.ROM) images.</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="https://www.msx.org/wiki/MultiMente">
              <article>
                <h3>MultiMente</h3>
                <p>Files manager for MSX-DOS 2, based on the file manager for MS-DOS called FILMTN</p>
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
                <p>Learn MSX Basic from first principles and a brief introduction to machine code.</p>
              </article>
            </a>
          </li>
      </ul>
    </div>
  </div>
</div>