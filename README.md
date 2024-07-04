# Домашнее задание к занятию "`Работа с данными (DDL/DML)`" - `Фёдоров Илья`#Задание 1

### Задание 1

![alt text](https://github.com/Limzor/ddl-dml/blob/main/Screenshot_1.png)

![alt text](https://github.com/Limzor/ddl-dml/blob/main/Screenshot_2.png)

![alt text](https://github.com/Limzor/ddl-dml/blob/main/Screenshot_3.png)

![alt text](https://github.com/Limzor/ddl-dml/blob/main/Screenshot_4.png)

### Задание 2

![alt text](https://github.com/Limzor/ddl-dml/blob/main/Screenshot_5.png)

![alt text](https://github.com/Limzor/ddl-dml/blob/main/Screenshot_6.png)

### команды
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=root -d mysql:8.0
docker exec -it mysql-container mysql -uroot -proot
CREATE USER 'sys_temp'@'%' IDENTIFIED BY 'password'
SELECT user, host FROM mysql.user
GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'%'
FLUSH PRIVILEGES
SHOW GRANTS FOR 'sys_temp'@'%'
ALTER USER 'sys_temp'@'%' IDENTIFIED WITH mysql_native_password BY 'password'
docker exec -it mysql-container mysql -usys_temp -ppassword
docker cp /path/to/sakila-db/sakila-schema.sql mysql-container:/sakila-schema.sql
docker cp /path/to/sakila-db/sakila-data.sql mysql-container:/sakila-data.sql
docker exec -it mysql-container mysql -usys_temp -ppassword -e "source /sakila-schema.sql"
docker exec -it mysql-container mysql -usys_temp -ppassword -e "source /sakila-data.sql"
use sakila
SHOW TABLES IN sakila
SHOW KEYS FROM actor WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM actor_info WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM address WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM category WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM city WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM country WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM customer WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM customer_list WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM film WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM film_actor WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM film_category WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM film_list WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM film_text WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM inventory WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM language WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM nicer_but_slower_film_list WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM payment WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM rental WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM sales_by_film_category WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM sales_by_store WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM staff WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM staff_list WHERE Key_name = 'PRIMARY'
SHOW KEYS FROM store WHERE Key_name = 'PRIMARY'
