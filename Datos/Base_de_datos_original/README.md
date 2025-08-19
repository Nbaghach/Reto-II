 Datos originales (documentaci�n de fuente)

Para garantizar **reproducibilidad** sin subir archivos pesados, aqu� se documenta la
**fuente oficial** de los datos usados para construir las bases de **inmigraci�n**, **emigraci�n** y **migraci�n neta**.

## Fuente oficial
- **UN DESA � International Migrant Stock (v�a Gapminder / open-numbers)**
  - Repositorio DDF: https://github.com/open-numbers/ddf--unpop--international_migrant_stock

### Archivos relevantes del repositorio DDF
- `ddf--datapoints--immigrant_stock--by--geo--year.csv` (stock de inmigrantes por pa�s y a�o)
- `ddf--datapoints--emigrant_stock--by--geo--year.csv` (stock de emigrantes por pa�s y a�o)
- (Opcional) `ddf--datapoints--migrant_stock--by--destination--origin--year.csv` (matriz destino�origen)
- Entidades auxiliares: `ddf--entities--geo.csv`, `ddf--entities--geo--world_4region.csv`,
  `ddf--entities--geo--income_groups.csv`, etc.

> **Nota:** anota el commit/fecha de descarga para trazabilidad.

## Flujo reproducible
1. Descargar los CSV originales desde el repositorio DDF anterior.
2. Ejecutar los scripts de `Datos/Codigo_depuracion/` para:
   - limpiar y estandarizar nombres/campos,
   - construir **inmigraci�n** y **emigraci�n** por pa�s�a�o,
   - generar **migraci�n neta = inmigrantes � emigrantes**.
3. Guardar los resultados en `Datos/Base_de_datos_depurada/`.

## Por qu� no subimos los originales
- GitHub limita archivos > 100 MB.
- Mantener el repositorio ligero y 100% reproducible con enlaces a la fuente oficial.