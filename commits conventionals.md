Nombrar los commits de manera efectiva en Git es una práctica fundamental para cualquier desarrollador, especialmente en proyectos colaborativos. No solo facilita la comprensión del historial del proyecto, sino que también mejora la depuración, la revisión de código y la automatización de herramientas como la generación de changelogs.

La "mejor práctica" universalmente aceptada es seguir las "Conventional Commits" (Commits Convencionales). Esta especificación proporciona un conjunto ligero de reglas para crear mensajes de commit explícitos y con un significado semántico.

Aquí te detallo cómo estructurar tus commits siguiendo las Conventional Commits y otras buenas prácticas:

Estructura de un Commit Convencional
Un mensaje de commit convencional consta de un encabezado (header) obligatorio, y un cuerpo (body) y pie de página (footer) opcionales.

<tipo>[<ámbito>]: <descripción>

[cuerpo_opcional]

[pie_de_pagina_opcional]

1. Encabezado (Header) - Obligatorio
Es la primera línea del mensaje de commit y debe ser concisa y clara.

<tipo> (Type): Un sustantivo que describe la naturaleza del cambio. Es la parte más importante y define el propósito principal del commit. Algunos tipos comunes incluyen:

feat: Una nueva característica para el usuario (se mapea a un minor en el Versionado Semántico).
fix: Una corrección de un error (se mapea a un patch en el Versionado Semántico).
docs: Cambios en la documentación (ej. README, comentarios en el código).
style: Cambios que no afectan el significado del código (ej. formato, puntos y coma, espacios en blanco).
refactor: Un cambio de código que no agrega una característica ni corrige un error, pero mejora la estructura o legibilidad.
perf: Un cambio de código que mejora el rendimiento.
test: Añadir pruebas faltantes o corregir pruebas existentes.
chore: Otros cambios que no son código de producción (ej. actualizaciones de dependencias, configuración de herramientas de construcción).
build: Cambios que afectan el sistema de compilación o dependencias externas (ej. npm, gulp).
ci: Cambios en los archivos y scripts de configuración de CI (Continuous Integration).
revert: Un commit que revierte un commit anterior.
[<ámbito>] (Scope) - Opcional: Un sustantivo o una frase corta entre paréntesis que indica la parte del código afectada por el cambio. Ayuda a dar más contexto.

Ejemplos: (auth), (ui), (api), (database), (componente-x).
Si el cambio es global o afecta a múltiples ámbitos, puedes omitirlo.
<descripción> (Description / Subject): Una descripción concisa del cambio.Ejemplos de encabezados:

Usa el modo imperativo y el tiempo presente: Piensa como si estuvieras dando una orden. "Añadir característica X" en lugar de "Añadí característica X" o "Se añadió característica X".
No capitalices la primera letra.
No termines con un punto.
Manténlo corto: Idealmente, menos de 50-72 caracteres (muchas herramientas de Git truncan mensajes más largos).
<!---->
feat(auth): add google login option
fix(ui): correct pagination overflow issue
docs: update README with setup instructions
refactor(utils): simplify date formatting function
chore: update dependencies
2. Cuerpo (Body) - Opcional
Si necesitas más detalles sobre el cambio, su motivación o por qué se hizo de esa manera, usa el cuerpo del commit.

Separado del encabezado por una línea en blanco.

Usa el modo imperativo y el tiempo presente también aquí.

Explica el "qué" y el "por qué": Describe el contexto, las decisiones tomadas y las implicaciones del cambio.

Envuelve las líneas a 72 caracteres para una mejor legibilidad en la mayoría de las interfaces de Git.**Ejemplo:**fix(auth): correct token validation logic

The token validation was failing due to a mismatch in timezones between the server and client. This fix ensures that the token expiration is checked against the server's current time.

3. Pie de Página (Footer) - Opcional
Utilizado para metadatos o para referenciar problemas (issues) o cambios que rompen la compatibilidad (breaking changes).

Separado del cuerpo por una línea en blanco.

Referencia a issues:

Closes #123: Si el commit resuelve el problema #123.
Fixes #456, #789: Si resuelve múltiples problemas.
See also #101: Si el commit está relacionado pero no lo cierra.
Cambios que rompen la compatibilidad (Breaking Changes):Si tu commit introduce un cambio que rompe la compatibilidad (es decir, los usuarios existentes de tu código necesitarán adaptar su código), debes indicarlo claramente.**Ejemplo con Breaking Change:**feat(api)!: rename getUser to fetchUser

This commit renames the getUser API endpoint to fetchUser to better reflect its asynchronous nature.

BREAKING CHANGE: The getUser endpoint has been replaced by fetchUser. Consumers of the API must update their calls to fetchUser.

Añade un ! después del type o scope en el encabezado (ej. feat!: add breaking change).
Añade una línea en el pie de página que comience con BREAKING CHANGE: seguida de una descripción clara de lo que cambió y cómo migrar.
Beneficios de Seguir Conventional Commits
Claridad del Historial: Facilita la navegación y comprensión del historial del proyecto.
Automatización: Permite que herramientas automaticen tareas como:
Generación de CHANGELOGs.
Determinación de la siguiente versión (ej. patch, minor, major en Versionado Semántico).
Disparar procesos de CI/CD.
Colaboración: Mejora la comunicación entre los miembros del equipo.
Depuración: Ayuda a identificar rápidamente el commit que introdujo un error.
Coherencia: Fomenta un estilo de commit uniforme en todo el equipo.
Consejos Adicionales para Buenos Commits
Commits atómicos: Cada commit debe representar un cambio lógico y único. Si estás corrigiendo un error y añadiendo una característica, haz dos commits separados. Esto hace que sea más fácil revertir, cherry-pick o entender cambios específicos.
Commits funcionales: Asegúrate de que el código sea compilable y, si es posible, ejecutable después de cada commit. Evita commits que dejen el proyecto en un estado roto.
Revisa tus cambios antes de hacer commit: Usa git status y git diff para asegurarte de que solo estás incluyendo los cambios que realmente pertenecen a ese commit. Usa git add -p (o git add --patch) para staging interactivo si necesitas seleccionar solo partes de un archivo.
Utiliza git commit -v o git commit sin -m: Esto abrirá tu editor de texto predeterminado, permitiéndote escribir mensajes de commit multilínea de forma más cómoda. El editor mostrará un diff de los cambios en el commit, lo cual es útil para escribir el mensaje.
Al adoptar estas prácticas, no solo tú te beneficiarás, sino que también contribuirás a un historial de proyecto más limpio, legible y útil para todo tu equipo.