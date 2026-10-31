# Instrucciones para agentes

## Estado del proyecto
Este repositorio contiene un prototipo estático de e-commerce con cinco vistas HTML integradas en `main`: `index.html`, `catalogo.html`, `producto.html`, `carrito.html` y `checkout.html`. La dirección visual y los patrones de diseño documentados están aprobados para el prototipo, pero no constituyen identidad oficial de una marca. Antes de cada cambio confirma rama, archivos autorizados y estado de trabajo; la integración existente no sustituye la revisión ni la validación de la tarea actual.

## Lectura obligatoria antes de trabajar
1. Lee este archivo y las reglas aplicables de `.agents/rules/`.
2. Lee `memory-bank/PROJECT.md` y `memory-bank/DESIGN-SYSTEM.md`.
3. Lee la SPEC de la vista asignada en `specs/` y `specs/shared-components.md`.
4. Consulta `memory-bank/CONTEXT.md`, `DECISIONS.md` y `PROGRESS.md`.
5. Revisa el estado de aprobación en `memory-bank/DECISIONS.md`; consulta al equipo antes de cambiar decisiones ya aprobadas o datos que continúen pendientes. Revisa rama y archivos autorizados.
6. Implementa únicamente el alcance solicitado. No edites páginas asignadas a otra persona ni rediseñes componentes compartidos por iniciativa propia.
7. Comprueba consistencia visual y semántica; informa cambios, pruebas realizadas y pendientes.

## Reglas centrales
- Stack permitido: HTML5 semántico, Tailwind CSS v4 y CSS adicional mínimo justificado. Sin frameworks, JavaScript personalizado, backend, APIs ni dependencias nuevas.
- No inventes marca corporativa, datos de contacto, valoraciones, disponibilidad, ofertas ni datos estructurados. La dirección visual indicada como aprobada en `memory-bank/DESIGN-SYSTEM.md` aplica al prototipo, no confirma identidad oficial ni aprueba datos comerciales.
- Consulta la documentación antes de cambiar cualquier archivo. No sobrescribas trabajo ajeno.
- No realices commit, push, merge, reset ni cambios de rama salvo solicitud explícita.

Las pruebas no se consideran aprobadas por el mero hecho de que las páginas estén integradas. Registra herramientas, fecha y evidencia para cada validación. No declares aprobados permisos de imágenes sin documentación comprobable de autoría/licencia y uso.

## Mapa de lectura por tarea
- Toda tarea: `PROJECT.md`, `DESIGN-SYSTEM.md`, `DECISIONS.md`, `PROGRESS.md`.
- Identidad y audiencia: `memory-bank/CONTEXT.md`.
- HTML: `.agents/rules/html-semantics.md`.
- Tailwind y estilos: `.agents/rules/tailwind-design.md`.
- Responsive/accesibilidad: `.agents/rules/responsive-accessibility.md`.
- SEO/schema: `.agents/rules/seo-schema.md` y `specs/quality-acceptance.md`.
- Git/equipo: `.agents/rules/git-collaboration.md` y `specs/collaboration-workflow.md`.
- Vistas/componentes: SPEC correspondiente y `specs/shared-components.md`.

## Conflictos de documentación
Si una SPEC contradice una regla, no improvises: detén el cambio y solicita aclaración. Registra los acuerdos aprobados en `memory-bank/DECISIONS.md` y actualiza los documentos afectados en una PR específica.