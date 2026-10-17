# Ficha del artículo

Completa esta ficha al crear el repositorio y mantenla al día. Es el único
lugar con datos propios del artículo; el README es igual en todos los
repositorios.

## Identificación

- **Título:** Efectos de la flexibilización laboral — El Quantificador
- **Descripción del repositorio:** Repositorio para el articulo de El Quantificador: Efecto de la flexibilización laboral en los costes salariales en Ecuador
- **Autoría:** [COMPLETAR: nombres, igual que en el sitio]
- **Fecha de publicación:** [COMPLETAR: AAAA-MM-DD]
- **Artículo publicado:** [COMPLETAR: enlace a elquantificador.org]
- **Categoría:** [COMPLETAR: Economía, Política, Salud, Educación o Valores y
  comportamiento]
- **Edición:** [COMPLETAR: por ejemplo, Julio-Diciembre 2026]

## Estado

[COMPLETAR: en preparación, en revisión editorial o publicado. Anota qué falta
para cerrar el artículo.]

## Pregunta y alcance

[COMPLETAR: dos o tres oraciones con la pregunta, el periodo, la cobertura
geográfica y la unidad de análisis.]

## Requisitos

- R [COMPLETAR: versión, por ejemplo 4.5.x].
- Paquetes de R: [COMPLETAR: lista en orden alfabético].

## Fuentes de datos

| Fuente | Institución | Periodo | Acceso | Script |
|---|---|---|---|---|
| [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR: descarga automática o manual] | `code/cleaning/00_download_fuente.R` |

Si alguna fuente no permite descarga automática, explica aquí cómo obtenerla y
dónde colocarla en `data/raw/`.

## Salidas

- `outputs/tables/[COMPLETAR].csv`: [COMPLETAR: qué contiene].
- `outputs/graphs/[COMPLETAR].png`: [COMPLETAR: qué muestra].
- `article/images/graficoN.png`: copias numeradas según el orden del texto.

## Cómo replicar en este repositorio

Este repositorio conserva sus instrucciones originales en la sección
"README anterior". Si todavía no tiene `MASTER.R`, sigue esas instrucciones.
Cuando se migre a la estructura estándar, reemplaza esta sección por los pasos
de `MASTER.R`.

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
