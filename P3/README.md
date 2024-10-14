# Práctica 3

## Autores: Antonio Manuel Sánchez Ramírez, Juan Jesús Suárez Miranda

A continuacion, se va a explicar brevemente, que se ha realizado en las tareas correspondientes a la práctica 3:

1. **Las tres imágenes cargadas en la celda inicial, han sido extraidas de las imágenes de mayor tamaño presentes en la carpeta. La tarea consiste en extraer características (geométricas y/o visuales) e identificar patrones que permitan distinguir las partículas de cada una de las tres clases, evaluando los aciertos y fallos con las imágenes completas considerando las métricas mostradas y la matriz de confusión. La matriz de confusión, muestra para cada clase el número de muestras que se clasifican correctamente de dicha clase, y el número de muestras que se clasifican incorrectamente por cada una de las otras dos clases.**
   
     - Mi compañero y yo, hemos llegado a una solución que es tomar en cuenta el area, el perimetro y a partir de ellos calcular la compacidad de cada contorno, teniendo en cuenta ademas parametros iniciales como un umbral del color oscuro ya que el alquitran es de color negro en comparacion con el pellet y los fragmentos y el 

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



 
