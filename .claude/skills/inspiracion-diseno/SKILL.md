---
name: inspiracion-diseno
description: Busca ejemplos de referencia para inspirarse al diseñar una app (móvil o escritorio) o una web, y guarda una selección organizada en un archivo Markdown del repositorio. Usar cuando el usuario pida inspiración, ejemplos, referencias o ideas para diseñar una app, una web, una landing, una pantalla o un flujo, o diga cosas como "busca ejemplos de", "quiero inspirarme", "moodboard", "referencias visuales".
---

# Inspiración de diseño (apps y webs)

Objetivo: reunir de 6 a 12 ejemplos reales, bien elegidos y explicados, para que el usuario tome decisiones de diseño con evidencia. Es referencia visual, no un plan de copia: nunca copiar assets, logos o textos de los sitios.

## 1. Entender el brief

Antes de buscar, confirmar (sin preguntar de más, usar valores razonables si no se indican):

- **Tipo**: app (móvil, escritorio o web app) o web (landing, sitio corporativo, portfolio, tienda, etc.).
- **Producto y público**: qué hace y para quién.
- **Tono**: sobrio, lúdico, premium, técnico, cálido, etc.
- **Restricciones**: marca existente, colores, idioma, modo claro u oscuro.

Si el usuario no indica el tipo, asumir "web" para una landing y "app" para algo con login o flujos.

## 2. Fuentes a consultar

Elegir según el tipo. Consultar varias en paralelo cuando sea posible.

**Apps (móvil y escritorio):**
- Dribbble (`dribbble.com`): muy visual, buena para pantallas sueltas y estilos.
- Mobbin (`mobbin.com`): flujos reales de apps (onboarding, pagos, ajustes). Lo mejor para ver cómo se conectan las pantallas. Parte del contenido requiere cuenta.
- Behance (`behance.net`): proyectos completos con proceso de diseño.

**Webs:**
- A1 Gallery (`a1.gallery`): sitios reales con capturas y medidas tomadas de la página en vivo (colores, tipografías, tamaños, espaciado). Es la primera opción para webs si sus herramientas `mcp__a1__*` están disponibles. No cubre apps.
- Awwwards (`awwwards.com`): webs premiadas, más experimentales.
- Land-book (`land-book.com`): landing pages organizadas por sección (hero, precios, FAQ).
- Godly (`godly.website`): webs con diseño cuidado y bien curadas.
- Dribbble y Behance también sirven para web.

Si el usuario pide fuentes concretas, usar esas. Si no, usar 2 o 3 del grupo que corresponda.

## 3. Cómo buscar

**Con A1 Gallery (webs):** si las herramientas `mcp__a1__*` no aparecen cargadas, buscarlas primero con ToolSearch (`a1 gallery`).
- `search_websites` con consultas cortas (1 a 3 palabras o términos de estilo, por ejemplo `dark`, `fintech`, `big-type`). Consultas largas devuelven poco. Usar `mode: "discovery"` cuando el brief sea un estilo y `relevance` cuando sea algo concreto. Si la respuesta trae `broadenedSearch`, decirlo al usuario: los resultados son más amplios de lo pedido.
- `browse_websites` con `styleSlugs` o `typeSlug` para filtrar por estilo o tipo de sitio (`get_design_filters` muestra los valores válidos).
- `search_sections` para ver secciones concretas (hero, precios, FAQ) con sus tokens medidos, y `analyze_design_tokens` para comparar tamaños, espaciado y paleta de un tipo de sección con la media de sitios reales.
- No hace falta `get_website` por cada resultado: los resultados ya traen url, captura, estilos, colores y tipos. Mostrar la captura que devuelve A1, no imágenes de otra fuente.

**Con otras fuentes (apps y webs sin A1):**

- Usar `WebSearch` con consultas tipo `site:dribbble.com <tipo de producto> <estilo>`, por ejemplo `site:dribbble.com fintech app dashboard dark`.
- Usar `WebFetch` solo sobre páginas concretas que se quieran describir. Muchos de estos sitios bloquean el acceso automatizado o requieren cuenta: si una página no se puede leer, decirlo en el resultado y no inventar detalles.
- Preferir ejemplos recientes (últimos 2 o 3 años) salvo que el estilo buscado sea clásico.
- Variar: no devolver 6 ejemplos del mismo estilo. Incluir al menos un ejemplo "seguro" y uno más arriesgado.

## 4. Qué anotar por ejemplo

Para cada ejemplo, solo lo que se pueda verificar en la página:

- **Nombre y enlace** (el enlace directo a la pieza, con la fuente).
- **Qué es**: app o web, sector, pantalla o sección concreta.
- **Qué aporta**: una o dos frases sobre lo que sirve como inspiración (jerarquía, uso del color, navegación, microcopy, espaciado, tipografía).
- **Paleta y tipografía**: si viene de A1, usar los valores medidos (hex con su rol y nombres de fuentes). En otras fuentes, usar valores aproximados (por ejemplo "fondo oscuro, acento naranja, sans serif geométrica") y no afirmar hex exactos.
- **Qué no copiar**: un aspecto que sea específico de esa marca o que no encaje con el brief.

Al final, resumir patrones que se repiten en los ejemplos (2 a 4 puntos) y una recomendación concreta para el brief del usuario.

## 5. Dónde guardar el resultado

Guardar siempre el resultado en un archivo Markdown dentro del repositorio, en la carpeta `inspiracion/`, con este nombre:

`inspiracion/<tema-en-kebab-case>-<AAAA-MM-DD>.md`

Por ejemplo: `inspiracion/app-finanzas-personales-2026-10-30.md`.

Estructura del archivo:

```markdown
# Inspiración: <tema>

**Brief:** <una o dos frases>
**Tipo:** app | web
**Fuentes consultadas:** <lista; indicar si A1 Gallery se usó>
**Fecha:** <AAAA-MM-DD>

## Ejemplos

### 1. <Nombre> — <fuente>
- Enlace: <url>
- Qué es: ...
- Qué aporta: ...
- Paleta y tipografía: ...
- Qué no copiar: ...

(repetir)

## Patrones comunes
- ...

## Recomendación para este brief
- ...

## Límites de esta búsqueda
- Páginas que no se pudieron leer, y por qué.
- Si A1 no estaba disponible para una búsqueda web, indicarlo aquí.
```

No crear Notion ni otros servicios externos salvo que el usuario lo pida: consumen más contexto y el archivo es suficiente.

## 6. Al terminar

1. Confirmar la ruta del archivo creado.
2. Dar un resumen de 3 a 5 líneas en el chat: los ejemplos más útiles y la recomendación principal.
3. Si el trabajo es para el repositorio, hacer commit en la rama de trabajo. No abrir pull request salvo que el usuario lo pida.
