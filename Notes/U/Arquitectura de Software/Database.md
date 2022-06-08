# Creación BDD
```SQL
CREATE TABLE users ( id SERIAL PRIMARY KEY, email VARCHAR NOT NULL, password VARCHAR NOT NULL, name TEXT NOT NULL, surname TEXT NOT NULL, admin BOOLEAN NOT NULL DEFAULT 'f' );

CREATE TABLE pcb ( id SERIAL PRIMARY KEY, layout TEXT NOT NULL, swch_num INTEGER NOT NULL, swch_type TEXT NOT NULL, color TEXT NOT NULL, usb_type TEXT NOT NULL, hotswap BOOLEAN NOT NULL DEFAULT 'f', leds BOOLEAN NOT NULL DEFAULT 'f', quantity INTEGER NOT NULL DEFAULT 0, price INTEGER NOT NULL DEFAULT 0 );

CREATE TABLE kb_case ( id SERIAL PRIMARY KEY, model TEXT NOT NULL, material TEXT NOT NULL, color TEXT NOT NULL, quantity INTEGER NOT NULL DEFAULT 0, price INTEGER NOT NULL DEFAULT 0 );

CREATE TABLE switch ( id SERIAL PRIMARY KEY, model TEXT NOT NULL, sw_type TEXT NOT NULL, quantity INTEGER NOT NULL DEFAULT 0, price INTEGER NOT NULL DEFAULT 0 );

CREATE TABLE keycaps ( id SERIAL PRIMARY KEY, model TEXT NOT NULL, sw_type TEXT NOT NULL, color TEXT NOT NULL, quantity INTEGER NOT NULL DEFAULT 0, price INTEGER NOT NULL DEFAULT 0 );

CREATE TABLE pcb_case_compatible ( id SERIAL PRIMARY KEY, case_id INTEGER REFERENCES kb_case(id), pcb_id INTEGER NOT REFERENCES pcb(id) );

CREATE TABLE purchase_history ( id SERIAL PRIMARY KEY, user_id INTEGER REFERENCES users(id), pcb_id INTEGER REFERENCES pcb(id), case_id INTEGER REFERENCES kb_case(id), switch_id INTEGER REFERENCES switch(id), keycap_id INTEGER REFERENCES keycaps(id) );


---------------------------------------------------------------------------------
DROP 

```

# Acciones de servicios

## Login
Debe interactuar con la tabla usuarios -> Recibe un usuario y contraseña para luego comprobar si están bien o no.

## Personalización

Es el servicio más complejo en cuanto a querys. Recibe un estado:
- Estado (0): No recibe nada. Devuelve todos los PCB existentes para ser mostrados en la página.
- Estado (1): Recibe la PCB elegida. Devuelve todos los Case compatibles con la PCB. La compatibilidad se define a través de la tabla pcb_case_compatible.
- Estado (2): No recibe nada. Devuelve todos los Switches.
- Estado (3): Recibe el Switch elegido. Devuelve todos los Keycaps compatibles con los Switches. La compatibilidad se define a través del atributo type.

-- Si uno de los elementos no tiene stock, no se debe continuar la personalización con ese elemento (bloqueado) desde el front --

## Compra

Este servicio define todo el proceso de compra. Se hace búsqueda de los datos utilizados por el usuario en compras anteriores, para así devolver los últimos datos utilizados. En caso de que no haya comprado ninguna vez, se devuelve en blanco. 

Se hace un proceso de aprobación de la compra. Es decir, se genera una transacción que verifica que los elementos pedidos durante la personalización tienen un stock > 0. Este devuelve un estado OK en caso de que realice la compra. En otro caso, no se pudo procesar la transacción.

Por otro lado, si es que se genera la transacción, se debe guardar la compra en PurchaseHistory.

## agregarStock

Este servicio define uno de los procedimientos para poder agregar/actualizar Stock. Deberá tener métodos para agregar Stock de forma sincrónica:
- PCB > Agregar/editar/eliminar Stock 
- Case > Agregar/editar/eliminar Stock
- Switch > Agregar/editar/eliminar Stock 
- Keycaps > Agregar/editar/eliminar Stock 

Por otro lado, debe existir un método para agregar cada uno de los stocks de forma masiva. Básicamente deberá parsear cada una de las lineas y ejecutar las funciones definidas arriba.


# Diseño página

![[Drawing 2022-06-08 14.06.59.excalidraw|800]]
