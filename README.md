# Islas Malvinas — Pixel Art & Interacción 3D HTML5 Canvas

Un mapa interactivo en **Pixel Art de las Islas Malvinas** ($54 \times 28$ celdas) desarrollado en HTML5 Canvas nativo, con animación de disolución aleatoria, efecto de iluminación radial y elevación 3D táctil.

---

## 🚀 Características

- **Standalone & Ultra Ligero**: Cero dependencias externas. HTML, CSS y JS nativo en un solo archivo.
- **Paleta ASCII por Luminosidad**: Estructura de código en ASCII art donde los datos forman la silueta de las islas directamente en la fuente.
- **Animación de Entrada / Salida**: Disolución aleatoria fluida a 60 FPS con curva cinematográfica (*Ease-Out Quartic*).
- **Iluminación & Elevación 3D (Hover / Touch)**:
  - **Luminosidad**: Halo radial de luz (+50% en el centro a +10% en el borde, radio de 5 módulos).
  - **Elevación**: Efecto domo 3D (hasta 3px de elevación en el eje Y) con sombra proyectada.
- **Soporte Multi-dispositivo (Desktop & Mobile)**:
  - **Desktop**: Puntero `cell` con respuesta a `mousemove` y `click`.
  - **Mobile**: Gestos táctiles diferenciados (**Tap** rápido para disolver, **Tap & Hold / Drag** para explorar relieve y luz).

---

## 🎮 Controles e Interacción

| Dispositivo | Acción | Resultado |
| :--- | :--- | :--- |
| **Desktop** | **Hover** | Activa el halo de luz (+50%) y elevación 3D (3px) en un radio de 5 módulos. |
| **Desktop** | **Click** | Alterna la animación de entrada / salida por disolución aleatoria. |
| **Mobile** | **Tap Rápido** (<220ms) | Alterna la animación de entrada / salida. |
| **Mobile** | **Tap & Hold / Arrastrar** | Enciende la iluminación radial y elevación 3D siguiendo la yema del dedo. |

---

## 🛠️ Estructura del Código

El archivo `index.html` incluye:
- **`malvinasPalette`**: Objeto con los 8 colores ordenados por densidad/luminosidad (`' '`, `.`, `:`, `-`, `=`, `+`, `#`, `@`).
- **`malvinasMap`**: Matriz ASCII de $54 \times 28$ celdas.
- **Adaptación Retina / High-DPI**: Renderizado nítido con `devicePixelRatio` y `image-rendering: pixelated`.

---

## 📄 Licencia

Este proyecto está bajo la Licencia [MIT](LICENSE).
