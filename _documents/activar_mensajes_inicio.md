---
titulo: Activar los mensajes durante el inicio del sistema
descripcion: Como ver los mensajes de carga del sistema Linux de la Raspberry Pi
autor: Rober
categoria: tutoriales
---
Cuando pulsamos el botón de encendido la pantalla se tira un buen rato en negro hasta que vemos el logo del MSXVR. Durante ese tiempo lo que ocurre es que está cargando el sistema Linux de la Raspberry Pi pero es práctica habitual en las distribuciones Linux ocultar los mensajes de carga del sistema.

Normalmente cuando se ocultan estos mensajes se muestra un logo con algún indicador de estado para indicar que el sistema está cargando, pero de momento esto no se ha personalizado en el MSXVR. El problema como seguramente alguna vez te habrá pasado es cuando el sistema no termina de cargar o incluso algunas veces carga pero notas que se ha demorado más de lo normal y no sabes por qué.

Activando esta configuración podemos ver los mensajes de carga del sistema Linux de la Raspberry Pi, de esta manera nada más pulsar el botón veremos que el sistema está funcionando lo que da una mejor sensación de que todo va bien o, si pasa algo, nos daremos cuenta de inmediato. Por ejemplo así descubrí que cuando tarda en cargar más de lo habitual es por que realiza un escaneo del sistema de ficheros en busca de errores, tarea que le demora un buen rato.

Para realizar esta configuración accederemos a la partición "boot" de la tarjeta SD lo cual podemos hacer desde Windows o Linux ya que está en formato FAT32 y abriremos con un editor de texto el fichero “cmdline.txt”, el cual por defecto tiene esta configuración(todo está en una línea muy larga):

```
dwc_otg.lpm_enable=0 console=serial0,115200 console=tty13 loglevel=3 
vt.global_cursor_default=0 root=PARTUUID=3f222e3d-02 rootfstype=ext4 
elevator=deadline fsck.repair=yes rootwait quiet logo.nologo 
usbhid.mousepoll=0 
```

Cambiaremos el parámetro “console” al valor “tty1” ya que es la consola que por defecto se activa al inicio pero además eliminaremos el parámetro “quiet” que es concretamente el que se encarga de ocultar los mensajes.

Si vamos a anular la carga del software del MSXVR como explico en este otro tema, deberemos eliminar o poner a “1” el parámetro “vt.global_cursor_default” ya que a “0” hace que se oculte el cursor lo que dificulta saber por donde vamos escribiendo cuando estamos en la terminal. En resumen la línea quedaría así:

```
dwc_otg.lpm_enable=0 console=serial0,115200 console=tty1 loglevel=3  
root=PARTUUID=3f222e3d-02 rootfstype=ext4 elevator=deadline fsck.repair=yes
rootwait logo.nologo usbhid.mousepoll=0
```

Ahora al iniciar el MSXVR veremos algo como esto:

![Mensajes de inicio](/assets/documents/activar_mensajes_inicio/mensajes_de_inicio.png)

Si queremos mejorar todavía más la sensación de respuesta en el encendido del MSXVR, podemos editar el fichero “config.txt” que también se encuentra en la partición “boot” y cambiar el parámetro “disable_splash” poniendo su valor a “0”:

```
disable_splash=0
```

De esta manera ahora al encender el MSXVR lo primero que vemos es una pantalla de colores que se corresponde al momento en el que la RPI inicializa la salida de vídeo ya que esto se produce antes de que se empiecen a mostrar los mensajes de carga.


![Pantalla de colores](/assets/documents/activar_mensajes_inicio/pantalla_de_colores_al_inicio.png)

Si tu monitor tarda en activar la imagen puede que no llegues a ver esta pantalla cuando enciendes el MSXVR pero sí deberías verla si haces un reinicio del MSXVR(desde el VR-DOS ejecutar “reset /hw”).