# Workflow colaborativo y GitHub

> Flujo recomendado para dos integrantes; no se asignan tareas por nombre. Adaptar si el equipo acuerda otro proceso.

## Secuencia de trabajo
1. Crear rama documental `feature/project-foundation` desde `main`.
2. Revisar reglas, memoria, sistema visual y specs; acordar decisiones y rutas.
3. Abrir PR de fundaciones; ambos revisan y aprueban componentes/tokens compartidos.
4. Integrar la fundación en `main` mediante el flujo normal de GitHub.
5. Crear ramas independientes de vistas/funcionalidades desde `main` actualizado.
6. Implementar solo la SPEC asignada y mantener commits descriptivos y frecuentes.
7. Actualizar rama desde `main` antes de PR; resolver conflictos preservando cambios de ambos.
8. Abrir PR, revisar HTML, diseño, rutas y accesibilidad; registrar pruebas y pendientes.
9. Al integrar las cinco páginas, repetir validación de sitio completo y registrar PageSpeed.

## Ejemplos de ramas
- `feature/project-foundation`
- `feature/home`
- `feature/catalogo`
- `feature/producto`
- `feature/carrito`
- `feature/checkout`
- `fix/responsive`
- `fix/seo-performance`

## Convenciones de PR
Una PR por alcance acotado; no mezclar cambios de una vista ajena. Archivos compartidos (tokens, contratos, navbar/footer, datos) preferentemente en PR separada revisada por ambos. Incluir resumen, capturas de UI, lista de validaciones y limitaciones del prototipo. No cerrar una PR con rutas rotas o tokens propios.

## Actualizar la rama sin sobrescribir trabajo
Antes de actualizar, revisar `git status`, guardar/commitear cambios propios y confirmar rama. Obtener cambios de `main` y aplicar estrategia acordada (merge es opción conservadora para equipo pequeño; rebase solo si se entiende y no se reescribe historia publicada). Resolver cada conflicto comparando ambas versiones; no elegir “ours/theirs” globalmente ni descartar archivos ajenos. Probar enlaces/validación tras resolver. Si hay duda, parar y pedir revisión.

No usar `reset --hard`, force-push o comandos destructivos para resolver conflictos. Evitar cambios simultáneos a los mismos archivos compartidos; coordinarlos en PR específica. No incluir información secreta en commits.

## Responsabilidades
Asignar persona responsable y revisor en el tablero/PR cuando el equipo comunique la distribución. Hasta entonces dejar “Por asignar” en `PROGRESS.md` y no inferir nombres.