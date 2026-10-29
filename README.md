# ATELIER — E-commerce de Moda

ATELIER es un prototipo académico de comercio electrónico para una marca francesa de moda, desarrollado de forma colaborativa en el programa **AI Engineering de 4Geeks Academy**. La propuesta explora una experiencia editorial de moda y una estructura de cinco vistas; el repositorio todavía contiene una integración parcial y no es una tienda operativa.

Los objetivos del proyecto son establecer un diseño moderno y consistente, facilitar la navegación entre vistas, adaptar la interfaz a móvil, tablet y escritorio, atender criterios de accesibilidad y SEO técnico —incluido Schema.org solo cuando corresponda— y practicar el desarrollo colaborativo con Git y GitHub.

> **Estado actual:** está integrado `catalogo.html`. `checkout.html` es una página temporal para pruebas locales, no la vista final. `index.html`, `producto.html` y `carrito.html` no están integrados. La arquitectura y el sistema visual de `memory-bank/` se registran como propuestas pendientes de aprobación.

## Tecnologías y enfoque

- **HTML5 semántico** para las páginas estáticas.
- **Tailwind CSS v4 mediante CDN de navegador**, sin proceso de compilación. El catálogo usa esta integración:

  ```html
  <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
  ```

  La página temporal de checkout no carga Tailwind. La integración común de las vistas sigue pendiente.
- **Git y GitHub** para control de versiones y colaboración; **GitHub Codespaces** como entorno posible de trabajo.
- El repositorio no contiene actualmente una hoja `styles.css` ni una implementación con React, Vue o JavaScript personalizado. No se requiere `npm install` para servir las páginas estáticas.

## Vistas: alcance previsto y estado

Las siguientes descripciones recogen el alcance documentado en `specs/`. Solo se presentan como implementadas las partes comprobables en los HTML actuales.

| Vista | Alcance previsto | Estado comprobado |
|---|---|---|
| **Home — `index.html`** | Navbar y footer compartidos, hero de campaña, nuevos lanzamientos y selección editorial de más vendidos. | **Pendiente de integración.** La especificación existe; no hay `index.html`. |
| **Catálogo — `catalogo.html`** | 20 referencias, filtros visuales de categoría y talla, cuadrícula adaptable, fotografías y enlace a una ficha de muestra. | **Integrado parcialmente.** Hay 20 tarjetas y filtros deshabilitados que se identifican como demostrativos. Solo la primera tarjeta enlaza a `producto.html`; la ficha aún no existe. El HTML referencia imágenes locales, pero su origen y permisos no están verificados. |
| **Producto — `producto.html`** | Foto principal, nombre, SKU, precio, selector de talla y cantidad, acción visual para el carrito, descripción, materiales y uso recomendado. | **Pendiente de integración.** Está especificada como ficha de muestra; no hay archivo HTML. |
| **Carrito — `carrito.html`** | Tres productos de ejemplo con miniaturas, precios, cantidades, totales por línea, subtotal, impuesto ilustrativo y total; acceso al checkout. | **Pendiente de integración.** La especificación propone un subtotal de **€240,00**, impuesto de ejemplo del 20 % (**€48,00**) y total de **€288,00**. Estos valores son ejemplos documentados, no datos de una vista integrada. |
| **Checkout — `checkout.html`** | Datos personales y de entrega, sección de pago con tarjeta solo ilustrativa y diseño adaptable. | **Existe solo como archivo temporal de pruebas.** Muestra tres secciones estáticas y advierte que no se introduzcan datos de tarjeta. No es el checkout completo especificado y actualmente enlaza a rutas que no están integradas. |

La navegación completa entre las cinco vistas no está disponible mientras falten las páginas indicadas. Las rutas y componentes compartidos se describen como propuestas en las especificaciones del proyecto.

## Limitaciones funcionales

El proyecto es una maqueta estática en HTML y Tailwind CSS. En particular:

- Los filtros de catálogo son demostrativos y no filtran productos; la búsqueda no está implementada.
- No hay carrito persistente ni operaciones reales de compra. Las cantidades, impuestos y totales previstos son ejemplos estáticos.
- No hay backend ni procesamiento de pedidos o pagos. El checkout es una representación visual; no se deben introducir datos reales de tarjeta.
- Nombres, productos y precios de muestra no acreditan un catálogo comercial real. No se pueden comprar productos mediante este prototipo.

## Sistema visual

`memory-bank/DESIGN-SYSTEM.md` define una dirección editorial cálida y minimalista, **todavía propuesta y pendiente de aprobación**. La paleta documentada es:

| Uso | Color |
|---|---|
| Marfil | `#F7F4EE` |
| Blanco | `#FFFFFF` |
| Superficie cálida | `#EEEAE2` |
| Grafito | `#242321` |
| Texto secundario | `#6B6862` |
| Bordes | `#D8D2C8` |
| Borgoña | `#6E1F32` |
| Hover borgoña | `#551727` |

La tipografía propuesta es **Georgia / Times New Roman** para títulos y **Arial / Helvetica** para textos e interfaz, utilizando fuentes locales. La especificación recomienda mantener la uniformidad mediante `AGENTS.md`, Memory Bank, reglas, vistas de `specs/` y contratos de componentes compartidos. No existe todavía una hoja CSS común implementada.

## Diseño adaptable, semántica y SEO

Las reglas y especificaciones plantean un enfoque **mobile-first**, con utilidades responsive de Tailwind para adaptar navegación, rejillas, imágenes y formularios entre móvil, tablet y escritorio. Los anchos de referencia para futuras comprobaciones son 320, 375, 768, 1024 y 1440 px. No se afirma que esas pruebas se hayan realizado.

Las reglas del proyecto solicitan HTML semántico, jerarquía coherente de encabezados, `title` y `description` por página, textos alternativos para imágenes, etiquetas asociadas a campos, navegación por teclado y foco visible. El catálogo actual incluye metadatos, textos `alt`, etiquetas de formulario y estados de foco en sus clases; esto no equivale a una auditoría completa de accesibilidad. `checkout.html` contiene metadatos básicos, pero es temporal. **No se encontró marcado Schema.org/JSON-LD en los HTML inspeccionados**, y no se han registrado validaciones W3C ni puntuaciones Lighthouse.

## Estructura actual del repositorio

Árbol resumido de archivos versionados relevantes; se omiten recursos temporales o locales ignorados:

```text
.
├── AGENTS.md
├── README.md
├── catalogo.html
├── checkout.html                 # temporal; no es la vista final
├── server.py                     # servidor Flask de la plantilla original
├── learn.json                    # metadatos de la plantilla original
├── assets/
│   └── catalog/
│       ├── *.jpg                 # 20 imágenes; procedencia/licencias sin verificar
│       └── SOURCES.md            # registro disponible de procedencia
├── .agents/
│   └── rules/
│       ├── git-collaboration.md
│       ├── html-semantics.md
│       ├── responsive-accessibility.md
│       ├── seo-schema.md
│       └── tailwind-design.md
├── memory-bank/
│   ├── CONTEXT.md
│   ├── DECISIONS.md
│   ├── DESIGN-SYSTEM.md
│   ├── PROGRESS.md
│   └── PROJECT.md
└── specs/
    ├── 01-home.md
    ├── 02-catalogo.md
    ├── 03-producto.md
    ├── 04-carrito.md
    ├── 05-checkout.md
    ├── collaboration-workflow.md
    ├── quality-acceptance.md
    └── shared-components.md
```

No se muestran `index.html`, `producto.html` ni `carrito.html` porque no existen actualmente en la raíz.

## Instalación y ejecución local

No hay paso de compilación para las páginas estáticas. Para probar el contenido actual:

1. Clona el repositorio y abre la carpeta en VS Code o GitHub Codespaces:

   ```bash
   git clone <URL-del-repositorio>
   cd Equipo-Carrillo-Rengifo
   ```

2. Inicia un servidor HTTP desde el directorio que contiene los HTML:

   ```bash
   python3 -m http.server 8000
   ```

3. Abre `http://localhost:8000/catalogo.html` para ver el catálogo actual o `http://localhost:8000/checkout.html` para la página temporal.
4. Cuando Home, Producto y Carrito estén integrados, se podrá abrir `index.html` y probar el recorrido completo de las cinco vistas.

La integración CDN de Tailwind requiere conexión a internet. El `server.py` heredado de la plantilla utiliza Flask, pero no es necesario para el servidor estático recomendado arriba.

## Desarrollo colaborativo

La distribución indicada para el proyecto es:

- **Desarrollador 1 — Joaquín Rengifo:** catálogo, vista de producto y carrito.
- **Desarrolladora 2 — integrante del equipo:** Home y Checkout. Su nombre no está consignado en la documentación disponible.

El flujo documentado contempla ramas `feature` por vista, commits descriptivos, push frecuente, Pull Requests hacia `main`, revisión e integración de cambios y resolución colaborativa de conflictos. Es el flujo de trabajo descrito, no una afirmación de que las PR ya estén aprobadas o fusionadas.

## Pruebas y validación

La validación completa está **pendiente**. Las herramientas y comprobaciones previstas son:

- **W3C Nu Validator:** validar cada documento HTML.
- **Schema Markup Validator:** revisar JSON-LD únicamente en páginas donde se incorpore.
- **Lighthouse** y **PageSpeed Insights:** registrar resultados medidos y fecha.
- **Pruebas responsive:** revisar los anchos de referencia indicados y detectar desbordamiento o recortes.
- **Comprobación de enlaces** internos y **verificación de imágenes** y sus rutas.

El criterio del proyecto exige un rendimiento mínimo de **80 puntos en PageSpeed Insights** y recomienda superar 90; se adjunta una captura `pagespeed-result.png` en los recursos verificados.

**Evidencia PageSpeed Insights:** `pagespeed-result.png`.

## Recursos fotográficos

`assets/catalog/` contiene 20 fotografías JPG asociadas por nombre a referencias del catálogo. `assets/catalog/SOURCES.md` indica que no dispone de información comprobada sobre fuente original, autoría, titularidad, licencias ni condiciones de uso. Por tanto, **el uso autorizado de estas imágenes está pendiente de revisión**; su presencia en el repositorio no constituye verificación de derechos.

## Autores y contexto académico

- **Proyecto:** ATELIER — E-commerce de Moda.
- **Institución:** 4Geeks Academy.
- **Programa:** AI Engineering.
- **Modalidad:** proyecto colaborativo.
- **Desarrolladores:**
  Joaquín Rengifo - integrante del equipo responsable de Catálogo, vista de producto, carrito.
  Carla Carrillo -  integrante del equipo responsable de Home y Checkout.




