# ReUso — motion graphics UI

Loop cuadrado de interfaz para presentar ReUso con una única forma que cambia de función bajo la acción de un cursor.

## Archivos principales

- `ReUso_Motion_120BPM.mp4`: video final con música y sonidos de interfaz.
- `ReUso_Motion_Interactivo.html`: versión autónoma; se abre en un navegador y permite buscar cualquier instante con `window.seek(segundos)`.
- `ReUso_Motion_Poster.png`: imagen de portada.
- `ReUso_Motion_Revision.png`: hoja de revisión tomada del MP4 final.
- `validacion_motion.json`: informe técnico del render.

## Especificaciones

- 1440 × 1440 píxeles.
- 60 fps y 840 fotogramas.
- 14,000 segundos, 7 compases de 4/4 a 120 BPM.
- H.264 High y audio AAC estéreo a 48 kHz.
- Cuatro subfotogramas por cuadro, combinados para producir desenfoque de movimiento.
- Tipografía Geist Variable incrustada en el HTML.
- Paleta: gris cálido, negro, blanco y un único verde `#168A5B`.
- Loop visual continuo: el primer cuadro, el último subfotograma de origen y `seek(14)` son idénticos.

## Secuencia

1. Publicar sobrante.
2. Carga y confirmación.
3. Isla dinámica.
4. Vista previa de una ventana de aluminio.
5. Recorrido del material.
6. Disponibilidad.
7. Filtro «Solo cerca».
8. Pestañas Materiales, Busco y Donaciones.
9. Meta piloto de 20 publicaciones en 6 semanas.
10. Búsqueda de «ventana».
11. Confirmación de la solicitud.
12. Regreso al botón inicial.

La meta del gráfico está rotulada como propuesta de piloto; no representa un resultado real. La ubicación y el material son ejemplos de la interfaz.

## Música

«ReUso — Un objeto, otra vida» fue sintetizada para este proyecto, sin muestras ni material de terceros, y publicada bajo CC0 1.0. La procedencia y las mediciones están en `assets/MUSICA_FUENTE_Y_LICENCIA.txt`.

## Volver a renderizar

Requiere Python 3, Node.js, Chromium, FFmpeg y las bibliotecas Python `numpy`, `Pillow` y `playwright`.

```sh
npm ci
npm run audio
npm run build
npm run beats
npm run render
npm run validate
```

`npm run beats` crea una prueba de los 28 picos musicales medidos antes de iniciar el render completo. La animación es determinista: no usa transiciones CSS, temporizadores ni estado acumulado entre cuadros.

El video narrado extenso del proyecto ReUso se entrega por separado. Esta pieza corta usa música original y sonidos de interfaz para funcionar como apertura, publicación en redes o apoyo visual durante la exposición.
