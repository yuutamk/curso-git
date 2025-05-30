# **Sistemas Informáticos: Conceptos Claves y Clasificación**

### **¿Qué define a un sistema informático?**  
Un sistema informático es una estructura integrada por componentes físicos (hardware), programas (software) y usuarios, que interactúan para gestionar, procesar, almacenar y distribuir información. El usuario actúa como el eje de control, supervisando las operaciones, mientras que el sistema transforma datos en resultados útiles y facilita su comunicación.

#### **Elementos esenciales:**  
- **Hardware:** Componentes tangibles como la CPU, memoria RAM o dispositivos de almacenamiento.  
- **Software:** Conjunto de instrucciones programadas que dictan las acciones del sistema, desde aplicaciones móviles hasta plataformas web.  
- **Interacción práctica:** Por ejemplo, al introducir una dirección en Google Maps, el software interpreta la solicitud, procesa datos geográficos y genera rutas personalizadas.  

#### **Funcionalidades clave:**  
1. **Procesamiento de datos:** Analiza volúmenes masivos de información de múltiples fuentes, permitiendo análisis integrales para decisiones estratégicas.  
2. **Almacenamiento:** Conserva registros históricos, facilitando la identificación de tendencias mediante comparativas temporales.  
3. **Transmisión:** Garantiza que la información crítica llegue a los destinatarios adecuados en tiempo oportuno, optimizando la ejecución de acciones.  

#### **Clasificación de sistemas informáticos:**  
- **Sistemas de Soporte a Decisiones (DSS):**  
  Herramientas estratégicas para directivos, enfocadas en evaluar escenarios, resolver problemas complejos y seleccionar alternativas viables mediante simulaciones y análisis predictivos.  

- **Sistemas de Planificación de Recursos Empresariales (ERP):**  
  Plataformas integradas que centralizan la gestión de operaciones internas (finanzas, logística, recursos humanos), mejorando la coordinación entre departamentos.  

- **Sistemas de Información Ejecutiva (EIS):**  
  Ofrecen acceso inmediato a datos consolidados de la organización, tanto internos como externos, presentándolos en formatos visuales o resumidos para agilizar la toma de decisiones gerenciales.  

Estos sistemas, adaptables a diversas necesidades organizacionales, optimizan la eficiencia operativa y fortalecen la competitividad en entornos dinámicos.


## **Control de Versiones: Funcionalidad y Tipos**  

### **¿Qué es el control de versiones?**  
Es un sistema software diseñado para registrar cambios en el código de un proyecto a lo largo del tiempo. Cada modificación se guarda como una *instantánea* permanente, lo que permite recuperar versiones anteriores en cualquier momento. Este proceso facilita la colaboración, evita pérdidas de información y mantiene un historial detallado de las actualizaciones.  

### **Ventajas clave:**  
- **Seguimiento organizado:**  
  Cada cambio incluye una descripción clara (ej.: "Corrección de errores" o "Nueva función"), permitiendo al equipo entender las modificaciones por versión, no por archivos individuales.  
- **Recuperación flexible:**  
  Acceso y restauración de cualquier versión almacenada, lo que facilita la corrección de errores o la reutilización de código previo.  
- **Colaboración eficiente:**  
  Sincroniza cambios entre usuarios, previniendo conflictos incluso cuando múltiples desarrolladores trabajan simultáneamente.  
- **Historial detallado:**  
  Registra quién realizó cada cambio, cuándo y por qué, brindando transparencia y permitiendo experimentar sin riesgos (si hay errores, se puede revertir a una versión estable).  

### **¿Cómo funciona?**  
1. **Repositorio y rama principal:**  
   Al crear un repositorio, se establece una *rama principal* (o *troncal*), que contiene la versión estable del código, lista para implementarse.  
2. **Bifurcaciones (*branches*):**  
   Los desarrolladores crean ramas secundarias a partir de la principal para trabajar en nuevas funciones o correcciones sin afectar la base estable. Una vez probados los cambios, estos se fusionan (*merge*) de vuelta a la rama principal.  

### **Tipos de sistemas de control de versiones**  

1. **Distribuidos (DVCS):**  
   - Cada colaborador tiene una copia completa del repositorio en la nube.  
   - Permiten trabajar sin conexión y sincronizar cambios después.  
   - Ideal para equipos remotos: evitan dependencia de redes lentas o VPN.  
   - Ejemplos: Git, Mercurial.  

2. **Centralizados (CVCS):**  
   - Todos los cambios se almacenan en un servidor central.  
   - Los usuarios deben conectarse al servidor para actualizar o descargar código.  
   - Ofrecen mayor seguridad al centralizar el control de accesos.  
   - Ejemplos: Subversion (SVN), Perforce.  

3. **Locales (LVCS):**  
   - Diseñados para uso individual: todo el historial se guarda en un solo equipo.  
   - Cada actualización se registra como una *revisión* incremental.  
   - Desventaja: Diagnóstico de errores complejo, ya que requiere revisar todas las revisiones para reconstruir un estado específico.  
   - Ejemplo: RCS (Revision Control System).  

### **Elección según necesidades:**  
- **Equipos colaborativos:** Optar por sistemas distribuidos o centralizados según la necesidad de flexibilidad o seguridad.  
- **Proyectos individuales:** Los sistemas locales son una opción sencilla, aunque limitada en escalabilidad.  

Estos sistemas son esenciales para mantener la integridad del código, optimizar el trabajo en equipo y garantizar la trazabilidad en el desarrollo de software.