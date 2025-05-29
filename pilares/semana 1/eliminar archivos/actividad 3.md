1. crear una cuenta de github

    ![cuenta de github](./img/01_cuenta_github.png)

2. descargar proyecto
    ![Proyecto inicial](./img/01_inicial.png)

3. crear repositorio local
    ![repositorio local](./img/02_git_init.png)


4. **Crear el archivo `.gitignore`**

- Abre una terminal o visual studio code en la raíz de tu proyecto:

- Crea o abre el archivo .gitignore:

    **Desde la terminal**

    ```bash
    nano .gitignore
    ```

    ![crear gitignore](./A3/01_gitignore_create.png)

- Escribe los nombres de los archivos o carpetas que deseas ignorar, uno por línea. Por ejemplo:

    ```bash
    # Ignorar archivos temporales
    *.tmp
    *.log

    # Ignorar carpetas específicas
    /node_modules/
    /dist/

    # Ignorar imágenes y archivos de iconos
    assets/img/
    assets/icons/

    # Ignorar archivos del sistema
    .DS_Store
    Thumbs.db
    ```

    ![gitignore comando](./A3/02_gitignore_nano.png)

- Guarda el archivo y cierra el editor (en `nano`, presiona `CTRL+O`, luego `Enter`, y finalmente `CTRL+X`).

5. **Confirmar el archivo `.gitignore` en el repositorio**

- Añade el archivo `.gitignore` al área de preparación:

    ```bash
    git add .gitignore
    ```

    ![confirmar el cambio](./A3/03_confirm_gitignore.png)
- Realiza una confirmación:

    ```bash
    git commit -m "Añadir archivo .gitignore para ignorar archivos y carpetas no deseados"
    ```

    ![git commit](./A3/04_commit_gitignore.png)

6. **Verificar que los archivos ignorados no se rastrean**

- Usa el comando git status para verificar que los archivos o carpetas especificados en .gitignore no aparecen en el área de preparación:

    ```bash
    git status
    ```

    ![git status](./A3/05_git_status.png)


