# Informe TPComplejidadAlgoritmica

1. Problema
2. Dataset
3. Algoritmos 
    3.1 Fuerza Bruta
    3.2 Algoritmo UCS

## Problema
   Dada una lista de ciudades y las distancias entre ellas.
   ¿Cual es la ruta mas corta posible que visite todas las ciudades y regrese donde inicio?

## Dataset
   Dataset recogida de http://sigmed.minedu.gob.pe/descargas/, aproximadamente son 150mil datos, los cuales son convertidos en un clase
   llamada Point que contiene: Name, Longitud y Latiudad.

## Algoritmos
   Para la resolucion del problema, tomamos dos puntos de vista diferentes, el primero es la union de todos los nodos con la ruta mas corta posible,
   pero esto tiene un uso de recursos elevados y un tiempo demasiado largo. El segundo punto de vista es la mayor cantidad de nodos con la menor ruta posible,
   la cual es rapida pero no logra unir todos los puntos.

### Algoritmo Fuerza Bruta
   Este algoritmo busca unir todos los nodos en la menor distancia posible.  
   Primero se generan todas las posible rutas, de ahi se recorre cada ruta, se calcula la distancia y se suma. Finalmente regresa la distancia menor y su recorrido.

### Algoritmo UCS
   Este algoritmo busca unir la mayor cantidad de nodos posibles en la menor distancia posible.
   Busca la ruta mas corta de un punto de los nodso que no han sido visitados, guardo su peso en una cola, revisa cada peso de la cola y la vuelve a buscar, si el nuevo peso
   es menor lo guarda, el algoritmo termina cuando se revisan todos los elementos de la cola.