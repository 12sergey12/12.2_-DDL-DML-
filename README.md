# Домашнее задание к занятию 12.2. «Работа с данными (DDL/DML)» Баранов Сергей


---


Задание можно выполнить как в любом IDE, так и в командной строке.


### Задание 1

1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

![monitoring](https://github.com/12sergey12/12.2_-DDL-DML-/blob/main/images/12.2-1.1.png)

1.2. Создайте учётную запись sys_temp. 

mysql> CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY 'password';
Query OK, 0 rows affected (0.01 sec)

![monitoring](https://github.com/12sergey12/12.2_-DDL-DML-/blob/main/images/12.2-1.3.png)

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

![monitoring](https://github.com/12sergey12/12.2_-DDL-DML-/blob/main/images/12.2-1.3.png)

1.4. Дайте все права для пользователя sys_temp. 

GRANT ALL PRIVILEGES ON * . * TO 'sys_temp'@'localhost';

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

![monitoring](https://github.com/12sergey12/12.2_-DDL-DML-/blob/main/images/12.2-1.5.png)

1.6. Переподключитесь к базе данных от имени sys_temp.

![monitoring](https://github.com/12sergey12/12.2_-DDL-DML-/blob/main/images/12.2-1.6.png)

Для смены типа аутентификации с sha2 используйте запрос: 

```sql
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

mysql -u root -p sakila < /home/baranovsa/Загрузки/sakila-db/sakila-schema.sql

![monitoring](https://github.com/12sergey12/12.2_-DDL-DML-/blob/main/images/12.2-1.7.png)

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

![monitoring](https://github.com/12sergey12/12.2_-DDL-DML-/blob/main/images/12.2-1.8.png)

*Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.*


---


### Задание 2


Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)
```
Название таблицы | Название первичного ключа
customer         | customer_id
```

![monitoring](https://github.com/12sergey12/12.2_-DDL-DML-/blob/main/images/%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0.png)






