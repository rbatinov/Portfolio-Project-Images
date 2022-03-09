# MS SQL Server Snippets

Това е разширение за VS Code, което съдържа много на брой удобни фрагменти на езикът T-SQL, специфичен за Microsoft SQL Server. 

Подходящо е за разработчици, програмисти, администратори на бази данни, които искат да подобрят продуктивността си и да създават своите заявки по-бързо.

С това разширение ще пишете лесно вашите процедури, фунцкии, view-та, ще добавяте нови таблици, индекси и др.

![Демо на разширението](/demo.gif)

## Съдържание
***
- [1. Характеристики](#характеристики) 
- [2. Изисквания](#изисквания)
- [3. Как да използвате](#как-да-използвате)
- [4. Списък с налични фрагменти и техните префикси](#списък-с-налични-фрагменти-и-техните-префикси)
    - [Модифициране на информация](#модифициране-на-информация)
    - [MS SQL Server вградени функции](#ms-sql-server-вградени-функции)
    - [Условна логика](#условна-логика)
    - [Деклариране на променливи](#деклариране-на-променливи)
    - [Дефиниране на структури](#дефиниране-на-структури)
    - [Полезни скриптове](#полезни-скриптове)
    - [Създаване на процедури, функции, view-та](#създаване-на-процедури-функции-view)
- [5. Проблеми](#проблеми)
- [6. Версии](#версии)
- [7. Лиценз](#лиценз)


## Характеристики
***  

- ### Фрагменти за:
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


## Изисквания
*** 

- Всичко, от което се нуждаете, е да имате инсталиран VS Code, и разбира се това разширение.

## Как да използвате
***  

1. Инсталиране на приложението:
    - от [Marketplace](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-snippets&ssr=false#overview).  
    ![Как изглежда разширението в Marketplace](/extension-marketplace.png) 
    - от VS Code
        1. Отворете VS Code.
        2. Изберете `Extensions` от левия панел или натиснете клавишна комбинация `Ctrl + Shift + X`.
        3. Напишете `mssql-snippets`. Разширение с име `MSSQL Snippets` ще се появи.   
        ![Разширението в търсачката на VS Code](/extension-search.png)  
        4. Може да изберете разширението и да прочетете подробна информация за него.
        ![Как изглежда разширението във VS Code](/extension-overview.png) 
        5. Изберете `Install` и разширението ще се инсталира.

2. Може да се наложи рестартиране на VS Code.  
3. След като го инсталирате, ще може да го използвате в файлове `.sql`, `csharp`, `java`, `php`, `python`, `ruby`, `go`.
4. Започнете да пишете някой от префиксите, посочени `долу` и ще се появи popup с информация за фрагментите. Натиснете `TAB` , за да въведете фрагмента.

## Списък с налични фрагменти и техните префикси
***  

## ***Модифициране на информация***
***  

> ## SELECT statement
>  **Prefix:** sel
```sql
 /*Започнете да пишете sel и натиснете Tab, за да въведете фрагмента*/ 
 SELECT * 
FROM tableName ;
 
```  
> ## SELECT statement 
>  **Prefix:** selc
```sql
 /*Започнете да пишете selc и натиснете Tab, за да въведете фрагмента*/ 
 

BLOCK_COMMENT_START Snippet Generated Select with current selected text BLOCK_COMMENT_END
SELECT * 
FROM TM_SELECTED_TEXT:1 ; 0
BLOCK_COMMENT_START End of the Snippet Generated Select BLOCK_COMMENT_END


 
```  
> ## SELECT statement FROM CLIBOARD. You can copy some tableName and then type some of the prefixes and press Tab and select sattement with the copied table will be inserted.
>  **Prefix:** selcopied ИЛИ selclip ИЛИ selclipboard  
```sql
 /*Започнете да пишете selcopied ИЛИ selclip ИЛИ selclipboard   и натиснете Tab, за да въведете фрагмента*/ 
 

SELECT * 
FROM CLIPBOARD:1 ;


 
```  
> ## SELECT statement with WHERE clause
>  **Prefix:** selw
```sql
 /*Започнете да пишете selw и натиснете Tab, за да въведете фрагмента*/ 
 SELECT * 
FROM tableName
WHERE whereClause ;
 
```  
> ## SELECT statement with WHERE clause with IN (...)
>  **Prefix:** selwin
```sql
 /*Започнете да пишете selwin и натиснете Tab, за да въведете фрагмента*/ 
 SELECT * 
FROM tableName as ot
WHERE ot.colName IN (
	 SELECT it.colName
	 FROM innerTableName as it
	 WHERE it.whereClause
);
 
```  
> ## SELECT statement with WHERE clause with NOT IN(...)
>  **Prefix:** selwnotin
```sql
 /*Започнете да пишете selwnotin и натиснете Tab, за да въведете фрагмента*/ 
 SELECT * 
FROM tableName as ot
WHERE ot.colName NOT IN (
	 SELECT it.colName
	 FROM innerTableName as it
	 WHERE it.whereClause
);
 
```  
> ## SELECT statement with WHERE clause with EXISTS(...)
>  **Prefix:** selwexists ИЛИ selwex  
```sql
 /*Започнете да пишете selwexists ИЛИ selwex   и натиснете Tab, за да въведете фрагмента*/ 
 SELECT * 
FROM tableName as ot
WHERE ot.colName EXISTS (
	 SELECT it.colName
	 FROM innerTableName as it
	 WHERE it.innerColumnName = ot.outerColumnName
);
 
```  
> ## SELECT statement with WHERE clause with EXISTS(...)
>  **Prefix:** selwnexists ИЛИ selwnex  
```sql
 /*Започнете да пишете selwnexists ИЛИ selwnex   и натиснете Tab, за да въведете фрагмента*/ 
 SELECT * 
FROM tableName as ot
WHERE ot.colName NOT EXISTS (
	 SELECT it.colName
	 FROM innerTableName as it
	 WHERE it.innerColumnName = ot.outerColumnName
);
 
```  
> ## Creates common table expression
>  **Prefix:** cte
```sql
 /*Започнете да пишете cte и натиснете Tab, за да въведете фрагмента*/ 
 ;WITH cteName (col1 col2 col3)  
AS  
-- Define the CTE query.  
(  
	SELECT col1 col2 col3
	FROM tablename
	WHERE whereClause ;
)  
-- Define the outer query referencing the CTE name.  
SELECT col1 col2 col3
FROM cteName  
ORDER BY col1
 
```  
> ## Creates recursive common table expression
>  **Prefix:** rcte
```sql
 /*Започнете да пишете rcte и натиснете Tab, за да въведете фрагмента*/ 
 ;WITH
cteName(col1 col2 col3 1recursionLevel)
AS
(
	SELECT col1 col2 col3, 1 as 1recursionLevel
	FROM tableName
	WHERE ancorColumn IS NULL

	UNION ALL

	SELECT e.col4, e.col5, e.1col6, r.1recursionLevel + 1
	FROM tableName e
		INNER JOIN cteName r
		ON e.col4 = r.col1
)
SELECT col1 col1 col1
FROM cteName
ORDER BY 1recursionLevel
 
```  
> ## INSERT values into table
>  **Prefix:** ins ИЛИ insert  
```sql
 /*Започнете да пишете ins ИЛИ insert   и натиснете Tab, за да въведете фрагмента*/ 
 INSERT INTO TableName (Column)
VALUES(ColumnValue) ;
 
```  
> ## INSERT values into table (from CLIPBOARD)
>  **Prefix:** inscopied ИЛИ insertcopied ИЛИ insclip ИЛИ insclipboard ИЛИ icopied ИЛИ iclip ИЛИ iclipboard  
```sql
 /*Започнете да пишете inscopied ИЛИ insertcopied ИЛИ insclip ИЛИ insclipboard ИЛИ icopied ИЛИ iclip ИЛИ iclipboard   и натиснете Tab, за да въведете фрагмента*/ 
 INSERT INTO CLIPBOARD:1 (Column)
VALUES(ColumnValue) ;
 
```  
> ## INSERT values into table with SELECT FROM TABLE
>  **Prefix:** inss ИЛИ inssel  
```sql
 /*Започнете да пишете inss ИЛИ inssel   и натиснете Tab, за да въведете фрагмента*/ 
 INSERT INTO TableName (Column)
SELECT Column
FROM tableName ;
 
```  
> ## INSERT values into table with EXEC procedure
>  **Prefix:** inse ИЛИ insexec  
```sql
 /*Започнете да пишете inse ИЛИ insexec   и натиснете Tab, за да въведете фрагмента*/ 
 INSERT INTO TableName (Column)
EXEC procedureName
	@p_parameterName = parameterValue ;
 
```  
> ## SELECT values INTO table
>  **Prefix:** selinto
```sql
 /*Започнете да пишете selinto и натиснете Tab, за да въведете фрагмента*/ 
 SELECT col1 col2
INTO tableNameToInsert
FROM tableFromGetData;
 
```  
> ## UPDATE rows from table
>  **Prefix:** upd ИЛИ update  
```sql
 /*Започнете да пишете upd ИЛИ update   и натиснете Tab, за да въведете фрагмента*/ 
 UPDATE TableName 
SET ColumnName = ColumnValue
WHERE WhereClause ;
 
```  
> ## UPDATE rows from table (from CLIPBOARD)
>  **Prefix:** updcopied ИЛИ updatecopied ИЛИ updclip ИЛИ updclipboard ИЛИ ucopied ИЛИ uclip ИЛИ iclipboard  
```sql
 /*Започнете да пишете updcopied ИЛИ updatecopied ИЛИ updclip ИЛИ updclipboard ИЛИ ucopied ИЛИ uclip ИЛИ iclipboard   и натиснете Tab, за да въведете фрагмента*/ 
 UPDATE CLIPBOARD:1 
SET ColumnValue = ColumnValue ;
WHERE WhereClause ;
 
```  
> ## UPDATE rows from table with JOIN
>  **Prefix:** updj ИЛИ updatej  
```sql
 /*Започнете да пишете updj ИЛИ updatej   и натиснете Tab, за да въведете фрагмента*/ 
 UPDATE t
SET t.columnName = jt.columnName
FROM tableToUpdate AS t 
	JOIN joinedTable AS jt 
		ON t.columnName = jt.columnName
;  
 
```  
> ## DELETE rows from table
>  **Prefix:** del ИЛИ delete  
```sql
 /*Започнете да пишете del ИЛИ delete   и натиснете Tab, за да въведете фрагмента*/ 
 DELETE FROM tableName
WHERE whereClause ;
 
```  
> ## DELETE rows from table
>  **Prefix:** delcopied ИЛИ deletecopied ИЛИ delclip ИЛИ deleteclip ИЛИ dclip ИЛИ dcopied  
```sql
 /*Започнете да пишете delcopied ИЛИ deletecopied ИЛИ delclip ИЛИ deleteclip ИЛИ dclip ИЛИ dcopied   и натиснете Tab, за да въведете фрагмента*/ 
 DELETE FROM CLIPBOARD:1
WHERE whereClause ;
 
```  
> ## DELETE TOP(n) rows from table
>  **Prefix:** delt ИЛИ deletet  
```sql
 /*Започнете да пишете delt ИЛИ deletet   и натиснете Tab, за да въведете фрагмента*/ 
 DELETE TOP(numberRowsToDelete) FROM tableName
WHERE whereClause ;
 
```  
> ## TRUNCATE table
>  **Prefix:** trunc
```sql
 /*Започнете да пишете trunc и натиснете Tab, за да въведете фрагмента*/ 
 TRUNCATE TABLE tableName ; 
 
```  
> ## MERGE data
>  **Prefix:** merge
```sql
 /*Започнете да пишете merge и натиснете Tab, за да въведете фрагмента*/ 
 MERGE INTO targetTable AS TGT
USING sourceTable as SRC
	ON SRC.col = TGT.col
WHEN MATCHED -- two clauses allowed:
	THEN 5|UPDATE SET TGT.col = SRC.col,DELETE| -- one with UPDATE one with DELETE
WHEN NOT MATCHET  -- one clause allowed
	THEN INSERT VALUES(val1 valN)-- if indicated, action must be INSERT
WHEN NOT MATCHED BY SOURCE -- two clauses allowed:
THEN 8|UPDATE SET TGT.col = SRC.col,DELETE|; -- one with UPDATE one with DELETE
 
```  
> ## Filters query with OFFSET-FETCH
>  **Prefix:** offset
```sql
 /*Започнете да пишете offset и натиснете Tab, за да въведете фрагмента*/ 
 SELECT colName
FROM tableName
ORDER BY colName
OFFSET numRowsOffset ROWS FETCH FIRST numRowsToFetch ROWS ONLY;
 
```  
> ## UNIONS table results
>  **Prefix:** uni
```sql
 /*Започнете да пишете uni и натиснете Tab, за да въведете фрагмента*/ 
 SELECT colName as colName
FROM firstTableName

UNION 

SELECT colName as colName
FROM N-thTableName;
 
```  
> ## UNIONS ALL table results
>  **Prefix:** uniall
```sql
 /*Започнете да пишете uniall и натиснете Tab, за да въведете фрагмента*/ 
 SELECT colName as colName
FROM firstTableName

UNION ALL

SELECT colName as colName
FROM N-thTableName;
 
```  
> ## INTERSECTS table results
>  **Prefix:** intersect
```sql
 /*Започнете да пишете intersect и натиснете Tab, за да въведете фрагмента*/ 
 SELECT colName as colName
FROM firstTableName

INTERSECT

SELECT colName as colName
FROM N-thTableName;
 
```  
> ## EXCEPTS table results
>  **Prefix:** except
```sql
 /*Започнете да пишете except и натиснете Tab, за да въведете фрагмента*/ 
 SELECT colName as colName
FROM firstTableName

EXCEPT

SELECT colName as colName
FROM N-thTableName;
 
```  
> ## CROSS JOIN tables
>  **Prefix:** cjoin
```sql
 /*Започнете да пишете cjoin и натиснете Tab, за да въведете фрагмента*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	CROSS JOIN N-thTableName as N-thTableAlias;
 
```  
> ## INNER JOIN tables
>  **Prefix:** ijoin
```sql
 /*Започнете да пишете ijoin и натиснете Tab, за да въведете фрагмента*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	INNER JOIN N-thTableName as N-thTableAlias ON firstTableAlias.colName = firstTableAlias.colName;
 
```  
> ## signle INNER JOIN line (without SELECT FROM statement)
>  **Prefix:** ij
```sql
 /*Започнете да пишете ij и натиснете Tab, за да въведете фрагмента*/ 
 	INNER JOIN N-thTableName as N-thTableAlias ON N-thTableAlias.colName = firstTableAlias.colName
 
```  
> ## LEFT OUTER JOIN tables
>  **Prefix:** ljoin
```sql
 /*Започнете да пишете ljoin и натиснете Tab, за да въведете фрагмента*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	LEFT OUTER JOIN N-thTableName as N-thTableAlias ON firstTableAlias.colName = firstTableAlias.colName;
 
```  
> ## signle LEFT OUTER JOIN line (without SELECT FROM statement)
>  **Prefix:** lj
```sql
 /*Започнете да пишете lj и натиснете Tab, за да въведете фрагмента*/ 
 	LEFT OUTER JOIN N-thTableName as N-thTableAlias ON N-thTableAlias.colName = firstTableAlias.colName
 
```  
> ## RIGHT OUTER JOIN tables
>  **Prefix:** rjoin
```sql
 /*Започнете да пишете rjoin и натиснете Tab, за да въведете фрагмента*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	RIGHT OUTER JOIN N-thTableName as N-thTableAlias ON firstTableAlias.colName = firstTableAlias.colName;
 
```  
> ## signle RIGHT OUTER JOIN line (without SELECT FROM statement)
>  **Prefix:** rj
```sql
 /*Започнете да пишете rj и натиснете Tab, за да въведете фрагмента*/ 
 	RIGHT OUTER JOIN N-thTableName as N-thTableAlias ON N-thTableAlias.colName = firstTableAlias.colName
 
```  
> ## FULL OUTER JOIN tables
>  **Prefix:** fjoin
```sql
 /*Започнете да пишете fjoin и натиснете Tab, за да въведете фрагмента*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	FULL OUTER JOIN N-thTableName as N-thTableAlias ON firstTableAlias.colName = firstTableAlias.colName;
 
```  
> ## signle FULL OUTER JOIN line (without SELECT FROM statement)
>  **Prefix:** fj
```sql
 /*Започнете да пишете fj и натиснете Tab, за да въведете фрагмента*/ 
 	FULL OUTER JOIN N-thTableName as N-thTableAlias ON N-thTableAlias.colName = firstTableAlias.colName
 
```  
> ## INSERT into Table with OUTPUT
>  **Prefix:** io ИЛИ insertoutput ИЛИ inso ИЛИ insoutput  
```sql
 /*Започнете да пишете io ИЛИ insertoutput ИЛИ inso ИЛИ insoutput   и натиснете Tab, за да въведете фрагмента*/ 
 INSERT INTO tableName(col1 col2 col3)
OUTPUT
	inserted.col1, inserted.col2, inserted.col3
SELECT col1 col2 col3
FROM tableName
WHERE WhereClause;
 
```  
> ## UPDATE Table with OUTPUT
>  **Prefix:** uo ИЛИ updateoutput ИЛИ updo ИЛИ updoutput  
```sql
 /*Започнете да пишете uo ИЛИ updateoutput ИЛИ updo ИЛИ updoutput   и натиснете Tab, за да въведете фрагмента*/ 
 UPDATE tableName
	SET colName = value
OUTPUT
	inserted.colName as new_value,
	deleted.colName as old_value
WHERE WhereClause;
 
```  
> ## UPDATE Table with OUTPUT
>  **Prefix:** do ИЛИ deleteoutput ИЛИ delo ИЛИ deloutput  
```sql
 /*Започнете да пишете do ИЛИ deleteoutput ИЛИ delo ИЛИ deloutput   и натиснете Tab, за да въведете фрагмента*/ 
 DELETE FROM tableName
OUTPUT
	deleted.colName as deleted_value
WHERE WhereClause;
 
```  
> ## MERGE data with OUTPUT
>  **Prefix:** mergeoutput ИЛИ mo  
```sql
 /*Започнете да пишете mergeoutput ИЛИ mo   и натиснете Tab, за да въведете фрагмента*/ 
 MERGE INTO targetTable AS TGT
USING sourceTable as SRC
	ON SRC.col = TGT.col
WHEN MATCHED -- two clauses allowed:
	THEN 5|UPDATE SET TGT.col = SRC.col,DELETE| -- one with UPDATE one with DELETE
WHEN NOT MATCHET  -- one clause allowed
	THEN INSERT VALUES(val1 valN)-- if indicated, action must be INSERT
WHEN NOT MATCHED BY SOURCE -- two clauses allowed:
THEN 8|UPDATE SET TGT.col = SRC.col,DELETE|; -- one with UPDATE one with DELETE
OUTPUT
\action as the_action
COALESCE(inserted.col, deleted.col) as operation_value
 
```  
> ## SELECT statement with CROSS APPLY
>  **Prefix:** selca ИЛИ selcrossapply ИЛИ crossapply  
```sql
 /*Започнете да пишете selca ИЛИ selcrossapply ИЛИ crossapply   и натиснете Tab, за да въведете фрагмента*/ 
 SELECT * 
FROM tableName as ot
	CROSS APPLY (SELECT TOP(numRows) colName 
				 FROM innerTableName as it
				 WHERE it.innerColumnName = ot.outerColumnName
				 ORDER BY colName) AS A
WHERE whereClause ;
 
```  
> ## SELECT statement with OUTER APPLY
>  **Prefix:** seloa ИЛИ selouterapply ИЛИ outerapply  
```sql
 /*Започнете да пишете seloa ИЛИ selouterapply ИЛИ outerapply   и натиснете Tab, за да въведете фрагмента*/ 
 SELECT * 
FROM tableName as ot
	OUTER APPLY (SELECT TOP(numRows) colName 
				 FROM innerTableName as it
				 WHERE it.innerColumnName = ot.outerColumnName
				 ORDER BY colName) AS A
WHERE whereClause ;
 
```  
> ## PIVOT data
>  **Prefix:** piv ИЛИ pivot  
```sql
 /*Започнете да пишете piv ИЛИ pivot   и натиснете Tab, за да въведете фрагмента*/ 
 WITH PivotData AS
(
	SELECT
		<grouping-column>,
		<spreading-column>,
		<aggregation-column>
	 FROM<source-table>
)
SELECT <grouping-column> distinct-spreading-values
FROM PivotData
	PIVOT( <aggregate-function>(<aggregate-column) 
		FOR <spreading-colimn> IN (distinct-spreading-values)
) AS P;
 
```  
> ## UNPIVOT data
>  **Prefix:** unpiv ИЛИ unpivot  
```sql
 /*Започнете да пишете unpiv ИЛИ unpivot   и натиснете Tab, за да въведете фрагмента*/ 
 SELECT
	<column-list>,
	<names-column>,
	<values-column>
FROM<source-table>
	UNPIVOT( <values-column> FOR <names-column IN <source-column> ) AS U;
 
```  

## ***MS SQL Server вградени функции***
*** 

> ## MS SQL built-in CAST function - converts data type
>  **Prefix:** cast
```sql
 /*Започнете да пишете cast и натиснете Tab, за да въведете фрагмента*/ 
 CAST(value AS dataTypeForConversion)
 
```  
> ## MS SQL built-in TRY_CAST function - converts data type. If it does not succeed it returns NULL.
>  **Prefix:** try_cast
```sql
 /*Започнете да пишете try_cast и натиснете Tab, за да въведете фрагмента*/ 
 TRY_CAST(value AS dataTypeForConversion)
 
```  
> ## MS SQL built-in CONVERT function - converts data type
>  **Prefix:** convert
```sql
 /*Започнете да пишете convert и натиснете Tab, за да въведете фрагмента*/ 
 CONVERT(dataTypeForConversion value)
 
```  
> ## MS SQL built-in TRY_CONVERT function - converts data type. If it does not succeed the function returns NULL.
>  **Prefix:** tryconvert
```sql
 /*Започнете да пишете tryconvert и натиснете Tab, за да въведете фрагмента*/ 
 TRY_CONVERT(dataTypeForConversion value)
 
```  
> ## MS SQL built-in PARSE function - Returns the result of an expression, translated to the requested data type in SQL Server.
>  **Prefix:** parse
```sql
 /*Започнете да пишете parse и натиснете Tab, за да въведете фрагмента*/ 
 PARSE(value AS dataTypeForConversion)
 
```  
> ## MS SQL built-in TRY_PARSE function - Returns the result of an expression, translated to the requested data type,ИЛИnull if the cast fails in SQL Server. Use TRY_PARSE only for converting from string to date/time and number types.
>  **Prefix:** try_parse
```sql
 /*Започнете да пишете try_parse и натиснете Tab, за да въведете фрагмента*/ 
 TRY_PARSE(value AS dataTypeForConversion)
 
```  
> ## MS SQL built-in DATEPART function - Returns an integer representing the specified datepart of the specified date. | Nondeterministic
>  **Prefix:** datepart ИЛИ dpart  
```sql
 /*Започнете да пишете datepart ИЛИ dpart   и натиснете Tab, за да въведете фрагмента*/ 
 DATEPART(1|year,quarter,month,dayofyear,day,week,weekday,hour,minute,second,millisecond,microsecond,nanosecond,tzoffset,iso_week| date)
 
```  
> ## MS SQL built-in DATENAME function - Returns a character string representing the specified datepart of the specified date. | Nondeterministic
>  **Prefix:** datename ИЛИ dname  
```sql
 /*Започнете да пишете datename ИЛИ dname   и натиснете Tab, за да въведете фрагмента*/ 
 DATENAME(1|year,quarter,month,dayofyear,day,week,weekday,hour,minute,second,millisecond,microsecond,nanosecond,tzoffset,iso_week| date)
 
```  
> ## MS SQL built-in DAY function - Returns an integer representing the day part of the specified date. | Deterministic
>  **Prefix:** day
```sql
 /*Започнете да пишете day и натиснете Tab, за да въведете фрагмента*/ 
 DAY(date)
 
```  
> ## MS SQL built-in MONTH function - Returns an integer representing the month part of a specified date. | Deterministic
>  **Prefix:** month
```sql
 /*Започнете да пишете month и натиснете Tab, за да въведете фрагмента*/ 
 MONTH(date)
 
```  
> ## MS SQL built-in YEAR function - Returns an integer representing the year part of a specified date. | Deterministic
>  **Prefix:** year
```sql
 /*Започнете да пишете year и натиснете Tab, за да въведете фрагмента*/ 
 YEAR(date)
 
```  
> ## MS SQL built-in DATEFROMPARTS function - Returns a date value for the specified year, month, and day.
>  **Prefix:** datefromparts ИЛИ dfp  
```sql
 /*Започнете да пишете datefromparts ИЛИ dfp   и натиснете Tab, за да въведете фрагмента*/ 
 DATEFROMPARTS(year month day)
 
```  
> ## MS SQL built-in DATETIMEFROMPARTS function - Returns a datetime value for the specified date and time.
>  **Prefix:** datetimefromparts ИЛИ dtfp  
```sql
 /*Започнете да пишете datetimefromparts ИЛИ dtfp   и натиснете Tab, за да въведете фрагмента*/ 
 DATETIMEFROMPARTS(year month day hour minute seconds milliseconds)
 
```  
> ## MS SQL built-in DATETIME2FROMPARTS function - Returns a datetime2 value for the specified date and time, with the specified precision.
>  **Prefix:** datetime2fromparts ИЛИ dt2fp  
```sql
 /*Започнете да пишете datetime2fromparts ИЛИ dt2fp   и натиснете Tab, за да въведете фрагмента*/ 
 DATETIME2FROMPARTS(year month day hour minute seconds fractions precision)
 
```  
> ## MS SQL built-in DATETIMEOFFSETFROMPARTS function - Returns a datetimeoffset value for the specified date and time, with the specified offsets and precision.
>  **Prefix:** datetimeoffsetfromparts ИЛИ dtofp  
```sql
 /*Започнете да пишете datetimeoffsetfromparts ИЛИ dtofp   и натиснете Tab, за да въведете фрагмента*/ 
 DATETIMEOFFSETFROMPARTS(year month day hour minute seconds fractions hour_offset minute_offset 1precision)
 
```  
> ## MS SQL built-in SMALLDATETIMEFROMPARTS function - Returns a smalldatetime value for the specified date and time.
>  **Prefix:** smalldatetimefromparts ИЛИ sdtfp  
```sql
 /*Започнете да пишете smalldatetimefromparts ИЛИ sdtfp   и натиснете Tab, за да въведете фрагмента*/ 
 SMALLDATETIMEFROMPARTS(year month day hour minute)
 
```  
> ## MS SQL built-in TIMEFROMPARTS function - Returns a time value for the specified time, with the specified precision.
>  **Prefix:** timefromparts ИЛИ tfp  
```sql
 /*Започнете да пишете timefromparts ИЛИ tfp   и натиснете Tab, за да въведете фрагмента*/ 
 TIMEFROMPARTS(hour minute seconds fractions precision)
 
```  
> ## MS SQL built-in DATEDIFF function - Returns the number of dateИЛИtime datepart boundaries, crossed between two specified dates. | Deterministic
>  **Prefix:** datediff ИЛИ dd  
```sql
 /*Започнете да пишете datediff ИЛИ dd   и натиснете Tab, за да въведете фрагмента*/ 
 DATEDIFF(1|year,quarter,month,dayofyear,day,week,hour,minute,second,millisecond,microsecond,nanosecond| startdate enddate)
 
```  
> ## MS SQL built-in DATEDIFF_BIG function - Returns the number of dateИЛИtime datepart boundaries, crossed between two specified dates. | Deterministic
>  **Prefix:** datediff_big ИЛИ ddb  
```sql
 /*Започнете да пишете datediff_big ИЛИ ddb   и натиснете Tab, за да въведете фрагмента*/ 
 DATEDIFF_BIG(1|year,quarter,month,dayofyear,day,week,hour,minute,second,millisecond,microsecond,nanosecond| startdate enddate)
 
```  
> ## MS SQL built-in DATEADD function - Returns a new datetime value by adding an interval to the specified datepart of the specified date. | Deterministic
>  **Prefix:** dateadd ИЛИ dadd  
```sql
 /*Започнете да пишете dateadd ИЛИ dadd   и натиснете Tab, за да въведете фрагмента*/ 
 DATEADD(1|year,quarter,month,dayofyear,day,week,hour,minute,second,millisecond,microsecond,nanosecond| number date)
 
```  
> ## MS SQL built-in EOMONTH function - Returns the last day of the month containing the specified date, with an optional offset. | Deterministic
>  **Prefix:** eomonth ИЛИ eom  
```sql
 /*Започнете да пишете eomonth ИЛИ eom   и натиснете Tab, за да въведете фрагмента*/ 
 EOMONTH(start_date month_to_add)
 
```  
> ## MS SQL built-in SWITCHOFFSET function - SWITCHOFFSET changes the time zone offset of a DATETIMEOFFSET value, and preserves the UTC value. | Deterministic
>  **Prefix:** switchoffset ИЛИ soffset  
```sql
 /*Започнете да пишете switchoffset ИЛИ soffset   и натиснете Tab, за да въведете фрагмента*/ 
 SWITCHOFFSET(datetimeoffset_expression timezoneoffset_expression)
 
```  
> ## MS SQL built-in TODATETIMEOFFSET function - TODATETIMEOFFSET transforms a datetime2 value into a datetimeoffset value. TODATETIMEOFFSET interprets the datetime2 value in local time, for the specified time_zone. | Deterministic
>  **Prefix:** todatetimeoffset ИЛИ tdtoffset  
```sql
 /*Започнете да пишете todatetimeoffset ИЛИ tdtoffset   и натиснете Tab, за да въведете фрагмента*/ 
 TODATETIMEOFFSET(expression time_zone)
 
```  
> ## MS SQL built-in ISDATE function - Determines whether a datetimeИЛИsmalldatetime input expression has a valid dateИЛИtime value.
>  **Prefix:** isdate
```sql
 /*Започнете да пишете isdate и натиснете Tab, за да въведете фрагмента*/ 
 ISDATE(expression)
 
```  
> ## MS SQL built-in DATALENGTH function - This function returns the number of bytes used to represent any expression.
>  **Prefix:** datalength ИЛИ datal  
```sql
 /*Започнете да пишете datalength ИЛИ datal   и натиснете Tab, за да въведете фрагмента*/ 
 DATALENGTH(expression)
 
```  
> ## MS SQL built-in ASCII function - Returns the ASCII code value of the leftmost character of a character expression.
>  **Prefix:** ascii
```sql
 /*Започнете да пишете ascii и натиснете Tab, за да въведете фрагмента*/ 
 ASCII(expression)
 
```  
> ## MS SQL built-in CHAR function - Returns the single-byte character with the specified integer code, as defined by the character set and encoding of the default collation of the current database.
>  **Prefix:** char
```sql
 /*Започнете да пишете char и натиснете Tab, за да въведете фрагмента*/ 
 CHAR(integer_expression)
 
```  
> ## MS SQL built-in CHARINDEX function - This function searches for one character expression inside a second character expression, returning the starting position of the first expression if found.
>  **Prefix:** charindex
```sql
 /*Започнете да пишете charindex и натиснете Tab, за да въведете фрагмента*/ 
 CHARINDEX(expressionToFind expressionToSearch)
 
```  
> ## MS SQL built-in CONCAT function - This function returns a string resulting from the concatenation,ИЛИjoining, of twoИЛИmore string values in an end-to-end manner. (To add a separating value during concatenation, see CONCAT_WS.)
>  **Prefix:** concat ИЛИ conc  
```sql
 /*Започнете да пишете concat ИЛИ conc   и натиснете Tab, за да въведете фрагмента*/ 
 CONCAT(string_value1 string_valueN)
 
```  
> ## MS SQL built-in CONCAT_WS function - This function returns a string resulting from the concatenation,ИЛИjoining, of twoИЛИmore string values in an end-to-end manner. It separates those concatenated string values with the delimiter specified in the first function argument. (CONCAT_WS indicates concatenate with separator.)
>  **Prefix:** concat_ws ИЛИ concws  
```sql
 /*Започнете да пишете concat_ws ИЛИ concws   и натиснете Tab, за да въведете фрагмента*/ 
 CONCAT_WS(separator string_value1 string_valueN)
 
```  
> ## MS SQL built-in DIFFERENCE function - This function returns an integer value measuring the difference between the SOUNDEX() values of two different character expressions.
>  **Prefix:** difference
```sql
 /*Започнете да пишете difference и натиснете Tab, за да въведете фрагмента*/ 
 DIFFERENCE(character_expression character_expression)
 
```  
> ## MS SQL built-in FORMAT function - Returns a value formatted with the specified format and optional culture. Use the FORMAT function for locale-aware formatting of date/time and number values as strings. For general data type conversions, use CASTИЛИCONVERT.
>  **Prefix:** format
```sql
 /*Започнете да пишете format и натиснете Tab, за да въведете фрагмента*/ 
 FORMAT(value format culture)
 
```  
> ## MS SQL built-in LEFT function - Returns the left part of a character string with the specified number of characters.
>  **Prefix:** left
```sql
 /*Започнете да пишете left и натиснете Tab, за да въведете фрагмента*/ 
 LEFT(character_expression integer_expression)
 
```  
> ## MS SQL built-in LEN function - Returns the number of characters of the specified string expression, excluding trailing spaces.
>  **Prefix:** len
```sql
 /*Започнете да пишете len и натиснете Tab, за да въведете фрагмента*/ 
 LEN(string_expression)
 
```  
> ## MS SQL built-in LOWER function - Returns a character expression after converting uppercase character data to lowercase.
>  **Prefix:** lower
```sql
 /*Започнете да пишете lower и натиснете Tab, за да въведете фрагмента*/ 
 LOWER(character_expression)
 
```  
> ## MS SQL built-in LTRIM function - Returns a character expression after it removes leading blanks.
>  **Prefix:** ltrim
```sql
 /*Започнете да пишете ltrim и натиснете Tab, за да въведете фрагмента*/ 
 LTRIM(character_expression)
 
```  
> ## MS SQL built-in NCHAR function - Returns the Unicode character with the specified integer code, as defined by the Unicode standard.
>  **Prefix:** nchar
```sql
 /*Започнете да пишете nchar и натиснете Tab, за да въведете фрагмента*/ 
 NCHAR(integer_expression)
 
```  
> ## MS SQL built-in PATINDEX function - Returns the starting position of the first occurrence of a pattern in a specified expression,ИЛИzeros if the pattern is not found, on all valid text and character data types.
>  **Prefix:** patindex
```sql
 /*Започнете да пишете patindex и натиснете Tab, за да въведете фрагмента*/ 
 PATINDEX('%integer_expression%' expression)
 
```  
> ## MS SQL built-in QUOTENAME function - Returns a Unicode string with the delimiters added to make the input string a valid SQL Server delimited identifier.
>  **Prefix:** quotename
```sql
 /*Започнете да пишете quotename и натиснете Tab, за да въведете фрагмента*/ 
 QUOTENAME('character_string')
 
```  
> ## MS SQL built-in REPLACE function - Replaces all occurrences of a specified string value with another string value.
>  **Prefix:** replace
```sql
 /*Започнете да пишете replace и натиснете Tab, за да въведете фрагмента*/ 
 REPLACE(string_expression string_pattern string_replacement)
 
```  
> ## MS SQL built-in REPLICATE function - Repeats a string value a specified number of times.
>  **Prefix:** replicate
```sql
 /*Започнете да пишете replicate и натиснете Tab, за да въведете фрагмента*/ 
 REPLICATE(string_expression integer_expression)
 
```  
> ## MS SQL built-in REVERSE function - Returns the reverse order of a string value.
>  **Prefix:** reverse
```sql
 /*Започнете да пишете reverse и натиснете Tab, за да въведете фрагмента*/ 
 REVERSE(string_expression)
 
```  
> ## MS SQL built-in RIGHT function - Returns the right part of a character string with the specified number of characters.
>  **Prefix:** right
```sql
 /*Започнете да пишете right и натиснете Tab, за да въведете фрагмента*/ 
 RIGHT(character_expression integer_expression)
 
```  
> ## MS SQL built-in RTRIM function - Returns a character string after truncating all trailing spaces.
>  **Prefix:** rtrim
```sql
 /*Започнете да пишете rtrim и натиснете Tab, за да въведете фрагмента*/ 
 RTRIM(character_expression)
 
```  
> ## MS SQL built-in SOUNDEX function - Returns a four-character (SOUNDEX) code to evaluate the similarity of two strings.
>  **Prefix:** soundex
```sql
 /*Започнете да пишете soundex и натиснете Tab, за да въведете фрагмента*/ 
 SOUNDEX(character_expression)
 
```  
> ## MS SQL built-in SPACE function - Returns a string of repeated spaces.
>  **Prefix:** space
```sql
 /*Започнете да пишете space и натиснете Tab, за да въведете фрагмента*/ 
 SPACE(integer_expression)
 
```  
> ## MS SQL built-in STR function - Returns character data converted from numeric data. The character data is right-justified, with a specified length and decimal precision.
>  **Prefix:** str
```sql
 /*Започнете да пишете str и натиснете Tab, за да въведете фрагмента*/ 
 STR(float_expression length decimal)
 
```  
> ## MS SQL built-in STRING_AGG function - Concatenates the values of string expressions and places separator values between them. The separator isn't added at the end of string.
>  **Prefix:** string_agg
```sql
 /*Започнете да пишете string_agg и натиснете Tab, за да въведете фрагмента*/ 
 STRING_AGG(expression separator) WITHIN GROUP ( ORDER BY order_by_expression_list 4|ASC,DESC| )
 
```  
> ## MS SQL built-in STRING_ESCAPE function - Escapes special characters in texts and returns text with escaped characters. STRING_ESCAPE is a deterministic function, introduced in SQL Server 2016.
>  **Prefix:** string_escape
```sql
 /*Започнете да пишете string_escape и натиснете Tab, за да въведете фрагмента*/ 
 STRING_ESCAPE(text type)
 
```  
> ## MS SQL built-in STRING_SPLIT function - A table-valued function that splits a string into rows of substrings, based on a specified separator character.
>  **Prefix:** string_split
```sql
 /*Започнете да пишете string_split и натиснете Tab, за да въведете фрагмента*/ 
 SELECT value 
FROM STRING_SPLIT(string separator);
 
```  
> ## MS SQL built-in STUFF function - The STUFF function inserts a string into another string. It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.
>  **Prefix:** stuff
```sql
 /*Започнете да пишете stuff и натиснете Tab, за да въведете фрагмента*/ 
 STUFF(character_expression start length replaceWith_expression)
 
```  
> ## MS SQL built-in SUBSTRING function - Returns part of a character, binary, text,ИЛИimage expression in SQL Server.
>  **Prefix:** substring
```sql
 /*Започнете да пишете substring и натиснете Tab, за да въведете фрагмента*/ 
 SUBSTRING(expression start length)
 
```  
> ## MS SQL built-in TRANSLATE function - Returns the string provided as a first argument after some characters specified in the second argument are translated into a destination set of characters specified in the third argument.
>  **Prefix:** translate
```sql
 /*Започнете да пишете translate и натиснете Tab, за да въведете фрагмента*/ 
 TRANSLATE(inputString characters translations)
 
```  
> ## MS SQL built-in TRIM function - Removes the space character char(32)ИЛИother specified characters from the start and end of a string.
>  **Prefix:** trim
```sql
 /*Започнете да пишете trim и натиснете Tab, за да въведете фрагмента*/ 
 TRIM(string)
 
```  
> ## MS SQL built-in UNICODE function - Returns the integer value, as defined by the Unicode standard, for the first character of the input expression.
>  **Prefix:** unicode
```sql
 /*Започнете да пишете unicode и натиснете Tab, за да въведете фрагмента*/ 
 UNICODE('ncharacter_expression')
 
```  
> ## MS SQL built-in UPPER function - Returns a character expression with lowercase character data converted to uppercase.
>  **Prefix:** upper
```sql
 /*Започнете да пишете upper и натиснете Tab, за да въведете фрагмента*/ 
 UPPER(character_expression)
 
```  
> ## MS SQL built-in IIF function - Returns one of two values, depending on whether the Boolean expression evaluates to trueИЛИfalse in SQL Server.
>  **Prefix:** iif
```sql
 /*Започнете да пишете iif и натиснете Tab, за да въведете фрагмента*/ 
 IIF(boolean_expression true_value false_value)
 
```  
> ## MS SQL built-in CHOOSE function - Returns the item at the specified index from a list of values in SQL Server.
>  **Prefix:** choose
```sql
 /*Започнете да пишете choose и натиснете Tab, за да въведете фрагмента*/ 
 CHOOSE(index val_1 val_n)
 
```  
> ## MS SQL built-in ABS function - A mathematical function that returns the absolute (positive) value of the specified numeric expression. (ABS changes negative values to positive values. ABS has no effect on zeroИЛИpositive values.)
>  **Prefix:** abs
```sql
 /*Започнете да пишете abs и натиснете Tab, за да въведете фрагмента*/ 
 ABS(numeric_expression)
 
```  
> ## MS SQL built-in ACOS function - A function that returns the angle, in radians, whose cosine is the specified float expression. This is also called arccosine.
>  **Prefix:** acos
```sql
 /*Започнете да пишете acos и натиснете Tab, за да въведете фрагмента*/ 
 ACOS(float_expression)
 
```  
> ## MS SQL built-in ASIN function - A function that returns the angle, in radians, whose sine is the specified float expression. This is also called arcsine.
>  **Prefix:** asin
```sql
 /*Започнете да пишете asin и натиснете Tab, за да въведете фрагмента*/ 
 ASIN(float_expression)
 
```  
> ## MS SQL built-in ATAN function - A function that returns the angle, in radians, whose tangent is a specified float expression. This is also called arctangent.
>  **Prefix:** atan
```sql
 /*Започнете да пишете atan и натиснете Tab, за да въведете фрагмента*/ 
 ATAN(float_expression)
 
```  
> ## MS SQL built-in ATN2 function - Returns the angle, in radians, between the positive x-axis and the ray from the origin to the point (y, x), where x and y are the values of the two specified float expressions.
>  **Prefix:** atan2
```sql
 /*Започнете да пишете atan2 и натиснете Tab, за да въведете фрагмента*/ 
 ATN2(float_expression float_expression)
 
```  
> ## MS SQL built-in CEILING function - This function returns the smallest integer greater than,ИЛИequal to, the specified numeric expression.
>  **Prefix:** ceiling
```sql
 /*Започнете да пишете ceiling и натиснете Tab, за да въведете фрагмента*/ 
 CEILING(numeric_expression)
 
```  
> ## MS SQL built-in COS function - A mathematical function that returns the trigonometric cosine of the specified angle - measured in radians - in the specified expression.
>  **Prefix:** cos
```sql
 /*Започнете да пишете cos и натиснете Tab, за да въведете фрагмента*/ 
 COS(float_expression)
 
```  
> ## MS SQL built-in COT function - A mathematical function that returns the trigonometric cotangent of the specified angle - in radians - in the specified float expression.
>  **Prefix:** cot
```sql
 /*Започнете да пишете cot и натиснете Tab, за да въведете фрагмента*/ 
 COT(float_expression)
 
```  
> ## MS SQL built-in DEGREES function - This function returns the corresponding angle, in degrees, for an angle specified in radians.
>  **Prefix:** degrees
```sql
 /*Започнете да пишете degrees и натиснете Tab, за да въведете фрагмента*/ 
 DEGREES(numeric_expression)
 
```  
> ## MS SQL built-in EXP function - Returns the exponential value of the specified float expression.
>  **Prefix:** exp
```sql
 /*Започнете да пишете exp и натиснете Tab, за да въведете фрагмента*/ 
 EXP(float_expression)
 
```  
> ## MS SQL built-in FLOOR function - Returns the largest integer less thanИЛИequal to the specified numeric expression.
>  **Prefix:** floor
```sql
 /*Започнете да пишете floor и натиснете Tab, за да въведете фрагмента*/ 
 FLOOR(numeric_expression)
 
```  
> ## MS SQL built-in LOG function - Returns the natural logarithm of the specified float expression in SQL Server.
>  **Prefix:** log
```sql
 /*Започнете да пишете log и натиснете Tab, за да въведете фрагмента*/ 
 LOG(float_expression base)
 
```  
> ## MS SQL built-in LOG10 function - Returns the base-10 logarithm of the specified float expression.
>  **Prefix:** log10
```sql
 /*Започнете да пишете log10 и натиснете Tab, за да въведете фрагмента*/ 
 LOG10(float_expression)
 
```  
> ## MS SQL built-in POWER function - Returns the value of the specified expression to the specified power.
>  **Prefix:** power
```sql
 /*Започнете да пишете power и натиснете Tab, за да въведете фрагмента*/ 
 POWER(float_expression y)
 
```  
> ## MS SQL built-in RADIANS function - Returns radians when a numeric expression, in degrees, is entered.
>  **Prefix:** radians
```sql
 /*Започнете да пишете radians и натиснете Tab, за да въведете фрагмента*/ 
 RADIANS(numeric_expression)
 
```  
> ## MS SQL built-in RAND function - Returns a pseudo-random float value from 0 through 1, exclusive.
>  **Prefix:** randf
```sql
 /*Започнете да пишете randf и натиснете Tab, за да въведете фрагмента*/ 
 RAND(seed)
 
```  
> ## MS SQL built-in ROUND function - Returns a numeric value, rounded to the specified lengthИЛИprecision.
>  **Prefix:** round
```sql
 /*Започнете да пишете round и натиснете Tab, за да въведете фрагмента*/ 
 ROUND(seed length 3|tinyint,smallint,int|)
 
```  
> ## MS SQL built-in SIGN function - Returns the positive (+1), zero (0),ИЛИnegative (-1) sign of the specified expression.
>  **Prefix:** sign
```sql
 /*Започнете да пишете sign и натиснете Tab, за да въведете фрагмента*/ 
 SIGN(numeric_expression)
 
```  
> ## MS SQL built-in SIN function - Returns the trigonometric sine of the specified angle, in radians, and in an approximate numeric, float, expression.
>  **Prefix:** sin
```sql
 /*Започнете да пишете sin и натиснете Tab, за да въведете фрагмента*/ 
 SIN(float_expression)
 
```  
> ## MS SQL built-in SQRT function - Returns the square root of the specified float value.
>  **Prefix:** sqrt
```sql
 /*Започнете да пишете sqrt и натиснете Tab, за да въведете фрагмента*/ 
 SQRT(float_expression)
 
```  
> ## MS SQL built-in SQUARE function - Returns the square of the specified float value.
>  **Prefix:** square
```sql
 /*Започнете да пишете square и натиснете Tab, за да въведете фрагмента*/ 
 SQUARE(float_expression)
 
```  
> ## MS SQL built-in TAN function - Returns the tangent of the input expression.
>  **Prefix:** tan
```sql
 /*Започнете да пишете tan и натиснете Tab, за да въведете фрагмента*/ 
 TAN(float_expression)
 
```  
> ## MS SQL built-in ISJSON function - Tests whether a string contains valid JSON.
>  **Prefix:** isjson
```sql
 /*Започнете да пишете isjson и натиснете Tab, за да въведете фрагмента*/ 
 ISJSON(expression)
 
```  
> ## MS SQL built-in JSON_VALUE function - Extracts a scalar value from a JSON string.
>  **Prefix:** json_value
```sql
 /*Започнете да пишете json_value и натиснете Tab, за да въведете фрагмента*/ 
 JSON_VALUE(expression path)
 
```  
> ## MS SQL built-in JSON_QUERY function - Extracts an objectИЛИan array from a JSON string.
>  **Prefix:** json_query
```sql
 /*Започнете да пишете json_query и натиснете Tab, за да въведете фрагмента*/ 
 JSON_QUERY(expression path)
 
```  
> ## MS SQL built-in JSON_MODIFY function - Updates the value of a property in a JSON string and returns the updated JSON string.
>  **Prefix:** json_modify
```sql
 /*Започнете да пишете json_modify и натиснете Tab, за да въведете фрагмента*/ 
 JSON_MODIFY(expression path newValue)
 
```  
> ## MS SQL built-in APPROX_COUNT_DISTINCT function - This function returns the approximate number of unique non-null values in a group.
>  **Prefix:** approx_count_distinct
```sql
 /*Започнете да пишете approx_count_distinct и натиснете Tab, за да въведете фрагмента*/ 
 APPROX_COUNT_DISTINCT(expression)
 
```  
> ## MS SQL built-in AVG function - This function returns the average of the values in a group. It ignores null values.
>  **Prefix:** avg
```sql
 /*Започнете да пишете avg и натиснете Tab, за да въведете фрагмента*/ 
 AVG(expression)
 
```  
> ## MS SQL built-in CHECKSUM_AGG function - This function returns the checksum of the values in a group. CHECKSUM_AGG ignores null values. The OVER clause can follow CHECKSUM_AGG.
>  **Prefix:** checksum_agg
```sql
 /*Започнете да пишете checksum_agg и натиснете Tab, за да въведете фрагмента*/ 
 CHECKSUM_AGG(expression)
 
```  
> ## MS SQL built-in COUNT function - This function returns the number of items found in a group. COUNT operates like the COUNT_BIG function. These functions differ only in the data types of their return values. COUNT always returns an int data type value. COUNT_BIG always returns a bigint data type value.
>  **Prefix:** count
```sql
 /*Започнете да пишете count и натиснете Tab, за да въведете фрагмента*/ 
 COUNT(1|expression*|)
 
```  
> ## MS SQL built-in COUNT_BIG function - This function returns the number of items found in a group. COUNT_BIG operates like the COUNT function. These functions differ only in the data types of their return values. COUNT_BIG always returns a bigint data type value. COUNT always returns an int data type value.
>  **Prefix:** count_big
```sql
 /*Започнете да пишете count_big и натиснете Tab, за да въведете фрагмента*/ 
 COUNT_BIG(1|expression*|)
 
```  
> ## MS SQL built-in GROUPING function - Indicates whether a specified column expression in a GROUP BY list is aggregatedИЛИnot. GROUPING returns 1 for aggregatedИЛИ0 for not aggregated in the result set. GROUPING can be used only in the SELECT <select> list, HAVING, and ORDER BY clauses when GROUP BY is specified.
>  **Prefix:** grouping
```sql
 /*Започнете да пишете grouping и натиснете Tab, за да въведете фрагмента*/ 
 GROUPING(column_expression)
 
```  
> ## MS SQL built-in GROUPING_ID function - Is a function that computes the level of grouping. GROUPING_ID can be used only in the SELECT <select> list, HAVING,ИЛИORDER BY clauses when GROUP BY is specified.
>  **Prefix:** grouping_id
```sql
 /*Започнете да пишете grouping_id и натиснете Tab, за да въведете фрагмента*/ 
 GROUPING_ID(column_expression)
 
```  
> ## MS SQL built-in MAX function - Returns the maximum value in the expression.
>  **Prefix:** max
```sql
 /*Започнете да пишете max и натиснете Tab, за да въведете фрагмента*/ 
 MAX(expression)
 
```  
> ## MS SQL built-in MIN function - Returns the minimum value in the expression. May be followed by the OVER clause.
>  **Prefix:** min
```sql
 /*Започнете да пишете min и натиснете Tab, за да въведете фрагмента*/ 
 MIN(expression)
 
```  
> ## MS SQL built-in STDEV function - Returns the statistical standard deviation of all values in the specified expression.
>  **Prefix:** stdev
```sql
 /*Започнете да пишете stdev и натиснете Tab, за да въведете фрагмента*/ 
 STDEV(expression)
 
```  
> ## MS SQL built-in STDEVP function - Returns the statistical standard deviation for the population for all values in the specified expression.
>  **Prefix:** stdevp
```sql
 /*Започнете да пишете stdevp и натиснете Tab, за да въведете фрагмента*/ 
 STDEVP(expression)
 
```  
> ## MS SQL built-in SUM function - Returns the sum of all the values,ИЛИonly the DISTINCT values, in the expression. SUM can be used with numeric columns only. Null values are ignored.
>  **Prefix:** sum
```sql
 /*Започнете да пишете sum и натиснете Tab, за да въведете фрагмента*/ 
 SUM(expression)
 
```  
> ## MS SQL built-in VAR function - Returns the statistical variance of all values in the specified expression. May be followed by the OVER clause.
>  **Prefix:** var
```sql
 /*Започнете да пишете var и натиснете Tab, за да въведете фрагмента*/ 
 VAR(expression)
 
```  
> ## MS SQL built-in VARP function - Returns the statistical variance for the population for all values in the specified expression.
>  **Prefix:** varp
```sql
 /*Започнете да пишете varp и натиснете Tab, за да въведете фрагмента*/ 
 VARP(expression)
```  


## ***Условна логика***
*** 


> ## CASE expression WHEN
>  **Prefix:** case ИЛИ cw  
```sql
 /*Започнете да пишете case ИЛИ cw   и натиснете Tab, за да въведете фрагмента*/ 
 CASE value
	WHEN firstCase THEN IfFirstCaseValue  
	WHEN N-thCase THEN IfN-thCaseValue 
ELSE ElseCaseValue
END
 
```  
> ## IF operator
>  **Prefix:** if
```sql
 /*Започнете да пишете if и натиснете Tab, за да въведете фрагмента*/ 
 if (condition)
BEGIN
	bodyOfIf
END
 
```  
> ## IF-ELSE operator
>  **Prefix:** ife
```sql
 /*Започнете да пишете ife и натиснете Tab, за да въведете фрагмента*/ 
 if (condition)
BEGIN
	bodyOfIf
END
ELSE
BEGIN
	bodyOfElse
END
 
```  
> ## IF-ELSE IF operator
>  **Prefix:** ifeif
```sql
 /*Започнете да пишете ifeif и натиснете Tab, за да въведете фрагмента*/ 
 if (condition)
BEGIN
	bodyOfIf
END
ELSE IF(condition)
BEGIN
	bodyOfElse
END
 
```  
> ## IF EXISTS - Specifies a subquery to test for the existence of rows.
>  **Prefix:** ifex
```sql
 /*Започнете да пишете ifex и натиснете Tab, за да въведете фрагмента*/ 
 if exists( SELECT * 
			FROM tableName
			WHERE whereClause )
BEGIN
	bodyOfIf
END
 
```  
> ## IF NOT EXISTS - Specifies a subquery to test for the existence of rows.
>  **Prefix:** ifnex
```sql
 /*Започнете да пишете ifnex и натиснете Tab, за да въведете фрагмента*/ 
 if not exists( SELECT * 
			FROM tableName
			WHERE whereClause )
BEGIN
	bodyOfIf
END
 
```  

## ***Деклариране на променливи***
*** 

> ## Declares a BIGINT variable WITH DECLARE
>  **Prefix:** decbi
```sql
 /*Започнете да пишете decbi и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName BIGINT 
 
```  
> ## Declares a BIGINT variable
>  **Prefix:** @pbi
```sql
 /*Започнете да пишете @pbi и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName BIGINT, 
 
```  
> ## Declares an INT variable WITH DECLARE
>  **Prefix:** deci
```sql
 /*Започнете да пишете deci и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName INT 
 
```  
> ## Declares an INT variable
>  **Prefix:** @pi
```sql
 /*Започнете да пишете @pi и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName INT, 
 
```  
> ## Declares a SMALLINT variable WITH DECLARE
>  **Prefix:** decsi
```sql
 /*Започнете да пишете decsi и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName SMALLINT 
 
```  
> ## Declares a SMALLINT variable
>  **Prefix:** @psi
```sql
 /*Започнете да пишете @psi и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName SMALLINT, 
 
```  
> ## Declares a TINYINT variable WITH DECLARE
>  **Prefix:** decti
```sql
 /*Започнете да пишете decti и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName TINYINT 
 
```  
> ## Declares a TINYINT variable
>  **Prefix:** @pti
```sql
 /*Започнете да пишете @pti и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName TINYINT, 
 
```  
> ## Declares a DECIMAL variable WITH DECLARE
>  **Prefix:** decdec
```sql
 /*Започнете да пишете decdec и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName DECIMAL(precision scale) 
 
```  
> ## Declares a DECIMAL variable
>  **Prefix:** @pdec
```sql
 /*Започнете да пишете @pdec и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName DECIMAL(precision scale), 
 
```  
> ## Declares a MONEY variable WITH DECLARE
>  **Prefix:** decm
```sql
 /*Започнете да пишете decm и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName MONEY 
 
```  
> ## Declares a MONEY variable
>  **Prefix:** @pm
```sql
 /*Започнете да пишете @pm и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName MONEY, 
 
```  
> ## Declares a SMALLMONEY variable WITH DECLARE
>  **Prefix:** decsm
```sql
 /*Започнете да пишете decsm и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName SMALLMONEY 
 
```  
> ## Declares a SMALLMONEY variable
>  **Prefix:** @psm
```sql
 /*Започнете да пишете @psm и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName SMALLMONEY, 
 
```  
> ## Declares a BIT variable WITH DECLARE
>  **Prefix:** decb
```sql
 /*Започнете да пишете decb и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName BIT 
 
```  
> ## Declares a BIT variable
>  **Prefix:** @pb
```sql
 /*Започнете да пишете @pb и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName BIT, 
 
```  
> ## Declares a FLOAT variable WITH DECLARE
>  **Prefix:** decf
```sql
 /*Започнете да пишете decf и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName FLOAT(precision) 
 
```  
> ## Declares a FLOAT variable
>  **Prefix:** @pf
```sql
 /*Започнете да пишете @pf и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName FLOAT(precision), 
 
```  
> ## Declares a REAL variable WITH DECLARE
>  **Prefix:** decr
```sql
 /*Започнете да пишете decr и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName REAL 
 
```  
> ## Declares a REAL variable
>  **Prefix:** @pr
```sql
 /*Започнете да пишете @pr и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName REAL, 
 
```  
> ## Declares a DATE variable WITH DECLARE
>  **Prefix:** decd
```sql
 /*Започнете да пишете decd и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varNamdatee DATE 
 
```  
> ## Declares a DATE variable
>  **Prefix:** @pd
```sql
 /*Започнете да пишете @pd и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName DATE, 
 
```  
> ## Declares a DATETIME variable WITH DECLARE
>  **Prefix:** decdt
```sql
 /*Започнете да пишете decdt и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName DATETIME 
 
```  
> ## Declares a DATETIME variable
>  **Prefix:** @pdt
```sql
 /*Започнете да пишете @pdt и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName DATETIME, 
 
```  
> ## Declares a SMALLDATETIME variable WITH DECLARE
>  **Prefix:** decsmdt
```sql
 /*Започнете да пишете decsmdt и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName SMALLDATETIME 
 
```  
> ## Declares a SMALLDATETIME variable
>  **Prefix:** @psmdt
```sql
 /*Започнете да пишете @psmdt и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName SMALLDATETIME, 
 
```  
> ## Declares a DATETIME2 variable WITH DECLARE
>  **Prefix:** decdt2
```sql
 /*Започнете да пишете decdt2 и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName DATETIME2 
 
```  
> ## Declares a DATETIME2 variable
>  **Prefix:** @pdt2
```sql
 /*Започнете да пишете @pdt2 и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName DATETIME2, 
 
```  
> ## Declares a TIME variable WITH DECLARE
>  **Prefix:** dect
```sql
 /*Започнете да пишете dect и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName TIME(fractionalSecondScale)) 
 
```  
> ## Declares a TIME variable
>  **Prefix:** @pt
```sql
 /*Започнете да пишете @pt и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName TIME(fractionalSecondScale)), 
 
```  
> ## Declares a DATETIMEOFFSET variable WITH DECLARE
>  **Prefix:** decdto
```sql
 /*Започнете да пишете decdto и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName DATETIMEOFFSET(fractionalSecondScale)) 
 
```  
> ## Declares a DATETIMEOFFSET variable
>  **Prefix:** @pdto
```sql
 /*Започнете да пишете @pdto и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName DATETIMEOFFSET(fractionalSecondScale)), 
 
```  
> ## Declares a CHAR variable WITH DECLARE
>  **Prefix:** decc
```sql
 /*Започнете да пишете decc и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName CHAR(varSize) 
 
```  
> ## Declares a CHAR variable
>  **Prefix:** @pc
```sql
 /*Започнете да пишете @pc и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName CHAR(varSize), 
 
```  
> ## Declares a NCHAR variable WITH DECLARE
>  **Prefix:** decnc
```sql
 /*Започнете да пишете decnc и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName NCHAR(varSize) 
 
```  
> ## Declares a NCHAR variable
>  **Prefix:** @pnc
```sql
 /*Започнете да пишете @pnc и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName NCHAR(varSize), 
 
```  
> ## Declares a VARCHAR variable WITH DECLARE
>  **Prefix:** decv
```sql
 /*Започнете да пишете decv и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName VARCHAR(varSize) 
 
```  
> ## Declares a VARCHAR variable
>  **Prefix:** @pv
```sql
 /*Започнете да пишете @pv и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName VARCHAR(varSize), 
 
```  
> ## Declares a NVARCHAR variable WITH DECLARE
>  **Prefix:** decnv
```sql
 /*Започнете да пишете decnv и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName NVARCHAR(varSize) 
 
```  
> ## Declares a NVARCHAR variable
>  **Prefix:** @pnv
```sql
 /*Започнете да пишете @pnv и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName NVARCHAR(varSize), 
 
```  
> ## Declares a BINARY variable WITH DECLARE
>  **Prefix:** decbin
```sql
 /*Започнете да пишете decbin и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName BINARY(varSize) 
 
```  
> ## Declares a BINARY variable
>  **Prefix:** @pbin
```sql
 /*Започнете да пишете @pbin и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName BINARY(varSize), 
 
```  
> ## Declares a VARBINARY variable WITH DECLARE
>  **Prefix:** decvbin
```sql
 /*Започнете да пишете decvbin и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName VARBINARY(varSize) 
 
```  
> ## Declares a VARBINARY variable
>  **Prefix:** @pvbin
```sql
 /*Започнете да пишете @pvbin и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName VARBINARY(varSize), 
 
```  
> ## Declares a SQL_VARIANT variable WITH DECLARE
>  **Prefix:** decsqlv
```sql
 /*Започнете да пишете decsqlv и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName SQL_VARIANT 
 
```  
> ## Declares a SQL_VARIANT variable
>  **Prefix:** @psqlv
```sql
 /*Започнете да пишете @psqlv и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName SQL_VARIANT, 
 
```  
> ## Declares a XML variable WITH DECLARE
>  **Prefix:** decxml
```sql
 /*Започнете да пишете decxml и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName XML 
 
```  
> ## Declares a XML variable
>  **Prefix:** @pxml
```sql
 /*Започнете да пишете @pxml и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName XML, 
 
```  
> ## Declares a UNIQUEIDENTIFIER variable WITH DECLARE
>  **Prefix:** decuniqi
```sql
 /*Започнете да пишете decuniqi и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName UNIQUEIDENTIFIER = NEWID();
 
```  
> ## Declares a UNIQUEIDENTIFIER variable
>  **Prefix:** @puniqi
```sql
 /*Започнете да пишете @puniqi и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName UNIQUEIDENTIFIER, 
 
```  
> ## Declares a GEOGRAPHY variable WITH DECLARE
>  **Prefix:** decgeo
```sql
 /*Започнете да пишете decgeo и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName GEOGRAPHY 
 
```  
> ## Declares a GEOGRAPHY variable
>  **Prefix:** @pgeo
```sql
 /*Започнете да пишете @pgeo и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName GEOGRAPHY, 
 
```  
> ## Declares a GEOMETRY variable WITH DECLARE
>  **Prefix:** decgeom
```sql
 /*Започнете да пишете decgeom и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName GEOMETRY 
 
```  
> ## Declares a GEOMETRY variable
>  **Prefix:** @pgeom
```sql
 /*Започнете да пишете @pgeom и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName GEOMETRY, 
 
```  
> ## Declares a TABLE variable WITH DECLARE
>  **Prefix:** dectable
```sql
 /*Започнете да пишете dectable и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_varName TABLE(col1 col1DataType col2 col2DataType)
 
```  
> ## Declares a TABLE variable
>  **Prefix:** @ptable
```sql
 /*Започнете да пишете @ptable и натиснете Tab, за да въведете фрагмента*/ 
 @p_varName TABLE(col1 col1DataType col2 col2DataType), 
 
```  


## ***Дефиниране на структури***
*** 


> ## Adds column to table
>  **Prefix:** addc ИЛИ add.column ИЛИ addco  
```sql
 /*Започнете да пишете addc ИЛИ add.column ИЛИ addco   и натиснете Tab, за да въведете фрагмента*/ 
 ALTER TABLE tableName ADD colName dataType 4|NULL,NOT NULL|;
 
```  
> ## Drops column table
>  **Prefix:** alterc ИЛИ altercolumn ИЛИ alterco  
```sql
 /*Започнете да пишете alterc ИЛИ altercolumn ИЛИ alterco   и натиснете Tab, за да въведете фрагмента*/ 
 ALTER TABLE tableName ALTER COLUMN colName dataType 4|NULL,NOT NULL|;
 
```  
> ## Drops column table
>  **Prefix:** dropc ИЛИ dropcolumn ИЛИ dropco  
```sql
 /*Започнете да пишете dropc ИЛИ dropcolumn ИЛИ dropco   и натиснете Tab, за да въведете фрагмента*/ 
 ALTER TABLE tableName DROP COLUMN colName;
 
```  
> ## Creates a CLUSTERED INDEX on table
>  **Prefix:** cci ИЛИ clustindex ИЛИ create.clusteredindex  
```sql
 /*Започнете да пишете cci ИЛИ clustindex ИЛИ create.clusteredindex   и натиснете Tab, за да въведете фрагмента*/ 
 CREATE CLUSTERED INDEX indexName ON tableName(columnName);
 
```  
> ## Creates an UNIQUE CLUSTERED INDEX on table
>  **Prefix:** cuci ИЛИ uniqueclustindex ИЛИ create.uniqueclusteredindex  
```sql
 /*Започнете да пишете cuci ИЛИ uniqueclustindex ИЛИ create.uniqueclusteredindex   и натиснете Tab, за да въведете фрагмента*/ 
 CREATE UNIQUE CLUSTERED INDEX indexName ON tableName(columnName);
 
```  
> ## Creates an UNIQUE CLUSTERED INDEX on table
>  **Prefix:** cnci ИЛИ nonclustindex ИЛИ create.nonclusteredindex  
```sql
 /*Започнете да пишете cnci ИЛИ nonclustindex ИЛИ create.nonclusteredindex   и натиснете Tab, за да въведете фрагмента*/ 
 CREATE NONCLUSTERED INDEX indexName ON tableName(columnName);
 
```  
> ## DROPS an INDEX on table
>  **Prefix:** di ИЛИ drop.index  
```sql
 /*Започнете да пишете di ИЛИ drop.index   и натиснете Tab, за да въведете фрагмента*/ 
 DROP INDEX indexName ON tableName;
 
```  
> ## ADDS PRIMARY KEY to CREATE TABLE STATEMENT
>  **Prefix:** pk ИЛИ primarykey  
```sql
 /*Започнете да пишете pk ИЛИ primarykey   и натиснете Tab, за да въведете фрагмента*/ 
 CONSTRAINT PK_primaryKeyName PRIMARY KEY CLUSTERED (columnName) 
 
```  
> ## ADDS FOREIGN KEY to CREATE TABLE STATEMENT
>  **Prefix:** fk ИЛИ foreignkey  
```sql
 /*Започнете да пишете fk ИЛИ foreignkey   и натиснете Tab, за да въведете фрагмента*/ 
 CONSTRAINT FK_primaryKeyName FOREIGN KEY (columnName) 
	REFERENCES referencedTable (columnInReferencedTable)
 
```  
> ## ADDS PRIMARY KEY to an existing TABLE
>  **Prefix:** addpk ИЛИ add.primarykey  
```sql
 /*Започнете да пишете addpk ИЛИ add.primarykey   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

ALTER TABLE tableName
ADD CONSTRAINT PK_primaryKeyName PRIMARY KEY CLUSTERED (columnName);
 
```  
> ## ADDS FOREIGN KEY to an existing TABLE
>  **Prefix:** addfk ИЛИ add.foreignkey  
```sql
 /*Започнете да пишете addfk ИЛИ add.foreignkey   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

ALTER TABLE tableName
ADD CONSTRAINT FK_primaryKeyName FOREIGN KEY (columnName)
	REFERENCES referencedTable (columnInReferencedTable); 
 
```  
> ## DROP CONSTRAINT of an existing TABLE
>  **Prefix:** dc ИЛИ drop.constraint  
```sql
 /*Започнете да пишете dc ИЛИ drop.constraint   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

ALTER TABLE tableName
DROP CONSTRAINT primaryKeyName ;
 
```  
> ## CREATES a new TABLE
>  **Prefix:** ct ИЛИ create.table  
```sql
 /*Започнете да пишете ct ИЛИ create.table   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

CREATE TABLE tableName
(
	colName dataType 5|NOT NULL, NULL|
	colName dataType 8|NOT NULL, NULL|
	colName 1dataType 11|NOT NULL, NULL|
	1colName 1dataType 14|NOT NULL, NULL|
	1colName 1dataType 17|NOT NULL, NULL|
	1colName 1dataType 20|NOT NULL, NULL|
CONSTRAINT PK_2primaryKeyName PRIMARY KEY CLUSTERED (colName) 
);
 
```  


## ***Създаване на процедури, функции, view***
*** 

> ## CREATES a view 
>  **Prefix:** cv ИЛИ create.view  
```sql
 /*Започнете да пишете cv ИЛИ create.view   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

CREATE VIEW viewName
AS
	SELECT * 
	FROM tableName
	WHERE whereClause ;
GO
 
```  
> ## ALTERES a view 
>  **Prefix:** av ИЛИ alter.view  
```sql
 /*Започнете да пишете av ИЛИ alter.view   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

ALTER VIEW viewName
AS
	SELECT * 
	FROM tableName
	WHERE whereClause ;
GO
 
```  
> ## DROPS a view 
>  **Prefix:** dv ИЛИ drop.view  
```sql
 /*Започнете да пишете dv ИЛИ drop.view   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

DROP VIEW IF EXISTS viewName 
 
```  
> ## CREATES an inline table function 
>  **Prefix:** cif ИЛИ create.inlinefunction  
```sql
 /*Започнете да пишете cif ИЛИ create.inlinefunction   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

CREATE FUNCTION functionName (
	@p_paramName AS paramDataType
)
RETURNS TABLE
AS
	SELECT * 
	FROM tableName
	WHERE whereClause ;
GO
 
```  
> ## CREATES an inline table function 
>  **Prefix:** csf ИЛИ create.scalarfunction  
```sql
 /*Започнете да пишете csf ИЛИ create.scalarfunction   и натиснете Tab, за да въведете фрагмента*/ 
 BLOCK_COMMENT_START A scalar user-defined function accepts parameters, applies calculations, and returns a single value. BLOCK_COMMENT_END
USE DatabaseName

CREATE FUNCTION functionName (
	@p_paramName AS paramDataType
)
RETURNS dataTypeThatFunctionReturns
AS
BEGIN
	BLOCK_COMMENT_START Write your logic here BLOCK_COMMENT_END
	RETURN @p_variable
END;
GO
 
```  
> ## CREATES an inline table function 
>  **Prefix:** cmtvf ИЛИ create.multistatementfunction  
```sql
 /*Започнете да пишете cmtvf ИЛИ create.multistatementfunction   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

CREATE FUNCTION functionName (
	@p_paramName AS paramDataType
)
RETURNS nameOfReturnedTable TABLE
(
	col1 dataType, 
	colNth dataTypeNth, 
)
AS
BEGIN
BLOCK_COMMENT_START
	Write your logic here
	The function should have INSERT INTO TABLE which will be returned

	INSERT INTO nameOfReturnedTable(col1 dataType colNth dataTypeNth)
	VALUES(1someValue 1someValue); 
BLOCK_COMMENT_END
	RETURN;
END;
GO
 
```  
> ## ALTERES an inline table function 
>  **Prefix:** aif ИЛИ alter.inlinefunction  
```sql
 /*Започнете да пишете aif ИЛИ alter.inlinefunction   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

ALTER FUNCTION functionName (
	@p_paramName AS paramDataType
)
RETURNS TABLE
AS
	SELECT * 
	FROM tableName
	WHERE whereClause ;
GO
 
```  
> ## DROPS a function 
>  **Prefix:** df ИЛИ drop.function  
```sql
 /*Започнете да пишете df ИЛИ drop.function   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

DROP FUNCTION IF EXISTS functionName ;
 
```  
> ## Creates basic body of procedure
>  **Prefix:** createproc ИЛИ create.procedure ИЛИ cproc  
```sql
 /*Започнете да пишете createproc ИЛИ create.procedure ИЛИ cproc   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE     procedure procedureName
variables,

as

begin
begin try
procedureBody
end try

begin catch
	if @@trancount > 0 
		rollback

	declare @p_err_num int,
		@p_err_sev int,
		@p_err_sta varchar(max),
		@p_err_prc varchar(max),
		@p_err_lne int,
		@p_err_mes varchar(max)

	select 
		@p_err_num = ERROR_NUMBER(),
		@p_err_sev = ERROR_SEVERITY(), 
		@p_err_sta = ERROR_STATE(),
		@p_err_prc = ERROR_PROCEDURE(), 
		@p_err_lne = ERROR_LINE(),
		@p_err_mes = ERROR_MESSAGE()

	exec logErrorsProcedureName
		@p_err_num = @p_err_num,
		@p_err_sev = @p_err_sev,
		@p_err_sta = @p_err_sta,
		@p_err_prc = @p_err_prc,
		@p_err_lne = @p_err_lne,
		@p_err_mes = @p_err_mes ,
		@p_cre_by = @p_cre_by

end catch

end

GO

 
```  
> ## DROPS a procedure 
>  **Prefix:** dp ИЛИ drop.procedure ИЛИ dproc  
```sql
 /*Започнете да пишете dp ИЛИ drop.procedure ИЛИ dproc   и натиснете Tab, за да въведете фрагмента*/ 
 USE DatabaseName

DROP PROCEDURE procedureName ;
GO
 
```  

## ***Полезни скриптове***
*** 

> ## Inserts `6 random Base-10 digits number` 
>  **Prefix:** random ИЛИ r  
```sql
 /*Започнете да пишете random ИЛИ r   и натиснете Tab, за да въведете фрагмента*/ 
 RANDOM
 
```  
> ## Inserts Block with Comments  
>  **Prefix:** bc ИЛИ blockcomment  
```sql
 /*Започнете да пишете bc ИЛИ blockcomment   и натиснете Tab, за да въведете фрагмента*/ 
 BLOCK_COMMENT_START
	yourCommentHere
BLOCK_COMMENT_END
 
```  
> ## Inserts Line Comments // 
>  **Prefix:** lc ИЛИ linecomment  
```sql
 /*Започнете да пишете lc ИЛИ linecomment   и натиснете Tab, за да въведете фрагмента*/ 
 LINE_COMMENT  yourCommentHere
 
```  
> ## Inserts current date 
>  **Prefix:** today ИЛИ currentdate ИЛИ currd  
```sql
 /*Започнете да пишете today ИЛИ currentdate ИЛИ currd   и натиснете Tab, за да въведете фрагмента*/ 
 'CURRENT_YEARCURRENT_MONTHCURRENT_DATE'
 
```  
> ## Inserts current datetime 
>  **Prefix:** now ИЛИ currentdatetime ИЛИ currdt  
```sql
 /*Започнете да пишете now ИЛИ currentdatetime ИЛИ currdt   и натиснете Tab, за да въведете фрагмента*/ 
 'CURRENT_YEARCURRENT_MONTHCURRENT_DATE CURRENT_HOUR:CURRENT_MINUTE:CURRENT_SECOND'
 
```  
> ## Inserts UNIX timestamp 
>  **Prefix:** unix  
```sql
 /*Започнете да пишете unix   и натиснете Tab, за да въведете фрагмента*/ 
 'CURRENT_SECONDS_UNIX'
 
```  
> ## TRY CATCH 
>  **Prefix:** try ИЛИ trycatch ИЛИ catch ИЛИ tc  
```sql
 /*Започнете да пишете try ИЛИ trycatch ИЛИ catch ИЛИ tc   и натиснете Tab, за да въведете фрагмента*/ 
 begin try
	statement
end try
begin catch
	if @@trancount > 0 
		rollback

	declare @p_err_num int,
			@p_err_sev int,
			@p_err_sta varchar(max),
			@p_err_prc varchar(max),
			@p_err_lne int,
			@p_err_mes varchar(max)

	select 
		@p_err_num = ERROR_NUMBER(),
		@p_err_sev = ERROR_SEVERITY(), 
		@p_err_sta = ERROR_STATE(),
		@p_err_prc = ERROR_PROCEDURE(), 
		@p_err_lne = ERROR_LINE(),
		@p_err_mes = ERROR_MESSAGE()

	exec logErrorProcedureName
		@p_err_num = @p_err_num,
		@p_err_sev = @p_err_sev,
		@p_err_sta = @p_err_sta,
		@p_err_prc = @p_err_prc,
		@p_err_lne = @p_err_lne,
		@p_err_mes = @p_err_mes ,
		@p_cre_by = @p_cre_by

end catch
 
```  

> ## Insert delay of execution of batchИЛИprocedure 
>  **Prefix:** delay ИЛИ waitfor ИЛИ wait  
```sql
 /*Започнете да пишете delay ИЛИ waitfor ИЛИ wait   и натиснете Tab, за да въведете фрагмента*/ 
 WAITFOR DELAY 'hoursminutesseconds' ;
 
```  
> ## Begins transaction 
>  **Prefix:** tran ИЛИ transaction ИЛИ begin.transaction ИЛИ begin.tran  
```sql
 /*Започнете да пишете tran ИЛИ transaction ИЛИ begin.transaction ИЛИ begin.tran   и натиснете Tab, за да въведете фрагмента*/ 
 BEGIN TRAN


yourTransactionStatements

IF @@TRANCOUNT > 0
BEGIN
	COMMIT
END
ELSE
BEGIN
	ROLLBACK
END
 
```  
> ## Example of correct executing of Dynamic SQL
>  **Prefix:** dsql ИЛИ dynamic ИЛИ dynamicsql  
```sql
 /*Започнете да пишете dsql ИЛИ dynamic ИЛИ dynamicsql   и натиснете Tab, за да въведете фрагмента*/ 
 DECLARE @p_param1 dataTypeParam1, 
		@p_param2 dataTypeParam2

DECLARE @p_sql AS NVARCHAR(MAX) = N'
	SELECT col1 colN
	FROM tableName
	WHERE 1 = 1
'
+ CASE WHEN @p_param1 IS NOT NULL THEN N' AND col1 = @p_param1' ELSE N'' END
+ CASE WHEN @p_param2 IS NOT NULL THEN N' AND colN = @p_param2' ELSE N'' END
+ N';'

EXEC sys.sp_executesql
	@stmt = @p_sql,
	@params = N'@p_param1 AS dataTypeParam1 @p_param2 as dataTypeParam2',
	@p_param1 = @p_param1,
	@p_param2 = @p_param2 ;
GO
 
```  



## Проблеми

За сега няма открити проблеми.

## Версии

### 0.2.0

Обновяване на документацията
    
### 0.0.1

Публикуване на разширението
    
## Лиценз

[MIT](LICENSE.txt)

**Приятно използване!**,  
**[Маг. Инж. Р. Батинов](https://radoslav-batinov.bss.design/)**
