# Análisis de ventas de hipermercados

Proyecto de análisis exploratorio y estadístico sobre datos de ventas de hipermercados. Incluye limpieza, calidad de datos, detección de outliers, visualizaciones y conclusiones orientadas a inventario y estrategia comercial.

**Autor:** Jesús Gustavo Camacho Olivos  
**Versión principal del análisis:** 2.0 (notebook mejorado, abril 2026)

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

## Licencia y uso académico

Si este trabajo forma parte de un curso o entrega, respeta las normas de citación y uso de datos de tu institución.
