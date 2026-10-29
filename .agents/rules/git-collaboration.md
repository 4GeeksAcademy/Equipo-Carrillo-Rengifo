# Regla: colaboración Git

- No desarrolles directamente en `main`. Trabaja en una rama por vista o funcionalidad, acordada con el equipo.
- Usa commits frecuentes y descriptivos. Push después de cada etapa funcional según el flujo acordado y abre PR para integrar.
- Antes de abrir PR, actualiza tu rama con `main` usando la estrategia aprobada por el equipo; inspecciona conflictos y conserva el trabajo de ambas partes.
- No hagas force-push, reset destructivo ni sobrescribas cambios ajenos sin acuerdo explícito.
- Los archivos compartidos (estilos/tokens, navbar/footer, datos de referencia y reglas) se modifican preferentemente en PR separadas, revisadas por ambos integrantes.
- Antes de editar, revisa `git status`, rama, alcance asignado y cambios existentes. Nunca incluyas cambios ajenos en tu PR.
- No ejecutes operaciones Git de escritura sin autorización explícita en esta fase de fundaciones.