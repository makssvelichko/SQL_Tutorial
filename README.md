- [Введення в SQL](#введення-в-sql)
- [Синтаксис SQL](#синтаксис-sql)
- [Інструкція SQL SELECT](#інструкція-sql-select)
- [Інструкція SQL SELECT DISTINCT](#інструкція-sql-select-distinct)
- [SQL WHERE](#sql-where)
- [SQL ORDER BY](#sql-order-by)
- [Оператор SQL AND](#оператор-sql-and)
- [Оператор OR](#оператор-sql-or)
- [Оператор NOT](#оператор-sql-not)
- [Інструкція SQL INSERT INTO](#інструкція-sql-insert-into)
- 
 

<a name="Введення_в_SQL"></a>
# Введення в SQL
## Що таке SQL?
+ SQL означає мову структурованих запитів
+ SQL дозволяє отримувати доступ до баз даних і керувати ними
+ SQL став стандартом Американського національного інституту стандартів (ANSI) у 1986 році та Міжнародної організації зі стандартизації (ISO) у 1987 році.

## Що може SQL?
+ SQL може виконувати запити до бази даних
+ SQL може отримувати дані з бази даних
+ SQL може вставляти записи в базу даних
+ SQL може оновлювати записи в базі даних
+ SQL може видаляти записи з бази даних
+ SQL може створювати нові бази даних
+ SQL може створювати нові таблиці в базі даних
+ SQL може створювати збережені процедури в базі даних
+ SQL може створювати представлення в базі даних
+ SQL може встановлювати дозволи для таблиць, процедур і представлень
___
<a name="Синтаксис_SQL"></a>
# Синтаксис SQL
### Інструкції SQL
Більшість дій, які вам потрібно виконати з базою даних, виконуються за допомогою операторів SQL.

Інструкції SQL складаються з ключових слів, які легко зрозуміти.

Наступний оператор SQL повертає всі записи з таблиці під назвою «Клієнти»:
### приклад
```SQL 
SELECT * FROM Customers;
```
## Таблиці бази даних
База даних найчастіше містить одну або декілька таблиць. Кожна таблиця ідентифікується назвою (наприклад, «Клієнти» або «Замовлення») і містить записи (рядки) з даними.

Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |


Таблиця вище містить п’ять записів (по одному для кожного клієнта) і сім стовпців (CustomerID, CustomerName, ContactName, Address, City, PostalCode та Country).

## Майте на увазі, що...
+ Ключові слова SQL НЕ чутливі до регістру: `select` те саме, що `SELECT`

## Крапка з комою після операторів SQL?
Деякі системи баз даних вимагають крапки з комою в кінці кожного оператора SQL.

Крапка з комою — це стандартний спосіб відокремлення кожного оператора SQL у системах баз даних, які дозволяють виконувати кілька операторів SQL під час одного виклику до сервера.

## Деякі з найважливіших команд SQL
+ `SELECT` - витягує дані з бази даних
+ `UPDATE` - оновлює дані в базі даних
+ `DELETE` - видаляє дані з бази даних
+ `INSERT INTO` - вносить нові дані в базу даних
+ `CREATE DATABASE` - створює нову базу даних
+ `ALTER DATABASE` - змінює базу даних
+ `CREATE TABLE` - створює нову таблицю
+ `ALTER TABLE` - змінює таблицю
+ `DROP TABLE` - видаляє таблицю
+ `CREATE INDEX` - створює індекс (ключ пошуку)
+ `DROP INDEX` - видаляє індекс

___
# Інструкція SQL SELECT
 Інструкція `SELECT` використовується для вибору даних із бази даних.

### приклад
Повернути дані з таблиці Клієнти:
```SQL
SELECT CustomerName, City FROM Customers;
```

## Синтаксис
```SQL
SELECT column1, column2, ...
FROM table_name;
```
Тут стовпець1, стовпець2, ... — це назви полів таблиці, з якої потрібно вибрати дані.
Table_name представляє назву таблиці, з якої потрібно вибрати дані.

## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |


## Виберіть УСІ стовпці
 Якщо ви хочете повернути всі стовпці, не вказуючи ім’я кожного стовпця, ви можете використати синтаксис `SELECT *`:
 ### приклад

```sql
SELECT * FROM Customers;
```

___
# Інструкція SQL SELECT DISTINCT
Оператор `SELECT DISTINCT` використовується для повернення лише різних (різних) значень.

### приклад

Виберіть усі різні країни з таблиці «Клієнти»:

```sql
SELECT DISTINCT Country FROM Customers;
```

Усередині таблиці стовпець часто містить багато повторюваних значень; іноді вам потрібно лише перелічити різні (різні) значення.

## Синтаксис
```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## SELECT Приклад без DISTINCT
Якщо пропустити `DISTINCT` ключове слово, оператор SQL повертає значення "Країна" з усіх записів таблиці "Клієнти":
### приклад
```sql
SELECT Country FROM Customers;
```

## Розрахунок відмінних
Використовуючи `DISTINCT` ключове слово у функції під назвою `COUNT`, ми можемо повернути кількість різних країн.
### приклад
```sql
SELECT COUNT(DISTINCT Country) FROM Customers;
```
___
# SQL WHERE
## Речення SQL WHERE
Речення `WHERE` використовується для фільтрації записів.

Він використовується для вилучення лише тих записів, які відповідають певній умові.

### приклад

Виберіть усіх клієнтів з Мексики:

```sql
SELECT * FROM Customers
WHERE Country='Mexico';
```

## Синтаксис
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## Текстові поля проти числових полів

SQL вимагає одинарних лапок навколо текстових значень (більшість систем баз даних також допускають подвійні лапки).

Однак числові поля не слід брати в лапки:

### приклад
```sql
SELECT * FROM Customers
WHERE CustomerID=1;
```

## Оператори в реченні WHERE
Для фільтрації пошуку можна використовувати інші оператори, крім оператора `=`.

### приклад
Виберіть усіх клієнтів із CustomerID більше 80:
```sql
SELECT * FROM Customers
WHERE CustomerID > 80;
```

Можна використовувати такі оператори WHERE:
| Оператор | Опис |
| --- | --- |
| = | Рівний |
| > | Більше ніж |
| < | Менше ніж |
| >= | Більше ніж або рівний |
| <= | Менше ніж або рівний |
| <> | Не рівний. Примітка: У деяких версіях SQL цей оператор може бути записаний як != |
| BETWEEN | Між певним діапазоном |
| LIKE | Пошук за шаблоном |
| IN | Вказати кілька можливих значень для стовпця |

___
# SQL ORDER BY

Ключове `ORDER BY` слово використовується для сортування набору результатів у порядку зростання або спадання.

### приклад


Сортувати товари за ціною:
```sql
SELECT * FROM Products
ORDER BY Price;
```
## Синтаксис
```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Продукти» , яка використовується в прикладах:

| ProductID | ProductName | SupplierID | CategoryID | Unit | Price |
| --- | --- | --- | --- | --- | --- |
| 1 | Chais | 1 | 1 | 10 boxes x 20 bags | 18 |
| 2 | Chang | 1 | 1 | 24 - 12 oz bottles | 19 |
| 3 | Aniseed Syrup | 1 | 2 | 12 - 550 ml bottles | 10 |
| 4 | Chef Anton's Cajun Seasoning | 2 | 2 | 48 - 6 oz jars | 22 |
| 5 | Chef Anton's Gumbo Mix | 2 | 2 | 36 boxes | 21.35 |

## Ключове слово DESC
За умовчанням ключове 'ORDER BY' слово сортує записи в порядку зростання. Щоб відсортувати записи в порядку спадання, використовуйте 'DESC' ключове слово.

### приклад
Розсортуйте продукти від найвищої до найнижчої ціни:
```sql
SELECT * FROM Products
ORDER BY Price DESC;
```
## Порядок в алфавітному порядку

Для рядкових значень `ORDER BY` ключове слово буде впорядковано в алфавітному порядку:

### приклад
Відсортуйте продукти в алфавітному порядку за назвою продукту:
```sql
SELECT * FROM Products
ORDER BY ProductName;
```

## За алфавітом DESC

Щоб відсортувати таблицю в зворотному алфавітному порядку, використовуйте `DESC` ключове слово:

### приклад
Відсортуйте продукти за назвою продукту у зворотному порядку:
```sql
SELECT * FROM Products
ORDER BY ProductName DESC;
```

## ПОРЯДОК за кількома колонками
Наступний оператор SQL вибирає всіх клієнтів із таблиці «Клієнти», відсортованих за стовпцями «Країна» та «Назва клієнта». Це означає, що він упорядковує їх за країною, але якщо деякі рядки мають однакову країну, вони впорядковуються за назвою клієнта:

### приклад
```sql
SELECT * FROM Customers
ORDER BY Country, CustomerName;
```

## Використання як ASC, так і DESC
Наступний оператор SQL вибирає всіх клієнтів із таблиці «Клієнти», відсортованих за зростанням за стовпцем «Країна» та за спаданням за стовпцем «Назва клієнта»:

### приклад
```sql
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;
```
___
<a name="Оператор_SQL_AND"></a>
# Оператор SQL AND

`WHERE` може містити один або кілька `AND` операторів.

Оператор `AND` використовується для фільтрації записів на основі кількох умов, наприклад, якщо ви хочете повернути всіх клієнтів з Іспанії, які починаються з літери «G»:

### приклад
Виберіть усіх клієнтів з Іспанії, які починаються з літери "G":
```sql
SELECT *
FROM Customers
WHERE Country = 'Spain' AND CustomerName LIKE 'G%';
```

Синтаксис
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
```

## І проти АБО
Оператор `AND` виводить запис, якщо всі умови ІСТИННІ.

Оператор `OR` виводить запис, якщо будь-яка з умов є TRUE.

## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## Усі умови мають відповідати дійсності
У наведеному нижче операторі SQL вибираються всі поля, серед `Customers` яких `Country` «Німеччина» ТА `City` «Берлін» ТА `PostalCode` більше 12000:
### приклад
```sql
SELECT * FROM Customers
WHERE Country = 'Germany'
AND City = 'Berlin'
AND PostalCode > 12000;
```

## Поєднання І та АБО
Ви можете комбінувати оператори ANDі OR.

Наступний оператор SQL вибирає всіх клієнтів з Іспанії, які починаються з «G» або «R».

Переконайтеся, що ви використовуєте дужки, щоб отримати правильний результат.

### приклад
Виберіть усіх іспанських клієнтів, які починаються на "G" або "R":
```sql
SELECT * FROM Customers
WHERE Country = 'Spain' AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');
```

Без дужок оператор `select` поверне всіх клієнтів з Іспанії, які починаються з «G», а також усіх клієнтів, які починаються з «R», незалежно від значення країни:

### приклад
Виберіть усіх клієнтів, які:
з Іспанії та починаються з літери "G" або
літери "R":
```sql
SELECT * FROM Customers
WHERE Country = 'Spain' AND CustomerName LIKE 'G%' OR CustomerName LIKE 'R%';
```
___
<a name="Оператор_SQL_OR"></a>
# Оператор SQL OR
`WHERE` може містити один або декілька `OR` операторів.

Оператор `OR` використовується для фільтрації записів на основі більш ніж однієї умови, наприклад, якщо ви хочете повернути всіх клієнтів з Німеччини, а також клієнтів з Іспанії:

приклад
Виберіть усіх клієнтів з Німеччини чи Іспанії:
```sql
SELECT *
FROM Customers
WHERE Country = 'Germany' OR Country = 'Spain';
```

## Синтаксис
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |


## Принаймні одна умова має виконуватися
Наступна інструкція SQL вибирає всі поля від клієнтів, де або `City` "Берлін", `Customer` Nameпочинається з літери "G" або `Country` "Норвегія": 

### приклад
```sql
SELECT * FROM Customers
WHERE City = 'Berlin' OR CustomerName LIKE 'G%' OR Country = 'Norway';
```
___
<a name="Оператор_SQL_NOT"></a>
# Оператор SQL NOT
Оператор `NOT` використовується в поєднанні з іншими операторами для отримання протилежного результату, який також називають негативним результатом.

У операторі select нижче ми хочемо повернути всіх клієнтів, які НЕ з Іспанії:

### приклад
Виберіть лише клієнтів, які НЕ з Іспанії:
```sql
SELECT * FROM Customers
WHERE NOT Country = 'Spain';
```

У прикладі вище `NOT` оператор використовується в комбінації з `=` оператором, але його можна використовувати в комбінації з іншими операторами порівняння та/або логічними операторами. Дивіться приклади нижче.

## Синтаксис
```sql
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## NOT LIKE
### приклад
Виберіть клієнтів, які не починаються з літери «А»:
```sql
SELECT * FROM Customers
WHERE CustomerName NOT LIKE 'A%';
```

## NOT BETWEEN
### приклад
Виберіть клієнтів із ідентифікатором клієнта не між 10 і 60:
```sql
SELECT * FROM Customers
WHERE CustomerID NOT BETWEEN 10 AND 60;
```

## NOT IN
### приклад
Виберіть клієнтів, які не з Парижа чи Лондона:
```sql
SELECT * FROM Customers
WHERE City NOT IN ('Paris', 'London');
```

## НЕ більше ніж
### приклад
Виберіть клієнтів з CustomerId не більше 50:
```sql
SELECT * FROM Customers
WHERE NOT CustomerID > 50;
```
**Примітка**: існує оператор не більше: `!>` це дасть той самий результат.

## НЕ менше
### приклад
Виберіть клієнтів з CustomerID не менше 50:
```sql
SELECT * FROM Customers
WHERE NOT CustomerId < 50;
```
**Примітка**: існує оператор not-меньше-тоді: `!<` це дасть вам той самий результат.

___
<a name="Інструкція_SQL_INSERT_INTO"></a>
# Інструкція SQL INSERT INTO
Інструкція `INSERT INTO` використовується для вставки нових записів у таблицю.

## INSERT INTO Синтаксис
Написати заяву можна `INSERT INTO` двома способами:

1. Вкажіть назви стовпців і значення, які потрібно вставити:
```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```
2. Якщо ви додаєте значення для всіх стовпців таблиці, вам не потрібно вказувати назви стовпців у SQL-запиті. Однак переконайтеся, що порядок значень відповідає порядку стовпців у таблиці.
Тут `INSERT INTO` синтаксис буде таким:
```sql
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 89 | White Clover Markets | Karl Jablonski | 305 - 14th Ave. S. Suite 3B | Seattle | 98128 | USA |
| 90 | Wilman Kala | Matti Karttunen | Keskuskatu 45 | Helsinki | 21240 | Finland |
| 91 | Wolski | Zbyszek | ul. Filtrowa 68 | Walla | 01-012 | Poland |

## INSERT INTO Приклад
Наступний оператор SQL вставляє новий запис у таблицю "Клієнти":
### приклад
```sql
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');
```

Вибір із таблиці «Клієнти» тепер виглядатиме так:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 89 | White Clover Markets | Karl Jablonski | 305 - 14th Ave. S. Suite 3B | Seattle | 98128 | USA |
| 90 | Wilman Kala | Matti Karttunen | Keskuskatu 45 | Helsinki | 21240 | Finland |
| 91 | Wolski | Zbyszek | ul. Filtrowa 68 | Walla | 01-012 | Poland |
| 92 | Cardinal | Tom B. Erichsen | Skagen 21 | Stavanger | 4006 | Norway |

## Вставити дані лише у вказані стовпці
Також можна вставляти дані лише в певні стовпці.

Наступний оператор SQL вставить новий запис, але вставить дані лише в стовпці «CustomerName», «City» і «Country» (CustomerID буде оновлено автоматично):

### приклад
```sql
INSERT INTO Customers (CustomerName, City, Country)
VALUES ('Cardinal', 'Stavanger', 'Norway');
```
Вибір із таблиці «Клієнти» тепер виглядатиме так:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 89 | White Clover Markets | Karl Jablonski | 305 - 14th Ave. S. Suite 3B | Seattle | 98128 | USA |
| 90 | Wilman Kala | Matti Karttunen | Keskuskatu 45 | Helsinki | 21240 | Finland |
| 91 | Wolski | Zbyszek | ul. Filtrowa 68 | Walla | 01-012 | Poland |
| 92 | Cardinal | null | null | Stavanger | null | Norway |

## Вставити кілька рядків
Також можна вставити кілька рядків в один оператор.

Щоб вставити кілька рядків даних, ми використовуємо той самий `INSERT INTO` оператор, але з кількома значеннями:

### приклад
```sql
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES
('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway'),
('Greasy Burger', 'Per Olsen', 'Gateveien 15', 'Sandnes', '4306', 'Norway'),
('Tasty Tee', 'Finn Egan', 'Streetroad 19B', 'Liverpool', 'L1 0AA', 'UK');
```
Обов’язково розділяйте кожен набір значень комою `,`.

Вибір із таблиці «Клієнти» тепер виглядатиме так:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 89 | White Clover Markets | Karl Jablonski | 305 - 14th Ave. S. Suite 3B | Seattle | 98128 | USA |
| 90 | Wilman Kala | Matti Karttunen | Keskuskatu 45 | Helsinki | 21240 | Finland |
| 91 | Wolski | Zbyszek | ul. Filtrowa 68 | Walla | 01-012 | Poland |
| 92 | Cardinal | Tom B. Erichsen | Skagen 21 | Stavanger | 4006 | Norway |
| 93 | Greasy Burger | Per Olsen | Gateveien 15 | Sandnes | 4306 | Norway |
| 94 | Tasty Tee | Finn Egan | Streetroad 19B | Liverpool | L1 0AA | UK |

