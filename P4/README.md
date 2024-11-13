# Práctica 4
## Autores: Antonio Manuel Sánchez Ramírez, Juan Jesús Suárez Miranda
A continuación, se explican brevemente las tareas realizadas en la práctica 4. En esta práctica, hemos desarrollado un programa que reconoce las matrículas de vehículos y detecta personas en un video. Como aclaración, previamente se ha hecho una prueba entrenando yolo con un dataset recogido de internet (best2.pt), y posteriormente con un modelo preentrenado para comparar los posibles resultados que se pueden obtener(placa.pt).

### **1. Reconocimiento de matrículas en imágenes estáticas**
Primero, especificamos el uso de la CPU para analizar la imagen de forma estática. Para la detección de vehículos, empleamos un modelo basado en YOLO que delimita los objetos etiquetados como "CAR". Utilizamos la biblioteca Ultralytics para facilitar la detección.

Una vez definidos los parámetros iniciales, el proceso de detección consiste en los siguientes pasos:

1. Recortamos la imagen cuando detectamos un coche.
2. Aplicamos un modelo específico para la detección de matrículas sobre el recorte y volvemos a recortar la imagen en la región de la matrícula, obteniendo sus coordenadas.
3. Para extraer la información de la matrícula, utilizamos las coordenadas obtenidas previamente y procesamos la imagen con pytesseract.
   Este procedimiento permite reconocer y extraer el texto de la matrícula de vehículos en imágenes estáticas de manera eficiente.
  
  Imagen de coche detectado con su matricula: ![image](https://github.com/user-attachments/assets/36be0d57-0439-4b92-a276-fe946d521d4e)


### **2. Reconocimiento de matrículas y personas en video**
Para esta detección, utilizamos la GPU con CUDA para el reconocimiento de vehículos y personas en un video, empleando la misma versión de YOLO.

Para el reconocimiento de vehículos, seguimos el mismo proceso que en la detección en imágenes estáticas. Para detectar personas, también utilizamos un marco de YOLO que etiqueta los elementos detectados como "PERSON". Al momento de la detección, se discrimina entre personas y vehículos para el conteo y para registrar los datos en un archivo CSV. Además, en el caso de detección de una matrícula, se realiza un recorte de imagen similar al del reconocimiento en imágenes estáticas.

Salida de los modelos aplicados al video de prueba: ![image](https://github.com/user-attachments/assets/dd73067f-e358-42b8-8a5b-cc453ea2b14f)

El video procesado se guarda en el dispositivo junto con el archivo CSV que contiene los datos de las detecciones.

Video original: https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/EZY6OoIKkbZLl3LJVbHAGYoBBlHPB3Rwl-_gc_WslSuo5g?e=TKrUsC&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Video con los modelos aplicados: https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/EVCk0efUHnBOvIf_Zox7aoABQnQGvuB07HRpJkrPqaC1eQ?e=qbZ1qg&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Video de modesto test usando el modelo placa: https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/EfQrzqpItRZBtPwEfqLF7XIB6M_Jvq4gsFGvlBNabHrhlw?e=k42HXc&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Video de modesto test usando el modelo entrenado: https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/EfQn_Fe814tJjb4xWyT_z3IB4MzQ4REPs8V33dVDbY-BTw?e=M1KhFP&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Video de cosecha propia usando el modelo entrenado: https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/EaJ2EtM7VjZPg4ooJbS0wBwBoXBMm58CTyWg3vsSc2w9HQ?e=bgIN8f&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

## Referencias
- https://chatgpt.com/
- https://docs.ultralytics.com/
- https://opencv-tutorial.readthedocs.io/en/latest/yolo/yolo.html
- (modelo preentrenado) https://github.com/jrguignan/Proyecto-Deteccion_de_Matriculas
- (dataset) https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e/dataset/6
