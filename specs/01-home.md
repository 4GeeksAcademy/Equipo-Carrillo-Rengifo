# SPEC 01 — Home (`index.html`)

> Ruta propuesta, pendiente de aprobación. Prototipo estático; aplicar `AGENTS.md`, reglas y contrato `shared-components.md`.

## Objetivo
Presentar la dirección editorial de la tienda y permitir acceso claro a catálogo y categorías.

## Estructura HTML
`header`/navbar compartida, `main` con un único `h1` dentro del hero, secciones de novedades y más vendidos, `footer` compartido. Un orden lógico, semántico y navegable.

## Componentes obligatorios
- Navbar canónica con logo conceptual aprobado, búsqueda no funcional, acceso de cuenta y rutas comunes.
- Hero de campaña con imagen autorizada, título, breve copy y enlace real a `catalogo.html`.
- Nuevos lanzamientos y Más vendidos, cada uno con cards horizontales en desktop (scroll por teclado/gesto solo si se conserva acceso; preferir rejilla adaptable y evitar carrusel sin JS).
- Footer canónico.

## Contenido mínimo
Título/descripcion de campaña, al menos 4 cards en cada franja como propuesta, nombre, imagen, alt y precio EUR. Mantener SKU, nombre y precio idénticos a `shared-components.md` si se comparte producto. No proclamar “más vendido” como hecho comercial: rotular como selección editorial o “Más vendidos (contenido de ejemplo)” hasta tener ventas verificadas.

## Elementos compartidos
Navbar, footer, botones, cards, tokens, rutas, formatos de precio e imágenes según `shared-components.md`.

## Responsive
Mobile-first; hero apila texto/imagen según ancho. Las cards se convierten en rejilla de 2 columnas móvil, hasta 4 en escritorio, o fila horizontal que no fuerce scroll de página. Validar 320/375/768/1024/1440.

## Accesibilidad
Un h1, alt contextual, enlaces con nombres descriptivos, foco visible, orden de lectura DOM y contraste. CTA como enlace si navega.

## SEO
Title/description únicos y descriptivos, contenido visible indexable, idioma es, meta viewport, alt y enlaces internos. No añadir datos organizacionales ficticios.

## Criterios de aceptación
- [ ] Navbar y footer coinciden con las demás páginas.
- [ ] Hero, lanzamientos, selección editorial y cards están presentes.
- [ ] Rutas internas destino existen y son coherentes.
- [ ] Producto repetido conserva nombre/SKU/precio.
- [ ] Sin scroll horizontal, errores Nu Validator ni elementos que prometan funcionalidad.
- [ ] Metadatos, contraste y teclado revisados.

## Exclusiones
No implementar búsqueda, cuenta, favoritos, filtros, animaciones JS, compra ni feed dinámico. Las etiquetas promocionales/de ventas requieren evidencia.