# Módulo de Entrenamiento Completo - Pregunta 3

Este módulo contiene el código y la documentación necesaria para replicar el proceso de reentrenamiento completo del modelo YOLOv8 sobre el dataset **Caltech Camera Traps 20 (CCT-20)** para la detección de fauna silvestre.

> **Nota para la evaluación:** Este módulo se incluye por razones de transparencia y reproducibilidad técnica. Dado que el reentrenamiento completo requiere un entorno con GPU (Kaggle/Google Colab) y toma considerable tiempo de cómputo, se recomienda al docente utilizar el módulo `pregunta_3_evaluacion_monitoreo` para una verificación rápida de resultados.

---

## 📁 Contenido de la Carpeta

* `pregunta3_train.ipynb`: Cuaderno Jupyter/Kaggle interactivo utilizado para la descarga del dataset CCT-20, formateo a etiquetas YOLO, configuración de hiperparámetros y fine-tuning del modelo `YOLOv8s`.
* `requirements.txt`: Dependencias requeridas para ejecutar el entrenamiento completo en un entorno local o de nube.

---

## 🚀 Replicación del Entrenamiento

### Requisitos Previos

* Entorno con GPU habilitada (mínimo 8 GB de VRAM recomendados).
* Acceso a los datos de CCT-20 (el cuaderno incluye los scripts automatizados de descarga).

### Instrucción de Ejecución (Comando Único)

Si se desea ejecutar el reentrenamiento completo en local:

```bash
pip install -r requirements.txt && jupyter nbconvert --to notebook --execute pregunta3_train.ipynb
```

### Configuración del Entrenamiento

* **Modelo Base:** `yolov8s.pt`
* **Épocas:** 30
* **Tamaño de Imagen:** 640x640
* **Optimizador:** Auto (SGD/AdamW)
* **Salida de Pesos:** Los mejores pesos generados por este pipeline se exportan a la ruta `runs/yolov8s_cct/weights/best.pt` para su uso en el módulo de evaluación.