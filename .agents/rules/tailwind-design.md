# Regla: Tailwind y sistema visual

- Usa exclusivamente Tailwind CSS v4. En esta plantilla el método sugerido es el CDN oficial de navegador documentado en `README.es.md`; no mezcles v3 ni agregues build tooling/dependencias sin aprobación.
- Consulta `memory-bank/DESIGN-SYSTEM.md`. Sus tokens son la fuente visual común y, hasta su aprobación, son propuestas.
- Compón utilidades Tailwind con los tokens CSS canónicos; evita duplicar valores hexadecimales, crear paletas por página o usar valores arbitrarios cuando hay un token equivalente.
- No introduzcas un color, fuente, breakpoint, escala de espaciado o estilo nuevo sin actualizar la especificación y obtener aprobación del equipo.
- El CSS adicional debe limitarse a tokens globales o necesidades justificadas que no cubran las utilidades. No crear hojas independientes por vista.
- Mantén los contratos de componentes de `specs/shared-components.md`. No presentes elementos visuales estáticos como si tuvieran funcionalidad real.