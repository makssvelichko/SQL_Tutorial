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
- [Значення SQL NULL](#значення-sql-null)
- [Інструкція SQL UPDATE](#інструкція-sql-update)
- [Інструкція SQL DELETE](#інструкція-sql-delete)
- [SQL SELECT TOP](#sql-select-top)
- [Агрегатні функції SQL](#агрегатні-функції-sql)
- [Функції SQL MIN() і MAX()](#функції-sql-min-і-max)
- [Функція SQL COUNT()](#функція-sql-count)
- [Функція SQL SUM()](#функція-sql-sum)
- [Функція SQL AVG()](#функція-sql-avg)
- [Оператор SQL LIKE](#оператор-sql-like)
- [Символи підстановки SQL](#символи-підстановки-sql)
- [Оператор SQL IN](#оператор-sql-in)
- [Оператор SQL BETWEEN](#оператор-sql-between)
- [Псевдоніми SQL](#псевдоніми-sql)
- [SQL об'єднання](#sql-обєднання)
- [SQL INNER JOIN](#sql-inner-join)
- [SQL LEFT JOIN](#sql-left-join)
- [SQL RIGHT JOIN](#sql-right-join)
- [SQL FULL OUTER JOIN](#sql-full-outer-join)
- [SQL Self Join](#sql-self-join)
- [SQL UNION](#sql-union)
- [Інструкція SQL GROUP BY](#інструкція-sql-group-by)
- [SQL HAVING](#sql-having)
- [SQL EXISTS](#sql-exists)
- [SQL ANY та ALL](#sql-any-та-all)
- [SQL SELECT INTO](#sql-select-into)
- [SQL INSERT INTO SELECT](#sql-insert-into-select)
- [SQL CASE](#sql-case)
- [SQL NULL](#sql-null)
- [Збережені процедури SQL](#збережені-процедури-sql)
- [Коментарі SQL](#коментарі-sql)
- [Оператори SQL](#оператори-sql)

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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all">Спробуйте самі</a>
</div>

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

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_columns">Спробуйте самі</a>
</div>

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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all">Спробуйте самі</a>
</div>

___
# Інструкція SQL SELECT DISTINCT
Оператор `SELECT DISTINCT` використовується для повернення лише різних (різних) значень.

### приклад

Виберіть усі різні країни з таблиці «Клієнти»:

```sql
SELECT DISTINCT Country FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_distinct">Спробуйте самі</a>
</div>



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

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_no_distinct">Спробуйте самі</a>
</div>



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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_where">Спробуйте самі</a>
</div>


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

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_where_number">Спробуйте самі</a>
</div>


## Оператори в реченні WHERE
Для фільтрації пошуку можна використовувати інші оператори, крім оператора `=`.

### приклад
Виберіть усіх клієнтів із CustomerID більше 80:
```sql
SELECT * FROM Customers
WHERE CustomerID > 80;
```

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_where_gt">Спробуйте самі</a>
</div>


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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_orderby_price">Спробуйте самі</a>
</div>


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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_orderby_price_desc">Спробуйте самі</a>
</div>

## Порядок в алфавітному порядку

Для рядкових значень `ORDER BY` ключове слово буде впорядковано в алфавітному порядку:

### приклад
Відсортуйте продукти в алфавітному порядку за назвою продукту:
```sql
SELECT * FROM Products
ORDER BY ProductName;
```

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_orderby_name">Спробуйте самі</a>
</div>

## За алфавітом DESC

Щоб відсортувати таблицю в зворотному алфавітному порядку, використовуйте `DESC` ключове слово:

### приклад
Відсортуйте продукти за назвою продукту у зворотному порядку:
```sql
SELECT * FROM Products
ORDER BY ProductName DESC;
```

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_orderby_name_desc">Спробуйте самі</a>
</div>

## ПОРЯДОК за кількома колонками
Наступний оператор SQL вибирає всіх клієнтів із таблиці «Клієнти», відсортованих за стовпцями «Країна» та «Назва клієнта». Це означає, що він упорядковує їх за країною, але якщо деякі рядки мають однакову країну, вони впорядковуються за назвою клієнта:

### приклад
```sql
SELECT * FROM Customers
ORDER BY Country, CustomerName;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_orderby2">Спробуйте самі</a>
</div>


## Використання як ASC, так і DESC
Наступний оператор SQL вибирає всіх клієнтів із таблиці «Клієнти», відсортованих за зростанням за стовпцем «Країна» та за спаданням за стовпцем «Назва клієнта»:

### приклад
```sql
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_orderby3">Спробуйте самі</a>
</div>

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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_and">Спробуйте самі</a>
</div>


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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_where_and_and">Спробуйте самі</a>
</div>


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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_and_or">Спробуйте самі</a>
</div>

Без дужок оператор `select` поверне всіх клієнтів з Іспанії, які починаються з «G», а також усіх клієнтів, які починаються з «R», незалежно від значення країни:

### приклад
Виберіть усіх клієнтів, які:
з Іспанії та починаються з літери "G" або
літери "R":
```sql
SELECT * FROM Customers
WHERE Country = 'Spain' AND CustomerName LIKE 'G%' OR CustomerName LIKE 'R%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_and_or2">Спробуйте самі</a>
</div>

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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_or">Спробуйте самі</a>
</div>

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

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_where_or_or">Спробуйте самі</a>
</div>

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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not">Спробуйте самі</a>
</div>


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
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not_like">Спробуйте самі</a>
</div>

## NOT BETWEEN
### приклад
Виберіть клієнтів із ідентифікатором клієнта не між 10 і 60:
```sql
SELECT * FROM Customers
WHERE CustomerID NOT BETWEEN 10 AND 60;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not_between2">Спробуйте самі</a>
</div>

## NOT IN
### приклад
Виберіть клієнтів, які не з Парижа чи Лондона:
```sql
SELECT * FROM Customers
WHERE City NOT IN ('Paris', 'London');
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not_in">Спробуйте самі</a>
</div>

## НЕ більше ніж
### приклад
Виберіть клієнтів з CustomerId не більше 50:
```sql
SELECT * FROM Customers
WHERE NOT CustomerID > 50;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not_gt">Спробуйте самі</a>
</div>

**Примітка**: існує оператор не більше: `!>` це дасть той самий результат.

## НЕ менше
### приклад
Виберіть клієнтів з CustomerID не менше 50:
```sql
SELECT * FROM Customers
WHERE NOT CustomerId < 50;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not_lt">Спробуйте самі</a>
</div>

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

___
<a name="Значення_SQL_NULL"></a>
# Значення SQL NULL
## Що таке значення NULL?
Поле зі значенням NULL є полем без значення.

Якщо поле в таблиці є необов’язковим, можна вставити новий запис або оновити запис, не додаючи значення до цього поля. Тоді поле буде збережено зі значенням NULL.

## Як перевірити значення NULL?
Неможливо перевірити значення NULL за допомогою операторів порівняння, таких як =, < або <>.

Замість цього нам доведеться використовувати оператори `IS NULL` and `IS NOT NULL`.

### Синтаксис IS NULL
```sql
SELECT column_names
FROM table_name
WHERE column_name IS NULL;
```

```sql
IS NOT NULL Синтаксис
SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;
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

## Оператор IS NULL
Оператор `IS NULL` використовується для перевірки порожніх значень (значення NULL).

Наступний SQL перераховує всіх клієнтів із значенням NULL у полі "Адреса":

### приклад
```sql
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NULL;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_is_null">Спробуйте самі</a>
</div>

## Оператор IS NOT NULL
Оператор `IS NOT NULL` використовується для перевірки непорожніх значень (НЕ NULL).

Наступний SQL перераховує всіх клієнтів із значенням у полі "Адреса":

### приклад
```sql
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NOT NULL;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_is_not_null">Спробуйте самі</a>
</div>

___
# Інструкція SQL UPDATE
Інструкція `UPDATE` використовується для зміни наявних записів у таблиці.

## UPDATE Синтаксис
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
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

## Таблиця UPDATE
Наступний оператор SQL оновлює першого клієнта (CustomerID = 1) за допомогою нової контактної особи та нового міста.
### приклад
```sql
UPDATE Customers
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE CustomerID = 1;
```

Вибір із таблиці «Клієнти» тепер виглядатиме так:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Alfred Schmidt | Obere Str. 57 | Frankfurt | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## UPDATE кількох записів
Це `WHERE` пункт, який визначає, скільки записів буде оновлено.

Наступна інструкція SQL оновить ContactName на "Juan" для всіх записів, де країна "Мексика":

### приклад
```sql
UPDATE Customers
SET ContactName='Juan'
WHERE Country='Mexico';
```
Вибір із таблиці «Клієнти» тепер виглядатиме так:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Alfred Schmidt | Obere Str. 57 | Frankfurt | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Juan | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Juan | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## Попередження про оновлення!
Будьте обережні при оновленні записів. Якщо ви опустите `WHERE` пункт, ВСІ записи будуть оновлені!

### приклад
```sql
UPDATE Customers
SET ContactName='Juan';
```

Вибір із таблиці «Клієнти» тепер виглядатиме так:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Juan | Obere Str. 57 | Frankfurt | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Juan | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Juan | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Juan | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Juan | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |
___
# Інструкція SQL DELETE

Інструкція `DELETE` використовується для видалення існуючих записів у таблиці.

## Синтаксис DELETE
```sql
DELETE FROM table_name WHERE condition;
```

Примітка. Будьте обережні, видаляючи записи в таблиці! Зверніть увагу на `WHERE` пункт у `DELETE` заяві. У `WHERE` пункті вказується, які записи слід видалити. Якщо ви опустите `WHERE` пункт, усі записи в таблиці будуть видалені!

## Демонстраційна база даних

Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Juan | Obere Str. 57 | Frankfurt | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Juan | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Juan | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Juan | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Juan | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## Приклад SQL DELETE
Наступний оператор SQL видаляє клієнта "Alfreds Futterkiste" із таблиці "Клієнти":

### приклад
```sql
DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';
```

Тепер таблиця «Клієнти» матиме такий вигляд:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## Видалити всі записи
Можна видалити всі рядки в таблиці, не видаляючи таблицю. Це означає, що структура таблиці, атрибути та індекси залишаться незмінними:
```sql
DELETE FROM table_name;
```

Наступний оператор SQL видаляє всі рядки в таблиці "Клієнти", не видаляючи таблицю:
### приклад
```sql
DELETE FROM Customers;
```

## Видалити таблицю
Щоб повністю видалити таблицю, скористайтеся оператором `DROP TABLE`:

### приклад
Видалення таблиці клієнтів:
```sql
DROP TABLE Customers;
```

# SQL SELECT TOP
Речення `SELECT TOP` використовується для визначення кількості записів, які потрібно повернути.

Цей `SELECT TOP` пункт корисний для великих таблиць із тисячами записів. Повернення великої кількості записів може вплинути на продуктивність.

### приклад
Виберіть лише перші 3 записи таблиці Клієнти:
```sql
SELECT TOP 3 * FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_top">Спробуйте самі</a>
</div>

## Демонстраційна база даних

Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Juan | Obere Str. 57 | Frankfurt | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Juan | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Juan | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Juan | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Juan | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## LIMIT
Наступний оператор SQL показує еквівалентний приклад для MySQL:

### приклад
Виберіть перші 3 записи таблиці Клієнти:
```sql
SELECT * FROM Customers
LIMIT 3;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_select_limit">Спробуйте самі</a>
</div>

## FETCH FIRST
Наступний оператор SQL показує еквівалентний приклад для Oracle:

### приклад
Виберіть перші 3 записи таблиці Клієнти:
```sql
SELECT * FROM Customers
FETCH FIRST 3 ROWS ONLY;
```

## Приклад ВЕРШОГО ВІДСОТКУ SQL
Наступний оператор SQL вибирає перші 50% записів із таблиці «Клієнти» (для SQL Server/MS Access):

### приклад
```sql
SELECT TOP 50 PERCENT * FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_top_percent">Спробуйте самі</a>
</div>

## ДОДАТИ РЕЧЕННЯ WHERE
Наступний оператор SQL вибирає перші три записи з таблиці «Клієнти», де країна — «Німеччина» (для SQL Server/MS Access):

### приклад
```sql
SELECT TOP 3 * FROM Customers
WHERE Country='Germany';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_top_where">Спробуйте самі</a>
</div>

## ДОДАТИ ПОРЯДОК ЗА Ключовим словом
Додайте `ORDER BY` ключове слово, якщо хочете відсортувати результат, і поверніть перші 3 записи відсортованого результату.

Для SQL Server і MS Access:

### приклад
Відсортуйте результат в алфавітному порядку за ім’ям клієнта та поверніть перші 3 записи:
```sql
SELECT TOP 3 * FROM Customers
ORDER BY CustomerName DESC;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_top_orderby">Спробуйте самі</a>
</div>

___
# Агрегатні функції SQL
Агрегатна функція – це функція, яка виконує обчислення набору значень і повертає одне значення.

Агрегатні функції часто використовуються з `GROUP BY` умовою оператора `SELECT`. Речення `GROUP BY` розбиває набір результатів на групи значень, а агрегатну функцію можна використовувати для повернення окремого значення для кожної групи.

Найпоширенішими агрегатними функціями SQL є:
+ `MIN()` - повертає найменше значення у вибраному стовпці
+ `MAX()` - повертає найбільше значення у вибраному стовпці
+ `COUNT()` - повертає кількість рядків у наборі
+ `SUM()` - повертає загальну суму числового стовпця
+ `AVG()` - повертає середнє значення числового стовпця

Агрегатні функції ігнорують нульові значення (крім `COUNT()`).

___
# Функції SQL MIN() і MAX().
Функція `MIN()` повертає найменше значення вибраного стовпця.

Функція `MAX()` повертає найбільше значення вибраного стовпця.

## Приклад MINО
Знайдіть найнижчу ціну в стовпці Ціна:
```sql
SELECT MIN(Price)
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_min">Спробуйте самі</a>
</div>

## Приклад MAX
Знайдіть найвищу ціну в стовпці Ціна:
```sql
SELECT MAX(Price)
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_max">Спробуйте самі</a>
</div>


## Синтаксис
```sql
SELECT MIN(column_name)
FROM table_name
WHERE condition;
```

```sql
SELECT MAX(column_name)
FROM table_name
WHERE condition;
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Продукти» , яка використовується в прикладах:

| ProductID | ProductName                 | SupplierID | CategoryID | Unit                 | Price |
|-----------|-----------------------------|------------|------------|----------------------|-------|
| 1         | Chais                       | 1          | 1          | 10 boxes x 20 bags   | 18    |
| 2         | Chang                       | 1          | 1          | 24 - 12 oz bottles   | 19    |
| 3         | Aniseed Syrup               | 1          | 2          | 12 - 550 ml bottles  | 10    |
| 4         | Chef Anton's Cajun Seasoning| 2          | 2          | 48 - 6 oz jars       | 22    |
| 5         | Chef Anton's Gumbo Mix      | 2          | 2          | 36 boxes             | 21.35 |


## Встановити назву стовпця (псевдонім)
Якщо ви використовуєте `MIN()` або `MAX()`, повернутий стовпець не матиме описової назви. Щоб дати стовпцю описову назву, використовуйте `AS` ключове слово:

### приклад
```sql
SELECT MIN(Price) AS SmallestPrice
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_min_as">Спробуйте самі</a>
</div>

## Використовуйте MIN() із GROUP BY
Тут ми використовуємо `MIN()`функцію та `GROUP BY` пункт, щоб повернути найменшу ціну для кожної категорії в таблиці Products:

### приклад
```sql
SELECT MIN(Price) AS SmallestPrice, CategoryID
FROM Products
GROUP BY CategoryID;
```

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_min_groupby">Спробуйте самі</a>
</div>

# Функція SQL COUNT()
Функція `COUNT()` повертає кількість рядків, які відповідають заданому критерію.
### приклад
Знайдіть загальну кількість рядків у Products таблиці:
```sql
SELECT COUNT(*)
FROM Products;
```

##Синтаксис
```sql
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Продукти» , яка використовується в прикладах:
| ProductID | ProductName                 | SupplierID | CategoryID | Unit                 | Price |
|-----------|-----------------------------|------------|------------|----------------------|-------|
| 1         | Chais                       | 1          | 1          | 10 boxes x 20 bags   | 18    |
| 2         | Chang                       | 1          | 1          | 24 - 12 oz bottles   | 19    |
| 3         | Aniseed Syrup               | 1          | 2          | 12 - 550 ml bottles  | 10    |
| 4         | Chef Anton's Cajun Seasoning| 2          | 2          | 48 - 6 oz jars       | 22    |
| 5         | Chef Anton's Gumbo Mix      | 2          | 2          | 36 boxes             | 21.35 |

## Укажіть стовпець
Ви можете вказати назву стовпця замість символу зірочки `(*)`.

Якщо ви вкажете назву стовпця замість `(*)`, значення NULL не будуть зараховані.

### приклад
Знайдіть кількість продуктів, де ProductNameне дорівнює нулю:
```sql
SELECT COUNT(ProductName)
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_count3">Спробуйте самі</a>
</div>

## Додайте речення WHERE
Ви можете додати `WHERE` пункт, щоб визначити умови:

### приклад
Знайдіть кількість продуктів, у яких `Price` більше 20:
```sql
SELECT COUNT(ProductID)
FROM Products
WHERE Price > 20;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_count2">Спробуйте самі</a>
</div>

## Ігнорувати дублікати
Ви можете ігнорувати дублікати, використовуючи `DISTINCT` ключове слово у `COUNT()` функції.

Якщо `DISTINCT` вказано, рядки з однаковим значенням для вказаного стовпця вважатимуться одним.

### приклад
Скільки різних цін у `Products` таблиці:
```sql
SELECT COUNT(DISTINCT Price)
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_select_count_distinct">Спробуйте самі</a>
</div>

## Використовуйте псевдонім
Дайте назву підрахованому стовпцю за допомогою `AS` ключового слова.

### приклад
Назвіть стовпець «Кількість записів»:
```sql
SELECT COUNT(*) AS [Number of records]
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_count_as">Спробуйте самі</a>
</div>

## Використовуйте COUNT() із GROUP BY
Тут ми використовуємо `COUNT()` функцію та GROUP BYпропозицію, щоб повернути кількість записів для кожної категорії в таблиці Products:

### приклад
```sql
SELECT COUNT(*) AS [Number of records], CategoryID
FROM Products
GROUP BY CategoryID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_count_groupby">Спробуйте самі</a>
</div>


# Функція SQL SUM()
Функція SUM()повертає загальну суму числового стовпця.

### приклад
Повертає суму всіх Quantityполів у OrderDetailsтаблиці:
```sql
SELECT SUM(Quantity)
FROM OrderDetails;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_sum">Спробуйте самі</a>
</div>


## Синтаксис
```sql
SELECT SUM(column_name)
FROM table_name
WHERE condition;
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці OrderDetails, яка використовується в прикладах:

| OrderDetailID | OrderID | ProductID | Quantity |
|---------------|---------|-----------|----------|
| 1             | 10248   | 11        | 12       |
| 2             | 10248   | 42        | 10       |
| 3             | 10248   | 72        | 5        |
| 4             | 10249   | 14        | 9        |
| 5             | 10249   | 51        | 40       |


## Додайте речення WHERE
Ви можете додати `WHERE` пункт, щоб визначити умови:

### приклад
Повертає суму поля Quantityдля добутку з ProductID11:
```sql
SELECT SUM(Quantity)
FROM OrderDetails
WHERE ProductId = 11;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_sum_where">Спробуйте самі</a>
</div>

## Використовуйте псевдонім
Дайте назву підсумковому стовпцю за допомогою `AS` ключового слова.

### приклад
Назвіть стовпець «усього»:
```sql
SELECT SUM(Quantity) AS total
FROM OrderDetails;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_sum_as">Спробуйте самі</a>
</div>

## Використовуйте SUM() із GROUP BY
Тут ми використовуємо `SUM()` функцію та `GROUP BY` пропозицію, щоб повернути `Quantity` для кожного `OrderID` в таблиці OrderDetails:

### приклад
```sql
SELECT OrderID, SUM(Quantity) AS [Total Quantity]
FROM OrderDetails
GROUP BY OrderID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_sum_groupby">Спробуйте самі</a>
</div>

## SUM() з виразом
Параметр всередині `SUM()` функції також може бути виразом.

Якщо припустити, що кожен продукт у `OrderDetails` стовпчику коштує 10 доларів, ми можемо знайти загальний прибуток у доларах, помноживши кожну кількість на 10:

### приклад
Використовуйте вираз у `SUM()` функції:
```sql
SELECT SUM(Quantity * 10)
FROM OrderDetails;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_sum2">Спробуйте самі</a>
</div>

Ми також можемо приєднати `OrderDetails` таблицю до `Products` таблиці, щоб знайти фактичну суму, замість того, щоб вважати, що вона становить 10 доларів:

### приклад
Приєднайтеся `OrderDetails` до `Products`, і використовуйте `SUM()`, щоб знайти загальну суму:
```sql
SELECT SUM(Price * Quantity)
FROM OrderDetails
LEFT JOIN Products ON OrderDetails.ProductID = Products.ProductID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_sum3">Спробуйте самі</a>
</div>

___
# Функція SQL AVG()
Функція AVG()повертає середнє значення числового стовпця.

### приклад
Знайдіть середню ціну всіх товарів:
```sql
SELECT AVG(Price)
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_avg">Спробуйте самі</a>
</div>

## Синтаксис
```sql
SELECT AVG(column_name)
FROM table_name
WHERE condition;
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Продукти» , яка використовується в прикладах:

| ProductID | ProductName                 | SupplierID | CategoryID | Unit                 | Price |
|-----------|-----------------------------|------------|------------|----------------------|-------|
| 1         | Chais                       | 1          | 1          | 10 boxes x 20 bags   | 18    |
| 2         | Chang                       | 1          | 1          | 24 - 12 oz bottles   | 19    |
| 3         | Aniseed Syrup               | 1          | 2          | 12 - 550 ml bottles  | 10    |
| 4         | Chef Anton's Cajun Seasoning| 2          | 2          | 48 - 6 oz jars       | 22    |
| 5         | Chef Anton's Gumbo Mix      | 2          | 2          | 36 boxes             | 21.35 |

## Додайте речення WHERE
Ви можете додати `WHERE` пункт, щоб визначити умови:

### приклад
Поверніть середню ціну продуктів у категорії 1:
```sql
SELECT AVG(Price)
FROM Products
WHERE CategoryID = 1;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_avg_where">Спробуйте самі</a>
</div>

## Використовуйте псевдонім
Дайте назву стовпцю AVG за допомогою `AS` ключового слова.

### приклад
Назвіть стовпець «середня ціна»:
```sql
SELECT AVG(Price) AS [average price]
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_avg_as">Спробуйте самі</a>
</div>

## Вище середнього
Щоб отримати список усіх записів із ціною, вищою за середню, ми можемо використати `AVG()` функцію у підзапиті:

### приклад
Повернути всі товари з ціною вищою за середню:
```sql
SELECT * FROM Products
WHERE price > (SELECT AVG(price) FROM Products);
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_avg2">Спробуйте самі</a>
</div>

## Використовуйте AVG() із GROUP BY
Тут ми використовуємо `AVG()` функцію та `GROUP BY` речення, щоб повернути середню ціну для кожної категорії в таблиці Products:

### приклад
```sql
SELECT AVG(Price) AS AveragePrice, CategoryID
FROM Products
GROUP BY CategoryID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_avg_groupby">Спробуйте самі</a>
</div>

___
# Оператор SQL LIKE
Оператор `LIKE` використовується в `WHERE` пропозиції для пошуку заданого шаблону в стовпці.

У поєднанні з оператором часто використовуються два символи підстановки `LIKE`:

 Знак відсотка `%` означає нуль, один або декілька символів
 Знак підкреслення `_` означає один символ

### приклад
Виберіть усіх клієнтів, які починаються з літери «а»:
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'a%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like">Спробуйте самі</a>
</div>

## Синтаксис
```sql
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName                      | ContactName    | Address                   | City         | PostalCode | Country |
|------------|-----------------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Obere Str. 57             | Berlin       | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mataderos 2312            | México D.F.  | 05023      | Mexico  |
| 4          | Around the Horn                   | Thomas Hardy   | 120 Hanover Sq.           | London       | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                | Christina Berglund | Berguvsvägen 8        | Luleå       | S-958 22   | Sweden  |

## Символ підстановки _
Символ `_` підстановки представляє один символ.

Це може бути будь-який символ або число, але кожен `_` представляє один і тільки один символ.

### приклад
Повернути всіх клієнтів із міста, яке починається з «L», за яким іде один символ підстановки, потім «nd», а потім два символи підстановки:
```sql
SELECT * FROM Customers
WHERE city LIKE 'L_nd__';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_london">Спробуйте самі</a>
</div>

## Символ підстановки %
Символ `%` підстановки представляє будь-яку кількість символів, навіть нуль символів.

### приклад
Повернути всіх клієнтів з міста, яке містить літеру "L":
```sql
SELECT * FROM Customers
WHERE city LIKE '%L%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_l">Спробуйте самі</a>
</div>

## Починається з
Щоб повернути записи, які починаються з певної літери або фрази, додайте `%` в кінці літери або фрази.

### приклад
Повернути всіх клієнтів, які починаються з "La":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'La%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_la">Спробуйте самі</a>
</div>


#### **Порада**. Ви також можете комбінувати будь-яку кількість умов за допомогою операторів ANDабо OR.

### приклад
Повернути всіх клієнтів, які починаються на "a" або на "b":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'a%' OR CustomerName LIKE 'b%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_ending2">Спробуйте самі</a>
</div>

## Закінчується на
Щоб повернути записи, які закінчуються певною літерою чи фразою, додайте `%` на початку літери чи фрази.

### приклад
Повернути всіх клієнтів, які закінчуються на "a":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '%a';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_ending">Спробуйте самі</a>
</div>

#### **Порада**. Ви також можете комбінувати "починається з" і "закінчується з":

### приклад
Повернути всіх клієнтів, які починаються на "b" і закінчуються на "s":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'b%s';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_startend">Спробуйте самі</a>
</div>

## Містить
Щоб повернути записи, які містять певну літеру чи фразу, додайте `%` до та після літери чи фрази.

### приклад
Повернути всіх клієнтів, які містять фразу "або"
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '%or%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_pattern">Спробуйте самі</a>
</div>

## Об'єднайте символи підстановки
Будь-який символ узагальнення, наприклад `%` і `_`, можна використовувати в поєднанні з іншими символами підстановки.

### приклад
Повернути всіх клієнтів, які починаються з "a" і містять принаймні 3 символи:
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'a__%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_start_least">Спробуйте самі</a>
</div>

### приклад
Повернути всіх клієнтів, які мають «r» на другій позиції:
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '_r%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_underscore">Спробуйте самі</a>
</div>

## Без символу підстановки
Якщо символ підстановки не вказано, фраза повинна мати точний збіг, щоб повернути результат.

### приклад
Повернути всіх клієнтів з Іспанії:
```sql
SELECT * FROM Customers
WHERE Country LIKE 'Spain';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_spain">Спробуйте самі</a>
</div>

___
# Символи підстановки SQL
Символ підстановки використовується для заміни одного або кількох символів у рядку.

З оператором використовуються символи підстановки . Оператор використовується в пропозиції для пошуку заданого шаблону в стовпці. `LIKE` `LIKE` `WHERE`

### приклад
Повернути всіх клієнтів, які починаються з літери "а":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'a%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_wildcard_a">Спробуйте самі</a>
</div>

## Символи підстановки

| Symbol | Description                                   |
|--------|-----------------------------------------------|
| %      | Represents zero or more characters            |
| _      | Represents a single character                 |
| []     | Represents any single character within the brackets * |
| ^      | Represents any character not in the brackets * |
| -      | Represents any single character within the specified range * |
| {}     | Represents any escaped character ** |

* Не підтримується в базах даних PostgreSQL і MySQL.

* Підтримується лише в базах даних Oracle.

## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:

| CustomerID | CustomerName                      | ContactName    | Address                   | City         | PostalCode | Country |
|------------|-----------------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Obere Str. 57             | Berlin       | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mataderos 2312            | México D.F.  | 05023      | Mexico  |
| 4          | Around the Horn                   | Thomas Hardy   | 120 Hanover Sq.           | London       | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                | Christina Berglund | Berguvsvägen 8        | Luleå       | S-958 22   | Sweden  |


## Використання символу підстановки %
Символ `%` підстановки представляє будь-яку кількість символів, навіть нуль символів.

### приклад
Повернути всіх клієнтів, які закінчуються шаблоном "es":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '%es';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_wildcard_endswith">Спробуйте самі</a>
</div>

### приклад
Повернути всіх клієнтів, які містять шаблон "mer":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '%mer%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_wildcard_contains">Спробуйте самі</a>
</div>

## Використання символу підстановки _
Символ `_` підстановки представляє один символ.

Це може бути будь-який символ або число, але кожен `_` представляє один і тільки один символ.
### приклад
Повернути всіх клієнтів, які `City` починаються з будь-якого символу, після якого йде «ondon»:
```sql
SELECT * FROM Customers
WHERE City LIKE '_ondon';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_wildcard_underscore">Спробуйте самі</a>
</div>

приклад
Повернути всіх клієнтів, які `City` починаються з "L", за якими слідують будь-які 3 символи, що закінчуються "on":
```sql
SELECT * FROM Customers
WHERE City LIKE 'L___on';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_wildcard_3_underscores">Спробуйте самі</a>
</div>

## Використання символу підстановки [].
Символ `[]` підстановки повертає результат, якщо будь-який із символів усередині знайде збіг.

### приклад
Повернути всіх клієнтів, починаючи з "b", "s" або "p":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '[bsp]%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_wildcard_charlist">Спробуйте самі</a>
</div>

## Використання символу підстановки
Символ `-` узагальнення дозволяє вказати діапазон символів усередині цього `[]` символу.

### приклад
Повернути всіх клієнтів, які починаються на "a", "b", "c", "d", "e" або "f":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '[a-f]%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_wildcard_charlist2">Спробуйте самі</a>
</div>

## Об'єднайте символи підстановки
Будь-який символ узагальнення, наприклад `%` і `_` , можна використовувати в поєднанні з іншими символами підстановки.

### приклад
Повернути всіх клієнтів, які починаються з "a" і містять принаймні 3 символи:
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'a__%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_start_least">Спробуйте самі</a>
</div>

### приклад
Повернути всіх клієнтів, які мають «r» на другій позиції:
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '_r%';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_underscore">Спробуйте самі</a>
</div>

## Без символу підстановки
Якщо символ підстановки не вказано, фраза повинна мати точний збіг, щоб повернути результат.

### приклад
Повернути всіх клієнтів з Іспанії:
```sql
SELECT * FROM Customers
WHERE Country LIKE 'Spain';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_like_spain">Спробуйте самі</a>
</div>

## Символи підстановки Microsoft Access
База даних Microsoft Access має деякі інші символи підстановки:

| Symbol | Description                                   | Example                             |
|--------|-----------------------------------------------|-------------------------------------|
| *      | Represents zero or more characters            | bl* finds bl, black, blue, and blob |
| ?      | Represents a single character                 | h?t finds hot, hat, and hit         |
| []     | Represents any single character within the brackets | h[oa]t finds hot and hat, but not hit |
| !      | Represents any character not in the brackets | h[!oa]t finds hit, but not hot and hat |
| -      | Represents any single character within the specified range | c[a-b]t finds cat and cbt |
| #      | Represents any single numeric character | 2#5 finds 205, 215, 225, 235, 245, 255, 265, 275, 285, and 295 |

# Оператор SQL IN
Оператор `IN` дозволяє вказати кілька значень у `WHERE`реченні.

Оператор `IN` є скороченням кількох `OR` умов.

### приклад
Повернути всіх клієнтів із «Німеччини», «Франції» або «Великобританії»
```sql
SELECT * FROM Customers
WHERE Country IN ('Germany', 'France', 'UK');
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_in">Спробуйте самі</a>
</div>

## Синтаксис
```sql
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиці "Клієнти" , яка використовується в прикладах:
| CustomerID | CustomerName                      | ContactName    | Address                   | City         | PostalCode | Country |
|------------|-----------------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Obere Str. 57             | Berlin       | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mataderos 2312            | México D.F.  | 05023      | Mexico  |
| 4          | Around the Horn                   | Thomas Hardy   | 120 Hanover Sq.           | London       | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                | Christina Berglund | Berguvsvägen 8        | Luleå       | S-958 22   | Sweden  |

## НЕ В
Використовуючи `NOT` ключове слово перед `IN` оператором, ви повертаєте всі записи, які НЕ є жодним із значень у списку.

### приклад
Повернути всіх клієнтів, які НЕ з "Німеччини", "Франції" або "Великобританії":
```sql
SELECT * FROM Customers
WHERE Country NOT IN ('Germany', 'France', 'UK');
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not_in2">Спробуйте самі</a>
</div>

## В (ВИБРАТИ)
Ви також можете використовувати `IN` з підзапитом у `WHERE` реченні.

За допомогою підзапиту ви можете повернути всі записи з основного запиту, які присутні в результаті підзапиту.

### приклад
Повернути всіх клієнтів, які мають замовлення, у таблиці «Замовлення» :
```sql
SELECT * FROM Customers
WHERE CustomerID IN (SELECT CustomerID FROM Orders);
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_in2">Спробуйте самі</a>
</div>

## НЕ В (ВИБРАТИ)
Результат у наведеному вище прикладі повернув 74 записи, що означає, що є 17 клієнтів, які не розмістили жодного замовлення.

Давайте перевіримо, чи це правильно, за допомогою `NOT IN` оператора.

приклад
Повернути всіх клієнтів, які НЕ зробили жодного замовлення, у таблицю «Замовлення» :
```sql
SELECT * FROM Customers
WHERE CustomerID NOT IN (SELECT CustomerID FROM Orders);
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_in_not">Спробуйте самі</a>
</div>

___
# Оператор SQL BETWEEN
Оператор `BETWEEN` вибирає значення в заданому діапазоні. Значеннями можуть бути числа, текст або дати.

Оператор `BETWEEN` включає: початкове та кінцеве значення включено. 

### приклад
Вибирає всі товари з ціною від 10 до 20:
```sql
SELECT * FROM Products
WHERE Price BETWEEN 10 AND 20;
```

## Синтаксис
```sql
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Продукти» , яка використовується в прикладах:
| ProductID | ProductName                 | SupplierID | CategoryID | Unit                 | Price |
|-----------|-----------------------------|------------|------------|----------------------|-------|
| 1         | Chais                       | 1          | 1          | 10 boxes x 20 bags   | 18    |
| 2         | Chang                       | 1          | 1          | 24 - 12 oz bottles   | 19    |
| 3         | Aniseed Syrup               | 1          | 2          | 12 - 550 ml bottles  | 10    |
| 4         | Chef Anton's Cajun Seasoning| 2          | 2          | 48 - 6 oz jars       | 22    |
| 5         | Chef Anton's Gumbo Mix      | 2          | 2          | 36 boxes             | 21.35 |

## НЕ МІЖ
Щоб відобразити продукти поза діапазоном попереднього прикладу, використовуйте `NOT BETWEEN`:

### приклад
```sql
SELECT * FROM Products
WHERE Price NOT BETWEEN 10 AND 20;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not_between">Спробуйте самі</a>
</div>

## МІЖ з В
Наступний оператор SQL вибирає всі продукти з ціною від 10 до 20. Крім того, CategoryID має мати значення 1, 2 або 3:

### приклад
```sql
SELECT * FROM Products
WHERE Price BETWEEN 10 AND 20
AND CategoryID IN (1,2,3);
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_between_in">Спробуйте самі</a>
</div>

## МІЖ текстовими значеннями
Наступний оператор SQL вибирає всі продукти з ProductName в алфавітному порядку між Carnarvon Tigers і Mozzarella di Giovanni:

### приклад
```sql
SELECT * FROM Products
WHERE ProductName BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni'
ORDER BY ProductName;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_between_text">Спробуйте самі</a>
</div>

Наступний оператор SQL вибирає всі продукти з ProductName між Carnarvon Tigers і Chef Anton's Cajun Seasoning:

### приклад
```sql
SELECT * FROM Products
WHERE ProductName BETWEEN "Carnarvon Tigers" AND "Chef Anton's Cajun Seasoning"
ORDER BY ProductName;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_between_text2">Спробуйте самі</a>
</div>

## НЕ МІЖ текстовими значеннями
Наступний оператор SQL вибирає всі продукти з ProductName не між Carnarvon Tigers і Mozzarella di Giovanni:

### приклад
```sql
SELECT * FROM Products
WHERE ProductName NOT BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni'
ORDER BY ProductName;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_not_between_text">Спробуйте самі</a>
</div>

## МІЖ датами
Наступний оператор SQL вибирає всі замовлення з OrderDate між «01-July-1996» і «31-July-1996»:

### приклад
```sql
SELECT * FROM Orders
WHERE OrderDate BETWEEN #07/01/1996# AND #07/31/1996#;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_between_date">Спробуйте самі</a>
</div>

АБО:

### приклад
```
SELECT * FROM Orders
WHERE OrderDate BETWEEN '1996-07-01' AND '1996-07-31';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_select_between_date2">Спробуйте самі</a>
</div>

## Зразок таблиці
Нижче наведено вибірку з таблиці замовлень , яка використовується в прикладах:

| OrderID | CustomerID | EmployeeID | OrderDate | ShipperID |
|---------|------------|------------|-----------|-----------|
| 10248   | 90         | 5          | 7/4/1996  | 3         |
| 10249   | 81         | 6          | 7/5/1996  | 1         |
| 10250   | 34         | 4          | 7/8/1996  | 2         |
| 10251   | 84         | 3          | 7/9/1996  | 1         |
| 10252   | 76         | 4          | 7/10/1996 | 2         |

# Псевдоніми SQL

Псевдоніми SQL
Псевдоніми SQL використовуються для надання таблиці або стовпцю в таблиці тимчасового імені.

Псевдоніми часто використовуються, щоб зробити назви стовпців більш читабельними.

Псевдонім існує лише протягом цього запиту.

Псевдонім створюється за допомогою `AS` ключового слова.

### приклад
```sql
SELECT CustomerID AS ID
FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_alias1">Спробуйте самі</a>
</div>

## AS необов'язковий
Фактично, у більшості мов баз даних ви можете пропустити ключове слово AS і отримати той самий результат:

### приклад
```sql
SELECT CustomerID ID
FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_select_alias2">Спробуйте самі</a>
</div>

## Синтаксис
Коли псевдонім використовується в стовпці:
```sql
SELECT column_name AS alias_name
FROM table_name;
```
Коли в таблиці використовується псевдонім:
```sql
SELECT column_name(s)
FROM table_name AS alias_name;
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиць «Клієнти» та «Замовлення» , які використовуються в прикладах.

Клієнти
| CustomerID | CustomerName                      | ContactName    | Address                   | City         | PostalCode | Country |
|------------|-----------------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Obere Str. 57             | Berlin       | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mataderos 2312            | México D.F.  | 05023      | Mexico  |

Замовлення

| OrderID | CustomerID | EmployeeID | OrderDate | ShipperID |
|---------|------------|------------|-----------|-----------|
| 10248   | 90         | 5          | 7/4/1996  | 3         |
| 10249   | 81         | 6          | 7/5/1996  | 1         |
| 10250   | 34         | 4          | 7/8/1996  | 2         |

## Псевдонім для стовпців
Наступний оператор SQL створює два псевдоніми, один для стовпця CustomerID і інший для стовпця CustomerName:

### приклад
```sql
SELECT CustomerID AS ID, CustomerName AS Customer
FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_alias_column0">Спробуйте самі</a>
</div>

## Використання псевдонімів із символом пробілу
Якщо ви хочете, щоб ваш псевдонім містив один або кілька пробілів, наприклад «`My Great Products`», візьміть псевдонім у квадратні дужки або подвійні лапки.

### приклад
Використання [квадратних дужок] для псевдонімів із пробілами:
```sql
SELECT ProductName AS [My Great Products]
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_alias_brackets">Спробуйте самі</a>
</div>

### приклад
Використання «подвійних лапок» для псевдонімів із пробілами:
```sql
SELECT ProductName AS "My Great Products"
FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_alias_quotes">Спробуйте самі</a>
</div>

## Об’єднати стовпці
Наступний оператор SQL створює псевдонім із назвою «Адреса», який об’єднує чотири стовпці (адреса, поштовий індекс, місто та країна):

### приклад
```sql
SELECT CustomerName, Address + ', ' + PostalCode + ' ' + City + ', ' + Country AS Address
FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_alias_column2">Спробуйте самі</a>
</div>

#### **Примітка**. Щоб наведений вище оператор SQL працював у MySQL, використовуйте наступне:

### Приклад MySQL
```sql
SELECT CustomerName, CONCAT(Address,', ',PostalCode,', ',City,', ',Country) AS Address
FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_select_alias_mysql_concat">Спробуйте самі</a>
</div>

## Псевдонім для таблиць
Ці ж правила застосовуються, якщо ви хочете використовувати псевдонім для таблиці.

### приклад
Натомість використовуйте таблицю "Клієнти" як "Особи":
```sql
SELECT * FROM Customers AS Persons;
```
Може здатися марним використовувати псевдоніми для таблиць, але коли ви використовуєте більше однієї таблиці у своїх запитах, це може зробити оператори SQL коротшими.

Наступний оператор SQL вибирає всі замовлення від клієнта з CustomerID=4 (Around the Horn). Ми використовуємо таблиці «Клієнти» та «Замовлення» та надаємо їм псевдоніми таблиць «c» та «o» відповідно (тут ми використовуємо псевдоніми, щоб зробити SQL коротшим):

### приклад
```sql
SELECT o.OrderID, o.OrderDate, c.CustomerName
FROM Customers AS c, Orders AS o
WHERE c.CustomerName='Around the Horn' AND c.CustomerID=o.CustomerID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_alias_table">Спробуйте самі</a>
</div>

Наступний оператор SQL такий самий, як і вище, але без псевдонімів:

### приклад
```sql
SELECT Orders.OrderID, Orders.OrderDate, Customers.CustomerName
FROM Customers, Orders
WHERE Customers.CustomerName='Around the Horn' AND Customers.CustomerID=Orders.CustomerID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_alias_no">Спробуйте самі</a>
</div>

#### Псевдоніми можуть бути корисними, коли:

+ У запиті бере участь більше однієї таблиці
+ У запиті використовуються функції
+ Назви стовпців великі або погано читаються
+ Два або більше стовпців об'єднують разом
  
___
# SQL об'єднання
Речення `JOIN` використовується для об’єднання рядків з двох або більше таблиць на основі пов’язаного стовпця між ними.

Розглянемо вибірку з таблиці «Замовлення»:
| OrderID | CustomerID | OrderDate  |
|---------|------------|------------|
| 10308   | 2          | 1996-09-18 |
| 10309   | 37         | 1996-09-19 |
| 10310   | 77         | 1996-09-20 |

Потім перегляньте вибір із таблиці «Клієнти»:

| CustomerID | CustomerName                      | ContactName    | Country |
|------------|-----------------------------------|----------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mexico  |

Зауважте, що стовпець «CustomerID» у таблиці «Orders» відноситься до «CustomerID» у таблиці «Customers». Зв’язок між двома таблицями вище – це стовпець «CustomerID».

Потім ми можемо створити такий оператор SQL (який містить `INNER JOIN`), який вибирає записи, що мають відповідні значення в обох таблицях:

### приклад
```sql
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders
INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_join">Спробуйте самі</a>
</div>

#### і це створить щось на зразок цього:

| OrderID | CustomerName                      | OrderDate  |
|---------|-----------------------------------|------------|
| 10308   | Ana Trujillo Emparedados y helados| 9/18/1996  |
| 10365   | Antonio Moreno Taquería           | 11/27/1996 |
| 10383   | Around the Horn                   | 12/16/1996 |
| 10355   | Around the Horn                   | 11/15/1996 |
| 10278   | Berglunds snabbköp                | 8/12/1996  |

## Різні типи SQL JOIN
Ось різні типи JOIN у SQL:

`(INNER) JOIN`: повертає записи, які мають відповідні значення в обох таблицях
`LEFT (OUTER) JOIN`: повертає всі записи з лівої таблиці та відповідні записи з правої таблиці
`RIGHT (OUTER) JOIN`: повертає всі записи з правої таблиці та відповідні записи з лівої таблиці
`FULL (OUTER) JOIN`: повертає всі записи, якщо є відповідність у лівій або правій таблиці

![alt text](image.png)
![alt text](image-1.png)
![alt text](image-2.png)
![alt text](image-3.png)

___
# SQL INNER JOIN
Ключове `INNER JOIN` слово вибирає записи, які мають відповідні значення в обох таблицях.

Давайте подивимося на вибір таблиці Продукти :

| ProductID | ProductName   | CategoryID | Price |
|-----------|---------------|------------|-------|
| 1         | Chais         | 1          | 18    |
| 2         | Chang         | 1          | 19    |
| 3         | Aniseed Syrup | 2          | 10    |

І вибір таблиці категорій :

| CategoryID | CategoryName | Description                                       |
|------------|--------------|---------------------------------------------------|
| 1          | Beverages    | Soft drinks, coffees, teas, beers, and ales       |
| 2          | Condiments   | Sweet and savory sauces, relishes, spreads, and seasonings |
| 3          | Confections  | Desserts, candies, and sweet breads               |

Ми об’єднаємо таблицю «Продукти» з таблицею «Категорії», використовуючи `CategoryID` поле з обох таблиць:

прикладОтримайте власний SQL Server
Об’єднайте продукти та категорії за допомогою ключового слова `INNER JOIN`:
```sql
SELECT ProductID, ProductName, CategoryName
FROM Products
INNER JOIN Categories ON Products.CategoryID = Categories.CategoryID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_join_inner_prod">Спробуйте самі</a>
</div>

##
![alt text](image-4.png)

#### Примітка. Ключове `INNER JOIN` слово повертає лише рядки з відповідністю в обох таблицях. Це означає, що якщо у вас є продукт без CategoryID або з CategoryID, якого немає в таблиці Categories, цей запис не буде повернено в результаті.

## Синтаксис
```sql
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```
## Назви колонок
Рекомендується включати назву таблиці під час визначення стовпців у операторі SQL.

### приклад
Вкажіть назви таблиць:
```sql
SELECT Products.ProductID, Products.ProductName, Categories.CategoryName
FROM Products
INNER JOIN Categories ON Products.CategoryID = Categories.CategoryID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_join_inner_prod2">Спробуйте самі</a>
</div>

Наведений вище приклад працює без вказівки імен таблиць, оскільки жодна з указаних імен стовпців не присутня в обох таблицях. Якщо ви спробуєте включити `CategoryID` в `SELECT` оператор, ви отримаєте повідомлення про помилку, якщо не вкажете назву таблиці (оскільки `CategoryID` присутня в обох таблицях).

## JOIN або INNER JOIN
`JOIN` і `INNER JOIN` поверне той самий результат.

`INNER` є типовим типом об’єднання для `JOIN`, тому, коли ви пишете, `JOIN` аналізатор фактично записує INNER `JOIN`.

### приклад
JOIN те саме, що INNER JOIN:
```sql
SELECT Products.ProductID, Products.ProductName, Categories.CategoryName
FROM Products
JOIN Categories ON Products.CategoryID = Categories.CategoryID;
```

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_select_join_inner_prod3">Спробуйте самі</a>
</div>

## ПРИЄДНАЙТЕСЬ до трьох столів
Наступний оператор SQL вибирає всі замовлення з інформацією про клієнта та відправника:

### приклад
```sql
SELECT Orders.OrderID, Customers.CustomerName, Shippers.ShipperName
FROM ((Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID)
INNER JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID);
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_join_inner2">Спробуйте самі</a>
</div>

# SQL LEFT JOIN

Ключове `LEFT JOIN` слово повертає всі записи з лівої таблиці (таблиця1) і відповідні записи з правої таблиці (таблиця2). Результатом буде 0 записів з правого боку, якщо немає відповідності.

## Синтаксис LEFT JOIN
```sql
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

#### Примітка. У деяких базах даних LEFT JOIN називається LEFT OUTER JOIN.

![alt text](image-5.png)

## Демонстраційна база даних
У цьому підручнику ми будемо використовувати відомий приклад бази даних Northwind.

Нижче наведено вибір із таблиці «Клієнти»:
| CustomerID | CustomerName                      | ContactName    | Country |
|------------|-----------------------------------|----------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mexico  |

І вибірка з таблиці «Замовлення»:

| OrderID | CustomerID | EmployeeID | OrderDate  | ShipperID |
|---------|------------|------------|------------|-----------|
| 10308   | 2          | 7          | 1996-09-18 | 3         |
| 10309   | 37         | 3          | 1996-09-19 | 1         |
| 10310   | 77         | 8          | 1996-09-20 | 2         |

## Приклад SQL LEFT JOIN
Наступний оператор SQL вибере всіх клієнтів і будь-які замовлення, які вони можуть мати:

### приклад
```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID
ORDER BY Customers.CustomerName;
```

___
# SQL RIGHT JOIN
Ключове RIGHT JOINслово повертає всі записи з правої таблиці (table2) і відповідні записи з лівої таблиці (table1). Результатом є 0 записів зліва, якщо немає відповідності.

## Синтаксис RIGHT JOIN
```sql
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_join_left">Спробуйте самі</a>
</div>

#### Примітка. У деяких базах даних `RIGHT JOIN` називається `RIGHT OUTER JOIN`.

![alt text](image-6.png)

Демонстраційна база даних
У цьому підручнику ми будемо використовувати відомий приклад бази даних Northwind.

Нижче наведено вибір із таблиці «Замовлення»:
| OrderID | CustomerID | EmployeeID | OrderDate  | ShipperID |
|---------|------------|------------|------------|-----------|
| 10308   | 2          | 7          | 1996-09-18 | 3         |
| 10309   | 37         | 3          | 1996-09-19 | 1         |
| 10310   | 77         | 8          | 1996-09-20 | 2         |

І вибірка з таблиці "Співробітники":
| EmployeeID | LastName  | FirstName | BirthDate | Photo     |
|------------|-----------|-----------|-----------|-----------|
| 1          | Davolio   | Nancy     | 12/8/1968 | EmpID1.pic|
| 2          | Fuller    | Andrew    | 2/19/1952 | EmpID2.pic|
| 3          | Leverling | Janet     | 8/30/1963 | EmpID3.pic|

## Приклад SQL RIGHT JOIN
Наступний оператор SQL поверне всіх співробітників і будь-які замовлення, які вони могли розмістити:

### приклад
```sql
SELECT Orders.OrderID, Employees.LastName, Employees.FirstName
FROM Orders
RIGHT JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
ORDER BY Orders.OrderID;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_join_right">Спробуйте самі</a>
</div>

___
# SQL FULL OUTER JOIN

Ключове `FULL OUTER JOIN` слово повертає всі записи, якщо є відповідність у лівих (таблиця1) або правих (таблиця2) записах таблиці.

Порада: `FULL OUTER JOIN` і `FULL JOIN` однакові.
```sql
FULL OUTER JOIN Синтаксис
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;
```

![alt text](image-7.png)

## Демонстраційна база даних
У цьому підручнику ми будемо використовувати відомий приклад бази даних Northwind.

Нижче наведено вибір із таблиці «Клієнти»:
| CustomerID | CustomerName                      | ContactName    | Country |
|------------|-----------------------------------|----------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mexico  |

І вибірка з таблиці «Замовлення»:

| OrderID | CustomerID | EmployeeID | OrderDate  | ShipperID |
|---------|------------|------------|------------|-----------|
| 10308   | 2          | 7          | 1996-09-18 | 3         |
| 10309   | 37         | 3          | 1996-09-19 | 1         |
| 10310   | 77         | 8          | 1996-09-20 | 2         |


## SQL FULL OUTER JOIN Приклад
Наступний оператор SQL вибирає всіх клієнтів і всі замовлення:
```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
```
Вибір із набору результатів може виглядати так:

| CustomerName                      | OrderID |
|-----------------------------------|---------|
| Null                              | 10309   |
| Null                              | 10310   |
| Alfreds Futterkiste               | Null    |
| Ana Trujillo Emparedados y helados| 10308   |
| Antonio Moreno Taquería           | Null    |

Примітка. Ключове `FULL OUTER JOIN` слово повертає всі відповідні записи з обох таблиць незалежно від того, відповідає інша таблиця чи ні. Таким чином, якщо є рядки в «Клієнти», які не мають збігів у «Замовленнях», або якщо є рядки в «Замовленнях», які не мають збігів у «Клієнтах», ці рядки також будуть перераховані.

___
# SQL Self Join

Самооб’єднання є звичайним об’єднанням, але таблиця об’єднується сама з собою.

Синтаксис самооб'єднання
```sql
SELECT column_name(s)
FROM table1 T1, table1 T2
WHERE condition;
```
T1 і T2 є різними псевдонімами для однієї таблиці.

## Демонстраційна база даних
У цьому підручнику ми будемо використовувати відомий приклад бази даних Northwind.

Нижче наведено вибір із таблиці «Клієнти»:

| CustomerID | CustomerName                      | ContactName    | Country |
|------------|-----------------------------------|----------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mexico  |

## Приклад самостійного приєднання SQL
Наступний оператор SQL відповідає клієнтам з одного міста:

### приклад
```sql
SELECT A.CustomerName AS CustomerName1, B.CustomerName AS CustomerName2, A.City
FROM Customers A, Customers B
WHERE A.CustomerID <> B.CustomerID
AND A.City = B.City
ORDER BY A.City;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_join_self">Спробуйте самі</a>
</div>

___
# SQL UNION
Оператор `UNION` використовується для поєднання набору результатів двох або більше `SELECT` операторів.

+ Кожен `SELECT` оператор усередині `UNION` повинен мати однакову кількість стовпців
+ Стовпці також повинні мати подібні типи даних
+ Стовпці в кожній `SELECT`заяві також мають бути в однаковому порядку
## Синтаксис UNION
```sql
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```

## Синтаксис UNION ALL
`UNION` За замовчуванням оператор вибирає лише різні значення . Щоб дозволити повторювані значення, використовуйте `UNION ALL`:
```sql
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
```

Демонстраційна база даних
У цьому підручнику ми будемо використовувати відомий приклад бази даних Northwind.

Нижче наведено вибір із таблиці «Клієнти»:

| CustomerID | CustomerName                      | ContactName    | Country |
|------------|-----------------------------------|----------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mexico  |

І вибірка з таблиці «Постачальники»:

| SupplierID | SupplierName             | ContactName     | Address         | City       | PostalCode | Country |
|------------|--------------------------|-----------------|-----------------|------------|------------|---------|
| 1          | Exotic Liquid            | Charlotte Cooper| 49 Gilbert St.  | London     | EC1 4SD    | UK      |
| 2          | New Orleans Cajun Delights| Shelley Burke  | P.O. Box 78934  | New Orleans| 70117      | USA     |
| 3          | Grandma Kelly's Homestead| Regina Murphy  | 707 Oxford Rd.  | Ann Arbor  | 48104      | USA     |

## Приклад SQL UNION
Наступний оператор SQL повертає міста (тільки різні значення) з таблиці «Клієнти» та «Постачальники»:

### приклад
```sql
SELECT City FROM Customers
UNION
SELECT City FROM Suppliers
ORDER BY City;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_union">Спробуйте самі</a>
</div>

## Приклад SQL UNION ALL
Наступний оператор SQL повертає міста (також повторювані значення) з обох таблиць «Клієнти» та «Постачальники».

### приклад
```sql
SELECT City FROM Customers
UNION ALL
SELECT City FROM Suppliers
ORDER BY City;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_union_all">Спробуйте самі</a>
</div>

## ОБ'ЄДНАННЯ SQL з WHERE
Наступний оператор SQL повертає німецькі міста (лише різні значення) з обох таблиць «Клієнти» та «Постачальники».

### приклад
```sql
SELECT City, Country FROM Customers
WHERE Country='Germany'
UNION
SELECT City, Country FROM Suppliers
WHERE Country='Germany'
ORDER BY City;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_union2">Спробуйте самі</a>
</div>

## SQL UNION ALL With WHERE
Наступний оператор SQL повертає німецькі міста (також повторювані значення) з таблиці «Клієнти» та «Постачальники»:

### приклад
```sql
SELECT City, Country FROM Customers
WHERE Country='Germany'
UNION ALL
SELECT City, Country FROM Suppliers
WHERE Country='Germany'
ORDER BY City;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_union_all2">Спробуйте самі</a>
</div>

## Ще один приклад СОЮЗУ
Наступний оператор SQL містить список усіх клієнтів і постачальників:

### приклад
```sql
SELECT 'Customer' AS Type, ContactName, City, Country
FROM Customers
UNION
SELECT 'Supplier', ContactName, City, Country
FROM Suppliers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_union3">Спробуйте самі</a>
</div>

# Інструкція SQL GROUP BY
Інструкція `GROUP BY` групує рядки з однаковими значеннями в підсумкові рядки, наприклад «знайти кількість клієнтів у кожній країні».

Оператор GROUP BYчасто використовується з агрегатними функціями ( `COUNT(), MAX(), MIN(), SUM(), AVG()`) для групування набору результатів за одним або кількома стовпцями.

## GROUP BY Синтаксис
```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Клієнти» у прикладі бази даних Northwind:

| CustomerID | CustomerName                      | ContactName    | Address                   | City         | PostalCode | Country |
|------------|-----------------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Obere Str. 57             | Berlin       | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mataderos 2312            | México D.F.  | 05023      | Mexico  |
| 4          | Around the Horn                   | Thomas Hardy   | 120 Hanover Sq.           | London       | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                | Christina Berglund | Berguvsvägen 8        | Luleå       | S-958 22   | Sweden  |

## Приклади SQL GROUP BY
У наступному операторі SQL перераховано кількість клієнтів у кожній країні:

### приклад
```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_groupby">Спробуйте самі</a>
</div>

## У наведеному нижче операторі SQL перераховано кількість клієнтів у кожній країні, відсортованих від старшого до нижчого:

### приклад
```SQL
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
ORDER BY COUNT(CustomerID) DESC;
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Клієнти» у прикладі бази даних Northwind:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
|------------|-----------------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Obere Str. 57             | Berlin       | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mataderos 2312            | México D.F.  | 05023      | Mexico  |
| 4          | Around the Horn                   | Thomas Hardy   | 120 Hanover Sq.           | London       | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                | Christina Berglund | Berguvsvägen 8        | Luleå       | S-958 22   | Sweden  |

## Приклади SQL GROUP BY
У наступному операторі SQL перераховано кількість клієнтів у кожній країні:

### приклад
```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_groupby">Спробуйте самі</a>
</div>

У наведеному нижче операторі SQL перераховано кількість клієнтів у кожній країні, відсортованих від старшого до нижчого:

### приклад
```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
ORDER BY COUNT(CustomerID) DESC;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_groupby_orderby">Спробуйте самі</a>
</div>

## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Замовлення» у прикладі бази даних Northwind:
| OrderID | CustomerID | EmployeeID | OrderDate | ShipperID |
|---------|------------|------------|-----------|-----------|
| 10248   | 90         | 5          | 1996-07-04| 3         |
| 10249   | 81         | 6          | 1996-07-05| 1         |
| 10250   | 34         | 4          | 1996-07-08| 2         |

І вибірка з таблиці "Важдивідправники":

| ShipperID | ShipperName |
|-----------|-------------|
| 1         | Speedy Express |
| 2         | United Package |
| 3         | Federal Shipping |

## Приклад GROUP BY з JOIN
У наведеному нижче операторі SQL перераховано кількість замовлень, надісланих кожним відправником:

### приклад
```sql
SELECT Shippers.ShipperName, COUNT(Orders.OrderID) AS NumberOfOrders FROM Orders
LEFT JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID
GROUP BY ShipperName;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_groupby1">Спробуйте самі</a>
</div>

___
# SQL HAVING
Речення `HAVING` було додано до SQL, оскільки `WHERE` ключове слово не можна використовувати з агрегатними функціями.
```sql
HAVING Синтаксис
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Клієнти» у прикладі бази даних Northwind:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
|------------|-----------------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Obere Str. 57             | Berlin       | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mataderos 2312            | México D.F.  | 05023      | Mexico  |
| 4          | Around the Horn                   | Thomas Hardy   | 120 Hanover Sq.           | London       | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                | Christina Berglund | Berguvsvägen 8        | Luleå       | S-958 22   | Sweden  |

## Приклади SQL HAVING
У наступному операторі SQL перераховано кількість клієнтів у кожній країні. Включіть лише країни, у яких більше ніж 5 клієнтів:

### приклад
```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_having">Спробуйте самі</a>
</div>

У наведеному нижче операторі SQL перераховано кількість клієнтів у кожній країні, відсортованих від старшого до нижчого (включайте лише країни, де більше ніж 5 клієнтів):

### приклад
```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5
ORDER BY COUNT(CustomerID) DESC;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_having_orderby">Спробуйте самі</a>
</div>


## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Замовлення» у прикладі бази даних Northwind:

| OrderID | CustomerID | EmployeeID | OrderDate | ShipperID |
|---------|------------|------------|-----------|-----------|
| 10248   | 90         | 5          | 1996-07-04| 3         |
| 10249   | 81         | 6          | 1996-07-05| 1         |
| 10250   | 34         | 4          | 1996-07-08| 2         |

І вибірка з таблиці "Співробітники":

## Більше прикладів
У наведеному нижче операторі SQL перераховано співробітників, які зареєстрували понад 10 замовлень:

### приклад
```sql
SELECT Employees.LastName, COUNT(Orders.OrderID) AS NumberOfOrders
FROM (Orders
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID)
GROUP BY LastName
HAVING COUNT(Orders.OrderID) > 10;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_having2">Спробуйте самі</a>
</div>

Наступний оператор SQL перераховує, якщо співробітники "Davolio" або "Fuller" зареєстрували більше 25 замовлень:

### приклад
```
SELECT Employees.LastName, COUNT(Orders.OrderID) AS NumberOfOrders
FROM Orders
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
WHERE LastName = 'Davolio' OR LastName = 'Fuller'
GROUP BY LastName
HAVING COUNT(Orders.OrderID) > 25;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_having_where">Спробуйте самі</a>
</div>

___
# SQL EXISTS
Оператор `EXISTS` використовується для перевірки існування будь-якого запису в підзапиті.

Оператор `EXISTS` повертає TRUE, якщо підзапит повертає один або більше записів.
```sql
EXISTS Синтаксис
SELECT column_name(s)
FROM table_name
WHERE EXISTS
(SELECT column_name FROM table_name WHERE condition);
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Продукти» у прикладі бази даних Northwind:

| ProductID | ProductName | SupplierID | CategoryID | Unit | Price |
|-----------|-------------|------------|------------|------|-------|
| 1         | Chais       | 1          | 1          | 10 boxes x 20 bags | 18 |
| 2         | Chang       | 1          | 1          | 24 - 12 oz bottles | 19 |
| 3         | Aniseed Syrup | 1        | 2          | 12 - 550 ml bottles | 10 |
| 4         | Chef Anton's Cajun Seasoning | 2 | 2 | 48 - 6 oz jars | 22 |
| 5         | Chef Anton's Gumbo Mix | 2 | 2 | 36 boxes | 21.35 |

І вибірка з таблиці «Постачальники»:


| SupplierID | SupplierName | ContactName | Address | City | PostalCode | Country |
|------------|-----------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Exotic Liquid              | Charlotte Cooper | 49 Gilbert St.          | London       | EC1 4SD    | UK      |
| 2          | New Orleans Cajun Delights | Shelley Burke   | P.O. Box 78934          | New Orleans  | 70117      | USA     |
| 3          | Grandma Kelly's Homestead  | Regina Murphy   | 707 Oxford Rd.          | Ann Arbor    | 48104      | USA     |
| 4          | Tokyo Traders              | Yoshi Nagase    | 9-8 Sekimai Musashino-shi | Tokyo      | 100        | Japan   |

## SQL ІСНУЄ Приклади
Наступний оператор SQL повертає TRUE і містить список постачальників із ціною продукту менше 20:

### приклад
```sql
SELECT SupplierName
FROM Suppliers
WHERE EXISTS (SELECT ProductName FROM Products WHERE Products.SupplierID = Suppliers.supplierID AND Price < 20);
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_exists">Спробуйте самі</a>
</div>

Наступний оператор SQL повертає TRUE і містить список постачальників із ціною продукту, що дорівнює 22:

### приклад
```sql
SELECT SupplierName
FROM Suppliers
WHERE EXISTS (SELECT ProductName FROM Products WHERE Products.SupplierID = Suppliers.supplierID AND Price = 22);
```

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_exists2">Спробуйте самі</a>
</div>

___
# SQL ANY та ALL
Оператори `ANY`and `ALL`дозволяють виконувати порівняння між значеннями одного стовпця та діапазоном інших значень.

## Оператор SQL ANY
Оператор `ANY`:

+ у результаті повертає логічне значення
+ повертає TRUE, якщо БУДЬ-ЯКЕ зі значень підзапиту відповідає умові
  
`ANY` означає, що умова буде істинною, якщо операція буде істинною для будь-якого зі значень у діапазоні.

## БУДЬ-ЯКИЙ синтаксис
```sql
SELECT column_name(s)
FROM table_name
WHERE column_name operator ANY
  (SELECT column_name
  FROM table_name
  WHERE condition);
```

## Оператор SQL ALL
Оператор ALL:

+ у результаті повертає логічне значення
+ повертає TRUE, якщо ВСІ значення підзапиту відповідають умові
+ використовується з SELECTі WHEREоператорамиHAVING

`ALL` означає, що умова буде істинною, лише якщо операція буде істинною для всіх значень у діапазоні. 

## ALL Синтаксис з SELECT
```sql
SELECT ALL column_name(s)
FROM table_name
WHERE condition;
```
## ALL Синтаксис з WHERE або HAVING
```sql
SELECT column_name(s)
FROM table_name
WHERE column_name operator ALL
  (SELECT column_name
  FROM table_name
  WHERE condition);
```

## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Продукти» у прикладі бази даних Northwind:

| ProductID | ProductName | SupplierID | CategoryID | Unit | Price |
|-----------|-----------------------------|------------|------------|---------------------|-------|
| 1         | Chais                      | 1          | 1          | 10 boxes x 20 bags  | 18    |
| 2         | Chang                      | 1          | 1          | 24 - 12 oz bottles  | 19    |
| 3         | Aniseed Syrup              | 1          | 2          | 12 - 550 ml bottles | 10    |
| 4         | Chef Anton's Cajun Seasoning | 2        | 2          | 48 - 6 oz jars      | 22    |
| 5         | Chef Anton's Gumbo Mix     | 2          | 2          | 36 boxes            | 21.35 |
| 6         | Grandma's Boysenberry Spread | 3        | 2          | 12 - 8 oz jars      | 25    |
| 7         | Uncle Bob's Organic Dried Pears | 3      | 7          | 12 - 1 lb pkgs.     | 30    |
| 8         | Northwoods Cranberry Sauce | 3          | 2          | 12 - 12 oz jars     | 40    |
| 9         | Mishi Kobe Niku            | 4          | 6          | 18 - 500 g pkgs.    | 97    |

І вибір із таблиці "Деталі замовлення" :

| OrderDetailID | OrderID | ProductID | Quantity |
|---------------|---------|-----------|----------|
| 1             | 10248   | 11        | 12       |
| 2             | 10248   | 42        | 10       |
| 3             | 10248   | 72        | 5        |
| 4             | 10249   | 14        | 9        |
| 5             | 10249   | 51        | 40       |
| 6             | 10250   | 41        | 10       |
| 7             | 10250   | 51        | 35       |
| 8             | 10250   | 65        | 15       |
| 9             | 10251   | 22        | 6        |
| 10            | 10251   | 57        | 15       |

## Приклади SQL ANY
Наступний оператор SQL перераховує ProductName, якщо він знаходить БУДЬ-ЯКИЙ запис у таблиці OrderDetails із значенням Quantity, рівним 10 (це поверне значення TRUE, оскільки стовпець Quantity має деякі значення 10):

### приклад
```sql
SELECT ProductName
FROM Products
WHERE ProductID = ANY
  (SELECT ProductID
  FROM OrderDetails
  WHERE Quantity = 10);
```

<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_any">Спробуйте самі</a>
</div>

Наступний оператор SQL перераховує ProductName, якщо він знаходить БУДЬ-ЯКИЙ запис у таблиці OrderDetails із кількістю, більшою за 99 (це поверне TRUE, оскільки стовпець Quantity містить деякі значення, більші за 99):

### приклад
```sql
SELECT ProductName
FROM Products
WHERE ProductID = ANY
  (SELECT ProductID
  FROM OrderDetails
  WHERE Quantity > 99);
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_any2">Спробуйте самі</a>
</div>

Наступний оператор SQL перераховує ProductName, якщо він знаходить БУДЬ-ЯКИЙ запис у таблиці OrderDetails із кількістю, більшою за 1000 (це поверне значення FALSE, оскільки стовпець Quantity не містить значень, більших за 1000):

## приклад
```sql
SELECT ProductName
FROM Products
WHERE ProductID = ANY
  (SELECT ProductID
  FROM OrderDetails
  WHERE Quantity > 1000);
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_any3">Спробуйте самі</a>
</div>

Наступний оператор SQL перераховує ВСІ назви продуктів:

### приклад
```sql
SELECT ALL ProductName
FROM Products
WHERE TRUE;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all2">Спробуйте самі</a>
</div>

___
# SQL SELECT INTO
Оператор `SELECT INTO` копіює дані з однієї таблиці в нову таблицю.

## Синтаксис SELECT INTO
Скопіюйте всі стовпці в нову таблицю:
```sql
SELECT *
INTO newtable [IN externaldb]
FROM oldtable
WHERE condition;
```
Скопіюйте лише деякі стовпці в нову таблицю:
```sql
SELECT column1, column2, column3, ...
INTO newtable [IN externaldb]
FROM oldtable
WHERE condition;
```
Нова таблиця буде створена з назвами стовпців і типами, як визначено в старій таблиці. Ви можете створити нові назви стовпців за допомогою `AS` пропозиції.

## Приклади SQL SELECT INTO
Наступний оператор SQL створює резервну копію клієнтів:
```sql
SELECT * INTO CustomersBackup2017
FROM Customers;
```

Наступний оператор SQL використовує `IN` пункт для копіювання таблиці в нову таблицю в іншій базі даних:
```sql
SELECT * INTO CustomersBackup2017 IN 'Backup.mdb'
FROM Customers;
```

Наступний оператор SQL копіює лише кілька стовпців у нову таблицю:
```sql
SELECT CustomerName, ContactName INTO CustomersBackup2017
FROM Customers;
```
Наступний оператор SQL копіює лише німецьких клієнтів у нову таблицю:
```sql
SELECT * INTO CustomersGermany
FROM Customers
WHERE Country = 'Germany';
```

Наступний оператор SQL копіює дані з кількох таблиць у нову таблицю:
```sql
SELECT Customers.CustomerName, Orders.OrderID
INTO CustomersOrderBackup2017
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID;
```
Порада: `SELECT INTO` також можна використовувати для створення нової порожньої таблиці за допомогою іншої схеми. Просто додайте WHEREпункт, який змушує запит не повертати дані:
```sql
SELECT * INTO newtable
FROM oldtable
WHERE 1 = 0;
```

___
# SQL INSERT INTO SELECT
Оператор `INSERT INTO SELECT` копіює дані з однієї таблиці та вставляє їх в іншу таблицю.

Інструкція `INSERT INTO SELECT` вимагає, щоб типи даних у вихідній і цільовій таблицях збігалися.

#### Примітка. Існуючі записи в цільовій таблиці не впливають.

## Синтаксис INSERT INTO SELECT
Скопіюйте всі стовпці з однієї таблиці в іншу:
```sql
INSERT INTO table2
SELECT * FROM table1
WHERE condition;
```
Скопіюйте лише деякі стовпці з однієї таблиці в іншу:
```sql
INSERT INTO table2 (column1, column2, column3, ...)
SELECT column1, column2, column3, ...
FROM table1
WHERE condition;
```

## Демонстраційна база даних
У цьому підручнику ми будемо використовувати відомий приклад бази даних Northwind.

Нижче наведено вибір із таблиці «Клієнти»:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
|------------|-----------------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Obere Str. 57             | Berlin       | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mataderos 2312            | México D.F.  | 05023      | Mexico  |

І вибірка з таблиці «Постачальники»:

| SupplierID | SupplierName | ContactName | Address | City | Postal Code | Country |
|------------|-----------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Exotic Liquid              | Charlotte Cooper | 49 Gilbert St.          | Londona      | EC1 4SD    | UK      |
| 2          | New Orleans Cajun Delights | Shelley Burke   | P.O. Box 78934          | New Orleans  | 70117      | USA     |
| 3          | Grandma Kelly's Homestead  | Regina Murphy   | 707 Oxford Rd.          | Ann Arbor    | 48104      | USA     |

## Приклади SQL INSERT INTO SELECT
### приклад
Скопіюйте «Постачальники» в «Клієнти» (колонки, які не заповнені даними, будуть містити NULL):
```sql
INSERT INTO Customers (CustomerName, City, Country)
SELECT SupplierName, City, Country FROM Suppliers;
```

### приклад
Скопіюйте «Постачальники» в «Клієнти» (заповніть усі стовпці):
```sql
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
SELECT SupplierName, ContactName, Address, City, PostalCode, Country FROM Suppliers;
```

### приклад
Скопіюйте лише німецьких постачальників у «Клієнти»:
```sql
INSERT INTO Customers (CustomerName, City, Country)
SELECT SupplierName, City, Country FROM Suppliers
WHERE Country='Germany';
```
___
# SQL CASE
Вираз `CASE` проходить через умови та повертає значення, коли виконується перша умова (як оператор if-then-else). Отже, як тільки умова виконується, вона припинить читання та поверне результат. Якщо жодна умова не виконується, повертається значення в `ELSE` пропозиції.

Якщо частина відсутня `ELSE` і умови не виконуються, повертається NULL.

## Синтаксис CASE
```sql
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```

## Демонстраційна база даних
Нижче наведено вибір із таблиці «OrderDetails» у прикладі бази даних Northwind:

| OrderDetailID | OrderID | ProductID | Quantity |
|---------------|---------|-----------|----------|
| 1             | 10248   | 11        | 12       |
| 2             | 10248   | 42        | 10       |
| 3             | 10248   | 72        | 5        |
| 4             | 10249   | 14        | 9        |
| 5             | 10249   | 51        | 40       |

## Приклади SQL CASE
Наступний SQL перевіряє умови та повертає значення, коли виконується перша умова:

### приклад
```sql
SELECT OrderID, Quantity,
CASE
    WHEN Quantity > 30 THEN 'The quantity is greater than 30'
    WHEN Quantity = 30 THEN 'The quantity is 30'
    ELSE 'The quantity is under 30'
END AS QuantityText
FROM OrderDetails;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_case">Спробуйте самі</a>
</div>

Наступний SQL упорядкує клієнтів за містом. Однак, якщо місто дорівнює NULL, упорядкуйте за країною:
### приклад
```sql
SELECT CustomerName, City, Country
FROM Customers
ORDER BY
(CASE
    WHEN City IS NULL THEN Country
    ELSE City
END);
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_case2">Спробуйте самі</a>
</div>

___
# SQL NULL
## Функції SQL IFNULL(), ISNULL(), COALESCE() і NVL()
Подивіться на наступну таблицю «Продукти»:

| P_Id | ProductName | UnitPrice | UnitsInStock | UnitsOnOrder |
|------|-------------|-----------|--------------|--------------|
| 1    | Jarlsberg   | 10.45     | 16           | 15           |
| 2    | Mascarpone  | 32.56     | 23           |              |
| 3    | Gorgonzola  | 15.67     | 9            | 20           |

Припустімо, що стовпець "UnitsOnOrder" необов'язковий і може містити значення NULL.

Подивіться на наступний оператор SELECT:
```sql
SELECT ProductName, UnitPrice * (UnitsInStock + UnitsOnOrder)
FROM Products;
```
У прикладі вище, якщо будь-яке зі значень "UnitsOnOrder" дорівнює NULL, результат буде NULL.

## Рішення
### MySQL

Функція MySQL `IFNULL()` дозволяє повертати альтернативне значення, якщо вираз дорівнює NULL:
```sql
SELECT ProductName, UnitPrice * (UnitsInStock + IFNULL(UnitsOnOrder, 0))
FROM Products;
```
або ми можемо скористатися цією функцією: `COALESCE()`
```sql
SELECT ProductName, UnitPrice * (UnitsInStock + COALESCE(UnitsOnOrder, 0))
FROM Products;
```

### SQL Server

Функція SQL Server `ISNULL()` дозволяє повертати альтернативне значення, коли вираз має значення NULL:
```sql
SELECT ProductName, UnitPrice * (UnitsInStock + ISNULL(UnitsOnOrder, 0))
FROM Products;
```
або ми можемо скористатися `COALESCE()` цією функцією:
```sql
SELECT ProductName, UnitPrice * (UnitsInStock + COALESCE(UnitsOnOrder, 0))
FROM Products;
```
### MS Access

Функція MS Access `IsNull()` повертає TRUE (-1), якщо вираз має нульове значення, інакше FALSE (0):
```sql
SELECT ProductName, UnitPrice * (UnitsInStock + IIF(IsNull(UnitsOnOrder), 0, UnitsOnOrder))
FROM Products;
```

___
# Збережені процедури SQL
## Що таке збережена процедура?
Збережена процедура — це підготовлений код SQL, який можна зберегти, щоб код можна було використовувати знову і знову.

Отже, якщо у вас є SQL-запит, який ви пишете знову і знову, збережіть його як збережену процедуру, а потім просто викличте її для виконання.

Ви також можете передати параметри збереженій процедурі, щоб збережена процедура могла діяти на основі переданих значень параметра.

## Синтаксис збереженої процедури
```sql
CREATE PROCEDURE procedure_name
AS
sql_statement
GO;
```

### Виконати збережену процедуру
```sql
EXEC procedure_name;
```
## Демонстраційна база даних
Нижче наведено вибірку з таблиці «Клієнти» у прикладі бази даних Northwind:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
|------------|-----------------------------------|----------------|---------------------------|--------------|------------|---------|
| 1          | Alfreds Futterkiste               | Maria Anders   | Obere Str. 57             | Berlin       | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados| Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería           | Antonio Moreno | Mataderos 2312            | México D.F.  | 05023      | Mexico  |
| 4          | Around the Horn                   | Thomas Hardy   | 120 Hanover Sq.           | London       | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                | Christina Berglund | Berguvsvägen 8        | Luleå       | S-958 22   | Sweden  |

## Приклад збереженої процедури
Наступний оператор SQL створює збережену процедуру під назвою «SelectAllCustomers», яка вибирає всі записи з таблиці «Клієнти»:

### приклад
```sql
CREATE PROCEDURE SelectAllCustomers
AS
SELECT * FROM Customers
GO;
```

Виконайте наведену вище збережену процедуру таким чином:

### приклад
```sql
EXEC SelectAllCustomers;
```
## Збережена процедура з одним параметром
Наступний оператор SQL створює збережену процедуру, яка вибирає клієнтів із певного міста з таблиці «Клієнти»:

### приклад
```sql
CREATE PROCEDURE SelectAllCustomers @City nvarchar(30)
AS
SELECT * FROM Customers WHERE City = @City
GO;
```

Виконайте наведену вище збережену процедуру таким чином:

### приклад
```sql
EXEC SelectAllCustomers @City = 'London';
```
## Збережена процедура з кількома параметрами
Налаштувати кілька параметрів дуже просто. Просто перерахуйте кожен параметр і тип даних, розділивши їх комою, як показано нижче.

Наступний оператор SQL створює збережену процедуру, яка вибирає клієнтів із певного міста з певним поштовим індексом із таблиці «Клієнти»:

### приклад
```sql
CREATE PROCEDURE SelectAllCustomers @City nvarchar(30), @PostalCode nvarchar(10)
AS
SELECT * FROM Customers WHERE City = @City AND PostalCode = @PostalCode
GO;
```
Виконайте наведену вище збережену процедуру таким чином:

### приклад
```sql
EXEC SelectAllCustomers @City = 'London', @PostalCode = 'WA1 1DP';
```
___
# Коментарі SQL

Коментарі використовуються для пояснення розділів інструкцій SQL або для запобігання виконанню інструкцій SQL.

**Примітка.** Коментарі не підтримуються в базах даних Microsoft Access!

## Однорядкові коментарі
Однорядкові коментарі починаються з `--`.

Будь-який текст між `--` і кінцем рядка буде проігноровано (не буде виконано).

У наступному прикладі як пояснення використовується однорядковий коментар:

### приклад
```sql
-- Select all:
SELECT * FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_comment_single_1">Спробуйте самі</a>
</div>

У наступному прикладі використовується однорядковий коментар, щоб ігнорувати кінець рядка:

### приклад
```sql
SELECT * FROM Customers -- WHERE City='Berlin';
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_comment_single_2">Спробуйте самі</a>
</div>

У наступному прикладі використовується однорядковий коментар, щоб ігнорувати оператор:

### приклад
```sql
-- SELECT * FROM Customers;
SELECT * FROM Products;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_comment_single_3">Спробуйте самі</a>
</div>


Багаторядкові коментарі
Багаторядкові коментарі починаються з `/*і` закінчуються на `*/`.

Будь-який текст між /* і */ ігноруватиметься.

У наступному прикладі використовується багаторядковий коментар як пояснення:

### приклад
```sql
/*Select all the columns
of all the records
in the Customers table:*/
SELECT * FROM Customers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_comment_multi_1">Спробуйте самі</a>
</div>

У наступному прикладі використовується багаторядковий коментар, щоб ігнорувати багато тверджень:

### приклад
```sql
/*SELECT * FROM Customers;
SELECT * FROM Products;
SELECT * FROM Orders;
SELECT * FROM Categories;*/
SELECT * FROM Suppliers;
```
<div style="background-color:rgba(255, 165, 0, 0.2); width:120px; text-align:center; border-radius:12px">
    <a href="https://www.w3schools.com/sql/trymysql.asp?filename=trysql_comment_multi_2">Спробуйте самі</a>
</div>

Щоб проігнорувати лише частину оператора, також використовуйте коментар /* */.

У наступному прикладі використовується коментар, щоб ігнорувати частину рядка:

### приклад
```sql
SELECT CustomerName, /*City,*/ Country FROM Customers;
```

___
# Оператори SQL
## Арифметичні оператори SQL
| Operator | Description | Example |
|----------|-------------|---------|
| +        | Add         | 3 + 2 = 5 |
| -        | Subtract    | 5 - 2 = 3 |
| *        | Multiply    | 2 * 3 = 6 |
| /        | Divide      | 10 / 2 = 5 |
| %        | Modulo      | 10 % 3 = 1 |

## Побітові оператори SQL
| Operator | Description |
|----------|-------------|
| &        | Bitwise AND |
| \|       | Bitwise OR  |
| ^        | Bitwise exclusive OR |

## Оператори порівняння SQL

| Operator | Description |
|----------|-------------|
| =        | Equal to    |
| >        | Greater than|
| <        | Less than   |
| >=       | Greater than or equal to |
| <=       | Less than or equal to |
| <>       | Not equal to |

Складені оператори SQL:
| Operator | Description |
|----------|-------------|
| +=       | Add equals  |
| -=       | Subtract equals |
| *=       | Multiply equals |
| /=       | Divide equals |
| %=       | Modulo equals |
| &=       | Bitwise AND equals |
| ^-=      | Bitwise exclusive equals |
| \|*=     | Bitwise OR equals |

Логічні оператори SQL:

| Operator | Description |
|----------|-------------|
| ALL      | TRUE if all of the subquery values meet the condition |
| AND      | TRUE if all the conditions separated by AND is TRUE |
| ANY      | TRUE if any of the subquery values meet the condition |
| BETWEEN  | TRUE if the operand is within the range of comparisons |
| EXISTS   | TRUE if the subquery returns one or more records |
| IN       | TRUE if the operand is equal to one of a list of expressions |
| LIKE     | TRUE if the operand matches a pattern |
| NOT      | Displays a record if the condition(s) is NOT TRUE |
| OR       | TRUE if any of the conditions separated by OR is TRUE |
| SOME     | TRUE if any of the subquery values meet the condition |









