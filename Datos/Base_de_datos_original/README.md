 Datos originales (documentaci�n de fuente)

Este directorio contiene los archivos originales m�nimos necesarios para la depuraci�n del proyecto Migraci�n Internacional (1990�2019), junto con la documentaci�n de la fuente para garantizar la reproducibilidad.

## Fuente oficial

- **UN DESA � International Migrant Stock (v�a Gapminder / open-numbers)**
  - Repositorio DDF: https://github.com/open-numbers/ddf--unpop--international_migrant_stock

### Archivos relevantes del repositorio 

- `ddf--datapoints--immigrant_stock--by--geo--year.csv` (stock de inmigrantes por pa�s y a�o)
- `ddf--datapoints--emigrant_stock--by--geo--year.csv` (stock de emigrantes por pa�s y a�o)
- `ddf--entities--geo--country.csv` (Metadatos de pa�ses (ISO3, nombre, grupos de ingresos,etc.))


## Flujo reproducible
1. Usar estas bases de datos originales como entrada.
2. Ejecutar los scripts de `Datos/Codigo_depuracion/` para:
   - limpiar y estandarizar nombres/campos,
   - construir **inmigraci�n** y **emigraci�n** por pa�s�a�o,
   - generar **migraci�n neta = inmigrantes � emigrantes**.
3. Guardar los resultados en `Datos/Base_de_datos_depurada/`.

