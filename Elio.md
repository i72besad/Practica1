Integrar ramas a la actual:


		git merge nombre_rama

Resolver conflictos(se suele hacer manualmante):

	
		git merge --abort


**Comandos Ramas III**

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


#0.5. GitHub

#GitHub no es Git


![Imagen de google](data:image/png;base64,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)

#Comandos GitHub I

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


#Comandos GitHub II
Ver *branches* remotos:


		git branch -r


Ver todos los *branches*:


		git branch -a 


Clonar un repositorio remoto:


		git clone url


#Dar seguimiento a *branches* remotos

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

#Operaciones con *branches* remotos

	* Creación:
	1. Crear branch local.
	2. Hacer cambios en dicho branch
	3. Hacer commit
	4. Copiar el branch al repositorio remoto:
		git push -u origin branch_remoto

	*copia:
		git checkout -b local remoto

	*Eliminación:
		git push origin --delete branch_remoto


		
