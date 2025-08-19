# Datos originales y procesados

Esta carpeta contiene los archivos utilizados para la construcci�n de la base final de migraci�n neta.

## Estructura

- **archivos originales/**  
  Contiene el dataset bruto descargado de Gapminder, que sirve como fuente principal.

- **inmigracion/**  
  Aqu� se integran y procesan los datos originales relacionados con la inmigraci�n.  
  Resultado: `inmigracion_total.csv`.

- **emigracion/**  
  Aqu� se integran y procesan los datos originales relacionados con la emigraci�n.  
  Resultado: `emigracion_total.csv`.

- **migracion neta/**  
  Contiene el dataset final generado a partir de la diferencia entre inmigraci�n y emigraci�n.  
  Resultado: `migracion_neta_por_pais_ano.csv`.

## Notas
- Todos los datos provienen de **Gapminder** (https://www.gapminder.org/).  
- La base final de **migraci�n neta** ser� utilizada en el resto del proyecto (depuraci�n, an�lisis y visualizaci�n).