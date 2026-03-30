Pipeline principal de entrenamiento y explicabilidad XAI.


import obspy
import numpy as np
import matplotlib.pyplot as plt
import seisbench.models as sbm
import shap
import torch
from obspy.clients.fdsn import Client

# 1. [span_21](start_span)[span_22](start_span)CARGA DE DATOS SAC (Simulación con ObsPy)[span_21](end_span)[span_22](end_span)
def load_rcc_data(file_path):
    st = obspy.read(file_path)
    [span_23](start_span)st.filter('bandpass', freqmin=1.0, freqmax=45.0) # Preprocesamiento[span_23](end_span)
    [span_24](start_span)st.resample(100.0) # Frecuencia de muestreo 100Hz[span_24](end_span)
    return st[0].data

# 2. [span_25](start_span)[span_26](start_span)CARGA DE MODELO PHASENET (U-Net)[span_25](end_span)[span_26](end_span)
model = sbm.PhaseNet.from_pretrained("stead")
model.eval()

# 3. [span_27](start_span)[span_28](start_span)PREDICCIÓN[span_27](end_span)[span_28](end_span)
# Nota: PhaseNet espera ventanas de 3000 muestras (30s a 100Hz)
sample_data = np.random.randn(1, 3, 3000).astype(np.float32) # Dummy para ejemplo
with torch.no_grad():
    predictions = model(torch.tensor(sample_data))

# 4. [span_29](start_span)[span_30](start_span)[span_31](start_span)EXPLICABILIDAD CON SHAP[span_29](end_span)[span_30](end_span)[span_31](end_span)
# Usamos un integrador de gradientes para series temporales
explainer = shap.GradientExplainer(model, torch.tensor(sample_data))
shap_values = explainer.shap_values(torch.tensor(sample_data))

# 5. [span_32](start_span)[span_33](start_span)VISUALIZACIÓN[span_32](end_span)[span_33](end_span)
plt.figure(figsize=(12, 6))
plt.subplot(2, 1, 1)
plt.plot(sample_data[0, 0, :], label='Señal RCC (Z)')
plt.title('Detección de Onda P - Estación Río Carpintero')
plt.subplot(2, 1, 2)
plt.plot(shap_values[0][0, 0, :], color='red')
plt.title('Importancia de Atributos (SHAP Value)')
plt.tight_layout()
plt.show()
