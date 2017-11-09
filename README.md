## Página oficial de GIT
https://git-scm.com/

## Libro oficial PRO GIT en Español
https://git-scm.com/book/es/v2

## Repositorio del libro PRO GIT en Español
https://github.com/progit/progit2-es

## Configuración inicial
```
git config --global user.email "tu_correo@correo.com"
git config --global user.name "nombre_de_usuario"
```

## Ver una lista de configuraciones
```
git config --list
```

## Configuración de proxy
```
git config --global http.proxy 192.168.241.14:8080
git config --global https.proxy 192.168.241.14:8080 
```

## Desactivar el proxy
```
git config --global --unset http.proxy
```

## No colocar siempre las credenciales de github
```
git config --global credential.helper 'cache --timeout=864000'
```

## Inicializar un repositorio local
```
git init
```

## Conectar tu repositorio local con uno remoto
```
git remote add origin URL	// Conectar
git remote -v			// Ve los repositorios remotos
git remote remove origin	// Quita el repositorio remoto
```
## Comandos varios
```
git clone url                                 // Baja el proyecto de la nube
git status                                    // Ver el estado
git add .                                     // Añado todo cuando hago cambios
git commit -m "mensaje"                       // Sube local
git push                                      // Envía a online
git pull                                      // Baja de online
git log                                       // Ve todos los commits
git log --pretty=oneline                      // Ve todos los commits por linea solo con IDS
git log --pretty=format:"%h - %an, %ar : %s"
git checkout ID_COMMIT`                       // Vuelve al estado del ID_COMMIT
```
INVESTIGAR amend para cambiar el mensaje de los commit

## Ramas
```
git branch nombre               // Crea una nueva rama
git checkout nombreBranch       // Cambio a esa rama
git checkout master             // Vuelve al mas actual
git add .                       // Añadiendo antes de subir
git push origin nombreBranch    // Subiendo a GIT HUB
git branch -D NOMBRE_RAMA       // Eliminar una rama
```

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
```
git tag -a v0.1 -m "Mensaje de versión"             // Se le asigna al último commit
git tag -a v0.1 -m "Mensaje de versión"	SHA_COMMIT  // Tag a un commit en específico
git push origin v0.1
git push origin --tags                              // Sube todos los tags que hemos creado
```

# Trabajo en equipo

Para cuando se trabaja en equipo, y existen cambios y hay que verificar si existe algun cambio
```
git add .
git commit -m "Cambios propios"
git pull                // Se descargan y se mezclan los archivos
```
Si existen mezclas con conflicto, se deberán solucionar

```
git add .
git commit -m "Mezclando"
git pull
```
Este procese se hace mientras hayan cambios online.
Una vez que ya no hayan cambios online:
```
git push
```

## Colores en terminal
```
git config --global color.ui true
```
