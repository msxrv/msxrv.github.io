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
            <img src="assets/img/telegram.png">
          </figure>
        </div>
        <div class="msxvr-link-description">
          <a href="https://telegram.org/">Telegram</a>
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
      {% assign primeros_pasos = site.documents | where: "categoria", "primeros_pasos" | where: "status" , status != "wip" %}
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
        {% assign programacion = site.documents | where: "categoria" , "programming" | where: "status" , status != "wip" %}
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
        {% assign tutoriales = site.documents | where: "categoria", "tutoriales" | where: "status" , status != "wip" %}
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
        <h1>Tutoriales</h1>
        <ul>
          <li>
            <a class="article" href="https://riunet.upv.es/bitstream/handle/10251/145214/Memoria.pdf?sequence=2&isAllowed=y">
              <article>
                <h3>Curso de Assembler rápido</h3>
                <p>Videotutoriales para iniciarse en la programación en ensamblador por BitVision.</p>
              </article>
            </a>
          </li> 
          <li>
            <a class="article" href="https://riunet.upv.es/bitstream/handle/10251/145214/Memoria.pdf?sequence=2&isAllowed=y">
              <article>
                <h3>Tutorial de desarrollo de videojuegos</h3>
                <p>Desarrollar videojuegos para el MSX a través de la compilación cruzada de proyectos mediante la librería FUSION-C.</p>
              </article>
            </a>
          </li>          
          <li>
            <a class="article" href="https://konamiman.github.io/MSX2-Technical-Handbook">
              <article>
                <h3>Z80 Assembly programming for the MSX and MSX2</h3>
                <p>Learn Assembly Programming with ChibiAkumas.</p>
              </article>
            </a>
          </li>
        </ul>
      </div>        
    <div class="box">
      <h1>Documentación técnica</h1>
      <ul>      
          <li>
            <a class="article" href="https://github.com/gseidler/The-MSX-Red-Book/blob/master/the_msx_red_book.md/">
              <article>
                <h3>The MSX Red Book</h3>
                <p>El objectivo de este libro es dar una descripcion del software y hardware estandard del MSX, con un nivel de detalle suficiente para satisfecer al usuario mas exigente, el programador de codigo maquina.</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="./assets/documents/lenguaje_maquina.pdf">
              <article>
                <h3>Lenguaje Máquina para MSX</h3>
                <p>El propósito que persigue este libro es enseñarte a programar en el código máquina de los ordenadores MSX, es decir, programar el microprocesador Z-80. Cuando digo que vas a aprender a programar, me refiero a que, al final de haber estudiado este libro, serás capaz de hacer por tt mismo rutinas que utilicen todo lo que te ofrece tu MSX.</p>
              </article>
            </a>
          </li>            
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
              <a class="article" href="https://8bitworkshop.com/v3.9.0/?platform=msx&file=helloworld.asm#">
                <article>
                  <h3>8bitworkshop</h3>
                  <p>Editor the codigo para maquinas de 8 bits en tu navegador</p>
                </article>
              </a>
            </li>
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
                </article>
              </a>
            </li>
            <li>
              <a class="article" href="https://www.msx.org/wiki/MultiMente">
                <article>
                  <h3>MultiMente</h3>
                  <p>Administrador de archivos para el MSX-DOS 2, basado en el administrador de archivos para MS-DOS FILMTN.</p>
                </article>
              </a>
            </li>
        </ul>
    </div>
  </div>
  <hr/>
  <div class="row">
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
            <a class="article" href="assets/documents//practical_msx_machine_code_programming_steve_webb.pdf">
              <article>
                <h3>Practical MSX Machine Code Programming</h3>
                <p>The intention of this book is to introduce you to Machine Code programming on MSX computers.</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="assets/documents/lenguaje_maquina.pdf">
              <article>
                <h3>Lenguaje Máquina Para MSX</h3>
                <p>Introducción y Conceptos avanzados.</p>
              </article>
            </a>
          </li>          <li>
            <a class="article" href="https://www.amazon.com/dp/1527298094?linkCode=ogi&th=1&psc=1&tag=sofferscom1-20">
              <article>
                <h3>Modern MSX BASIC Game Development</h3>
                <p>Desarrolla juegos retro en MSX Basic usando herramientas modernas.</p>
              </article>
            </a>
          </li>
          <li>
            <a class="article" href="https://www.amazon.com/FUSION-C-MSX-Library-complete-journey/dp/1730828612">
              <article>
                <h3>FUSION-C: MSX C Library complete journey</h3>
                <p>With FUSION-C you will be able to code games or any other softwares for the MSX computers, in C. The library is compatible for MSX1, MSX2, MSX2+, and MSX Turbo-R and can take advantage of the hardware of each model.</p>
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
                <p>Curso de programación de videojuegos en YouTube por la Memorial University</p>
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

