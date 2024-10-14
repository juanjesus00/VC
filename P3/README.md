# Práctica 3

## Autores: Antonio Manuel Sánchez Ramírez, Juan Jesús Suárez Miranda

A continuacion, se va a explicar brevemente, que se ha realizado en las tareas correspondientes a la práctica 3:

<p align="justify">1. **Captura una o varias imágenes con monedas no solapadas. Tras visualizar la imagen, identifica de forma interactiva (por ejemplo haciendo clic en la imagen) una moneda de un valor determinado en la imagen (por ejemplo de 1€). Tras ello, la tarea se resuelve mostrando por pantalla el número de monedas y la cantidad de dinero presentes en la imagen. No hay restricciones sobre utilizar medidas geométricas o de color. ¿Qué problemas han observado?
Nota: Para establecer la correspondencia entre píxeles y milímetros, comentar que la moneda de un euro tiene un diámetro de 23.25 mm. la de 50 céntimos de 24.35, la de 20 céntimos de 22.25, etc. 
Extras: Considerar que la imagen pueda contener objetos que no son monedas y/o haya solape entre las monedas. Demo en vivo.**
   
     - Mi compañero y yo, luego de plantear varios intentos de soluciones, nos topamos con varios problemas, ¿y si nos llega una imagen movida?, o ¿la imagen es tomada desde mas lejos o cerca?, para ello tuvimos que descartar todo tipo de obtención de características basadas en los píxeles respecto al tamaño de la imagen, ya que, con la profundidad de los objetos en la imagen no se podría obtener con exactitud, o tener encuenta las medias de los diámetros de las monedas, pero esto, obligaria a tener siempre una moneda de 2 euros y una de 1 céntimo para establecer dicha relación. Para resolver esto, aplicamos la solución de usar un objeto de referencia el cual conocamos su tamaño en mm (en este caso una tarjeta con medida de 86 mm), y que las monedas siempre estén en el mismo plano. Con esta solución podremos obtener el largo de la referencia en píxeles, el diámetro de cada moneda en píxeles, y hacer la división del diámetro entre el largo de la referencia y tendríamos el % que aplicaremos a la medida de la referencia en mm, para obtener una aproximación del tamaño real de cada moneda. Previamente, antes de este proceso se usarán las funciones de umbralización de la imagen para que sea mas fácil la detección de contornos. Por último, añadimos el extra de detección de monedas superpuestas, y seleccionar las monedas en vivo, obteniendo su valor concreto.</p>

2. **Las tres imágenes cargadas en la celda inicial, han sido extraidas de las imágenes de mayor tamaño presentes en la carpeta. La tarea consiste en extraer características (geométricas y/o visuales) e identificar patrones que permitan distinguir las partículas de cada una de las tres clases, evaluando los aciertos y fallos con las imágenes completas considerando las métricas mostradas y la matriz de confusión. La matriz de confusión, muestra para cada clase el número de muestras que se clasifican correctamente de dicha clase, y el número de muestras que se clasifican incorrectamente por cada una de las otras dos clases.**
   
    - Mi compañero y yo, hemos llegado a una solución que es tomar en cuenta el área, el perímetro y a partir de ellos calcular la compacidad de cada contorno, teniendo en cuenta además parámetros iniciales como un umbral del color oscuro, ya que el alquitrán es de color negro en comparación con el pellet y los fragmentos y el umbral de la relación de aspecto que también se calcula en base a la relación entre el ancho y el alto, gracias a estos cálculos para cada contorno podemos distinguir con una precisión del 75% los elementos de las 3 imágenes que se han tenido en cuenta (PEL.png, FRA.png, TAR.png).

**Referencias**
- https://chat.openai.com

**IMAGENES**

1. Tarea 1:

  Conversión de una imagen no enderezada a imagen enderezada:

  ![image](https://github.com/user-attachments/assets/cede6cc6-e367-4fd3-be75-b8c2f110b0fe)

  Detección de monedas:
  
  ![image](https://github.com/user-attachments/assets/571fa1d2-8c40-4ac4-9ab5-a6dd24c6ebf7)

  Seleccionador interactivo de monedas encontradas (Clicar en una de las monedas te devolverá un output con el valor de la moneda):

  ![image](https://github.com/user-attachments/assets/d2ef1ff2-9928-4a8d-acef-ecc91f936fa2)

2. Tarea 2:

   Resultados obtenidos a partir de las características tomadas, mostrando la precision, accuracy, recall y F1 Score.

   ![image](https://github.com/user-attachments/assets/51ca58b6-bd83-4b23-8b4b-eb90dd5aaebb)



 
