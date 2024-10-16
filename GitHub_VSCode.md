
# Uso de GitHub en VS Code con Interfaz Gráfica

## 1. Instalación de Git y VS Code
Antes de comenzar, asegúrate de tener Git y Visual Studio Code (VS Code) instalados en tu ordenador.

- **Instalar Git**: Descárgalo e instálalo desde [git-scm.com](https://git-scm.com/). Aunque no utilizaremos la línea de comandos, Git es esencial para la integración con VS Code.
- **Instalar VS Code**: Descárgalo desde [code.visualstudio.com](https://code.visualstudio.com/) e instálalo en tu sistema operativo.

## 2. Instalar la Extensión de GitHub en VS Code
Para mejorar la integración entre GitHub y VS Code, es recomendable instalar la extensión oficial de GitHub.

- **Abrir VS Code**.
- **Acceder a las Extensiones**:
  - Haz clic en el ícono de extensiones en la barra lateral izquierda (parece cuatro bloques).
- **Buscar la Extensión**:
  - En la barra de búsqueda, escribe "GitHub Pull Requests and Issues".
- **Instalar la Extensión**:
  - Selecciona la extensión desarrollada por GitHub y haz clic en "Install".

## 3. Configurar la Extensión de GitHub
Después de instalar la extensión, es necesario configurarla para que se conecte con tu cuenta de GitHub.

- **Iniciar Sesión en GitHub**:
  - Haz clic en el ícono de Cuenta en la barra de estado inferior de VS Code.
  - Selecciona "Sign in to GitHub" y sigue las instrucciones para autorizar VS Code en tu cuenta de GitHub.

## 4. Clonar un Repositorio de GitHub
Clonar un repositorio te permite trabajar en tu proyecto localmente desde VS Code.

- **Abrir la Paleta de Comandos**:
  - Presiona Ctrl + Shift + P (Windows/Linux) o Cmd + Shift + P (Mac) para abrir la paleta de comandos.
- **Ejecutar el Comando de Clonación**:
  - Escribe "Git: Clone" y selecciona la opción que aparece.
- **Ingresar la URL del Repositorio**:
  - Copia la URL de tu repositorio de GitHub (por ejemplo, https://github.com/tu-usuario/tu-repo.git) y pégala en el cuadro que aparece.
- **Seleccionar la Carpeta de Destino**:
  - Elige la ubicación en tu ordenador donde deseas clonar el repositorio.
- **Abrir el Repositorio en VS Code**:
  - Una vez clonado, VS Code te preguntará si deseas abrir el repositorio recién clonado. Haz clic en "Open".

## 5. Explorando la Interfaz de Source Control en VS Code
VS Code proporciona una interfaz gráfica intuitiva para gestionar el control de versiones.

- **Acceder a Source Control**:
  - Haz clic en el ícono de Control de Código Fuente en la barra lateral izquierda (parece una rama de árbol).
- **Visualizar Cambios**:
  - Aquí verás una lista de archivos modificados, añadidos o eliminados.
- **Agregar Cambios al Área de Preparación (Staging Area)**:
  - Puedes hacer clic en el ícono "+" al lado de cada archivo para añadirlo al área de preparación.
  - También puedes añadir todos los cambios de una vez haciendo clic en el ícono "+" junto a "Changes".

## 6. Realizar un Commit
Un commit guarda tus cambios con un mensaje descriptivo.

- **Escribir un Mensaje de Commit**:
  - En la parte superior de la vista de Source Control, encontrarás un campo para escribir tu mensaje de commit.
  - Escribe un mensaje claro y descriptivo, por ejemplo: "Añadir flujo estándar al tutorial".
- **Confirmar el Commit**:
  - Después de escribir el mensaje, haz clic en el icono de checkmark (✓) para realizar el commit.

## 7. Sincronizar Cambios con GitHub
Para subir tus commits locales al repositorio remoto en GitHub:

- **Sincronizar**:
  - En la barra de estado inferior, verás un icono de sincronización (dos flechas formando un círculo). Haz clic en él para sincronizar tus cambios.
- **Confirmar la Sincronización**:
  - VS Code realizará un push de tus commits locales al repositorio remoto en GitHub y también realizará un pull para obtener los últimos cambios si los hay.

## 8. Crear y Gestionar Ramas (Branches) Gráficamente
Trabajar con ramas te permite desarrollar funcionalidades o corregir errores sin afectar la rama principal.

- **Crear una Nueva Rama**:
  - Haz clic en el nombre de la rama actual en la barra de estado inferior (por ejemplo, main).
  - Selecciona "Create New Branch..." y escribe el nombre de la nueva rama, por ejemplo, nueva-funcionalidad.
- **Cambiar de Rama**:
  - Para cambiar a otra rama, haz clic nuevamente en el nombre de la rama en la barra de estado y selecciona la rama deseada de la lista.
- **Fusionar Ramas (Merge)**:
  - Después de trabajar en una rama y querer fusionarla con main:
    - Cambia a la rama main haciendo clic en ella en la barra de estado.
    - Haz clic en el nombre de la rama nuevamente y selecciona la opción "Merge Branch...".
    - Elige la rama que deseas fusionar, por ejemplo, nueva-funcionalidad.
