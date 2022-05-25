# Pasos

Se le pide que tenga un cluster de cassandra con 3 nodos. 

![[Diagrama.png]]

Cada una de las tablas debe existir en un Keyspace distinto, donde pacientes debe tener un factor de replicación de 2 y recetas debe tener un factor de replicación de 3, ambos utilizando una Estrategia simple.

```
CREATE KEYSPACE pacientes WITH replication = {'class': 'SimpleStrategy', 'replication_factor' : 2};
   
CREATE KEYSPACE recetas WITH replication = {'class': 'SimpleStrategy', 'replication_factor' : 3};
```

Se crean las tablas de manera separada.

```
CREATE TABLE pacientes.paciente (
id int,
nombre text,
apellido text,
rut text,
email text,
fecha_nacimiento timeuuid,
PRIMARY KEY (id));

CREATE TABLE recetas.receta (
id int,
id_paciente int,
comentarios text,
farmacos text,
doctor text,
PRIMARY KEY (id));
```

```
USE pacientes;
INSERT INTO paciente (id, nombre, apellido, rut, email, fecha_nacimiento) values (1, 'Nicolás', 'Núñez', '20120225-6', 'nicolas.nunez2@mail.udp,cl', now());
INSERT INTO paciente (id, nombre, apellido, rut, email, fecha_nacimiento) values (2, 'Nicolás', 'Araya', '123', 'nicolas.araya@mail.udp,cl', now());
INSERT INTO paciente (id, nombre, apellido, rut, email, fecha_nacimiento) values (3, 'Nicolás', 'Hidalgo', '312', 'nicolas.hidalgoc@mail.udp,cl', now());

USE recetas;
INSERT INTO receta (id, id_paciente, comentarios, farmacos, doctor) values (1, 1, 'Tomar cada 8 hrs', '{[ \"Metanfetamina\" ]}', 'El Jordan23');
```

Al probar en cada nodo:

```
SELECT * FROM paciente;
```

Funciona en todos los nodos, pero tiene replicación en sólo 2 nodos. ¿Cómo es posible? :o (posible pregunta).