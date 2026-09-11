# 📈 Análisis Estratégico de Ventas, Marketing y Rentabilidad por Producto

## 🎯 Objetivo del Proyecto
El propósito de este proyecto es consolidar, auditar y analizar de punta a punta la actividad comercial y publicitaria de una compañía a partir de tres fuentes de datos aisladas (`clientes.csv`, `marketing.csv` y `ventas.csv`). 

A través de este desarrollo, se demuestran habilidades avanzadas en la ingeniería de datos, modelado estadístico para la toma de decisiones, análisis de atribución cronológica de campañas y diseño de dashboards ejecutivos para la dirección del negocio.

---

## 🛠️ Tecnologías y Librerías Utilizadas
* **Lenguaje:** Python 3.x
* **Entorno de Trabajo:** Google Colab / Jupyter Notebooks
* **Manipulación de Datos:** `pandas`, `numpy`
* **Visualización Avanzada:** `seaborn`, `matplotlib`
* **Estándares de Calidad:** Adherencia a las directrices **PEP 8** (código limpio, optimización de memoria y centralización de imports).

---

## 🚀 Arquitectura del Proyecto e Impacto Técnico

### 1. Ingesta y Diagnóstico Inicial (EDA)
Se realizó una auditoría estructural exhaustiva por cada DataFrame de forma independiente utilizando métodos como `.info()`, `.duplicated()`, `.isnull()`, y `.describe()`. Esto permitió mapear la metadata original e identificar inconsistencias críticas antes de alterar los sets de datos.

### 2. Curación de Datos (Data Wrangling)
Se aplicó un flujo riguroso de saneamiento que incluyó:
* **Normalización Monetaria:** Remoción de caracteres especiales (`$`) en precios y conversión a tipos flotantes numéricos.
* **Depuración de Duplicados:** Detección y eliminación de **35 registros transaccionales idénticos** mediante `drop_duplicates(ignore_index=True)`, evitando una sobreestimación artificial del **5.8%** en la facturación.
* **Casteo Temporal Nativo:** Conversión de cadenas de texto a objetos cronológicos `datetime64` para habilitar análisis de series de tiempo.

### 3. Analítica Avanzada e Ingeniería de Variables
* **Umbral de Alto Rendimiento:** Implementación del **Percentil 75** sobre los ingresos totales por venta para aislar científicamente los "productos estrella".
* **Atribución Cronológica de Marketing:** Clasificación de transacciones en los estados *Dentro de Campaña* y *Fuera de Campaña* cruzando las fechas de compra contra la vigencia exacta de las pautas publicitarias.
* **Matriz de Rentabilidad (ROI):** Cálculo del Retorno de Inversión Atribuido por categoría y producto específico.

---

## 🎨 Dashboards e Insights Clave Visualizados

El notebook genera visualizaciones corporativas de alto impacto para la toma de decisiones:
1. **Distribución de Ingresos y Curva de Densidad (KDE):** Valida estadísticamente el comportamiento transaccional marcando el límite exacto del Percentil 75.
2. **Impacto Financiero Apilado:** Gráfico que contrasta el volumen gigante de ventas generadas frente al costo publicitario invertido por categoría.
3. **Histograma de Integración Venta & Marketing:** Muestra la frecuencia y comportamiento de compra comparando transacciones bajo pauta vs. orgánicas.
4. **Ranking de Ganancia Neta por Producto:** Identifica con precisión qué artículos específicos lideran el margen neto real de la empresa y cuáles generan pérdidas operativas.

---

## 📈 Conclusiones para la Dirección Ejecutiva

* **Decisiones Basadas en Datos Reales:** La remoción de duplicados y nulos garantizó estados financieros de alta fidelidad para el negocio, previniendo presupuestos inflados.
* **Optimización de Presupuesto:** El análisis granular por producto revela de forma concluyente qué campañas justifican su inversión. Se recomienda reasignar capital de los productos con rendimiento plano hacia aquellos con mayor **ROI Atribuido**.
* **Estrategia Geográfica:** El perfil socio-demográfico permite identificar las ciudades clave con mayor ingreso anual medio para coordinar futuros lanzamientos de pauta geolocalizada.

---
## 💻 Cómo Ejecutar el Proyecto
1. Clona este repositorio o descarga los archivos `.csv`.
2. Sube el archivo `.ipynb` a tu entorno de **Google Colab** o Jupyter Notebook.
3. Asegúrate de actualizar las rutas o URLs de los archivos en la primera celda de código.
4. Ejecuta las celdas de forma secuencial (`Ctrl + F9` en Colab) para renderizar los reportes y gráficos en tiempo real.
