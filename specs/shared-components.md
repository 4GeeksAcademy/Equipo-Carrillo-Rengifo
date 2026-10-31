# Contrato de componentes, contenido y recursos compartidos

> Contrato de referencia para las cinco vistas integradas en `main`. Las páginas existentes deben mantenerse coherentes con estos patrones; cambios adicionales siguen el flujo de revisión del equipo.

## Fuente visual única
Los tokens están descritos en `memory-bank/DESIGN-SYSTEM.md`. Las páginas integradas consumen variables mediante utilidades Tailwind y cargan Tailwind CDN v4. No se encontró una definición común de las variables `--color-*`; una hoja `styles.css` no es requisito explícito del proyecto. Mantener uso coherente de clases utility y breakpoints responsive; no añadir build tooling sin acuerdo.

## Reutilización estática
No existen imports, componentes, includes ni plantillas dinámicas en este stack. `shared-components.md` es el fragmento canónico de referencia: mantener bloques HTML de navbar y footer idénticos mediante copia controlada, hacer cambios en PR específica, revisar diff entre las cinco páginas tras propagar el cambio y ejecutar búsqueda de rutas/textos/tokens. No declarar una sincronización automática inexistente. Una revisión del equipo verifica el contrato.

## 1. Navbar canónica
- Wordmark provisional idéntico en todas las vistas: **“ATELIER — MARQUE À CONFIRMER”** como placeholder del prototipo; no es nombre real. Reemplazarlo solo cuando se confirme una identidad. Logotipo enlaza a `index.html` y tiene nombre accesible.
- Fondo `--color-canvas`; texto `--color-ink`; borde inferior `--color-line`; altura de referencia 80 px desktop y 64 px móvil; mismo padding del contenedor, baseline y tipografía en todas las páginas.
- Desktop: marca a la izquierda, búsqueda centrada (campo visible pero deshabilitado, con label y nota “Búsqueda de demostración; no disponible”), navegación principal con los enlaces Inicio, Catálogo, Producto, Carrito y Checkout, y Cuenta/Carrito a la derecha. Carrito aparece intencionalmente tanto en la navegación principal como en el acceso superior derecho. No existe vista de cuenta ni operación de carrito: mostrar “Cuenta (prototipo)” como texto no interactivo y enlazar Carrito únicamente a `carrito.html`; no inventar destinos ni simular acciones.
- Rutas de vistas propuestas y consistentes: Home `index.html`, Catálogo `catalogo.html`, Producto `producto.html`, Carrito `carrito.html`, Checkout `checkout.html`. Cuenta no tiene vista: no crear ruta ficticia.
- Móvil: reflujo en dos líneas o filas; enlaces principales visibles. No esconder navegación en un menú que requiera JS.
- Misma altura, logo, buscador, cuenta, links, color, orden y espaciado en cinco vistas. Las etiquetas y el orden de la navegación principal son idénticos: Inicio (`index.html`), Catálogo (`catalogo.html`), Producto (`producto.html`), Carrito (`carrito.html`), Checkout (`checkout.html`). Cambiar estado activo mediante `aria-current="page"` solo en el enlace de la vista correspondiente.

### Esqueleto de referencia (no copiar variaciones)
`header.site-header` > contenedor compartido > enlace wordmark + `nav` con enlaces de vistas + campo de búsqueda deshabilitado y label persistente; no añadir submit ni formulario sin destino funcional. El marcado concreto debe cumplir las reglas HTML y sus enlaces deben existir.

## 2. Footer canónico
- Fondo `--color-surface-muted`, texto `--color-ink`, borde superior `--color-line`; mismo ancho, espaciado y estructura en cada página.
- Columnas: Categorías (Calzado, Camisas, Pantalones, Accesorios), Legal (Términos y condiciones, Privacidad, Sobre la marca), Contacto.
- Para categorías, enlace a una sección/ancla del catálogo solo si existe y se implementa; usar ruta real. Legal/contacto están pendientes de páginas/datos reales: pueden ser texto informativo o enlaces a documentos aprobados; no usar `#` ni inventar correo/dirección/URLs. Marcarlos pendientes hasta tener destino.
- Pie incluye wordmark provisional aprobado y nota de prototipo académico si corresponde. Igual orden y texto en las cinco vistas.

## 3. Product Card
Imagen 4:5, alt contextual, nombre, precio EUR, categoría/SKU cuando la vista lo requiera, enlace a `producto.html`. CTA textual “Ver producto”. No incluir selector de talla en card. Badge solo dato confirmado; etiqueta de contenido de muestra no simula una promoción. Mismo orden/escala/estilos.

## 4. Botones
Primario borgoña de ancho/altura común, texto contraste; secundario borde grafito. Enlaces que navegan son `<a>`; acciones son `<button>`. Hover, focus-visible y disabled legibles. No usar links falsos ni afirmar acción no implementada.

## 5. Filtros
Categoría y talla usan vocabulario común. Si no funcionan, indicar “Controles de demostración: no filtran” y representarlos como ejemplos no interactivos o controles deshabilitados; nunca capturar una selección y no cambiar cards.

## 6. Inputs
Label persistente, `id`, `name`, tipo correcto, ayuda y foco visible. Placeholders solo como ejemplo, no como etiqueta. No apariencia visual idéntica con labels divergentes entre checkout y búsqueda.

## 7. Contenedor de página
`mx-auto w-full max-w-7xl px-4 sm:px-6 lg:px-8`; lectura larga `max-w-3xl`. Mismo ritmo y gutters. Contenido principal encabezado por un único h1.

## 8. Breadcrumbs
Opcionales, mismo patrón semántico `<nav aria-label="Ruta de navegación"><ol>…`; enlaces anteriores reales y página actual como texto con `aria-current="page"`. No usar en Home.

## 9. Imágenes
Proporción de card 4:5 y producto principal en proporción editorial uniforme; fuentes con permiso explícito, optimizadas para web, archivos locales en ruta acordada, sin hotlink frágil. Alt conciso y útil. Usar width/height si dimensiones conocidas, `loading="lazy"` debajo del fold, no lazy-load del hero/LCP.

## 10. Precios y promociones
Formato visual: EUR con símbolo antes y coma decimal, dos decimales: `€ 89,00`; espacio no separable recomendado entre símbolo y cifra. SKU de patrón `CAT-TIPO-NNN`: `CAM-LIN-001`, `PAN-REC-002`, `ACC-BOL-003`, `CAL-ZAP-004`. Precio anterior/descuento solo si está aprobado y se muestra precio actual claramente. No implicar oferta o stock sin dato.

## Taxonomía y tallas propuestas
- Categorías del footer obligatorias: calzado, camisas, pantalones, accesorios. Puede haber categorías de catálogo adicionales solo por aprobación.
- Tallas textiles: XS, S, M, L, XL, XXL; calzado: tallas EU 36–46 como rango de muestra sujeto a aprobación. No imponer tallas no pertinentes al producto.
- Selección editorial ficticia en español, nombres y precios de muestra para mantener consistencia (requiere aprobación, no son productos del cliente):

| SKU | Nombre | Categoría | Precio ejemplo |
|---|---|---|---:|
| `CAM-LIN-001` | Camisa de lino Atelier | Camisas | € 89,00 |
| `PAN-REC-002` | Pantalón recto Épure | Pantalones | € 120,00 |
| `ACC-BOL-003` | Bolso Le Marché | Accesorios | € 31,00 |
| `CAL-ZAP-004` | Zapato Derby Rivage | Calzado | € 145,00 |
| `CAM-POP-005` | Camisa Popeline Rue | Camisas | € 79,00 |
| `CAM-OVR-006` | Camisa oversize Ligne | Camisas | € 95,00 |
| `CAM-SAT-007` | Camisa satinada Nuit | Camisas | € 110,00 |
| `CAM-STR-008` | Camisa a rayas Côte | Camisas | € 85,00 |
| `PAN-PLI-009` | Pantalón plisado Forme | Pantalones | € 130,00 |
| `PAN-LAR-010` | Pantalón amplio Sable | Pantalones | € 115,00 |
| `PAN-DEN-011` | Jean recto Bleu | Pantalones | € 99,00 |
| `PAN-CHI-012` | Chino ligero Jardin | Pantalones | € 92,00 |
| `ACC-CEI-013` | Cinturón de cuero Ligne | Accesorios | € 65,00 |
| `ACC-FOU-014` | Pañuelo de seda Fleur | Accesorios | € 55,00 |
| `ACC-POR-015` | Cartera compacta Port | Accesorios | € 49,00 |
| `ACC-SAC-016` | Bolso bandolera Minuit | Accesorios | € 135,00 |
| `CAL-MOC-017` | Mocasín Céleste | Calzado | € 155,00 |
| `CAL-BAL-018` | Bailarina Aube | Calzado | € 125,00 |
| `CAL-BOT-019` | Bota corta Atelier | Calzado | € 189,00 |
| `CAL-SAN-020` | Sandalia Riviera | Calzado | € 105,00 |

No asumir que los materiales, origen o disponibilidad se conocen por el nombre. Los tres primeros forman el ejemplo aritmético del carrito.

## Nombres de imágenes
Formato minúsculas ASCII `sku-vista-numero.webp`, por ejemplo `cam-lin-001-frente-01.webp`, `cam-lin-001-detalle-02.webp`. Mantener imágenes locales, peso/calidad optimizados, nombres descriptivos y permiso/licencia registrado en la revisión de recursos. No incorporar dependencia de iconos.