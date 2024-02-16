# Comandos de GIT

> Se realizarán cambios mientras más se vayan agregando comandos en los apuntes. Mientras tanto se realizará la siguiente clasificación:

## Clasificación de comandos GIT:

- Repositorio Local.
- Cambios.
- Ramas.
- Historial.
- Remoto.
- Etiquetas.
- Utilidades.
- Configuración.
- Otros.

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

## Ramas.

Cambiar a otra rama del árbol de trabajo.

```ssh
    git checkout <branch>
```

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

## Historial.

Muestra el historial de commits.

```ssh
    git log
```

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

## Utilidades.

Muestra el estado del directorio de trabajo (Working Directory) y el área de preparación (Stagin area).

```ssh
    git status
```

Crea atajos de teclado para evitar la redundancia en la escritura del código (Boilerplate text).

```ssh
    git config --global alias.<nombre> <comando>
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
