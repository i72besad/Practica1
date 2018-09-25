


# 0.2. Instalación y configuración

## Instalación

* Para instalar Git: https://git-scm.com.
* En el curso se utilizará Git a través de líneas de comandos.
* Para eclipse existen *plugins* integrados: https://www.eclipse.org/egit.

## Configuración básica

Nombre del administrador:

	git config --global user.name "Antonio M. Durán Rosal"

Correo electrónico:

	git config --global user.email aduran@uco.es

Editor de texto:

	git config --global core.editor "gedit"


Color de la interfaz:

	git config --global color.ui true

Listado de la configuración:

	git config --global color.ui true

#0.3 Uso básico

##Los tres estados de Git

![Local Operations](http://1.bp.blogspot.com/-0ESPAhDYGQ4/ThMfRvj9FGI/AAAAAAAAAMM/Gifzuv9wwEA/s1600/git%2Blocal%2Boperations.jpg)

##Comandos básicos I

Iniciar repositorio en un directorio:

	git init

Agregar cambios al área de *staging*:

	git add

Validar cambios en el repositorio:

	git commit -m "Mensaje"

Hacer los dos pasos anteriores en uno:

	git commit -am "Mensaje"

Historial de commits:

	git log

##Comandos básicos II

Ayuda del listado anterior:

	git help log

Listar los 5 commits más recientes:

	git log -n 5

Listar los commits desde una fecha:

	git log --since=2018-09-18

Listar los commits por autor:

	git log --author="Antonio"

Ver cambios en el directorio:

	git status

##Comandos básicos III

Ver diferencia entre ficheros en el directorio y el repositorio de git:

	git diff

Ver diferencia entre ficheros en el *staging* y el repositorio:

	git diff --staged

Eliminar archivos:

	git rm archivo
	git commit -m "Mensaje"

Mover o renombrar archivos:

	git mv antiguo nuevo
	git commit -m "Mensaje"
