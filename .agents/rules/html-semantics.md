# Regla: HTML semántico

- Cada documento debe usar `<!doctype html>`, `<html lang="es">`, charset UTF-8, meta viewport y una estructura válida.
- Usa `header`, `nav`, `main`, `section`, `article` y `footer` según su significado; no elijas elementos solo por apariencia.
- Debe existir un único `h1` que describa la vista. Mantén la jerarquía de encabezados sin saltos arbitrarios.
- Los formularios deben tener `label` asociado mediante `for`/`id`, `name` y tipos adecuados; agrupa campos relacionados con `fieldset`/`legend` cuando aplique.
- Cada imagen informativa necesita `alt` breve y contextual; las decorativas usan `alt=""`. No repitas en alt el texto adyacente.
- Usa enlaces `<a>` para navegación con rutas reales y coherentes; botones para acciones. Evita `href="#"` y controles falsos.
- Asegura nombres accesibles para controles iconográficos y enlaces ambiguos; no dependas solo del color.
- El HTML resultante debe pasar Nu Validator sin errores. No agregues atributos/eventos JavaScript.