# Uso de Comandos con GIT: Guía Completa

## GIT: Control de Versiones y Flujo de Trabajo

### Comandos Básicos para Gestión de Cambios

- **git status:**  
  Muestra el estado actual del repositorio, incluyendo archivos modificados, nuevos o eliminados que aún no están en el área de *staging*. También indica la rama actual y si está sincronizada con el remoto.

- **git add [archivo]:**  
  Agrega cambios específicos al área de *staging* para prepararlos para un commit. Ejemplos:  
  - `git add .`: Añade todos los archivos modificados.  
  - `git add *.js`: Añade solo archivos JavaScript.

- **git commit -m "mensaje":**  
  Registra los cambios del área de *staging* en el historial del repositorio con un mensaje descriptivo. Usar mensajes claros (ej: "Corrige error de login") facilita el rastreo de cambios.

- **git show [commit_hash]:**  
  Detalla los cambios específicos de un commit, incluyendo diferencias en código (*diff*) y metadatos (autor, fecha).

- **git diff [commitA] [commitB]:**  
  Compara diferencias entre dos commits, ramas o estados del repositorio. Ejemplo útil:  
  `git diff main feature/login` muestra cambios entre la rama principal y una rama de funcionalidad.

- **git log -- [filename]:**  
  Muestra el historial completo de commits que afectan a un archivo específico, incluyendo fechas y autores. Opciones útiles:  
  - `--oneline`: Resume commits en una línea.  
  - `--graph`: Muestra ramas visualmente.

- **git reset [opciones]:**  
  - `git reset --soft [commit]`: Deshace commits manteniendo cambios en el área de *staging*.  
  - `git reset --hard [commit]`: Elimina todos los cambios posteriores al commit especificado (¡uso cuidadoso!).

- **git revert [commit_hash]:**  
  Crea un nuevo commit que deshace los cambios de un commit anterior, ideal para corregir errores sin alterar el historial.

- **git commit --amend -m "nuevo mensaje":**  
  Modifica el mensaje del último commit (antes de hacer *push*). También permite añadir cambios olvidados con `git add` previo.

- **git push --force:**  
  Sobrescribe el historial remoto con el local. Útil para corregir commits, pero peligroso en ramas compartidas. Alternativa segura: `git push --force-with-lease`.

---

## Ramas: Estrategias y Comandos Clave

### ¿Qué son las ramas?  
Cada rama es un puntero móvil a un commit específico. Al crear una rama, Git genera una nueva línea de desarrollo independiente, permitiendo trabajar en paralelo sin afectar la versión estable (ej: `main` o `master`).

### Creación y Gestión de Ramas

| Comando | Descripción |  
|---------|-------------|  
| `git branch [nombre]` | Crea una rama nueva sin cambiar a ella. |  
| `git checkout -b [nombre]` | Crea y cambia a la nueva rama (versión antigua). |  
| `git switch -c [nombre]` | Alternativa moderna a `checkout -b`. |  
| `git branch -m [nombre_viejo] [nombre_nuevo]` | Renombra una rama local. |  
| `git branch -d [nombre]` | Elimina una rama local (solo si está fusionada). |  
| `git push origin --delete [nombre]` | Elimina una rama remota. |  

### Flujo de Trabajo con Ramas

1. **Desarrollo Aislado:**  
   Ejemplo: Crear `feature/user-profile` para añadir perfiles de usuario sin tocar `main`.

2. **Fusión de Cambios:**  
   - `git merge [rama]`: Integra cambios de una rama a otra (historial lineal).  
   - `git rebase [rama]`: Reorganiza el historial para simular cambios secuenciales (ideal para limpiar commits antes de fusionar).

3. **Resolución de Conflictos:**  
   Git marca archivos con conflictos. Edítalos manualmente, luego usa `git add` y `git commit` para finalizar.

### Ventajas Clave de Usar Ramas

- **Experimentación Segura:** Prueba ideas en ramas dedicadas (ej: `experiment/optimizacion-db`).  
- **Trabajo en Equipo:** Cada desarrollador trabaja en su rama (ej: `fix/login-juan`), evitando colisiones.  
- **Lanzamientos Controlados:** Ramas como `dev`, `staging`, y `prod` permiten gestionar versiones.  
- **Revisión de Código:** Integra *Pull Requests* en plataformas como GitHub para discutir cambios antes de fusionar.  

---

## Buenas Prácticas

- **Nomenclatura Clara:** Usa prefijos como `feature/`, `bugfix/`, o `hotfix/` en nombres de ramas.  
- **Commits Atómicos:** Cambios pequeños y enfocados en una sola funcionalidad.  
- **Sincronización Frecuente:** Haz `git pull` regularmente para actualizar tu rama local con cambios remotos.  
- **Evita `push --force` en Ramas Compartidas:** Podrías sobrescribir el trabajo de otros.  

🔍 **Consejo Final:** Usa `git tag [versión]` para marcar releases importantes (ej: `v1.2.3`), facilitando el despliegue y el control de versiones.