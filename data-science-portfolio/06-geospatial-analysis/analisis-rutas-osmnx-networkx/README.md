# Análisis de Rutas Urbanas con OpenStreetMap (Salta, Argentina)

Este proyecto explora la red vial de la ciudad de Salta utilizando datos de OpenStreetMap, con el objetivo de analizar y comparar distintos algoritmos de búsqueda de rutas.
Se aplican técnicas de análisis de grafos para modelar la ciudad como una red de nodos y aristas, permitiendo evaluar la eficiencia de distintos métodos de búsqueda en un contexto urbano real.

## Objetivos

- Obtener y visualizar la red de calles de Salta.
- Modelar la red como un grafo.
- Aplicar algoritmos de búsqueda de caminos:
  - BFS (Breadth-First Search)
  - DFS (Depth-First Search)
  - A* (A-star)
- Comparar el rendimiento de los algoritmos en términos de:
  - Tiempo de ejecución
  - Nodos explorados
  - Longitud del camino
- Visualizar las rutas obtenidas.

## Datos

Los datos se obtienen de **OpenStreetMap** utilizando la librería OSMnx.
Se trabaja con la red vial de tipo `drive`, que representa las calles transitables por vehículos.

## Tecnologías

- Python  
- OSMnx  
- NetworkX  
- GeoPandas  
- Folium  
- Matplotlib

## Metodología

1. Descarga del grafo urbano de Salta.
2. Conversión a GeoDataFrames para análisis.
3. Selección de puntos de origen y destino.
4. Aplicación de algoritmos de búsqueda:
   - BFS
   - DFS
   - A*
5. Medición de métricas de rendimiento.
6. Visualización de resultados.

## Resultados

Comparación del rendimiento de los algoritmos en términos de tiempo de ejecución, longitud del recorrido y cantidad de nodos explorados.
Incluye representaciones gráficas de cada ruta calculada.

### Observaciones:

- **A\*** mostró mayor eficiencia en la búsqueda del camino óptimo.
- **BFS** encuentra rutas óptimas en grafos no ponderados, pero puede explorar muchos nodos.
- **DFS** no garantiza el camino más corto y explora una mayor cantidad de nodos.

## Conclusiones

El uso de algoritmos de búsqueda en redes urbanas permite analizar la eficiencia de distintas estrategias de navegación.
Este tipo de análisis tiene aplicaciones en:

- optimización de rutas  
- logística  
- transporte urbano  
- planificación territorial  

## Notebook

Podés ver la implementación completa en el siguiente enlace:
[Google Colab - Análisis de Rutas Urbanas](https://colab.research.google.com/drive/1Lj_rhh9xVRDACefTHQS01Ln2lQekWLU5#scrollTo=V5ZbOeROxT30)

--------------------------------------------------------------------------------

# Urban Route Analysis with OpenStreetMap (Salta, Argentina)

This project explores the road network of the city of Salta using OpenStreetMap data, with the objective of analyzing and comparing different pathfinding algorithms.

Graph analysis techniques are applied to model the city as a network of nodes and edges, allowing the evaluation of the efficiency of different search methods in a real urban context.

## Objectives

- Obtain and visualize the road network of Salta.
- Model the network as a graph.
- Apply pathfinding algorithms:
  - BFS (Breadth-First Search)
  - DFS (Depth-First Search)
  - A* (A-star)
- Compare algorithm performance in terms of:
  - Execution time
  - Explored nodes
  - Path length
- Visualize the resulting routes.

## Data

Data is obtained from **OpenStreetMap** using the OSMnx library.  
The project uses the `drive` network type, representing streets accessible by vehicles.

## Technologies

- Python  
- OSMnx  
- NetworkX  
- GeoPandas  
- Folium  
- Matplotlib  

## Methodology

1. Download the urban graph of Salta.
2. Convert the graph into GeoDataFrames for analysis.
3. Select origin and destination points.
4. Apply pathfinding algorithms:
   - BFS
   - DFS
   - A*
5. Measure performance metrics.
6. Visualize results.

## Results

Comparison of algorithm performance in terms of execution time, route length, and number of explored nodes.  
Includes graphical representations of each computed route.

### Observations:

- **A\*** showed the highest efficiency in finding the optimal path.
- **BFS** finds optimal paths in unweighted graphs but may explore many nodes.
- **DFS** does not guarantee the shortest path and explores a larger number of nodes.

## Conclusions

The use of search algorithms in urban networks allows the evaluation of different navigation strategies.
This type of analysis has applications in:

- route optimization  
- logistics  
- urban transportation  
- territorial planning  

## Notebook

You can view the full implementation at the following link:  
[Google Colab - Urban Route Analysis](https://colab.research.google.com/drive/1Lj_rhh9xVRDACefTHQS01Ln2lQekWLU5#scrollTo=V5ZbOeROxT30)
