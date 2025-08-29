# Proyecto de Ciencia de Datos Reproducible: Migración Internacional (1990–2019)

Este repositorio contiene un proyecto de **Ciencia de Datos Reproducible** realizado en RStudio.  
El objetivo es analizar los **patrones de inmigración, emigración y migración neta por país y año** a partir de datos públicos, aplicando buenas prácticas de reproducibilidad (GitHub, RMarkdown, flexdashboard, etc.).

---

## Estructura del repositorio

```r
├─ Datos/
│  ├─ Base_de_datos_original/             # CSV originales + README con la fuente oficial
│  ├─ Codigo_depuracion/
│  │  └─ depuracion_script.Rmd            # depuración y unificación
│  └─ Base_de_datos_depurada/
│     └─ migracion_neta_limpio.csv        # dataset final
├─ Dashboard/
│  ├─ Codigo/
│  │  ├─ dashboard_migracion.Rmd          # Dashboard dinámico (Shiny)
│  │  └─ Dashboard_migracion_static.Rmd   # Dashboard estático (HTML)
│  └─ HTML/
│     └─ dashboard_migracion_static.html  # salida compilada
├─ Informe/
│  ├─ Codigo/
│  │  └─ informe_migracion.Rmd            # Informe técnico (RMarkdown/knitr)
│  └─ PDF/
│     └─ informe_migracion.pdf            # salida compilada
├─ Presentacion/
│  ├─ Codigo/
│  │  └─ Presentacion.Rmd                 # ioslides
│  └─ PDF_HTML/
│     └─ Presentacion.html                # salida compilada
├─ Reto-II.Rproj                          # proyecto de RStudio
└─ README.md                              # este archivo
```
---
## Reproducibilidad

- **Fuente de datos**: [UN DESA – International Migrant Stock (vía Gapminder/open-numbers)](https://github.com/open-numbers/ddf--unpop--international_migrant_stock)

- Los análisis usan **parámetros de entrada (`params$data_path`)** para localizar los datos.  
  > Es decir, primero hay que ejecutar el script de **depuración**, que genera los CSV en `Datos/Base_de_datos_depurada/`.

- Los outputs generados (tablas, gráficos, dashboard, informe, presentación)  
  se guardan en sus carpetas correspondientes.
---

## Ejecución

Para reproducir el proyecto completo en RStudio:

1.**Depuración de datos**  

   Ejecuta el script que limpia y unifica las bases de datos originales: 
   
 ```r
rmarkdown::render("Datos/Codigo_depuracion/depuracion_script.Rmd")
```

2.**Informe Técnico**

Compila el informe con knitr:

 ```r
rmarkdown::render("Informe/Codigo/Informe.Rmd")
```

3. **Dashboard interactivo** 

Lanza el dashboard con flexdashboard + Shiny:

```r
rmarkdown::run("Dashboard/Codigo/Dashboard_migracion.Rmd")
```

4.**Presentación**

Genera la presentación en formato HTML o PDF:

```r
rmarkdown::render("Presentacion/Codigo/Presentacion.Rmd")
```
---

## Paquetes necesarios

```r
install.packages(c(
  "tidyverse","janitor","scales","knitr","rmarkdown",
  "flexdashboard","shiny","plotly","here","countrycode",
  "sf","rnaturalearth","rnaturalearthdata" 
))
```
---
## Autoría 

Nabel Baghach — Repositorio: https://github.com/Nbaghach/Reto-II
