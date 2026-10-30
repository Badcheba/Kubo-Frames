---
name: inspiracion-diseno
description: Busca ejemplos de referencia para diseñar una app (móvil o escritorio) o una web, y guarda una selección con análisis en un archivo Markdown dentro de la carpeta inspiracion/ del repositorio. Usar cuando el usuario pida inspiración, ejemplos, referencias, ideas o moodboard para una app, web, landing, pantalla, flujo o sección, o diga cosas como "busca ejemplos de", "quiero inspirarme", "referencias visuales", "cómo debería verse".
---

# Inspiración de diseño (apps y webs)

Objetivo: reunir de 6 a 12 ejemplos reales, elegidos y explicados, para que la persona decida con evidencia. Es referencia visual, no un plan de copia: nunca copiar assets, logos ni textos de los sitios.

Flujo: entender el brief → elegir fuentes con la persona → buscar → anotar → guardar → resumir.

## 1. Entender el brief

Confirmar solo lo que falte y sea necesario:

- **Tipo**: app (móvil, escritorio o web app) o web (landing, corporativa, portfolio, tienda).
- **Producto y público**: qué hace y para quién.
- **Tono**: sobrio, lúdico, premium, técnico, cálido, etc.
- **Restricciones**: marca existente, colores, idioma, modo claro u oscuro.

Si no se indica el tipo: "web" para una landing o un sitio informativo, "app" para algo con login o flujos. Si el brief ya es claro, no preguntar nada más.

## 2. Elegir fuentes con la persona

Antes de buscar, preguntar con `AskUserQuestion` (selección múltiple) qué fuentes quiere. Así no se gastan tokens en fuentes que no interesan. Poner primero la opción recomendada, con "(Recomendado)".

| Tipo | Fuentes | Para qué sirven |
|---|---|---|
| Web | **A1 Gallery** | Sitios reales con capturas y medidas tomadas de la página en vivo (colores, tipografías, tamaños, espaciado). Recomendada para webs. |
| Web | Land-book | Landing pages separadas por sección (hero, precios, FAQ). |
| Web | Awwwards | Webs premiadas, más experimentales. |
| Web | Godly | Webs con diseño cuidado y bien curado. |
| App | Mobbin | Flujos reales (onboarding, pagos, ajustes). Parte del contenido requiere cuenta. |
| App | Dribbble | Pantallas sueltas y estilos visuales muy variados. |
| App | Behance | Proyectos completos con proceso de diseño. |

Dribbble y Behance también sirven para web. Si la persona responde "decide tú" o no contesta, elegir 2 o 3 según el tipo y dejarlo indicado en el archivo. Si pide fuentes concretas, usar esas.

## 3. Buscar

### Con A1 Gallery

1. Si las herramientas `mcp__a1__*` no están cargadas, cargarlas con ToolSearch (`select:mcp__a1__search_websites,mcp__a1__browse_websites,mcp__a1__search_sections,mcp__a1__analyze_design_tokens`). Si no están disponibles, seguir con las otras fuentes y anotarlo en los límites.
2. `search_websites` con consultas cortas: 1 a 3 palabras o términos de estilo (`dark`, `fintech`, `big-type`). Las consultas largas devuelven poco. Usar `mode: "discovery"` si el brief es un estilo o una sensación, y `relevance` si es algo concreto.
3. Si la respuesta trae `broadenedSearch`, decirlo: los resultados son más amplios de lo pedido.
4. `browse_websites` con `styleSlugs` o `typeSlug` para filtrar. `get_design_filters` lista los valores válidos.
5. `search_sections` para ver secciones concretas (hero, precios, FAQ) con sus tokens medidos. `analyze_design_tokens` sirve para comparar tamaños, espaciado y paleta de un tipo de sección con la media de sitios reales.
6. No llamar `get_website` por cada resultado: ya traen url, captura, estilos, colores y tipos. Mostrar la captura que devuelve A1.

### Con otras fuentes

- `WebSearch` con `site:` y términos del brief, por ejemplo `site:mobbin.com onboarding fintech` o `site:dribbble.com dashboard app dark`.
- `WebFetch` solo sobre páginas concretas que valga la pena describir. Muchos de estos sitios bloquean la lectura automática o piden cuenta: si una página no se puede leer, decirlo y no inventar detalles.
- Preferir trabajos recientes (últimos 2 o 3 años), salvo que el estilo buscado sea clásico.

### Criterios de selección

- Variar: no devolver 6 ejemplos del mismo estilo. Incluir al menos uno "seguro" y uno más arriesgado.
- Cuidar el número de llamadas: con 6 a 8 resultados alcanza para la mayoría de los briefs.

## 4. Anotar cada ejemplo

Solo lo que se pueda verificar en la página o en los datos de la búsqueda:

- **Nombre y enlace**: el enlace directo a la pieza, con su fuente.
- **Qué es**: app o web, sector, pantalla o sección concreta.
- **Qué aporta**: una o dos frases sobre lo que sirve como inspiración (jerarquía, color, navegación, microcopy, espaciado, tipografía).
- **Paleta y tipografía**: si vienen de A1, usar los valores medidos (hex con su rol y nombres de fuentes). En otras fuentes, usar descripciones aproximadas ("fondo oscuro, acento naranja, sans serif geométrica") y no afirmar hex exactos.
- **Qué no copiar**: lo que sea específico de la marca o no encaje con el brief.

Al final, incluir 2 a 4 patrones que se repiten y una recomendación concreta para el brief.

## 5. Guardar

Guardar en `inspiracion/` dentro del repositorio, con este nombre:

`inspiracion/<tema-en-kebab-case>-<AAAA-MM-DD>.md`

Obtener la fecha con `date +%F`. Por ejemplo: `inspiracion/app-finanzas-personales-2026-10-30.md`.

Estructura:

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

## Patrones comunes
- ...

## Recomendación para este brief
- ...

## Límites de esta búsqueda
- Páginas que no se pudieron leer, y por qué.
- Fuentes que no estuvieron disponibles, por ejemplo A1 Gallery.
```

No crear páginas en Notion ni otros servicios externos salvo que la persona lo pida: consumen más contexto y el archivo basta.

## 6. Cerrar

1. Confirmar la ruta del archivo creado.
2. Dar un resumen de 3 a 5 líneas en el chat: los ejemplos más útiles y la recomendación principal.
3. Si el archivo va al repositorio, hacer commit y push en la rama de trabajo. No abrir un pull request salvo que la persona lo pida.
