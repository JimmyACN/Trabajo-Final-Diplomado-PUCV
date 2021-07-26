# Trabajo-Final-Diplomado-PUCV

# 1 Título, Autor y control de versiones (4 puntos).

#     1.1 Evaluacion del efecto de la densidad de cultivo el volumen de estanques en la intensidad de luz de dos modulos de sietemas de cultivo RAS. 

#     1.2 Jimmy Carrillo Novoa. 


# 2 Resumen del problema a resolver (4 puntos).

#     2.1 Se requiere saber si la intensidad de luz medida watt/m2 en el fondo del estanque es influenciada por el tamaño del estanque y la densidad de cultivo. Para medir el efecto en la intensidad de luz se usara un set de datos de una granja de peces con Sistema RAS, se analizaran 272 mediciones en dos módulos diferentes de cultivo-Moduo A y Modulo B.


# 3 Resumen de los datos originales (4 puntos).

#  Density         Volume_m3         Tank              Module         
 Min.   : 17.00   Min.   : 50.0   Length:272         Length:272        
 1st Qu.: 55.00   1st Qu.: 50.0   Class :character   Class :character  
 Median : 71.00   Median :200.0   Mode  :character   Mode  :character  
 Mean   : 70.47   Mean   :134.9                                        
 3rd Qu.: 84.12   3rd Qu.:200.0                                        
 Max.   :116.00   Max.   :200.0                                        
 Light_Intensity_watt/sq2
 Min.   :0.00100         
 1st Qu.:0.05175         
 Median :0.11000         
 Mean   :0.13058         
 3rd Qu.:0.17525         
 Max.   :0.80000         

# 4 Resumen de los métodos estadísticos utilizados (4 puntos)

## 1-Se realizara un modelo de efectos fijo-"Modelo_1"" con variable respuesta light_intensity y como efectos fijos del modelo las variables densidad y volumen del estanque. 

## 2- Se realizara un modelo lineal mixto-"Modelo_2"" con la variable respuesta light y como efectos fijos del modelo las variables densidad y volumen del estanque, la variabble modulo se usara como efecto aleatorio.

## 3- Se realizara un ajuste al modelo anterior "Modelo_2-Ajust"" como efectos fijos densidad de cultivo y el volumen, la interaccion densidad volumen y como efecto aleatorio el Modulo. 

## Luego se determinara cual es el mejor modelo para analizar el efecto de las variables sobre la variable respuesta light. 


# Porgress on July 18.

## 1- Se incluyen librerias 
## 2- Exploratorio del set de datos light_Intensity.xlsx
## 3- Ajuste de la variable del set de datos
## 4- Resumen estadistico de la variables del set de datos
## 5- Exploratorio de las variables.
## 6- Modelo de efectos fijos.


## Progess on July 19 *****

## ## MODELOS LINEALES MIXTOS##

        ## Modelo de efectos fijos.
        ## Modelo con efectos aleatorios 
        ## Comparacion de los modelos aleatorios
        
## Progress on July 20 *****

## ANALISIS PARTE 1

##ANALISIS DE MODELOS LINEALES MIXTOS DE EFECTOS FIJOS Y EFECTOS ALEATORIOS PARA EL ANALISIS DEL EFECTO DE LA DENSIDAD DE CULTIVO, EL VOLUMEN DEL ESTANQUE SOBRE LA INTENSIDAD DE LUZ

## La variable respuesta no tiene distribucion normal por lo tanto no es posible concluir a travez del analisis mediante Modelos Lineals Mixtos.

## ANALISIS PARTE 2

##ANALISIS DE MODELOS LINEALES GENERALIZADOS PARA EL ANALISIS DEL EFECTO DE LA DENSIDAD DE CULTIVO, EL VOLUMEN DEL ESTANQUE SOBRE LA INTENSIDAD DE LUZ.

## Se realiza analisi mediante 7 modelos distintos:

## Modelo 1             mod.g1 <- glm(watt_sq2 ~ 1, family= binomial, data = light) Componentes nulo

## Modelo 2             mod.g2 <- glm(watt_sq2 ~ Density, family= binomial, data = light) 

## Modelo 3             mod.g2a <- glm(watt_sq2 ~ Density, family= binomial(link="cloglog"), data = light)                          enlace canonico cloglog

## Modelo 4             mod.g2aa <- glm(watt_sq2 ~ Density+Module, family= binomial(link="cloglog"), data =                         light) enlace canocico cloglog y efecto de density mas Module

## Modelo 5             mod.g2ab <- glm(watt_sq2 ~ Density, family= binomial(link=probit), data = light)                            enlace canonico probit

## Modelo 6             mod.g2ab1 <- glm(watt_sq2 ~ Density:Module, family= binomial(link=probit), data =                           light) encale canonico probit sobre efecto entre densidad y module 

## Modelo 7             mod.g2aab <- glm(watt_sq2 ~ Density+Volume_m3, family= binomial(link="cloglog"),                            data = light) enlace canonico cloglog con sobre efecto density mas volume.

## CONCLUSIONES PRELIMINARES

## De acuerdo al analisis anova la suma de cuadrados residuales de modelo 7 es menor al resto de los modelos, por lo tanto el modelo 7 Model 7: watt_sq2 ~ Density + Volume_m3 se ajusta de mejor a los datos analizados. De acuerdo al analisis anova se puede decir que la densidad de cultivo y el volumen del estanque tienen un efecto en la intensidad de luz. Conclusion del analisis 2: Mediante un analisis modelos generales linealizados se puede predecir el efecto de la densidad y del tamano del estqanque sobre la intensdad de la luz medida. 


## Progress on July 23


# Se agrega al reporte: 

warning=FALSE and message=FALSE en el primer bloque de códigos.

Se inclutye los itmes al archivo Rmarkdown: 

Título y autor.
Planteamiento del problema a resolver (4 puntos).
Descripción detallada de los datos originales (4 puntos).
Análisis exploratorio de datos (4 puntos).
Análisis estadístico de los datos (4 puntos).
Interpretación de los resultados y conclusión (4 puntos) 

# Progress on July 26 FINAL REPORTING 

Modelamiento GLM para el set de datos.
Calculo de tres modelos GLM
        Modeo nulo
        Modelo saturado
        Modelo completo
Calculo de p-values para cada modelo
Calculo de AIC para cada modelo
Seleccion del Modelo
Calculo de DEVIANCE para Modelo Seleccionado
Conclusiones. 



