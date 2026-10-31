# SPEC 03 — Producto (`producto.html`)

> `producto.html` está integrado en `main`. Producto de muestra; selección y carrito no ejecutan operación. Esta SPEC no declara completados sus criterios de aceptación.

## Objetivo
Describir con detalle un artículo y ofrecer una presentación clara de sus atributos y precio.

## Estructura HTML
Navbar, breadcrumb opcional, `main` con una ficha de producto `article`, región de imágenes y región de detalles, secciones descriptivas y footer.

## Componentes obligatorios
- En escritorio dos columnas: imagen a izquierda (aprox. mitad de contenedor), información a derecha.
- Nombre (h1), SKU, precio EUR, talla, cantidad y CTA “Añadir al carrito” de presentación.
- Descripción detallada, materiales y uso recomendado.
- Navbar/footer compartidos.

## Contenido mínimo
Usar artículo con identidad exacta del catálogo: nombre “Camisa de lino Atelier”, SKU `CAM-LIN-001`, precio de muestra `€ 89,00`, categoría camisas, sujeto a aprobación y claramente no oficial. Confirmar o reemplazar este registro de ejemplo antes de publicar. Materiales/uso solo si se definen como datos ficticios explícitos y coherentes. No hacer afirmaciones de composición no verificadas.

## Elementos compartidos
Tokens, navbar/footer, card/precio, SKU, imagen editorial y formato. Los datos de producto deben coincidir con catálogo y carrito cuando se refiera al mismo artículo.

## Responsive
En móvil apilar imagen y texto; controles al ancho disponible, sin recortes. En desktop mantener aproximadamente 50/50.

## Accesibilidad
Imágenes con alt útil, select de talla con label y opciones documentadas, cantidad no operativa claramente estática o campo deshabilitado explicado. CTA puede ser botón deshabilitado con nota de prototipo, o enlace al carrito si el equipo acuerda flujo solo visual; no afirmar que añade.

## SEO
Title con nombre del producto, meta description única, h1 producto, contenido de materiales/descripción indexable. `Product` JSON-LD solo con datos visibles consistentes; `Offer` únicamente si precio y availability están aprobados. No inventar valoraciones.

## Criterios de aceptación
- [ ] Dos columnas aprox. 50/50 en desktop y composición apilada móvil.
- [ ] Nombre, SKU y precio coinciden con referencia.
- [ ] Talla, cantidad, descripción, materiales y uso están documentados.
- [ ] No se asevera composición, descuento, stock ni operación real sin datos.
- [ ] Accesibilidad, SEO y validez comprobados.

## Exclusiones
No variantes dinámicas, inventario, cálculo de precio, favoritos ni añadido real al carrito.