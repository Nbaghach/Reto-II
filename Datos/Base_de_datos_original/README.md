 Datos originales (documentación de fuente)

Para garantizar **reproducibilidad** sin subir archivos pesados, aquí se documenta la
**fuente oficial** de los datos usados para construir las bases de **inmigración**, **emigración** y **migración neta**.

## Fuente oficial
- **UN DESA – International Migrant Stock (vía Gapminder / open-numbers)**
  - Repositorio DDF: https://github.com/open-numbers/ddf--unpop--international_migrant_stock

### Archivos relevantes del repositorio DDF
- `ddf--datapoints--immigrant_stock--by--geo--year.csv` (stock de inmigrantes por país y año)
- `ddf--datapoints--emigrant_stock--by--geo--year.csv` (stock de emigrantes por país y año)
- (Opcional) `ddf--datapoints--migrant_stock--by--destination--origin--year.csv` (matriz destino–origen)
- Entidades auxiliares: `ddf--entities--geo.csv`, `ddf--entities--geo--world_4region.csv`,
  `ddf--entities--geo--income_groups.csv`, etc.

> **Nota:** anota el commit/fecha de descarga para trazabilidad.

## Flujo reproducible
1. Descargar los CSV originales desde el repositorio DDF anterior.
2. Ejecutar los scripts de `Datos/Codigo_depuracion/` para:
   - limpiar y estandarizar nombres/campos,
   - construir **inmigración** y **emigración** por país–año,
   - generar **migración neta = inmigrantes – emigrantes**.
3. Guardar los resultados en `Datos/Base_de_datos_depurada/`.

## Por qué no subimos los originales
- GitHub limita archivos > 100 MB.
- Mantener el repositorio ligero y 100% reproducible con enlaces a la fuente oficial.