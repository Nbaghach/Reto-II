# Datos originales y procesados

Esta carpeta contiene los archivos utilizados para la construcción de la base final de migración neta.

## Estructura

- **archivos originales/**  
  Contiene el dataset bruto descargado de Gapminder, que sirve como fuente principal.

- **inmigracion/**  
  Aquí se integran y procesan los datos originales relacionados con la inmigración.  
  Resultado: `inmigracion_total.csv`.

- **emigracion/**  
  Aquí se integran y procesan los datos originales relacionados con la emigración.  
  Resultado: `emigracion_total.csv`.

- **migracion neta/**  
  Contiene el dataset final generado a partir de la diferencia entre inmigración y emigración.  
  Resultado: `migracion_neta_por_pais_ano.csv`.

## Notas
- Todos los datos provienen de **Gapminder** (https://www.gapminder.org/).  
- La base final de **migración neta** será utilizada en el resto del proyecto (depuración, análisis y visualización).