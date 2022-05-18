# MSSQL Extension Starter Pack 

Това е пакет с разширения за Visual Studioe Code, което представлява пакет от разширения, помагащи за разработката и администрацията на MS SQL Server.
Вече удобно може да управлявате и разработвате MS SQL Server бази данни чрез Visual Studio Code.

## Table of Contents
***
- [1. Характеристики](#характеристики) 
- [2. Изисквания](#изисквания)
- [3. Как да използвате](#как-да-използвате)
- [4. Проблеми](#проблеми)
- [5. Версии](#версии)
- [6. Лиценз](#лиценз)

## Характеристики
***  
Пакетът с разширения включва следните:

| # | Име на разширението              | Кратко описание | Линк към VS Code Marketplace                                                         |
|---|-----------------------------|:-----------------:|---------------------------------------------------------------------------------|
| 1 | **SQL Server (mssql)**          | Разработка на Microsoft SQL Server, Azure SQL Бази данни and SQL Data Warehouse everywhere                  | https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql              |
| 2 | **MSSQL Snippets**              | Полезни snippets за Microsoft SQL Server Snippets за писане на вашите заявки по-бързо.                  | https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-snippets |
| 3 | **MSSQL Scripts and Utilities** | MSSQL скриптове за администрация, дефиниране и управление на данните, за улеснение на разработката на бази данни. Автоматизирайте задачи. Изпълнявайте заявките си по-бързо.                  | https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-scripts  |

1. ## [SQL Server (mssql)](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql) е официалното разширение на Microsoft за урпавление на базите им данни. То помага със следните неща:
    - Връзка с MS SQL Server.
    - Преглед на обектите в удобен панел (`Server`, `Databases`, `Tables`, `Views`, `Procedures`, `Functions`, `etc.`) .
    - Писане и изпълнение на заявки.
2. ## [MSSQL Snippets](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-snippets) е разширение, което има много различни snippets за работа с MSSQL Server. Може да пишете кода си по-бързо само с въвеждането на няколко символа или фрази. Всички тези snippets са налични:
    - ### **Модифициране на данни**
        - `SELECT`, `SELECT WITH WHERE CLAUSE`, `SELECT WITH EXISTS/NOT EXISTS`, `SELECT WITH IN/NOT IN`, 
        - `CTEs`, `RECURSIVE CTEs`
        - `INSERT INTO`, `INSERT WITH SELECT`, `INSERT EXEC`, `SELECT INTO`
        - `UPDATE`, `UPDATE WITH JOIN`
        - `DELETE`, `DELETE TOP(N)`, `TRUNCATE`
        - `MERGING DATA`
        - `INSERT WITH OUTPUT`, `UPDATE WITH OUTPUT`, `DELETE WITH OUTPUT`, `MERGE WITH OUTPUT`
        - `UNION`, `INTERSECT`, `EXCEPT`
        - `OFFSET-FETCH`
        - Всички типове JOINS - `INNER JOIN`, `LEFT OUTER JOIN`, `RIGHT OUTER JOIN`, `FULL OUTER JOIN`, `CROSS JOIN`
        - `CROSS APPLY` и `OUTER APPLY`
        - `PIVOT` и `UNPIVOT` на данни
        - ##### **УСЛОВНА ЛОГИКА - IF ELSE**
            - `IF`, `IF-ELSE`, `IF EXISTS`, `IF NOT EXISTS`, `CASE`

    - ### **ДЕФИНИЦИЯ НА СТРУКТУРИ**
        - ### **ДЕКЛАРИРАНЕ НА ПРОМЕНЛИВИ И ТИПОВЕ ДАННИ**
            - DECLARE `INT`, `BIGINT`, `SMALLINT`, `TINYINT`, `MONEY`, `SMALLMONEY`, `DECIMAL`, `FLOAT`, `REAL`, `BIT`, `DATE`, `DATETIME`, `SMALLDATETIME`, `DATETIMEOFFSET`, `TIME`, `CHAR`, `VARCHAR`, `NVARCHAR`, `BINARY`, `VARBINARY`, `SQL_VARIANT`, `XML`, `UNIQUEIDENTIFIER`, `GEOGRAPHY`, `GEOMETRY`, `TABLE`
        - ### **CREATE**, **ALTER** и **DROP**
            - `TABLES`, `VIEWS`, `INLINE FUNCTIONS`, `SCALAR FUNCTIONS`, `MULTISTATEMENT TABLE-VALUED FUNCTIONS`, `PROCEDURES`, `CLUSTERED INDEXES`, `NON-CLUSTERED INDEXES`, `PRIMARY KEYS`, `FOREIGN KEYS`, `CONSTRAINTS`

    - ### **ВСИЧКИ MS SQL Server вградени ФУНКЦИИ**
        - ### **Преобразуване**
            - `CAST`, `TRY_CAST`, `CONVERT`, `TRY_CONVERT`, `PARSE`, `TRY_PARSE`
        - ### **Дата и час**
            - `DATEPART`, `DATENAME`, `DAY`, `MONTH`, `YEAR`, `DATEFROMPARTS`, `DATETIMEFROMPARTS`, `DATETIME2FROMPARTS`, `DATETIMEOFFSETFROMPARTS`, `SMALLDATETIMEFROMPARTS`, `TIMEFROMPARTS`, `DATEDIFF`, `DATEDIFF_BIG`, `DATEADD`, `EOMONTH`, `SWITCHOFFSET`, `TODATETIMEOFFSET`, `ISDATE`
        - ### **Данни**
            - `DATALENGTH`
        - ### **Стрингове**
            - `ASCII`, `CHAR`, `CHARINDEX`, `CONCAT`, `CONCAT_WS`, `DIFFERENCE`, `FORMAT`, `LEFT`, `LEN`, `LOWER`, `LTRIM`, `NCHAR`, `PATINDEX`, `QUOTENAME`, `REPLACE`, `REPLICATE`, `REVERSE`, `RIGHT`, `RTRIM`, `SOUNDEX`, `SPACE`, `STR`, `STRING_AGG`, `STRING_ESCAPE`, `STRING_SPLIT`, `STUFF`, `SUBSTRING`, `TRANSLATE`, `TRIM`, `UNICODE`, `UPPER`
        - ### **Условия**
            - `IIF`, `CHOOSE`
        - ### **Математически**
            - `ABS`, `ACOS`, `ASIN`, `ATAN`, `ATN2`, `CEILING`, `COS`, `COT`, `DEGREES`, `EXP`, `FLOOR`, `LOG`, `LOG10`, `POWER`, `RADIANS`, `RAND`, `ROUND`, `SIGN`, `SIN`, `SQRT`, `SQUARE`, `TAN`
        - ### **JSON**
            - `ISJSON`, `JSON_VALUE`, `JSON_QUERY`, `JSON_MODIFY`
        - ### **Агрегатни**
            - `APPROX_COUNT_DISTINCT`, `AVG`, `CHECKSUM_AGG`, `COUNT`, `COUNT_BIG`, `GROUPING`, `GROUPING_ID`, `MAX`, `MIN`, `STDEV`, `STDEVP`, `SUM`, `VAR`, `VARP`
    - ### **Други полезни скриптове**
        - `RANDOM NUMBER`, `BLOCK OF COMMENTS`, `LINE OF COMMENTS`, `GET CURRENT DATE`, `GET CURRENT DATETIME`, `GET UNIX TIMESTAMP`, `TRY-CATCH`, `INSERT DELAY`, `BEGIN TRANSACTION`, `EXECUTE DYNAMIC SQL`

3. ## [MSSQL Scripts and Utilities](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-scripts) е разширение, което има различни скриптове, които могат да бъдат изпълнявани директно, в зависимост от избрания обект. Разширението включва всички тези скриптове:
    - ## Ниво Сървър
        - Properties
        - Версия на сървъра
        - Системна информация
        - Освобождаване на кеша с плановете
        - [Помощни процедури](#помощни-процедури)
        - [Добавки](#utilities)
        - [SQL Server Monitoring](#sql-server-monitoring)
        - [Database Mail](#database-mail)
    - ## Ниво База данни
        - СЪЗДАВАНЕ на нова таблица
        - ДИЗАЙН на нова таблица
        - Освобождаване на кеша с плановете
        - Properties
        - Query Statistics
        - Конвертиране на Query в HTML таблица
        - Query sys.objects за избраната база данни
        - Търсене в базата данни
        - Задачи
            - BackUp/Restore на базата данни
            - Online/Offline
            - Информация за таблиците
            - Shrink Database
            - Shrink File
        - [Helper Procedures](#помощни-процедури)
        - [Utilities](#utilities)
        - [SQL Server Monitoring](#sql-server-monitoring)
    - ## Ниво таблици
        - СЪЗДАВАНЕ на нова таблица
        - ДИЗАЙН на нова таблица
        - Drop Table
        - Properties
        - Данни от избраната таблица като HTML таблица
        - Query Statistics
        - Script As
            - INSERT
            - UPDATE
            - DELETE
            - TRUNCATE
        - SELECT 
            - COUNT(*)
            - TOP N rows
        - Колони
            - ADD, ALTER, DROP column
            - SELECT column names
            - Column names info
        - [Помощни процедури](#помощни-процедури)
        - [Utilities](#utilities)
        - [SQL Server Monitoring](#sql-server-monitoring)
    - ## Ниво Views
        - DROP View
        - [Помощни процедури](#помощни-процедури)
        - [Utilities](#utilities)
        - [SQL Server Monitoring](#sql-server-monitoring)
    - ## Ниво процедури
        - DROP Procedure
        - [Помощни процедури](#помощни-процедури)
        - [Utilities](#utilities)
        - [SQL Server Monitoring](#sql-server-monitoring)
    - ## Ниво функции
        - DROP Function
        - [Помощни процедури](#помощни-процедури)
        - [Utilities](#utilities)
        - [SQL Server Monitoring](#sql-server-monitoring)
    - ## Помощни процедури
        - Database Physical Paths
        - Всички активни заявки
        - Образец за изпращане на e-mail
        - Информация за всички бази данни
        - Информация за всички типове данни
        - Object Dependencies
        - Информация за външни ключове
        - Информация за първични ключове
        - sp_help `Table`
        - Информация за сървъра
        - Статистики
        - Права върху таблицата
        - sp_who
        - sp_who2
        - Пълна информация за системата
        - Списък на папки и файлове
        - Името на сървъра в текущата активна връзка
    - ## Utilities
        - Всички статистики, създадени от потребителя
        - Среден размер на ред в Базата данни
        - Среден размер на ред в избрана таблица
        - Информация за фрагментиране във всички таблици
        - Списък с всички асемблита
        - Списък с обекти в базата данни и информация за използваното място от тях
        - Списък на базите данни и заеманото място от тях
        - Recompile all Programmable Objects
        - Refresh all Views in Database
        - Роли и права
        - Таблици БЕЗ първичен ключ
        - Таблици с Identity колони
        - Таблици с INSTEAD OF triggers
        - Таблици с повече от N колони
        - Таблици с повече от N индекси
        - Таблици с N тригери
        - Таблици с брой редове в тях
        - Таблици с XML колони
        - Таблици без clustered index
        - TOP 50 неизползвани индекси 
    - ## SQL Server Monitoring
        - Скриптове, които се изпълняват в момента
        - Активни сесии
        - Информация за всички бази данни
        - Статистики за всички обекти в базата данни
        - Средно време за Четене/Писане в базата данни
        - BackUp Check
        - Блокиращи сесии и заявки
        - Index Maintenance Scripts
        - Статистики за използването на индексите
        - IO Waits at Database Level
        - IO Waits at File Level
        - Последно изпълнени заявки
        - Wait Events
    - ## Performance Tuning
        - Статистики за всички бази данни
        - Използване на процесора от всички бази данни
        - TOP N CPU заявки за база данни
        - TOP N IO заявки за база данни
    - ## Database Mail
        - Всички
        - Изпратени
        - Event Log
        - Неизпратени
        - Образец за изпращане на e-mail
        
## Изисквания
*** 

- Трябва да имате `VS Code инсталиран`.
- Трябва да инсталирате този пакета с разширения.


## Как да използвате
***  

1. Инсталирайте разширението:  
    - от [Marketplace](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-extensions-starter-pack&ssr=false#overview).  
    ![Extension Search](Images/extension-marketplace.png) 
    - от VS Code
        1. Отворете VS Code.
        2. Изберете `Extensions` от левия панел или натиснете клавишна комбинация `Ctrl + Shift + X`.
        3. Напишете `mssql-extensions-starter-pack`. Разширение с името `MSSQL Extension Starter Pack` ще се покаже.   
        ![Extension Search](Images/extension-search.png)  
        4. Може да изберете разширението и да прочетете повече за него, ако желаете.  
        ![Extension Search](Images/extension-overview.png) 
        5. Натиснете бутона `Install` и сте готови.
        6. Чрез инсталиране на `MSSQL Extension Starter Pack` ВСИЧКИ тези разширения ще бъдат инсталирани: 
            - [SQL Server (mssql)](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql)
            - [MSSQL Snippets](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-snippets)
            - [MSSQL Scripts and Utilities](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-scripts)
2. Рестартиране на VS Code може да бъде нужно.  
3. След инсталацията сте готови да го използвате.
4. Първо трябва да настроите връзка към вашния MSSQL Server. Може да прочетете повече как това става в [Официалната документация на MSSQL Extension](https://github.com/microsoft/vscode-mssql/wiki/manage-connection-profiles)
5. Когато се свържете с вашия MSSQL Server object explorer view с вашите бази данни, таблици, view-та, и др. ще бъде заредено.
    - Десен бутон с мишката на сървър, таблица, процедура, view, фунцкия и ще се зареди контекстово меню с опции.
    - Изберете някоя команда и скриптът ще бъде зареден.
    - Има 2 възможности:
        - `Ако скриптът не изисква информация от потребителя` - ще бъдете попитани за валидна връзка и след избирането й скриптът ще бъде автоматично изпълнен.
        - `Ако скриптът изисква информация от потребителя` - В конкретните placeholders ще ви бъде показано какво трябва да попълните и след това може да изпълните вашият новопопълнен скрипт.
6. ВСИЧКИ скриптове ДИНАМИЧНО се попълват с информацията за конкретния сървър, таблица, view, процедура, в зависимост от това какво сте избрали. 
7. За да използвате snippets отворете `.sql` файл и започнете да пишете някои от prefix-ите и наличните опции ще бъдат заредени в контекстово меню. Може да изберете някой от тях или да напишете конкретния prefix и да изберете бутон TAB - фрагментът ще бъде попълнен. 
    - Всички налични фрагменти могат да бъдат видени в [MSSQL Snippets Документацията](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-snippets#all-available-snippets-and-their-prefixes)


## Проблеми

За в момента няма налични проблеми.

## Версии

### 0.2.0

Обновяване на документацията

### 0.1.0

Първи release на разширението
    
## Лиценз

[MIT](LICENSE.txt)

**Приятно използване!**,  
**[Маг. Инж. Р. Батинов](https://radoslav-batinov.bss.design/)**

