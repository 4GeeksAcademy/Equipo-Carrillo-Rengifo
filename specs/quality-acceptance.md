# Calidad y aceptación del proyecto

> Criterios derivados del encargo/rúbrica indicada. Las cinco páginas están integradas en `main`; ninguna comprobación de aceptación se declara realizada hasta registrar evidencia verificable.

## Aceptación funcional y técnica
- [ ] Revisar que las cinco vistas integradas (`index.html`, `catalogo.html`, `producto.html`, `carrito.html`, `checkout.html`) estén completas y enlazadas correctamente.
- [ ] HTML5 semántico sin errores en W3C Nu Validator; un h1, metadatos, labels/alt y rutas coherentes.
- [ ] Tailwind CSS v4 exclusivamente; estilos y tokens compartidos; sin framework ni JavaScript personalizado/dependencias prohibidas.
- [ ] Navbar/footer uniformes; copy, rutas, cards, SKU, precio y componentes conforme a `shared-components.md`.
- [ ] Catálogo de veinte referencias; carrito de tres productos y aritmética verificada; checkout estático sin datos de tarjeta reales.
- [ ] Responsive en móvil/tablet/escritorio, probado a 320, 375, 768, 1024 y 1440 px; sin scroll horizontal accidental.
- [ ] Navegación teclado, foco, contraste, zoom y controles accesibles revisados manualmente.
- [ ] Schema Markup Validator sin errores para JSON-LD utilizado y solo con información válida.
- [ ] Enlaces internos funcionales, sin rutas ficticias ni `href="#"`.
- [ ] Flujo Git por ramas, PR revisadas; no desarrollo en main.

## SEO y datos estructurados
- Title único y meta description por vista; idioma es, viewport, texto indexable, encabezados y alt.
- `Organization` solamente con identidad/datos confirmados; `Product` para producto individual con datos visibles; `Offer` únicamente con precio/disponibilidad acordados.
- No inventar ratings, reviews, address, domain, redes, stock, promociones ni resultados de Google.
- Validator comprueba sintaxis, no garantiza rich results.

## Herramientas y registro de evidencia
1. **W3C Nu Validator:** cada HTML y revisión del sitio integrado; registrar URLs/archivos y errores corregidos.
2. **Schema Markup Validator:** JSON-LD real, por página; no evaluar ejemplos con placeholders como datos oficiales.
3. **Lighthouse:** registrar auditoría local, navegador, dispositivo/perfil, fecha y métricas relevantes.
4. **PageSpeed Insights:** evaluar URL accesible y guardar captura llamada exactamente `pagespeed-result.png` en el repositorio. Si el sitio no está desplegado, documentar el bloqueo; no inventar score.
5. **Prueba manual responsive:** 320, 375, 768, 1024, 1440 px; comprobar overflow, imágenes, rejillas y formulario.
6. **Prueba manual teclado:** Tab/Shift+Tab, foco visible, enlaces/controles, orden y zoom.

## Rendimiento
PageSpeed Insights: mínimo de aceptación **80 puntos** de rendimiento; objetivo recomendado **90 o más**. No son resultados presentes ni garantizados. Optimizar imágenes, evitar scripts adicionales/fuentes remotas y lazy-load debajo del fold; no lazy-load del hero principal. Registrar mediciones reales y captura.

## Entrega
PR de cada rama con alcance, capturas cuando haya UI, pruebas ejecutadas/pendientes, riesgos, y confirmación de que no altera datos o trabajo ajeno. Tras integrar las cinco, repetir validación completa del sitio.