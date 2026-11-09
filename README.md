# 🦴 Museo Virtual de Paleontología

**Una sala de museo en 3D para recorrer desde el navegador, la tablet o el celular, con anteojos de cartón (Cardboard) si se tienen.**
Recurso educativo de la cátedra *Informática Educativa II* · Profesorado Universitario en Computación · FCEyN · UNLPam.

[![Abrir el museo](https://img.shields.io/badge/▶_Abrir_el_museo-e6c384?style=for-the-badge&labelColor=2a1f17)](https://villariasthiago.github.io/Museo-Virtual/)

👉 **https://villariasthiago.github.io/Museo-Virtual/**

---

## ¿Qué es?

Un museo virtual de una sola sala, hecho para mirar de cerca fósiles escaneados en 3D. No hay que instalar nada: se abre el enlace y se camina por la sala. Cada pieza se puede **tomar, girar y acercar** para verla desde todos los lados.

## ¿Qué se puede hacer?

| Acción | Cómo |
|---|---|
| **Mirar alrededor** | Arrastrar con el mouse o el dedo (en el celular también con el giroscopio) |
| **Caminar** | Teclas `W` `A` `S` `D` o las flechas |
| **Tomar una pieza** | Hacer clic o tocar el objeto: sale del plinto y queda frente a vos |
| **Girar la pieza** | Arrastrar |
| **Acercar o alejar** | Rueda del mouse, pellizco en pantalla táctil, botones `+` `−` o teclas `+` `-` |
| **Soltarla** | Botón *Soltar pieza* o tecla `Esc` |
| **Recorrido guiado** | Botón *Recorrido guiado*: pasa por cada pieza y termina frente al cartel del autor |
| **Anteojos VR** | Botón *Anteojos VR (Cardboard)*: pantalla dividida en dos ojos, con el recorrido automático |
| **Ajustar el visor** | Botón *Ajustar visor*: corrige la lente, el zoom, la separación entre ojos y el centrado |

## La sala

- **Cinco piezas** sobre plintos, cada una con su foco en el techo y una luz de realce, en una sala en penumbra para que los objetos resalten. Las piezas giran solas y cada una tiene su tarjeta con los datos.
- **Paredes de estratos** de roca sedimentaria con amonites, y piso de lajas de piedra.
- **Línea del tiempo geológico** (Precámbrico, Paleozoico, Mesozoico y Cenozoico) y paneles de campo: *Cuadrícula de excavación* y *Capas del tiempo*.
- **Cuatro peceras** con escorpiones y una serpiente coral que se mueven solos.
- **Cartel del autor** en la pared de la entrada.

## Las piezas

| Pieza | Descripción |
|---|---|
| `Macaca sp.` | Cráneo fósil |
| `PVSJ 585` | Fragmento de la Colección Ricardo |
| `GHUNLPam 15375` | Muestra de la Colección Paleontológica |
| `Montsecosuchus depereti` | Placa con esqueleto |
| `GHUNLPam 29818` | Muestra de la Colección Ricardo |

> ⚠️ **Los datos de las tarjetas son ilustrativos.** El nombre científico, el período, la procedencia y el tamaño son de ejemplo y están marcados en pantalla como *"Datos ilustrativos · a confirmar"*. Hay que reemplazarlos por la información verificada de cada pieza (ver más abajo).

## Cómo está hecho

Es una sola página HTML con [A-Frame](https://aframe.io/) 1.4.2 (WebGL). Los carteles, las paredes y el piso se dibujan con canvas, y las peceras y sus animales se arman con formas simples, sin imágenes externas. Los fósiles son archivos `.glb` en la misma carpeta. Funciona en un navegador común, sin servidor propio.

```
Museo-Virtual/
├── index.html            # la sala, las luces, los controles y el modo VR
├── macaca.glb            # modelos 3D de las piezas
├── modelo2.glb           #   (PVSJ 585)
├── modelo3.glb           #   (GHUNLPam 15375)
├── modelo4.glb           #   (GHUNLPam 29818)
├── montsecosuchus.glb
└── README.md
```

## Probarlo en tu compu

Los modelos se cargan por red, así que no alcanza con abrir `index.html` con doble clic. Desde la carpeta del proyecto:

```bash
python3 -m http.server 8000
```

y abrir <http://localhost:8000>.

## Cómo editar el contenido

Todo está al principio de `index.html`:

- **Datos de cada pieza:** el bloque `DATOS` (nombre científico, período, procedencia, tamaño). Al completarlos con datos reales, cambiar `ilustrativo` a `false` y se va el aviso.
- **Piezas y posición:** la lista `PIEZAS` (archivo, plinto, tamaño, inclinación, velocidad de giro y brillo de la luz de realce).
- **Luces:** en `buildSala` (luz ambiente) y `buildPieza` (foco y realce).
- **Cartel del autor:** la función `nombreCv`.

Para agregar una pieza: copiar el `.glb` a la carpeta y sumarlo a `PIEZAS`.

## Pendientes

- [ ] Cargar los datos reales de las cinco piezas.
- [ ] Revisar el peso de los modelos para equipos lentos (el cráneo es el más pesado).

## Autor

**Thiago Llovio Villarías** · Estudiante de 3.º año del Profesorado Universitario en Computación · UNLPam.
Parte de mi [e-portfolio](https://villariasthiago.github.io/e-portfolio/).
