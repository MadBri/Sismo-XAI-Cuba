# Sismo-XAI: Predicción Sísmica con Inteligencia Artificial Explicable en Cuba

Este proyecto presenta un modelo de **Deep Learning** basado en la arquitectura **PhaseNet (U-Net)** para la detección automática de ondas P y eventos sismológicos. Se enfoca específicamente en los registros de la **Estación Río Carpintero (RCC)** del **CENAIS**.

## 🚀 Objetivo
Desarrollar una herramienta transparente que no solo detecte sismos con alta precisión, sino que utilice **XAI (Explainable AI)** para mostrar a los especialistas qué patrones de la señal activaron la alerta.

## 🛠️ Tecnologías
- **Core:** Python, TensorFlow/Keras, PyTorch.
- **Sismología:** ObsPy (procesamiento SAC), SeisBench (modelos pre-entrenados).
- **XAI:** SHAP, LIME, Captum (Grad-CAM).
- **Entorno:** Kaggle Notebooks con aceleración por GPU.
- **Metodología:** Desarrollo Ágil con Extreme Programming (XP).

## 📊 Datos
- **Dataset de Entrenamiento:** STEAD (Stanford Earthquake Dataset).
- **Datos de Validación:** Señales reales de la red sismológica cubana (CENAIS).

## 🛠️ Instalación y Uso
1. Clonar el repositorio: `git clone https://github.com/usuario/Sismo-XAI-Cuba.git`
2. Instalar dependencias: `pip install -r requirements.txt`
3. Ejecutar el notebook en `notebooks/pipeline_xai.py`.

## 🎓 Créditos
**Autora:** Madeley Graham León
**Tutor:** Dr.C Dionis López Ramos
**Institución:** Universidad de Oriente / CENAIS (Santiago de Cuba).
