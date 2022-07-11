# Control 5-6 -Arquitectura y tráfico celular
- Tecnología: AMPS  
- N = 19
- Número de sectores: 3  
- Tráfico cursado por sector: 2,85 E  
-  Disciplina de atención: llamadas bloqueadas perdidas  
-  Grado de servicio experimentado: 5%

Preguntas:

- Determine el número mínimo de portadoras de radiofrecuencia a instalar por sector, por celda y por clúster

- Suponga que no se aplica sectorización. ¿Qué grado de servicio se experimentaría en este caso, si se mantuviera el número de canales calculados por usted en el punto anterior, en cada celda?

- En vista de los resultados obtenidos en los casos anteriores, ¿qué diseño presentaría mayor robustez frente a alzas de  tráfico más allá del calculado sobre la hora cargada? Argumente.


# Control teoría de tráfico

Una celda de telefonía celular GSM está dividida en tres sectores de igual área: sector X, sector Y y sector Z. Cada  
uno de los sectores administra de forma separada cuántos canales de radiofrecuencia requiere para cumplir con cierto  
grado de servicio (Erlang-B).  
  
• El sector X cubre un área de 1 Km2. Distintas observaciones permiten deducir que los usuarios enganchados  
a dicho sector generan en promedio una demanda de 8.5 E.  
• El sector Y tiene configurados 3 ARFCN. La central celular muestra que este sector porta en promedio 20 E  
de tráfico.  
• El sector Z posee una densidad de tráfico ofrecido de 18 E/Km2.

Responda ordenadamente a las siguientes preguntas:  
  
a. ¿Cuántos canales de radiofrecuencia se debe instalar en el Sector X, si éste debe cumplir con un 1% de GOS?

b. ¿Cuál es la probabilidad de bloqueo experimentada por el Sector Y?

c. ¿Qué podría decir sobre el grado de servicio del Sector Z si éste cuenta con 8 canales de tráfico disponibles en sus instalaciones?


# GOS - Control llamadas bloqueadas con retorno

La instalación de una celda de telefonía celular analógica AMPS requiere de una probabilidad de bloqueo (Erlang B) del 5%. Un estudio de demanda de tráfico reflejó que el área cubierta por el sistema ofrece un máximo de 30 [E] a la hora cargada, uniformemente distribuido en el espacio. A su vez, se observó que  frente a la existencia de congestión (bloqueo por saturación de enlaces), el 80% de la demanda no satisfecha retornará. Suponga que el tráfico ofrecido se distribuye uniformemente en el espacio.  
	a) Determine el número de canales a instalar en la celda para cumplir con la condición de bloqueo especificada en el enunciado.  
	b) Suponga ahora que la celda se divide en tres sectores de 120º cada uno. ¿Cuántos canales se requerirá en cada sector para seguir cumpliendo con las condiciones del enunciado?  
En caso de ser necesario, explicite claramente vuestras suposiciones.