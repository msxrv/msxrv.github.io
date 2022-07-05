---
titulo: Como usar GitHub en el MSXVR
descripcion: Administra y versiona el codigo fuente de tus proyectos en GitHub
autor: Fluffy
categoria: programming
---
# Que es Git
Git es un sistema de control de versiones de software. Fue creado en 2005 por el creador de Linux, Linus Torvalds, para gestionar el desarrollo del kernel del sistema operativo.

Un sistema de control de versiones permite acceder, guardar y compartir en un servidor todo el historial del codigo fuente de una aplicacion o programa. Colbaroacion. Esto permite poder . Para equipos con multiples desarrolladores, un sistema de control de versiones tambien permite incorporar los cambios de los programadores de manera simultanea, con un sistema que permite unir sin que se pueda borrar . Y si por alguna razon se sobreescirbiera o borrara parte del codigo, al guardar todo el historal de codigo, siempre se puede revertir los cambiios.

Aunque existen otros sistemas de control de versiones, Git es actualmente y de lejos el mas popular. Se puede utilizar en modo de comandos o utilizar utilidades graficas disponibles para los diferentes sistemas operativos. La mayoria de editores de codigo como Visual Studio, Eclipse, XCode o Sublime tambien incluyen integracion nativa con Git.

# Que es GitHub
GitHub es una plataforma de alojamiento de servidores Git. La compania se creo en 2008 y fue aquirida por Microsoft en 2018. Aunque existen otros servicios de alojamiento Git como BitBucket y GitLab, GitHub es actualmente la plataforma mas popular para proyectos de software con mas de 200 millones de repositories de codigo.

GitHub tiene varios planes de pago disponibles, incluyendo un plan gratis con algunas limitaciones. Puedes encontrar mas informacion sobre los planes en https://github.com/pricing

## Como crear una cuenta en GitHub
Aunque no es estrictamente necesario si no tienes planteado subir codigo a GitHub, es recomendable empezar con crear un usuario en GitHub. Para esto, sigue los pasos indicados en la pagina https://github.com/join 

# Usando Git en el VR-DOS
El MSXVR, mediante el VR-DOS, viene con Git instalado por defecto. Estos son los comandos mas usados:

| Comando           | Descripcion                                       |
|:------------------|:--------------------------------------------------|
| git init          | Crea un nuevo repositorio de codigo               |
| git clone         | Clona un repositorio de codigo existente          |
| git status        | Muestra el estado del arbol de trabajo            |
| git log           | Muestra el historial de cambios
| git add           | Envia tus cambios a la zona staging               |
| git commit        | Guarda tus cambios en el repositorio local        |
| git pull          | Actualiza tu repositorio local                    |
| git push          | Sincroniza tu repositorio local con el remoto     |

Para poder accedar a un repositorio remoto Git, vas a tener que autenticarte con tu usuario. GitHub soporta 2 metodos principales, los token y los certificados de clave publica.  Una vez tengas una cuenta GitHub


