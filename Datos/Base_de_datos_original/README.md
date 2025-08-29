 # Datos originales — Migración Internacional

Este directorio contiene los **datos originales** descargados de la fuente oficial antes de cualquier procesamiento.

## Fuente 

- **Fuente utilizada**: dataset integrado en el repositorio abierto [Gapminder / open-numbers](https://github.com/open-numbers/ddf--unpop--international_migrant_stock)  
- **Fecha de descarga**: agosto 2025  

## Archivos incluidos
- `ddf--entities--geo--country.csv` → listado de países y regiones con metadatos (códigos ISO, nombres, clasificaciones).  
- `ddf--datapoints--immigrant_stock--by--geo--year.csv` → stock de inmigrantes por país y año.  
- `ddf--datapoints--emigrant_stock--by--geo--year.csv` → stock de emigrantes por país y año.  

## Flujo reproducible

- Usar estas bases de datos originales como entrada.
- La limpieza y transformación se hace en el script [`Datos/Codigo_depuracion/depuracion_script.Rmd`]
- Los resultados de la depuración se guardan en `Datos/Base_de_datos_depurada/`.



