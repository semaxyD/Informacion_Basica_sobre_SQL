# Informacion_Basica_sobre_SQL
Información para principiantes en el mundo de la Base de datos.

Crear una Base de Datos (BD)

Para crear una nueva base de datos en MySQL, puedes utilizar el comando CREATE DATABASE.
La sintaxis es la siguiente:
CREATE DATABASE nombre_de_la_bd;

Por ejemplo, para crear una base de datos llamada "mi_bd", ejecuta el siguiente comando:
CREATE DATABASE mi_bd;




Crear Tablas
Una vez que tienes una base de datos creada, puedes crear tablas dentro de ella. Para hacer esto, utiliza el comando CREATE TABLE. La sintaxis es la siguiente:
CREATE TABLE nombre_de_la_tabla (
  		columna1 tipo_de_dato1,
  		columna2 tipo_de_dato2,
  		columna3 tipo_de_dato3,
  		...
      );
      
Cada columna en una tabla tiene un nombre y un tipo de dato. Por ejemplo, para crear una tabla llamada "usuarios" con dos columnas (id y nombre), ejecuta el siguiente comando:
CREATE TABLE usuarios (
  		id INT,
  		nombre VARCHAR(50)
);




Modificar estructura de las tablas
Puedes modificar la estructura de una tabla existente utilizando el comando ALTER TABLE. La sintaxis es la siguiente:
ALTER TABLE nombre_de_la_tabla
  	 ADD columna tipo_de_dato;


ALTER TABLE nombre_de_la_tabla
  	 MODIFY columna tipo_de_dato;


ALTER TABLE nombre_de_la_tabla
  	 DROP COLUMN columna;
     
Por ejemplo, para agregar una nueva columna "email" a la tabla "usuarios", ejecuta el siguiente comando:
ALTER TABLE usuarios
  	 ADD email VARCHAR(100);
     
     

Insertar/Actualizar/Eliminar/Consultar datos

Para agregar datos a una tabla, utiliza el comando INSERT INTO. La sintaxis es la siguiente:
INSERT INTO nombre_de_la_tabla (columna1, columna2, columna3)
  	VALUES (valor1, valor2, valor3, ...);

Por ejemplo, para agregar un nuevo usuario a la tabla "usuarios", ejecuta el siguiente comando:
INSERT INTO usuarios (id, nombre, email)
  	 VALUES (1, 'Juan Perez', 'juan.perez@example.com');
     
Para actualizar datos en una tabla, utiliza el comando UPDATE. La sintaxis es la siguiente:
UPDATE nombre_de_la_tabla
  	 SET columna1 = valor1, columna2 = valor2, ...
  	 WHERE condición;
     
Por ejemplo, para actualizar el correo electrónico de un usuario en la tabla "usuarios", ejecuta el siguiente comando:
UPDATE usuarios
  	 SET email = 'nuevo.email@example.com'
  	 WHERE id = 1;
     
Para eliminar datos de una tabla, utiliza el comando DELETE FROM. La sintaxis es la siguiente:
DELETE FROM nombre_de_la_tabla
   	 WHERE condición;
     
Por ejemplo, para eliminar un usuario de la tabla "usuarios", ejecuta el siguiente comando:
	DELETE FROM usuarios
  	 WHERE id = 1;

Para consultar datos en una tabla, utiliza el comando SELECT. La sintaxis es la siguiente:
SELECT columna1, columna2,...
FROM nombre_de_la_tabla
WHERE condición;

Por ejemplo, para obtener todos los usuarios de la tabla "usuarios", ejecuta el siguiente comando:
SELECT *
 FROM usuarios;




Tipos de datos de MySQL
MySQL admite varios tipos:

 INT: Entero de tamaño fijo. Puede almacenar valores enteros entre -2147483648 y 2147483647.
 
 FLOAT: Número de punto flotante de precisión simple. Puede almacenar números     reales con una precisión de 6 a 7 dígitos.
 
 DOUBLE: Número de punto flotante de doble precisión. Puede almacenar números reales con una precisión de 15 a 16 dígitos.
 
 DECIMAL: Número decimal de precisión fija. Puede almacenar números decimales con una precisión y escala definidas por el usuario.
 
 VARCHAR: Cadena de longitud variable. Puede almacenar una cadena de caracteres de longitud variable hasta un máximo definido por el usuario.
 
 CHAR: Cadena de longitud fija. Puede almacenar una cadena de caracteres de longitud fija hasta un máximo definido por el usuario.
 
 DATE: Fecha en formato 'YYYY-MM-DD'. Puede almacenar fechas desde '1000-01-01' hasta '9999-12-31'.
 
 TIME: Hora en formato 'HH:MM:SS'. Puede almacenar tiempos desde '-838:59:59' hasta '838:59:59'.
 
 DATETIME: Fecha y hora en formato 'YYYY-MM-DD HH:MM:SS'. Puede almacenar fechas y tiempos desde '1000-01-01 00:00:00' hasta '9999-12-31 23:59:59'.
 
 TIMESTAMP: Marca de tiempo en formato 'YYYY-MM-DD HH:MM:SS'. Puede almacenar fechas y tiempos desde '1970-01-01 00:00:01' hasta '2038-01-19 03:14:07'.
 
 ENUM: Tipo de dato de enumeración. Puede almacenar uno de los valores predefinidos en una lista de opciones definida por el usuario.
 
 SET: Tipo de dato de conjunto. Puede almacenar una combinación de valores predefinidos en una lista de opciones definida por el usuario.
