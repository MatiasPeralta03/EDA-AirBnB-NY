# 🏡 Exploratory Data Analysis de Alojamientos

Este proyecto realiza un **análisis exploratorio de datos (EDA)** sobre un conjunto de datos de alojamientos (Airbnb-style), aplicando técnicas de limpieza, visualización y correlación entre variables clave.

---

## 📁 Dataset

El dataset incluye variables como:

- `latitude` y `longitude`: ubicación geográfica del alojamiento
- `price`: precio por noche
- `minimum_nights`: cantidad mínima de noches para reservar
- `number_of_reviews`: cantidad total de reseñas
- `reviews_per_month`: promedio de reseñas por mes
- `availability_365`: cantidad de días al año disponibles
- `beds`: cantidad de camas

---

## ⚙️ Herramientas utilizadas

- Python (Pandas, NumPy)
- Visualización: Matplotlib, Seaborn
- Jupyter Notebook

---

## 🧹 Limpieza de Datos

- Eliminación de valores nulos en columnas críticas (`reviews_per_month`, `beds`)
- Conversión de tipos de datos (por ejemplo, fechas si aplicara)
- Detección y eliminación de *outliers* en columnas como `price` y `minimum_nights` usando IQR

---

## 📊 Análisis y Visualizaciones

1. **Distribución del precio**
   - Gráfico de histograma revela fuerte sesgo a la derecha.
   - Se aplicó log-transform para visualizar mejor.

2. **Scatter Plot: Precio vs Latitude / Longitude**
   - Permite observar si hay zonas geográficas con mayor concentración de precios altos.
   - Algunas regiones muestran precios desproporcionadamente altos → *potenciales outliers*.

3. **Mapa de calor de correlaciones**
   - Matriz de correlación entre variables numéricas.
   - Revela una correlación moderada entre:
     - `number_of_reviews` y `reviews_per_month` (`r ≈ 0.63`)
   - Las demás correlaciones son bajas o nulas (|r| < 0.1).

4. **Boxplots para detectar outliers**
   - `price` y `minimum_nights` tienen valores extremos que fueron filtrados.

---

## 📌 Conclusiones

- La mayoría de los alojamientos son de bajo precio, pero existen algunos valores atípicos que elevan el promedio.
- No hay correlación fuerte entre `price` y variables como `beds` o `availability_365`.
- La relación entre `number_of_reviews` y `reviews_per_month` indica que muchas propiedades con reseñas mensuales activas también tienen buen volumen acumulado.
- La dispersión geográfica muestra concentración de precios altos en ciertos puntos (zonas exclusivas o céntricas).

---

## 🚀 Próximos pasos

- Crear un modelo de predicción de precios con regresión
- Desarrollar un dashboard interactivo con Tableau o Power BI
- Analizar diferencias por tipo de alojamiento (si estuviera disponible la variable)

---
