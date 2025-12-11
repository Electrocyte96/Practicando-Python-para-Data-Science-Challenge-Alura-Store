# Practicando Python para Data Science — Alura Store (Breve resumen)

Este README resume el notebook `AluraStoreLatam.ipynb` (fuente) que realiza un análisis exploratorio de ventas de cuatro tiendas de ejemplo, usando las bases públicas del challenge de Alura.

Notebook fuente:
https://github.com/Electrocyte96/Practicando-Python-para-Data-Science-Challenge-Alura-Store/blob/7b5e992a5b38200d5699ac47e1404f270226e026/AluraStoreLatam.ipynb

## Objetivo
Realizar análisis de facturación y ventas por categoría para 4 tiendas (conjuntos de datos CSV) y presentar visualizaciones y tablas que permitan comparar ingresos y distribución por categorías.

## Datos
Los datos se cargan desde los CSV públicos del challenge (raw GitHub):
- tienda_1.csv
- tienda_2.csv
- tienda_3.csv
- tienda_4.csv

Columnas principales (muestra en el notebook):
- Producto
- Categoría del Producto
- Precio
- Costo de envío
- Fecha de Compra
- Vendedor
- Lugar de Compra
- Calificación
- Método de pago
- Cantidad de cuotas
- lat, lon

(En el notebook se muestra un head() con filas de ejemplo).

## Dependencias
Usa las bibliotecas:
- pandas
- matplotlib
- seaborn
- math

Instalación rápida:
```bash
pip install pandas matplotlib seaborn
```

## Análisis y resultados clave
1. Análisis de facturación:
   - Se calculan los ingresos totales por tienda (suma de la columna Precio).
   - Ingresos observados (aprox):
     - Tienda 1: 1,150,880,400.00
     - Tienda 2: 1,116,343,500.00
     - Tienda 3: 1,098,019,600.00
     - Tienda 4: 1,038,375,700.00
   - Se genera un gráfico de barras comparando ingresos por tienda.

2. Ventas por categoría:
   - Se agrupan las ventas por "Categoría del Producto" y se suman los precios por categoría para cada tienda.
   - Las categorías con mayor facturación (por rango observado en las 4 tiendas) son, en orden aproximado:
     1. Electrónicos (rondas de cientos de millones por tienda)
     2. Electrodomésticos
     3. Muebles
   - Se concatena la información de las 4 tiendas y se dibuja un gráfico de barras apiladas/comparativas por categoría.

En el notebook también se muestran las tablas resultantes (`ventas_tiendas`) con valores numéricos por categoría y tienda.

## Visualizaciones
- Gráfico de barras: Ingresos por tienda.
- Gráfico de barras: Ventas por categoría (comparación entre tiendas).
Las figuras se generan con matplotlib / pandas plotting (y se pueden refinar con seaborn).

## Cómo reproducir
1. Clona el repositorio y abre el notebook:
   ```bash
   git clone https://github.com/Electrocyte96/Practicando-Python-para-Data-Science-Challenge-Alura-Store.git
   cd Practicando-Python-para-Data-Science-Challenge-Alura-Store
   jupyter notebook AluraStoreLatam.ipynb
   ```
2. O ejecuta el notebook con nbconvert:
   ```bash
   jupyter nbconvert --to notebook --execute AluraStoreLatam.ipynb
   ```

## Notas
- El notebook es un análisis exploratorio (EDA) orientado a practicar agregaciones, agrupamientos y visualizaciones.
- Si quieres, puedo:
  - Generar un README más detallado con tablas y capturas de las figuras (incluir imágenes exportadas desde el notebook).
  - Cometer el README.md al repo en una rama específica. Indica rama y si puede sobrescribir README.md existente.