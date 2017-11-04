# Comandos GIT
## Página oficial de GIT
https://git-scm.com/

## Configuración inicial
```
git config --global user.email "tu_correo@correo.com"
git config --global user.name "nombre_de_usuario"
```

## Configuración de proxy
```
git config --global http.proxy 192.168.241.14:8080 
git config --global --unset http.proxy
```

## No colocar siepre las credenciales de github
```
git config --global credential.helper 'cache --timeout=864000'
```

## Conectar tu repositorio local con uno remoto
```
git remote add origin URL	// Conectar
git remote -v			// Ve los repositorios remotos
git remote remove origin	// Quita el repositorio remoto
```
## Comandos varios

`git clone url`				// Baja el proyecto de la nube
`git status` 					// ver el estado
`git add .` 					// añado todo cuando hago cambios
`git commit -m "mensaje"` 	// sube local
`git push` 					// envia a online
`git pull` 					// baja de online
`git log`						// Ve todos los commits
`git log --pretty=oneline`	// Ve todos los commits por linea solo con IDS
`git log --pretty=format:"%h - %an, %ar : %s"`
`git checkout ID_COMMIT`		// vuelve al estado del idCommit
INVESTIGAR amend para cambiar el mensaje de los commit

## Ramas
`git branch nombre`			// crea una nueva rama
`git checkout nombreBranch`	// cambio a esa rama
`git checkout master`			// vuelve al mas actual
`git add .`					// añadiendo antes de subir
`git push origin nombreBranch`		// Subiendo a GIT HUB
`git branch -D NOMBRE_RAMA`		// Eliminar una rama

### Mezclar rama master con una rama
```
git checkout master
git merge nombreRama
```
### Eliminar una rama
```
git branch -d nombreRama
```
### Muestra grafico
```
git log --oneline --graph --all
```

## Mostrar las ramas no fusionadas
```
git branch --no-merged
```

# Tags
Los tags no se suben con los push

`git tag -a v0.1 -m "Mensaje de versión"`			// se le asigna al Ãºltimo commit
`git tag -a v0.1 -m "Mensaje de versión"	SHA_COMMIT`	// Tag a un commit en especÃ­fico
`git push origin v0.1`
`git push origin --tags`					// SUBE TODOS LOS TAGS QUE HEMOS CREADO


# Trabajo en equipo

Para cuando se trabaja en equipo, y existen cambios y hay que verificar si existe algun cambio
```
git fetch origin
git merge origin/master
git push origin/master
```
