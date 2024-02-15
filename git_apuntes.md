# Comandos de GIT

### Se realizarán cambios mientras más se vayan agregando comandos en los apuntes. Mientras tanto se realizará la siguiente clasificación:

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

Restaurar un archivo a un commit anterior. Puedes cambiar **HEAD~1** (commit anterior) a cualquiera con el hashcode del commit requerido.

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

## Historial.

Muestra el historial de commits.

```ssh
    git log
```

Muestra el detalle de un commit en especifico

```ssh
    git show <hash_del_commit>
```

Muestra los archivos (blobs) de un commit en especifico

```ssh
    git ls-tree <hash_del_commit>
```

## Remoto.

## Etiquetas.

## Utilidades.

Muestra el estado del directorio de trabajo (Working Directory) y el área de preparación (Stagin area).

```ssh
    git status
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

## Otros.
