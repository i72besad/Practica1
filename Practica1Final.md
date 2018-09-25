


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

# 0.3 Uso básico

## Los tres estados de Git

![Local Operations](http://1.bp.blogspot.com/-0ESPAhDYGQ4/ThMfRvj9FGI/AAAAAAAAAMM/Gifzuv9wwEA/s1600/git%2Blocal%2Boperations.jpg)

## Comandos básicos I

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

## Comandos básicos II

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

## Comandos básicos III

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
## Comandos básicos IV

Deshacer cambios con git:

	git checkout -- nombre_fichero

Retirar archivos del *stagin*:

	git reset HEAD nombre_fichero

Complementar último commit:

	gir commit --amend -m "Mensaje"

Recuperar versión de un fichero de commit antiguo:

	git checkout <id_commit> -- nombre_archivo

Revertir un commit:

	git revert <id_commit>

## Comandos básicos V

Deshacer múltiples cambios en el repositorio:

	git reset --soft <id_commit>
	git reset --mixed <id_commit>
	git reset --hard <id_commit>

Listar archivos que git no controla:

	git clean -n

Eliminar archivos que git no controla:

	git clean -f

Ignorar archivos en el repositorio: .gitignore

## Comandos básicos VI

Listar el contenido del repositorio de git:

	git ls-tree master
	git ls-tree master^^^
	git ls-tree master~3

Log en una línea:

	git log --oneline

Log con los tres últimos commits en una línea:

	git log --oneline -3

Para más opciones consultar documentación de git.

## Comandos básivos VII

Examinar el contenido de un commit:

	git show <id>

Comparar un commit con el actual:

	git diff <id> nombre_archivo

Comparar dos commits:

	git diff id..id nombre_archivo

# 0.4. Ramas
## Ramas o *Branches*

Es la forma para separar la l´ınea actual de desarrollo con respecto a la principal. Normalmente
representan versiones del software que posteriormente son integradas a la línea principal.

![Imagen de Ramas o Branches](https://i.stack.imgur.com/mvLUy.png)

## Comandos Ramas I

Ver listado de ramas:

	git branch

Crear una rama:

	git branch nombre_rama

Cambiarnos a una rama:

	git checkout nombre_rama

Crear una rama y moverse en un paso:

	git checkout -b nombre_rama

Comparar ramas:

	git diff nombre_rama..nombre_rama

## Comandos Ramas II

Ver ramas identicas a la actual:

	git branch --merged

Renombrar ramas:

	git branch -m nombre_antiguo nombre_nuevo

Eliminar ramas:

	git branch -d nombre_rama
	git branch -D nombre_ramaIntegrar ramas a la actual:

	git merge nombre_rama

Resolver conflictos(se suele hacer manualmante):

	git merge --abort

## Comandos Ramas III

Almacenar cambios temporales:

	git stash save "Mensaje"

Listar cambios:

	git stash list

Ver contenido de un cambio temporal:

	git stash show -p nombre_stash

Ver contenido de un cambio temporal:

	git stash show -p nombre_stash

Eliminar un cambio temporal:

	git stash drop nombre_stash

Aplicar cambio del *stash:*

	git stash apply nombre_stash
	git stash pop nombre_stash

# 0.5. GitHub

## GitHub no es Git

![Imagen de Google](http://1.bp.blogspot.com/-WY2YpNr3W6g/UY6tZAc-H3I/AAAAAAAABLY/xJ9x3wIY8V8/s1600/Github2.png)

## Comandos GitHub I

Añadir repositorio remoto:

	git remote add origin url

Ver repositorios remotos:

	git remote add origin url

Ver repositorios remotos:

	git remote -v 

Eliminar repositorio remoto:

	git remote rm origin

Añadir cambios del repositorio local al remoto:

	git push -u origin master

Añadir cambios del repositorio remoto al local:

	git pull

## Comandos GitHub II

Ver *branches* remotos:

	git branch -r

Ver todos los *branches*:

	git branch -a 

Clonar un repositorio remoto:

	git clone url

**Dar seguimiento a *branches* remotos**

* LOCAL->REMOTO

	1. Cambios en el repositorio local.
	2. Commit de los cambios.
	3. Añadir cambios a repostorio remoto:
	
			git push
		
* REMOTO->LOCAL
	
	* Sincronización y unión:
	
			git fetch origin
			git merge origin/master


	* En un solo paso:
	
			git pull

**Operaciones con *branches* remotos**

* Creación:
	1. Crear branch local.
	2. Hacer cambios en dicho branch
	3. Hacer commit
	4. Copiar el branch al repositorio remoto:
		
			git push -u origin branch_remoto

* Copia:
		
		git checkout -b local remoto

* Eliminación:
		
		git push origin --delete branch_remoto


		

