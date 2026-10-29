# Sistema de diseño propuesto

> Estado: propuesta para aprobar antes del desarrollo paralelo. No constituye identidad oficial del cliente.

## Dirección visual
E-commerce editorial premium: fondos cálidos, grafito para lectura, borgoña como acento limitado, composición sobria y fotografía de moda consistente. No asignar una paleta distinta a cada vista.

## Tokens principales
| Token | Valor | Aplicación |
|---|---|---|
| `--color-canvas` | `#F7F4EE` | Fondo global marfil |
| `--color-surface` | `#FFFFFF` | Cards, inputs y superficies claras |
| `--color-surface-muted` | `#EEEAE2` | Secciones alternas y controles secundarios |
| `--color-ink` | `#242321` | Texto principal y navegación |
| `--color-ink-muted` | `#6B6862` | Texto secundario, metadatos |
| `--color-line` | `#D8D2C8` | Bordes y divisores |
| `--color-accent` | `#6E1F32` | Borgoña: CTA, foco/acento y enlaces destacados |
| `--color-accent-hover` | `#551727` | Estado hover/activo del CTA |
| `--color-on-accent` | `#FFFFFF` | Texto/icono sobre borgoña |
| `--color-sale` | `#8A2D2D` | Etiqueta de rebaja solo si el dato existe |
| `--color-success` | `#315B45` | Confirmación visual no transaccional |
| `--color-error` | `#A12D2D` | Errores de formulario |

Estos valores deben revisarse con una herramienta de contraste sobre combinaciones reales antes de aprobarse. No son garantía automática de conformidad.

## Fuente de verdad y carga
Método compatible con la plantilla actual: CDN oficial `@tailwindcss/browser@4` descrito en `README.es.md` y una sola hoja común `styles.css` con las variables CSS de este documento y solo las reglas globales estrictamente necesarias. Las páginas enlazan esa misma hoja; sus clases Tailwind consumen variables (por ejemplo `bg-[var(--color-canvas)]`, `text-[var(--color-ink)]`, `border-[var(--color-line)]`). No repetir hexadecimales en HTML ni crear paletas locales. Comprobar el comportamiento de compilación de utilidades variables en el navegador con CDN en una prueba técnica previa. No introducir `@theme`/build tooling sin validar compatibilidad y aprobación.

## Tipografía
- Titulares editoriales: `Georgia, 'Times New Roman', serif` (`font-serif`), peso regular; alternativa local, sin descarga externa.
- Interfaz y cuerpo: `Arial, Helvetica, sans-serif` (`font-sans`), peso normal/medio.
- Evitar fuentes remotas hasta acordar rendimiento/licencia. Uso global común, no tipografía distinta por página.

## Jerarquía, espaciado y geometría
- H1: 36–56 px responsive, serif, leading compacto; H2: 28–40 px; H3: 20–24 px. Cuerpo 16 px; metadatos 12–14 px. Contraste y tamaño prevalecen sobre lo ornamental.
- Escala sugerida: 4, 8, 12, 16, 24, 32, 48, 64, 96 px; usar escala Tailwind y espacio amplio en desktop.
- Contenedor central: `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`; ancho de lectura prolongada `max-w-3xl`.
- Radio: 0–4 px para controles sobrios, 0 para imágenes; no usar grandes cápsulas salvo indicador pequeño justificado.
- Bordes 1 px color `--color-line`; sombras discretas y solo para elevación necesaria, sin sombras decorativas fuertes.

## Clases Tailwind de referencia
| Uso | Referencia de clase |
|---|---|
| Fondo global | `bg-[var(--color-canvas)]` |
| Sección alterna | `bg-[var(--color-surface-muted)]` |
| Texto principal/secundario | `text-[var(--color-ink)]` / `text-[var(--color-ink-muted)]` |
| Acento | `text-[var(--color-accent)]` |
| Botón primario | `bg-[var(--color-accent)] text-[var(--color-on-accent)] hover:bg-[var(--color-accent-hover)] focus-visible:outline-2` más padding común |
| Botón secundario | `border border-[var(--color-ink)] text-[var(--color-ink)] hover:bg-[var(--color-surface-muted)]` |
| Input | `w-full border border-[var(--color-line)] bg-[var(--color-surface)] text-[var(--color-ink)] focus-visible:outline-2` |
| Card | `bg-[var(--color-surface)] text-[var(--color-ink)]` con borde opcional |
| Contenedor | `mx-auto w-full max-w-7xl px-4 sm:px-6 lg:px-8` |
| Navbar/Footer | composición contractual de `specs/shared-components.md` con fondo canvas, texto ink y divisor line |
| H1 / H2 / H3 | `font-serif text-[var(--color-ink)]` + escala responsive aprobada |

Las utilidades comunes se combinan con escala estándar de Tailwind. Documentar una composición canónica por componente en `shared-components.md`; las páginas no deben desarrollar variantes.

## Componentes visuales
- Botones: altura/touch target cómoda, texto explícito, estados hover/focus/disabled visibles; primario borgoña y secundario contorneado.
- Inputs: label persistente, altura común, borde cálido, foco visible. No usar placeholder como etiqueta.
- Product card: fotografía 4:5 consistente, título, variante/color solo si confirmado, precio EUR; badge solo para atributo demostrado.
- Badges: cápsula discreta, texto legible, nunca comunicar estado únicamente por color.
- Iconos: preferir texto o símbolos simples accesibles; si se usan pictogramas, decorativos ocultos al lector o con nombre accesible. No sumar librería.
- Imágenes: uso permitido, optimizadas, proporción coherente, `width`/`height` cuando se conozcan, `object-cover`; alt descriptivo o vacío si decorativa.

## Estados y breakpoints
Estados visuales: default, hover, focus-visible, active y disabled; no implican funcionalidad. Mobile-first con breakpoints estándar Tailwind (`sm` 640, `md` 768, `lg` 1024, `xl` 1280, `2xl` 1536 px); verificar también 320, 375, 768, 1024 y 1440 px. No crear breakpoint a medida sin acuerdo.

## Fondos, navbar y footer
Canvas en el sitio completo; superficie blanca en cards; muted en bloques alternos cuando ayude a segmentar. Navbar/footer siguen exactamente las especificaciones compartidas, no variantes por ruta.