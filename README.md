# Sismo-XAI: Predicción Sísmica con Inteligencia Artificial Explicable en Cuba

[span_34](start_span)[span_35](start_span)Este proyecto presenta un modelo de **Deep Learning** basado en la arquitectura **PhaseNet (U-Net)** para la detección automática de ondas P y eventos sismológicos[span_34](end_span)[span_35](end_span). [span_36](start_span)[span_37](start_span)[span_38](start_span)Se enfoca específicamente en los registros de la **Estación Río Carpintero (RCC)** del **CENAIS**[span_36](end_span)[span_37](end_span)[span_38](end_span).

## 🚀 Objetivo
[span_39](start_span)[span_40](start_span)[span_41](start_span)Desarrollar una herramienta transparente que no solo detecte sismos con alta precisión, sino que utilice **XAI (Explainable AI)** para mostrar a los especialistas qué patrones de la señal activaron la alerta[span_39](end_span)[span_40](end_span)[span_41](end_span).

## 🛠️ Tecnologías
- **[span_42](start_span)[span_43](start_span)Core:** Python, TensorFlow/Keras, PyTorch[span_42](end_span)[span_43](end_span).
- **[span_44](start_span)Sismología:** ObsPy (procesamiento SAC), SeisBench (modelos pre-entrenados)[span_44](end_span).
- **[span_45](start_span)XAI:** SHAP, LIME, Captum (Grad-CAM)[span_45](end_span).
- **[span_46](start_span)Entorno:** Kaggle Notebooks con aceleración por GPU[span_46](end_span).
- **Metodología:** Desarrollo Ágil con Extreme Programming (XP).

## 📊 Datos
- **[span_47](start_span)Dataset de Entrenamiento:** STEAD (Stanford Earthquake Dataset)[span_47](end_span).
- **[span_48](start_span)[span_49](start_span)[span_50](start_span)Datos de Validación:** Señales reales de la red sismológica cubana (CENAIS)[span_48](end_span)[span_49](end_span)[span_50](end_span).

## 🛠️ Instalación y Uso
1. Clonar el repositorio: `git clone https://github.com/usuario/Sismo-XAI-Cuba.git`
2. Instalar dependencias: `pip install -r requirements.txt`
3. Ejecutar el notebook en `notebooks/01_pipeline_xai.ipynb`.

## 🎓 Créditos
**[span_51](start_span)[span_52](start_span)Autora:** Madeley Graham León[span_51](end_span)[span_52](end_span)  
**[span_53](start_span)[span_54](start_span)Tutor:** Dr.C Dionis López Ramos[span_53](end_span)[span_54](end_span)  
**[span_55](start_span)[span_56](start_span)Institución:** Universidad de Oriente / CENAIS (Santiago de Cuba)[span_55](end_span)[span_56](end_span).
