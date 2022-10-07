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

ejemplo:

SELECT * FROM Customers
WHERE Country='Germany' AND (City='Berlin' OR City='München'); 
