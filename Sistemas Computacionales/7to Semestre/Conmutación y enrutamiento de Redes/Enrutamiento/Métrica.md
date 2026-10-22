La métrica de red se refiere al valor asignado a una ruta estática en función de su costo o distancia estimada en relación a otras rutas disponibles. En otras palabras, la métrica de red es una medida de la eficiencia o calidad de una ruta determinada.

Esta métrica se utiliza en el proceso de selección de la ruta óptima para enviar un paquete de datos desde un origen a un destino a través de la red. El ruteo estático implica que el administrador de la red ha definido manualmente las rutas y las métricas asociadas, en lugar de dejar que los protocolos de enrutamiento dinámico determinen automáticamente las mejores rutas.

En situaciones donde hay varias rutas hacia la misma red remota, las métricas de routing se utilizan para determinar el “costo” total de una ruta de origen a destino. Los protocolos de routing determinan la mejor ruta sobre la base del costo más bajo.

Los diferentes protocolos de enrutamiento pueden usar diferentes métricas. La métrica utilizada por un protocolo de enrutamiento no es comparable con la métrica utilizada por otro protocolo de enrutamiento. Dos protocolos de routing distintos pueden elegir diferentes rutas hacia el mismo destino.

En el siguiente video, se muestra que el protocolo RIP elegiría la ruta con la menor cantidad de saltos, mientras que el protocolo OSPF elegiría la ruta con el mayor ancho de banda.

![[7.1.4.8 Métricas de los protocolos de routing - Brave 2026-10-19 11-38-18.mp4]]

Algunas de las métricas comunes utilizadas en el ruteo estático incluyen:
- **Costo:** Es el valor asignado a una ruta en función de su costo estimado en términos de tiempo, ancho de banda o cualquier otro factor que pueda influir en su rendimiento.
- **Distancia:** Es la medida de la distancia física o lógica entre el origen y el destino de la ruta.
- **Ancho de banda:** Es la cantidad de datos que se pueden transferir por segundo a través de la ruta.
- **Retardo:** Es el tiempo que tarda un paquete de datos en viajar a través de la ruta.
- **Confiabilidad:** Es la probabilidad de que la ruta esté disponible y funcione correctamente.

Los siguientes son algunos ejemplos prácticos de cómo se utiliza la métrica de red en el ruteo estático:

- Supongamos que una empresa tiene dos routers conectados a su red interna, y uno de ellos está conectado a una red externa. El administrador de la red ha definido una ruta estática a través del router conectado a la red externa para acceder a un servidor externo. Para determinar la mejor ruta, el administrador puede asignar una métrica de costo a cada ruta disponible. Si la ruta a través del router conectado a la red externa tiene un costo más bajo en términos de tiempo y ancho de banda, se seleccionará como la ruta óptima.

- Otra empresa tiene varias sucursales ubicadas en diferentes ciudades, cada una con una conexión a Internet separada. El administrador de la red ha definido varias rutas estáticas entre las sucursales para permitir la comunicación directa entre ellas. Para determinar la mejor ruta para enviar datos entre dos sucursales, el administrador puede asignar una métrica de distancia a cada ruta disponible. Si una ruta tiene una distancia menor, se seleccionará como la ruta óptima.
