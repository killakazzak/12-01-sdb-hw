# Домашнее задание к занятию "`Базы данных`" - `Тен Денис`

### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).

### Решение Задание 1

Таблицы:

№1

Сотрудники (
+ идентификатор, первичный ключ, serial
+ фамилия varchar(50)
+ имя varchar(50)
+ отчество varchar(50)  
+ оклад numeric(18,2) 
+ идентификатор, тип подразделения, integer
+ идентификатор, структурное подразделение, integer
+ дата найма, date
+ идентификатор,  адрес сотрудника, integer
+ идентификатор, проект, integer)

№2

Типы Подразделений (
+ идентификатор, первичный ключ, serial
+ наименование varchar(50))

№3

Структурные подразделения (
+ идентификатор, первичный ключ, serial
+ наименование varchar(50))

№4

Должности (
+ идентификатор, первичный ключ, serial
+ аименование varchar(100))

№5

Регионы (
+ идентификатор, первичный ключ, serial
+ наименование varchar(50))

№6

Города (
+ идентификатор, первичный ключ, serial
+ наименование varchar(50))

№7

Улицы (
+идентификатор, первичный ключ, serial
+наименование varchar(50))

№8

Адреса сотрудников (
+ идентификатор, первичный ключ, serial
+ идентификатор, регион, integer
+ идентификатор, город, integer
+ идентификатор, улица, integer
+ номер дома, varchar(10))

№9

Проекты (
+идентификатор, первичный ключ, serial
+наименование varchar(150))








  


## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.


### Задание 2*

Перечислите, какие, на ваш взгляд, в этой денормализованной таблице встречаются функциональные зависимости и какие правила вывода нужно применить, чтобы нормализовать данные.

### Решение Задание 2*
