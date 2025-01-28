# Scraper de Precios de Viviendas en Clasipar

Este repositorio contiene un **scraper** en Python para extraer información de precios de viviendas desde el sitio web de Clasipar. El script permite obtener datos de múltiples páginas, limpiarlos y analizarlos con Pandas Profiling.

## Contexto
Si bien se trata de un proyecto sencillo, representa un primer paso importante hacia la obtención de datos para análisis más complejos. Además, en lo personal, este proyecto me ayudó a encontrar la mejor casa en el lugar ideal durante mi búsqueda de vivienda.
El problema que se resolvió con este proyecto es la dificultad de recopilar datos estructurados sobre los precios de viviendas en Paraguay desde plataformas web. Muchos anuncios incluyen precios en diferentes monedas y formatos, lo que dificulta su análisis automático. Este scraper facilita la recopilación y procesamiento de esta información para realizar análisis de mercado de manera eficiente.

## Métodos
Los pasos seguidos en el desarrollo del proyecto incluyen:
1. **Obtención de datos:** Se utiliza `BeautifulSoup` y `requests` para extraer información de Clasipar.
2. **Manejo de errores:** Se implementan reintentos con backoff exponencial para evitar problemas de conexión.
3. **Limpieza de datos:** Se procesan los valores de precios, normalizando las monedas y eliminando información redundante.
4. **Conversión de monedas:** Se convierten los precios en dólares a guaraníes utilizando un factor de conversión.
5. **Análisis exploratorio:** Se genera un reporte detallado con `ydata-profiling` para visualizar tendencias y distribuciones.

## Resultados
- Se obtuvo un **DataFrame** estructurado con las columnas `Ciudad`, `Precio_Gs`, `Precio_USD`, facilitando su análisis.
- Se eliminaron inconsistencias en los precios y ubicaciones, asegurando datos más limpios y usables.
- Se generaron **visualizaciones** que muestran la distribución de precios por ciudad y un resumen estadístico de los datos extraídos.
- Se logró automatizar el proceso de recopilación y análisis de precios de viviendas en Paraguay, evitando la necesidad de recopilación manual.

## Aprendizaje
- Se descubrió que muchos anuncios incluyen información de precios con formatos inconsistentes, lo que requirió una mejor estrategia de limpieza.
- Se mejoró la eficiencia del scraping al permitir configurar dinámicamente el número de páginas a extraer.
- Se podría optimizar aún más el procesamiento de datos incorporando técnicas de detección de valores atípicos más avanzadas.
- Se podría expandir el scraper para incluir otras plataformas similares y mejorar el análisis comparativo de precios entre sitios.

## Requisitos
Antes de ejecutar el script, instala las dependencias necesarias:

```bash
pip install requests beautifulsoup4 pandas numpy fake-useragent ydata-profiling
```

## Uso
Ejecuta el script con:

```bash
python scraper_original_mejorado.py
```

Puedes cambiar el número de páginas a extraer modificando la variable `num_paginas` en el script:

```python
num_paginas = 10  # Cambia el número de páginas según sea necesario
```

## Salida
El script generará:
- Un **DataFrame** con las columnas `Ciudad`, `Precio_Gs`, `Precio_USD`.
- Un **reporte exploratorio** en la notebook si se ejecuta en un entorno Jupyter.

## Contacto
Si tienes sugerencias o mejoras, siéntete libre de contribuir o contactarme. ¡Espero que este scraper te sea útil! 🚀

