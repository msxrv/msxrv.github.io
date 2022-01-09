---
titulo: Editor de texto
descripcion:  Como configurar el editor de texto
autor: Alberto
categoria: primeros_pasos
link: https://msxvr.com/vros-app-texteditor/
order: 3
---
# Funcionalidad
El editor de texto es una herramienta que nos permite editar archivo de texto bien de uso documental, datos o para programación.

La forma de invocarse desde VR-DOS es:

```
C:/> edit
```

O bien podemos indicar un archivo existente o nuevo que queramos editar:

```
C:/> edit catalogo.bat
```

# Menú
![Menu](/assets/documents/vros-texteditor/menu.png)

# Archivo INI
## Local
Al iniciar el editor se busca la existencia de un archivo «edit.ini» ubicado en la misma carpeta desde la que se ejecuta. En caso de hallarse, se leerá e inicializará el editor en función de su contenido. Un ejemplo:

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

```s
fontsize=2
linenumbers=true
theme=dark
runpath=D:/tuto_demo/monkey/monkey.pi
runparams=
project=true
logger=false
codehelper=false
openfile=D:/tuto_demo/monkey/monkey.pi
windowed=true
```

## Genérico
Del mismo modo que el local, también se buscará un archivo en «$SYSTEM:/user/edit_config.ini». En caso de encontrarse, se leerá su contenido e inicializará el editor. NOTA: Los parámetros leídos en el INI Local siempre son más prioritarios que el genérico.

```
fontsize=12
fontname=lucon
theme=dark

[common-colors-bright]
fg_default=RGB(0,0,0)
fg_comment=RGB(150,150,150)
fg_number=RGB(255,0,0)
fg_string=RGB(255,0,0)
fg_label=RGB(100,100,100)
fg_preprocessor=RGB(0,200,0)
fg_reserved_1=RGB(0,162,232)
fg_reserved_2=RGB(0,100,200)
fg_delimiter_hl=RGB(255,255,255)
bg_delimiter_hl=RGB(255,0,255)
fg_delimiter=RGB(0,0,0)

[common-colors-dark]
fg_default=RGB(255,255,255)
fg_comment=RGB(100,100,100)
fg_number=RGB(255,0,0)
fg_string=RGB(255,0,0)
fg_label=RGB(132,240,109)
fg_preprocessor=RGB(0,255,0)
fg_reserved_1=RGB(0,162,232)
fg_reserved_2=RGB(0,100,200)
fg_delimiter_hl=RGB(255,255,255)
bg_delimiter_hl=RGB(255,0,255)
fg_delimiter=RGB(255,255,255
```

## Propiedades que se pueden establecer en un INI

| Key	            | Concepto                      |
|:------------------|:------------------------------|
|[generic]	        | A partir de aquí se pueden usar las claves son de uso genérico. Este contexto es el que hay por defecto en cualquier INI. |
| [common-colors-bright] | Establece los colores para el tema «bright» de todos los modos de resaltado de sintaxis existentes.|
| [common-colors-dark]	| Establece los colores para el tema «dark» de todos los modos de resaltado de sintaxis existentes. |
| [vrscript-colors-bright]	| Establece los colores para el tema «bright» del resaltado de sintaxis «vrscript». |
| [vrscript-colors-dark]	| Establece los colores para el tema «dark» del resaltado de sintaxis «vrscript». |
| [basic-colors-bright]	| Establece los colores para el tema «bright» del resaltado de sintaxis «basic». |
| [basic-colors-dark]	| Establece los colores para el tema «dark» del resaltado de sintaxis «basic». |
| [asm-colors-bright]	| Establece los colores para el tema «bright» del resaltado de sintaxis «asm». |
| [asm-colors-dark]	| Establece los colores para el tema «dark» del resaltado de sintaxis «asm». |
| fontsize = int	| Tamaño de la fuente de letra (por defecto: 12) |
| fontname = string	| Nombre de la fuente de letra (por defecto: consola) |
| linenumbers = true \| false	| Mostrar número de línea (por defecto: false) |
| theme = bright \| dark	| Tema de colores (por defecto: bright) |
| runpath = string	| Ruta de archivo a ejecutar (por defecto: vacío) |
| runparams = string	| Parámetros de ejecución (por defecto: vacío) |
| project = true \| false	| Panel de proyecto abierto (por defecto: false) |
| logger = true \| false	| Panel de logger abierto (por defecto: false) |
| codehelper = true \| false	| Panel de code helper abierto (por defecto: false) |
| openfile = string	\| Abrir archivo (por defecto: vacío) |
| windowed = true \| false	| Archivo en modo ventana (por defecto: false) |
| fg_default = color	| Color de tinta del texto |
| fg_comment = color	| Color de tinta para los comentarios |
| fg_number = color	| Color de tinta para los números |
| fg_string = color	| Color de tinta para las cadenas (Texto entre comillas) |
| fg_label = color	| Color de tinta para las etiquetas |
| fg_preprocessor = color	| Color de tinta para las claves de preprocesador (#) |
| fg_reserved_1 = color	| Color de tinta para las palabras reservadas de tipo 1 |
| fg_reserved_2 = color	| Color de tinta para las palabras reservadas de tipo 2 |
| fg_delimiter_hl = color	| Color de tinta para la marca de comienzo y fin de ámbito (por defecto: RGB(255,255,255)) |
| fg_delimiter = color	| Color de tinta para los delimitadores |
| bg_default = color	| Color de fondo para el texto (por defecto: transparente) |
| bg_comment = color	| Color de fondo para los comentarios (por defecto: transparente) |
| bg_number = color	| Color de fondo para los números (por defecto: transparente) |
| bg_string = color	| Color de fondo para las cadenas (por defecto: transparente) |
| bg_label = color	| Color de fondo para las etiquetas (por defecto: transparente) |
| bg_preprocessor = color	| Color de fondo para las claves de preprocesador (por defecto: transparente) |
| bg_reserved_1 = color	| Color de fondo para las palabras reservadas de tipo 1 (por defecto: transparente) |
| bg_reserved_2 = color	| Color de fondo para las palabras reservadas de tipo 2 (por defecto: transparente) |
| bg_delimiter_hl = color	| Color de fondo para la marca de comienzo y fin de ámbito (por defecto: RGB(255,0,255)) |
| bg_delimiter = color	| Color de fondo para los delimitadores (por defecto: transparente) |

## Color
\<color\> puede expresarse como RGB(r, g, b) o ARGB(a, r, g, b). Siendo el valor transparente = 0.

# Panel de proyecto
Lo abriremos y cerraremos usando el atajo de teclado: LCTRL + P o desde el menú View -> Project.

![Panel de proyecto](/assets/documents/vros-texteditor/panel_proyecto.png)

Este panel podemos ubicarlo y redimensionarlo en la zona de trabajo del editor. Esta información se almacena, de modo que si cerramos el editor y volvemos a abrirlo, todo permanecerá en su posición y tamaño.

El panel de proyecto se ubica siempre en el directorio de trabajo, desde donde se ha invocado el editor o desde la ruta en la que se encuentra el archivo de texto abierto.

Las subcarpetas se representan entre corchetes y al hacer doble-click accedemos a las mismas pudiendo volver atrás usando la carpeta «[..]»

Los diferentes tipos de archivo se representan en colores distintos. Si un archivo tiene una extensión que está vinculada a una aplicación del sistema, al hacer doble-click se procederá abrirse con dicha aplicación. En el caso de los archivos de textos, al abrirse, se harán sobre la misma instancia de aplicación en la que estamos. De manera que el archivo en curso, si está modificado se guardará automáticamente y se procederá a abrir el nuevo. En caso de que el archivo en curso no tenga nombre, se abrirá el diálogo de archivos y se nos pedirá asignarle uno.

El panel tiene en la parte de arriba un control de texto que opera como filtro. Esto nos permite filtrar por coincidencia de texto los distintos archivos que hayan en la carpeta facilitándonos la búsqueda o acceso.

# Panel de logger
Los abriremos y cerramos usando el atajo de teclado: LCTRL + L o a través del menú View -> Project.

![Panel de logger](/assets/documents/vros-texteditor/panel_logger.png)

Desde este panel podemos ver los distintos mensajes de log que puedan ocurrir durante la ejecución un programa en el editor. Este panel tiene una caja de texto que actúa como filtro para facilitar la búsqueda de mensajes. También tiene un botón de «Clear» que borrará todos los mensajes existentes en el panel.

# Panel de inspección de clases
Lo abriremos y cerraremos usando el atajo de teclado: LCTRL + H o a través del menú View -> Code Helper.

![Panel de inspeccionb](/assets/documents/vros-texteditor/panel_inspeccion1.png)

Por un lado, la primera caja de texto nos permite indicar la clase que queremos inspeccionar. La segunda caja de texto actuará como filtro de las funciones encontradas, por ejemplo:

![Panel de inspeccionb](/assets/documents/vros-texteditor/panel_inspeccion2.png)


El inspector nos permite navegas entre las distintas funciones de una clase y nos ofrece información.

![Panel de inspeccionb](/assets/documents/vros-texteditor/panel_inspeccion3.png)


# Resaltado de sintaxis
En función del tipo de extensión de archivo que estemos editando, automáticamente se activará el resaltado de sintaxis. Si el archivo no tiene una extensión reconocida por ningún resaltador, no se aplicará. Los resaltadores actuales son:

| Extensión	        | Tipo                          |
|:------------------|:------------------------------|
| .pi	            | Archivo de VR-Script          |
| .bas	            | Archivo BASIC o VR-Basic      |
| .asm	            | Archivo ensamblador           |

# Atajos de teclado

| Atajo	            | Funcionalidad                 |
|:------------------|:------------------------------|
| LCTRL + S	        | Guardar archivo               |
| LCTRL + LSHIFT + S| Guardar archivo como          |
| LCTRL + N	        | Archivo nuevo                 |
| LCTRL + O	        | Abrir archivo                 |
| LCTRL + Q	        | Cerrar archivo y Salir        |
| LCTRL + P	        | Abrir/Cerrar panel de proyecto|
| LCTRL + H	        | Abrir/Cerrar panel de inspector de clases |
| LCTRL + L	        | Abrir/Cerrar panel de logger  |
| LCTRL + Z	        | Deshacer                      |
| LCTRL + Y	        | Rehacer                       |
| LCTRL + C	        | Copiar                        |
| LCTRL + V	        | Pegar                         |
| LCTRL + X	        | Cortar                        |
| LALT + DELETE	    | Borrar línea actual           |
| LCTRL + K	        | Borrar línea actual           |
| LCTRL + R	        | Ejecutar programa             |
| LALT + UP	        | Mover línea hacía arriba      |
| LALT + DOWN	    | Mover línea hacía abajo       |
| LCTRL + A	        | Seleccionar todo el texto     |
| LCTRL + F	        | Abrir panel de búsqueda       |
| F3	            | Siguiente búsqueda            |
| LCTRL + NEXT	    | Buscar siguiente función      |
| LCTRL + PREV	    | Buscar anterior función       |

# Modo ventana / completo
Es posible establecer la ventana del archivo en edición en dos modos. Por defecto (salvo indicado en un INI) se abrirá el archivo de texto en modo completo. Esto no permite redimensionar la ventana ni cambiar su posición dentro del área de trabajo. En modo Ventana si sería posible ajustar posición y tamaño dentro del área de trabajo. El modo ventana está pensado para usarse en combinación con los paneles de proyecto y logger, o sea, cuando se usa el editor en modo de desarrollador.

# Ejecutar un script
Si estamos editando un script y queremos lanzarlo, usaremos el atajo LCTRL + R o a través del menú Edit -> Run.

Por defecto se lanza el script del archivo de texto en curso, sin embargo, es posible poder establecer otro archivo de script de manera que podamos estar editando diferentes archivos y lanzar únicamente el que hace referencia a nuestro programa de arranque.

![Panel de propiedades de ejecución](/assets/documents/vros-texteditor/ejecutar_script.png)

---
**NOTA**: Aunque pongamos un nombre de archivo, si tenemos activado el check de «siempre ejecutar el archivo abierto», se ignorará, o sea, siempre ejecutaremos el archivo abierto en curso.

---

