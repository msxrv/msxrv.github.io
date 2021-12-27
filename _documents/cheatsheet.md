---
titulo: Cheat Sheet
descripcion: Comandos útiles para ejecutar en VR-DOS
autor: Aorante
categoria: primeros_pasos
order: 2
---
# Cargando software con PLAY
Hemos recopilado algunos comandos útiles para ejecutar con el player de MSXVR (Play).

|  Descripción | Comando |
|:-------------|:--------|
| Ejecutar fichero.rom usando la máquina MSX2 por defecto del sistema | PLAY FICHERO.ROM /MSX2 |
| Ejecutar fichero.rom usando la máquina MSX2+ por defecto del sistema | PLAY FICHERO.ROM /MSX2P o PLAY FICHERO.ROM /MSX2+ | 
| Ejecutar fichero.rom usando la máquina MSX2+ Extra | PLAY FICHERO.ROM /MODEL MSX2P_EXTRA |
| Ejecutar fichero.rom usando la máquina MSX Turbo R por defecto del sistema | PLAY FICHERO.ROM /MSXTR |
| Ejecutar un cartucho introducido en el SLOT 3	| 1) GR /OFF 2) Insertar Stevedore en SLOT#3 3) GR /ON 4) En VR-DOS escribir: play *.rom /mapper vri /grslot1 3 |
| Ejecutar un cartucho introducido en el SLOT 4	| 1) GR /OFF 2) Insertar Stevedore en SLOT#4 3) GR /ON4) En VR-DOS escribir: play *.rom /mapper vri /grslot1 4 |
| Arranca una máquina MSX2 con Nextor y tenemos unidad A: con Nextor y la unidad C: que es la unidad en la que estabas en VRDOS	| PLAY *.ROM /MSX2 /VRT |
| Ejecuta en un MSXTR, un fichero rom añadiendo la tarjeta de video v9990 y mapeando una tarjeta de sonido Moonsound | play archivo.rom /dev v9990 /video v9990 /mapper2 moonsound /msxtr |
| Ejecuta en un MSXTR, un fichero rom añadiendo la tarjeta de video v9990 y mapeando una tarjeta de sonido opl4	| play archivo.rom /dev v9990 /video v9990 /opl4 /model msxtr |
| Apaga la alimentación de los cartuchos | gr /off |
| Enciende la alimentación de los cartuchos	| gr /on |
| Ejecuta un cartucho físico insertado en el slot 2	| gr /S2 /r |
| Para borrar la flash de un cartucho | GR /S1 /E |
| Para grabar una rom en un cartucho flash | GR /S1 /L smw.rom ASCII16 |
| Aplica el parche valis1.ips a la imagen de disco valis1.dsk y crea una nueva imagen de disco llamada valis1_con_ips.dsk | gr /IN valis1.dsk /IPS valis1.ips /OUT valis1_con_ips.dsk |
| Ejecuta la rom USAS.ROM y le aplica, en vuelo, el parche PARCHE_VISTOR_USAS.ips, pero sin afectar a la rom original. | play USAS.ROM /ips PARCHE_VICTOR_USAS.ips |
| Ejecuta el disco de la unidad a: sdsant1.dsk aplicándole un mapper konami5 sin sonido SCC	| play a:sdsnat1.dsk /mapper1 konami5 |
| Ejecuta el disco de la unidad a: sdsant1.dsk aplicándole un mapper konamiscc de modo que tenemos sonido SCC | play a:sdsnat1.dsk /mapper1 konamiscc |
| Asigna al vuelvo la cantidad de memoria ram que quieras para tu MSX: 128, 256, 512, 1024, 2048, …	| play *.rom /ram 1024 |

# Entorno VRDOS
Aquí encontrarás algunos comandos que te facilitarán la vida en el uso del entorno VRDOS. ¡Vuelve a sentir la línea de comandos en tus dedos!

|  Descripción | Comando |
|:-------------|:--------|
| Fija la hora del sistema en la zona de España	| time /a /z Madrid |
| Montar ftp en la unidad E: | MOUNT /RW E: ftp://[dirección IP/DNS]/[directorio] |
| Montar Samba en la unidad B: | MOUNT /RW B: SAMBA://192.168.0.198/Datos |
| Montar samba de lectura y escritura en la unidad b: pasando por parámetro el usuario y el password | mount /rw b: samba:usuario:password@ip_host |
| Montar FTP de lectura y escritura en la unidad f: pasando por parámetro el usuario y el password | mount /rw f: ftp:usuario:password@host:puerto |
| Primero creamos un fichero .zip | ZIPTOOL /c backup.zip |
| Después añadimos los ficheros que deseamos a dicho .zip | ZIPTOOL /a backup.zip *.* |
| Extraemos el contenido del fichero .zip | ZIPTOOL /e backup.zip |
| Si quieres quitarle la protección de escritura de disco (DSK): | PLAY DISCO.DSK /dskwra |

# Mantén a punto tu sistema MSXVR
No te olvides de mantener al día tu MSXVR. Aquí puedes tener algunas ideas.

|  Descripción | Comando |
|:-------------|:--------|
| Restaura todas las configuraciones de las Máquinas Virtuales a sus versiones originales | PKG /RESTORE VMACHINES |
| Descarga todas las ROMS de las Máquinas Virtuales | PKG /INSTALL SYSTEM_VMACHINES_ROMS |
| Actualiza el sistema a la última versión disponible | PKG /CLEAN /UPDATE |
| Actualiza el sistema a la última versión disponible directamente sin pedir confirmación | PKG /CLEAN /UPDATE /Y |
| Actualiza el sistema a la versión en desarrollo. Esta opción es solo para valientes ya que el sistema se puede volver inestable. Usar bajo vuestro propio riesgo	| 1) Escribir en la línea de comando «user developer» 2) Cuando el sistema solicite la contraseña pulsar ENTER 3) ejecutar PKG /CLEAN /UPDATE |

# A vueltas con el Debugger
Aquí encontrarás algunas utilidades para facilitarte el uso del debugger.

|  Descripción | Comando |
|:-------------|:--------|
| Ver o situarse en un segmento de memoria | VIEW dirección (ejemplo: 0xc000 para c000) |
| Encontrar un valor, por ejemplo Find 2 para encontrar el valor 2 | FIND valor |
| Hacer copia del estado actual de la memoria | DUMP MEM AUX |
| Seguir ejecutando el juego para provocar un cambio (ejemplo una vida menos) . Para volver al Debbuger CTRL+ALT+C	| RUN |
| Encontrar donde antes había un valor y ahora otro. | COMPARE valorActual valorAnterior |
| Colocar un valor en una dirección. Ejemplo Poke 0xC003 0x99 CTRL+ALT+C | POKE dirección valor |