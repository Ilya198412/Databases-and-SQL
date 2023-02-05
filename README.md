# Databases-and-SQL

## Создание таблицы

CREATE TABLE mobilephones_list
(
    product_name character varying(30),
    manufacturer character varying(30),
    product_count int,
    price character varying(30)
);




## Заполнение таблицы данными

INSERT INTO mobilephones_list
	(product_name, manufacturer, product_count, price )
VALUES

	('Apple iPhone 14 Pro 128Gb', 'Apple', 10, '123 990'),
    ('Huawei nova Y61 4/64Gb', 'Huawei', 11, '10 270'),
    ('REALME C25s 4/64Gb', 'REALME', 2, '9 990'),
    ('Xiaomi Redmi 9A 2/32Gb', 'Xiaomi', 5, '5 990'),
    ('Apple iPhone 13 128Gb, A2631', 'Apple', 4, '64 140'),
    ('Samsung Galaxy A53 5G 8/256Gb', 'Samsung', 22, '29 530'),
    ('Samsung Galaxy A13 4/64Gb', 'Samsung', 1, '10 990'),
    ('Xiaomi Poco C40 4/64Gb', 'Xiaomi', 20, '8 990'),
    ('INFINIX Note 12 Pro 8/256Gb', 'INFINIX', 10, '21 990');


## Запросы по поиску 

4.* С помощью SELECT-запроса с оператором LIKE / REGEXP найти:
4.1.* Товары, в которых есть упоминание "Iphone"
4.2.* Товары, в которых есть упоминание "Samsung"
4.3.* Товары, в названии которых есть ЦИФРЫ
4.4.* Товары, в названии которых есть ЦИФРА "8"

select *
from mobilephones_list
where product_name like "%iPhone%"


select *
from mobilephones_list
where product_name like "%sams%"

select *
from mobilephones_list
where product_name like "%8%"


select *
from mobilephones_list
where product_name regexp '[0-9]'


select *
from mobilephones_list
where product_name regexp '[8-9]'

select *
from mobilephones_list
where product_name regexp 'iPhone'


select *
from mobilephones_list
where product_name regexp 'samsung'
