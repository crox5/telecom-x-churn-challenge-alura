# Telecom X Churn Analysis

**Propósito del Análisis**
Este proyecto aborda el desafío de la alta tasa de cancelación de clientes (churn) en Telecom X. A través de técnicas de extracción, transformación y análisis exploratorio de datos (EDA), buscamos identificar patrones y factores críticos que influyen en la evasión para proponer estrategias de retención.

## Estructura del Proyecto

```
telecom-x-churn-challenge-alura/
├── notebooks/
│   ├── 01_extraccion.ipynb      # Extracción de datos desde API
│   ├── 02_transformacion.ipynb  # Limpieza, ETL y creación de variables
│   ├── 03_eda.ipynb             # Análisis descriptivo y visualizaciones
│   └── 04_correlacion.ipynb     # Análisis de correlación (extra)
├── data/                        # Carpeta para datos brutos (vacía)
├── README.md                    # Documentación del proyecto
└── requirements.txt             # Dependencias: pandas, matplotlib, requests, scikit-learn
```

## Ejecución

1. Clona el repositorio:

   ```bash
   git clone https://github.com/crox5/telecom-x-churn-challenge-alura.git
   cd telecom-x-churn-challenge-alura
   ```
2. Abre el notebook en Google Colab (o localmente) y ejecuta las celdas en orden:

   1. `01_extraccion.ipynb`
   2. `02_transformacion.ipynb`
   3. `03_eda.ipynb`
   4. `04_correlacion.ipynb`
3. (Opcional) Instala dependencias para entorno local:

   ```bash
   pip install -r requirements.txt
   ```

## Ejemplos de Gráficas e Insights

* **Distribución de Churn:** gráfico de barras que muestra \~73% clientes retenidos vs \~27% churn.
* **Boxplots de Antigüedad y Cargos:** comparativa de `customer.tenure`, `MonthlyCharges`, `TotalCharges` y `Cuentas_Diarias` entre churn y no churn, revelando medianas claramente distintas.
* **Matriz de Correlación:** heatmap anotado con coeficientes, destacando `tenure` (r=–0.35) y `CargoMensual` (r=+0.19) como drivers.
* **Churn vs Número de Servicios:** línea que muestra la tasa de churn según la cantidad de servicios contratados.

## Insights Clave

* **Antigüedad**: a mayor permanencia, menor churn.
* **Precio**: cargos mensuales y diarios altos elevan la tasa de abandono.
* **Plan y servicio**: Month-to-month y Fiber optic presentan churn más elevado.
* **Método de pago**: Electronic check tiene el churn rate más alto (\~45%).

## Próximos Pasos y Modelado

Para la fase de modelado predictivo, se utiliza una copia escalada de los datos (`df_model`) para entrenar algoritmos como regresión logística o árboles de decisión, permitiendo anticipar clientes en riesgo y activar campañas de retención automáticas.

---

*Documentado por crox5 – [GitHub](https://github.com/crox5)*
