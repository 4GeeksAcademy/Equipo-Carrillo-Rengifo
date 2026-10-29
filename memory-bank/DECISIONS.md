# Registro de decisiones

Usar este formato por entrada: **Decisión / Fecha / Motivo / Alternativas / Consecuencias / Estado**. Estados permitidos: propuesta, aprobada, sustituida.

## D-001 — Stack HTML y Tailwind v4
- **Fecha:** 2026-10-29
- **Decisión:** Proponer HTML5 estático, Tailwind CSS v4 vía CDN oficial de navegador ya mencionado por el README español, y CSS mínimo común.
- **Motivo:** Ajustarse al ejercicio y evitar dependencias/build no pedidos.
- **Alternativas:** Compilación local de Tailwind v4; se reserva si CDN no sirve para el flujo acordado.
- **Consecuencias:** Probar CDN/utilidades antes de implementar; no añadir scripts propios ni configuraciones v3.
- **Estado:** propuesta.

## D-002 — Identidad conceptual y tokens
- **Fecha:** 2026-10-29
- **Decisión:** Proponer marfil `#F7F4EE`, grafito `#242321`, borgoña `#6E1F32`, superficies cálidas y serif/sans del sistema; tokens CSS comunes.
- **Motivo:** Dirección editorial premium compatible con briefing sin adjudicar identidad oficial.
- **Alternativas:** Blanco puro/acento negro; se mantiene la propuesta cálida para revisión.
- **Consecuencias:** Contraste por comprobar; un solo archivo de tokens y sin overrides por página.
- **Estado:** propuesta.

## D-003 — Rutas de las cinco vistas
- **Fecha:** 2026-10-29
- **Decisión:** Proponer `index.html`, `catalogo.html`, `producto.html`, `carrito.html`, `checkout.html`.
- **Motivo:** URLs sencillas, internas y consistentes con plantilla estática.
- **Alternativas:** Rutas con directorios o nombres alternos.
- **Consecuencias:** Aprobación previa y uso idéntico en navbar, cards y checkout.
- **Estado:** propuesta.

## D-004 — Reutilización de componentes sin JS
- **Fecha:** 2026-10-29
- **Decisión:** Fragmentos canónicos documentados, copia controlada y revisión cruzada de navbar/footer; una hoja CSS compartida.
- **Motivo:** Reutilización honesta compatible con HTML estático y prohibición de JS/plantillas.
- **Alternativas:** Componentes/imports, descartados por incompatibilidad con el alcance.
- **Consecuencias:** Actualizaciones duplicadas se coordinan y se validan por diff en PR.
- **Estado:** propuesta.

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