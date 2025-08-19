# Proyecto de Ciencia de Datos Reproducible: Migración Internacional (1990–2019)

Este repositorio contiene un proyecto de **Ciencia de Datos Reproducible** realizado en RStudio.  
El objetivo es analizar los **patrones de migración neta por país y año** a partir de datos públicos,  
aplicando buenas prácticas de reproducibilidad (GitHub, RMarkdown, flexdashboard, etc.).

---

##  Estructura del repositorio

- **Datos/**
  - `Base_de_datos_original/` ??? contiene el archivo original `migracion_neta_por_pais_ano.csv`.
  - `Codigo_depuracion/` ??? scripts de R para cargar y depurar los datos.
  - `Base_de_datos_depurada/` ??? datos procesados listos para análisis.

- **Dashboard/**
  - `Codigo/` ??? código RMarkdown para generar el dashboard.
  - `HTML/` ??? versión compilada del dashboard.

- **Informe/**
  - `Codigo/` ??? archivo `.Rmd` del informe técnico.
  - `PDF/` ??? versión compilada en PDF.

- **Presentacion/**
  - `Codigo/` ??? archivo `.Rmd` de la presentación.
  - `PDF_HTML/` ??? versión compilada en PDF o HTML.

---

##  Reproducibilidad

- Los datos originales **no se modifican**.  
- Todos los análisis usan **rutas relativas** (ej. `here::here()` en R).  
- Los outputs generados (tablas, gráficos, dashboard, informe, presentación)  
  se guardan en sus carpetas correspondientes.  

---

##  Paquetes necesarios

Para ejecutar el proyecto se necesitan los siguientes paquetes de R:

```r
install.packages(c(
  "tidyverse", "here", "readr", "dplyr", 
  "knitr", "rmarkdown", "flexdashboard", 
  "shiny", "leaflet", "plotly"
))

## Autoría

Proyecto desarrollado por **Nabel Baghach**  
Repositorio GitHub: [Reto-II](https://github.com/Nbaghach/Reto-II)