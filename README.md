# Censo de Alumbrado Público – San José

Análisis exploratorio del relevamiento de alumbrado público del departamento de San José (agosto–noviembre 2026), hecho en R + Quarto.

## Contenido

| Archivo | Descripción |
|---|---|
| `analisis_alumbrado.qmd` | Documento Quarto con limpieza, tablas, gráficos y mapa |
| `data/` | Carpeta para la base `base_alumbrado.xlsx` (no versionada por defecto) |
| `censo-alumbrado.Rproj` | Proyecto de RStudio |

## Análisis incluidos

- Puntos y artefactos por localidad
- Tipos de luminaria (con recodificación de "other": reflectores, solares)
- Material de apoyo (incluye detección de postes de madera)
- Luminarias en parques y plazas
- Mapa interactivo (leaflet)
- Clasificación de observaciones
- Avance del relevamiento

## Cómo reproducir

1. Clonar el repositorio y abrir `censo-alumbrado.Rproj`.
2. Copiar `base_alumbrado.xlsx` en `data/`.
3. Instalar paquetes:
   ```r
   install.packages(c("tidyverse", "readxl", "gt", "scales", "sf", "leaflet"))
   ```
4. Renderizar:
   ```bash
   quarto render analisis_alumbrado.qmd
   ```
