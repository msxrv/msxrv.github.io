---
titulo: Desactivar la carga del software del MSXVR.
descripcion: Toma el control del sistema antes de que este inicie.
autor: Rober
categoria: tutoriales
---
Antes de realizar esta configuración es conveniente [activar los mensajes durante el inicio del sistema](./activar_mensajes_inicio.html).

Desactivar la carga del software del MSXVR nos permitirá tomar el control del sistema antes de que este inicie, lo que nos dará acceso al terminal de comandos de Linux. Podremos configurar muchas cosas del sistema, como el acceso por SSH, acceder a la parción "boot", crear nuestros backups del MSXVR, montar memorias USB, etc. y en general no depender de otro PC para realizar modificaciones sobre los ficheros de la tarjeta SD.

Comentar que no es estrictamente necesario realizar esta configuración para acceder al terminal de Linux. Podemos cerrar el entorno del MSXVR haciendo lo siguiente. Desde el VR-DOS ejecutaremos "user developer" y cuando pregunte por la contraseña pulsamos directamente ENTER. Ahora ejecutamos "exit os" y saldremos a la terminal de comandos de Linux. Si lo que te interesa es desactivar la carga del software del MSXVR de forma permanente, algo que recomiendo para los que estamos haciendo pruebas y algunas veces el sistema se nos va al carajo, entonces sigue leyendo.

Un detalle a tener en cuenta es que desde la terminal de Linux no funciona ninguno de los botones del MSXVR, lo que confirma que estos botones son controlados por software, y solo funcionan desde el entorno del MSXVR.

La carga del software del MSXVR se realiza ejecutando el script “run” que se encuentra en el directorio “/root”. El script “run” es llamado desde el script “/etc/profile” el cual no es la mejor opción ya que ese fichero es ejecutado por cualquier usuario que inicie una sesión de terminal en el sistema. El caso es que para desactivar la ejecución de “run” hay que editar el fichero “/etc/profile” y anular la línea “run” que se encuentra al final del fichero. Así que saldremos al terminal de Linux tal como se ha explicado en el párrafo anterior y ejecutaremos la orden "nano /etc/profile" para editar el fichero. Para anular la línea "./run" poner una almohadilla “#” al inicio de la misma de manera que queda así:

```
#./run
```

Saldremos del editor pulsando Ctrl+X, luego la tecla "s" y Enter para confirmar. Una vez desactivada esa línea podemos comprobar(reboot para reiniciar) que ahora, al encender el MSXVR nos quedamos en la terminal de Linux. Si queremos iniciar el software del MSXVR sólo tenemos que ejecutar el script “run” acordándonos de poner siempre el “./” delante para indicar que el script está en el directorio actual, de lo contrario no lo encontrará y dará un error de “orden no encontrada”:

```
root@msxvr:~# ./run
```

Si queremos que el software del MSXVR vuelva a cargar automáticamente sólo tenemos que deshacer el cambio en el fichero “/etc/profile” y quitar la almohadilla, aunque como decimos este no es el sitio más idóneo para ello(si configuran el acceso por SSH comprenderán por qué) por lo que sugiero que añadan la orden “./run” en el fichero “.profile” del usuario "root"(es un fichero oculto por llevar un punto “.” delante) que se encuentra precisamente en su directorio principal o como se dice en Linux en la "$HOME" del usuario, y que para "root" la ruta no está en "/home" si no que al ser un usuario especial cuelga directamente de la raíz del sistema y está en "/root". Por ejemplo desde el Linux de la propia RPI se puede modificar fácilmente el ".profile" con el editor de texto “nano”:
CÓDIGO: SELECCIONAR TODO

```bash
nano ~/.profile
```

---
**NOTAS**: El carácter “~” sale pulsando AltGr+4. No es necesario añadir este carácter si ya estamos en el directorio principal del usuario, podemos ejecutar antes “cd” para asegurarnos. Para cerrar el editor pulsar Ctrl+X, luego la tecla “s” y luego ENTER para grabar los cambios.

---

A modo de ejemplo este es el contenido de mi “.profile”:
```
root@msxvr:~# cd
root@msxvr:~# cat .profile 
# ~/.profile: executed by Bourne-compatible login shells.
if [ "$BASH" ]; then
  if [ -f ~/.bashrc ]; then
    . ~/.bashrc
  fi
fi
mesg n || true
#./run
```

Con la orden “cd” sin argumentos nos aseguramos que nos movemos al directorio principal del usuario, en este caso "root", y la orden “cat” es el equivalente al “type” de MS-DOS para mostrar el contenido de un fichero. Como se observa he añadido la línea "./run" pero la tengo anulada ;)