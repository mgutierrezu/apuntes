# Comandos de Linux

> Se realizarán cambios mientras más se vaya agregando información en los apuntes. Mientras tanto se realizará la siguiente clasificación:

## Clasificación de comandos Linux:

- [Gestión de archivos y directorios](#1-gestión-de-archivos-y-directorios)
- [Gestión de procesos](#2-gestión-de-procesos)
- [Gestión de usuarios y permisos](#3-gestión-de-usuarios-y-permisos)
- [Gestión de redes](#4-gestión-de-redes)
- [Gestión de paquetes y software](#5-gestión-de-paquetes-y-software)
- [Manipulación de texto y procesamiento de datos](#6-manipulación-de-texto-y-procesamiento-de-datos)
- [Administración del sistema y monitoreo](#7-administración-del-sistema-y-monitoreo)
- [Seguridad y cifrado](#8-seguridad-y-cifrado)
- [Sistema de archivos y almacenamiento](#9-sistema-de-archivos-y-almacenamiento)
- [Automatización y scripting](#10-automatización-y-scripting)

## 1. Gestión de archivos y directorios

- ### Manipulación básica

**ls (list):** Lista el contenido de un directorio.

```bash
ls /home/user/documents
```

**cd (change directory):** Cambia el directorio actual.

```bash
cd /var/www/html
```

**pwd (print working directory):** Muestra la ruta del directorio actual.

```bash
pwd
```

**mkdir (make directory):** Crea un nuevo directorio.

```bash
mkdir nuevo_directorio
```

**rmdir (remove directory):** Elimina un directorio vacío.

```bash
rmdir directorio_a_eliminar
```

**cp (copy):** Copia archivos y directorios.

```bash
cp archivo.txt /ruta/destino
```

**mv (move):** Mueve o renombra archivos y directorios.

```bash
mv archivo.txt /nueva/ruta
```

**rm (remove):** Elimina archivos o directorios.

```bash
rm archivo.txt
```

**touch:** Crea un archivo vacío.

```bash
touch nuevo_archivo.txt
```

**cat (concatenate):** Muestra el contenido de un archivo.

```bash
cat archivo.txt
```

**more:** Muestra el contenido de un archivo paginado.

```bash
more archivo.txt
```

**less:** Permite visualizar el contenido de un archivo de forma paginada.

```bash
less archivo.txt
```

**head:** Muestra las primeras líneas de un archivo.

```bash
head archivo.txt
```

**tail:** Muestra las últimas líneas de un archivo.

```bash
tail archivo.txt
```

- ### Búsqueda y localización

**find:** Busca archivos y directorios en función de diferentes criterios como nombre, tamaño, etc.

```bash
find /ruta -name "nombre_archivo"
```

**grep (Global Regular Expression Print):** Busca patrones en archivos de texto.

```bash
grep "patrón" archivo.txt
```

```bash

```

**locate:** Busca archivos mediante una base de datos previamente construida para una búsqueda más rápida.

```bash
locate archivo.txt
```

**which:** Muestra la ubicación de un ejecutable en el sistema de archivos.

```bash
which comando
```

**whereis:** Muestra la ubicación de archivos binarios, código fuente y páginas de manual relacionadas con un comando.

```bash
whereis comando
```

**updatedb (Update Database):** Actualiza la base de datos utilizada por el comando `locate` para realizar búsquedas rápidas.

```bash
sudo updatedb
```

**fd (Find Directory):** Una alternativa más moderna y rápida al comando `find`.

```bash
fd "patrón" /ruta
```

**ack (Acknowledgment):** Un reemplazo más potente y amigable de `grep` para buscar patrones en archivos.

```bash
ack "patrón" archivo.txt
```

**ag (Silver Searcher):** Otro reemplazo de `grep` optimizado para buscar rápidamente patrones en archivos.

```bash
ag "patrón" archivo.txt
```

**rg (RipGrep):** Una alternativa moderna y rápida a `grep` y `ag`.

```bash
rg "patrón" archivo.txt
```

## 2. Gestión de procesos

- ### Monitoreo de procesos
- ### Control de procesos

## 3. Gestión de usuarios y permisos

- ### Administración de usuarios
- ### Administración de grupos
- ### Gestión de permisos y propiedad

## 4. Gestión de redes

- ### Herramientas de diagnóstico
- ### Configuración de red
- ### Transferencia de archivos y comunicación remota

## 5. Gestión de paquetes y software

- ### Instalación y actualización de software
- ### Compilación y gestión de software desde código fuente
- ### Herramientas de empaquetado

## 6. Manipulación de texto y procesamiento de datos

- ### Visualización y concatenación
- ### Edición y transformación
- ### Búsqueda y filtrado de texto

## 7. Administración del sistema y monitoreo

- ### Información del sistema
- ### Gestión de servicios y procesos
- ### Monitoreo y logs

## 8. Seguridad y cifrado

- ### Gestión de llaves y certificados
- ### Seguridad de archivos
- ### Herramientas de auditoría y seguridad

## 9. Sistema de archivos y almacenamiento

- ### Gestión de particiones y volúmenes
- ### Sistemas de archivos y diagnóstico
- ### Manejo de cuotas de disco

## 10. Automatización y scripting

- ### Programación en shell
- ### Automatización de tareas
  }
