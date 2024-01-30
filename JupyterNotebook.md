## **Uso de GitHub en Jupyter Notebook**

1. **Instalar Git**: Asegúrate de tener Git instalado en tu ordenador. Si no es así, puedes descargarlo e instalarlo desde [git-scm.com](https://git-scm.com/).
2. **Configurar Git**: Configura tu usuario y correo electrónico de Git con los comandos:
    
    ```bash
    git config --global user.name "Tu Nombre"
    git config --global user.email "tuemail@example.com"
    ```
    
3. **Crear un Repositorio en GitHub**: Ve a [GitHub](https://github.com/) y crea un nuevo repositorio. Copia la URL del repositorio.
4. **Clonar el Repositorio**: Abre tu terminal o línea de comandos y navega al directorio donde quieres tener tu proyecto. Luego, clona el repositorio con:
    
    ```bash
    git clone <url-del-repositorio>
    ```
    
5. **Crear o Mover tu Jupyter Notebook**: Si ya tienes un Jupyter Notebook, muévelo a la carpeta del repositorio clonado. Si no, abre Jupyter y crea un nuevo notebook en esta carpeta.
6. **Trabajar en tu Notebook**: Realiza tus análisis, escribe código y notas en tu Jupyter Notebook como lo harías normalmente.
7. **Guardar y Añadir Cambios al Repositorio**: Una vez que hayas terminado de trabajar en tu notebook, guarda los cambios. Luego, usa los siguientes comandos de Git para añadir tus cambios al repositorio:
    
    ```bash
    git add .
    git commit -m "Descripción de los cambios realizados"
    ```
    
8. **Subir Cambios a GitHub**: Finalmente, sube tus cambios al repositorio de GitHub con:
    
    ```bash
    git push origin master
    ```
    
9. **Ver el Notebook en GitHub**: Una vez que hayas subido tus notebooks a GitHub, puedes verlos directamente en la interfaz web de GitHub. GitHub renderiza automáticamente los Jupyter Notebooks, permitiendo ver el código y los resultados sin necesidad de ejecutar el notebook.