# 📊 Predecir Ventas con Python (Análisis de Hipermercados)

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Data_Analysis-💡-blue?style=for-the-badge)

## 📌 Título del Proyecto
**Predecir ventas con Python** — Un enfoque predictivo y humano para entender el comportamiento comercial en hipermercados.

---

## 🎯 Desafío (El Problema)
El proyecto aborda la falta de visibilidad detallada sobre el rendimiento comercial y las fluctuaciones de la demanda. Específicamente, se buscaba resolver:
* **Falta de optimización de stock:** Ineficiencia en el control de inventarios debido al desconocimiento de patrones de compra[cite: 3].
* **Incertidumbre comercial:** Dificultad para anticipar tendencias temporales y estacionalidad en las ventas[cite: 3].
* **Decisiones intuitivas:** Necesidad de transformar datos crudos en insights accionables para sustituir las corazonadas por decisiones basadas en evidencia estadística[cite: 3].

---

## ⚙️ Proceso (El Enfoque Técnico)

El problema se abordó mediante un flujo de trabajo riguroso de Ciencia de Datos estructurado en las siguientes fases:

### 1. Stack Tecnológico
* **Manipulación de Datos:** `Pandas` (v3.0.2) y `NumPy` (v2.4.4)[cite: 3].
* **Análisis Estadístico:** `SciPy` (módulo `stats`)[cite: 3].
* **Visualización:** `Matplotlib`, `Seaborn` y `Plotly` para gráficos interactivos[cite: 3].

### 2. Pipeline de Desarrollo
* **Limpieza y Robustez:** Se corrigieron imports incompletos, se parametrizó la ruta del archivo CSV para asegurar la portabilidad del código y se implementó un manejo de excepciones exhaustivo para evitar fallos en la ejecución[cite: 3].
* **Calidad del Dato:** Tratamiento de valores nulos mediante la imputación con la mediana para variables numéricas (evitando el sesgo de outliers) y la moda para variables categóricas[cite: 3].
* **Tratamiento de Outliers:** Identificación de valores atípicos mediante el método del Rango Intercuartílico ($IQR$)[cite: 3].
* **Ingeniería de Características:** Creación de variables dinámicas como `categoria_ventas` basadas en cuartiles para segmentar el rendimiento de los productos[cite: 3].

---

## 🚀 Resultado e Impacto

### 📈 Hallazgos Técnicos y de Negocio
* **Comportamiento de las Ventas:** La distribución de la variable `Sales` presenta un marcado sesgo positivo (asimetría de $12.98$ y curtosis de $304.29$), indicando que la gran mayoría de las transacciones son de bajo valor, pero existen compras de gran volumen que representan picos críticos de ingresos[cite: 3].
* **Valores Atípicos:** Se detectaron $1,145$ outliers en las ventas (equivalentes al $11.68\%$ del dataset)[cite: 3]. Estos no son errores de medición, sino eventos de alta demanda comercial que requieren estrategias de distribución diferenciadas[cite: 3].
* **Eficiencia del Código:** Mediante la conversión inteligente de tipos de datos a variables categóricas, se logró una **optimización de memoria del 82.49%** (reduciendo el dataset de $8.84\text{ MB}$ a solo $1.55\text{ MB}$), asegurando la escalabilidad del script para datasets más grandes[cite: 3].

### 💡 Lecciones Aprendidas
> El análisis de datos no consiste en eliminar lo que "rompe la norma". La detección del $11.68\%$ de outliers demostró que los comportamientos atípicos contienen el verdadero valor estratégico para la toma de decisiones del negocio[cite: 3].

---
Autores: **Jesus Gustavo Camacho Olivos** • Abril 2026[cite: 3]

## Contenido del repositorio

| Archivo | Descripción |
|--------|-------------|
| `S18_VENTAS_HIPERMERCADOS_MEJORADO.ipynb` | Notebook principal: análisis completo con correcciones, validaciones y documentación por secciones. |
| `S18_VENTAS_HIPERMERCADOS.ipynb` | Versión original del análisis (referencia). |
| `train.csv` | Dataset de entrenamiento / análisis (~9.800 filas × 18 columnas). |
| `datos_procesados.csv` | Datos ya procesados (si el flujo los genera o exporta). |
| `requirements.txt` | Todas las dependencias del notebook (datos, visualización, SciPy, Jupyter). |

## Requisitos

- **Python** 3.10 o superior (recomendado).
- **Jupyter** o **VS Code / Cursor** con soporte para notebooks, para ejecutar los `.ipynb`.

## Instalación

### 1. Entorno virtual (recomendado)

```bash
cd S18_PER_VENTAS_HIPERMERCADOS
python -m venv .venv
```

**Windows (PowerShell):**

```powershell
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux:**

```bash
source .venv/bin/activate
```

### 2. Dependencias

Un solo comando instala NumPy, Pandas, Matplotlib, Seaborn, Plotly, SciPy, **openpyxl** (exportación a Excel), Jupyter Notebook e IPython kernel (versiones fijadas en el archivo):

```bash
pip install -r requirements.txt
```

## Uso

1. Activa el entorno virtual (si lo usas).
2. Arranca Jupyter o abre el notebook en el editor:
   ```bash
   jupyter notebook S18_VENTAS_HIPERMERCADOS_MEJORADO.ipynb
   ```
3. Ejecuta las celdas **en orden** desde el principio para mantener la reproducibilidad.
4. **Carga de datos:** en la sección de carga, configura `ruta_datos` para que apunte a tu `train.csv`. Lo más portable es usar ruta relativa al directorio del proyecto, por ejemplo:
   ```python
   ruta_datos = "train.csv"
   ```
   o una variable de entorno si el notebook ya lo contempla.

Si el archivo no se encuentra en la ruta indicada, revisa el mensaje de error en la celda de carga y coloca `train.csv` junto al notebook o ajusta la ruta.

## Qué incluye el análisis (resumen)

- Objetivos: patrones de ventas, productos destacados, tendencias temporales, regiones y categorías, outliers, correlaciones e insights para decisiones.
- Herramientas: Pandas/NumPy, visualizaciones estáticas (Matplotlib/Seaborn) e interactivas (Plotly), estadística con SciPy.

