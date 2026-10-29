# SPEC 04 — Carrito (`carrito.html`)

> Ruta propuesta, pendiente de aprobación. Resumen estático: los importes son ejemplos y no corresponden a una orden real.

## Objetivo
Mostrar un resumen comprensible de tres artículos y un ejemplo matemáticamente coherente de subtotal, impuestos y total.

## Estructura HTML
Navbar, `main` con h1 y lista de tres líneas (artículo, unidad, cantidad, total de línea), resumen semántico de importes, CTA y footer.

## Componentes obligatorios
Tres productos, miniatura, nombre, SKU, precio unitario, cantidad, total por línea; subtotal, impuestos, total; botón/enlace Comprar y navbar/footer.

## Datos del ejemplo (requieren aprobación)
Para evitar presentar un tipo fiscal real como confirmado, ejemplo aritmético marcado “Importes ilustrativos para el prototipo; tasa de ejemplo 20%, no es cotización fiscal”: Camisa de lino Atelier `CAM-LIN-001` €89,00 x1 = €89,00; Pantalón recto Épure `PAN-REC-002` €120,00 x1 = €120,00; Bolso Le Marché `ACC-BOL-003` €31,00 x1 = €31,00. Subtotal neto €240,00 + impuesto ilustrativo €48,00 (20%) = total €288,00. Moneda/formato común según `shared-components.md`. Confirmar si importes deben ser netos o incluir impuestos antes de cambiar el copy.

## Elementos compartidos
Navbar/footer, miniatura/product card, dato de producto, SKU, precio y tokens. No crear una variante de precio exclusiva del carrito.

## Responsive
En escritorio puede usarse lista + resumen lateral. En móvil una columna; etiquetas de cantidades y totales claras, sin tabla que desborde.

## Accesibilidad
Estructura de lista con nombres; cada miniatura con alt; cantidad se presenta como texto/disabled y no como control falso. Explicar el carácter ilustrativo de impuestos. CTA “Continuar al checkout” puede enlazar a `checkout.html` con texto que no implique transacción; si se conserva “Comprar”, indicar prototipo y no procesamiento.

## SEO
Title/description únicos, h1, enlaces internos. Carrito privado no es real, pero no añadir noindex sin decisión de publicación; evitar schema Product/Offer por resumen de carrito.

## Criterios de aceptación
- [ ] Hay exactamente 3 líneas de ejemplo.
- [ ] Totales de línea: €89,00, €120,00 y €31,00; suma €240,00.
- [ ] Impuesto de ejemplo €48,00 y total €288,00; copy lo identifica como supuesto ilustrativo.
- [ ] SKU y nombres coinciden con catálogo/producto.
- [ ] CTA lleva a checkout estático y no aparenta compra real.
- [ ] Responsive y validación completadas.

## Exclusiones
No persistencia, modificación de cantidades, eliminar líneas, cupones, cálculo en vivo, reserva ni cobro.