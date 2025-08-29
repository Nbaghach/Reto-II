# Datos depurados

Esta carpeta contiene los **datasets intermedios** y el **dataset final** generados a partir de los datos originales documentados en [`Datos/Base_de_datos_original/`](../Base_de_datos_original/).  
Los archivos aquí presentes son el resultado directo del script de depuración (`depuracion_script.Rmd`).

---

## Contenido

- **immigrants.csv**  
  Stock de inmigrantes por país y año (**dataset intermedio**).  

  **Variables principales:**  
  - `iso3` → código ISO Alpha-3 del país  
  - `country_name` → nombre del país  
  - `year` → año de referencia  
  - `immigrants` → stock de inmigrantes  
  - + metadatos auxiliares (regiones, ingresos, etc.)

- **emigrants.csv**  
  Stock de emigrantes por país y año (**dataset intermedio**).  

  **Variables principales:**  
  - `iso3`, `country_name`, `year`  
  - `emigrants` → stock de emigrantes  
  - + metadatos auxiliares

- **migracion_neta.csv**  
  Dataset **intermedio** con la migración neta = `immigrants - emigrants`.  
  Incluye duplicados y columnas adicionales, por lo que **no debe usarse para análisis finales**.

- **migracion_neta_limpio.csv**  
  **Dataset final del proyecto** (depurado y estandarizado).  

  **Variables principales:**  
  - `iso3`, `country_name`, `year`  
  - `immigrants`, `emigrants`, `net_migration`  
  - `region4`, `region6`  
  - `income_groups`  
  - `g77_ocde`  
  - `un_state`  
  - `landlocked`  
  - `latitude`, `longitude`  
  - `religion`

---

## Notas


- Estos archivos se generan automáticamente al ejecutar el script de depuración.  
- En este repositorio académico se incluyen **tanto los datos originales como los datos depurados** para facilitar la revisión.  
- **migracion_neta_limpio.csv** es la base oficial para todos los análisis, visualizaciones e informes del proyecto.  