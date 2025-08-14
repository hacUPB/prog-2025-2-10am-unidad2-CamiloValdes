# Taller algoritmos  

 
## Punto 1 - Verificación de peso de despegue
En una pista de pruebas de aeronaves, el sistema debe verificar si el peso total de la aeronave, incluyendo combustible y carga, supera el límite máximo permitido para el despegue. Dependiendo del resultado, el sistema deberá indicar si la aeronave está lista para despegar o si debe reducir carga o combustible.


|Variables|Tipo|Notas|
|---------|----|-----|
|peso maximo|Entrada|el peso maximo para despegar|
|peso_aeronave|Entrada|el peso calculado con combustible y carga|
|peso_exceso|salida|el peso por el que la aeronave supera el maximo

```
Inicio
Leer peso_aeronave
    Si peso_aeronave > peso_maximo
        peso_exceso = peso_aeronave - peso_maximo
        Escribir "La aeronave no puede despegar", "su aeronave supera el peso maximo por:", peso_exceso "Kg"
    Si no 
        Escribir "La aeronave esta lista para despegar"
    Fin Si
Fin
```
## Punto 3 - Registro de altitudes de vuelo

Un sistema debe registrar la altitud de vuelo cada 10 minutos durante una hora y mostrar todas las mediciones al final.
|Variables|Tipo|Comentario|
|---------|----|----------|
|Altitud|Entrada|Altitudes ingresadas|
|Contador|Salida|Mediciones|
|Lista|Salida|Altitudes registradas|


```
Inicio
    contador = 0
    Mientras contador < 6 :
          Escribir "Ingrese la altitud de vuelo en metros:"
          leer Altitud
          Lista[contador] = Altitud
          contador = contador + 1
    Fin Mientras
    Desde contador = 0 hasta contador = 6
         Escribir "Altitudes registradas:"
         Escribir Lista[contador]
    Fin Desde
Fin
```


## Punto 5 - Detección de turbulencia en trayecto
Un sensor mide la aceleración vertical de la aeronave en intervalos de un segundo durante un trayecto de 2 minutos. Si el valor medido supera un umbral, indicar que se ha detectado turbulencia en ese instante. Al final, mostrar cuántas turbulencias se detectaron.

|Variables|Tipo|Comentario|
|---------|----|----------|
|Umbral|Constante|Umbral de referencia|
|acel|Variable|aceleración vertical de la aeronave|
|i|Variable intermedia|Intervalos de segundo durante dos segundos|


```
Inicio
Umbral = 500
para i=1 hasta i=120
    leer acel
    Si acel > umbral
        Escribir "Turbulencia detectada" , acel
    Fin si 
Fin para 
Fin     
```
## Hecho por Camilo Valdés Montoya, Jose Alejandro Granados y Santiago Bustamante