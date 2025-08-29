# Dashboards — Migración Internacional (1990–2019)

Este directorio contiene dos versiones del dashboard del proyecto:

- **Dinámico (Shiny)**: interactivo con filtros en vivo (RMarkdown + flexdashboard + Shiny).
- **Estático (HTML)**: archivo autocontenido que funciona con doble-click (sin servidor Shiny).

**Datos de entrada**: ambos leen `Datos/Base_de_datos_depurada/migracion_neta_limpio.csv`  
**Fuente**: UN DESA (vía Gapminder / open-numbers).

---

## Requisitos

- R y RStudio.  
- Paquetes necesarios:  
  "tidyverse","readr","dplyr","tidyr","ggplot2","forcats",
  "scales","janitor","plotly","flexdashboard","shiny",
  "here","stringr","htmltools","countrycode".  

---

## Estructura del proyecto

Dashboard/
├─ Codigo/
│  ├─ dashboard_migracion.Rmd          # Dashboard dinámico (Shiny)
│  └─ Dashboard_migracion_static.Rmd   # Dashboard estático (HTML)
└─ HTML/
   └─ Dashboard_migracion_static.html          # Render del estático
---

## Qué muestra?

- **Gráfico de líneas** (1990-2019): evolución global y por región.  
- **Mapa choropleth**: distribución por país en el año elegido.  
- **Rankings**: Top 5 en inmigrantes, emigrantes y migración neta.  
- **Estadísticas globales**: totales en la vista activa.

**Filtros del dashboard dinámico:**
- Año (`year`)  
- Métrica (`inmigrants`, `emigrants`, `net`)  
- Región (`region`)  
- Grupo de ingreso (`income_groups`)  

---

## Variables esperadas en `migracion_neta_limpio.csv`

- `iso3` (código ISO3)  
- `country_name`  
- `year`  
- `inmigrants`  
- `emigrants`  
- `net_migration`  
- `region4`, `region6`  
- `income_groups`  

El `.Rmd` armoniza los nombres a:  
`iso3`, `country`, `year`, `inmigrants`, `emigrants`, `net`, `region`, `income`.

---
## Dashboard dinámico (Shiny)

**Archivo**: Dashboard/Codigo/dashboard_migracion.Rmd
**Nota**. con runtime: shiny, usa Run Document o rmarkdown::run() (no “Knit”).
---
## Dashboard estático (HTML)

**Archivo**: Dashboard/Codigo/Dashboard_migracion_static.Rmd

**Parámetros** (editar en el chunk setup)
year_selected <- 2019          # año 
show_metric   <- "inmigrants" # "inmigrants" | "emigrants" | "net"

## Cita de datos
UN DESA — International Migrant Stock (vía Gapminder / open-numbers).
Repositorio DDF: https://github.com/open-numbers/ddf--unpop--international_migrant_stock