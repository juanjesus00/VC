# Práctica 2

## Autores: Antonio Manuel Sánchez Ramírez, Juan Jesús Suárez Miranda

A continuacion, se va a explicar brevemente, que se ha realizado en las tareas correspondientes a la práctica 2:

1. **Realiza la cuenta de píxeles blancos por filas (en lugar de por columnas). Determina el valor máximo de píxeles blancos para filas, maxfil, mostrando el número de filas y sus respectivas posiciones, con un número de píxeles blancos mayor o igual que 0.95*maxfil:**
   
     - Mi compañero y yo, hemos llegado a una solución parecida al ejemplo propuesto para la realización de esta tarea, convertimos a gris la imagen, obtenemos los contornos con el operador canny, normalizamos en base al número de filas, obteniendo así el número de píxeles blancos por filas, obtenemos el valor máximo de entra las filas que existen en el array, y de ahí sacamos el 95%, luego filtramos aquellas filas que superen dicho umbral y mostramos por grafica.

2. **Aplica umbralizado a la imagen resultante de Sobel (convertida a 8 bits), y posteriormente realiza el conteo por filas y columnas similar al realizado en el ejemplo con la salida de Canny de píxeles no nulos. Calcula el valor máximo de la cuenta por filas y columnas, y determina las filas y columnas por encima del 0.95*máximo. Remarca con alguna primitiva gráfica dichas filas y columnas sobre la imagen. ¿Cómo se comparan los resultados obtenidos a partir de Sobel y Canny?:**
   
    - Primero, convertimos la imagen a gris, eliminamos las altas frecuencias con guassiana, calculamos el sobel en ambas direcciones y los juntamos, definimos el valor del umbral y umbralizamos el resultado de la imagen convertida con sobel, aplicamos canny a la imagen y recogemos los pixeles no nulos tanto de las columnas como de las filas, encontramos el valor máximo de cada dirección (fila y columna) y filtramos tanto filas como columnas que superen el 95% de dicho umbral, para finalmente mostrar por la grafica tanto las filas como las columnas.

3. **Proponer un demostrador que capture las imágenes de la cámara, y les permita exhibir lo aprendido en estas dos prácticas ante quienes no cursen la asignatura :). Es por ello que además de poder mostrar la imagen original de la webcam, incluya al menos dos usos diferentes de aplicar las funciones de OpenCV trabajadas hasta ahora:**
   
    - Para la realización de esta tarea, hemos decidido generar 3 modos, el primer modo es simplemente mostrar los frames de la webcam sin filtro, el segundo modo se encarga de mostrar cada frame pero únicamente el fondo a su vez tiene un detector de manos y por ultimo el tercer modo que es un modo fantasmal o sin fondo en el que no se mostraran pixeles blancos a no ser que se detecte movimiento o cambio de colores de pixeles en la webcam simulando una apariencia fantasmal, ademas este modo detecta las manos tambien, en ambos modos (el 2 y el 3) se dibujara un circulo verde en el segundo y blanco en el tercero mostrando la mano detectada, (PARA PASAR DE UN MODO A OTRO SE DEBE DE PULSAR LOS NÚMEROS DEL TECLADO 1,2 Y 3 PARA PASAR A LOS RESPECTIVOS MODOS).

4. **Tras ver los vídeos [My little piece of privacy](https://www.niklasroy.com/project/88/my-little-piece-of-privacy), [Messa di voce](https://youtu.be/GfoqiyB1ndE?feature=shared) y [Virtual air guitar](https://youtu.be/FIAmyoEpV5c?feature=shared) proponer un demostrador reinterpretando la parte de procesamiento de la imagen, tomando como punto de partida alguna de dichas instalaciones:**
   
    - Juan Jesús se encargo de en base a una imagen generar 3 copias, una ajusta los valores de los canales rojo y azul disminuyendolos, luego en otra la pone a escala de grises y la última en blanco y negro.
    - Antonio se encargo de realizar una captura de video de la webcam y por cada fotograma separa el canal azul, y de manera aleatoria modifica su valor mostrandolo de imagen.

**Referencias**
- https://docs.opencv.org/4.x/dc/da5/tutorial_py_drawing_functions.html
- https://chat.openai.com
- https://docs.opencv.org/4.x/df/d9d/tutorial_py_colorspaces.html

**IMAGENES**

1. Tarea 1:
   
   ![image](https://github.com/user-attachments/assets/84d984dc-23cd-4d9d-9e28-76bf2dc7c0cd)

2. Tarea 2:
   
   ![image](https://github.com/user-attachments/assets/8949fece-dcdc-44e6-b03a-fe3e760578a5)
   
3. Tarea 3:

   Modo sin filtro:
   
   ![image](https://github.com/user-attachments/assets/6221ccbe-574d-4e50-bb26-3f14ee5d4dd5)

   Modo fondo:

   ![image](https://github.com/user-attachments/assets/452fc920-0534-43d9-9e30-d04258d46220)

   Modo fantasmal o sin fondo:

   ![image](https://github.com/user-attachments/assets/c47fb111-26ed-49bc-8287-1f285a5c8a7a)

5. Tarea 4:

   
