# **Personal Finance** - Analyze Financial Habits

## **Contexto**

En un mundo donde las decisiones financieras personales impactan directamente en la estabilidad económica de los hogares, comprender los patrones de comportamiento financiero es fundamental. Sin embargo, los datos reales sobre finanzas personales suelen ser sensibles y difíciles de obtener debido a su naturaleza privada.

El Personal Finance ML Dataset ha sido creado para simular de forma sintética (2021 - 2025), pero realista, el comportamiento financiero de personas de diferentes regiones, niveles de ingreso y situaciones crediticias. Este conjunto de datos reproduce de manera real las dinámicas del mundo real, permitiendo analizar hábitos financieros y estudiar la relación entre ingresos, gastos y deudas.

---

## **Objetivo del Proyecto**

El objetivo de este proyecto es realizar un proceso completo de limpieza y análisis exploratorio (EDA) sobre el conjunto de datos del Personal Finance ML Dataset, con el fin de comprender las características principales de la población representada y extraer patrones significativos sobre el comportamiento financiero individual.

En este caso, el análisis se ha centrado en un estudio demográfico y geográfico de la situación financiera de los individuos, explorando cómo variables como la edad, el género, el nivel educativo y la región influyen en indicadores económicos clave como el nivel de endeudamiento (debt_to_income_ratio), el puntaje crediticio (credit_score), el nivel de ahorro (savings_usd) y la proporción ahorro-ingreso (savings_to_income_ratio).

El propósito de este enfoque es detectar patrones de estabilidad o riesgo financiero entre distintos grupos poblacionales y regiones, permitiendo obtener una visión más completa del estado financiero global representado en los datos.

En futuras etapas, este análisis podría ampliarse con técnicas de segmentación o modelado predictivo, orientadas a identificar perfiles de riesgo crediticio, estimar la salud financiera individual o desarrollar modelos de recomendación financiera.

---

## **Descripción de los datos**

Usabilidad de la base de datos según Kaggle: 7.06

Tamaño base de datos: 4.19 MB

Origen base de datos: https://www.kaggle.com/datasets/miadul/personal-finance-ml-dataset/code

El dataset contiene 32.424 registros individuales (filas), donde cada fila representa el perfil financiero de una persona. Los datos incluyen información demográfica, económica, crediticia y temporal, con el objetivo de reflejar la diversidad de comportamientos financieros a nivel global.

* **user_id**: Identificador único que representa a cada individuo.
* **age**: Edad del individuo, expresada en años (rango de 18 a 70).
* **gender**: Género del individuo: Masculino, Femenino u Otro.
* **education_level**: Nivel educativo más alto alcanzado (por ejemplo, Secundaria, Grado, Máster o Doctorado).
* **employment_status**: Situación laboral actual del individuo (por ejemplo, Empleado, Desempleado, Estudiante, Jubilado).
* **job_title**: Puesto de trabajo o cargo desempeñado.
* **monthly_income_usd**: Ingreso mensual aproximado en dólares estadounidenses.
* **monthly_expenses_usd**: Gastos mensuales aproximados en dólares estadounidenses.
* **savings_usd**: Total de ahorros acumulados por el individuo.
* **has_loan**: Indica si el individuo tiene un préstamo activo: Sí o No.
* **loan_type**: Tipo de préstamo asociado, en caso de tenerlo (por ejemplo, personal, hipotecario, automotriz o educativo).
* **loan_amount_usd**: Monto total del préstamo en dólares estadounidenses.
* **loan_term_months**: Duración del préstamo expresada en meses.
* **monthly_emi_usd**: Cuota mensual del préstamo (EMI, Equated Monthly Installment).
* **loan_interest_rate_pct**: Tasa de interés anual aplicada al préstamo, expresada en porcentaje.
* **debt_to_income_ratio**: Relación entre los pagos de deuda y los ingresos del individuo (DTI).
* **credit_score**: Puntuación crediticia sintética en una escala de 300 a 850.
* **savings_to_income_ratio**: Relación entre los ahorros y los ingresos anuales del individuo.
* **region**: Región geográfica en la que reside el individuo.
* **record_date**: Fecha de registro de la información financiera.

---

##  Estructura del Repositorio
```bash
Big-4-Financial-Risk-Insights-2020-2025/
│
├── data/                           # Carpeta principal de datos
│   ├── raw/                        # Datos originales sin modificar
│   │   └── synthetic_personal_finance_dataset.csv
│   └── processed/                  # Datos limpios y transformados tras la fase de limpieza
│
├── notebooks/                      # Jupyter Notebooks del proyecto
│   ├── 1_primera_aproximacion.ipynb   # Exploración inicial y revisión del dataset
│   ├── 2_data_clean.ipynb             # Limpieza, tratamiento de nulos y formateo de variables
│   └── 3_eda.ipynb                    # Análisis exploratorio y visualización de resultados
│
├── src/                            # Scripts y funciones auxiliares (por ejemplo, limpieza o visualización)
│
├── .gitignore                      # Archivos y carpetas que Git debe ignorar
├── requirements.txt                # Dependencias y librerías necesarias para ejecutar el proyecto
└── README.md                       # Documentación principal del proyecto
```

---

## Librerías y entorno

Este proyecto fue desarrollado en **Python 3.13.0**, utilizando un entorno virtual creado con `venv` para asegurar la reproducibilidad.


* **pandas** → Manejo y análisis de datos en estructuras tabulares (DataFrames). Utilizada para la limpieza, transformación y exploración de datos.
* **numpy** → Soporte para cálculos numéricos, creación de arrays y operaciones matemáticas vectorizadas.
* **matplotlib.pyplot** → Visualización de datos en gráficos básicos como histogramas, boxplots, scatterplots o distribuciones.
* **seaborn** → Visualización estadística avanzada basada en matplotlib. Permite gráficos más claros, estéticos y analíticos.
* **plotly** → Creación de gráficos interactivos y dashboards exploratorios para análisis visuales más dinámicos.
* **folium** → Generación de mapas interactivos y representaciones geográficas (por ejemplo, heatmaps o mapas de densidad por región).
* **warnings** → Control de mensajes de advertencia para mantener salidas limpias en notebooks.
* **sys** → Acceso a funciones del sistema, usado para extender rutas y acceder a módulos del proyecto (src/).
* **Configuración de pandas (pd.options.display.max_columns = None)** → Permite mostrar todas las columnas de un DataFrame sin cortes, facilitando el análisis.

Todas las dependencias se gestionan a través del archivo **`requirements.txt`**, lo que permite instalar el entorno completo con un solo comando:

```bash
pip install -r requirements.txt
```

##  Metodología

El proyecto sigue un enfoque exploratorio y analítico, estructurado en tres fases principales: revisión inicial del dataset, limpieza y preparación de datos, y análisis exploratorio con enfoque demográfico y geográfico.

1️⃣ Revisión inicial de los datos

En esta etapa se exploró la estructura del dataset y se evaluó su usabilidad (7.06/10). Se verificó el tamaño, tipos de variables, valores nulos y duplicados, con el fin de identificar posibles inconsistencias.

Se definieron los primeros Next Steps, orientados a normalizar texto, eliminar columnas redundantes y preparar los datos para su limpieza formal.

2️⃣ Limpieza y transformación de datos

Esta fase se centró en dejar la base lista para el análisis exploratorio.

Las acciones incluyeron:
* Conversión de variables: has_loan a formato booleano y record_date a formato datetime.
* Imputación de valores nulos y formateo de nombres de columnas.
* Revisión y ajuste de tipos de datos (Dtypes).
* Creación de un nuevo archivo limpio (clean_personal_finance_dataset.csv).

3️⃣ Análisis exploratorio (EDA)

En esta última etapa se realizó un análisis descriptivo, demográfico y geográfico.

Se combinaron métricas estadísticas con visualizaciones informativas para interpretar patrones financieros entre distintos grupos.

El análisis se estructuró en dos niveles:

**Análisis general**: revisión de distribuciones, correlaciones y relaciones entre indicadores financieros (ingresos, gastos, ahorros, deudas).

**Análisis demográfico y geográfico**:
* Edad: relación con credit_score, savings_usd, debt_to_income_ratio y savings_to_income_ratio.
* Género: diferencias en ahorro, endeudamiento y puntuación crediticia.
* Nivel educativo: comparación del comportamiento financiero según educación formal.
* Región: análisis económico por zonas con mapas y gráficos de distribución (usando folium, plotly y seaborn).

Los gráficos combinan enfoques estadísticos (boxplots, violines, comparativas de medias/medianas) y geográficos (choropleth maps y heatmaps) para representar las conclusiones de forma visual y accesible.

##  Resultados Finales del EDA

El análisis exploratorio permitió obtener una visión completa del comportamiento financiero de más de **32.000 individuos**, combinando un enfoque **descriptivo, demográfico y geográfico**.  

---

### Análisis general  
Se observaron **distribuciones coherentes y realistas** en las principales métricas financieras.  

- El **Debt-to-Income Ratio (DTI)** tiene una mediana de 0, reflejando que la mayoría de los individuos no presenta deuda activa.  
- El **Credit Score** promedio (575) se sitúa en un rango medio-bajo, indicando perfiles de riesgo moderado.  
- El **Savings-to-Income Ratio** ronda una media de 5, lo que sugiere un nivel de ahorro proporcional al ingreso.  
- Los **ahorros totales (savings_usd)** presentan una fuerte asimetría: la media se ve afectada por valores muy altos, pero la mediana (~201.700 USD) describe mejor la realidad de la mayoría.  

Las correlaciones confirmaron coherencia entre ingresos, gastos y ahorros, sin relaciones fuertes con el score o el endeudamiento.  

---

### Análisis demográfico  
- **Edad:** no se detectan diferencias significativas en deuda, ahorro ni puntaje crediticio. Los valores se mantienen estables a lo largo de todas las edades.  
- **Género:** hombres, mujeres y otros géneros presentan patrones casi idénticos en ahorro, endeudamiento y crédito.  
- **Nivel educativo:** el nivel de estudios no influye de manera clara en el DTI, el crédito o los ahorros. Las medias y medianas se mantienen constantes en todos los grupos.  

---

### Análisis geográfico  
Las regiones muestran **una notable homogeneidad financiera**:  

- El porcentaje de personas con deuda ronda el **40% en todas las zonas**.  
- El ahorro relativo (`savings_to_income_ratio`) y absoluto (`savings_usd`) se distribuyen de forma uniforme entre continentes.  
- Europa y África presentan ligeras ventajas en capacidad de ahorro (≈72% de individuos con más de 100k USD), aunque las diferencias son mínimas.  
- Los puntajes crediticios son prácticamente idénticos entre regiones, sin evidencias de disparidades relevantes.  

---

### Conclusión global  
El conjunto de datos refleja una **población financieramente estable y equilibrada**, sin diferencias marcadas entre grupos demográficos ni regiones.  
Las métricas financieras principales se mantienen consistentes, lo que sugiere un **comportamiento económico homogéneo** a nivel global, lo cual no es muy ideal para futuras segmentaciones por la poca diferencia entre los distintos grupos de población.


##  Next Steps

* Segmentación de usuarios en funión de su salud financiera.
* Modelado de elegibilidad para préstamos.
* Predicción del puntaje crediticio de los usuarios.
* Análisis de gastos y recomendaciones de ahorro.
* Aplicación de machine learning en las finanzas de los usuarios.

##  Autor

Proyecto desarrollado por Roger Fernando Arroyo Herrera como práctica de limpieza de datos y desarrollo exhaustivo de EDA en Python. Todo esto no hubiese sido posible sin la supervición, guía y motivación de dos de los grandes prodijios de la Ciencia de datos, Jean Charles y Ana García.
	
•	 LinkedIn: www.linkedin.com/in/f-arroyo-herrera