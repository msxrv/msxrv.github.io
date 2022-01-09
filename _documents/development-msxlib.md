---
titulo: Libreria para desarollo nativo MSXLIB
descripcion: Desarrolla juegos nativos compatibles MSX usando tu MSXVR
autor: Alberto
categoria: programming
url: https://msxvr.com/vros-development-msxlib/
---
# ¿Qué es MSXLIB?
Se trata de una librería para desarrollar juegos nativos compatibles MSX usando las herramientas que proporciona el MSXVR.

# Contenido
En la carpeta «SRC» podrás encontrar los fuentes de la librería. Dentro encontrarás un MAKE.BAT para compilar la librería según lo establecido en el archivo «msxlib_config.h».

Ejemplos en las distintas carpetas del repositorio. Cada ejemplo tiene su MAKE.BAT con el que podrá generar el archivo ROM, DSK, etc. según el caso. Y también el archivo «RUN.BAT» que te permitirá ejecutar en una máquina virtual, la ROM o archivo de salida generado.

En la carpeta «CRT» podremos encontrar los distintos puntos de entrada e inicialización de nuestros programas.
En la carpeta «MSXLIB.LIB» será nuestra librería compilada y que usarán los ejemplos del repositorio.

# Extensiones de archivo

| 	            	| 				                 |
|:------------------|:-------------------------------|
| .PI				| VR-SCRIPT nativo. Usa una sintaxis restrictiva con el fin de poder convertirlos en lenguaje ensamblador. |
| .ASM				| Archivo de texto que contiene lenguaje ensamblador. |
| .LIB				| Archivo binario que contiene una librería de código. |
| .MAP				| Archivo de texto que contiene información sobre cómo se han resuelto las direcciones de los distintos símbolos utilizados. También ofrece información sobre el tamaño ocupado por las distintas áreas de código y datos. |
| .SYM				| Archivo de texto con la lista de símbolos, direcciones e información de depuración que utilizará el depurador en tiempo real si así se lo indicamos.|
| .ROM				| Archivo binario con una cabecera (16 bytes) + datos |
| .BAT				| Archivos de procesamiento por lotes que se pueden ejecutar en VR-DOS y que desempeñan una secuencia de tareas. |

# Herramientas necesarias

| 	            	| 				                 |
|:------------------|:-------------------------------|
| AS Tool (VR-DOS)	| Para convertir los scripts, compilar los ASM y linkar el proyecto. |
| Player			| Para reproducir los ROM, DSK, etc. generados. |
| Player-Debugger	| Para depurar el código en tiempo de ejecución. |

# Instalación
Crear una carpeta:

```
C:>mkdir msxlib
C:>cd msxlib
C:/msxlib/>
```

Descargar el paquete con los fuentes y ejemplos:

C:/msxlib/>wget http://msxvr.es/resources/msxlib.zip
Una vez descargado:

```
C:/msxlib/>ziptool /E msxlib.zip
```

Esto descomprimirá el contenido del ZIP y podrás acceder al contenido citado previamente.

# Example 1
Hello World

### Example_1.pi

```
#include "msxlib.h"

class Example_1 partial MSXLIB_H
{
	function Init() : void
	{
		MSXLIB_Init();
	
		VDP_SetScreenMode(0);
		VDP_SetColor (8, 1);
		
		Screen_Print("HELLO WORLD!", 0, 0);
		Screen_Flush();
		
		while(1)
		{
		}
	}
} 
```

### Make.bat

```
as /OUT example_1.rom /CODE 0x4000 /DATA 0xC000 /CPU Z80 /INCLUDE ../src ../crt/msx_rom_crt.pi
```