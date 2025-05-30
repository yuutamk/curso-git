Git es una herramienta de control de versiones que se puede instalar en varios sistemas operativos. En esta guía, aprenderás cómo instalar Git en Windows, Mac y distribuciones de Linux.

Instalación en Windows
1. Descarga el instalador de Git

Visita el sitio oficial de Git (https://gitforwindows.org/) y haz clic en el botón "Download" para descargar el instalador de Git más reciente para Windows.
Haz clic en el archivo descargado para iniciar el proceso de instalación.
2. Inicia la instalación

Haz clic en "Next" en la pantalla de bienvenida.
3. Selecciona la ubicación de la instalación

Elige el lugar donde te gustaría que Git se instalara en tu computadora. La ubicación predeterminada generalmente es adecuada, pero puedes cambiarla si es necesario. Haz clic en "Next" para continuar.
4. Selecciona los componentes a instalar

Verás una lista de componentes para instalar. Las opciones predeterminadas suelen ser suficientes, pero siéntete libre de hacer cambios según tus necesidades. Después de hacer tus selecciones, haz clic en "Next".
5. Selecciona el menú de inicio

Puedes elegir un nombre para el acceso directo de Git en el menú de inicio. La opción predeterminada es "Git". Después de hacer tu selección, haz clic en "Next".
6. Elige el editor predeterminado que utilizará Git

Selecciona el editor que prefieres usar con Git. Por defecto, sugerirá el editor Vim, pero puedes elegir otro editor que esté instalado en tu sistema, como Notepad++, VS Code, Atom, etc. Después de hacer tu selección, haz clic en "Next".
7. Elige el nombre de la rama inicial

Se te pedirá que elijas el nombre de la rama inicial. Los nombres "master" y "main" son comúnmente utilizados, siendo "main" la nueva convención predeterminada. Elige la que prefieras para tu ambiente de trabajo y haz clic en "Next".
8. Ajusta tu PATH

En la próxima pantalla, se te pedirá que ajustes tu PATH. Elige la opción "Git from the command line and also from 3rd-party software" para asegurarte de que podrás usar Git desde la línea de comandos de Windows o PowerShell. Haz clic en "Next".
9. Elecciones de SSH y Configura los finales de línea

En las siguientes pantallas, se te pedirá que elijas el cliente SSH, no hay necesidad de cambiar la elección predeterminada, haz clic en “Next” hasta llegar a “Configuring the line ending conversions”, que significa cómo Git debe tratar los finales de línea. La opción recomendada es "Checkout Windows-style, commit Unix-style line endings". Haz clic en "Next".
10. Elige el emulador de terminal

Aquí puedes elegir el emulador de terminal que Git usará. La opción predeterminada es "MinTTY", pero puedes elegir usar la línea de comandos de Windows si lo prefieres. Haz clic en "Next".
11. Elige el administrador de credenciales

Aquí debes dejar seleccionado “Git Credential Manager”. Haz clic en "Next".
12. Elige las opciones extra

Aquí puedes elegir algunas opciones extras. Las opciones predeterminadas son generalmente suficientes para la mayoría de los usuarios. Haz clic en "Next".
13. Instala

Haz clic en "Install" para comenzar la instalación. Verás una barra de progreso mientras se está instalando Git.
14. Completa la instalación

Una vez que la instalación se haya completado, haz clic en "Finish". Ahora Git debería estar instalado en tu computadora.
Para verificar si la instalación fue exitosa, puedes abrir Git Bash (o PowerShell) y escribir git --version. Esto debería devolver la versión de Git que acabas de instalar.

Configurando el nombre de usuario en Git
Abre la terminal de Windows o Git Bash, que puedes encontrar escribiendo en la barra de búsqueda.
Escribe el siguiente comando:
git config --global user.name "Tu Nombre"
Reemplaza "Tu Nombre" por el nombre que deseas asociar a todos tus commits en Git. Este no necesita ser el mismo que tu nombre de usuario de GitHub o de cualquier otro servicio Git que puedas estar usando, aunque muchas personas prefieren mantener la consistencia.

Configurando el correo electrónico en Git
En la terminal, escribe el siguiente comando:

git config --global user.email "tu-email@ejemplo.com"
Reemplaza "tu-email@ejemplo.com" por la dirección de correo electrónico que deseas asociar a todos tus commits en Git. Usa el mismo correo electrónico que utilizas para tu cuenta de GitHub u otros servicios Git.

Con estos comandos, has configurado un nombre de usuario y una dirección de correo electrónico para Git, que se asociarán a todos los commits que realices.

Si quieres verificar las configuraciones, puedes usar los siguientes comandos:

Para el nombre de usuario:
git config --global user.name
Para el correo electrónico:
git config --global user.email
Estos comandos devolverán el nombre de usuario y el correo electrónico configurados actualmente en Git, respectivamente.