# Módulo de Evaluación y Monitoreo - Pregunta 3

Este módulo contiene los elementos necesarios para realizar la validación, inferencia y monitoreo de fauna silvestre utilizando la arquitectura YOLOv8 entrenada sobre el dataset CCT-20 (Caltech Camera Traps 20), cumpliendo estrictamente con la ejecución desde cero mediante un único comando.

## 📁 Contenido de la Carpeta

- `pregunta3_eval.ipynb`: Cuaderno Jupyter que carga el modelo preentrenado, realiza inferencias sobre imágenes de prueba y calcula las métricas de rendimiento.
- `requirements_de_evaluacion.txt`: Lista de dependencias y librerías necesarias (incluyendo YOLOv8, OpenCV, etc.).
- `runs/yolov8s_cct/weights/best.pt`: Pesos optimizados y entrenados del modelo `YOLOv8s` listos para su uso directo.

---

## ⚡ Ejecución en un Solo Comando (Requerido para Calificación)

OBSERVACIÓN: EN WINDOWS EJECUTAR EN ANACONDA PROMPT

Para cumplir con la rúbrica de ejecución end-to-end automatizada sin requerir la hora de reentrenamiento, abre tu terminal en esta ruta (`pregunta_3/pregunta_3_evaluacion_monitoreo`) y ejecuta la siguiente instrucción integrada:


python -m pip install -r requirements_de_evaluacion.txt && python -m jupyter nbconvert --to notebook --execute --inplace pregunta3_eval.ipynb


El notebook ejecutado con todas las salidas, tablas y métricas procesadas se guardará automáticamente en:

       Ruta: en el directorio actual del proyecto

       Nombre de archivo: pregunta3_eval.nbconvert.ipynb,  Deberá cargar el archivo en por ejemplo jupyter, donde visualizará el código y las salidas de la ejecución

### ¿Qué hace este comando?
1. **`pip install -r requirements_de_evaluacion.txt`**: Instala de forma automatizada todas las librerías necesarias en tu entorno virtual o local.
2. **`&&`**: Concatena las acciones de manera secuencial.
3. **`jupyter nbconvert --to notebook --execute pregunta3_eval.ipynb`**: Ejecuta de principio a fin el cuaderno de evaluación, procesando las imágenes y generando las salidas del modelo con los pesos `best.pt` incluidos, sin requerir intervención manual.
