# Estudio Vinilo — terminado

Landing estática en `index.html`, `styles.css` y `script.js`. Abrir con un servidor estático, por ejemplo `python3 -m http.server 8000`.

Incluye navegación, hero con vinilo CSS, salas, equipo, tarifas demo en ARS, CTA WhatsApp +54 11 5555-0404 y footer Demo conceptual. No hay reservas simuladas ni formulario sin backend. Tarifas y prestaciones ilustrativas; fotografías generadas con IA.

## Imágenes
Se usó imagegen integrado, sin CLI. PNG originales en `assets/images/hero-sala.png`, `consolas.png`, `vinilos.png`, `banda.png`. Derivados WebP servidos por la página: aproximadamente 885 KB en total frente a 9,8 MB de PNG. Prompts completos en `image-prompts.md`.

## Validación
- Chromium/Playwright: capturas inspeccionadas en 390 y 1280 px, guardadas en `qa/`.
- Fotos decodificadas correctamente; sin errores de JS ni respuestas HTTP fallidas durante la revisión.
- Un h1, lang es-AR, salto al contenido y foco visible. Primer Tab llega al salto de contenido.
- Sin overflow horizontal a 390 y 1280 px; revisión adicional a 320 y 640 px.
- Pausar vinilo cambia animation-play-state a paused. Reduced-motion desactiva la animación y oculta su control.
- CTA WhatsApp apuntan a 541155550404 con consultas precargadas. No se enviaron mensajes.
- Favicon SVG, meta robots noindex/nofollow y `_headers` con X-Robots-Tag para hosts compatibles. Python http.server no interpreta `_headers`; otros servidores deben configurar esa cabecera. La meta noindex funciona independientemente de esa integración.
- Diseño revisado usando anti-generico, frontend-design y web-review. No equivale a una auditoría integral de accesibilidad ni a pruebas en dispositivos físicos. Fuentes requieren conexión; hay alternativas de sistema.

Sin git ni publicación.
