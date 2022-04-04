# MS SQL Server Scripts and Utilities

This is a VS Code extension that has a lot of useful scripts that are helpful for faster retrieval of information, administering SQL Server, executing saved queries, and much more.

You just need to right click on some Server, Table, View, Procedure or another object in Object Explorer and all script commands will be loaded. Choose your desired script and it will be scripted and executed.

It can be useful for anyone who develops and administrates MS SQL Server databases and writes queries, procedures, functions, creates tables and many other SQL commands.

By installing `MSSQL Scripts and Utilities` the [SQL Server (mssql)](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql) extension will be installed automatically.

`SQL Server (mssql)` extension helps you connect to your MS SQL Server and gives you another tools and options to configure, develop and execute queries.

![Demo of Extension](/demo.gif)

## Table of Contents
***
- [1. Features](#features) 
- [2. Requirements](#requirements)
- [3. How to use](#how-to-use)
- [4. Gallery](#gallery)
- [5. Known Issues](#known-issues)
- [6. Release Notes](#release-notes)
- [7. License](#license)


## Features
***  
The Extension has all these scrips included in different levels in object explorer view.  

For exmaple if you right-click on your `server` then `context` menu with specified options in **Server Level** will show, if you right-click on `your database` then `context` menu with specified options in **Database Level** will show, etc.

List of all available scripts:

- ## Server Level
    - Properties
    - Server Version
    - System Info
    - Free cache plan
    - [Helper Procedures](#helper-procedures)
    - [Utilities](#utilities)
    - [SQL Server Monitoring](#sql-server-monitoring)
    - [Database Mail](#database-mail)
- ## Database Level
    - CREATE new Table
    - DESIGN new Table
    - Free cache plan
    - Properties
    - Query Statistics
    - Query to HTML Table
    - Query sys.objects for the selected Database
    - Search in selected Database
    - Tasks
        - BackUp/Restore Database
        - Online/Offline
        - Select tables info
        - Shrink Database
        - Shrink File
    - [Helper Procedures](#helper-procedures)
    - [Utilities](#utilities)
    - [SQL Server Monitoring](#sql-server-monitoring)
- ## Tables Level
    - CREATE new Table
    - DESIGN new Table
    - Drop Table
    - Properties
    - Table Result to HTML Table
    - Query Statistics
    - Script As
        - INSERT
        - UPDATE
        - DELETE
        - TRUNCATE
    - SELECT 
        - COUNT(*)
        - TOP N rows
    - Columns
        - ADD, ALTER, DROP column
        - SELECT column names
        - Column names info
    - [Helper Procedures](#helper-procedures)
    - [Utilities](#utilities)
    - [SQL Server Monitoring](#sql-server-monitoring)
- ## Views Level
    - DROP View
    - [Helper Procedures](#helper-procedures)
    - [Utilities](#utilities)
    - [SQL Server Monitoring](#sql-server-monitoring)
- ## Stored Procedures Level
    - DROP Procedure
    - [Helper Procedures](#helper-procedures)
    - [Utilities](#utilities)
    - [SQL Server Monitoring](#sql-server-monitoring)
- ## Functions Level
    - DROP Function
    - [Helper Procedures](#helper-procedures)
    - [Utilities](#utilities)
    - [SQL Server Monitoring](#sql-server-monitoring)
- ## Helper Procedures
    - Database Physical Paths
    - All Active Queries
    - Template for sending e-mail
    - All Databases Info
    - All Data Types Info
    - Object Dependencies
    - Foreign Key Info
    - Primary Key Info
    - sp_help `Table`
    - Server Info
    - Statistics
    - Table Permissions
    - sp_who
    - sp_who2
    - System Full Info
    - List file and folders
    - Current Server Name
- ## Utilities
    - All User-Created Statistics
    - Average Size of Rows in all Database Tables
    - Average Size of Rows in SELECTED Tables
    - Fragmentation Info in All Tables
    - List All Assemblies in Database
    - List Database Object with Space Info
    - List Database with Size Info
    - Recompile all Programmable Objects
    - Refresh all Views in Database
    - Server Roles and Permissions in Database
    - Tables that don't have Primary Key
    - Tables with Identity Columns
    - Tables with INSTEAD OF triggers
    - Tables with more than N Columns
    - Tables with more than N Indexes
    - Tables with N Triggers
    - Tables with number of rows
    - Tables with XML Columns
    - Tables without clustered index
    - TOP 50 unused indexes 
- ## SQL Server Monitoring
    - Active Running Queries
    - Currently Active Sessions
    - All Databases Information
    - All Objects in Database Statistics
    - Average Read/Write Time per Database
    - BackUp Check
    - Blocking Sessions and Queries
    - Index Maintenance Scripts
    - Index Usage Statistics
    - IO Waits at Database Level
    - IO Waits at File Level
    - Last-run Queries
    - Wait Events
- ## Performance Tuning
    - All Database Statistics
    - All Database CPU Resource Usage
    - TOP N CPU Queries in Database
    - TOP N IO Queries in Database
- ## Database Mail
    - All Items
    - Sent Items
    - Event Log
    - Failed Items
    - Template for sending HTML E-mail
    
## Requirements
*** 

- You need to have `VS Code Installed`.
- This extension works with the official MS SQL Server extension -> [SQL Server (mssql)](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).
- By installing `MSSQL Scripts and Utilities` the `SQL Server (mssql)` extension will be installed automatically.
- If you have `SQL Server (mssql)` installed then only `MSSQL Scripts and Utilities` will be installed.


## How to use
***  

1. Install the extension: 
    - from [Marketplace](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-scripts&ssr=false#overview).  
    ![Extension Search](/extension-marketplace.png) 
    - from VS Code
        1. Open VS Code.
        2. Select `Extensions` from left panel or press `Ctrl + Shift + X`.
        3. Type in `mssql-scripts`. The extension with name `MSSQL Scripts` will show.   
        ![Extension Search](/extension-search.png)  
        4. You can select the extension and read the overview features if you want.  
        ![Extension Search](/extension-overview.png) 
        5. Pres `Install` button and you are ready.
        6. By installing `MSSQL Scripts and Utilities` the [SQL Server (mssql)](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql) extension will be installed automatically.
2. Restart of VS Code may be needed.  
3. After installation you are ready to use it.
4. First you need to configure your MSSQL Connection. You can read more about how in the [MSSQL Extension Documentation](https://github.com/microsoft/vscode-mssql/wiki/manage-connection-profiles)
5. When you connect to your MSSQL Server object explorer view with your databases information, tables, views, etc. will be shown.
    - Right-click on your server, table, view, procedures, functions and all of the context menu commands will show.
    - Just click on your selected command and a script will be loaded.
    - There are 2 options for executing:
        - `If script does not need any user information to write down` - it will ask for a valid connection and after selecting one it will be directly executed.
        - `If script does need any user information to write down` - placeholders will show what you need to write down and then you can just execute the script.
6. Note that all objects are dynamically filled in the script based on your object click. So there is no need to type object information when executing the script. 

## Gallery 

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

## Known Issues

Currently there are no known issues.

## Release Notes

### 0.3.0

Documentation update 

### 0.2.0

First release of extension
    
## License

[MIT](LICENSE.txt)

**Enjoy!**,  
**[M. Eng. R. Batinov](https://radoslav-batinov.bss.design/)**
