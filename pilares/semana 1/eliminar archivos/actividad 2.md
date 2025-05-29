1. crear una cuenta de github

    ![cuenta de github](./img/01_cuenta_github.png)

2. descargar proyecto
    ![Proyecto inicial](./img/01_inicial.png)

3. crear repositorio local
    ![repositorio local](./img/02_git_init.png)



Actividad 1

1. Cambiar el nombre de un archivo

cambiamos el nombre del archivo index.html a home.html.

- Ejecuta el comando `git mv` para cambiar el nombre del archivo:

    ```bash
    git mv index.html home.html
    ```
    Esto cambiará el nombre del archivo en el sistema de archivos y preparará el cambio para la próxima confirmación.

    ![cambiar nombre](./img/03_mv_cambiar_nombre.png)
    


- Confirma el cambio en el repositorio:
    ```bash
    git commit -m "Renombrar index.html a home.html"
    ```

2. Eliminar un archivo

eliminamos el archivo style.css.

- Ejecutamos el comando `git rm` para eliminar el archivo:

    ```bash
    git rm assets/css/style.css
    ```

    Esto eliminará el archivo del sistema de archivos y añadirá el evento de eliminación al índice.

    ![eliminar archivo](./img/04_rm_eliminar_archivo.png)

- Confirma la eliminación en el repositorio:

    ```bash
    git commit -m "Eliminar archivo style.css"
    ```

3. Confirmar cambios múltiples (opcional)
Si realizas varios cambios (renombrar y eliminar archivos), puedes confirmarlos todos en un solo paso:

- Asegúrate de que todos los cambios están listos:
    ```bash
    git status
    ```

    ![git status](./img/05_status.png)

- Confirma todos los cambios:

    ```bash
    git commit -m "Renombrar y eliminar archivos según la actividad"
    ```

    ![confirmar los cambios](./img/06_git_commit_01.png)

4. Verifica los cambios
Para verificar que los cambios se han aplicado correctamente, usa:

    ```bash
    git log --oneline
    ```

    Esto mostrará un historial de confirmaciones, incluyendo los cambios realizados.

    ![git log](./img/07_verificar_cambios.png)



Actividad 2

1. Cambiar el nombre de un archivo fuera de Git

    Usando un IDE (como Visual Studio Code):

    - Abre el archivo en el explorador de archivos del IDE.
    - Haz clic derecho sobre el archivo que deseas renombrar (por ejemplo, `galery_blog.html`).
    - Selecciona la opción **Renombrar** y cambia el nombre (por ejemplo, a `gallery_blog.html`).
    - Guarda los cambios.
    
    ![renombrar archivo](./img/08_renombrar_clic_derecho.png)

    **Usando Bash:**
    - Usa el comando `mv` para renombrar el archivo:

        ```bash
        mv templates/galery_blog.html templates/gallery_blog.html
        ```
        ![cambiar nombre css](./img/09_cambiar_nombre.png)
2. Eliminar un archivo fuera de Git

    **Usando Bash:**

    - Para eliminar un archivo no rastreado por Git (por ejemplo, galery.css), usa:

        ```bash
        git clean -f
        ```

        Esto eliminará los archivos no rastreados del directorio de trabajo.

        ![git clean -f](./img/10_git_clean.png)

    - Si también deseas eliminar subdirectorios vacíos, usa:

        ```bash
        git clean -f -d
        ```

        ![git clean -f -d](./img/11_git_clean_directory.png)

3. Cambiar el nombre de un archivo en Git


    - Usa el comando `git mv` para renombrar un archivo rastreado por Git:

        ```bash
        git mv templates/galery_blog.html templates/gallery_blog.html
        ```

        Esto actualizará el índice de Git con el nuevo nombre.

        
    - Confirma el cambio:

        ```bash
        git commit -m "Renombrar galery_blog.html a gallery_blog.html"
        ```
        
        ![commit](./img/12_commit_rename.png)

4. Eliminar un archivo de Git

    - Usa el comando git rm para eliminar un archivo rastreado por Git (por ejemplo, galery.css):

        ```bash
        git rm assets/css/galery.css
        ```

        ![remove](./img/13_remove_css.png)

    - Confirma la eliminación:

        ```bash
        git commit -m "Eliminar archivo galery.css"
        ```

        ![commit](./img/14_confirmar_eliminar_css.png)

        

5. Verificar los cambios

    - Usa git status para verificar los cambios pendientes:

        ```bash
        git status
        ```

    - Usa git log para confirmar los cambios realizados:

        ```Bash
        git log --oneline
        ```
        ![git log](./img/16_git_logs.png)
