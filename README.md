# Práctica 1

A continuacion, se va a explicar brevemente, que se ha realizado en las tareas correspondientes a la práctica 1:

1. **Creación de una Imagen con Textura de Tablero de Ajedrez:**
    - Mi compañero y yo, hemos llegado a una solución parecida sobre la creación de un tablero de ajedrez, para ello, utilizamos un tablero de 800x800 y los cuadrados son de 40x40 píxeles, para el pintado, se ha utilizado dos bucles for, haciendo que se pinten cada cuadrado teniendo encuenta el espacion en blanco y el desfase de las filas pares. 

2. **Creación de una Imagen al Estilo Mondrian:**
    - Se ha creado una imagen de 500 x 500, donde se han pintado los rectangulos de forma aleatoria. La generación de rectángulos se hace for filas, dictaminando el tamaño de la fila, por el tamaño del primer rectángulo generado, las coordenadas de los rectángulos serán guardadas en una lista, para posteriormente, en las siguientes filas a dibujar, tener encuenta la altura del rectángulo superior y quitar el riesgo a superponer los rectángulos.

3. **Creación de una Imagen al Estilo trablero de ajedrez:**
    -Para la realización de esta tarea, replicamos los hecho en la tarea 1, pero añadiendo las herramientas de creación de rectángulos de OpenCV, por lo tanto, simplemente usando la misma metodología de un doble bucle pintamos los rectángulos en la posición indicada.

4. **Modificación de los Valores de un Plano de la Imagen:**
    - Capturamos imágenes de la cámara web y separamos sus canales. A continuación, aumentamos la intensidad de cada canal en 75 unidades y mostramos la fusión de la imagen original junto con otras tres imágenes que representan la unión de dos canales. Este resultado podría considerarse como una propuesta de pop-art.

5. **Pintura de Círculos en las Posiciones del Píxel Más Claro y Más Oscuro de la Imagen:**
    - Creamos un fotograma en escala de grises para mejorar la interpretación de la "luminosidad". Luego, recorrimos cada píxel de este fotograma y registramos la posición del píxel con el valor más alto y más bajo. Posteriormente, pintamos un círculo verde en la posición del píxel más claro y otro rojo en la posición del píxel más oscuro.

6. **Propuesta de Pop-Art:**
    - Hemos desarrollado una propuesta similar a la anterior, pero implementada de manera diferente. Recorrimos el fotograma de la misma manera que en el ejercicio anterior y si el valor del píxel estaba dentro de uno de los tres umbrales predefinidos (azul, rojo, verde), lo pintamos del color correspondiente. Esto hace que la propuesta sea poco eficiente pero también lo hace nuestro.


**Referencias**
- https://docs.opencv.org/4.x/dc/da5/tutorial_py_drawing_functions.html
- https://chat.openai.com
- https://docs.opencv.org/4.x/df/d9d/tutorial_py_colorspaces.html
