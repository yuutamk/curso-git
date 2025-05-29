**Instrucciones claras y precisas para la actividad:**  

---

### **Objetivo de la actividad**  
Aprender a gestionar cambios de nombre y eliminación de archivos en un repositorio Git, tanto utilizando comandos directos de Git (git mv, git rm) como herramientas externas (IDE o Bash), y documentar los procesos mediante capturas de pantalla.  

---

### **Pasos previos**  
1. **Crear una cuenta en GitHub** (si no la tienes).  
2. **Descargar el proyecto web** desde Google Drive.  
3. **Inicializar un repositorio Git local** en la carpeta del proyecto descargado:  
   ```bash  
   git init  
   ```  

---

### **Actividad 1: Cambiar nombre y eliminar archivos *dentro* de Git**  
**Objetivo:** Usar comandos de Git (`git mv` y `git rm`) para gestionar archivos.  

#### **Pasos:**  
1. **Cambiar el nombre de un archivo con `git mv`:**  
   ```bash  
   git mv nombre_actual.txt nombre_nuevo.txt  
   ```  
   - Esto renombra el archivo y prepara el cambio para confirmar.  

2. **Eliminar un archivo con `git rm`:**  
   ```bash  
   git rm archivo_a_eliminar.txt  
   ```  
   - Esto elimina el archivo del repositorio y del sistema de archivos.  

3. **Confirmar los cambios:**  
   ```bash  
   git commit -m "Explicación: cambios de nombre y eliminación de archivos"  
   ```  

#### **Nota:**  
Git detecta automáticamente los cambios de nombre si se usan `git mv` o si se combinan eliminaciones y adiciones en la misma confirmación.  

---

### **Actividad 2: Cambiar nombre y eliminar archivos *fuera* de Git**  
**Objetivo:** Gestionar archivos usando herramientas externas (IDE o Bash) y luego sincronizar cambios con Git.  

#### **Pasos:**  
1. **Cambiar el nombre de un archivo usando un IDE o Bash:**  
   - **En un IDE:**  
     - Abre el explorador de archivos.  
     - Renombra el archivo manualmente (ej: `archivo_viejo.html` → `archivo_nuevo.html`).  
   - **En Bash (sin Git):**  
     ```bash  
     mv archivo_viejo.html archivo_nuevo.html  
     ```  

2. **Eliminar un archivo usando Bash:**  
   ```bash  
   rm archivo_a_eliminar.txt  
   ```  

3. **Sincronizar cambios con Git:**  
   - Para cambios de nombre:  
     ```bash  
     git add archivo_nuevo.html  
     git rm archivo_viejo.html  
     ```  
   - Para eliminaciones:  
     ```bash  
     git rm archivo_a_eliminar.txt  
     ```  

4. **Confirmar los cambios:**  
   ```bash  
   git commit -m "Explicación: cambios realizados fuera de Git"  
   ```  

---

### **Entrega**  
1. **Capturas de pantalla para la Actividad 1:**  
   - Muestra el uso de `git mv`, `git rm` y la confirmación de cambios (commit).  
   - Incluye el resultado de `git status` antes y después de los comandos.  

2. **Capturas de pantalla para la Actividad 2:**  
   - Muestra:  
     - El proceso de renombrado en el IDE o Bash.  
     - Los comandos usados para sincronizar cambios con Git (`git add`, `git rm`).  
     - La confirmación final (`git commit`).  

---

### **Recomendaciones**  
- Verifica los cambios con `git status` antes de confirmar.  
- Si usas `git clean -f -d`, asegúrate de entender que este comando elimina archivos no rastreados por Git (solo para casos específicos).  
- Evita borrar archivos críticos del proyecto.  

¡Listo! Sube las capturas a la plataforma indicada.