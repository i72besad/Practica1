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
	git branch -D nombre_rama