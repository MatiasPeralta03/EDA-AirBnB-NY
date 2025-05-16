# Análisis de Datos Exploratorio (EDA) | Listados de AirBnB en NY (2024)

Este proyecto realiza un **análisis exploratorio de datos (EDA)** sobre los AirBnB de Nueva York, explorando diferentes patrones, aplicando técnicas de limpieza, visualización y correlación para obtener insights claves sobre la oferta y demanda en la plataforma.

---

## Objetivo del Análisis
El objetivo de este análisis es reponder a diferentes preguntas sobre el mercado de AirBnB en Nueva York:

- ¿Cómo se distribuyen los precios de los alojamientos en distintos vecindarios?  
- ¿Existe una relación entre disponibilidad y número de reseñas?  
- ¿Cuáles son los factores que más influyen en el precio de los listados?  
- ¿Cómo varían los tipos de habitaciones en términos de ubicación y demanda?  

Este análisis es relevante porque permite comprender mejor la oferta y demanda en la plataforma, ofreciendo información valiosa para huéspedes que buscan alojamientos y anfitriones que desean optimizar sus precios.

---

## Dataset ([New York Airbnb Open Data 2024](https://www.kaggle.com/datasets/vrindakallu/new-york-dataset))

El dataset contiene 20.770 filas y 22 columnas, incluyendo variables como:

- `latitude` y `longitude`: ubicación geográfica del alojamiento
- `price`: precio por noche
- `minimum_nights`: cantidad mínima de noches para reservar
- `number_of_reviews`: cantidad total de reseñas
- `reviews_per_month`: promedio de reseñas por mes
- `availability_365`: cantidad de días al año disponibles
- `beds`: cantidad de camas

---

## Herramientas utilizadas

- Python (Pandas - NumPy - Matplotlib - Seaborn)
- Jupyter Notebook

---
## Pasos del Análisis  

### Limpieza de Datos  
Antes de realizar el análisis, se aplicaron técnicas de limpieza para garantizar la calidad de los datos:

- **Eliminación de valores nulos y duplicados** para reducir ruido en el dataset.  
- **Conversión de tipos de datos** para asegurar consistencia en valores categóricos y numéricos.  
- **Detección de outliers** en `price`, utilizando el método del **IQR** para excluir valores extremos.  

---

### Exploración de Datos (EDA)  
Para comprender la estructura del dataset, se analizaron estadísticas descriptivas y tendencias clave.  

- **Distribución de precios** para identificar rangos predominantes y sesgos en los datos.  
- **Patrones de disponibilidad** para entender cuántos días al año los alojamientos están activos.  
- **Número de reseñas** para evaluar la interacción y demanda de los listados.  

Estos análisis previos permitieron detectar relaciones clave antes de la fase de visualización.  

---

### Visualizaciones  

#### **Distribución de Precios**  
- **Histograma con KDE**  
  - Alta concentración de listados en rangos de precios bajos.  
  - Distribución sesgada positivamente, con una minoría de listados caros.  
- **Boxplot**  
  - Muestra la dispersión y presencia de valores atípicos.  
  - La mediana confirma que la mayoría de los precios son accesibles.  
- **Violin Plot**  
  - Refleja la densidad y distribución de los precios, confirmando la existencia de una minoría con precios elevados.  

---

#### **Distribución de Disponibilidad**  
- **Histograma con KDE**  
  - Patrón bimodal: muchos alojamientos tienen baja disponibilidad, mientras que otros están activos todo el año.  
- **Boxplot**  
  - Resalta la variabilidad en la cantidad de días disponibles.  
- **Violin Plot**  
  - Evidencia alta concentración en valores bajos y una cola extendida en disponibilidad completa.  

---

### **Análisis Multivariado**  

#### **Precio vs. Vecindario por Tipo de Habitación**  
- Se observa que **los precios varían significativamente según el vecindario**.  
- **Los alojamientos enteros tienden a ser más costosos**, mientras que las habitaciones privadas y compartidas presentan precios más bajos.  
- En **vecindarios premium**, los precios tienden a ser más elevados.  

---

#### **Precio vs. Número de Reseñas por Grupo de Vecindario**  
- **Mayor cantidad de reseñas está asociada con precios más bajos**, lo que sugiere que alojamientos accesibles generan más interacción.  
- **Los listados caros con muchas reseñas pueden ser alojamientos premium** con alta demanda.  

---

#### **Distribución Geográfica por Tipo de Habitación**  
- Se identifican **zonas con alta concentración de listados**.  
- **Las habitaciones privadas y compartidas predominan en zonas accesibles**, mientras que los alojamientos enteros están más presentes en vecindarios exclusivos.  

---

#### **Heatmap de Correlación**  
- **El precio muestra poca correlación con la mayoría de las variables**, indicando que el costo de los listados depende de múltiples factores externos.  
- **La disponibilidad se relaciona con el número de reseñas**, lo que sugiere que alojamientos activos generan más interacción con huéspedes.  

---

#### **Pairplot: Relaciones Bivariadas**  
- **Distribución de precios, noches mínimas, reseñas y disponibilidad según tipo de habitación**.  
- **Los alojamientos con precios elevados muestran menos reseñas**, indicando posible menor rotación de huéspedes.  

---
---

## Conclusiones

- La mayoría de los alojamientos son de bajo precio, pero existen algunos valores atípicos que elevan el promedio.
- No hay correlación fuerte entre `price` y variables como `beds` o `availability_365`.
- La relación entre `number_of_reviews` y `reviews_per_month` indica que muchas propiedades con reseñas mensuales activas también tienen buen volumen acumulado.
- La dispersión geográfica muestra concentración de precios altos en ciertos puntos (zonas exclusivas o céntricas).

---

## Próximos pasos

- Crear un modelo de predicción de precios con regresión
- Desarrollar un dashboard interactivo con Tableau o Power BI
- Analizar diferencias por tipo de alojamiento (si estuviera disponible la variable)

---
