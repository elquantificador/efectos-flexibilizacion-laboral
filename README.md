# Efectos de la flexibilización laboral — El Quantificador

Repositorio para el artículo sobre los efectos de la flexibilización laboral en el mercado de trabajo argentino.

## Estructura del repositorio

```
elquantificador-articulo/
│
├── elquantificador-articulo.Rproj     # Proyecto R (obligatorio)
│
├── code/                              # Scripts (separados por etapa)
│   ├── 00_setup.R                     # Carga/instala paquetes, rutas, opciones
│   ├── download/                      # Descarga o lectura de fuentes
│   │   └── 01_download.R
│   ├── cleaning/                      # Limpieza, validación y transformación
│   │   └── 02_cleaning.R
│   └── analysis/                      # Análisis, tabulados, modelos y figuras
│       └── 03_analysis.R
│
├── data/                              # Datos (NO subir pesados o sensibles)
│   ├── raw/                           # Datos crudos (inmutables)
│   └── processed/                     # Datos listos para análisis
│
├── images/                            # Gráficos y figuras exportadas
│
├── report/                            # Reportes intermedios/finales
│   ├── draft.Rmd                      # Borrador reproducible
│   └── final.pdf                      # Versión final (ligera)
│
├── README.md                          # Guía del proyecto y reproducción
├── LICENSE                            # Licencia
└── .gitignore                         # Ignorar temporales y binarios
```

## Requisitos técnicos

- R (versión recomendada: >= 4.0)
- Paquetes: `survey`, `tidyverse`, `patchwork`, `openxlsx`, `haven`
- Instalación/carga automática en `code/00_setup.R`

## Cómo reproducir

1. Ejecutar `code/efectos_flexibilizacion_laboral_analisis.R` para replicar el análisis.
2. El reporte se genera mediante el archivo `report/texto-articulo.Rmd`.

(Opcional: crear un `run_all.R` para automatizar)

## Fuentes de datos

- Los datos crudos no se incluyen por tamaño/licencia. Ver instrucciones y enlaces en `code/download/01_download.R`.

## Resultados

- Tablas y figuras exportadas en `images/`
- Reportes en `report/`

## Licencia y créditos

- Ver archivo `LICENSE`.
- Artículo y scripts por El Quantificador.

## Notas

- No subir datos sensibles ni archivos pesados.
- Documentar excepciones en este README.
