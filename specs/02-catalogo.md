# SPEC 02 — Catálogo (`catalogo.html`)

> Ruta propuesta, pendiente de aprobación. Filtros y catálogo son visuales; no filtran resultados.

## Objetivo
Permitir explorar visualmente la colección de muestra de forma consistente y adaptable.

## Estructura HTML
Navbar, `main` con breadcrumb opcional, h1, introducción breve, controles de filtro agrupados y rejilla semántica de artículos, footer.

## Componentes obligatorios
- Navbar/footer y filtros visuales por categoría y talla.
- Rejilla de exactamente 20 productos de referencia; en escritorio ancho: 4 columnas x 5 filas.
- Cards compartidas, con enlace a `producto.html` (se puede mostrar un único producto de detalle como muestra; documentar que no hay 20 páginas de detalle individuales).

## Contenido mínimo
Veinte registros de `shared-components.md`, cada uno con imagen autorizada, alt, nombre, SKU visible o disponible en detalle, precio EUR y categoría. Valores de filtros deben corresponder a la taxonomía común. Sin etiquetas de stock/discount no confirmadas.

## Elementos compartidos
Todos los descritos en `shared-components.md`; precios, SKU y taxonomía idénticos en todas las vistas.

## Responsive
4 columnas desktop; 3 tablet amplia, 2 móvil. Filtros apilados/ajustados para móvil y con labels. No usar controles de apariencia interactiva que aparenten filtrar. Se pueden presentar como controles deshabilitados con explicación “Filtros de demostración” o como navegación enlazada a secciones/categorías existentes.

## Accesibilidad
Filtros en `fieldset`/`legend` y controles con labels; si no operan, `disabled` y texto explicativo, no controles engañosos. Tarjetas con enlaces descriptivos y alt.

## SEO
Title/description propios, H1 “Catálogo”, enlaces rastreables, texto visible, metadatos base y sin schema de oferta si disponibilidad no está confirmada.

## Criterios de aceptación
- [ ] Exactamente 20 cards, con 4x5 en escritorio de referencia.
- [ ] 2+ columnas en móvil sin desbordamiento y grilla adaptable en tablet.
- [ ] Filtros categoría/talla presentes y declarados prototipo.
- [ ] Datos y rutas respetan catálogo de referencia.
- [ ] Validación HTML, teclado, SEO y consistencia completados.

## Exclusiones
No filtrar, ordenar, buscar, paginar, guardar selección, consultar inventario ni cargar productos vía API.