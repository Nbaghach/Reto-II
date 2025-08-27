 Datos originales (documentación de fuente)

Este directorio contiene los archivos originales mínimos necesarios para la depuración del proyecto Migración Internacional (1990–2019), junto con la documentación de la fuente para garantizar la reproducibilidad.

## Fuente oficial

- **UN DESA – International Migrant Stock (vía Gapminder / open-numbers)**
  - Repositorio DDF: https://github.com/open-numbers/ddf--unpop--international_migrant_stock

### Archivos relevantes del repositorio 

- `ddf--datapoints--immigrant_stock--by--geo--year.csv` (stock de inmigrantes por país y año)
- `ddf--datapoints--emigrant_stock--by--geo--year.csv` (stock de emigrantes por país y año)
- `ddf--entities--geo--country.csv` (Metadatos de países (ISO3, nombre, grupos de ingresos,etc.))


## Flujo reproducible
1. Usar estas bases de datos originales como entrada.
2. Ejecutar los scripts de `Datos/Codigo_depuracion/` para:
   - limpiar y estandarizar nombres/campos,
   - construir **inmigración** y **emigración** por país–año,
   - generar **migración neta = inmigrantes – emigrantes**.
3. Guardar los resultados en `Datos/Base_de_datos_depurada/`.

