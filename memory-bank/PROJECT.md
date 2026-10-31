# Proyecto

> Estado: cinco vistas integradas en `main`. Dirección visual aprobada para el prototipo; identidad comercial, permisos de imágenes y validación integral conservan estados independientes. Actualizado: 2026-10-31.

## Objetivo
Mantener un prototipo estático y navegable de e-commerce de moda para el ejercicio colaborativo de 4Geeks Academy — AI Engineering.

## Contexto del cliente
El briefing describe una marca reconocida de ropa con sede en Francia, pero no da nombre, dominio, identidad oficial ni datos corporativos. La dirección visual conceptual premium/editorial aprobada para el prototipo no es una afirmación sobre la marca real.

## Alcance académico
Cinco vistas HTML estáticas —Home, Catálogo, Producto, Carrito y Checkout— integradas en `main`. El flujo es una demostración visual navegable, no una tienda operativa.

## Requisitos técnicos
- HTML5 semántico y Tailwind CSS v4 mediante CDN de navegador, con clases utility coherentes y responsive.
- Git/GitHub para trabajo por ramas y PR. No se establece una hoja `styles.css` como requisito.
- No React/Vue/Angular/Next/Bootstrap/jQuery/TypeScript, JavaScript personalizado, backend, APIs, pasarelas reales ni dependencias contradictorias.
- Checkout, filtros, búsqueda y carrito son estáticos: no filtran, calculan, persisten, procesan ni envían operaciones reales.

## Vistas obligatorias
1. Home: campaña, lanzamientos y más vendidos.
2. Catálogo: filtros visuales y referencia de 20 productos.
3. Producto: galería/detalles y opción de talla/cantidad estática.
4. Carrito: tres ejemplos y totales coherentes pero no dinámicos.
5. Checkout: tres pasos visuales, sin solicitar ni almacenar tarjetas reales.

## Entregables
- Cinco documentos HTML presentes e integrados. La presencia no implica que todas las comprobaciones de aceptación se hayan realizado.
- Navbar y footer consistentes, catálogo de referencia compartido y tokens de diseño únicos.
- Metadatos SEO y JSON-LD prudente donde aplique.
- Evidencia de validación HTML/schema, pruebas responsive/teclado, Lighthouse/PageSpeed y `pagespeed-result.png` en la fase de implementación.
- Ramas y PR revisadas; documentación actualizada.

## Criterios de éxito
Cumplir `specs/quality-acceptance.md`: HTML válido, semántica, uso de Tailwind v4, cinco vistas completas, consistencia, enlaces funcionales, responsive, accesibilidad, Schema.org válido donde proceda y proceso colaborativo. Objetivo de rendimiento PageSpeed Insights: mínimo 80, ideal 90+; no hay mediciones todavía.