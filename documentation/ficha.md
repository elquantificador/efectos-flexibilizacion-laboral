# Ficha del artículo

Completa esta ficha al crear el repositorio y mantenla al día. Es el único
lugar con datos propios del artículo; el README es igual en todos los
repositorios.

## Identificación

- **Título:** Efecto de la flexibilización laboral en los costes salariales en Ecuador
- **Descripción del repositorio:** Repositorio para el articulo de El Quantificador: Efecto de la flexibilización laboral en los costes salariales en Ecuador
- **Autoría:** José Luis Solá
- **Fecha de publicación:** 2025-08-19
- **Artículo publicado:** https://elquantificador.org/post/economia/2025-08-19-efecto-de-la-flexibilizacion-laboral-en-los-costes-salariales-en-ecuador/
- **Categoría:** Economía
- **Edición:** Julio - Diciembre 2025

## Estado

Publicado el 2025-08-19.

## Pregunta y alcance

El artículo pregunta si la reforma laboral de 2016 (Ley Orgánica para la
Protección del Trabajo Juvenil, Protección del Empleo y Seguro del Desempleo)
cambió el crecimiento de los salarios y del coste laboral total en las
empresas ecuatorianas. Usa un panel de empresas de 2011 a 2019, con estados
financieros de la Superintendencia de Compañías (SUPERCIAS), y estima modelos
de efectos fijos y aleatorios con una variable binaria para los años desde 2016
y el crecimiento de las ventas como control. La unidad de análisis es la
empresa por año, identificada por RUC.

## Requisitos

- R: no documentada en el repositorio (el README anterior recomienda 4.0 o
  superior).
- Paquetes de R: DescTools, dplyr, dygraphs, foreign, GGally, ggplot2, Hmisc,
  htmlwidgets, knitr (para renderizar el `.Rmd`), lattice, lmtest, lubridate,
  outliers, plm, plotly, plyr, reshape2, rvest, sandwich, stargazer,
  tidyverse, tseries, webshot.

## Fuentes de datos

| Fuente | Institución | Periodo | Acceso | Script |
|---|---|---|---|---|
| Estados financieros de empresas (archivos `estadosFinancieros_AAAA.zip`) | Superintendencia de Compañías, Valores y Seguros (SUPERCIAS), portal de mercado de valores | 2011 a 2019 | Descarga automática desde `https://mercadodevalores.supercias.gob.ec/reportes/zip/estadosFinancieros_AAAA.zip` (2011 a 2019) | `code/efectos_flexibilizacion_laboral_analisis.R` |

Los datos no están en el repositorio: el script descarga y descomprime los nueve
`.zip` (2011 a 2019) en `data/raw/`, que git ignora.

## Salidas

- `images/graf1-labor-market.png`: crecimiento porcentual de los salarios
  (gráfico dinámico `dygraphs` exportado con `webshot`).
- `images/graf2-labor-market.png`: crecimiento porcentual del coste laboral
  total (salarios más seguridad social).
- `tables/Tablas_EQ.txt`: tabla `stargazer` en texto con los cuatro modelos de
  panel (efectos fijos y aleatorios para salarios y coste laboral), con errores
  estándar robustos.
- `images/graf1-labor-market.html` y `images/graf2-labor-market.html`: versiones
  interactivas de los gráficos; no están versionadas.

## Cómo replicar en este repositorio

Este repositorio no tiene `MASTER.R`. El directorio de trabajo es la raíz del
repositorio (abre `elquantificador-articulo.Rproj` o haz `setwd()` a la raíz).

1. Clona o descarga el repositorio.
2. Ejecuta `code/efectos_flexibilizacion_laboral_analisis.R` completo. En orden:
   crea `data/raw/`, `images/` y `tables/`; descarga y descomprime los `.zip` de
   SUPERCIAS de 2011 a 2019 en `data/raw/`; lee los archivos
   `balances_AAAA_N.txt`; elimina RUC duplicados por año; une los años en
   `masterdata`; calcula crecimientos y winsoriza al 5 %; estima los modelos
   `plm`; escribe `tables/Tablas_EQ.txt` y exporta los dos gráficos a HTML y PNG
   en `images/`. Requiere internet y `webshot::install_phantomjs()`.
3. Renderiza `report/texto-articulo.Rmd` para regenerar el texto. Busca las
   figuras en `../images/`, es decir, en la carpeta `images/` de la raíz.

## README anterior

Texto del README de este repositorio antes de adoptar el README estándar,
conservado sin cambios de contenido para no perder información.

### Efectos de la flexibilización laboral — El Quantificador

Repositorio para el artículo sobre los efectos de la flexibilización laboral en el mercado de trabajo ecuatoriano por José Solá. 

#### Requisitos técnicos

- R (versión recomendada: >= 4.0)
- Paquetes: tidyverse, plm, DescTools, rvest, reshape2, plotly, GGally, Hmisc, lmtest, sandwich, stargazer, tseries, dygraphs, webshot y htmlwidgets.
  
#### Cómo reproducir

1. Ejecutar `code/efectos_flexibilizacion_laboral_analisis.R` para replicar el análisis.
2. El reporte se genera mediante el archivo `report/texto-articulo.Rmd`.

El [repositorio original](https://github.com/Joseluissola/Labor-market-analysis-in-Ecuador) se encuentra en el perfil de GitHub del [autor](https://github.com/Joseluissola).
