# FRESCÓ · el sistema

Las tres pantallas del sistema de FRESCÓ, el restaurante del TFM en Inteligencia
Artificial e Innovación. La carta no cambia nunca: lo que cambia es el orden, y lo
decide lo que está a punto de caducar.

| Pantalla | Quién la mira | Qué hace |
|---|---|---|
| [`/servicio/`](servicio/) | Sala y cocina | Mesa, cocina y pantalla de comedor conectadas. Se pide desde la mesa, la comanda entra en el pase, descuenta producto y mueve la prioridad. |
| [`/carta/`](carta/) | El comensal | La carta franja a franja, con la recomendación de la casa y los textos que escribe el modelo de lenguaje. |
| [`/cocina/`](cocina/) | El pase | Prioridad por ingrediente, el motivo de cada decisión, el texto que se publicó y el que no. |

La landing del proyecto, que cuenta la idea entera, vive en su propio repositorio:
<https://norahmartinn.github.io/fresco-landing/>

## Cómo está montado

Tres archivos HTML autocontenidos. Sin build, sin dependencias, sin servidor: todo
el CSS, el JavaScript y las imágenes van dentro del propio archivo. Lo único que se
carga de fuera son las tipografías de Google Fonts.

El cálculo de riesgo de merma y la regla de decisión están portados a JavaScript
desde el simulador en Python del proyecto. La carta y el tablero reproducen una
ejecución grabada del brazo generativo, con la caché del modelo versionada, así que
los textos se reproducen sin claves de API.

## Desarrollo

No hay nada que compilar. Para verlo en local:

```bash
python3 -m http.server 8000
```

Y abrir <http://localhost:8000>.

---

Norah Martín Herrero · Trabajo Fin de Máster · 2026
