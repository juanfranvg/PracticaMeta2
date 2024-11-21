# PracticaMeta2
Para el desarrollo de esta práctica, se ha optado por la implementación desde cero de uno de los algoritmos metaheurísticos propuestos, utilizando el lenguaje de programación Java y el entorno de desarrollo integrado IntelliJ IDEA. Con el objetivo de facilitar la experimentación y la reproducibilidad de los resultados, se ha diseñado una arquitectura modular que permite parametrizar los experimentos a través de un archivo de configuración (config.txt). Este archivo centraliza todos los parámetros necesarios para la ejecución de cualquiera de los tres algoritmos implementados. Los parámetros son los siguientes:

archivos: Aquí indicaremos el nombre de los archivos con los que vamos a trabajar, semillas: Permutación de números a partir de nuestros DNIs explicado en informe, algoritmos: Algoritmos metaheurísticos que hemos desarrollado para la ejecuciónd de la práctica, k: es el número máximo que aplicaremos para escoger la ciudad aleatoria (es decir entre 1 y k), iteraciones: número máximo de reitera el algoritmo, tiempo: tiempo máximo de ejecución límite para la evolución, cruce: nombre de los operadores de cruce que utilizaremos en la ejecución, m: número de individuos en la población, e: se corresponde con las dos combinaciones de elitismo que utilizaremos, kBest: se corresponde con las dos combinaciones de torneo que se realizarán en las ejecuciones para el cruce, kWorst: se corresponde con el número de individuos para el torneo a la hora de elegir el peor, probMuta: probabilidad para la mutación del individuo, probCruce: probabilidad para la operación de cruce, por: Porcentaje de inicialización aleatoria para los individuos, kBestEst: se corresponde con las dos combinaciones de torneo que se realizarán en las ejecuciones para el cruce en el caso del algoritmo Estacionario, kWorstEst: se corresponde con el número de individuos para el torneo a la hora de elegir el peor en el caso del algoritmo Estacionario.

Ejemplo:
archivos:a280.tsp ch130.tsp d18512.tsp pr144.tsp u1060.tsp
semillas:77691602 02166977 69160277
algoritmos:Estacionario
k:5
iteraciones:50000
tiempo:60000
cruce:OX2 MOC
m:100
e:1 2
kBest:2 3
kWorst:3
probMuta:10
probCruce:70
por:0.8
kBestEst:2
kWorstEst:2

Una vez comienza la ejecución, procedemos a leer los diferentes archivos indicados a través de unas líneas de código que extraerán de estos archivos los datos necesarios para posteriormente guardarlos y poder usarlos en nuestro algoritmo.

Después de este procedimiento los archivos de logs quedarán guardados en la carpeta logs, donde podremos consultar las soluciones, costes, tiempos e iteraciones.

