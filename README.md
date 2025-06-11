# Telecom X Churn Analysis

**Objetivo**  
Analizar la alta tasa de cancelación de clientes (churn) en Telecom X, identificando patrones y factores críticos que influyen en la evasión para proponer estrategias de retención basadas en datos.

---

## 📂 Estructura del proyecto

telecom-x-churn-challenge-alura/
├── notebooks/
│ ├── 01_extraccion.ipynb # Extracción de datos desde API JSON
│ ├── 02_transformacion.ipynb # Limpieza, ETL y feature engineering
│ ├── 03_eda.ipynb # Análisis exploratorio y visualizaciones
│ └── 04_correlacion.ipynb # Análisis de correlación (extra)
├── data/ # Carpeta para datos brutos (vacía)
├── README.md # Documentación del proyecto
└── requirements.txt # pandas, numpy, matplotlib, scikit-learn, requests

yaml
Copiar

---

## ⚙️ Instalación y ejecución

1. Clonar el repositorio y entrar en la carpeta:
   ```bash
   git clone https://github.com/crox5/telecom-x-churn-challenge-alura.git
   cd telecom-x-churn-challenge-alura
(Opcional) Crear un entorno virtual e instalar dependencias:

bash
Copiar
python -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate      # Windows
pip install -r requirements.txt
Abrir y ejecutar los notebooks en orden (Colab o local):

01_extraccion.ipynb

02_transformacion.ipynb

03_eda.ipynb

04_correlacion.ipynb

🛠️ Pasos Técnicos
Extracción

Carga de datos JSON desde la API de Telecom X.

Transformación & ETL

Renombrado de columnas (customer.tenure→Tenure, CargoMensual→MonthlyCharge, etc.).

Conversión de binarios (Yes/No) y de Churn a 0/1.

Creación de features:

DailyCharge = MonthlyCharge/Tenure

tenure_segment ([0–10,11–24,25+ meses])

ServiceCount = número de servicios activos.

Estandarización & Codificación

StandardScaler sobre variables numéricas (Tenure, MonthlyCharge, TotalCharge, DailyCharge).

One-hot encoding de categóricas en df_model.

EDA y Visualizaciones

Perfil de cliente: churn rate por contrato, InternetService, género, pareja, dependientes y edad.

Tiempo de relación: churn vs. Tenure (línea) y por rangos de antigüedad (barras).

Facturación y montos: boxplots e histogramas de cargos y churn rate por método de pago.

Análisis opcional

Matriz de correlación (color-blind friendly) e impacto de ServiceCount.

📊 Ejemplos de gráficos e insights
Distribución de Churn: ~73 % de retención vs. ~27 % de abandono.

Churn por Contract:

Month-to-month ≈ 42 %, Two year ≈ 3 %.

Churn vs Tenure:

40 % en el primer mes, < 5 % tras 24 meses.

DailyCharge: mediana Stay $2.1 vs. Churn $2.7.

PaymentMethod: Electronic check ≈ 44 % churn, pago automático ≈ 12 %.

🔑 Hallazgos Clave
Ventana crítica: primeros 2–3 meses con churn > 40 %.

Contratos cortos: Month-to-month lidera en tasas de abandono.

Fiber optic: churn ≈ 42 %, foco de mejora de experiencia.

Gasto diario elevado: aumenta riesgo de fuga.

Pagos manuales: Electronic/Mailed check presentan churn > 40 %.

Segmentos de riesgo: adultos mayores (65+) y clientes sin familia.

🚀 Recomendaciones
Onboarding intensivo: seguimiento y tutoriales en primeros 90 días.

Incentivos de contrato: descuentos para migrar a planes 1–2 años.

Optimizar fibra óptica: soporte y monitorización proactiva.

Promover pagos automáticos: beneficios para tarjetas/transferencias.

Comunicaciones segmentadas: ofertas específicas para adultos mayores y hogares unipersonales.


*Documentado por crox5 – [GitHub](https://github.com/crox5)*
