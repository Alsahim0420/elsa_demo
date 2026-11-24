# Sistema de diseño de ELSA 360 (app móvil)

Referencia de tokens para diseñar y construir pantallas de la app. Los colores están resueltos a su valor hexadecimal.

> **Regla de oro:** lo que no está definido aquí no se inventa. Se le pide a diseño.

## Índice

1. [Principios](#principios)
2. [Colores por intención](#colores-por-intención)
3. [Colores de estado](#colores-de-estado)
4. [Colores de datos](#colores-de-datos)
5. [Paleta base](#paleta-base)
6. [Tipografía](#tipografía)
7. [Espacios, radios y bordes](#espacios-radios-y-bordes)
8. [Tamaños](#tamaños)
9. [Opacidades](#opacidades)
10. [Movimiento](#movimiento)
11. [Diseño adaptable](#diseño-adaptable)
12. [Origen de los valores](#origen-de-los-valores)

---

## Principios

- **Oscuro por defecto.** El tema claro solo aparece si la persona lo elige; la app no sigue el tema del sistema.
- **Sin sombras.** La profundidad se da con el tono del fondo, de abajo arriba: lienzo → superficie → elevada → tercera.
- **Colores de identidad:** verde ELSA `#54CF00` y negro ELSA `#030700`, con neutros cálidos de tono verdoso.
- **Valores iguales a la app web.** La única diferencia es el área táctil mínima: **48** en móvil, frente a 44 en la web.
- **Lo que no está definido no se inventa:** se le pide a diseño.

---

## Colores por intención

Usa siempre estos tokens en pantalla, nunca la paleta base directamente.

### Fondos

| Token | Uso | Oscuro | Claro |
|---|---|---|---|
| `bgCanvas` | Fondo de pantalla | `#030700` | `#FFFFFF` |
| `bgDeep` | Barras de app y de navegación | `#030700` | `#FFFFFF` |
| `bgSurface` | Tarjetas | `#14180F` | `#F4F6F2` |
| `bgSurfaceRaised` | Algo encima de una tarjeta | `#1F2418` | `#E9ECE7` |
| `bgSurfaceThird` | Tercer nivel | `#2A3122` | `#DCDFD9` |
| `bgSurfaceInset` | Hundido (campos de texto) | `#030700` | `#FFFFFF` |
| `bgOverlay` | Velo detrás de diálogos | `#030700` al 70 % | `#030700` al 70 % |
| `bgSelected` | Elemento seleccionado | `#2C3B1E` | `#D9F4C7` |
| `bgBrand` | Botón principal | `#54CF00` | `#54CF00` |

### Texto

| Token | Uso | Oscuro | Claro |
|---|---|---|---|
| `textPrimary` | Texto principal | `#F0F2ED` | `#1F2418` |
| `textSecondary` | Texto de apoyo | `#9AA293` | `#5F645B` |
| `textOnBrand` | Texto sobre verde | `#030700` | `#030700` |
| `textBrand` | Enlaces y acentos | `#54CF00` | `#266702` |

### Bordes

| Token | Uso | Oscuro | Claro |
|---|---|---|---|
| `borderDefault` | Divisores, tarjetas | `#292D25` | `#DCDFD9` |
| `borderInput` | Campos | `#696D66` | `#848880` |
| `borderBrand` | Borde de acento | `#54CF00` | `#266702` |
| `borderChip` | Chips | `#9AA293` | `#848880` |
| `borderFocus` | Foco del teclado | `#54CF00` | `#266702` |

### Marca (interacción)

| Token | Uso | Oscuro | Claro |
|---|---|---|---|
| `brandHover` | Al pasar el puntero por encima | `#60EB00` | `#60EB00` |
| `brandPressed` | Al presionar | `#47AD00` | `#47AD00` |
| `logo` | Logotipo | `#54CF00` | `#030700` |

---

## Colores de estado

Van **siempre en pareja**: el color se usa para el texto o el icono, y su `…Bg` para el fondo.

| Estado | Oscuro (color / fondo) | Claro (color / fondo) |
|---|---|---|
| `statusSuccess` | `#54CF00` / `#2C3B1E` | `#266702` / `#D9F4C7` |
| `statusWarning` | `#FFAB00` / `#4C3F36` | `#795A0E` / `#FFEDC7` |
| `statusDanger` | `#F87171` / `#492727` | `#76433C` / `#FDE0E0` |
| `statusInfo` | `#409EFF` / `#23303F` | `#2C5574` / `#D5EAFF` |

---

## Colores de datos

**Solo para gráficas y métricas.** No se usan en la interfaz general.

| Token | Uso | Oscuro | Claro |
|---|---|---|---|
| `dataPrimary` | Serie principal | `#54CF00` | `#3F9F00` |
| `dataHeartRate` | Frecuencia cardiaca | `#FF4500` | `#FF4500` |
| `dataPower` | Potencia | `#FFD700` | `#A48903` |
| `dataZone1` | Zona 1 (azul) | `#5DADE2` | `#4192C6` |
| `dataZone2` | Zona 2 (turquesa) | `#48C9B0` | `#069D87` |
| `dataZone3` | Zona 3 (amarillo) | `#F9E79F` | `#9C8B45` |
| `dataZone4` | Zona 4 (naranja) | `#EB984E` | `#C87729` |
| `dataZone5` | Zona 5 (rojo) | `#EC7063` | `#E06559` |
| `dataAxis` | Ejes | `#9AA293` | `#5F645B` |
| `dataGrid` | Cuadrícula | `#292D25` | `#DCDFD9` |
| `dataBackground` | Fondo de gráfica | `#030700` | `#F4F6F2` |

- Las zonas van de la más suave a la más intensa: azul, turquesa, amarillo, naranja y rojo.
- Para el relleno de un área de gráfica se aplica `opacityDataFill` (40 %).

---

## Paleta base

Valores crudos. **No se usan directamente**: los tokens de intención apuntan a ellos.

**Neutros**

| Paso | Valor |
|---|---|
| 20 | `#14180F` |
| 25 | `#1F2418` |
| 29 | `#292D25` |
| 30 | `#2A3122` |
| 47 | `#5F645B` |
| 53 | `#696D66` |
| 58 | `#848880` |
| 70 | `#9AA293` |
| 90 | `#DCDFD9` |
| 94 | `#E9ECE7` |
| 96 | `#F0F2ED` |
| 97 | `#F4F6F2` |

**Marca**

| Paso | Valor |
|---|---|
| 400 | `#60EB00` |
| 500 | `#54CF00` |
| 600 | `#47AD00` |
| 800 | `#266702` |
| Tinte | `#2C3B1E` |
| Tinte claro | `#D9F4C7` |

---

## Tipografía

Dos familias: **Archivo** para títulos y cifras, e **Inter** para todo lo demás.

> Todavía no están empaquetadas en la app, así que por ahora se ve la fuente del sistema.

| Token | Familia | Tamaño / alto de línea | Peso | Uso |
|---|---|---|---|---|
| `textDisplayLg` | Archivo | 32 / 38 | 900 | Título grande, marca |
| `textDisplayMd` | Archivo | 24 / 28 | 900 | Título destacado |
| `textTitleScreen` | Archivo | 24 / 25 | 900 | Título de pantalla |
| `textTitleSection` | Archivo | 18 / 22 | 700 | Título de sección |
| `textMetricLg` | Archivo | 20 / 24 | 700 | Cifras y métricas |
| `textHeadline` | Inter | 20 / 24 | 400 | Encabezado |
| `textBodyLg` | Inter | 18 / 24 | 400 | Texto grande |
| `textTitleMd` | Inter | 16 / 20 | 600 | Título de elemento |
| `textBodyMd` | Inter | 16 / 20 | 400 | Texto normal |
| `textButton` | Inter | 15 / 18 | 600 | Botones |
| `textBodySm` | Inter | 14 / 18 | 400 | Texto pequeño |
| `textLabel` | Inter | 12 / 16 | 400 | Etiquetas |
| `textLabelCaps` | Inter | 11 / 14 | 600, espaciado 0.88 | Etiquetas en mayúsculas |
| `textCaption` | Inter | 11 / 14 | 500 | Notas, términos |

---

## Espacios, radios y bordes

**Espacios:** `2` · `4` · `6` · `8` · `10` · `12` · `16` · `20` · `24` · `32` · `48`

- Margen lateral de pantalla: **16**.

**Radios**

| Token | Valor | Uso |
|---|---|---|
| `Xs` | 4 | |
| `Md` | 10 | |
| `Lg` | 12 | Botones |
| `Xl` | 24 | |
| `Full` | — | Píldora o círculo |

**Grosor de borde**

| Tipo | Valor |
|---|---|
| Normal | 1 |
| Chip | 1.5 |
| Stepper | 2 |
| Foco | 2 |

---

## Tamaños

**Controles**

| Tamaño | Alto | Uso |
|---|---|---|
| Grande | 48 | Botón principal |
| Mediano | 40 | |
| Pequeño | 32 | |

**Iconos:** `12` · `16` · `18` · `24` · `40`

**Área táctil mínima:** **48**

**Barras**

| Elemento | Alto |
|---|---|
| Barra de app | 56 |
| Barra de título | 48 |
| Navegación inferior | 74 |

---

## Opacidades

| Uso | Valor |
|---|---|
| Inactivo | 50 % |
| Deshabilitado | 60 % |
| Atenuado | 70 % |
| Relleno de datos | 40 % |

---

## Movimiento

**Duraciones (ms)**

| Token | Valor |
|---|---|
| Instantánea | 100 |
| Rápida | 150 |
| Normal | 250 |
| Lenta | 350 |
| Gráfica | 600 |
| Bucle | 1200 |

**Curvas (cubic-bezier)**

| Token | Valor |
|---|---|
| Estándar | `(0.2, 0, 0, 1)` |
| Entrada | `(0, 0, 0, 1)` |
| Salida | `(0.3, 0, 1, 1)` |

**Con movimiento reducido:** la animación se queda en un fundido de 100 ms y termina en el mismo estado final.

---

## Diseño adaptable

| Ancho de ventana | Navegación | Contenido |
|---|---|---|
| Menos de 600 | Barra inferior | A todo lo ancho, margen de 16 |
| 600 o más | Riel lateral (si la ventana mide al menos 480 de alto) | Centrado, con ancho máximo |

- **Nunca se decide por el tipo de aparato**, solo por el tamaño de la ventana.
- La orientación no se bloquea.
- El texto tiene que aguantar al **200 %** sin desbordarse.

---

## Origen de los valores

Los valores salen de los archivos de tokens `design/tokens/base.json`, `design/tokens/themes/dark.json` y `design/tokens/themes/light.json`. Si este documento y esos archivos no coinciden, mandan los archivos.
