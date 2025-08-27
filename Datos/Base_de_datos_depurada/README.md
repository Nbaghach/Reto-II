 Datos depurados

Esta carpeta contiene los **datasets intermedios** y el **dataset final** generados a partir de los datos originales documentados en `Datos/Base_de_datos_original/`. Los archivos aqu� presentes son el resultado directo del script de depuraci�n (`depuracion_script.Rmd`).

## Contenido

- **inmigrants.csv**  
  Stock de inmigrantes por pa�s y a�o (**dataset intermedio**).  
  
  **Variables principales:**  
  - `iso3` � c�digo ISO Alpha-3 del pa�s  
  - `country_name` � nombre del pa�s  
  - `year` � a�o de referencia  
  - `inmigrants` � stock de inmigrantes  
  - + metadatos auxiliares (regiones, ingresos, etc.)

- **emigrants.csv**  
  Stock de emigrantes por pa�s y a�o (**dataset intermedio**).  
  
  **Variables principales:**  
  - `iso3`, `country_name`, `year`  
  - `emigrants` � stock de emigrantes  
  - + metadatos auxiliares

- **migracion_neta.csv**  
  Dataset **intermedio** con la migraci�n neta = `inmigrants � emigrants`.  
  Incluye duplicados y columnas adicionales, por lo que **no debe usarse para an�lisis finales**.

- **migracion_neta_limpio.csv**  
  **Dataset final del proyecto** (depurado y estandarizado).  
  
  **Variables principales:**  
  - `iso3`, `country_name`, `year`  
  - `inmigrants`, `emigrants`, `net_migration`  
  - `region4`, `region6`  
  - `income_groups`  
  - `g77_ocde`  
  - `un_state`  
  - `landlocked`  
  - `latitude`, `longitude`  
  - `religion`

## Notas

- Estos archivos se generan **autom�ticamente** al ejecutar el script de depuraci�n.  
- **migracion_neta_limpio.csv** es la **base oficial** para todos los an�lisis, visualizaciones e informes del proyecto.  
