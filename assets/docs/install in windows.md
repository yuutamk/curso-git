### Tutorial Detallado: Instalación de Git en Windows  

---

#### **Requisitos Previos**  
- Windows 7 o superior  
- Conexión a internet  
- Permisos de administrador (recomendado)  

---

### **Método 1: Instalación Rápida con PowerShell**  
1. **Abre PowerShell como administrador**:  
   - Busca "PowerShell" en el menú de Inicio → Haz clic derecho → "Ejecutar como administrador".  
   ![PowerShell](./assets/img/winget.png)  

2. **Ejecuta el comando**:  
   ```powershell
   winget install --id Git.Git -e --source winget
   ```  
   - *Nota*: `winget` es el gestor de paquetes oficial de Microsoft (requiere Windows 10/11).  

---

### **Método 2: Instalación Manual (Recomendado)**  
#### **Paso 1: Descargar el Instalador**  
1. Visita [git-scm.com](https://git-scm.com/).  
   ![Página oficial](./assets/img/pagina%20oficial.png)  
2. Descarga la versión **64-bit** (compatible con la mayoría de sistemas):  
   ![Versión 64 bits](./assets/img/version%2064bit.png)  

---

#### **Paso 2: Ejecutar el Instalador**  
1. Haz doble clic en el archivo descargado (ej: `Git-2.48.1-64-bit.exe`):  
   ![Instalador de Windows](./assets/img/instalador.png)  

---

#### **Paso 3: Configuración Clave**  
Sigue estos pasos **cuidadosamente** durante la instalación:  

1. **Acepta la licencia**:  
   ![Términos y condiciones](./assets/img/terminos%20y%20condiciones.png)  

2. **Selección de componentes**:  
   - Marca todas las opciones para una integración completa:  
     - ✅ Git Bash  
     - ✅ Git GUI  
     - ✅ Git LFS (Soporte para archivos grandes)  
     - ✅ Asociar archivos `.sh` con Bash.  
   ![Select components](./assets/img/configuraciones.png)  

3. **Editor predeterminado**:  
   - **Recomendado**:  
     - **Visual Studio Code** (si lo tienes instalado).  
     - **Nano** (opción simple para principiantes).  
     - *Evita Vim si no tienes experiencia*.  
   ![Editor de consola](./assets/img/ajustes%20de%20editor%20de%20consola.png)  

4. **Nombre de rama inicial**:  
   - Selecciona **main** (estándar moderno en lugar de "master").  
   ![Nombre de repositorio](./assets/img/configuracion%20de%20nombre%20de%20repositorio.png)  

5. **Ajuste del PATH (¡Crítico!)**:
   - **Selecciona**:  
     ``` 
     Git from the command line and also from 3rd-party software 
     ```  
     - Esto permite usar `git` en **CMD**, **PowerShell** y editores de código.  
   ![Configuración de path](./assets/img/configuracion%20de%20path.png)  

6. **Manejador de credenciales**:  
   - Usa **Git Credential Manager Core** (almacena contraseñas de forma segura).  
   ![Manejador de credenciales](./assets/img/manejador%20de%20credenciales.png)  

7. **Finales de línea (Line Endings)**:  
   - Elige:  
     ```  
     Checkout Windows-style, commit Unix-style line endings  
     ```  
     - Evita problemas de compatibilidad entre Windows/Linux/macOS.  

8. **Terminal predeterminada**:  
   - **MinTTY** (más potente que la terminal de Windows).  

9. **Opciones extra**:  
   - Activa todas (habilitan caché y symlinks).  

---

#### **Paso 4: Finalizar Instalación**  
1. Haz clic en **Install**:  
   ![Instalar](./assets/img/instalar.png)  
2. Espera a que termine el proceso (barra de progreso).  
3. Haz clic en **Finish**.  

---

### **Verificación de la Instalación**  
1. Abre **Git Bash** desde el menú de Inicio:  
   ![git bash](./assets/img/git%20bash.png)  
2. Ejecuta:  
   ```bash 
   git --version
   ```  
   - Debe mostrar: `git version 2.xx.x.windows.x`  
   ![git --version](./assets/img/git%20--version.png)  

---

### **Configuración Inicial Obligatoria**  
Configura tu identidad para que Git asocie tus commits:  
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```  
![git global](./assets/img/git%20global%20user.png)  

#### Verifica la configuración:  
```bash
git config --global user.name  # Muestra tu nombre
git config --global user.email # Muestra tu email
```  

---

### **Notas Clave**  
1. **SSH**:  
   - La opción predeterminada (OpenSSH) funciona con GitHub/GitLab.  
   ![Conexión SSH](./assets/img/conexion%20SSH.png)  

2. **Recuperar configuración**:  
   - Los ajustes se guardan en `C:\Users\<tu_usuario>\.gitconfig`.  

3. **Actualizar Git**:  
   - Repite el proceso de instalación: Las nuevas versiones se instalan sobre la existente.  

4. **Solución de errores**:  
   - Si `git` no se reconoce en PowerShell:  
     1. Reinicia el sistema.  
     2. Verifica que la ruta de Git esté en `PATH` (busca "variables de entorno" en Windows).  

---

**¡Listo!** Ahora puedes usar Git en:  
- **Git Bash**: Terminal optimizada para comandos Unix.  
- **CMD/PowerShell**: Usa `git` directamente.  
- **Editores de código** (VS Code, IntelliJ): Integración automática.