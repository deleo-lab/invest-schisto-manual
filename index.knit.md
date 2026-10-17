---
title: "Pemba elimination scenario"
author: "Kayla Kauffman"
date: 07-25-2026 #important if sorting by date in tutorials
categories: [InVEST, Scenario] #rough ideas if want tags
image: invest-logo-registeredtm_202305_150dpi_0.png #must be in this folder
execute: 
    message: false
    warning: false
    echo: false
draft: false #true until ready to post
---



## Background  

Pemba Island, Tanzania is nearing elimination of schistosomiasis. Here we use risk maps derived from 2012, 2019, and 2025 to compare risk to human-case data. 

## Input layers  


::: {.cell}
::: {.cell-output .cell-output-stdout}

```
|---------|---------|---------|---------|=========================================                                          
```


:::

::: {.cell-output .cell-output-stdout}

```
|---------|---------|---------|---------|=========================================                                          |---------|---------|---------|---------|=========================================                                          
```


:::

::: {.cell-output .cell-output-stdout}

```
|---------|---------|---------|---------|=========================================                                          
```


:::
:::



::: {.cell}

:::


### AOI  

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-2-1.png){width=672}
:::
:::

The total area of the Pemba AOI is 919.8356919 km^2. The wikipedia pages say 988 km^2

### Water presence  


::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-3-1.png){width=672}
:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-3-2.png){width=672}
:::

::: {.cell-output-display}


Table: units = $km^2$

| Year| Water area| $y_i - y_1$| $y_i - y_{i-1}$|
|----:|----------:|-----------:|---------------:|
| 2015|      17.25|        0.00|              NA|
| 2017|      17.85|        0.60|            0.60|
| 2019|      17.88|        0.63|            0.02|
| 2021|      17.48|        0.23|           -0.40|
| 2023|      17.91|        0.66|            0.43|
| 2025|      17.87|        0.63|           -0.03|


:::

::: {.cell-output .cell-output-stdout}

```
|---------|---------|---------|---------|=========================================                                          
```


:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-3-3.png){width=672}
:::

::: {.cell-output .cell-output-stdout}

```
|---------|---------|---------|---------|=========================================                                          
```


:::

::: {.cell-output-display}


|N years with water |    Freq|
|:------------------|-------:|
|0                  | 7287308|
|1                  |  178259|
|2                  |   24619|
|3                  |   12128|
|4                  |    7305|
|5                  |    4388|
|6                  | 1718176|


:::
:::


Distance to water

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-4-1.png){width=672}
:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-4-2.png){width=672}
:::

::: {.cell-output .cell-output-stdout}

```
|---------|---------|---------|---------|=========================================                                          
```


:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-4-3.png){width=672}
:::

::: {.cell-output .cell-output-stdout}

```
[1] "max water dist = 576"
```


:::
:::



### Population 

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-5-1.png){width=672}
:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-5-2.png){width=672}
:::

::: {.cell-output-display}


| Year| Population| $y_i - y_1$| $y_i - y_{i-1}$|
|----:|----------:|-----------:|---------------:|
| 2013|   323552.5|        0.00|              NA|
| 2015|   331917.6|     8365.08|         8365.08|
| 2017|   340500.8|    16948.24|         8583.16|
| 2019|   349038.6|    25486.04|         8537.80|


:::
:::


The wikipedia page says the 2022 Census = 543,441
Compare that to the population suitability kmsq to ensure conversion in InVEST works. Using the two temp layers to ensure consistent across inputs.

::: {.cell}
::: {.cell-output .cell-output-stdout}

```
                                          sum
population_suit_sqkm_2019_BTtemp   3390024787
population_suitability_2019_BTtemp    4144261
population_suit_sqkm_2019_L8temp   3390024787
population_suitability_2019_L8temp    4144261
```


:::
:::


And the risk to pop estimates (rounded)

::: {.cell}
::: {.cell-output .cell-output-stdout}

```
                                           sum
risk_to_pop_abs_2019_BTtemp       183064747697
risk_to_pop_count_abs_2019_BTtemp   7226838970
risk_to_pop_count_rel_2019_BTtemp       110649
risk_to_pop_rel_2019_BTtemp            2802872
```


:::
:::



::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-8-1.png){width=672}
:::
:::


### Temperature dry  


::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-9-1.png){width=672}
:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-9-2.png){width=672}
:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-9-3.png){width=672}
:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-9-4.png){width=672}
:::
:::


### Temperature wet  


::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-10-1.png){width=672}
:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-10-2.png){width=672}
:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-10-3.png){width=672}
:::
:::


### NDVI dry


::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-11-1.png){width=672}
:::
:::


### NDVI wet  

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-12-1.png){width=672}
:::
:::





## Habitat risk  


#### Convolved habitat risk

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-14-1.png){width=672}
:::

::: {.cell-output-display}


Table: Pearson's correlations

|                                               | convolved_hab_risk_2013_2026_modisTEMP| convolved_hab_risk_2013_2026_NoTemp| convolved_hab_risk_2013_modisTEMP| convolved_hab_risk_2015_modisTEMP| convolved_hab_risk_2017_modisTEMP| convolved_hab_risk_2019_BTtemp| convolved_hab_risk_2019_L8temp| convolved_hab_risk_2019_L8temp_unmodifiedWater| convolved_hab_risk_2019_modisTEMP| convolved_hab_risk_2019_NOtemp| convolved_hab_risk_2021_modisTEMP| convolved_hab_risk_2023_modisTEMP| convolved_hab_risk_2025_modisTEMP|
|:----------------------------------------------|--------------------------------------:|-----------------------------------:|---------------------------------:|---------------------------------:|---------------------------------:|------------------------------:|------------------------------:|----------------------------------------------:|---------------------------------:|------------------------------:|---------------------------------:|---------------------------------:|---------------------------------:|
|convolved_hab_risk_2013_2026_modisTEMP         |                                   1.00|                                0.99|                              0.73|                              0.96|                              0.97|                           0.85|                           0.56|                                           0.56|                              0.98|                           0.83|                              0.95|                              0.97|                              0.99|
|convolved_hab_risk_2013_2026_NoTemp            |                                   0.99|                                1.00|                              0.72|                              0.97|                              0.96|                           0.84|                           0.55|                                           0.55|                              0.97|                           0.83|                              0.96|                              0.97|                              0.98|
|convolved_hab_risk_2013_modisTEMP              |                                   0.73|                                0.72|                              1.00|                              0.69|                              0.69|                           0.64|                           0.53|                                           0.53|                              0.69|                           0.60|                              0.66|                              0.68|                              0.74|
|convolved_hab_risk_2015_modisTEMP              |                                   0.96|                                0.97|                              0.69|                              1.00|                              0.95|                           0.83|                           0.53|                                           0.53|                              0.98|                           0.85|                              0.98|                              0.98|                              0.94|
|convolved_hab_risk_2017_modisTEMP              |                                   0.97|                                0.96|                              0.69|                              0.95|                              1.00|                           0.81|                           0.58|                                           0.58|                              0.97|                           0.81|                              0.95|                              0.96|                              0.96|
|convolved_hab_risk_2019_BTtemp                 |                                   0.85|                                0.84|                              0.64|                              0.83|                              0.81|                           1.00|                           0.51|                                           0.51|                              0.84|                           0.99|                              0.83|                              0.82|                              0.84|
|convolved_hab_risk_2019_L8temp                 |                                   0.56|                                0.55|                              0.53|                              0.53|                              0.58|                           0.51|                           1.00|                                           1.00|                              0.52|                           0.47|                              0.52|                              0.51|                              0.56|
|convolved_hab_risk_2019_L8temp_unmodifiedWater |                                   0.56|                                0.55|                              0.53|                              0.53|                              0.58|                           0.51|                           1.00|                                           1.00|                              0.52|                           0.47|                              0.52|                              0.51|                              0.56|
|convolved_hab_risk_2019_modisTEMP              |                                   0.98|                                0.97|                              0.69|                              0.98|                              0.97|                           0.84|                           0.52|                                           0.52|                              1.00|                           0.84|                              0.97|                              0.99|                              0.96|
|convolved_hab_risk_2019_NOtemp                 |                                   0.83|                                0.83|                              0.60|                              0.85|                              0.81|                           0.99|                           0.47|                                           0.47|                              0.84|                           1.00|                              0.84|                              0.83|                              0.81|
|convolved_hab_risk_2021_modisTEMP              |                                   0.95|                                0.96|                              0.66|                              0.98|                              0.95|                           0.83|                           0.52|                                           0.52|                              0.97|                           0.84|                              1.00|                              0.97|                              0.93|
|convolved_hab_risk_2023_modisTEMP              |                                   0.97|                                0.97|                              0.68|                              0.98|                              0.96|                           0.82|                           0.51|                                           0.51|                              0.99|                           0.83|                              0.97|                              1.00|                              0.96|
|convolved_hab_risk_2025_modisTEMP              |                                   0.99|                                0.98|                              0.74|                              0.94|                              0.96|                           0.84|                           0.56|                                           0.56|                              0.96|                           0.81|                              0.93|                              0.96|                              1.00|


:::
:::


Check the water temp suitability layers

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-15-1.png){width=672}
:::
:::


#### Normalized relative convolved risk  

The normalization likely needs to change to relative to optimal habitat suitability rather than max pixel in image. 

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-16-1.png){width=672}
:::

::: {.cell-output-display}


Table: Pearson's correlations

|                                                      | normalized_convolved_risk_2013_2026_modisTEMP| normalized_convolved_risk_2013_2026_NoTemp| normalized_convolved_risk_2013_modisTEMP| normalized_convolved_risk_2015_modisTEMP| normalized_convolved_risk_2017_modisTEMP| normalized_convolved_risk_2019_BTtemp| normalized_convolved_risk_2019_L8temp| normalized_convolved_risk_2019_L8temp_unmodifiedWater| normalized_convolved_risk_2019_modisTEMP| normalized_convolved_risk_2019_NOtemp| normalized_convolved_risk_2021_modisTEMP| normalized_convolved_risk_2023_modisTEMP| normalized_convolved_risk_2025_modisTEMP|
|:-----------------------------------------------------|---------------------------------------------:|------------------------------------------:|----------------------------------------:|----------------------------------------:|----------------------------------------:|-------------------------------------:|-------------------------------------:|-----------------------------------------------------:|----------------------------------------:|-------------------------------------:|----------------------------------------:|----------------------------------------:|----------------------------------------:|
|normalized_convolved_risk_2013_2026_modisTEMP         |                                          1.00|                                       0.99|                                     0.73|                                     0.96|                                     0.97|                                  0.85|                                  0.56|                                                  0.56|                                     0.98|                                  0.83|                                     0.95|                                     0.97|                                     0.99|
|normalized_convolved_risk_2013_2026_NoTemp            |                                          0.99|                                       1.00|                                     0.72|                                     0.97|                                     0.96|                                  0.84|                                  0.55|                                                  0.55|                                     0.97|                                  0.83|                                     0.96|                                     0.97|                                     0.98|
|normalized_convolved_risk_2013_modisTEMP              |                                          0.73|                                       0.72|                                     1.00|                                     0.69|                                     0.69|                                  0.64|                                  0.53|                                                  0.53|                                     0.69|                                  0.60|                                     0.66|                                     0.68|                                     0.74|
|normalized_convolved_risk_2015_modisTEMP              |                                          0.96|                                       0.97|                                     0.69|                                     1.00|                                     0.95|                                  0.83|                                  0.53|                                                  0.53|                                     0.98|                                  0.85|                                     0.98|                                     0.98|                                     0.94|
|normalized_convolved_risk_2017_modisTEMP              |                                          0.97|                                       0.96|                                     0.69|                                     0.95|                                     1.00|                                  0.81|                                  0.58|                                                  0.58|                                     0.97|                                  0.81|                                     0.95|                                     0.96|                                     0.96|
|normalized_convolved_risk_2019_BTtemp                 |                                          0.85|                                       0.84|                                     0.64|                                     0.83|                                     0.81|                                  1.00|                                  0.51|                                                  0.51|                                     0.84|                                  0.99|                                     0.83|                                     0.82|                                     0.84|
|normalized_convolved_risk_2019_L8temp                 |                                          0.56|                                       0.55|                                     0.53|                                     0.53|                                     0.58|                                  0.51|                                  1.00|                                                  1.00|                                     0.52|                                  0.47|                                     0.52|                                     0.51|                                     0.56|
|normalized_convolved_risk_2019_L8temp_unmodifiedWater |                                          0.56|                                       0.55|                                     0.53|                                     0.53|                                     0.58|                                  0.51|                                  1.00|                                                  1.00|                                     0.52|                                  0.47|                                     0.52|                                     0.51|                                     0.56|
|normalized_convolved_risk_2019_modisTEMP              |                                          0.98|                                       0.97|                                     0.69|                                     0.98|                                     0.97|                                  0.84|                                  0.52|                                                  0.52|                                     1.00|                                  0.84|                                     0.97|                                     0.99|                                     0.96|
|normalized_convolved_risk_2019_NOtemp                 |                                          0.83|                                       0.83|                                     0.60|                                     0.85|                                     0.81|                                  0.99|                                  0.47|                                                  0.47|                                     0.84|                                  1.00|                                     0.84|                                     0.83|                                     0.81|
|normalized_convolved_risk_2021_modisTEMP              |                                          0.95|                                       0.96|                                     0.66|                                     0.98|                                     0.95|                                  0.83|                                  0.52|                                                  0.52|                                     0.97|                                  0.84|                                     1.00|                                     0.97|                                     0.93|
|normalized_convolved_risk_2023_modisTEMP              |                                          0.97|                                       0.97|                                     0.68|                                     0.98|                                     0.96|                                  0.82|                                  0.51|                                                  0.51|                                     0.99|                                  0.83|                                     0.97|                                     1.00|                                     0.96|
|normalized_convolved_risk_2025_modisTEMP              |                                          0.99|                                       0.98|                                     0.74|                                     0.94|                                     0.96|                                  0.84|                                  0.56|                                                  0.56|                                     0.96|                                  0.81|                                     0.93|                                     0.96|                                     1.00|


:::
:::


### Compare convolved hab risk to snail data  

::: {.cell}
::: {.cell-output .cell-output-stdout}

```
[1] "missing coords for 13 observations in ZEST snails"
```


:::

::: {.cell-output .cell-output-stdout}

```
[1] "missing coords for 0 observations in SchistoBreak snails"
```


:::
:::


### ZEST snails

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-18-1.png){width=672}
:::

::: {.cell-output .cell-output-stdout}

```
[1] "B. globosus present"
```


:::

::: {.cell-output .cell-output-stdout}

```
       df      AIC
mod_BT 13 1768.919
mod_L8 13 1766.873
mod_NO 13 1767.755
```


:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-18-2.png){width=672}
:::
:::


### SchistoBreak Snails

::: {.cell}
::: {.cell-output .cell-output-stdout}

```
[1] "B. globosus present"
```


:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-19-1.png){width=672}
:::

::: {.cell-output .cell-output-stdout}

```
       df      AIC
mod_BT  9 3327.946
mod_L8  9 3313.761
mod_NO  9 3329.423
```


:::

::: {.cell-output .cell-output-stdout}

```
[1] "B. globosus infected"
```


:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-19-2.png){width=672}
:::

::: {.cell-output .cell-output-stdout}

```
       df      AIC
mod_BT  8 1180.571
mod_L8  8 1149.183
mod_NO  8 1174.058
```


:::
:::



## Population at risk 

### Normalized relative risk to population count (how many people are at risk)

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-20-1.png){width=672}
:::

::: {.cell-output-display}


Table: Pearson's correlations

|                                               | convolved_hab_risk_2013_2026_modisTEMP| convolved_hab_risk_2013_2026_NoTemp| convolved_hab_risk_2013_modisTEMP| convolved_hab_risk_2015_modisTEMP| convolved_hab_risk_2017_modisTEMP| convolved_hab_risk_2019_BTtemp| convolved_hab_risk_2019_L8temp| convolved_hab_risk_2019_L8temp_unmodifiedWater| convolved_hab_risk_2019_modisTEMP| convolved_hab_risk_2019_NOtemp| convolved_hab_risk_2021_modisTEMP| convolved_hab_risk_2023_modisTEMP| convolved_hab_risk_2025_modisTEMP|
|:----------------------------------------------|--------------------------------------:|-----------------------------------:|---------------------------------:|---------------------------------:|---------------------------------:|------------------------------:|------------------------------:|----------------------------------------------:|---------------------------------:|------------------------------:|---------------------------------:|---------------------------------:|---------------------------------:|
|convolved_hab_risk_2013_2026_modisTEMP         |                                   1.00|                                0.99|                              0.73|                              0.96|                              0.97|                           0.85|                           0.56|                                           0.56|                              0.98|                           0.83|                              0.95|                              0.97|                              0.99|
|convolved_hab_risk_2013_2026_NoTemp            |                                   0.99|                                1.00|                              0.72|                              0.97|                              0.96|                           0.84|                           0.55|                                           0.55|                              0.97|                           0.83|                              0.96|                              0.97|                              0.98|
|convolved_hab_risk_2013_modisTEMP              |                                   0.73|                                0.72|                              1.00|                              0.69|                              0.69|                           0.64|                           0.53|                                           0.53|                              0.69|                           0.60|                              0.66|                              0.68|                              0.74|
|convolved_hab_risk_2015_modisTEMP              |                                   0.96|                                0.97|                              0.69|                              1.00|                              0.95|                           0.83|                           0.53|                                           0.53|                              0.98|                           0.85|                              0.98|                              0.98|                              0.94|
|convolved_hab_risk_2017_modisTEMP              |                                   0.97|                                0.96|                              0.69|                              0.95|                              1.00|                           0.81|                           0.58|                                           0.58|                              0.97|                           0.81|                              0.95|                              0.96|                              0.96|
|convolved_hab_risk_2019_BTtemp                 |                                   0.85|                                0.84|                              0.64|                              0.83|                              0.81|                           1.00|                           0.51|                                           0.51|                              0.84|                           0.99|                              0.83|                              0.82|                              0.84|
|convolved_hab_risk_2019_L8temp                 |                                   0.56|                                0.55|                              0.53|                              0.53|                              0.58|                           0.51|                           1.00|                                           1.00|                              0.52|                           0.47|                              0.52|                              0.51|                              0.56|
|convolved_hab_risk_2019_L8temp_unmodifiedWater |                                   0.56|                                0.55|                              0.53|                              0.53|                              0.58|                           0.51|                           1.00|                                           1.00|                              0.52|                           0.47|                              0.52|                              0.51|                              0.56|
|convolved_hab_risk_2019_modisTEMP              |                                   0.98|                                0.97|                              0.69|                              0.98|                              0.97|                           0.84|                           0.52|                                           0.52|                              1.00|                           0.84|                              0.97|                              0.99|                              0.96|
|convolved_hab_risk_2019_NOtemp                 |                                   0.83|                                0.83|                              0.60|                              0.85|                              0.81|                           0.99|                           0.47|                                           0.47|                              0.84|                           1.00|                              0.84|                              0.83|                              0.81|
|convolved_hab_risk_2021_modisTEMP              |                                   0.95|                                0.96|                              0.66|                              0.98|                              0.95|                           0.83|                           0.52|                                           0.52|                              0.97|                           0.84|                              1.00|                              0.97|                              0.93|
|convolved_hab_risk_2023_modisTEMP              |                                   0.97|                                0.97|                              0.68|                              0.98|                              0.96|                           0.82|                           0.51|                                           0.51|                              0.99|                           0.83|                              0.97|                              1.00|                              0.96|
|convolved_hab_risk_2025_modisTEMP              |                                   0.99|                                0.98|                              0.74|                              0.94|                              0.96|                           0.84|                           0.56|                                           0.56|                              0.96|                           0.81|                              0.93|                              0.96|                              1.00|


:::
:::



### Compare to prevalence data (schools only) 

::: {.cell}

:::


### ZEST schools

::: {.cell}
::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-22-1.png){width=672}
:::

::: {.cell-output-display}
![](index_files/figure-html/unnamed-chunk-22-2.png){width=672}
:::

::: {.cell-output .cell-output-stdout}

```
       df      AIC
mod_BT 20 4281.382
mod_L8 20 4591.576
mod_NO 20 4295.191
```


:::
:::



