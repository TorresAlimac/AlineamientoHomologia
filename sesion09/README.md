---
title: "Cluster Omega vs MAFFT"
author: "Torres Camila"
date: "2026-10-16"
output: html_document
---
# Práctica: Clustal Omega contra MAFFT
## Sesión 9 

### Versiones: 

- Clustalo: 1.2.4
- MAFFT: v7.526
- Muscle: v3.8.1551
- Trimal: 1.2rev59

### Datos

Los datos y scripts utilizados para la práctica se copiaron desde:

`/mnt/data/bioinfo1/jmiranda/sesion09`

Se trabajó con dos familias de proteínas: R-spondinas (RSPO) y receptores LGR.

## Resultados

### RSPO

En RSPO, Clustal Omega y MAFFT coincidieron casi por completo en las regiones FU1+FU2 y TSP1, donde el acuerdo medio fue de 0.99. Las principales diferencias estuvieron en los extremos de la proteína. En el péptido señal, aproximadamente en las posiciones 1–21, el acuerdo bajó a 0.49, y en la región C-terminal, especialmente alrededor de las posiciones 211–243, bajó todavía más. Estas zonas también presentaron menor confianza en MUSCLE5 y varias posiciones fueron eliminadas por trimAl. Por esto, las regiones donde los programas no se ponen de acuerdo también tienden a ser las regiones menos confiables del alineamiento.

### RSPO por dominio

| Dominio | Acuerdo medio | LC medio | Residuos eliminados |
|---|---:|---:|---:|
| Péptido señal | 0.49 | 8.24 | 10 |
| Enlace N | 0.50 | 8.67 | 6 |
| FU1+FU2 | 0.99 | 9.00 | 3 |
| Enlace | 0.96 | 9.00 | 1 |
| TSP1 | 0.99 | 9.00 | 0 |
| C-terminal | 0.35 | 7.85 | 17 |

### LGR

En LGR hubo más diferencias entre Clustal Omega y MAFFT que en RSPO. La región 7TM fue la que mostró mayor acuerdo, con 0.96, mientras que el dominio LRR tuvo un acuerdo de 0.61 y muchas posiciones fueron eliminadas por trimAl. La región C-terminal fue la más problemática, con un acuerdo medio de 0.40 y una confianza de MUSCLE5 bastante menor. Esto se ve especialmente hacia el final de LGR5, alrededor de las posiciones 873–907, donde el acuerdo entre los alineamientos disminuye mucho y muchas posiciones también son eliminadas por trimAl. En general, las regiones de menor acuerdo también fueron las de menor confianza.

### LGR por dominio

| Dominio | Acuerdo medio | LC medio | Residuos eliminados |
|---|---:|---:|---:|
| LRR | 0.61 | 7.16 | 357 |
| Bisagra | 0.78 | 7.46 | 87 |
| 7TM | 0.96 | 8.95 | 32 |
| C-terminal | 0.40 | 4.66 | 82 |


## Árbol guía

No sería correcto usar el archivo `.dnd` de Clustal Omega como una filogenia, porque solamente es un árbol guía que el programa usa para decidir el orden en que va alineando las secuencias y no representa necesariamente su historia evolutiva.
