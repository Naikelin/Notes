# Sistemas de Telefonía Celular

Tecnología celular posibilita el acceso de usuarios a lugares dificilmente alcanzables. Tecnología celular recae en sistemas de comunicaciones personales, acceso inalámbrico a Internet, aplicaciones web y más.

## Red celular
Uso de múltiples transmisores de baja **potencia**.  Asímismo, la transmisión en un área puede ser dividida en distintas celdas, donde cada una disponte de *antenas*.
Cada celda posee una estación base, la cual se compone de: *Transmisor*, *Receptor* y *Unidad de Control*.
Celdas *adyacentes* reciben asignación de distintas frecuencias, así no se interfieren.

### Organización de una red celular

![[Drawing 2022-06-06 15.45.31.excalidraw|800]]



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
-

## Interferencias
Existen dos tipos de *interferencia*.
### Cocanal
Provocada por la recepción no deseada de señales provenientes del mismo canal RF asociado a otro cluster.
### Canal adyacente
Provocada por la recepción de señales no deseadas por los canales vecinos.

## Factor de reutilización

![[Drawing 2022-06-06 17.40.58.excalidraw|800]]