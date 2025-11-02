# **Personal Finance** - Analyze Financial Habits

Usabilidad de la base de datos: 7.06

Tamaño base de datos: 4.19 MB

Origen base de datos: https://www.kaggle.com/datasets/miadul/personal-finance-ml-dataset/code

---

## **Contexto**

En un mundo donde las decisiones financieras personales impactan directamente en la estabilidad económica de los hogares, comprender los patrones de comportamiento financiero es fundamental. Sin embargo, los datos reales sobre finanzas personales suelen ser sensibles y difíciles de obtener debido a su naturaleza privada.

El Personal Finance ML Dataset ha sido creado para simular de forma sintética (2021 - 2025), pero realista, el comportamiento financiero de personas de diferentes regiones, niveles de ingreso y situaciones crediticias. Este conjunto de datos reproduce de manera real las dinámicas del mundo real, permitiendo analizar hábitos financieros y estudiar la relación entre ingresos, gastos y deudas.

---

## **Objetivo del Proyecto**

El objetivo de este proyecto es realizar un proceso completo de limpieza y análisis exploratorio (EDA) sobre el conjunto de datos del Personal Finance ML Dataset, con el fin de comprender las características principales de la población representada y extraer patrones significativos sobre el comportamiento financiero individual.

De manera provisional, el análisis podría orientarse hacia alguno de los siguientes enfoques:
	•	Evaluar la salud financiera de los individuos según sus ingresos, gastos y nivel de ahorro.
	•	Identificar patrones de riesgo crediticio mediante el estudio del credit_score, debt_to_income_ratio y loan_status.
	•	Segregar perfiles financieros en función de la región, nivel educativo o tipo de préstamo.
	•	Explorar relaciones entre ingresos, ahorros y endeudamiento, generando visualizaciones que faciliten la interpretación.

En una segunda etapa, los resultados del EDA podrán servir como base para desarrollar un modelo de predicción o segmentación, dependiendo del enfoque que finalmente se elija.

---

## **Descripción de los datos**

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


* **pandas**  → Manejo y análisis de datos en formato tabular (DataFrames). Usada para limpieza, transformación y exploración.

* **numpy** → Librería de cálculo numérico eficiente. Soporte a arrays y operaciones matemáticas de base.

* **matplotlib.pyplot** → Visualización de datos. Permite crear gráficos básicos como histogramas, boxplots o scatterplots.

* **seaborn** → Librería de visualización estadística construida sobre matplotlib. Facilita gráficos más atractivos y con análisis exploratorios más rápidos.

* **warnings** → Usada para ignorar mensajes de advertencia y mantener las salidas limpias.

* **Configuración de pandas (pd.options.display.max_columns = None)** → Permite mostrar todas las columnas de un DataFrame sin cortes, facilitando el análisis.

Todas las dependencias se gestionan a través del archivo **`requirements.txt`**, lo que permite instalar el entorno completo con un solo comando:

```bash
pip install -r requirements.txt
```

##  Metodología


## Limpieza de datos


##  Resultados principales Finales del EDA


##  Next Steps


##  Autor

Proyecto desarrollado por Fernando Arroyo como práctica de limpieza y exploración de datos en Python. Todo esto no hubiese sido posible sin la supervición, guí y motivación de uno de los grandes prodijios de la Ciencia de datos, Jean Charles.
	
•	 LinkedIn: www.linkedin.com/in/f-arroyo-herrera