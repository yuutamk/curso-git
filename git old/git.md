# uso de comandos con GIT

## GIT

- **git status:** sirve para observar los cambios en un proyecto que se ha creado, modificado o eliminado

- **git add:** agrega los cambios al repositorio
- **git commit:** confirma los cambios/registrar los cambios añadidos al historial
- **git show:** auxilia en ver los cambios en un archivo
- **git diff commitA commitB:** observa la diferencia entre dos versiones
- **git log --[filename]:** se observa el historial de cambios de un archivo
- **git reset:** deshacer los cambios de un archivo
- **git revert:** revierte cambios
- **git commit -am:** actualiza el mensaje del commit
- **git push --force:** forza las actualizaciones de los cambios

## Ramas

Las ramas en git permiten desarrollar funcionalidades aisladas o trabajar en paralelo sin afectar la linea principal de codigo es decir es una linea de codigo independiente, ademas de que son escenciales para:
- Experimental sin riesgos
- Trabajar en equipo con eficiencia
- Gestionar diferentes versiones


**¿Pero que son las ramas?**

cada rama es un puntero movil a un commit especifico al crear una nueva rama, git crea un nuevo puntero que puede mover independientemente

**Para crear y renombrar las ramas**

comandos
- **crear rama:** ``git branch nuevaRama``
- **crear y cambiar:** ``git checkout -b nuevaRama`` ``git switch nuevaRama``
- **renombrar:** ``git branch -M nombreViejo nombreNuevo``

**Ventajas de usar ramas**

- permiten trabajar en caracteristicas nuevas sin afectar la rama principal

**creando una nueva rama**
- **nueva rama:** ``git branch nombre_de_rama
- **cambiar a una rama:** ``git checkout -b \<nuevo nombre>

Nota: Si el nuevo nombre ya existe al intentar renombrar una rama ocasiona -> git exhiba un error

- **renombrar una rama existente:** ``git branch -M nombre_actual nuevo_nombre``

- **para observar la rama que actualmente estas trabajando:** ``git branch --current``

**Diferencia entre git commit y git stash

- git stash guarda el cambio temporalmente

- git commit los guarda permanentemente

para guardar cambios actuales de trabajo en stash -> ``git stash``
creando nueva rama a partir de un stash existente -> ``git stash branch \<branch-name>

para ver todos los stash en lista y que estan guardados -> ``git stash list``

aplicas los cambios guardados en el stash a la rama actual sin eliminar el stash de la lista al mismo tiempo -> git stash pop

para hacer un merge de una rama a otra -> git merge branch_name

al fusionar un marge en la rama principal -> git marge checkout main y luego git marge feature

si se combina marge una rama en la rama principal -> se combina los cambios en una rama principal