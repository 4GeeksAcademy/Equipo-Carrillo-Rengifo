# Instrucciones para agentes

## Estado del proyecto
Este repositorio es una plantilla HTML de 4Geeks. La arquitectura del e-commerce está documentada como **propuesta pendiente de aprobación**. En esta fase no se deben implementar las páginas ni modificar los archivos originales de la plantilla.

## Lectura obligatoria antes de trabajar
1. Lee este archivo y las reglas aplicables de `.agents/rules/`.
2. Lee `memory-bank/PROJECT.md` y `memory-bank/DESIGN-SYSTEM.md`.
3. Lee la SPEC de la vista asignada en `specs/` y `specs/shared-components.md`.
4. Consulta `memory-bank/CONTEXT.md`, `DECISIONS.md` y `PROGRESS.md`.
5. Confirma con el equipo que la arquitectura y los componentes compartidos están aprobados; revisa rama y archivos autorizados.
6. Implementa únicamente el alcance solicitado. No edites páginas asignadas a otra persona ni rediseñes componentes compartidos por iniciativa propia.
7. Comprueba consistencia visual y semántica; informa cambios, pruebas realizadas y pendientes.

## Reglas centrales
- Stack permitido: HTML5 semántico, Tailwind CSS v4 y CSS adicional mínimo justificado. Sin frameworks, JavaScript personalizado, backend, APIs ni dependencias nuevas.
- No inventes marca corporativa, datos de contacto, valoraciones, disponibilidad, ofertas ni datos estructurados. Las decisiones visuales documentadas siguen siendo propuestas hasta que el equipo las apruebe.
- Consulta la documentación antes de cambiar cualquier archivo. No sobrescribas trabajo ajeno.
- No realices commit, push, merge, reset ni cambios de rama salvo solicitud explícita.

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