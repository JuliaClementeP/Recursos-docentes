# Tutorial Pedagógico sobre Git y GitHub

## Introducción: Diferencias entre Git y GitHub

- **Git** es un sistema de control de versiones distribuido. Permite gestionar el historial de cambios de un proyecto y facilita el trabajo colaborativo en el código.
- **GitHub**, por otro lado, es una plataforma de alojamiento de proyectos que utiliza Git para gestionar el código. Aunque están relacionados, Git y GitHub son herramientas independientes.

---

## Conceptos Básicos

### 1. Repositorio Git
Cuando ejecutas `git init` en un proyecto, Git crea un directorio oculto llamado `.git`. Este directorio es el que Git utiliza para llevar el control de versiones de tu proyecto.

### 2. Estado del Proyecto
En este punto, podrías estar en la rama principal (generalmente llamada `main`), pero aún no habrás hecho ningún commit:

```bash
No commits yet
```

Archivos como `.DS_Store`, que son creados automáticamente en sistemas macOS, no suelen ser necesarios para el proyecto, por lo que se pueden ignorar utilizando el archivo `.gitignore`.

### 3. Visualizar el Historial de Cambios
Para ver los cambios que has realizado en tu proyecto, puedes utilizar el comando:

```bash
git log
```
Este comando te mostrará el historial de commits que has hecho en tu proyecto.

### 4. Moviéndote a un Punto Específico del Historial
Si necesitas volver a un estado anterior del proyecto, puedes usar:

- `git checkout <nombre del archivo>`: Te posiciona en un commit o archivo en particular.
- `git reset`: Te lleva de vuelta a una "fotografía" anterior del proyecto, descartando los cambios posteriores.

Para visualizar de manera gráfica la historia del proyecto, puedes usar:

```bash
git log --graph
```
Puedes agregar opciones para simplificar la salida:

```bash
git log --graph --pretty=oneline
git log --graph --decorate --all --oneline
```

### 5. Crear Alias para Comandos
Si deseas simplificar comandos, puedes crear alias. Por ejemplo, el siguiente alias crea una representación gráfica simplificada del historial:

```bash
git config --global alias.tree "log --graph --decorate --all --oneline"
```

### 6. Ignorar Archivos con `.gitignore`
El archivo `.gitignore` te permite especificar qué archivos o carpetas deben ser ignorados por Git. Un ejemplo común es ignorar archivos `.DS_Store` en macOS:

```bash
**/.DS_Store
```
El uso de asteriscos (`**`) asegura que el archivo `.DS_Store` sea ignorado sin importar en qué directorio se encuentre.

---

## Comparando Cambios

### 7. Diferencias sin Hacer Commit
Para ver los cambios que has realizado sin necesidad de hacer un commit, puedes usar el comando `git diff`. Te muestra las diferencias entre tu archivo actual y su versión anterior.

```bash
git diff
```

### 8. Volver a un Estado Específico del Proyecto
Puedes volver a un commit específico utilizando su hash con:

```bash
git checkout <HASH>
```

Para volver al inicio del historial de tu proyecto, puedes utilizar:

```bash
git checkout HEAD
```

Si deseas resetear todos los cambios hasta un commit en particular:

```bash
git reset --hard <HASH>
```

### 9. Volver Atrás en el Tiempo
Si necesitas volver a un commit anterior, pero el `reset` no ha funcionado como esperabas, puedes utilizar `git reflog`. Este comando te muestra el historial completo de interacciones que has tenido con tu repositorio:

```bash
git reflog
```

Si encuentras el commit deseado en el reflog, puedes volver a él utilizando `git reset --hard <HASH>`.

---



## Manejo de Versiones y Etiquetas (Tags)

### 10. Tags en Git
Los **tags** te permiten marcar puntos importantes en el historial del proyecto. Normalmente, se usan para identificar versiones. Por ejemplo, podrías crear un tag llamado `v1.0` para marcar la primera versión de tu proyecto:

```bash
git tag v1.0
```

Moverte a un tag específico es simple:

```bash
git checkout tags/v1.0
```

### 11. Revertir Commits
Si deseas eliminar un commit específico pero mantener el historial, puedes usar `git revert`. Este comando elimina el commit creando uno nuevo que invierte los cambios del anterior:

```bash
git revert <HASH>
```

---

## Trabajo con Ramas

### 12. Crear y Cambiar entre Ramas
En Git, puedes trabajar en diferentes líneas de desarrollo (ramas) sin afectar la rama principal. Para crear una nueva rama y cambiarte a ella:

```bash
git branch <nombre_rama>
git switch <nombre_rama>
```

Esto es útil si deseas trabajar en una nueva funcionalidad sin afectar el proyecto principal.

### 13. Guardar Cambios Temporalmente
Si necesitas pausar tu trabajo temporalmente, puedes usar `git stash`, que guarda los cambios sin hacer un commit:

```bash
git stash
```

Para recuperar los cambios guardados:

```bash
git stash pop
```

Si ya no necesitas esos cambios guardados, puedes eliminarlos:

```bash
git stash drop
```

### 14. Eliminar Ramas
Una vez que hayas terminado con una rama, es una buena práctica eliminarla:

```bash
git branch -d <nombre_rama>
```

---

## Conclusión

Git es una herramienta poderosa para el control de versiones y trabajo colaborativo. Con los comandos y conceptos cubiertos, puedes gestionar el historial de tu proyecto, trabajar en nuevas funcionalidades de manera paralela, y colaborar eficientemente con otros.

<PARTE TEÓRICA>

## Comandos básicos

1. **Git Add**: Este comando se usa para seleccionar archivos que deseas rastrear. Al ejecutar `git add`, le indicas a Git que preste atención a los cambios realizados en esos archivos específicos.
2. **Git Status**: `Git status` proporciona una visión general del estado actual de tu repositorio. Te informa sobre los cambios que están listos para ser confirmados, aquellos que no lo están, y los archivos que Git aún no está rastreando.
3. **Git Commit**: Después de agregar archivos con `git add`, utilizas `git commit` para capturar una instantánea de esos archivos en su estado actual. Este comando sirve para confirmar oficialmente los cambios realizados, asignándoles una descripción clara.
4. **Git Push**: Con `git push`, subes los cambios confirmados al repositorio remoto en GitHub. Este proceso hace que tus cambios sean accesibles a otros colaboradores y los almacena de forma segura en la nube.
5. **Git Branch**: Este comando se emplea para trabajar con diferentes versiones paralelas de tu proyecto. Los branches permiten desarrollar nuevas funcionalidades o realizar pruebas en ambientes separados sin alterar la rama principal, usualmente conocida como `master` o `main`.
6. **Git Checkout**: `Git checkout` se utiliza para cambiar entre diferentes branches. Si deseas enfocarte en una funcionalidad específica o en una revisión particular, puedes cambiar a la rama correspondiente con este comando.
7. **Git Merge**: Se usa para integrar los cambios de una rama en otra. Este comando es fundamental en el flujo de trabajo de Git, ya que permite unir las actualizaciones o características desarrolladas en una rama secundaria con la rama principal del proyecto.
8. **Git Pull**: Este comando actualiza tu rama local con los últimos cambios del repositorio remoto. `Git pull` es esencial para mantener tu trabajo local alineado con el del equipo, permitiéndote incorporar los cambios más recientes antes de iniciar nuevas tareas o correcciones.

<COMANDOS BASICOS>

### Ejemplo práctico

1. **Crear un nuevo repositorio en GitHub.**
2. **Clonar el repositorio a tu máquina local.**
    
    ```bash
    git clone <url-del-repositorio>
    ```
    
3. **Crear y editar un archivo `hola_mundo.py`.**
4. **Usar para rastrear y confirmar los cambios:**
    
    Con `git add .` añade todos los ficheros del directorio actual y con `git add <nombre-del-fichero>` agrega el fichero que nombras solamente:
    
    ```bash
    git add .
    git status
    ```
    
    El mensaje que acompaña al commit ha de ser identificativo del cambio que se hace a continuación se dan unas pequeñas nociones para ese nombre:
    
    ```bash
    git commit -m 'mensaje-acompaña-al-commit'
    ```
    
    - Redacta el mensaje como si estuvieras dando una orden o instrucción.
    - Incluye información clave como el módulo o la funcionalidad que estás modificando. Por ejemplo, "Corrige error en el módulo de autenticación".
    - Antes de hacer un commit, revisa tus cambios y asegúrate de que el mensaje del commit refleje adecuadamente lo que está incluido en ese commit.

5. **Subir los cambios al repositorio remoto:**
    
    ```bash
    git push origin master
    ```
![flujo standar](./img/flujo.gif)

