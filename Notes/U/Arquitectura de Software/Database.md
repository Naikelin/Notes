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


