# Cuestionario de Control de Versiones - Unidad 2
**Alumno:** Juan Gustavo Ángel Cruz Méndez  
**Materia:** Desarrollo Web Integral  

---

### 1. ¿Qué sucede cuando hacemos un `git add`?
Cuando ejecutamos `git add`, movemos los cambios del "Working Directory" (directorio de trabajo) al **"Staging Area"** (área de preparación). Es el paso donde le indicamos a Git qué archivos o modificaciones queremos incluir en nuestra próxima "foto" o versión del proyecto.

### 2. ¿Qué sucede cuando hacemos un `git commit`? ¿Dónde está ese commit?
El `git commit` confirma los cambios que estaban en el Staging Area y crea un registro permanente en el historial del proyecto con un ID único (hash). Este commit reside **únicamente en tu repositorio local** (en la carpeta oculta `.git` de tu computadora).

### 3. ¿Por qué al hacer `git commit` todavía no está disponible ese commit en el repositorio remoto?
Porque Git es un sistema de control de versiones **distribuido**. Las operaciones de `add` y `commit` son locales para permitir trabajar sin internet. El commit solo vive en tu máquina hasta que decidas sincronizarlo explícitamente con el servidor.

### 4. ¿Qué hay que hacer para que veamos este commit en nuestro repositorio remoto de GitHub?
Es necesario ejecutar el comando **`git push`**. Este comando "empuja" los commits desde tu repositorio local hacia el repositorio remoto configurado (normalmente llamado `origin`).

### 5. ¿Qué diferencia hay entre hacer un fork o crear una nueva rama?
*   **Fork:** Es una copia completa de un repositorio ajeno en **tu propia cuenta de GitHub**. Se usa para contribuir a proyectos de otros o iniciar uno propio basado en otro.
*   **Rama (Branch):** Es una línea de tiempo paralela dentro del **mismo repositorio**. Se usa para desarrollar funciones nuevas sin afectar el código principal (`main`).

### 6. ¿Qué comando se utiliza para crear una nueva rama sin cambiarte a ella?
Se utiliza el comando:
`git branch nombre-de-la-rama`

### 7. ¿Cuál es la diferencia entre los comandos `git switch` y `git checkout` al trabajar con ramas?
*   `git checkout`: Es el comando clásico. Sirve para cambiar de rama, pero también para restaurar archivos, lo que lo hace un poco confuso.
*   `git switch`: Es un comando más moderno y específico, diseñado exclusivamente para **cambiar entre ramas**, haciendo el flujo más claro.

### 8. ¿Qué es una rama por defecto (como main o master) y por qué es importante?
Es la rama principal donde reside el código estable y "de producción". Es importante porque sirve como base para todas las demás ramas y es la que los usuarios o servidores de despliegue ven por defecto al acceder al proyecto.

### 9. ¿Qué comando te permite ver la lista de todas las ramas locales de tu repositorio?
El comando es:
`git branch`

### 10. En el contexto de Git, explica qué es una rama (branch) y cuál es su beneficio principal.
Una rama es como una "realidad alternativa" o un desvío del tronco principal del proyecto. Su beneficio principal es el **aislamiento**: permite trabajar en nuevas ideas o corregir errores sin riesgo de romper el código que ya funciona, facilitando el trabajo en equipo simultáneo.

### 11. ¿Qué ha pasado con el contenido de la carpeta `practica-taller-git`? ¿Por qué no la podemos ver en nuestro repositorio remoto de github?
Si la carpeta está vacía o si contiene otro repositorio de Git dentro (`.git`), Git no la subirá de forma convencional. GitHub no muestra carpetas vacías; además, si intentaste subir un repositorio dentro de otro sin configurarlo como submódulo, Git lo ignora por seguridad de la estructura.
