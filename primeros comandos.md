## Guía Completa de Instalación de Git y Primeros Comandos Esenciales 🛠️  

Antes de dominar Git, necesitamos instalarlo correctamente. Aquí tienes guías detalladas para cada sistema operativo, ¡incluyendo WSL para Windows!  

---

### 📥 Instalación de Git en Diferentes Sistemas  

#### **Windows (Opción 1: Nativo)**  
1. Descarga el instalador desde [git-scm.com](https://git-scm.com/download/win)  
2. Ejecuta el `.exe` y acepta todas las opciones predeterminadas  
3. Verifica en PowerShell o CMD:  
```bash
git --version  # Debe mostrar "git version x.x.x"
```

[Tutorial completo](./assets/docs/install%20in%20windows.md)

#### **Windows (Opción 2: WSL - Recomendado para desarrollo profesional)**  
1. Abre PowerShell como **Administrador**:  
```powershell
wsl --install  # Instala Ubuntu por defecto
```  
2. Reinicia tu computadora  
3. Al iniciar sesión, crea usuario/contraseña de Linux  
4. Actualiza paquetes:  
```bash
sudo apt update && sudo apt upgrade
```  
5. Instala Git en WSL:  
```bash
sudo apt install git
```

#### **macOS**  
1. Via **Homebrew** (recomendado):  
```bash
brew install git
```  
2. Via instalador gráfico: [Descargar desde git-scm.com](https://git-scm.com/download/mac)

#### **Linux (Debian/Ubuntu)**  
```bash
sudo apt update
sudo apt install git
```

> ✅ **Verifica instalación en TODOS los sistemas:**  
> ```bash
> git --version
> ```  
> Si ves algo como `git version 2.34.1`, ¡éxito!

---

### ⚙️ Configuración Inicial de Git  
Antes de empezar, personaliza tu identidad:  
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```  
**Tip:** Usa el mismo email asociado a GitHub/GitLab.

---

### 🚀 Primeros Pasos: Comandos Básicos de Git  

#### 1. **Crear y preparar tu proyecto**  
```bash
# Limpia la terminal (opcional)
clear  

# Crea carpeta y navega a ella
mkdir mi-proyecto-épico
cd mi-proyecto-épico
```

#### 2. **Inicializar repositorio**  
```bash
git init  # Crea rama "master" por defecto
```  
**¿Prefieres "main"?**  
```bash
git config --global init.defaultBranch main  # Cambio permanente
git branch -m main  # Renombra en este repositorio
```

#### 3. **Verificar estado del repositorio**  
```bash
git status
```  
> Muestra archivos no rastreados/modificados (tu "mapa" del proyecto).

#### 4. **Añadir archivos al staging area**  
Crea un archivo `index.html` y luego:  
```bash
git add index.html  # Añade UN archivo
git add .           # Añade TODOS los archivos nuevos/modificados
```

#### 5. **Confirmar cambios (Commit)**  
```bash
git commit -m "Mi primer commit: estructura base HTML"
```  
> **-m** agrega mensaje descriptivo (¡OBLIGATORIO!).

#### 6. **Revisar historial**  
```bash
git log  # Muestra commits con autor/fecha/mensaje
```  
**Salida útil:**  
```bash
commit a1b2c3d4... (HEAD -> main)
Author: Tu Nombre <tu@email.com>
Date:   Fri May 30 12:30:00 2025 -0500

    Mi primer commit: estructura base HTML
```

---

### 🧠 Recomendaciones Clave para Principiantes  
- **Siempre verifica `git status`** antes de añadir/commitear.  
- **Mensajes de commit claros**: "Fix login bug" > "cambios".  
- **Atajo útil**:  
```bash
git commit -am "Mensaje"  # Añade automaticamente cambios y hace commit
```  
*(Solo funciona para archivos YA rastreados)*  

---

### 🔍 ¿Olvidaste un comando? ¡Ayuda integrada!  
```bash
git help          # Muestra ayuda general
git add --help    # Ayuda específica para "add"
```

---

### 💻 Resumen Visual del Flujo Básico  
```mermaid
graph LR
    A[Archivos Modificados] --> B{git add}
    B --> C[Staging Area]
    C --> D{git commit}
    D --> E[Repositorio Local]
```

---

### 🎯 Próximos Pasos  
Ahora que tienes Git instalado y conoces los comandos básicos:  
1. Experimenta creando/borrando archivos y usando `add`/`commit`.  
2. Intenta modificar un archivo existente y haz otro commit.  

> ⚠️ **Reto**: ¿Qué pasa si ejecutas `git log --oneline`?  


🔗 **Descarga gratis**: [Cheat Sheet de Comandos Git](./assets/docs/github-git-cheat-sheet.pdf)  

