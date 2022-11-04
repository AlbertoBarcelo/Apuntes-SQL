# SQL basic SELECTS

SQL introduction for the unit 1.

## Crear tabla

create table series[
  * enviados VARCHAR (20)not null,
  *  DNI VARCHAR (20)not null Primari Key
 ]

## Comando **SELECT**

SELECT * FROM Customers;

## Comando SELECT DISTINCT

**Sirve para mostrar solo los elementos diferentes**

SELECT DISTINCT Country FROM Customers;

## The SQL COUNT()

**Sirve para contar**

SELECT COUNT(column_name)
FROM table_name

## Comando WHERE

**Se usa para filtrar informacion**

SELECT * FROM Customers
WHERE Country='Mexico'; 
operadores
| operator | description |
|--|--|
|=| 	Equal| 	
|> |	Greater than|
|< |	Less than|
|>= |	Greater than or equal|	
|<= |	Less than or equal|
|<> |	Not equal. Note: In some versions of SQL this operator may be written as !=|
|BETWEEN |	Between a certain range|
|LIKE |	Search for a pattern|
|IN |To specify multiple possible values for a column|

## Operadores AND, OR and NOT 


SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...; 

*Ejemplos*
1. SELECT * FROM Customers
WHERE Country='Germany' AND City='Berlin';

2. SELECT * FROM Customers
WHERE City='Berlin' OR City='München';

3. SELECT * FROM Customers
WHERE NOT Country='Uk' and not City='Berlin';

Con los parentesis 

*Ejemplo*

SELECT * FROM Customers
WHERE Country='Germany' AND (City='Berlin' OR City='München'); 

## SQL ORDER BY

Se utiliza para elegir el orden en que vamos a mostrar los resultados de forma ASC|DESC
Por defecto las Bases de datos estan ordenadas de manera aleatoria

*Ejemplo*

SELECT * FROM Customers
ORDER BY PostalCode ASC;

## INSERT INTO
Se usa para añadir datos a nuestra base de datos

*Ejemplos*

INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');

## NULL Values
Sirve para identificar un campo desconocido o para hacer la referencia a la nada

*Tipos*

IS NULL and IS NOT NULL

*Ejemplos*

SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NULL;

## DELETE
Se utiliza para eliminar rejistros de la base de datos

*Ejemplos*

 DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste'; 


 ## MIN / MAX
 Min se utiliza para encontrar el minimo de algo y el max se utiliza para encontrar el mayor de algo
 *Ejemplos*
 SELECT MIN(Price) FROM Products;
 
 Si hay varios productos con el mismo minimo/maximo se muestra solo un producto
 
 ## ALERTA
 Las funcionees (max, min, avg, sum, count) no se pueden acompañar de otra columna
Lo que se ha de hacer es lo siguiente: SELECT Productname From Products where Price=(select min(Price) from Products);
