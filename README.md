# Idoneidad Solar AHP — Evaluación Espacial Multicriterio para Parques Solares

Informe y presentación del proyecto final del curso **Geomática General** (Universidad
Nacional de Colombia, Sede Bogotá). El trabajo desarrolla un modelo de decisión
multicriterio (AHP) para identificar zonas aptas para parques solares fotovoltaicos y lo
materializa en un complemento de QGIS, `solar_site_suitability`, construido con PyQGIS y
los algoritmos de `qgis:processing`.

**Autores:** Fernán José Severich Díaz · Pedro Joaquín Perilla Vargas
**Docente:** Alexys Herleym Rodríguez Avellaneda, PhD (Ingeniero Civil, experto en geoinformática)
**Curso:** Geomática General · 2026

## Estructura

```
idoneidad-solar-ahp/
├── proyecto_final.qmd        informe en Quarto (fuente)
├── proyecto_final.pdf        informe renderizado (portada, TOC, listas, callouts)
├── proyecto_final.html       informe renderizado (web autocontenida)
├── referencias.bib           bibliografía (BibTeX)
├── apa.csl                   estilo de citación APA
├── custom.css                tipografía del informe HTML
├── figuras/                  figuras del informe y la presentación
└── presentacion/
    ├── presentacion_final.qmd   presentación en Quarto / reveal.js
    └── presentacion_final.html  presentación renderizada (autocontenida)
```

## El complemento

El complemento de QGIS asociado, `solar_site_suitability`, vive en su propio repositorio
y se publicó en el repositorio oficial de complementos de QGIS (`plugins.qgis.org`) bajo
licencia GPL-3.0-or-later; se encuentra en proceso de validación.

## Caso de demostración

El flujo se ejercita sobre el municipio de Concordia (Antioquia), con radiación ERA5 SSRD
de Copernicus, CRS EPSG:9377 y resolución de 1.0 m, excluyendo el casco urbano. La
ejecución entrega 15 polígonos óptimos (6.776 ha).

## Cómo renderizar

Requiere Quarto y una distribución de LaTeX para el PDF.

```bash
quarto render proyecto_final.qmd
quarto render presentacion/presentacion_final.qmd --to revealjs
```
