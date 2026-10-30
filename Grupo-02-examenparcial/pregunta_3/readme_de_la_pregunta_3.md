# Pregunta 3: Monitoreo de Fauna Silvestre con YOLOv8 en CCT-20

En este módulo implementamos una solución end-to-end para la detección y monitoreo automático de fauna silvestre utilizando el dataset **Caltech Camera Traps 20 (CCT-20)** y la arquitectura de visión por computadora **YOLOv8**.

\---

## 📁 Estructura del Módulo

Debido a las restricciones de tiempo de reentrenamiento completo (que supera 1 hora de cómputo en GPU), la Pregunta 3 se organiza en dos subcarpetas autónomas para facilitar la auditoría y la evaluación rápida por parte del docente:




pregunta_3
├── README.md                              
│
├── pregunta_3_entrenamiento              <-- Módulo de Reentrenamiento Completo (Desde Cero)
│   ├── pregunta3_train.ipynb              <-- Cuaderno de entrenamiento en Kaggle/Colab
│   ├── requirements.txt                   <-- Dependencias de entrenamiento
│   └── README.md                          <-- Instrucciones de reentrenamiento
│
└── pregunta_3_evaluacion_monitoreo       <-- Módulo de Evaluación Rápida y Monitoreo (Recomendado)
    ├── pregunta3_eval.ipynb               <-- Cuaderno/Script de inferencia y métricas
    ├── requirements.txt                   <-- Dependencias ligeras de evaluación
    ├── README.md                          <-- Instrucciones de ejecución en 1 solo comando
    └── runs/yolov8s_cct/weights/best.pt   <-- Pesos optimizados preentrenados
```

\---

## ⚡ Guía de Evaluación Rápida (Para evaluación)

Para la verificación funcional del modelo en tiempo récord sin requerir reentrenamiento completo:

1. Dirígete a la carpeta del módulo de evaluación:

```bash
   cd pregunta_3: pregunta_3_evaluacion_monitoreo
   

2. Ejecuta el comando de instalación y prueba directa estipulado en su respectivo `README.md`:

```bash
   pip install -r requirements.txt \&\& jupyter nbconvert --to notebook --execute pregunta3\_eval.ipynb
   ```

> \*\*Nota:\*\* Para consultar los detalles de la arquitectura, hiperparámetros o replicar el proceso de entrenamiento de la red desde cero, ingresa a la carpeta `pregunta\_3\_entrenamiento/`.

