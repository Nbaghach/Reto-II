# Código de depuración

Este directorio contiene el script principal de depuración de datos para el proyecto **Migración Internacional (1990–2019)**.

## Contenido

- **depuracion_script.Rmd**  
  Documento RMarkdown que implementa todo el flujo de depuración de los datos originales hasta obtener el dataset final.

## Flujo del script

1. **Paquetes y rutas**  
   - Carga de librerías (`readr`, `dplyr`, `here`).
   - Definición de rutas relativas para datos de entrada y salida.

2. **Importación de datos originales**  
   - Lectura de los CSV oficiales de inmigrantes, emigrantes y metadatos de países.
   - Revisión inicial de estructura y variables.

3. **Limpieza y estandarización**  
   - Creación de claves consistentes (`iso3`, `country_name`).
   - Unión con metadatos de países.
   - Generación de tablas intermedias: **immigrants.csv** y **emigrants.csv**.

4. **Cálculo de migración neta**  
   - Combinación de inmigrantes y emigrantes por país y año.
   - Cálculo de `net_migration = immigrants - emigrants`.
   - Exportación de un archivo intermedio: **migracion_neta.csv**.

5. **Depuración final**  
   - Eliminación de duplicados.
   - Selección y renombrado de variables finales (incluyendo `region4`, `region6`, `income_groups`, `g77_ocde`, `un_state`, `landlocked`, `latitude`, `longitude`, `religion`).
   - Exportación del dataset final: **migracion_neta_limpio.csv**.

6. **Registro de salidas**  
   - Verificación de archivos generados en `Datos/Base_de_datos_depurada/`.

## Notas

- El script está diseñado para ser **100% reproducible**:  
  - Usa rutas relativas con `here::here()`.  
  - No depende de directorios locales del usuario.  
- Todas las salidas se almacenan automáticamente en `Datos/Base_de_datos_depurada/`.  
- **migracion_neta_limpio.csv** es la base de datos oficial para análisis, dashboard e informe.  
