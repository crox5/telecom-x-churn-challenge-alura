# Telecom X Churn Analysis

Análisis de evasión de clientes (churn) para Telecom X, realizado en Python con Pandas y Matplotlib.

## Estructura del repositorio

* `notebooks/01_extraccion.ipynb` – Extracción y ETL inicial.
* `notebooks/02_transformacion.ipynb` – Limpieza, transformación y creación de variables.
* `notebooks/03_eda.ipynb` – Análisis descriptivo completo y gráficos.
* `notebooks/04_correlacion.ipynb` – Análisis de correlación (extra).
* `data/` – Carpeta para datos brutos o descargas.
* `requirements.txt` – Librerías necesarias:

  ```
  pandas
  matplotlib
  requests
  scikit-learn
  ```

## Cómo ejecutar

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/crox5/telecom-x-churn-challenge-alura.git
   cd telecom-x-churn-challenge-alura
   ```
2. Abrir los notebooks en Google Colab o localmente y ejecutar las celdas en orden:

   * `01_extraccion.ipynb` → `02_transformacion.ipynb` → `03_eda.ipynb` → `04_correlacion.ipynb`
3. (Opcional) Instalar dependencias localmente:

   ```bash
   pip install -r requirements.txt
   ```

## Contenido de los notebooks

1. **Extracción**: carga de datos desde la API y creación del DataFrame.
2. **Transformación**: limpieza de nulos, mapeo de categorías, creación de `Cuentas_Diarias`.
3. **EDA**:

   * Estadísticas básicas (media, mediana, desviación).
   * Distribución de churn.
   * Tasa de churn por variables categóricas.
   * Comparación de variables numéricas vs churn.
4. **Correlación (extra)**: matriz de correlación y análisis del número de servicios.

## Resultados clave

* **Antigüedad** protege contra el churn (r = –0.35); churners son nuevos (<12 meses).
* **Cargos mensuales** y **diarios** altos asocian a mayor churn (r ≈ +0.19).
* **Contratos** mensuales y **Fiber optic** muestran churn elevados.
* **Electronic check** tiene churn rate más alto (\~45 %).

## Recomendaciones

1. Ofrecer incentivos durante los primeros 3–6 meses.
2. Promover planes de 1–2 años con beneficios exclusivos.
3. Incentivar pagos automáticos (tarjeta/transferencia).
4. Mejorar la experiencia del servicio Fiber optic.
5. Segmentar comunicaciones para seniors y nuevos clientes.

---

*Documentado por crox5 – [GitHub](https://github.com/crox5)*
