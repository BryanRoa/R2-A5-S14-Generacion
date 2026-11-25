# Modelos Generativos: DCGAN y Fine-Tuning de Stable Diffusion (LoRA)

Este repositorio contiene la implementación práctica de dos paradigmas de modelos generativos en Deep Learning, desarrollados como parte de la actividad de la asignatura **DEEP LEARNING -CONCEPTOS**.

## 📂 Contenido del Repositorio

El proyecto está dividido en dos notebooks principales desarrollados en Google Colab:

1. **`Implementación_de_DCGAN_en_PyTorch.ipynb`**
   * Implementación de una Red Generativa Adversaria Convolucional Profunda (DCGAN) desde cero.
   * **Dataset:** Rostros humanos (LFW - Labeled Faces in the Wild).
   * **Objetivo:** Generar rostros sintéticos de 64x64 píxeles a partir de un vector latente (z).

2. **`Fine_Tuning_de_Stable_Diffusion_con_diffusers_y_LoRA.ipynb`**
   * Fine-tuning eficiente del modelo `runwayml/stable-diffusion-v1-5` utilizando la técnica LoRA (Low-Rank Adaptation).
   * **Dataset:** Mini-dataset sintético personalizado (colores sólidos).
   * **Objetivo:** Adaptar el modelo a un nuevo concepto (token `sks_style`) entrenando menos del 0.1% de los parámetros totales.

## 🛠️ Tecnologías y Librerías Utilizadas

* **Lenguaje:** Python 3
* **Deep Learning:** PyTorch
* **Modelos de Difusión:** Hugging Face (`diffusers`, `transformers`, `accelerate`)
* **Fine-Tuning:** PEFT (Parameter-Efficient Fine-Tuning)
* **Procesamiento de Datos:** Scikit-learn, Torchvision, PIL
* **Entorno de Ejecución:** Google Colab (GPU NVIDIA T4)

## 🚀 Cómo ejecutar los notebooks

1. Abre los archivos `.ipynb` directamente en Google Colab.
2. Asegúrate de tener activada la GPU en el entorno de ejecución: `Entorno de ejecución > Cambiar tipo de entorno de ejecución > T4 GPU`.
3. Ejecuta las celdas en orden secuencial. Las librerías necesarias se instalan automáticamente en la primera celda de cada notebook.

## 📊 Resumen de Resultados

* **DCGAN:** Se logró generar rostros con estructuras faciales básicas. La curva de pérdida evidenció una dominancia del Discriminador. El desenfoque visual es consecuencia de la baja resolución (64x64) y las limitadas iteraciones de entrenamiento.
* **Stable Diffusion + LoRA:** El modelo demostró una alta eficiencia en el uso de memoria (797,184 parámetros entrenables). La pérdida MSE mostró convergencia, pero la imagen resultante fue abstracta debido a las características del dataset sintético utilizado y los pocos pasos de entrenamiento (40 pasos).

## 👥 Autores e Información

* **Estudiante:** Bryan Felipe Roa Alvarado
* **Docente:** Nidia Stella García Roa
* **Institución:** Universidad de Cundinamarca
* **Fecha:** 24 de noviembre del 2026

---
*Este repositorio fue creado con fines académicos para evidenciar el proceso de implementación, entrenamiento y análisis de modelos generativos.*
