 Datos depurados

Esta carpeta contiene los **datasets intermedios** y el **dataset final** generados a partir de los datos originales documentados en `Datos/Base_de_datos_original/`.

## Contenido

- **inmigracion.csv**  
  Stock de inmigrantes por país y año.  
  Variables principales:  
  - `pais`  
  - `anio`  
  - `inmigrantes`  
  - (otras variables auxiliares si aplican, como región o grupo de ingresos)

- **emigracion.csv**  
  Stock de emigrantes por país y año.  
  Variables principales:  
  - `pais`  
  - `anio`  
  - `emigrantes`  
  - (otras variables auxiliares si aplican)

- **migracion_neta.csv**  
  Dataset final resultante de la diferencia entre inmigración y emigración.  
  Variables principales:  
  - `pais`  
  - `anio`  
  - `migracion_neta = inmigrantes – emigrantes`

## Notas
- Estos archivos son el resultado de integrar y procesar los datos originales.  
- Constituyen la base para los análisis, visualizaciones y dashboard del proyecto.  
- No deben ser modificados manualmente: cualquier cambio debe realizarse volviendo a procesar los datos originales.