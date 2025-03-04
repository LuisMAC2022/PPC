# Cluster para Programacion Paralela y Concurrente \

El objetivo de este repositorio es recopilar los recursos que se han generado para el desarrollo del proyecto. 

Reporte incial sobre como hacer un cluster e investigacion de las tecnologias de manejo de contenedores:

* <a href="https://www.canva.com/design/DAGfR4a7whA/i02xSP3xdR74fdKJOCp10Q/edit"> Clusters </a> 
* <a href="https://www.github.com/LuisMAC2022/PPC/blob/main/PDFs/AM.pdf"> Apache Mesos  </a> 
* <a href="https://www.github.com/LuisMAC2022/PPC/blob/main/PDFs/CO.pdf"> Docker Swarm y Kubernetes </a> 

Se realizaron tutoriales para:
 
* <a href="https://www.github.com/im-krizox/docker-project">Configurar un Cluster de Apache Spark en Docker Swarm </a> 
* <a href="https://www.github.com/eithan-hernandez/docker-cluster/tree/main">Montar una imagen de docker </a> 

A partir de los formularios enviados se genero:
* <a href="https://colab.research.google.com/drive/1aXXY24Kl7g5tQ1uE5Y7ldFCwUa_98sqV?usp=sharing ">Inventario de recursos
</a> 
* <a href="https://colab.research.google.com/drive/1ir-V35nmYBEi7nEbl2I3YDB2-lSpZrXs?usp=sharing
">Analisis de Hardware</a> 

Tras el analisis se llegaron a las siguientes recomendaciones:  


Más potente según Benchmark:

    1.- Mac M2 Pro (34628) de López Núñez Gustavo Isaac
    2.- i5-11400H (31278) de Huerta Orozco Yago Raúl
    3.- Ryzen 5 5500U (20148) de Baeza Guerrero Roberto


Recomendaciones
Candidato a Nodo Maestro:

    Laptop de Baeza Guerrero Roberto (Ryzen 5 5500U) equilibra un buen puntaje (20148) y 1 Gbps Ethernet nativo.

Alternativa: 
    Laptop de Huerta Orozco Yago Raúl (i5-11400H) con mayor potencia, pero solo 100 Mbps. O laptop de López Núñez Gustavo Isaac (M2 Pro) con el mejor benchmark, pero requiere adaptador Ethernet.

Rol de Equipos con Menor Rendimiento:

    Laptops de Martinez Arana Luis Daniel, Alvarado Reyes Jorge Miguel y Castillo Hernandez Nestor Eithan  podrían dedicarse a tareas de baja demanda dentro del cluster, ya que su potencia/benchmark es limitado.

Confirmar Virtualización y Adquirir Adaptadores si es Necesario:

    Asegurarse de que “No estoy seguro” pase a “Habilitada” en BIOS.
    Adquirir adaptadores 1 Gbps para laptops sin puerto o con 100 Mbps.

Almacenamiento y Disco:

    Monitorear especialmente la laptop con HDD, pues podría ralentizar lecturas/escrituras de Spark.
    Asegurarse de tener espacio suficiente para contenedores Docker y datos intermedios (por ejemplo, #2 solo tiene 55 GB totales, lo cual puede quedarse corto).

Retomar o Repetir Benchmark si hay Dudas:

    Para Peralta Cortés Jorge Alejandro (Ryzen 5 4600H) se recomienda obtener el benchmark real, ya que podría estar cerca de Baeza Guerrero Roberto o Huerta Orozco Yago Raúl y convertirse en un buen candidato para nodo maestro.
    Para Alvarado Reyes Jorge Migue, investigar por qué el puntaje es tan bajo (2060) en un Ryzen 7 3700U.
