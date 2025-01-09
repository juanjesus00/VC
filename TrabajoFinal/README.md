# Análisis de Ejecución de Ejercicios

Este proyecto es un programa innovador diseñado para analizar la ejecución de ejercicios clave como **peso muerto**, **sentadillas** y **press banca**, utilizando análisis de video. El sistema proporciona una evaluación detallada de la técnica del usuario para mejorar el rendimiento y la seguridad en el entrenamiento.

## Tabla de Contenidos

1. [Introducción](#introducción)
2. [Objetivos](#objetivos)
3. [Diseño](#diseño)
4. [Arquitectura](#arquitectura)
5. [Funcionalidades](#funcionalidades)
6. [Conclusiones](#conclusiones)
7. [Cómo Contribuir](#cómo-contribuir)
8. [Licencia](#licencia)

## Introducción

El programa analiza ejercicios clave para ofrecer información valiosa que permita a los usuarios mejorar su rendimiento y técnica mediante el uso de análisis de video.

## Objetivos

Los objetivos principales del programa son:

- **Evaluar extensiones y contracciones musculares**.
- **Medir el rango de movimiento (ROM)**.
- **Calcular la velocidad de ejecución**.
- **Contar repeticiones**.
- **Estimar el Repetición Máxima (RM)**.

## Diseño

La interfaz principal de la aplicación incluye:

![image](https://github.com/user-attachments/assets/506c2263-8417-402b-a462-73b2a719f880)
![video](https://alumnosulpgc-my.sharepoint.com/:v:/g/personal/juan_suarez139_alu_ulpgc_es/ET1kIKbAkfBJpMxXAUY9ZFUBoE1ApLerM4o4lGNbviMyXg?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=MDVlGB)

- **Selección de archivo**: Permite seleccionar videos de entrenamiento.
- **Selección de ejercicio**: Opción para escoger entre peso muerto, sentadillas y press banca.
- **Selección de pesos**: Campo para ingresar el peso utilizado en el video.
- **Generación**: Botón para ejecutar el análisis.
- **Resultados**: Presentación de los resultados, incluyendo RM, velocidad media y conteo de repeticiones.

## Arquitectura

La arquitectura del proyecto sigue el patrón **Model-View-Controller (MVC)**:

- **Vista (View)**: Responsable de la interfaz de usuario, mostrando datos y capturando entradas.
- **Controlador (Controller)**: Actúa como intermediario, gestionando las interacciones del usuario y coordinando la lógica entre la vista y el modelo.
- **Modelo (Model)**: Encapsula la lógica de negocio, procesando datos de entrada para generar resultados.

Esta arquitectura permite una separación clara de responsabilidades, facilitando la escalabilidad y mantenimiento del código.

## Funcionalidades

El proyecto incluye las siguientes funcionalidades:

- **Detección de ejercicios**: Detecta los 3 tipos de ejercicios (peso muerto, sentadillas y press banca).
- **Evaluación del ejercicio**: Proporciona una nota estimada en base a extensiones, contracciones y ROM.
- **Cálculo del RM**: Estima el Repetición Máxima.
- **Velocidad media**: Mide la rapidez de la ejecución del ejercicio.
- **Conteo de repeticiones**: Cuenta las repeticiones realizadas durante el ejercicio.

## Conclusiones

El uso de modelos preentrenados proporciona una base sólida para el análisis inicial. Sin embargo, la precisión se puede mejorar mediante el desarrollo de un dataset propio, optimizado para los ejercicios específicos.

## Cómo Contribuir

Las contribuciones son bienvenidas. Para contribuir:

1. Haz un **fork** del repositorio.
2. Crea una rama para tus cambios (`git checkout -b feature/nueva-funcionalidad`).
3. Confirma tus cambios (`git commit -m 'Añadir nueva funcionalidad'`).
4. Haz **push** a la rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un **Pull Request**.
