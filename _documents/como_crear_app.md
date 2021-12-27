---
titulo: Como crear un ejecutable
descripcion: Crea un paquete .APP ejecutable por una máquina MSXVR.
autor: Alberto
categoria: programming
order: 4
---
# ¿Qué es un APP?
Un APP o archivo con extensión .APP se trata de un paquete ejecutable por una máquina MSXVR.

Realmente el archivo es un ZIP (archivo comprimido con este formato) y que contiene una serie de archivos:

APP.XML
APP.PNG
Datos asociados a la aplicación (scripts, imágenes, audio, etc.)

Inspeccionando el contenido de una aplicación con ziptool.

# APP.XML
El archivo APP.XML contiene la siguiente información estructurada con el lenguaje de metadatos XML:

```xml
<?xml version="1.0" encoding="utf-8"?>
<icon name="app.png" />
<description 
bundle="com_demonvideogames_sj2"
name="Sky Jaguar 2"
developer="DemonVideogames"
date="01/01/2020" 
/>
<application name="data/scripts/game.pi" />
```

En este archivo encontraremos:

La cabecera de un archivo XML. Es de uso obligatorio.
El identificador del icono de la aplicación.
La descripción de la aplicación: nombre de bundle utilizado (uso obligatorio), nombre de la aplicación (uso obligatorio), desarrollador y fecha.
El script de arranque. Ruta relativa al contenido de zip. También de uso obligatorio.

# APP.PNG
El icono de la aplicación. Un archivo PNG con o sin transparencia.


Icono PNG de 256×256

# El Bundle
El bundle o nombre de bundle hace referencia a un identificador, único, de aplicación. Todos los scripts que operan bajo un nombre de bundle han de tener un namespace con el mismo nombre.

```
namespace com_demonvideogames_sj2;

class Game implements GL_Program
{
  ...
}
```

Esto es importante para la correcta ejecución de la aplicación. En caso contrario, pueden ocurrir errores de fallo en la carga de recursos o iniciación de otros scripts.

# Crear un ZIP
Una vez tenemos en una carpeta nuestros datos, app.xml y app.png, podemos crear un ZIP con este contenido. Esto podemos hacerlo bien desde el FileExplorer como por línea de comandos.

# Compilar Scripts
Si queremos compilar nuestros scripts para que no dejar expuesto el código fuente original, podemos usar la línea de comandos:

as /OUT *.pic *.pi
Esto generará tantos archivos con extensión «.pic» como archivos «.pi» encuentre. Una vez tengamos nuestros archivos «.pic» podemos renombrarlos de nuevo a la extensión «.pi» en la carpeta que vayamos a incluir dentro del ZIP