Numero de episodios

LR -> Tasa de aprendizaje. Mientras menor sea ese valor, más lento. Hay que subirselo

Bash size -> Toma muestras de a 4. Bajarselo para más rapidez

Dropout -> Es como normalización en los resultados de las capas convolucionales. Añade 0 randoms con dist bernoulli. Esta copiando en vez de aprenderlo

gamma -> optimizador -> Self.optimazer ADAM

Cambiar self.optimizer  -> SGD

# Capas
Q Solver -> Más convoluciones y Fully connected, relu
