# Comandos de GIT

> Se realizarán cambios mientras más se vayan agregando comandos en los apuntes. Mientras tanto se realizará la siguiente clasificación:

## Clasificación de comandos GIT:

- [Repositorio Local](#repositorio-local)
- [Cambios](#cambios)
- [Ramas](#ramas)
- [Merge](#merge)
- [Historial](#historial)
- [Remoto](#remoto)
- [Etiquetas](#etiquetas)
- [Utilidades](#utilidades)
- [Configuración](#configuración)
- [Otros](#otros)

## Repositorio Local.

Inicializar un nuevo repositorio GIT en un directorio.

```ssh
    git init
```

Clonar un repositorio GIT existente en un nuevo directorio.

```ssh
    git clone URL_del_repositorio
```

## Cambios.

Agregar cambios al área de preparación (Staging area).

```ssh
    git add archivo.txt
```

Registra los cambios en el repositorio. (Agregar mensaje simple y descriptivo)

```ssh
    git commit -m "Mensaje descriptivo al commit"
```

Descartar un commit hasta la posición X, se deberá de hacer un **git push origin +nombre_rama** para actualizar los cambios en remoto.

```ssh
    git reset HEAD~X
```

> Por defecto es --mixed, puedes usar --soft o --hard dependiendo de los requerimientos del cambio.

Restaurar un archivo a su estado en el último commit.

```ssh
    git restore archivo.txt
```

Restaurar un archivo desde Staging Area a Working Directory.

```ssh
    git restore --staged archivo.txt
```

Restaurar un archivo a un commit anterior. Puedes cambiar **HEAD~1** (commit anterior) a cualquiera con el hashcode del commit requerido. (Solo en Working Directory)

```ssh
    git restore --source=HEAD~1 archivo.txt
```

> Puedes reemplazar HEAD~1 por el nombre de la rama la cual quieres recuperar el archivo.

Elimina archivos de Stagin Area, GIT deja de hacer seguimiento al archivo indicado. (Útil para .gitignore)

```ssh
    git rm --cached archivo.txt
```

Ver los cambios en Stagin Area antes de llevarlos a repositorio. (commit)

```ssh
    git diff --cached
```

Ver los cambios en el directorio de trabajo. (Working Directory)

```ssh
    git diff
```

Modifica el commit mas reciente de la rama actual.

```ssh
    git commit --amend -m "Nuevo Mensaje"
```

## Ramas.

Cambiar a otra rama del árbol de trabajo.

```ssh
    git switch <branch>
```

> Se puede usar también **git checkout name_branch**, pero se recomienda usar switch.

Crea y cambia a una nueva rama del árbol de trabajo.

```ssh
    git checkout <new_branch>
```

Cambiar a un commit en especifico (modo "detached HEAD")

```ssh
    git checkout <hash_del_commit>
```

Restaura un archivo al Working Directory y Staging Area del commit indicado en el hash_code.

```ssh
    git checkout <hash_del_commit> archivo.txt
```

Elimina una rama existente

```ssh
    git branch -d branch_name
```

> Se deberá hacer una confirmación con -D si la rama no esta fusionada con la rama principal.

Muestra los commits de diferencia de branch_2 sobre branch_1.

```ssh
    git log branch_1..branch_2
```

Muestra la diferencia de codigo entre branch_2 sobre branch_1.

```ssh
    git diff branch_1..branch_2
```

Guarda los cambios no comiteados y nos permite cambiar de ramas.

```ssh
    git stash
```

> **git stash list:** Muestra la lista de todos los stash. <br> > **git stash show {index}:** Muestra los cambios del stash en específico.

Guarda los cambios no comiteados (y que no estan en Stagin Area) y nos permite cambiar de ramas.

```ssh
    git stash push -m "Mensaje de stash"
```

Aplica los cambios del ultimo stash y lo elimina del almacen stash.

```ssh
    git stash pop
```

> Si queremos hacer por separado esta funcion se puede aplicar **git stash apply / git stash drop** respectivamente.

Publica una rama de desarrollo en el repositorio remoto.

```ssh
    git push -u origin <nombre_rama>
```

> (**-u** = --set -upstream)

Elimina una rama de desarrollo del repositorio remoto.

```ssh
    git push -d origin <nombre_rama>
```

## Merge.

Combinar cambios de branch_name a la rama actual de trabajo.

```ssh
    git merge <branch_name>
```

> Por defecto el comando **git merge** realiza una merge tipo Fast-forward. <br>
> Si existen cambios en branch_name y en la rama actual de trabajo (puede ser **main** por defecto), se ejecutará un **3-ways merge**.

Combinar cambios de branch_name a la rama actual de trabajo, modalidad merge-commit (sin Fast-forward).

```ssh
    git merge --no-ff <branch_name>
```

Revertir los cambio realizados por un merge.

```ssh
    git revert -m 1 HEAD
```

> **-m 1:** Significa que revierte la fusión al padre principal (main).

Tomar algunos cambio realizados en otros commits sin hacer un merge.

```ssh
    git cherry-pick <Hash_commit>
```

Realiza un cambio en la base de la rama actual a la rama destino, dejando el historial de commits de manera lineal. (facilita el merge Fast-forward)

```ssh
    git rebase <rama_de_destino>
```

Reorganiza, edita o combina commits en la historia de la rama actual a partir del commit especificado en el Hash. (rebase interactivo)

```ssh
    git rebase -i <hash_del_commit>
```
> Agregando "^" al final del CLI. Puedes cambiar los mensajes de los commits remplazando "pick" por "reword".


Junta 2 commits consecutivos pequeños, se debe de eliminar la rama fusionada para limpiar el historial. (No se utiliza mucho este comando)

```ssh
    git merge --squash <rama_a_fusionar>
```

## Historial.

Muestra el historial de commits.

```ssh
    git log
```

Muestra todas las acciones realizadas en el historial de commits.

```ssh
    git reflog
```

> Util para recuperar commits eliminados.

Muestra el historial de commits en un archivo en especifico. (nombre de archivo siempre al final del CLI)

```ssh
    git log archivo.txt
```

Muestra la cantidad de commits de cada autor en el repositorio.

```ssh
    git shortlog
```

Muestra el historial de commits (una linea por commit).

```ssh
    git log --oneline
```

Muestra el historial de commits de manera completa.

```ssh
    git log --patch
```

Muestra el historial de commits de manera resumida.

```ssh
    git log --stat
```

> Puedes agregar lo siguiente para filtrar commits: <br>
> Por autor: **--author:"Mauricio"** <br>
> Por rango de fecha: **--after="2023-03-05"** **--before="last week"** <br>
> Por texto especifico en codigo: **-S"texto en codigo"** <br>
> Por texto especifico en commits: **--grep"text"** (Case sensitive)

Muestra el detalle de un commit en especifico

```ssh
    git show <hash_del_commit>
```

Muestra el contenido de archivo.txt hace 3 commits atras de HEAD.

```ssh
    git show HEAD~3:archivo.txt
```

> Puedes usar **--name-status** para ver solo los nombre de los archivos del commit, si fueron modificados, agregados o eliminados.

Muestra los archivos (blobs) de un commit en especifico

```ssh
    git ls-tree <hash_del_commit>
```

Muestra nombre, fecha y hora de los cambios (commits) realizados en un archivo.

```ssh
    git blame archivo.txt
```

## Remoto.

Enviar los cambios locales confirmados a un repositorio remoto.

```ssh
    git push
```

Trae los cambios desde un repositorio remoto a tu repositorio local.

```ssh
    git pull
```

> **git pull** = git fetch + git merge

Trae los cambios desde un repositorio remoto a tu repositorio local y se realiza un rebase de tus cambios locales sobre los cambios remotos.

```ssh
    git pull --rebase
```

> **git pull --rebase** = git pull + git rebase

Recupera todos los cambios y referencias de un repositorio remoto a tu repositorio local. (Por defecto es repositorio "origin" y la rama de "main")

```ssh
    git fetch
```

Clona el repositorio de la URL en el directorio actual. (puedes crear un nuevo directorio de trabajo)

```ssh
    git clone URL_HTTPS_PROYECTO <nombre_directorio_opcional>
```

Muestra una lista de los repositorios remotos.

```ssh
    git remote -v
```

## Etiquetas.

Crea una etiqueta para hacer referencia al commit señalado.

```ssh
    git tag <tag> <hash_commit>
```

> Ejemplo: git tag v1.0 abc123456

Crear una etiqueta y asignar un mensaje a la etiquera respectiva en el commit señalado.

```ssh
    git tag -a <tag> <Hash_commit> -m "mensaje"
```

> Ejemplo: git tag -a v1.0 abc123456 -m "Versión 1.0 - lanzamiento inicial del proyecto"

Subir la etiqueta al repositorio remoto.

```ssh
    git push origin <tag_name>
```

Eliminar la etiqueta del repositorio remoto.

```ssh
    git push origin --delete <tag_name>
```

## Utilidades.

Muestra el estado del directorio de trabajo (Working Directory) y el área de preparación (Stagin area).

```ssh
    git status
```

Herramienta para buscar un bug en el historial de commits, realiza una busqueda binara para encontrar el error (bug).

```ssh
    git bisect start

    git bisect good  / git bisect bad

    git bisect reset
```

Crea atajos de teclado para evitar la redundancia en la escritura del código (Boilerplate text).

```ssh
    git config --global alias.<nombre> <comando>
```

Muestra de manera grafica los commit en el historial. (Útil para ver merge)

```ssh
    git log --oneline --all --graph
```

## Configuración.

Configurar nombre del usuario.

```ssh
    git config --global user.name "Nombre Apellido"
```

Configurar email del usuario.

```ssh
    git config --global user.email mauricio@gmail.com
```

Abrir configuración en editor de texto.

```ssh
    git config --global -e
```

## Otros.

Elimina referencias locales a ramas remotas que ya no existen en repositorio remoto especificado (**origin**).

```ssh
    git remote prune origin
```
