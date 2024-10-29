# Práctica 4
## Autores: Antonio Manuel Sánchez Ramírez, Juan Jesús Suárez Miranda
A continuación, se explican brevemente las tareas realizadas en la práctica 4. En esta práctica, hemos desarrollado un programa que reconoce las matrículas de vehículos y detecta personas en un video.

### **1. Reconocimiento de matrículas en imágenes estáticas**
Primero, especificamos el uso de la CPU para analizar la imagen de forma estática. Para la detección de vehículos, empleamos un modelo basado en YOLO que delimita los objetos etiquetados como "CAR". Utilizamos la biblioteca Ultralytics para facilitar la detección.

Una vez definidos los parámetros iniciales, el proceso de detección consiste en los siguientes pasos:

1. Recortamos la imagen cuando detectamos un coche.
2. Aplicamos un modelo específico para la detección de matrículas sobre el recorte y volvemos a recortar la imagen en la región de la matrícula, obteniendo sus coordenadas.
3. Para extraer la información de la matrícula, utilizamos las coordenadas obtenidas previamente y procesamos la imagen con pytesseract.
   Este procedimiento permite reconocer y extraer el texto de la matrícula de vehículos en imágenes estáticas de manera eficiente.
  
  Imagen de coche detectado con su matricula: ![image](https://github.com/user-attachments/assets/36be0d57-0439-4b92-a276-fe946d521d4e)

Video original: https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/EZY6OoIKkbZLl3LJVbHAGYoBBlHPB3Rwl-_gc_WslSuo5g?e=TKrUsC&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Video con los modelos aplicados: https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/ESn1MsolNDFMleOzKlCp-UwBH7B6NqhelcvMeVp_aR-71A?e=rf5A0y&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Salida de los modelos aplicados al video de prueba: ![image](https://github.com/user-attachments/assets/dd73067f-e358-42b8-8a5b-cc453ea2b14f)

