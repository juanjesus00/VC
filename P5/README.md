# Práctica 5
## Autores: Antonio Manuel Sánchez Ramírez, Juan Jesús Suárez Miranda
A continuación, se explican brevemente las tareas realizadas en la práctica 5. En esta práctica, hemos desarrollado diferentes programas enfocados en la detección de caras mediante la libreria "dlib" aplicando una serie de transformaciones y filtros jugando con las detecciones faciales en la webcam

### **Tarea**
Tras mostrar opciones para la detección y extracción de información de caras humanas con deepface, la tarea a entregar consiste en proponer un escenario de aplicación y desarrollar un prototipo de temática libreque provoque reacciones a partir de la información extraida del rostro. Los detectores proporcionan información del rostro, y de sus elementos faciales. Ideas inmediatas pueden ser filtros, aunque no hay limitaciones en este sentido. La entrega debe venir acompañada de un gif animado o vídeo de un máximo de 30 segundos con momentos seleccionados de la propuesta. Se utilizará para una posterior votación y elección de las mejores entre el grupo.

#### **Filtro Minecraft**
He aplicado un filtro a las caras detectadas que superpone la imagen del personaje principal de Minecraft, "Steve". El objetivo de este filtro es aprovechar la detección en cada fotograma para que el usuario pueda jugar un minijuego. En este juego, desde la parte superior de la pantalla caerán dinamita y diamantes.

El jugador deberá esquivar la dinamita moviendo su cabeza; si es alcanzado, perderá 1 punto de vida. En cambio, si recoge un diamante, ganará 1 punto de vida. La meta del minijuego es evitar llegar a 0 de vida, lo cual provocará un "Game Over". En caso de que esto suceda, aparecerá el mensaje de "Game Over" y el programa se detendrá automáticamente tras 2 segundos. Además, el jugador puede presionar la tecla "q" en cualquier momento para salir del programa y terminar la partida con un "Game Over".

#### **Filtro Gigachad**
Este filtro utiliza tres imágenes distintas: dos para las cejas y una para la barba, con el objetivo de recrear la apariencia del meme "Gigachad". Se añade música de fondo característica del meme para mejorar la experiencia. Para lograr el efecto, se utiliza una función de superposición que coloca las imágenes en los puntos correspondientes a las cejas y el mentón de la cara detectada. Además, se aplica un filtro en escala de grises a la imagen para completar el estilo del meme.

#### **Filtro Majin**
Este filtro utiliza las dos imágenes de cejas del filtro anterior y añade una imagen de la marca "Majin" de la serie Dragon Ball Z. Emplea la misma función de superposición para posicionar las cejas y la marca en los puntos adecuados de la cara detectada. El filtro solo se activará cuando detecte que la persona está sonriendo. Para ello, se analiza la distancia horizontal entre las comisuras de la boca y la distancia vertical entre el centro superior e inferior de la boca; si la altura es pequeña en comparación con el ancho, se detecta una sonrisa y el filtro se activa.

#### **Videos/Imagenes**

1.- Filtro Minecraft

![ImagenMinecraft](https://github.com/user-attachments/assets/26e2f1bd-55b9-46dc-9c5d-3a91fdfc2b70)

https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/ETfr8HjOHUVBhweuHZ_JMOsB0YpqqV58j-T_864R3718sA?e=4NGfhO&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

2.- Filtro Majin

![WhatsApp Image 2024-11-12 at 13 29 16](https://github.com/user-attachments/assets/8210db77-926b-4223-92f8-75acf4c840f7)

![VideoFiltro2](https://github.com/user-attachments/assets/7c4f14ff-72ce-40dc-8d67-6f613e50534c)

3.- Filtro Gigachad

![WhatsApp Image 2024-11-12 at 13 29 16 (1)](https://github.com/user-attachments/assets/b029f6df-39dd-46a5-8701-e0e8338f31fb)

https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/antonio_sanchez120_alu_ulpgc_es/EXGk9oj5ZBJHiuGLDRWUFK4BnAVp0JlfjP2FQKcccRX7nw?e=neBIWr&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

#### **Referencias**

- https://chatgpt.com/
- http://dlib.net/python/index.html



