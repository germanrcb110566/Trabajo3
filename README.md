Readme.md
Publicacion del Trabajo #3 del Grupo 8 de la materia de Tratamiento de Datos.

# 📊 Análisis de Ventas y Rentabilidad en Retail – Grupo 8

Este repositorio documenta el trabajo práctico de la clase 3, realizado por el Grupo 8. Se analiza el dataset **"Sample – Superstore"**, aplicando técnicas de limpieza, transformación y visualización con Python.

---

## 🎯 Propósito del Dataset

El dataset contiene pedidos de una tienda minorista, con información sobre:

- Fechas de orden y envío
- Modos de envío
- Clientes y segmentos (`Consumer`, `Corporate`, `Home Office`)
- Ubicación geográfica (país, ciudad, estado, región)
- Detalles del producto (categoría, subcategoría, nombre)
- Métricas comerciales: `Sales`, `Quantity`, `Discount`, `Profit`

**Objetivo:** permitir el análisis de desempeño de ventas, rentabilidad por segmento y producto, eficiencia logística y tendencias geográficas/temporales para apoyar decisiones estratégicas.

---

## 🧹 Limpieza y Transformación de Datos

### Importación y configuración
- Librerías utilizadas: `pandas`, `matplotlib.pyplot`, `seaborn`
- Se ajustó el estilo y tamaño de gráficos para mejor lectura

### Formato de fechas
- La columna `Order Date` fue convertida a tipo `datetime`
- Se extrajo el año para facilitar agregaciones temporales

### Filtro temporal
- Se evaluó hacer análisis de los últimos 5 años
- Se encontró que los datos van de **2014 a 2017**, por lo tanto no se aplicó filtro

---

## 📈 Análisis por Segmento de Cliente

### Agrupación y métricas
- Agrupación por `Segment`
- Suma de `Sales` y `Profit`
- Cálculo de `Profit_Margin (%) = (Profit / Sales) * 100`
- Resultados ordenados por ventas

### Visualización
- `sns.barplot()` para comparar ventas por segmento
- Paleta: `Blues_d`
- Se añadieron etiquetas y título con `matplotlib`

---

## 📉 Evolución Anual

### Métricas por año
- Agrupación por año (`Sales`, `Profit`)
- Cálculo del `Profit_Margin (%)`
- Orden cronológico ascendente

### Visualizaciones
- Gráfico de líneas para evolución de ventas (`sns.lineplot`)
  - Color azul, puntos marcados con `marker="o"`
- Gráfico de barras para el margen anual (`sns.barplot`)
  - Paleta: `Purples_d`

---

## 🧠 Principales Hallazgos

- 🔹 El segmento **Consumer** lidera en ventas (~1.2M) pero tiene el margen más bajo (11%)
- 🔹 **Home Office** es el más rentable (14%) pese a menor volumen
- 🔹 **Corporate** equilibra bien ventas y rentabilidad (13%)
- 🔹 Ventas aumentaron un 29 % entre 2015 y 2016
- 🔹 En 2017 hubo un leve declive en ventas y margen

---

## 💡 Insights Estratégicos

- El repunte en 2016–2017 implicó promociones o productos de bajo margen
- Es necesario:
  - Optimizar el mix de productos para elevar el margen
  - Escalar ofertas rentables como Home Office
  - Ajustar precios en el segmento Consumer

---

## 📌 Recomendaciones

- Diseñar un plan para mejorar el margen sin sacrificar volumen
- Replicar tácticas exitosas de 2016 en segmentos menos rentables
- Implementar monitoreo trimestral de ventas vs. margen

---

> ✍️ Este `README` busca documentar y justificar cada paso del análisis, facilitando el aprendizaje compartido y la toma de decisiones basada en datos.

