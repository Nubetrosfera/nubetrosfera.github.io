---
layout: post
title: "limpieza de datos: 106 estaciones"
date: 2026-03-23
categories: recursos
image: assets/images/code.jpg
---
Para procesar las variables de precipitación y temperaturas extremas, utilicé el siguiente flujo en **R**:

```r
library(tidyverse)
# Cargar estaciones
data <- read_csv("estaciones_smn.csv") %>%
  filter(!is.na(tmax))
```