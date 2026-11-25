# Máquinas de estados finitos

Material didáctico para introducir las **máquinas de estados finitos (FSM)** en un curso de Sistemas Digitales, con un puente hacia la robótica.

## Contenido

| Carpeta | Qué hay |
|---|---|
| [`presentacion/`](presentacion/) | Presentación interactiva de 8 diapositivas (HTML) y su versión en PDF |
| [`matter_pkg/`](matter_pkg/) | Ejemplos en Python con la biblioteca [`transitions`](https://github.com/pytransitions/transitions): fases de la materia y la actividad de un robot |

## La presentación

Una clase introductoria de 12 minutos con enfoque conceptual:

1. **Por qué hace falta memoria.** El límite de la lógica combinacional, planteado con una pregunta sobre un semáforo.
2. **Estado, entrada y transición.** Las tres ideas base, en notación UML, con el ejemplo de los cambios de fase del agua.
3. **Un semáforo con botón peatonal.** La máquina se construye paso a paso con un simulador en vivo, y luego se verifica con su tabla de comportamiento.
4. **Moore y Mealy.** La misma transición vista de las dos formas: la salida en el estado o en la flecha.
5. **Extensión a la robótica.** El mismo modelo aplicado al comportamiento de un robot móvil en ROS 2.

Cierra con un reto de diseño: agregar un modo de emergencia al semáforo.

**Ver en línea:** [roncanciovl.github.io/maquinas-de-estados/presentacion](https://roncanciovl.github.io/maquinas-de-estados/presentacion/). Es interactiva y no requiere instalar nada.

**Sin conexión:** descarga [`presentacion/index.html`](presentacion/index.html) y ábrelo en un navegador.

| Tecla | Acción |
|---|---|
| `←` `→` | Cambiar de diapositiva |
| `F` | Pantalla completa |
| `N` | Notas del orador |
| `P` | Ventana de presentador con reloj de 12 minutos |

Si solo quieres leerla, usa el [PDF](presentacion/maquinas-de-estados-finitos.pdf).

Fue preparada para una sesión docente de Sistemas Digitales I en la Escuela de Ingenierías Eléctrica, Electrónica y de Telecomunicaciones (E3T) de la Universidad Industrial de Santander, en noviembre de 2026.

## Los ejemplos en Python

```bash
pip install transitions matplotlib
cd matter_pkg
python stm.py        # fases de la materia: sólido → líquido → gas
python stm_robot.py  # actividad de un robot, con acciones al entrar y al salir de un estado
```

`stm_robot.py` usa `on_enter` y `on_exit`, que corresponden a `entry /` y `exit /` de la notación UML que se explica en la presentación.

`stm.py` modela con código lo mismo que la diapositiva 3 dibuja en UML: estados, eventos que disparan transiciones y un estado inicial.

## Autor

Henry Antonio Roncancio Velandia — Ingeniero Electrónico (Universidad Distrital) · Magíster en Ingeniería Mecánica (Universidade de São Paulo).

## Licencia

[Apache 2.0](LICENSE), para todo el repositorio.
