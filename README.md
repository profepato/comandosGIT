# Comandos GIT
---------------------------
GIT (https://git-scm.com/)
---------------------------

/*-------------------CONFIGURACIÓN INICIAL----------------*/

git config --global user.email "patodeath@gmail.com"
git config --global user.name "pperezp"

/*-------------------CONFIGURACIÓN INICIAL----------------*/




/*----------------------PROXY-------------------------*/

git config --global http.proxy 192.168.241.14:8080 
git config --global --unset http.proxy

/*----------------------PROXY-------------------------*/


git config --global credential.helper 'cache --timeout=864000'


/*-------Conectar tu repositorio local con uno remoto------*/

git remote add origin URL	// Conectar
git remote -v			// Ve los repositorios remotos
git remote remove origin	// Quita el repositorio remoto

/*-------Conectar tu repositorio local con uno remoto------*/



git clone url				// Baja el proyecto de la nube
git status 					// ver el estado
git add . 					// añado todo cuando hago cambios
git commit -m "mensaje" 	// sube local
git push 					// envia a online
git pull 					// baja de online
git log						// Ve todos los commits
git log --pretty=oneline	// Ve todos los commits por linea solo con IDS
git log --pretty=format:"%h - %an, %ar : %s"
git checkout idCommit		// vuelve al estado del idCommit

INVESTIGAR amend para cambiar el mensaje de los commit


/*-----------------------------RAMAS-------------------------------*/

git branch nombre			// crea una nueva rama
git checkout nombreBranch	// cambio a esa rama
git checkout master			// vuelve al mas actual
git add .					// añadiendo antes de subir
git push origin nombreBranch		// Subiendo a GIT HUB

git branch -D NOMBRE_RAMA		// Eliminar una rama

// Mezclar master con rama
git checkout master
git merge nombreRama

// Eliminar una rama
git branch -d nombreRama

// Muestra grafico
git log --oneline --graph --all

// Muestra las ramas no fusionadas
git branch --no-merged

/*-----------------------------RAMAS-------------------------------*/


/*-------------------------TAGS-----------------------*/

// Los tags no se suben con los push

git tag -a v0.1 -m "Mensaje de versión"			// se le asigna al Ãºltimo commit
git tag -a v0.1 -m "Mensaje de versión"	SHA_COMMIT	// Tag a un commit en especÃ­fico
git push origin v0.1
git push origin --tags					// SUBE TODOS LOS TAGS QUE HEMOS CREADO

/*-------------------------TAGS-----------------------*/




/*--------------------------EQUIPO--------------------------*/

// Para cuando se trabaja en equipo, y existen cambios
// y hay que verificar si existe algun cambio

git fetch origin
git merge origin/master
git push origin/master

/*--------------------------EQUIPO--------------------------*/
