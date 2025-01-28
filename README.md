# Scraper de Precios de Viviendas en Clasipar

Este repositorio contiene un **scraper** en Python para extraer información de precios de viviendas desde el sitio web de Clasipar. El script permite obtener datos de múltiples páginas, limpiarlos y analizarlos con Pandas Profiling.

## Características
- **Extracción de datos web** usando `BeautifulSoup` y `requests`.
- **Manejo de errores y reintentos** para evitar fallos de conexión.
- **Procesamiento y limpieza de datos**, incluyendo conversión de monedas.
- **Análisis exploratorio** con `ydata-profiling`.
- **Número de páginas configurable** para mayor flexibilidad.

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

