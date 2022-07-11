## Dimensionamiento de canales telefónicos
**Trunking**: Número fijo de canales que dan servicio a X usuarios. Aprovecha el comportamiento estadístico de los usuarios.
*Mientras menor sea la cantidad de canales, mayor probabilidad de un usuario tenga su linea bloqueada por no disponibilidad*

-> Para enfrentar el problema: *Llamadas bloqueadas perdidas/retornadas*.

## Definiciones
**Set-up time**: tiempo requerido para asignar un canal de RF a un usuario que lo solicita.
**Holding time**: duración promedio de una llamada en segundo $T_m [s]$.
**Traffic Intensity**: medida de utilización del canal, utilizando la ocupación media en *Erlangs*  $A [E]$. { $1 E$ => utilización de una linea durante $1 hr$. }
**Load**: carga de la red. Se mide en *Erlangs*.
**Grade of service (GOS)**: probabilidad de que una llamada sea bloqueada *Erlang B* o demorada luego de cierto tiempo *Erlang C*.
**Request rate**: número medio de solicituded de conexión por unidad de tiempo $\lambda[\frac{1}{s}]$.
**Hora cargada**: hora del día, semana, mes o año en el que se registra el mayor tráfico telefónico.

## Modelamiento de trafico
Se asume existen llamadas telefónicas cuyo tiempo entre arribos es exponencial a una tasa $\lambda$.
El número de llamadas que arriban al sistema en cierto intervalo de tiempo sigue un proceso de conteo de Poisson de parámetro $\lambda$. => $\mu = \Delta t \cdot \lambda$

**Tráfico ofrecido**
Entonces, cada usuario ofrece, *en promedio*, un tráfico de $A_u = \lambda \cdot t_m$
Si existen $U$ usuarios, el tráfico total ofrecidom, *en promedio*, es $A = U \cdot A_u = U (\lambda \cdot t_m)$
Si existen N canales, donde se distribuye el tráfico de manera uniforme, el tráfico ofrecido en cada canal sería, *en promedio*, de $\frac{A}{N} = \frac{U \cdot A_u}{N} = \frac{U (\lambda \cdot t_m)}{N}$

**Tráfico cursado**
El tráfico cursado es el tráfico atendido por los canales disponibles en el sistema.

**Tráfico bloqueado**
El tráfico bloqueado es el tráfico que no puede ser atendido, debido a que la capacidad del canal es finita.

*En general*:
															$A_{of} = A_{cur} + A_{bloq}$
													<=>	$A_{of} = A_{cur} + (A_{of} \cdot B)$
													<=>	$A_{cur} = A_{of}(1 - B)$

## Llamadas bloqueadas perdidas Erlang-B

Mediante la distribución de Erlang-B, es posible determinar el número de canales necesarios para cumplir con cierto GOS, daod un tráfico ofrecido y número de circuitos N:

$Pr[bloqueo] = B = GOS =  E_1(N,A) = \frac{A^N}{N! \sum^{N}_{k=0} \frac{A^k}{k! }}$
## Llamadas bloquedas retornadas

Si $A_0=\lambda t_m$ es el tráfico ofrecido originalmente, entonces se tendrá una probabilidad de bloqueo inicial $B_0=f(A_0,N)$
=> $A_1=A_0(1+B_0)$ y $B_1=f(A_1, N)$
=> $A_2 = A_1(1 +B_1)$ y $B_2 = f(A_2,N)$
...
Hasta cuando no varíen los primeros dos decimales.