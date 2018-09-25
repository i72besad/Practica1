Integrar ramas a la actual:

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


		

