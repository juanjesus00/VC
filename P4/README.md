# Práctica 4

## Autores: Antonio Manuel Sánchez Ramírez, Juan Jesús Suárez Miranda

A continuacion, se va a explicar brevemente, que se ha realizado en las tareas correspondientes a la práctica 4:
En esta práctica 4, se ha realizado un programa que reconoce las matrículas de los vehículos y detecte las personas de un video.
**1.Reconocimiento de matrícula con imagen estática:**
  En primer lugar, especificamos que usaremos el cpu para analizar la imagen estaticamente, delimitamos con un marco de yolo los objetos que detecte como vehículos asignando la etiqueta de "CAR",     usamos ultralytics para mayor facildiad de detección, y una vex tengamos los parametros iniciales establecidos, en el proceso de detección, hacemos un recorte de la imagen cuando detectemos un      coche, aplicamos el model de deteccion de matriculas sobre el, volviendo a recortar la imagen por la matrícula y extrayendo las coordenadas. Para la obtencion de la informacion de la matricula,     hacemos uso de las coordenadas obtenidas anteriormente, procesamos la imagen y aplicamos el pytesseractsobre ella.
  Imagen de coche detectado con su matricula: ![image](https://github.com/user-attachments/assets/36be0d57-0439-4b92-a276-fe946d521d4e)

Video original: https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/EZY6OoIKkbZLl3LJVbHAGYoBBlHPB3Rwl-_gc_WslSuo5g?e=TKrUsC&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Video con los modelos aplicados: https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/ESn1MsolNDFMleOzKlCp-UwBH7B6NqhelcvMeVp_aR-71A?e=rf5A0y&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Salida de los modelos aplicados al video de prueba: ![image](https://github.com/user-attachments/assets/dd73067f-e358-42b8-8a5b-cc453ea2b14f)

