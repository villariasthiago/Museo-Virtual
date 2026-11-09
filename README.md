<div align="center">

# 🦴 Museo Virtual de Paleontología

### Una sala de museo en 3D para recorrer desde el navegador, la tablet o el celular

<br>

<a href="https://villariasthiago.github.io/Museo-Virtual/">
  <img src="https://img.shields.io/badge/%E2%96%B6%20%20ABRIR%20EL%20MUSEO-Sala%203D%20%C2%B7%20Cardboard-e6c384?style=for-the-badge&labelColor=2a1f17" alt="Abrir el museo" height="56">
</a>

<br><br>

🔗 **[villariasthiago.github.io/Museo-Virtual](https://villariasthiago.github.io/Museo-Virtual/)**

**👆 Hacé click y recorré la sala, sin instalar nada 👆**

<br>

![piezas](https://img.shields.io/badge/piezas-5%20fósiles%203D-e6c384?style=flat-square&labelColor=2a1f17)
![modo](https://img.shields.io/badge/modo-VR%20Cardboard-4a3a2b?style=flat-square)
![hecho con](https://img.shields.io/badge/hecho%20con-A--Frame-f6efe0?style=flat-square&labelColor=2a1f17)
![cátedra](https://img.shields.io/badge/cátedra-Informática%20Educativa%20II-cdbfa6?style=flat-square&labelColor=2a1f17)

</div>

---

Recurso educativo de la cátedra *Informática Educativa II* · Profesorado Universitario en Computación · FCEyN · UNLPam.

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

---

## 👋 Más proyectos

<div align="center">

<a href="https://villariasthiago.github.io/e-portfolio/#inicio">
  <img src="https://img.shields.io/badge/%F0%9F%8C%90%20%20Mi%20portafolio-ver%20otros%20proyectos-46e3c9?style=for-the-badge&labelColor=8f7bff" alt="Mi portafolio">
</a>

</div>
