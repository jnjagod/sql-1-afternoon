CREATE TABLE person (person_id SERIAL, name VARCHAR, age INTEGER, height INTEGER, city VARCHAR, favorite_color VARCHAR);

INSERT INTO person ( name, age, height, city, favorite_color ) VALUES ('Bob Dole', 77, 195, 'D.C.', 'blue');

INSERT INTO person ( name, age, height, city, favorite_color ) VALUES ('George Washington', 287, 180, 'Colonial Beach', 'red');

INSERT INTO person ( name, age, height, city, favorite_color ) VALUES ('Jimmy Thao', 30, 100, 'Oroville', 'white');

INSERT INTO person ( name, age, height, city, favorite_color ) VALUES ('Sue Collins', 88, 120, 'Seattle', 'pink');

INSERT INTO person ( name, age, height, city, favorite_color ) VALUES ('Connie Jutkins', 42, 130, 'Chico', 'purple');

SELECT * FROM person ORDER BY height DESC;

SELECT * FROM person ORDER BY height ASC;

SELECT * FROM person ORDER BY age DESC;

SELECT * FROM person WHERE age > 20;

SELECT * FROM person WHERE age = 18;

SELECT * FROM person WHERE age < 20 OR age > 30;

SELECT * FROM person WHERE age != 27;

SELECT * FROM person WHERE favorite_color != 'red';

SELECT * FROM person WHERE favorite_color != 'red' AND favorite_color != 'blue';

SELECT * FROM person WHERE favorite_color = 'orange' OR favorite_color = 'green';

SELECT * FROM person WHERE favorite_color IN ('orange', 'green', 'blue');

SELECT * FROM person WHERE favorite_color IN ('yellow', 'purple');




CREATE TABLE orders (person_id SERIAL, product_name VARCHAR, product_price NUMERIC, quantity INTEGER);

INSERT INTO orders (person_id, product_name, product_price, quantity) VALUES (1, 'Chia Pet', 100, 4), (2, 'Garden Gnome', 24.99, 10), (3, 'Dynamite', 10.99, 50), (4, 'Candle', 15, 100), (5, 'Jersey', 51.99, 2);

SELECT * FROM orders

SELECT sum(quantity) FROM orders;

SELECT sum(product_price * quantity) FROM orders;

SELECT sum(product_price * quantity) FROM orders WHERE person_id =4;




INSERT INTO artist (name) VALUES ('System of A Down'), ('Billie Eilish'), ('Disturbed');

SELECT * FROM artist ORDER BY name DESC LIMIT 10;

SELECT * FROM artist ORDER BY name ASC LIMIT 5;

SELECT * FROM artist WHERE name LIKE 'Black%';

SELECT * FROM artist WHERE name LIKE '%Black%';




SELECT first_name last_name FROM employee WHERE city = 'Calgary';

SELECT MAX(birth_date) FROM employee;

SELECT MIN(birth_date) FROM employee;

SELECT * FROM employee WHERE reports_to = 2;

SELECT COUNT(*) FROM employee WHERE city = 'Lethbridge';




SELECT count(*) FROM invoice WHERE billing_country = 'USA';

SELECT MAX(total) FROM invoice;

SELECT MIN(total) FROM invoice;

SELECT * FROM invoice WHERE total > 5;

SELECT * FROM invoice WHERE total < 5;

SELECT COUNT(*) FROM invoice WHERE billing_state IN ('CA', 'TX', 'AZ');

SELECT AVG(total) FROM invoice;

SELECT SUM(total) FROM invoice;