# 08 MySQL

## Ejercicio 8.1

**1. By executing SELECT User, Host FROM mysql.user; find out the number of entries in the user table in the mysql database.**

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_8.1.1.png?raw=true)

**2. What are the commands to create and delete a table, and to select data from a table? What about inserting data into a table? Hint: use the MySQL manual (http://dev.mysql.com/doc/refman/5.1/en/tutorial.html)**

Para crear una tabla hace falta el comando CREATE TABLE nombre_tabla y para borrar DROP nombre_tabla.

**3. Create a database called nselab. Within this database, create a table called users, with three fields: studentid, firstname and lastname. Make studentid the primary key field. This field cannot be empty for any record and should automatically increase by one each time a new record is added (the first record should have a studentid of 1, the second 2 etc.) The other two fields should be limited to a maximum of 25 characters each. Add two students to this table: Joe Bloggs and Ashley Smith. Devise a plan to test the validation rules (this will involve adding more records) and carry it out.**

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_8.1.3.png?raw=true)

## Ejercicio 8.2

**1. Create a MySQL user called adminsec and grant it full privileges to the nselab database only (and no privileges, including viewing, to any other database). You will need to look up the syntax (don’t try to do this by editing the mysql database directly).**

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_8.2.1.png?raw=true)