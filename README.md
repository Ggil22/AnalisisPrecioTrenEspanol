# Análisis del Precio de los Billetes del Tren de Alta Velocidad Español

Análisis exploratorio de datos (EDA) de los precios de los billetes de Renfe, con el objetivo de entender cómo varían según la ruta, el tipo de tren, la clase y el día de la semana.

## Dataset

Se utiliza el dataset de Kaggle [Spanish High Speed Rail System Ticket Pricing](https://www.kaggle.com/datasets/thegurus/spanish-high-speed-rail-system-ticket-pricing) (`thegurus-opendata-renfe-trips.csv`), del que se cargan ~3,5 millones de registros. Cada registro incluye origen, destino, fechas de salida y llegada, duración, tipo de tren, clase, tarifa y precio.

Las ciudades presentes son **Madrid, Barcelona, Sevilla, Valencia y Ponferrada**.

> El dataset no está incluido en el repositorio por su tamaño. El notebook está preparado para ejecutarse en Kaggle (ruta `../input/...`).

## Contenido del notebook

`AnalisisPreciosTrenAltaVelocidad.ipynb`:

1. **Preparación de los datos**: eliminación de columnas irrelevantes, imputación de precios nulos con la media y eliminación del resto de nulos.
2. **Exploración**:
   - Viajes por ciudad de origen y de destino.
   - Viajes por tipo de tren (AVE, ALVIA, AV City, INTERCITY, REGIONAL…) y por clase (Turista, Turista Plus, Preferente…).
   - Distribución del precio y comparativa de precio por clase y por tipo de tren.
   - Número de viajes, precio medio y recaudación total por día de la semana.
3. **Análisis de rutas desde Madrid**: duración y precio por tipo de tren para Madrid–Barcelona, Madrid–Sevilla, Madrid–Valencia y Madrid–Ponferrada.
4. **Reparto de rutas y tipos de tren** con gráficos interactivos.
5. **Conclusiones**.

## Conclusiones principales

- **Madrid** es con diferencia la ciudad de origen y destino más frecuente, y **Madrid–Barcelona** es la ruta más utilizada.
- El **AVE** es el tipo de tren dominante, al ser el más rápido en casi todas las rutas.
- La clase **Turista** es la más vendida, por ser la tarifa más económica.
- La distribución de precios es bimodal, con la mayoría de billetes entre 30 € y 80 €.
- **Viernes y domingos** concentran más viajes y precios medios más altos, reflejo de la mayor demanda al inicio y final del fin de semana. El sábado es el día con menos actividad.

## Tecnologías

Python · pandas · NumPy · Matplotlib · Seaborn · Plotly

## Cómo ejecutarlo

La forma más sencilla es importar el notebook en Kaggle y añadir el dataset *Spanish High Speed Rail System Ticket Pricing* como entrada.

Para ejecutarlo en local:

```bash
git clone https://github.com/Ggil22/AnalisisPrecioTrenEspanol.git
cd AnalisisPrecioTrenEspanol
pip install pandas numpy matplotlib seaborn plotly scikit-learn lightgbm jupyter
jupyter notebook AnalisisPreciosTrenAltaVelocidad.ipynb
```

Descarga el CSV desde Kaggle y ajusta la ruta de la celda de carga del dataset.

## Autor

**Guillermo Gil Ochoa** — [GitHub](https://github.com/Ggil22)
