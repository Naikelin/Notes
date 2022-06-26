Numero de episodios

LR -> Tasa de aprendizaje. Mientras menor sea ese valor, más lento. Hay que subirselo

Batch size -> Toma muestras de a 4. Bajarselo para más rapidez

Dropout -> Es como normalización en los resultados de las capas convolucionales. Añade 0 randoms con dist bernoulli. Esta copiando en vez de aprenderlo

gamma -> optimizador -> Self.optimazer ADAM

Cambiar self.optimizer  -> SGD

# Capas
Q Solver -> Más convoluciones y Fully connected, relu


# Combinaciones
## Forma 1: Mejora en el tiempo de ejecución
En primer lugar, se debe saber que la ejecución del código es bastante larga, con las configuraciones que se tiene al momento de obtener el mismo. Es por ello que se deben realizar algunos ajustes que permitan bajar el tiempo de ejecución del código.

### Número de episodios
El número de episodios viene con un valor de 10000. En este caso se puede observar que el número de episodios corresponde a una simulación en donde la máquina de entrenamiento lleva a lugar. La resolución de un episodio tiene como resultado un puntaje obtenido que es el que se busca maximizar. Sin embargo, la cantidad de episodios es tan grande, que demora mucho bajo un escenario de prueba y error. Es por lo anterior, que el número de episodios se ha bajado a 500, para empezar a realizar pruebas de manera correcta.

### Tasa de aprendizaje
La tasa de aprendizaje, en pro de realizar pruebas de manera rápida, puede ser modificada. Si bien recordamos, la tasa de aprendizaje corresponde a una constante que le indica el tamaño de los pasos que se deben realizar en una interación. En el caso, la tasa de aprendizaje o LR (learning rate), está con un valor por defecto de 0.00025. Lo anterior implica que los saltos que hará en la optimización serán muy pequeños, sin embargo, esto también lo ralentiza. De esta manera, se puede realizar una modificación para mejorar el tiempo, a un valor de 0,005.

### Tamaño del lote y memoria máxima
El tamaño del lote (batch size), es un valor que indica el tamaño del muestreo de la memoria a utilizar. Por otro lado, la memoría máxima indica la cantidad de memoria que se puede utilizar en la plataforma que se ejecute el código. En el caso, dado que se utiliza google colab, los recursos entregados (aunque no sean pocos), no son suficientes para ejecutar el código tal como viene por defecto. En el caso se ha disminuido la memoria máxima a 10GB y se ha disminuido el tamaño del lote de la experiencia, para tener un tiempo de ejecución razonable, a 16.




