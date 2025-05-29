Se asumirá que ya se tiene un proyecto guardado en un repositorio de git, si éste ya cuenta con varias ramas, revisa cuántas ramas han sido creadas usando el comando git branch --list. Sin embargo, si sólo se cuenta con la rama main, crea una nueva rama mediante el comando git branch name_branch, donde name_branch será el nombre de nuestra nueva rama.
Texto



Ya que verificaste que cuentas con más de una rama, ubícate en la rama main, realiza un par de modificaciones en algún archivo y ejecuta en la terminal el comando git status, en donde se visualiza el estado del proyecto con los cambios sin guardar.Texto



Seguido a esto, ejecuta el comando git add . para añadir los cambios de los archivos a staging, y posteriormente ejecuta el comando git stash para realizar un guardado rápido; de esta manera conseguirás un estado de proyecto limpio.Texto


Ahora, cambia de rama, mediante el comando git checkout name_branch, una vez en ésta, haz nuevas modificaciones en cualquiera de tus archivos y realiza un nuevo guardado rápido, siguiendo el orden anterior de comandos, es decir, comienza por git add ., y luego git stash.


Ya que realizaste un par de guardados en stash, visualiza la lista de los cambios almacenados en stashing mediante el comando git stash list, cabe destacar que el cambio más reciente al crear un stash siempre recibirá el valor de 0, mientras que los que estaban antes aumentan su valor de forma secuencial.Texto


Ahora bien, aplica los cambios de una posición específica del stash, para ello usa el comando git stash apply stash@{num_stash}, en donde el num_stash se obtiene de la lista mostrada anteriormente.

Ahora, recrea un conflicto de stash en el cual no existe una coincidencia de los cambios aplicados al momento de retomar un cambio almacenado en stash. Para ello, realiza nuevamente cambios en una de tus ramas del repositorio, ejecuta un commit para guardar estas modificaciones, nuevamente realiza nuevos cambios y guarda en stash.Texto


Vuelve a tu rama main y aplica el último cambio guardado en stash mediante el comando git stash pop. Esta acción genera un conflicto originado por la diferencia de contenido en nuestros archivos, ya que modificaste un mismo archivo en el stash y en la rama actual, es decir que el conflicto sucede porque el comando stash pop mezcla el estado guardado con la rama actual, la cual no presenta esos cambios.

Para resolver este conflicto se puede realizar lo siguiente:
Abre el archivo modificado.
Edita la sección que genera conflicto.
Guarda la versión final.
Ejecuta los comandos git add . y git commit -am “Mensaje”.
