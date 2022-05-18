# MS SQL Server Scripts and Utilities

Това е разширение за VS Code, което има доста полезни скриптове, които са полезни за по-бързо извличане на информация, администриране на SQL Server, изпълнение на запазени заявки и още много.

Единственото, което трябва да направите е да изберете десен бутон на секция Сървър, Таблица, View, Процедура или друг обект от панела Object Explorer и всички налични команди и скриптове ще бъдат заредени в контекстното меню. Изберете този, който желаете и той ще бъде директно изпълнен или зареден като текст за редактиране.

Това разширение е полезно за всеки, който разработва и администрира MS SQL Server бази данни и пише заявки, процедури, функции, създава таблици и всички останали SQL команди.

- Чрез инсталирането на  `MSSQL Scripts and Utilities`, разширението [SQL Server (mssql)](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql) ще бъде инсталирано автоматично.

![Демо на разширението](/images/demo.gif)

## Съдържание
***
- [1. Характеристики](#характеристики) 
- [2. Изисквания](#изисквания)
- [3. Как да използваме](#как-да-използваме)
- [4. Галерия](#галерия)
- [5. Проблеми](#проблеми)
- [6. Версии](#версии)
- [7. Лиценз](#лиценз)


## Характеристики
***  
Разширението има всички тези скриптове, които са включени в различните секции от Object Explorer панела.

Например, ако изберете десен бутон на мишката от секция `server`, след това `контекстово` меню със специфични за сървъра скриптове ще бъде отворено. Ако изберете десен бутон на секция `Базата данни`, то специфични скриптове за базите данни ще бъдат заредени и т.н.

Списък на всички налични скриптове:

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

- Трабва да имате `инсталиран VS Code`.
- Това разширение работи с официалното MS SQL Server разширение -> [SQL Server (mssql)](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).
- Чрез инсталирането на  `MSSQL Scripts and Utilities`, разширението `SQL Server (mssql)` ще бъде инсталирано автоматично.
- В случай, че имате вече инсталирано разширението `SQL Server (mssql)`, то само `MSSQL Scripts and Utilities` ще се инсталира.

## Как да използваме
***  

1. Инсталирайте разширението: 
    - от [Marketplace](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-scripts&ssr=false#overview).  
    ![Extension Search](/extension-marketplace.png) 
    - от VS Code
        1. Отворете VS Code.
        2. Изберете `Extensions` от левия панел или натиснете клавишна комбинация `Ctrl + Shift + X`.
        3. Напишете `mssql-scripts`. Разширение с името `MSSQL Scripts` ще се покаже.   
        ![Extension Search](/extension-search.png)  
        4. Може да изберете разширението и да прочетете повече за него, ако желаете.  
        ![Extension Search](/extension-overview.png) 
        5. Натиснете бутона `Install` и сте готови.

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

## Галерия 

![Demo of Columns Scripts](/Gallery/Columns.png)
***
![Demo of Database Mails Scripts](/Gallery/Database%20Mail.png)
***
![Demo of Database Scripts](/Gallery/Database.png)
***
![Demo of Design New Table Feature](/Gallery/Design%20new%20table.png)
***
![Demo of Functions Scripts](/Gallery/Functions.png)
***
![Demo of Helper Procedures Scripts](/Gallery/Helper%20Procedures.png)
***
![Demo of Monitoring Scripts](/Gallery/Monitoring.png)
***
![Demo of Performance Tuning Scripts](/Gallery/Performance%20Tuning.png)
***
![Demo of Script As Scripts](/Gallery/ScriptAs.png)
***
![Demo of Select Scripts](/Gallery/Select.png)
***
![Demo of Server Scripts](/Gallery/Server.png)
***
![Demo of Stored Procedures Scripts](/Gallery/Stored%20Procedures.png)
***
![Demo of Sys.Objects Scripts](/Gallery/Sys.objects.png)
***
![Demo of Table Scripts](/Gallery/Table.png)
***
![Demo of Tasks Scripts](/Gallery/Tasks.png)
***
![Demo of Utility Scripts](/Gallery/Utility.png)
***
![Demo of Views Scripts](/Gallery/Views.png)

## Проблеми

За в момента няма налични проблеми

## Версии

### 0.0.1

Първи release на разширението
    
## Лиценз

[MIT](LICENSE.txt)

**Наслаждавайте се!**,  
**[M. Eng. R. Batinov](https://radoslav-batinov.bss.design/)**
