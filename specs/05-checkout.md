# SPEC 05 — Checkout (`checkout.html`)

> `checkout.html` está integrado en `main` como formulario/prototipo estático; no incluir datos de tarjetas ni procesar pagos. Esta SPEC no declara completados sus criterios de aceptación.

## Objetivo
Mostrar la estructura y los campos habituales de un checkout en una experiencia explícitamente demostrativa.

## Estructura HTML
Navbar compartida, h1 “Finalizar pedido — demostración”, indicador ordenado de los pasos 1 Datos personales, 2 Entrega, 3 Pago, formulario semántico agrupado en `fieldset`/`legend`, resumen de pedido opcional y footer.

## Componentes obligatorios
- Indicador visual de tres pasos.
- Paso 1: nombre, apellidos, correo y teléfono solo si necesarios para maqueta.
- Paso 2: dirección, ciudad, código postal y país como muestra.
- Paso 3: mostrar el concepto “Pago con tarjeta” solo como apartado explicativo. No pedir número, vencimiento, CVV ni datos reales. Usar campos de ejemplo no sensibles si la rúbrica obliga a visualizar campos, con texto inequívoco “No introducir datos reales; prototipo sin procesamiento”; preferible no ofrecer inputs de tarjeta.
- Navbar/footer; CTA no transaccional o deshabilitado con explicación.

## Contenido mínimo
Los tres pasos visibles simultáneamente, sin prometer navegación progresiva. Contenido, campos y valores de ejemplo no deben exponer datos personales reales. Las rutas y textos reconocen que no hay compra.

## Elementos compartidos
Contenedor, tipografía, navbar, footer, inputs, botones, tokens y formato de precio. Si se muestra resumen, los datos coinciden con carrito.

## Responsive
Formulario en una columna en móvil; en desktop una columna de campos y resumen secundario opcional. Controles nunca menores que el espacio disponible; no scroll horizontal.

## Accesibilidad
Pasos marcados como lista ordenada y estado actual expresado también en texto; etiquetas persistentes, agrupación por paso, orden de teclado lógico, foco visible y errores/instrucciones textuales. No simular validación/confirmación con JS.

## SEO
Title/description únicos, h1, semántica, idioma, viewport. No incluir datos estructurados de pedido/oferta ni datos personales.

## Criterios de aceptación
- [ ] Pasos 1, 2 y 3 visibles y legibles.
- [ ] Diseño se adapta a 320–1440 px.
- [ ] No pide ni almacena tarjeta real, ni integra pasarela.
- [ ] Formulario tiene labels, tipos y nombres coherentes.
- [ ] No hay promesa de navegación dinámica o transacción.
- [ ] Enlaces, SEO, teclado y validación revisados.

## Exclusiones
No envío, pago, tokenización, validación por JavaScript, estado de pedido, persistencia ni datos sensibles reales.