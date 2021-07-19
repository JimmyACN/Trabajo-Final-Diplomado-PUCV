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


## Progess on July 19

## ## MODELOS LINEALES MIXTOS##

        ## Modelo de efectos fijos.
        ## Modelo con efectos aleatorios 

