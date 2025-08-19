# Proyecto de Ciencia de Datos Reproducible: Migraci�n Internacional (1990�2019)

Este repositorio contiene un proyecto de **Ciencia de Datos Reproducible** realizado en RStudio.  
El objetivo es analizar los **patrones de migraci�n neta por pa�s y a�o** a partir de datos p�blicos,  
aplicando buenas pr�cticas de reproducibilidad (GitHub, RMarkdown, flexdashboard, etc.).

---

##  Estructura del repositorio

- **Datos/**
  - `Base_de_datos_original/` ??? contiene el archivo original `migracion_neta_por_pais_ano.csv`.
  - `Codigo_depuracion/` ??? scripts de R para cargar y depurar los datos.
  - `Base_de_datos_depurada/` ??? datos procesados listos para an�lisis.

- **Dashboard/**
  - `Codigo/` ??? c�digo RMarkdown para generar el dashboard.
  - `HTML/` ??? versi�n compilada del dashboard.

- **Informe/**
  - `Codigo/` ??? archivo `.Rmd` del informe t�cnico.
  - `PDF/` ??? versi�n compilada en PDF.

- **Presentacion/**
  - `Codigo/` ??? archivo `.Rmd` de la presentaci�n.
  - `PDF_HTML/` ??? versi�n compilada en PDF o HTML.

---

##  Reproducibilidad

- Los datos originales **no se modifican**.  
- Todos los an�lisis usan **rutas relativas** (ej. `here::here()` en R).  
- Los outputs generados (tablas, gr�ficos, dashboard, informe, presentaci�n)  
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

## Autor�a

Proyecto desarrollado por **Nabel Baghach**  
Repositorio GitHub: [Reto-II](https://github.com/Nbaghach/Reto-II)