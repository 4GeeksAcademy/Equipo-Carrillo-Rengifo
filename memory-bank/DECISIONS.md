# Registro de decisiones

Usar este formato por entrada: **Decisión / Fecha / Motivo / Alternativas / Consecuencias / Estado**. Estados permitidos: propuesta, aprobada, sustituida. Aprobación de una dirección para el prototipo no equivale a aprobación de identidad, contenido comercial, licencias ni calidad técnica.

## D-001 — Stack HTML y Tailwind v4
- **Fecha:** 2026-10-29
- **Decisión:** Usar HTML5 estático y Tailwind CSS v4 vía CDN oficial de navegador, con clases utility coherentes y responsive.
- **Motivo:** Ajustarse al ejercicio y evitar dependencias/build no pedidos.
- **Alternativas:** Compilación local de Tailwind v4; se reserva si CDN no sirve para el flujo acordado.
- **Consecuencias:** Mantener el stack implementado; no añadir scripts propios ni configuraciones v3. La existencia de una hoja `styles.css` no se establece como requisito.
- **Estado:** aprobada para el prototipo.

## D-002 — Identidad conceptual y tokens
- **Fecha:** 2026-10-29
- **Decisión:** Aplicar en el prototipo la dirección de arte marfil `#F7F4EE`, grafito `#242321`, borgoña `#6E1F32`, superficies cálidas y serif/sans locales descrita en `DESIGN-SYSTEM.md`.
- **Motivo:** Dirección editorial premium compatible con briefing sin adjudicar identidad oficial.
- **Alternativas:** Blanco puro/acento negro; se mantiene la propuesta cálida para revisión.
- **Consecuencias:** No representa identidad oficial. Contraste y conformidad de accesibilidad requieren pruebas; no se impone un archivo CSS común.
- **Estado:** aprobada para el prototipo.

## D-003 — Rutas de las cinco vistas
- **Fecha:** 2026-10-29
- **Decisión:** Las vistas integradas usan `index.html`, `catalogo.html`, `producto.html`, `carrito.html` y `checkout.html`.
- **Motivo:** URLs sencillas, internas y consistentes con plantilla estática.
- **Alternativas:** Rutas con directorios o nombres alternos.
- **Consecuencias:** Mantener rutas consistentes; comprobar enlaces como parte de la validación.
- **Estado:** aprobada para el prototipo.

## D-004 — Reutilización de componentes sin JS
- **Fecha:** 2026-10-29
- **Decisión:** Mantener consistencia visual de navbar/footer y contenido compartido mediante revisión controlada de las páginas estáticas.
- **Motivo:** Reutilización honesta compatible con HTML estático y prohibición de JS/plantillas.
- **Alternativas:** Componentes/imports, descartados por incompatibilidad con el alcance.
- **Consecuencias:** Actualizaciones duplicadas se coordinan y se validan por diff en PR; no se presupone hoja CSS compartida.
- **Estado:** aprobada para el prototipo.

## D-005 — Carácter estático del prototipo
- **Fecha:** 2026-10-29
- **Decisión:** Búsqueda, filtros, cantidad/carrito y checkout son presentación visual; sin operaciones ni datos de tarjetas reales.
- **Motivo:** Restricciones explícitas del ejercicio.
- **Alternativas:** Simulación dinámica; prohibida en esta fase.
- **Consecuencias:** Etiquetar límites; formularios no aparentan procesar pagos.
- **Estado:** propuesta.

## D-006 — Catálogo y datos aún no oficiales
- **Fecha:** 2026-10-29
- **Decisión:** Definir referencia uniforme EUR, SKU, categorías y tallas para ejemplos, sin atribuirla a cliente real.
- **Motivo:** Consistencia entre las cinco vistas.
- **Alternativas:** Datos del cliente (no proporcionados).
- **Consecuencias:** Valores y tratamiento fiscal requieren aprobación; no inventar promociones/disponibilidad.
- **Estado:** propuesta.