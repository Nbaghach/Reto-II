# Proyecto de Ciencia de Datos Reproducible: Migracion Internacional (1990-2019)

Este repositorio contiene un proyecto de **Ciencia de Datos Reproducible** realizado en RStudio.  
El objetivo es analizar los **patrones de inmigración, emigración y migración neta por pais y año** a partir de datos públicos, aplicando buenas prácticas de reproducibilidad (GitHub, RMarkdown, flexdashboard, etc.).

---

##  Estructura del repositorio

- **Datos/**
  - Base_de_datos_original/ → README con la fuente oficial (UN DESA – Gapminder)
  - Codigo_depuracion/ → Scripts R de carga y limpieza
  - Base_de_datos_depurada/ → Datos procesados para análisis

- **Dashboard/**
  - Codigo/ → RMarkdown (flexdashboard / Shiny)
  - HTML/ → Dashboard compilado

- **Informe/**
  - Codigo/ → Informe .Rmd (knitr/Rmarkdown)
  - DF/ → Informe compilado

- **Presentacion/**
  - Codigo/ → Presentación .Rmd
  - PDF_HTML/ → Salida PDF/HTML
---

##  Reproducibilidad

- Fuente de datos: [UN DESA – International Migrant Stock (vía Gapminder/open-numbers)](https://github.com/open-numbers/ddf--unpop--international_migrant_stock)

- Todos los analisis usan **rutas relativas** (ej. `here::here()` en R).  

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
```

---

##  Autoría

Nabel Baghach — Repositorio: https://github.com/Nbaghach/Reto-II