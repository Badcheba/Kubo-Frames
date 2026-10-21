# KUBO · Brainstorming de la web

Estado al 21 de octubre de 2026. Temas 1 (apertura) y 2 (secciones) casi cerrados; faltan el 3 (movimiento) y el 4 (resumen final).

Manual de marca: https://claude.ai/artifact/Kc8RXLHXLARTWjo1PB18GE

## Reglas generales

- La marca siempre se escribe **KUBO**, en mayúsculas. Lema: **"Your passion, framed."**
- Una sola página, en inglés, con botón EN/ES.
- Moderna, sobria, de lujo. Nada de plantillas ni de tono de oferta.
- Paleta: carbón #575757, plata #D9D9D9, rojo #D8302E solo como acento, negro #111111 y blanco #FFFFFF. Tipografía Montserrat (800 en títulos, 500 en textos).
- Material visual: solo fotos y diseños propios. Sin fotos de stock.
- **No usar como referencia el boceto actual del repo** (`index.html`, `styles.css`). Se empieza de cero. Las imágenes de `img/` sí sirven para la prueba.
- **Sin KUBO Digital**: no se venden fondos descargables. En su lugar, envíos a todo el mundo.

## Líneas de producto (editables)

Las líneas viven en una lista de datos aparte del código. Agregar, sacar o renombrar una línea no obliga a tocar la animación.

| Línea | Habitación en la apertura | Ejemplos disponibles |
|---|---|---|
| Motor Legends (no numerada) | Museo, focos cenitales, concreto carbón | Ficha del Dodge Viper (`img/motor-legends-viper.jpg`) |
| Pop Culture | Cine a oscuras, haz del proyector | Falta: diseños de Canva |
| EV Line | Oficina de vidrio, luz de día fría | F-150 Lightning (`img/ev-line-f150.jpg`) |
| Japan Customs Line | Garage de noche con luz LED | Mazda MX-5 (`img/japan-customs-mx5.jpg`) |
| KUBO Custom | Pasillo de una casa, luz cálida | Falta: Black Widow / Colapinto |
| Truck Line (nombre provisorio) | Galpón de madera, lámpara de trabajo, nieve en la ventana | Dos diseños de Dodge RAM en Canva |
| Línea premium (nombre a definir; propuesta: KUBO Signature) | Vitrina oscura, un solo foco | Falta |

Las habitaciones se arman con luz, material de pared y un solo detalle. Sin muebles.

Aviso de marcas: en la web conviene usar el nombre del modelo como dato ("2019 RAM 1500") en lugar de logos oficiales.

## Tema 1 · Apertura (decidido)

- Recorrido en **primera persona** por un pasillo tipo galería, que avanza con el scroll. Botón **"Skip"** siempre visible.
- **Cada habitación es una línea.** Al avanzar, cada una se acomoda en pantalla y queda como la entrada a su colección, con uno o dos cuadros de ejemplo.
- Los cuadros se arman en digital a partir de los diseños de Canva: marco negro o blanco, vidrio con reflejo, sombra en la pared y el auto adelante, recortado de fotos sobre fondo liso.
- **Final:** el último cuadro (la vitrina premium) se convierte en la **O del logo**, aparece "KUB" y "Your passion, framed.", y el logo se achica y sube al menú fijo.
- **Celular:** versión más liviana, con un solo cuadro fijo mientras la pared cambia alrededor.
- La animación se programa en el código de la web. No hace falta video ni edición.

## Tema 2 · Secciones (propuesta, falta confirmar)

**Menú fijo:** logo, Collections, How it works, Pricing, Order, EN/ES y botón rojo "Start your frame".

1. **Apertura y colecciones.** El recorrido por las habitaciones.
2. **Frase de marca.** "Every frame tells a story: the movie, the era, the model."
3. **Colecciones.** Índice de las líneas. Cada una se abre con descripción, cuadros y precio "desde".
4. **Cómo funciona.** Elegís línea o contás tu idea → traés tu auto o lo conseguimos → diseñamos y armamos a mano. "Worldwide shipping."
5. **Hecho a mano.** Fotos reales sobre madera y detalle de la firma KUBO al pie del cuadro.
6. **Precios.** Tabla en CAD.
7. **Dónde verlos.** Memory Lane, más una línea para negocios ("For shops, garages and bars").
8. **Formulario** (ver abajo).
9. **Pie.** PREMIUM COLLECTOR SERIES · KUBO · Your passion, framed. Instagram, email, "Based in Winnipeg, Manitoba".

## Precios públicos (CAD)

| | Grande · 8 x 10 in | Chico |
|---|---|---|
| Colección, auto básico incluido | 45 | 30 |
| Colección con auto Pop Culture o F1 | 50 a 55 | 35 a 40 |
| Personalizado (el cliente trae el auto) | desde 55 | desde 50 |
| Línea premium con agregados 3D | 70 a 80 | — |

Envío: **"Worldwide shipping, quoted with your design"**. El costo de envío se cotiza junto con la propuesta, según el destino.

## Formulario (decidido)

Un solo formulario. Arriba: "What can we help you with?"

- **Question:** nombre, email, mensaje.
- **Custom order:**
  1. Contacto: nombre, email, Instagram (opcional), ciudad y país.
  2. El auto: modelo y año, si lo trae el cliente o lo consigue KUBO, y **de 1 a 5 fotos del auto** (computadora o cámara del celular). Ayuda: "Side and front photos on a plain background work best."
  3. El cuadro: tamaño (8 x 10 o chico) y línea base.
  4. El dueño: para el cliente o regalo. Si es regalo: para quién, su relación con el auto, sus gustos y la ocasión.
  5. La idea: historia, estilo, colores, épocas, referencias. Puede subir imágenes de inspiración.
  6. Plazo: fecha, si es para una ocasión.
  - Cierre: "Tell us the story of your car. We reply with a design idea and a price."
- **Business:** negocio, tipo de pedido, cantidad aproximada.

Muestra: **la arma Seba a mano** con las fotos del cliente y la envía con el precio. Sin vista previa automática por ahora.

Hace falta un servicio de envío de formularios con adjuntos; se define al armar la web.

## Pendientes

- [ ] Confirmar el orden de secciones (tema 2). ¿Sumar preguntas frecuentes sobre envío y tiempos?
- [ ] Usuario de Instagram y email de contacto.
- [ ] Exportar de Canva los diseños en PNG de alta calidad, nombrados por línea y auto (por ejemplo `pop-culture-batimovil.png`). Canva ya está conectado; se usa desde una sesión nueva.
- [ ] Una foto de frente de un cuadro real terminado, para copiar el marco en digital.
- [ ] Fotos de autos sueltos sobre fondo liso.
- [ ] Logo en PNG grande (o SVG) para la versión final.
- [ ] Nombres finales: línea de camionetas y línea premium.
- [ ] Actualizar el manual de marca: sacar KUBO Digital, sumar Truck Line y envíos a todo el mundo.
- [ ] Tema 3: movimiento al hacer scroll y al pasar el mouse sobre los cuadros.
- [ ] Tema 4: resumen final corto para pegar en el proyecto.
