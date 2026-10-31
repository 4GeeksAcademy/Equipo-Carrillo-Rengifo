# ATELIER — E-commerce de Moda

ATELIER es un prototipo académico de comercio electrónico para una marca francesa de moda, desarrollado de forma colaborativa en el programa **AI Engineering de 4Geeks Academy**. La propuesta explora una experiencia editorial de moda en cinco vistas HTML; no es una tienda operativa.

Los objetivos del proyecto son establecer un diseño moderno y consistente, facilitar la navegación entre vistas, adaptar la interfaz a móvil, tablet y escritorio, atender criterios de accesibilidad y SEO técnico —incluido Schema.org solo cuando corresponda— y practicar el desarrollo colaborativo con Git y GitHub.

> **Estado actual:** `index.html`, `catalogo.html`, `producto.html`, `carrito.html` y `checkout.html` están presentes en `main` tras integrar la Home (PR #6). Las cinco vistas y la navegación estática existen; esto no significa que todas las pruebas de aceptación se hayan ejecutado ni que los datos de ejemplo o derechos de imágenes estén aprobados. El sistema visual conceptual se aprobó para el prototipo; la identidad corporativa sigue sin confirmarse.

## Tecnologías y enfoque

- **HTML5 semántico** para las páginas estáticas.
- **Tailwind CSS v4 mediante CDN de navegador**, sin proceso de compilación. Las páginas usan esta integración:

  ```html
  <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
  ```

   Las vistas usan utilidades Tailwind y referencias a tokens `--color-*`; no existe una hoja `styles.css` común. No se ha verificado en esta actualización la apariencia de cada vista en navegador.
- **Git y GitHub** para control de versiones y colaboración; **GitHub Codespaces** como entorno posible de trabajo.
- El repositorio no contiene actualmente una hoja `styles.css` ni una implementación con React, Vue o JavaScript personalizado. No se requiere `npm install` para servir las páginas estáticas.

## Vistas: alcance previsto y estado

Las siguientes descripciones recogen el alcance documentado en `specs/`. Solo se presentan como implementadas las partes comprobables en los HTML actuales.

| Vista | Alcance previsto | Estado comprobado |
|---|---|---|
| **Home — `index.html`** | Hero editorial, lanzamientos, selección de muestra y navegación compartida. | **Integrada en `main` (PR #6).** Es contenido estático; la identidad y los productos son provisionales/de muestra. |
| **Catálogo — `catalogo.html`** | 20 referencias, filtros de demostración y cuadrícula adaptable. | **Integrado en `main`.** Los controles no filtran. Referencia imágenes locales cuyo origen y permisos no están verificados. |
| **Producto — `producto.html`** | Ficha de producto de muestra, atributos y controles visuales. | **Integrada en `main`.** No añade al carrito ni realiza operaciones. |
| **Carrito — `carrito.html`** | Tres productos de ejemplo, importes estáticos y acceso al checkout. | **Integrado en `main`.** Subtotal de muestra **€240,00**, impuesto ilustrativo **€48,00** y total **€288,00**; no es una orden real ni cálculo dinámico. |
| **Checkout — `checkout.html`** | Tres pasos visuales, campos de muestra y nota de prototipo. | **Integrado en `main` como checkout estático.** No procesa pagos ni debe recibir datos reales de tarjeta. |

Las cinco vistas tienen navegación HTML estática. La presencia de los destinos no demuestra por sí sola que cada enlace, ancla o flujo haya pasado una comprobación integral. Las especificaciones siguen siendo referencia de alcance y aceptación; no se deben interpretar sus casillas sin marcar como validaciones completadas.

## Limitaciones funcionales

El proyecto es una maqueta estática en HTML y Tailwind CSS. En particular:

- Los filtros de catálogo son demostrativos y no filtran productos; la búsqueda no está implementada.
- No hay carrito persistente ni operaciones reales de compra. Las cantidades, impuestos y totales previstos son ejemplos estáticos.
- No hay backend ni procesamiento de pedidos o pagos. El checkout es una representación visual; no se deben introducir datos reales de tarjeta.
- Nombres, productos y precios de muestra no acreditan un catálogo comercial real. No se pueden comprar productos mediante este prototipo.

## Sistema visual

`memory-bank/DESIGN-SYSTEM.md` documenta la dirección editorial cálida y minimalista **aprobada para este prototipo**; no es una identidad corporativa confirmada. La paleta documentada es:

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

La tipografía definida para el prototipo es **Georgia / Times New Roman** para títulos y **Arial / Helvetica** para textos e interfaz, utilizando fuentes locales. El HTML usa clases Tailwind que consumen variables CSS `--color-*`; no se encontró una hoja CSS común que defina esos tokens. Este hecho técnico no altera el requisito de utilizar Tailwind CSS de manera coherente, con clases utility y breakpoints responsive, ni implica que se deba crear `styles.css` en esta actualización documental.

## Diseño adaptable, semántica y SEO

Las reglas y especificaciones plantean un enfoque **mobile-first**, con utilidades responsive de Tailwind para adaptar navegación, rejillas, imágenes y formularios entre móvil, tablet y escritorio. Los anchos de referencia para futuras comprobaciones son 320, 375, 768, 1024 y 1440 px. No se afirma que esas pruebas se hayan realizado.

Las reglas del proyecto solicitan HTML semántico, jerarquía coherente de encabezados, `title` y `description` por página, textos alternativos para imágenes, etiquetas asociadas a campos, navegación por teclado y foco visible. La existencia de estas características en el código no equivale a una auditoría completa de accesibilidad. **No se ha registrado evidencia de validación W3C, auditoría completa de teclado/responsive ni puntuaciones Lighthouse/PSI en esta actualización.** No se encontró marcado Schema.org/JSON-LD en los HTML inspeccionados.

## Estructura actual del repositorio

Árbol resumido de archivos versionados relevantes; se omiten recursos temporales o locales ignorados:

```text
.
├── AGENTS.md
├── README.md
├── index.html                    # Home
├── catalogo.html
├── producto.html
├── carrito.html
├── checkout.html                 # prototipo estático
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

Las cinco páginas HTML están en la raíz y versionadas.

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

3. Abre `http://localhost:8000/index.html` para Home o `http://localhost:8000/catalogo.html` para el catálogo. También están disponibles `producto.html`, `carrito.html` y el checkout estático `checkout.html`.
4. Recorre los enlaces para una comprobación manual inicial; esta instrucción no constituye evidencia de pruebas ya realizadas.

La integración CDN de Tailwind requiere conexión a internet. El `server.py` heredado de la plantilla utiliza Flask, pero no es necesario para el servidor estático recomendado arriba.

## Desarrollo colaborativo

La distribución registrada para el proyecto es:

- **Desarrollador 1 — Joaquín Rengifo:** catálogo, vista de producto y carrito.
- **Desarrolladora 2 — integrante del equipo:** Home y Checkout. Su nombre no está consignado en la documentación disponible.

El flujo documentado contempla ramas `feature` por vista, commits descriptivos, push frecuente, Pull Requests hacia `main`, revisión e integración de cambios y resolución colaborativa de conflictos. Es el flujo de trabajo descrito, no una afirmación de que las PR ya estén aprobadas o fusionadas.

## Pruebas y validación

La validación completa está **pendiente de evidencia registrada**. Las herramientas y comprobaciones previstas son:

- **W3C Nu Validator:** validar cada documento HTML.
- **Schema Markup Validator:** revisar JSON-LD únicamente en páginas donde se incorpore.
- **Lighthouse** y **PageSpeed Insights:** registrar resultados medidos y fecha.
- **Pruebas responsive:** revisar los anchos de referencia indicados y detectar desbordamiento o recortes.
- **Comprobación de enlaces** internos y **verificación de imágenes** y sus rutas.

El criterio del proyecto exige un rendimiento mínimo de **80 puntos en PageSpeed Insights** y recomienda superar 90; se adjunta una captura `pagespeed-result.png` en los recursos verificados.

**Evidencia PageSpeed Insights:** revisar `/pagespeed-insights`; no declarar puntuación hasta localizar y verificar un informe con URL y fecha.

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




