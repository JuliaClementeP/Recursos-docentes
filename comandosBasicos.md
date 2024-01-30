## Comandos básicos

1. **Git Add**: Este comando se usa para seleccionar archivos que deseas rastrear. Al ejecutar `git add`, le indicas a Git que preste atención a los cambios realizados en esos archivos específicos.
2. **Git Status**: `Git status` proporciona una visión general del estado actual de tu repositorio. Te informa sobre los cambios que están listos para ser confirmados, aquellos que no lo están, y los archivos que Git aún no está rastreando.
3. **Git Commit**: Después de agregar archivos con `git add`, utilizas `git commit` para capturar una instantánea de esos archivos en su estado actual. Este comando sirve para confirmar oficialmente los cambios realizados, asignándoles una descripción clara.
4. **Git Push**: Con `git push`, subes los cambios confirmados al repositorio remoto en GitHub. Este proceso hace que tus cambios sean accesibles a otros colaboradores y los almacena de forma segura en la nube.
5. **Git Branch**: Este comando se emplea para trabajar con diferentes versiones paralelas de tu proyecto. Los branches permiten desarrollar nuevas funcionalidades o realizar pruebas en ambientes separados sin alterar la rama principal, usualmente conocida como `master` o `main`.
6. **Git Checkout**: `Git checkout` se utiliza para cambiar entre diferentes branches. Si deseas enfocarte en una funcionalidad específica o en una revisión particular, puedes cambiar a la rama correspondiente con este comando.
7. **Git Merge**: Se usa para integrar los cambios de una rama en otra. Este comando es fundamental en el flujo de trabajo de Git, ya que permite unir las actualizaciones o características desarrolladas en una rama secundaria con la rama principal del proyecto.
8. **Git Pull**: Este comando actualiza tu rama local con los últimos cambios del repositorio remoto. `Git pull` es esencial para mantener tu trabajo local alineado con el del equipo, permitiéndote incorporar los cambios más recientes antes de iniciar nuevas tareas o correcciones.

![Uso básico de Git](img/comandosBasicos1.svg)

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
    
6. **Crear y cambiar a una nueva rama para desarrollo adicional que llamaremos nueva-característica.**
    
    ```bash
    git branch nueva-caracteristica
    git checkout nueva-caracteristica
    ```
    
7. **Desarrollar y confirmar nuevos cambios en la nueva rama.**
    
    Desarrollamos cambios en nuestro fichero `hola_mundo.py` y luego realizamos el commit:
    
    ```bash
    git add hola_mundo.py
    git commit -m "Añade nueva funcionalidad a hola_mundo.py"
    git push origin nueva-caracteristica
    ```
    
8. **Fusionar los cambios de la nueva rama en `master`:**
    
    Primero, regresa a la rama `master` y luego fusiona los cambios:
    
    ```bash
    git checkout master
    git merge nueva-caracteristica
    git push origin master
    ```
    
9. **Actualizar regularmente la rama `master` local con cambios del repositorio remoto mediante `git pull`:**

![Ejemplo de uso de Git](img/comandosBasicosEjemplo.svg)