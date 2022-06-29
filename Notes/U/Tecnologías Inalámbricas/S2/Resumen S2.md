# Propagación Pequeña Escala
![[Drawing 2022-06-10 17.07.12.excalidraw|800]]
# Sistemas de Telefonía Celular

Tecnología celular posibilita el acceso de usuarios a lugares dificilmente alcanzables. Tecnología celular recae en sistemas de comunicaciones personales, acceso inalámbrico a Internet, aplicaciones web y más.

## Red celular
Uso de múltiples transmisores de baja **potencia**.  Asímismo, la transmisión en un área puede ser dividida en distintas celdas, donde cada una disponte de *antenas*.
Cada celda posee una estación base, la cual se compone de: *Transmisor*, *Receptor* y *Unidad de Control*.
Celdas *adyacentes* reciben asignación de distintas frecuencias, así no se interfieren.

### Organización de una red celular

![[Drawing 2022-06-06 15.45.31.excalidraw|600]]



### Reutilización de frecuencias
El punto importante para la reutilización de frecuencias, sin que estos interfieran entre si, es determinar cuántas celdas deben haber entre dos que utilicen la misma.
Pueden existir ciertos patrones para emplear una estrategia: clúster de 4, 7, 19 celdas... o más.

![[Drawing 2022-06-06 16.06.50.excalidraw|800]]

### Aumento de capacidad
Para hacer aumento de capacidad existen distintas estrategias:
- **Adición de nuevos canales**: Cuando se despliega en una región una red celular, es común que no se utilicen todos los canales. Es por esto que se pueden adicionar nuevos canales
- **Uso de frecuencias prestadas**: Celdas se prestan frecuencias adyacentes, o ir asignando frecuencias de manera dinámica.
- **División de celdas**: Las celdas pueden ser divididas en celdas aún más pequeñas. La cantidad de subceldas creadas, dependen netamente de características topográficas.
- **Sectorización de celdas**: Los transmisores utilizan antenas direccionales enfocadas en cada sector de una celda, donde cada una utiliza un conjunto de canales asignados al sector específico.
- **Microceldas**: El uso de microceldas permite una reducción de niveles de potencia en la estación base.. Es últil para zonas congestionadas, entre edificios, calles, etc.
### Organización de una red celular
Hay dos conceptos que se deben conocer:
- Al momento de que un móvil se desplaza entre una celda u otra, existe un traspaso de la estación base ***Handoff***.
- En una estación base, pueden existir cambios de canales ***Handover***.

## Interferencias
Existen dos tipos de *interferencia*.
### Cocanal
Provocada por la recepción no deseada de señales provenientes del mismo canal RF asociado a otro cluster.
### Canal adyacente
Provocada por la recepción de señales no deseadas por los canales vecinos.

## Factor de reutilización

![[Drawing 2022-06-06 17.40.58.excalidraw|1000]]

## Relación señal interferencia
![[Drawing 2022-06-06 18.09.22.excalidraw|800]]

## Funcionamiento

Existen algunos elementos principales en un sistema celular:

- **Estación base**: En el centro de cada celda. Contiene una *antena*, *controlador* y una *serie de transceptores* para al comunicación de los canales asignados. 
	- **Controlador**: Se usa para gestionar el proceso de llamada entre el móvil y el resto de la red.
- **MTSO**: Cada base se comunica con la MTSO, la cual debe ser una comunicación rápida y confiable (cableado). Se encarga de asignar un canal de voz a cada llamada, realizar traspasos y supervisar las llamadas para obtener la información para luego hacer cobros.

### Tipos de canales:
- **Canales de control**: Se usan para el intercambio de información para establecer y mantener una llamada. También se utiliza para mantener la conexión entre el móvil y la BS más cercana,
- **Canales de tráfico**: se utiliza para enviar información a través del medio.

## Pasos para llamada
![[Drawing 2022-06-06 19.04.45.excalidraw|800]]

## Mecanismos de acceso al medio
Existen principalmente tres mecanismos de acceso al medio

- **FDMA** (Frequency division multiple access): Se divide el espectro en distintas frecuencias, repartiendola para cada canal, donde un canal se usa para un usuario.
- **TDMA** (Time division multiple access): Se dividen los canales de uso en tiempo. Cada el canal se reparte al usuario en un cierto tiempo, para transmitir la información.
- **CDMA** (Code division multiple access): Se pueden transmitir muchas fuentes de datos en un solo canal, sin embargo, necesita mucho ancho de banda.


# Normas y Sistemas
## Telefonía celular
### Análoga
AMPS, ETACS y N-AMPS

![[Drawing 2022-06-07 13.16.35.excalidraw|800]]

#### USDC y GSM

### Digital
![[Drawing 2022-06-09 13.15.27.excalidraw|800]]