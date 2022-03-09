# MS SQL Server Snippets

This is a VS Code extension that has a lot of useful snippets that are helpful for faster writing of your T-SQL code.

It can be useful for anyone who develops and administrates MS SQL Server databases and writes queries, procedures, functions, creates tables and many other SQL commands.

![Demo of Extension](/demo.gif)

## Table of Contents
***
- [1. Features](#features) 
- [2. Requirements](#requirements)
- [3. How to use](#how-to-use)
- [4. ALL available Snippets and their Prefixes](#all-available-snippets-and-their-prefixes)
    - [Data Modification](#data-modification-snippets)
    - [MS SQL Server Build In Functions](#ms-sql-server-functions)
    - [Condition Logic](#condition-logic)
    - [Variable Declarations](#variable-declarations)
    - [Data Definition Language](#data-definition-language)
    - [Useful Scripts](#useful-scripts)
    - [Create PROCEDURES, FUNCTIONS, VIEWS](#create-procedures-functions-views)
- [5. Known Issues](#known-issues)
- [6. Release Notes](#release-notes)
- [7. License](#license)


## Features
***  

- ### Snippets for:
    - ### **DATA MODIFICATION**
        - `SELECT`, `SELECT WITH WHERE CLAUSE`, `SELECT WITH EXISTS/NOT EXISTS`, `SELECT WITH IN/NOT IN`, 
        - `CTEs`, `RECURSIVE CTEs`
        - `INSERT INTO`, `INSERT WITH SELECT`, `INSERT EXEC`, `SELECT INTO`
        - `UPDATE`, `UPDATE WITH JOIN`
        - `DELETE`, `DELETE TOP(N)`, `TRUNCATE`
        - `MERGING DATA`
        - `INSERT WITH OUTPUT`, `UPDATE WITH OUTPUT`, `DELETE WITH OUTPUT`, `MERGE WITH OUTPUT`
        - `UNION`, `INTERSECT`, `EXCEPT`
        - `OFFSET-FETCH`
        - ALL types of JOINS - `INNER JOIN`, `LEFT OUTER JOIN`, `RIGHT OUTER JOIN`, `FULL OUTER JOIN`, `CROSS JOIN`
        - `CROSS APPLY` and `OUTER APPLY`
        - `PIVOT` and `UNPIVOT` data
        - ##### **CONDITIONS LOGIC**
            - `IF`, `IF-ELSE`, `IF EXISTS`, `IF NOT EXISTS`, `CASE`

    - ### **DATA DEFINITION**
        - ### **DECLARATIONS OF ALL DATA TYPE VARIABLES**
            - DECLARE `INT`, `BIGINT`, `SMALLINT`, `TINYINT`, `MONEY`, `SMALLMONEY`, `DECIMAL`, `FLOAT`, `REAL`, `BIT`, `DATE`, `DATETIME`, `SMALLDATETIME`, `DATETIMEOFFSET`, `TIME`, `CHAR`, `VARCHAR`, `NVARCHAR`, `BINARY`, `VARBINARY`, `SQL_VARIANT`, `XML`, `UNIQUEIDENTIFIER`, `GEOGRAPHY`, `GEOMETRY`, `TABLE`
        - ### **CREATE**, **ALTER** and **DROP**
            - `TABLES`, `VIEWS`, `INLINE FUNCTIONS`, `SCALAR FUNCTIONS`, `MULTISTATEMENT TABLE-VALUED FUNCTIONS`, `PROCEDURES`, `CLUSTERED INDEXES`, `NON-CLUSTERED INDEXES`, `PRIMARY KEYS`, `FOREIGN KEYS`, `CONSTRAINTS`

    - ### **ALL MS SQL Server Built-in FUNCTIONS**
        - ### **Conversion FUNCTIONS**
            - `CAST`, `TRY_CAST`, `CONVERT`, `TRY_CONVERT`, `PARSE`, `TRY_PARSE`
        - ### **Date and Time FUNCTIONS**
            - `DATEPART`, `DATENAME`, `DAY`, `MONTH`, `YEAR`, `DATEFROMPARTS`, `DATETIMEFROMPARTS`, `DATETIME2FROMPARTS`, `DATETIMEOFFSETFROMPARTS`, `SMALLDATETIMEFROMPARTS`, `TIMEFROMPARTS`, `DATEDIFF`, `DATEDIFF_BIG`, `DATEADD`, `EOMONTH`, `SWITCHOFFSET`, `TODATETIMEOFFSET`, `ISDATE`
        - ### **Data FUNCTIONS**
            - `DATALENGTH`
        - ### **String FUNCTIONS**
            - `ASCII`, `CHAR`, `CHARINDEX`, `CONCAT`, `CONCAT_WS`, `DIFFERENCE`, `FORMAT`, `LEFT`, `LEN`, `LOWER`, `LTRIM`, `NCHAR`, `PATINDEX`, `QUOTENAME`, `REPLACE`, `REPLICATE`, `REVERSE`, `RIGHT`, `RTRIM`, `SOUNDEX`, `SPACE`, `STR`, `STRING_AGG`, `STRING_ESCAPE`, `STRING_SPLIT`, `STUFF`, `SUBSTRING`, `TRANSLATE`, `TRIM`, `UNICODE`, `UPPER`
        - ### **Conditions FUNCTIONS**
            - `IIF`, `CHOOSE`
        - ### **Mathematical FUNCTIONS**
            - `ABS`, `ACOS`, `ASIN`, `ATAN`, `ATN2`, `CEILING`, `COS`, `COT`, `DEGREES`, `EXP`, `FLOOR`, `LOG`, `LOG10`, `POWER`, `RADIANS`, `RAND`, `ROUND`, `SIGN`, `SIN`, `SQRT`, `SQUARE`, `TAN`
        - ### **JSON FUNCTIONS**
            - `ISJSON`, `JSON_VALUE`, `JSON_QUERY`, `JSON_MODIFY`
        - ### **Aggregate FUNCTIONS**
            - `APPROX_COUNT_DISTINCT`, `AVG`, `CHECKSUM_AGG`, `COUNT`, `COUNT_BIG`, `GROUPING`, `GROUPING_ID`, `MAX`, `MIN`, `STDEV`, `STDEVP`, `SUM`, `VAR`, `VARP`
    - ### **OTHER USEFUL SCRIPTS**
        - `RANDOM NUMBER`, `BLOCK OF COMMENTS`, `LINE OF COMMENTS`, `GET CURRENT DATE`, `GET CURRENT DATETIME`, `GET UNIX TIMESTAMP`, `TRY-CATCH`, `INSERT DELAY`, `BEGIN TRANSACTION`, `EXECUTE DYNAMIC SQL`


## Requirements
*** 

- All You need to have is VS Code Installed, and of course this extension.


## How to use
***  

1. Install the extension: 
    - from [Marketplace](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.mssql-snippets&ssr=false#overview).  
    ![Extension Search](/extension-marketplace.png) 
    - from VS Code
        1. Open VS Code.
        2. Select `Extensions` from left panel or press `Ctrl + Shift + X`.
        3. Type in `mssql-snippets`. The extension with name `MSSQL Snippets` will show.   
        ![Extension Search](/extension-search.png)  
        4. You can select the extension and read the overview features if you want.  
        ![Extension Search](/extension-overview.png) 
        5. Pres `Install` button and you are ready.

2. Restart of VS Code may be needed.  
3. After installation you are ready to use it in all your `.sql` files.
4. Just type some of the prefixes shown `below` and popup with info about the snippet will show. Press `TAB` to insert the snippet in the editor.

## ALL available Snippets and their Prefixes
***  

## ***Data Modification Snippets***
***  

> ## SELECT statement
>  **Prefix:** sel
```sql
 /*Write down  sel  and press Tab to insert snippet*/ 
 SELECT * 
FROM tableName ;
 
```  
> ## SELECT statement 
>  **Prefix:** selc
```sql
 /*Write down  selc  and press Tab to insert snippet*/ 
 

BLOCK_COMMENT_START Snippet Generated Select with current selected text BLOCK_COMMENT_END
SELECT * 
FROM TM_SELECTED_TEXT:1 ; 0
BLOCK_COMMENT_START End of the Snippet Generated Select BLOCK_COMMENT_END


 
```  
> ## SELECT statement FROM CLIBOARD. You can copy some tableName and then type some of the prefixes and press Tab and select sattement with the copied table will be inserted.
>  **Prefix:** selcopied  OR  selclip  OR  selclipboard  
```sql
 /*Write down  selcopied  OR  selclip  OR  selclipboard    and press Tab to insert snippet*/ 
 

SELECT * 
FROM CLIPBOARD:1 ;


 
```  
> ## SELECT statement with WHERE clause
>  **Prefix:** selw
```sql
 /*Write down  selw  and press Tab to insert snippet*/ 
 SELECT * 
FROM tableName
WHERE whereClause ;
 
```  
> ## SELECT statement with WHERE clause with IN (...)
>  **Prefix:** selwin
```sql
 /*Write down  selwin  and press Tab to insert snippet*/ 
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
 /*Write down  selwnotin  and press Tab to insert snippet*/ 
 SELECT * 
FROM tableName as ot
WHERE ot.colName NOT IN (
	 SELECT it.colName
	 FROM innerTableName as it
	 WHERE it.whereClause
);
 
```  
> ## SELECT statement with WHERE clause with EXISTS(...)
>  **Prefix:** selwexists  OR  selwex  
```sql
 /*Write down  selwexists  OR  selwex    and press Tab to insert snippet*/ 
 SELECT * 
FROM tableName as ot
WHERE ot.colName EXISTS (
	 SELECT it.colName
	 FROM innerTableName as it
	 WHERE it.innerColumnName = ot.outerColumnName
);
 
```  
> ## SELECT statement with WHERE clause with EXISTS(...)
>  **Prefix:** selwnexists  OR  selwnex  
```sql
 /*Write down  selwnexists  OR  selwnex    and press Tab to insert snippet*/ 
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
 /*Write down  cte  and press Tab to insert snippet*/ 
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
 /*Write down  rcte  and press Tab to insert snippet*/ 
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
>  **Prefix:** ins  OR  insert  
```sql
 /*Write down  ins  OR  insert    and press Tab to insert snippet*/ 
 INSERT INTO TableName (Column)
VALUES(ColumnValue) ;
 
```  
> ## INSERT values into table (from CLIPBOARD)
>  **Prefix:** inscopied  OR  insertcopied  OR  insclip  OR  insclipboard  OR  icopied  OR  iclip  OR  iclipboard  
```sql
 /*Write down  inscopied  OR  insertcopied  OR  insclip  OR  insclipboard  OR  icopied  OR  iclip  OR  iclipboard    and press Tab to insert snippet*/ 
 INSERT INTO CLIPBOARD:1 (Column)
VALUES(ColumnValue) ;
 
```  
> ## INSERT values into table with SELECT FROM TABLE
>  **Prefix:** inss  OR  inssel  
```sql
 /*Write down  inss  OR  inssel    and press Tab to insert snippet*/ 
 INSERT INTO TableName (Column)
SELECT Column
FROM tableName ;
 
```  
> ## INSERT values into table with EXEC procedure
>  **Prefix:** inse  OR  insexec  
```sql
 /*Write down  inse  OR  insexec    and press Tab to insert snippet*/ 
 INSERT INTO TableName (Column)
EXEC procedureName
	@p_parameterName = parameterValue ;
 
```  
> ## SELECT values INTO table
>  **Prefix:** selinto
```sql
 /*Write down  selinto  and press Tab to insert snippet*/ 
 SELECT col1 col2
INTO tableNameToInsert
FROM tableFromGetData;
 
```  
> ## UPDATE rows from table
>  **Prefix:** upd  OR  update  
```sql
 /*Write down  upd  OR  update    and press Tab to insert snippet*/ 
 UPDATE TableName 
SET ColumnName = ColumnValue
WHERE WhereClause ;
 
```  
> ## UPDATE rows from table (from CLIPBOARD)
>  **Prefix:** updcopied  OR  updatecopied  OR  updclip  OR  updclipboard  OR  ucopied  OR  uclip  OR  iclipboard  
```sql
 /*Write down  updcopied  OR  updatecopied  OR  updclip  OR  updclipboard  OR  ucopied  OR  uclip  OR  iclipboard    and press Tab to insert snippet*/ 
 UPDATE CLIPBOARD:1 
SET ColumnValue = ColumnValue ;
WHERE WhereClause ;
 
```  
> ## UPDATE rows from table with JOIN
>  **Prefix:** updj  OR  updatej  
```sql
 /*Write down  updj  OR  updatej    and press Tab to insert snippet*/ 
 UPDATE t
SET t.columnName = jt.columnName
FROM tableToUpdate AS t 
	JOIN joinedTable AS jt 
		ON t.columnName = jt.columnName
;  
 
```  
> ## DELETE rows from table
>  **Prefix:** del  OR  delete  
```sql
 /*Write down  del  OR  delete    and press Tab to insert snippet*/ 
 DELETE FROM tableName
WHERE whereClause ;
 
```  
> ## DELETE rows from table
>  **Prefix:** delcopied  OR  deletecopied  OR  delclip  OR  deleteclip  OR  dclip  OR  dcopied  
```sql
 /*Write down  delcopied  OR  deletecopied  OR  delclip  OR  deleteclip  OR  dclip  OR  dcopied    and press Tab to insert snippet*/ 
 DELETE FROM CLIPBOARD:1
WHERE whereClause ;
 
```  
> ## DELETE TOP(n) rows from table
>  **Prefix:** delt  OR  deletet  
```sql
 /*Write down  delt  OR  deletet    and press Tab to insert snippet*/ 
 DELETE TOP(numberRowsToDelete) FROM tableName
WHERE whereClause ;
 
```  
> ## TRUNCATE table
>  **Prefix:** trunc
```sql
 /*Write down  trunc  and press Tab to insert snippet*/ 
 TRUNCATE TABLE tableName ; 
 
```  
> ## MERGE data
>  **Prefix:** merge
```sql
 /*Write down  merge  and press Tab to insert snippet*/ 
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
 /*Write down  offset  and press Tab to insert snippet*/ 
 SELECT colName
FROM tableName
ORDER BY colName
OFFSET numRowsOffset ROWS FETCH FIRST numRowsToFetch ROWS ONLY;
 
```  
> ## UNIONS table results
>  **Prefix:** uni
```sql
 /*Write down  uni  and press Tab to insert snippet*/ 
 SELECT colName as colName
FROM firstTableName

UNION 

SELECT colName as colName
FROM N-thTableName;
 
```  
> ## UNIONS ALL table results
>  **Prefix:** uniall
```sql
 /*Write down  uniall  and press Tab to insert snippet*/ 
 SELECT colName as colName
FROM firstTableName

UNION ALL

SELECT colName as colName
FROM N-thTableName;
 
```  
> ## INTERSECTS table results
>  **Prefix:** intersect
```sql
 /*Write down  intersect  and press Tab to insert snippet*/ 
 SELECT colName as colName
FROM firstTableName

INTERSECT

SELECT colName as colName
FROM N-thTableName;
 
```  
> ## EXCEPTS table results
>  **Prefix:** except
```sql
 /*Write down  except  and press Tab to insert snippet*/ 
 SELECT colName as colName
FROM firstTableName

EXCEPT

SELECT colName as colName
FROM N-thTableName;
 
```  
> ## CROSS JOIN tables
>  **Prefix:** cjoin
```sql
 /*Write down  cjoin  and press Tab to insert snippet*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	CROSS JOIN N-thTableName as N-thTableAlias;
 
```  
> ## INNER JOIN tables
>  **Prefix:** ijoin
```sql
 /*Write down  ijoin  and press Tab to insert snippet*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	INNER JOIN N-thTableName as N-thTableAlias ON firstTableAlias.colName = firstTableAlias.colName;
 
```  
> ## signle INNER JOIN line (without SELECT FROM statement)
>  **Prefix:** ij
```sql
 /*Write down  ij  and press Tab to insert snippet*/ 
 	INNER JOIN N-thTableName as N-thTableAlias ON N-thTableAlias.colName = firstTableAlias.colName
 
```  
> ## LEFT OUTER JOIN tables
>  **Prefix:** ljoin
```sql
 /*Write down  ljoin  and press Tab to insert snippet*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	LEFT OUTER JOIN N-thTableName as N-thTableAlias ON firstTableAlias.colName = firstTableAlias.colName;
 
```  
> ## signle LEFT OUTER JOIN line (without SELECT FROM statement)
>  **Prefix:** lj
```sql
 /*Write down  lj  and press Tab to insert snippet*/ 
 	LEFT OUTER JOIN N-thTableName as N-thTableAlias ON N-thTableAlias.colName = firstTableAlias.colName
 
```  
> ## RIGHT OUTER JOIN tables
>  **Prefix:** rjoin
```sql
 /*Write down  rjoin  and press Tab to insert snippet*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	RIGHT OUTER JOIN N-thTableName as N-thTableAlias ON firstTableAlias.colName = firstTableAlias.colName;
 
```  
> ## signle RIGHT OUTER JOIN line (without SELECT FROM statement)
>  **Prefix:** rj
```sql
 /*Write down  rj  and press Tab to insert snippet*/ 
 	RIGHT OUTER JOIN N-thTableName as N-thTableAlias ON N-thTableAlias.colName = firstTableAlias.colName
 
```  
> ## FULL OUTER JOIN tables
>  **Prefix:** fjoin
```sql
 /*Write down  fjoin  and press Tab to insert snippet*/ 
 SELECT firstTableAlias.colName firstTableAlias.colName
FROM firstTableName as firstTableAlias
	FULL OUTER JOIN N-thTableName as N-thTableAlias ON firstTableAlias.colName = firstTableAlias.colName;
 
```  
> ## signle FULL OUTER JOIN line (without SELECT FROM statement)
>  **Prefix:** fj
```sql
 /*Write down  fj  and press Tab to insert snippet*/ 
 	FULL OUTER JOIN N-thTableName as N-thTableAlias ON N-thTableAlias.colName = firstTableAlias.colName
 
```  
> ## INSERT into Table with OUTPUT
>  **Prefix:** io  OR  insertoutput  OR  inso  OR  insoutput  
```sql
 /*Write down  io  OR  insertoutput  OR  inso  OR  insoutput    and press Tab to insert snippet*/ 
 INSERT INTO tableName(col1 col2 col3)
OUTPUT
	inserted.col1, inserted.col2, inserted.col3
SELECT col1 col2 col3
FROM tableName
WHERE WhereClause;
 
```  
> ## UPDATE Table with OUTPUT
>  **Prefix:** uo  OR  updateoutput  OR  updo  OR  updoutput  
```sql
 /*Write down  uo  OR  updateoutput  OR  updo  OR  updoutput    and press Tab to insert snippet*/ 
 UPDATE tableName
	SET colName = value
OUTPUT
	inserted.colName as new_value,
	deleted.colName as old_value
WHERE WhereClause;
 
```  
> ## UPDATE Table with OUTPUT
>  **Prefix:** do  OR  deleteoutput  OR  delo  OR  deloutput  
```sql
 /*Write down  do  OR  deleteoutput  OR  delo  OR  deloutput    and press Tab to insert snippet*/ 
 DELETE FROM tableName
OUTPUT
	deleted.colName as deleted_value
WHERE WhereClause;
 
```  
> ## MERGE data with OUTPUT
>  **Prefix:** mergeoutput  OR  mo  
```sql
 /*Write down  mergeoutput  OR  mo    and press Tab to insert snippet*/ 
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
>  **Prefix:** selca  OR  selcrossapply  OR  crossapply  
```sql
 /*Write down  selca  OR  selcrossapply  OR  crossapply    and press Tab to insert snippet*/ 
 SELECT * 
FROM tableName as ot
	CROSS APPLY (SELECT TOP(numRows) colName 
				 FROM innerTableName as it
				 WHERE it.innerColumnName = ot.outerColumnName
				 ORDER BY colName) AS A
WHERE whereClause ;
 
```  
> ## SELECT statement with OUTER APPLY
>  **Prefix:** seloa  OR  selouterapply  OR  outerapply  
```sql
 /*Write down  seloa  OR  selouterapply  OR  outerapply    and press Tab to insert snippet*/ 
 SELECT * 
FROM tableName as ot
	OUTER APPLY (SELECT TOP(numRows) colName 
				 FROM innerTableName as it
				 WHERE it.innerColumnName = ot.outerColumnName
				 ORDER BY colName) AS A
WHERE whereClause ;
 
```  
> ## PIVOT data
>  **Prefix:** piv  OR  pivot  
```sql
 /*Write down  piv  OR  pivot    and press Tab to insert snippet*/ 
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
>  **Prefix:** unpiv  OR  unpivot  
```sql
 /*Write down  unpiv  OR  unpivot    and press Tab to insert snippet*/ 
 SELECT
	<column-list>,
	<names-column>,
	<values-column>
FROM<source-table>
	UNPIVOT( <values-column> FOR <names-column IN <source-column> ) AS U;
 
```  

## ***MS SQL Server Functions***
*** 

> ## MS SQL built-in CAST function - converts data type
>  **Prefix:** cast
```sql
 /*Write down  cast  and press Tab to insert snippet*/ 
 CAST(value AS dataTypeForConversion)
 
```  
> ## MS SQL built-in TRY_CAST function - converts data type. If it does not succeed it returns NULL.
>  **Prefix:** try_cast
```sql
 /*Write down  try_cast  and press Tab to insert snippet*/ 
 TRY_CAST(value AS dataTypeForConversion)
 
```  
> ## MS SQL built-in CONVERT function - converts data type
>  **Prefix:** convert
```sql
 /*Write down  convert  and press Tab to insert snippet*/ 
 CONVERT(dataTypeForConversion value)
 
```  
> ## MS SQL built-in TRY_CONVERT function - converts data type. If it does not succeed the function returns NULL.
>  **Prefix:** tryconvert
```sql
 /*Write down  tryconvert  and press Tab to insert snippet*/ 
 TRY_CONVERT(dataTypeForConversion value)
 
```  
> ## MS SQL built-in PARSE function - Returns the result of an expression, translated to the requested data type in SQL Server.
>  **Prefix:** parse
```sql
 /*Write down  parse  and press Tab to insert snippet*/ 
 PARSE(value AS dataTypeForConversion)
 
```  
> ## MS SQL built-in TRY_PARSE function - Returns the result of an expression, translated to the requested data type, or null if the cast fails in SQL Server. Use TRY_PARSE only for converting from string to date/time and number types.
>  **Prefix:** try_parse
```sql
 /*Write down  try_parse  and press Tab to insert snippet*/ 
 TRY_PARSE(value AS dataTypeForConversion)
 
```  
> ## MS SQL built-in DATEPART function - Returns an integer representing the specified datepart of the specified date. | Nondeterministic
>  **Prefix:** datepart  OR  dpart  
```sql
 /*Write down  datepart  OR  dpart    and press Tab to insert snippet*/ 
 DATEPART(1|year,quarter,month,dayofyear,day,week,weekday,hour,minute,second,millisecond,microsecond,nanosecond,tzoffset,iso_week| date)
 
```  
> ## MS SQL built-in DATENAME function - Returns a character string representing the specified datepart of the specified date. | Nondeterministic
>  **Prefix:** datename  OR  dname  
```sql
 /*Write down  datename  OR  dname    and press Tab to insert snippet*/ 
 DATENAME(1|year,quarter,month,dayofyear,day,week,weekday,hour,minute,second,millisecond,microsecond,nanosecond,tzoffset,iso_week| date)
 
```  
> ## MS SQL built-in DAY function - Returns an integer representing the day part of the specified date. | Deterministic
>  **Prefix:** day
```sql
 /*Write down  day  and press Tab to insert snippet*/ 
 DAY(date)
 
```  
> ## MS SQL built-in MONTH function - Returns an integer representing the month part of a specified date. | Deterministic
>  **Prefix:** month
```sql
 /*Write down  month  and press Tab to insert snippet*/ 
 MONTH(date)
 
```  
> ## MS SQL built-in YEAR function - Returns an integer representing the year part of a specified date. | Deterministic
>  **Prefix:** year
```sql
 /*Write down  year  and press Tab to insert snippet*/ 
 YEAR(date)
 
```  
> ## MS SQL built-in DATEFROMPARTS function - Returns a date value for the specified year, month, and day.
>  **Prefix:** datefromparts  OR  dfp  
```sql
 /*Write down  datefromparts  OR  dfp    and press Tab to insert snippet*/ 
 DATEFROMPARTS(year month day)
 
```  
> ## MS SQL built-in DATETIMEFROMPARTS function - Returns a datetime value for the specified date and time.
>  **Prefix:** datetimefromparts  OR  dtfp  
```sql
 /*Write down  datetimefromparts  OR  dtfp    and press Tab to insert snippet*/ 
 DATETIMEFROMPARTS(year month day hour minute seconds milliseconds)
 
```  
> ## MS SQL built-in DATETIME2FROMPARTS function - Returns a datetime2 value for the specified date and time, with the specified precision.
>  **Prefix:** datetime2fromparts  OR  dt2fp  
```sql
 /*Write down  datetime2fromparts  OR  dt2fp    and press Tab to insert snippet*/ 
 DATETIME2FROMPARTS(year month day hour minute seconds fractions precision)
 
```  
> ## MS SQL built-in DATETIMEOFFSETFROMPARTS function - Returns a datetimeoffset value for the specified date and time, with the specified offsets and precision.
>  **Prefix:** datetimeoffsetfromparts  OR  dtofp  
```sql
 /*Write down  datetimeoffsetfromparts  OR  dtofp    and press Tab to insert snippet*/ 
 DATETIMEOFFSETFROMPARTS(year month day hour minute seconds fractions hour_offset minute_offset 1precision)
 
```  
> ## MS SQL built-in SMALLDATETIMEFROMPARTS function - Returns a smalldatetime value for the specified date and time.
>  **Prefix:** smalldatetimefromparts  OR  sdtfp  
```sql
 /*Write down  smalldatetimefromparts  OR  sdtfp    and press Tab to insert snippet*/ 
 SMALLDATETIMEFROMPARTS(year month day hour minute)
 
```  
> ## MS SQL built-in TIMEFROMPARTS function - Returns a time value for the specified time, with the specified precision.
>  **Prefix:** timefromparts  OR  tfp  
```sql
 /*Write down  timefromparts  OR  tfp    and press Tab to insert snippet*/ 
 TIMEFROMPARTS(hour minute seconds fractions precision)
 
```  
> ## MS SQL built-in DATEDIFF function - Returns the number of date or time datepart boundaries, crossed between two specified dates. | Deterministic
>  **Prefix:** datediff  OR  dd  
```sql
 /*Write down  datediff  OR  dd    and press Tab to insert snippet*/ 
 DATEDIFF(1|year,quarter,month,dayofyear,day,week,hour,minute,second,millisecond,microsecond,nanosecond| startdate enddate)
 
```  
> ## MS SQL built-in DATEDIFF_BIG function - Returns the number of date or time datepart boundaries, crossed between two specified dates. | Deterministic
>  **Prefix:** datediff_big  OR  ddb  
```sql
 /*Write down  datediff_big  OR  ddb    and press Tab to insert snippet*/ 
 DATEDIFF_BIG(1|year,quarter,month,dayofyear,day,week,hour,minute,second,millisecond,microsecond,nanosecond| startdate enddate)
 
```  
> ## MS SQL built-in DATEADD function - Returns a new datetime value by adding an interval to the specified datepart of the specified date. | Deterministic
>  **Prefix:** dateadd  OR  dadd  
```sql
 /*Write down  dateadd  OR  dadd    and press Tab to insert snippet*/ 
 DATEADD(1|year,quarter,month,dayofyear,day,week,hour,minute,second,millisecond,microsecond,nanosecond| number date)
 
```  
> ## MS SQL built-in EOMONTH function - Returns the last day of the month containing the specified date, with an optional offset. | Deterministic
>  **Prefix:** eomonth  OR  eom  
```sql
 /*Write down  eomonth  OR  eom    and press Tab to insert snippet*/ 
 EOMONTH(start_date month_to_add)
 
```  
> ## MS SQL built-in SWITCHOFFSET function - SWITCHOFFSET changes the time zone offset of a DATETIMEOFFSET value, and preserves the UTC value. | Deterministic
>  **Prefix:** switchoffset  OR  soffset  
```sql
 /*Write down  switchoffset  OR  soffset    and press Tab to insert snippet*/ 
 SWITCHOFFSET(datetimeoffset_expression timezoneoffset_expression)
 
```  
> ## MS SQL built-in TODATETIMEOFFSET function - TODATETIMEOFFSET transforms a datetime2 value into a datetimeoffset value. TODATETIMEOFFSET interprets the datetime2 value in local time, for the specified time_zone. | Deterministic
>  **Prefix:** todatetimeoffset  OR  tdtoffset  
```sql
 /*Write down  todatetimeoffset  OR  tdtoffset    and press Tab to insert snippet*/ 
 TODATETIMEOFFSET(expression time_zone)
 
```  
> ## MS SQL built-in ISDATE function - Determines whether a datetime or smalldatetime input expression has a valid date or time value.
>  **Prefix:** isdate
```sql
 /*Write down  isdate  and press Tab to insert snippet*/ 
 ISDATE(expression)
 
```  
> ## MS SQL built-in DATALENGTH function - This function returns the number of bytes used to represent any expression.
>  **Prefix:** datalength  OR  datal  
```sql
 /*Write down  datalength  OR  datal    and press Tab to insert snippet*/ 
 DATALENGTH(expression)
 
```  
> ## MS SQL built-in ASCII function - Returns the ASCII code value of the leftmost character of a character expression.
>  **Prefix:** ascii
```sql
 /*Write down  ascii  and press Tab to insert snippet*/ 
 ASCII(expression)
 
```  
> ## MS SQL built-in CHAR function - Returns the single-byte character with the specified integer code, as defined by the character set and encoding of the default collation of the current database.
>  **Prefix:** char
```sql
 /*Write down  char  and press Tab to insert snippet*/ 
 CHAR(integer_expression)
 
```  
> ## MS SQL built-in CHARINDEX function - This function searches for one character expression inside a second character expression, returning the starting position of the first expression if found.
>  **Prefix:** charindex
```sql
 /*Write down  charindex  and press Tab to insert snippet*/ 
 CHARINDEX(expressionToFind expressionToSearch)
 
```  
> ## MS SQL built-in CONCAT function - This function returns a string resulting from the concatenation, or joining, of two or more string values in an end-to-end manner. (To add a separating value during concatenation, see CONCAT_WS.)
>  **Prefix:** concat  OR  conc  
```sql
 /*Write down  concat  OR  conc    and press Tab to insert snippet*/ 
 CONCAT(string_value1 string_valueN)
 
```  
> ## MS SQL built-in CONCAT_WS function - This function returns a string resulting from the concatenation, or joining, of two or more string values in an end-to-end manner. It separates those concatenated string values with the delimiter specified in the first function argument. (CONCAT_WS indicates concatenate with separator.)
>  **Prefix:** concat_ws  OR  concws  
```sql
 /*Write down  concat_ws  OR  concws    and press Tab to insert snippet*/ 
 CONCAT_WS(separator string_value1 string_valueN)
 
```  
> ## MS SQL built-in DIFFERENCE function - This function returns an integer value measuring the difference between the SOUNDEX() values of two different character expressions.
>  **Prefix:** difference
```sql
 /*Write down  difference  and press Tab to insert snippet*/ 
 DIFFERENCE(character_expression character_expression)
 
```  
> ## MS SQL built-in FORMAT function - Returns a value formatted with the specified format and optional culture. Use the FORMAT function for locale-aware formatting of date/time and number values as strings. For general data type conversions, use CAST or CONVERT.
>  **Prefix:** format
```sql
 /*Write down  format  and press Tab to insert snippet*/ 
 FORMAT(value format culture)
 
```  
> ## MS SQL built-in LEFT function - Returns the left part of a character string with the specified number of characters.
>  **Prefix:** left
```sql
 /*Write down  left  and press Tab to insert snippet*/ 
 LEFT(character_expression integer_expression)
 
```  
> ## MS SQL built-in LEN function - Returns the number of characters of the specified string expression, excluding trailing spaces.
>  **Prefix:** len
```sql
 /*Write down  len  and press Tab to insert snippet*/ 
 LEN(string_expression)
 
```  
> ## MS SQL built-in LOWER function - Returns a character expression after converting uppercase character data to lowercase.
>  **Prefix:** lower
```sql
 /*Write down  lower  and press Tab to insert snippet*/ 
 LOWER(character_expression)
 
```  
> ## MS SQL built-in LTRIM function - Returns a character expression after it removes leading blanks.
>  **Prefix:** ltrim
```sql
 /*Write down  ltrim  and press Tab to insert snippet*/ 
 LTRIM(character_expression)
 
```  
> ## MS SQL built-in NCHAR function - Returns the Unicode character with the specified integer code, as defined by the Unicode standard.
>  **Prefix:** nchar
```sql
 /*Write down  nchar  and press Tab to insert snippet*/ 
 NCHAR(integer_expression)
 
```  
> ## MS SQL built-in PATINDEX function - Returns the starting position of the first occurrence of a pattern in a specified expression, or zeros if the pattern is not found, on all valid text and character data types.
>  **Prefix:** patindex
```sql
 /*Write down  patindex  and press Tab to insert snippet*/ 
 PATINDEX('%integer_expression%' expression)
 
```  
> ## MS SQL built-in QUOTENAME function - Returns a Unicode string with the delimiters added to make the input string a valid SQL Server delimited identifier.
>  **Prefix:** quotename
```sql
 /*Write down  quotename  and press Tab to insert snippet*/ 
 QUOTENAME('character_string')
 
```  
> ## MS SQL built-in REPLACE function - Replaces all occurrences of a specified string value with another string value.
>  **Prefix:** replace
```sql
 /*Write down  replace  and press Tab to insert snippet*/ 
 REPLACE(string_expression string_pattern string_replacement)
 
```  
> ## MS SQL built-in REPLICATE function - Repeats a string value a specified number of times.
>  **Prefix:** replicate
```sql
 /*Write down  replicate  and press Tab to insert snippet*/ 
 REPLICATE(string_expression integer_expression)
 
```  
> ## MS SQL built-in REVERSE function - Returns the reverse order of a string value.
>  **Prefix:** reverse
```sql
 /*Write down  reverse  and press Tab to insert snippet*/ 
 REVERSE(string_expression)
 
```  
> ## MS SQL built-in RIGHT function - Returns the right part of a character string with the specified number of characters.
>  **Prefix:** right
```sql
 /*Write down  right  and press Tab to insert snippet*/ 
 RIGHT(character_expression integer_expression)
 
```  
> ## MS SQL built-in RTRIM function - Returns a character string after truncating all trailing spaces.
>  **Prefix:** rtrim
```sql
 /*Write down  rtrim  and press Tab to insert snippet*/ 
 RTRIM(character_expression)
 
```  
> ## MS SQL built-in SOUNDEX function - Returns a four-character (SOUNDEX) code to evaluate the similarity of two strings.
>  **Prefix:** soundex
```sql
 /*Write down  soundex  and press Tab to insert snippet*/ 
 SOUNDEX(character_expression)
 
```  
> ## MS SQL built-in SPACE function - Returns a string of repeated spaces.
>  **Prefix:** space
```sql
 /*Write down  space  and press Tab to insert snippet*/ 
 SPACE(integer_expression)
 
```  
> ## MS SQL built-in STR function - Returns character data converted from numeric data. The character data is right-justified, with a specified length and decimal precision.
>  **Prefix:** str
```sql
 /*Write down  str  and press Tab to insert snippet*/ 
 STR(float_expression length decimal)
 
```  
> ## MS SQL built-in STRING_AGG function - Concatenates the values of string expressions and places separator values between them. The separator isn't added at the end of string.
>  **Prefix:** string_agg
```sql
 /*Write down  string_agg  and press Tab to insert snippet*/ 
 STRING_AGG(expression separator) WITHIN GROUP ( ORDER BY order_by_expression_list 4|ASC,DESC| )
 
```  
> ## MS SQL built-in STRING_ESCAPE function - Escapes special characters in texts and returns text with escaped characters. STRING_ESCAPE is a deterministic function, introduced in SQL Server 2016.
>  **Prefix:** string_escape
```sql
 /*Write down  string_escape  and press Tab to insert snippet*/ 
 STRING_ESCAPE(text type)
 
```  
> ## MS SQL built-in STRING_SPLIT function - A table-valued function that splits a string into rows of substrings, based on a specified separator character.
>  **Prefix:** string_split
```sql
 /*Write down  string_split  and press Tab to insert snippet*/ 
 SELECT value 
FROM STRING_SPLIT(string separator);
 
```  
> ## MS SQL built-in STUFF function - The STUFF function inserts a string into another string. It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.
>  **Prefix:** stuff
```sql
 /*Write down  stuff  and press Tab to insert snippet*/ 
 STUFF(character_expression start length replaceWith_expression)
 
```  
> ## MS SQL built-in SUBSTRING function - Returns part of a character, binary, text, or image expression in SQL Server.
>  **Prefix:** substring
```sql
 /*Write down  substring  and press Tab to insert snippet*/ 
 SUBSTRING(expression start length)
 
```  
> ## MS SQL built-in TRANSLATE function - Returns the string provided as a first argument after some characters specified in the second argument are translated into a destination set of characters specified in the third argument.
>  **Prefix:** translate
```sql
 /*Write down  translate  and press Tab to insert snippet*/ 
 TRANSLATE(inputString characters translations)
 
```  
> ## MS SQL built-in TRIM function - Removes the space character char(32) or other specified characters from the start and end of a string.
>  **Prefix:** trim
```sql
 /*Write down  trim  and press Tab to insert snippet*/ 
 TRIM(string)
 
```  
> ## MS SQL built-in UNICODE function - Returns the integer value, as defined by the Unicode standard, for the first character of the input expression.
>  **Prefix:** unicode
```sql
 /*Write down  unicode  and press Tab to insert snippet*/ 
 UNICODE('ncharacter_expression')
 
```  
> ## MS SQL built-in UPPER function - Returns a character expression with lowercase character data converted to uppercase.
>  **Prefix:** upper
```sql
 /*Write down  upper  and press Tab to insert snippet*/ 
 UPPER(character_expression)
 
```  
> ## MS SQL built-in IIF function - Returns one of two values, depending on whether the Boolean expression evaluates to true or false in SQL Server.
>  **Prefix:** iif
```sql
 /*Write down  iif  and press Tab to insert snippet*/ 
 IIF(boolean_expression true_value false_value)
 
```  
> ## MS SQL built-in CHOOSE function - Returns the item at the specified index from a list of values in SQL Server.
>  **Prefix:** choose
```sql
 /*Write down  choose  and press Tab to insert snippet*/ 
 CHOOSE(index val_1 val_n)
 
```  
> ## MS SQL built-in ABS function - A mathematical function that returns the absolute (positive) value of the specified numeric expression. (ABS changes negative values to positive values. ABS has no effect on zero or positive values.)
>  **Prefix:** abs
```sql
 /*Write down  abs  and press Tab to insert snippet*/ 
 ABS(numeric_expression)
 
```  
> ## MS SQL built-in ACOS function - A function that returns the angle, in radians, whose cosine is the specified float expression. This is also called arccosine.
>  **Prefix:** acos
```sql
 /*Write down  acos  and press Tab to insert snippet*/ 
 ACOS(float_expression)
 
```  
> ## MS SQL built-in ASIN function - A function that returns the angle, in radians, whose sine is the specified float expression. This is also called arcsine.
>  **Prefix:** asin
```sql
 /*Write down  asin  and press Tab to insert snippet*/ 
 ASIN(float_expression)
 
```  
> ## MS SQL built-in ATAN function - A function that returns the angle, in radians, whose tangent is a specified float expression. This is also called arctangent.
>  **Prefix:** atan
```sql
 /*Write down  atan  and press Tab to insert snippet*/ 
 ATAN(float_expression)
 
```  
> ## MS SQL built-in ATN2 function - Returns the angle, in radians, between the positive x-axis and the ray from the origin to the point (y, x), where x and y are the values of the two specified float expressions.
>  **Prefix:** atan2
```sql
 /*Write down  atan2  and press Tab to insert snippet*/ 
 ATN2(float_expression float_expression)
 
```  
> ## MS SQL built-in CEILING function - This function returns the smallest integer greater than, or equal to, the specified numeric expression.
>  **Prefix:** ceiling
```sql
 /*Write down  ceiling  and press Tab to insert snippet*/ 
 CEILING(numeric_expression)
 
```  
> ## MS SQL built-in COS function - A mathematical function that returns the trigonometric cosine of the specified angle - measured in radians - in the specified expression.
>  **Prefix:** cos
```sql
 /*Write down  cos  and press Tab to insert snippet*/ 
 COS(float_expression)
 
```  
> ## MS SQL built-in COT function - A mathematical function that returns the trigonometric cotangent of the specified angle - in radians - in the specified float expression.
>  **Prefix:** cot
```sql
 /*Write down  cot  and press Tab to insert snippet*/ 
 COT(float_expression)
 
```  
> ## MS SQL built-in DEGREES function - This function returns the corresponding angle, in degrees, for an angle specified in radians.
>  **Prefix:** degrees
```sql
 /*Write down  degrees  and press Tab to insert snippet*/ 
 DEGREES(numeric_expression)
 
```  
> ## MS SQL built-in EXP function - Returns the exponential value of the specified float expression.
>  **Prefix:** exp
```sql
 /*Write down  exp  and press Tab to insert snippet*/ 
 EXP(float_expression)
 
```  
> ## MS SQL built-in FLOOR function - Returns the largest integer less than or equal to the specified numeric expression.
>  **Prefix:** floor
```sql
 /*Write down  floor  and press Tab to insert snippet*/ 
 FLOOR(numeric_expression)
 
```  
> ## MS SQL built-in LOG function - Returns the natural logarithm of the specified float expression in SQL Server.
>  **Prefix:** log
```sql
 /*Write down  log  and press Tab to insert snippet*/ 
 LOG(float_expression base)
 
```  
> ## MS SQL built-in LOG10 function - Returns the base-10 logarithm of the specified float expression.
>  **Prefix:** log10
```sql
 /*Write down  log10  and press Tab to insert snippet*/ 
 LOG10(float_expression)
 
```  
> ## MS SQL built-in POWER function - Returns the value of the specified expression to the specified power.
>  **Prefix:** power
```sql
 /*Write down  power  and press Tab to insert snippet*/ 
 POWER(float_expression y)
 
```  
> ## MS SQL built-in RADIANS function - Returns radians when a numeric expression, in degrees, is entered.
>  **Prefix:** radians
```sql
 /*Write down  radians  and press Tab to insert snippet*/ 
 RADIANS(numeric_expression)
 
```  
> ## MS SQL built-in RAND function - Returns a pseudo-random float value from 0 through 1, exclusive.
>  **Prefix:** randf
```sql
 /*Write down  randf  and press Tab to insert snippet*/ 
 RAND(seed)
 
```  
> ## MS SQL built-in ROUND function - Returns a numeric value, rounded to the specified length or precision.
>  **Prefix:** round
```sql
 /*Write down  round  and press Tab to insert snippet*/ 
 ROUND(seed length 3|tinyint,smallint,int|)
 
```  
> ## MS SQL built-in SIGN function - Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.
>  **Prefix:** sign
```sql
 /*Write down  sign  and press Tab to insert snippet*/ 
 SIGN(numeric_expression)
 
```  
> ## MS SQL built-in SIN function - Returns the trigonometric sine of the specified angle, in radians, and in an approximate numeric, float, expression.
>  **Prefix:** sin
```sql
 /*Write down  sin  and press Tab to insert snippet*/ 
 SIN(float_expression)
 
```  
> ## MS SQL built-in SQRT function - Returns the square root of the specified float value.
>  **Prefix:** sqrt
```sql
 /*Write down  sqrt  and press Tab to insert snippet*/ 
 SQRT(float_expression)
 
```  
> ## MS SQL built-in SQUARE function - Returns the square of the specified float value.
>  **Prefix:** square
```sql
 /*Write down  square  and press Tab to insert snippet*/ 
 SQUARE(float_expression)
 
```  
> ## MS SQL built-in TAN function - Returns the tangent of the input expression.
>  **Prefix:** tan
```sql
 /*Write down  tan  and press Tab to insert snippet*/ 
 TAN(float_expression)
 
```  
> ## MS SQL built-in ISJSON function - Tests whether a string contains valid JSON.
>  **Prefix:** isjson
```sql
 /*Write down  isjson  and press Tab to insert snippet*/ 
 ISJSON(expression)
 
```  
> ## MS SQL built-in JSON_VALUE function - Extracts a scalar value from a JSON string.
>  **Prefix:** json_value
```sql
 /*Write down  json_value  and press Tab to insert snippet*/ 
 JSON_VALUE(expression path)
 
```  
> ## MS SQL built-in JSON_QUERY function - Extracts an object or an array from a JSON string.
>  **Prefix:** json_query
```sql
 /*Write down  json_query  and press Tab to insert snippet*/ 
 JSON_QUERY(expression path)
 
```  
> ## MS SQL built-in JSON_MODIFY function - Updates the value of a property in a JSON string and returns the updated JSON string.
>  **Prefix:** json_modify
```sql
 /*Write down  json_modify  and press Tab to insert snippet*/ 
 JSON_MODIFY(expression path newValue)
 
```  
> ## MS SQL built-in APPROX_COUNT_DISTINCT function - This function returns the approximate number of unique non-null values in a group.
>  **Prefix:** approx_count_distinct
```sql
 /*Write down  approx_count_distinct  and press Tab to insert snippet*/ 
 APPROX_COUNT_DISTINCT(expression)
 
```  
> ## MS SQL built-in AVG function - This function returns the average of the values in a group. It ignores null values.
>  **Prefix:** avg
```sql
 /*Write down  avg  and press Tab to insert snippet*/ 
 AVG(expression)
 
```  
> ## MS SQL built-in CHECKSUM_AGG function - This function returns the checksum of the values in a group. CHECKSUM_AGG ignores null values. The OVER clause can follow CHECKSUM_AGG.
>  **Prefix:** checksum_agg
```sql
 /*Write down  checksum_agg  and press Tab to insert snippet*/ 
 CHECKSUM_AGG(expression)
 
```  
> ## MS SQL built-in COUNT function - This function returns the number of items found in a group. COUNT operates like the COUNT_BIG function. These functions differ only in the data types of their return values. COUNT always returns an int data type value. COUNT_BIG always returns a bigint data type value.
>  **Prefix:** count
```sql
 /*Write down  count  and press Tab to insert snippet*/ 
 COUNT(1|expression*|)
 
```  
> ## MS SQL built-in COUNT_BIG function - This function returns the number of items found in a group. COUNT_BIG operates like the COUNT function. These functions differ only in the data types of their return values. COUNT_BIG always returns a bigint data type value. COUNT always returns an int data type value.
>  **Prefix:** count_big
```sql
 /*Write down  count_big  and press Tab to insert snippet*/ 
 COUNT_BIG(1|expression*|)
 
```  
> ## MS SQL built-in GROUPING function - Indicates whether a specified column expression in a GROUP BY list is aggregated or not. GROUPING returns 1 for aggregated or 0 for not aggregated in the result set. GROUPING can be used only in the SELECT <select> list, HAVING, and ORDER BY clauses when GROUP BY is specified.
>  **Prefix:** grouping
```sql
 /*Write down  grouping  and press Tab to insert snippet*/ 
 GROUPING(column_expression)
 
```  
> ## MS SQL built-in GROUPING_ID function - Is a function that computes the level of grouping. GROUPING_ID can be used only in the SELECT <select> list, HAVING, or ORDER BY clauses when GROUP BY is specified.
>  **Prefix:** grouping_id
```sql
 /*Write down  grouping_id  and press Tab to insert snippet*/ 
 GROUPING_ID(column_expression)
 
```  
> ## MS SQL built-in MAX function - Returns the maximum value in the expression.
>  **Prefix:** max
```sql
 /*Write down  max  and press Tab to insert snippet*/ 
 MAX(expression)
 
```  
> ## MS SQL built-in MIN function - Returns the minimum value in the expression. May be followed by the OVER clause.
>  **Prefix:** min
```sql
 /*Write down  min  and press Tab to insert snippet*/ 
 MIN(expression)
 
```  
> ## MS SQL built-in STDEV function - Returns the statistical standard deviation of all values in the specified expression.
>  **Prefix:** stdev
```sql
 /*Write down  stdev  and press Tab to insert snippet*/ 
 STDEV(expression)
 
```  
> ## MS SQL built-in STDEVP function - Returns the statistical standard deviation for the population for all values in the specified expression.
>  **Prefix:** stdevp
```sql
 /*Write down  stdevp  and press Tab to insert snippet*/ 
 STDEVP(expression)
 
```  
> ## MS SQL built-in SUM function - Returns the sum of all the values, or only the DISTINCT values, in the expression. SUM can be used with numeric columns only. Null values are ignored.
>  **Prefix:** sum
```sql
 /*Write down  sum  and press Tab to insert snippet*/ 
 SUM(expression)
 
```  
> ## MS SQL built-in VAR function - Returns the statistical variance of all values in the specified expression. May be followed by the OVER clause.
>  **Prefix:** var
```sql
 /*Write down  var  and press Tab to insert snippet*/ 
 VAR(expression)
 
```  
> ## MS SQL built-in VARP function - Returns the statistical variance for the population for all values in the specified expression.
>  **Prefix:** varp
```sql
 /*Write down  varp  and press Tab to insert snippet*/ 
 VARP(expression)
```  


## ***Condition Logic***
*** 


> ## CASE expression WHEN
>  **Prefix:** case  OR  cw  
```sql
 /*Write down  case  OR  cw    and press Tab to insert snippet*/ 
 CASE value
	WHEN firstCase THEN IfFirstCaseValue  
	WHEN N-thCase THEN IfN-thCaseValue 
ELSE ElseCaseValue
END
 
```  
> ## IF operator
>  **Prefix:** if
```sql
 /*Write down  if  and press Tab to insert snippet*/ 
 if (condition)
BEGIN
	bodyOfIf
END
 
```  
> ## IF-ELSE operator
>  **Prefix:** ife
```sql
 /*Write down  ife  and press Tab to insert snippet*/ 
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
 /*Write down  ifeif  and press Tab to insert snippet*/ 
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
 /*Write down  ifex  and press Tab to insert snippet*/ 
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
 /*Write down  ifnex  and press Tab to insert snippet*/ 
 if not exists( SELECT * 
			FROM tableName
			WHERE whereClause )
BEGIN
	bodyOfIf
END
 
```  

## ***Variable Declarations***
*** 

> ## Declares a BIGINT variable WITH DECLARE
>  **Prefix:** decbi
```sql
 /*Write down  decbi  and press Tab to insert snippet*/ 
 DECLARE @p_varName BIGINT 
 
```  
> ## Declares a BIGINT variable
>  **Prefix:** @pbi
```sql
 /*Write down  @pbi  and press Tab to insert snippet*/ 
 @p_varName BIGINT, 
 
```  
> ## Declares an INT variable WITH DECLARE
>  **Prefix:** deci
```sql
 /*Write down  deci  and press Tab to insert snippet*/ 
 DECLARE @p_varName INT 
 
```  
> ## Declares an INT variable
>  **Prefix:** @pi
```sql
 /*Write down  @pi  and press Tab to insert snippet*/ 
 @p_varName INT, 
 
```  
> ## Declares a SMALLINT variable WITH DECLARE
>  **Prefix:** decsi
```sql
 /*Write down  decsi  and press Tab to insert snippet*/ 
 DECLARE @p_varName SMALLINT 
 
```  
> ## Declares a SMALLINT variable
>  **Prefix:** @psi
```sql
 /*Write down  @psi  and press Tab to insert snippet*/ 
 @p_varName SMALLINT, 
 
```  
> ## Declares a TINYINT variable WITH DECLARE
>  **Prefix:** decti
```sql
 /*Write down  decti  and press Tab to insert snippet*/ 
 DECLARE @p_varName TINYINT 
 
```  
> ## Declares a TINYINT variable
>  **Prefix:** @pti
```sql
 /*Write down  @pti  and press Tab to insert snippet*/ 
 @p_varName TINYINT, 
 
```  
> ## Declares a DECIMAL variable WITH DECLARE
>  **Prefix:** decdec
```sql
 /*Write down  decdec  and press Tab to insert snippet*/ 
 DECLARE @p_varName DECIMAL(precision scale) 
 
```  
> ## Declares a DECIMAL variable
>  **Prefix:** @pdec
```sql
 /*Write down  @pdec  and press Tab to insert snippet*/ 
 @p_varName DECIMAL(precision scale), 
 
```  
> ## Declares a MONEY variable WITH DECLARE
>  **Prefix:** decm
```sql
 /*Write down  decm  and press Tab to insert snippet*/ 
 DECLARE @p_varName MONEY 
 
```  
> ## Declares a MONEY variable
>  **Prefix:** @pm
```sql
 /*Write down  @pm  and press Tab to insert snippet*/ 
 @p_varName MONEY, 
 
```  
> ## Declares a SMALLMONEY variable WITH DECLARE
>  **Prefix:** decsm
```sql
 /*Write down  decsm  and press Tab to insert snippet*/ 
 DECLARE @p_varName SMALLMONEY 
 
```  
> ## Declares a SMALLMONEY variable
>  **Prefix:** @psm
```sql
 /*Write down  @psm  and press Tab to insert snippet*/ 
 @p_varName SMALLMONEY, 
 
```  
> ## Declares a BIT variable WITH DECLARE
>  **Prefix:** decb
```sql
 /*Write down  decb  and press Tab to insert snippet*/ 
 DECLARE @p_varName BIT 
 
```  
> ## Declares a BIT variable
>  **Prefix:** @pb
```sql
 /*Write down  @pb  and press Tab to insert snippet*/ 
 @p_varName BIT, 
 
```  
> ## Declares a FLOAT variable WITH DECLARE
>  **Prefix:** decf
```sql
 /*Write down  decf  and press Tab to insert snippet*/ 
 DECLARE @p_varName FLOAT(precision) 
 
```  
> ## Declares a FLOAT variable
>  **Prefix:** @pf
```sql
 /*Write down  @pf  and press Tab to insert snippet*/ 
 @p_varName FLOAT(precision), 
 
```  
> ## Declares a REAL variable WITH DECLARE
>  **Prefix:** decr
```sql
 /*Write down  decr  and press Tab to insert snippet*/ 
 DECLARE @p_varName REAL 
 
```  
> ## Declares a REAL variable
>  **Prefix:** @pr
```sql
 /*Write down  @pr  and press Tab to insert snippet*/ 
 @p_varName REAL, 
 
```  
> ## Declares a DATE variable WITH DECLARE
>  **Prefix:** decd
```sql
 /*Write down  decd  and press Tab to insert snippet*/ 
 DECLARE @p_varNamdatee DATE 
 
```  
> ## Declares a DATE variable
>  **Prefix:** @pd
```sql
 /*Write down  @pd  and press Tab to insert snippet*/ 
 @p_varName DATE, 
 
```  
> ## Declares a DATETIME variable WITH DECLARE
>  **Prefix:** decdt
```sql
 /*Write down  decdt  and press Tab to insert snippet*/ 
 DECLARE @p_varName DATETIME 
 
```  
> ## Declares a DATETIME variable
>  **Prefix:** @pdt
```sql
 /*Write down  @pdt  and press Tab to insert snippet*/ 
 @p_varName DATETIME, 
 
```  
> ## Declares a SMALLDATETIME variable WITH DECLARE
>  **Prefix:** decsmdt
```sql
 /*Write down  decsmdt  and press Tab to insert snippet*/ 
 DECLARE @p_varName SMALLDATETIME 
 
```  
> ## Declares a SMALLDATETIME variable
>  **Prefix:** @psmdt
```sql
 /*Write down  @psmdt  and press Tab to insert snippet*/ 
 @p_varName SMALLDATETIME, 
 
```  
> ## Declares a DATETIME2 variable WITH DECLARE
>  **Prefix:** decdt2
```sql
 /*Write down  decdt2  and press Tab to insert snippet*/ 
 DECLARE @p_varName DATETIME2 
 
```  
> ## Declares a DATETIME2 variable
>  **Prefix:** @pdt2
```sql
 /*Write down  @pdt2  and press Tab to insert snippet*/ 
 @p_varName DATETIME2, 
 
```  
> ## Declares a TIME variable WITH DECLARE
>  **Prefix:** dect
```sql
 /*Write down  dect  and press Tab to insert snippet*/ 
 DECLARE @p_varName TIME(fractionalSecondScale)) 
 
```  
> ## Declares a TIME variable
>  **Prefix:** @pt
```sql
 /*Write down  @pt  and press Tab to insert snippet*/ 
 @p_varName TIME(fractionalSecondScale)), 
 
```  
> ## Declares a DATETIMEOFFSET variable WITH DECLARE
>  **Prefix:** decdto
```sql
 /*Write down  decdto  and press Tab to insert snippet*/ 
 DECLARE @p_varName DATETIMEOFFSET(fractionalSecondScale)) 
 
```  
> ## Declares a DATETIMEOFFSET variable
>  **Prefix:** @pdto
```sql
 /*Write down  @pdto  and press Tab to insert snippet*/ 
 @p_varName DATETIMEOFFSET(fractionalSecondScale)), 
 
```  
> ## Declares a CHAR variable WITH DECLARE
>  **Prefix:** decc
```sql
 /*Write down  decc  and press Tab to insert snippet*/ 
 DECLARE @p_varName CHAR(varSize) 
 
```  
> ## Declares a CHAR variable
>  **Prefix:** @pc
```sql
 /*Write down  @pc  and press Tab to insert snippet*/ 
 @p_varName CHAR(varSize), 
 
```  
> ## Declares a NCHAR variable WITH DECLARE
>  **Prefix:** decnc
```sql
 /*Write down  decnc  and press Tab to insert snippet*/ 
 DECLARE @p_varName NCHAR(varSize) 
 
```  
> ## Declares a NCHAR variable
>  **Prefix:** @pnc
```sql
 /*Write down  @pnc  and press Tab to insert snippet*/ 
 @p_varName NCHAR(varSize), 
 
```  
> ## Declares a VARCHAR variable WITH DECLARE
>  **Prefix:** decv
```sql
 /*Write down  decv  and press Tab to insert snippet*/ 
 DECLARE @p_varName VARCHAR(varSize) 
 
```  
> ## Declares a VARCHAR variable
>  **Prefix:** @pv
```sql
 /*Write down  @pv  and press Tab to insert snippet*/ 
 @p_varName VARCHAR(varSize), 
 
```  
> ## Declares a NVARCHAR variable WITH DECLARE
>  **Prefix:** decnv
```sql
 /*Write down  decnv  and press Tab to insert snippet*/ 
 DECLARE @p_varName NVARCHAR(varSize) 
 
```  
> ## Declares a NVARCHAR variable
>  **Prefix:** @pnv
```sql
 /*Write down  @pnv  and press Tab to insert snippet*/ 
 @p_varName NVARCHAR(varSize), 
 
```  
> ## Declares a BINARY variable WITH DECLARE
>  **Prefix:** decbin
```sql
 /*Write down  decbin  and press Tab to insert snippet*/ 
 DECLARE @p_varName BINARY(varSize) 
 
```  
> ## Declares a BINARY variable
>  **Prefix:** @pbin
```sql
 /*Write down  @pbin  and press Tab to insert snippet*/ 
 @p_varName BINARY(varSize), 
 
```  
> ## Declares a VARBINARY variable WITH DECLARE
>  **Prefix:** decvbin
```sql
 /*Write down  decvbin  and press Tab to insert snippet*/ 
 DECLARE @p_varName VARBINARY(varSize) 
 
```  
> ## Declares a VARBINARY variable
>  **Prefix:** @pvbin
```sql
 /*Write down  @pvbin  and press Tab to insert snippet*/ 
 @p_varName VARBINARY(varSize), 
 
```  
> ## Declares a SQL_VARIANT variable WITH DECLARE
>  **Prefix:** decsqlv
```sql
 /*Write down  decsqlv  and press Tab to insert snippet*/ 
 DECLARE @p_varName SQL_VARIANT 
 
```  
> ## Declares a SQL_VARIANT variable
>  **Prefix:** @psqlv
```sql
 /*Write down  @psqlv  and press Tab to insert snippet*/ 
 @p_varName SQL_VARIANT, 
 
```  
> ## Declares a XML variable WITH DECLARE
>  **Prefix:** decxml
```sql
 /*Write down  decxml  and press Tab to insert snippet*/ 
 DECLARE @p_varName XML 
 
```  
> ## Declares a XML variable
>  **Prefix:** @pxml
```sql
 /*Write down  @pxml  and press Tab to insert snippet*/ 
 @p_varName XML, 
 
```  
> ## Declares a UNIQUEIDENTIFIER variable WITH DECLARE
>  **Prefix:** decuniqi
```sql
 /*Write down  decuniqi  and press Tab to insert snippet*/ 
 DECLARE @p_varName UNIQUEIDENTIFIER = NEWID();
 
```  
> ## Declares a UNIQUEIDENTIFIER variable
>  **Prefix:** @puniqi
```sql
 /*Write down  @puniqi  and press Tab to insert snippet*/ 
 @p_varName UNIQUEIDENTIFIER, 
 
```  
> ## Declares a GEOGRAPHY variable WITH DECLARE
>  **Prefix:** decgeo
```sql
 /*Write down  decgeo  and press Tab to insert snippet*/ 
 DECLARE @p_varName GEOGRAPHY 
 
```  
> ## Declares a GEOGRAPHY variable
>  **Prefix:** @pgeo
```sql
 /*Write down  @pgeo  and press Tab to insert snippet*/ 
 @p_varName GEOGRAPHY, 
 
```  
> ## Declares a GEOMETRY variable WITH DECLARE
>  **Prefix:** decgeom
```sql
 /*Write down  decgeom  and press Tab to insert snippet*/ 
 DECLARE @p_varName GEOMETRY 
 
```  
> ## Declares a GEOMETRY variable
>  **Prefix:** @pgeom
```sql
 /*Write down  @pgeom  and press Tab to insert snippet*/ 
 @p_varName GEOMETRY, 
 
```  
> ## Declares a TABLE variable WITH DECLARE
>  **Prefix:** dectable
```sql
 /*Write down  dectable  and press Tab to insert snippet*/ 
 DECLARE @p_varName TABLE(col1 col1DataType col2 col2DataType)
 
```  
> ## Declares a TABLE variable
>  **Prefix:** @ptable
```sql
 /*Write down  @ptable  and press Tab to insert snippet*/ 
 @p_varName TABLE(col1 col1DataType col2 col2DataType), 
 
```  


## ***Data Definition Language***
*** 


> ## Adds column to table
>  **Prefix:** addc  OR  add.column  OR  addco  
```sql
 /*Write down  addc  OR  add.column  OR  addco    and press Tab to insert snippet*/ 
 ALTER TABLE tableName ADD colName dataType 4|NULL,NOT NULL|;
 
```  
> ## Drops column table
>  **Prefix:** alterc  OR  altercolumn  OR  alterco  
```sql
 /*Write down  alterc  OR  altercolumn  OR  alterco    and press Tab to insert snippet*/ 
 ALTER TABLE tableName ALTER COLUMN colName dataType 4|NULL,NOT NULL|;
 
```  
> ## Drops column table
>  **Prefix:** dropc  OR  dropcolumn  OR  dropco  
```sql
 /*Write down  dropc  OR  dropcolumn  OR  dropco    and press Tab to insert snippet*/ 
 ALTER TABLE tableName DROP COLUMN colName;
 
```  
> ## Creates a CLUSTERED INDEX on table
>  **Prefix:** cci  OR  clustindex  OR  create.clusteredindex  
```sql
 /*Write down  cci  OR  clustindex  OR  create.clusteredindex    and press Tab to insert snippet*/ 
 CREATE CLUSTERED INDEX indexName ON tableName(columnName);
 
```  
> ## Creates an UNIQUE CLUSTERED INDEX on table
>  **Prefix:** cuci  OR  uniqueclustindex  OR  create.uniqueclusteredindex  
```sql
 /*Write down  cuci  OR  uniqueclustindex  OR  create.uniqueclusteredindex    and press Tab to insert snippet*/ 
 CREATE UNIQUE CLUSTERED INDEX indexName ON tableName(columnName);
 
```  
> ## Creates an UNIQUE CLUSTERED INDEX on table
>  **Prefix:** cnci  OR  nonclustindex  OR  create.nonclusteredindex  
```sql
 /*Write down  cnci  OR  nonclustindex  OR  create.nonclusteredindex    and press Tab to insert snippet*/ 
 CREATE NONCLUSTERED INDEX indexName ON tableName(columnName);
 
```  
> ## DROPS an INDEX on table
>  **Prefix:** di  OR  drop.index  
```sql
 /*Write down  di  OR  drop.index    and press Tab to insert snippet*/ 
 DROP INDEX indexName ON tableName;
 
```  
> ## ADDS PRIMARY KEY to CREATE TABLE STATEMENT
>  **Prefix:** pk  OR  primarykey  
```sql
 /*Write down  pk  OR  primarykey    and press Tab to insert snippet*/ 
 CONSTRAINT PK_primaryKeyName PRIMARY KEY CLUSTERED (columnName) 
 
```  
> ## ADDS FOREIGN KEY to CREATE TABLE STATEMENT
>  **Prefix:** fk  OR  foreignkey  
```sql
 /*Write down  fk  OR  foreignkey    and press Tab to insert snippet*/ 
 CONSTRAINT FK_primaryKeyName FOREIGN KEY (columnName) 
	REFERENCES referencedTable (columnInReferencedTable)
 
```  
> ## ADDS PRIMARY KEY to an existing TABLE
>  **Prefix:** addpk  OR  add.primarykey  
```sql
 /*Write down  addpk  OR  add.primarykey    and press Tab to insert snippet*/ 
 USE DatabaseName

ALTER TABLE tableName
ADD CONSTRAINT PK_primaryKeyName PRIMARY KEY CLUSTERED (columnName);
 
```  
> ## ADDS FOREIGN KEY to an existing TABLE
>  **Prefix:** addfk  OR  add.foreignkey  
```sql
 /*Write down  addfk  OR  add.foreignkey    and press Tab to insert snippet*/ 
 USE DatabaseName

ALTER TABLE tableName
ADD CONSTRAINT FK_primaryKeyName FOREIGN KEY (columnName)
	REFERENCES referencedTable (columnInReferencedTable); 
 
```  
> ## DROP CONSTRAINT of an existing TABLE
>  **Prefix:** dc  OR  drop.constraint  
```sql
 /*Write down  dc  OR  drop.constraint    and press Tab to insert snippet*/ 
 USE DatabaseName

ALTER TABLE tableName
DROP CONSTRAINT primaryKeyName ;
 
```  
> ## CREATES a new TABLE
>  **Prefix:** ct  OR  create.table  
```sql
 /*Write down  ct  OR  create.table    and press Tab to insert snippet*/ 
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


## ***Create PROCEDURES, FUNCTIONS, VIEWS***
*** 

> ## CREATES a view 
>  **Prefix:** cv  OR  create.view  
```sql
 /*Write down  cv  OR  create.view    and press Tab to insert snippet*/ 
 USE DatabaseName

CREATE VIEW viewName
AS
	SELECT * 
	FROM tableName
	WHERE whereClause ;
GO
 
```  
> ## ALTERES a view 
>  **Prefix:** av  OR  alter.view  
```sql
 /*Write down  av  OR  alter.view    and press Tab to insert snippet*/ 
 USE DatabaseName

ALTER VIEW viewName
AS
	SELECT * 
	FROM tableName
	WHERE whereClause ;
GO
 
```  
> ## DROPS a view 
>  **Prefix:** dv  OR  drop.view  
```sql
 /*Write down  dv  OR  drop.view    and press Tab to insert snippet*/ 
 USE DatabaseName

DROP VIEW IF EXISTS viewName 
 
```  
> ## CREATES an inline table function 
>  **Prefix:** cif  OR  create.inlinefunction  
```sql
 /*Write down  cif  OR  create.inlinefunction    and press Tab to insert snippet*/ 
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
>  **Prefix:** csf  OR  create.scalarfunction  
```sql
 /*Write down  csf  OR  create.scalarfunction    and press Tab to insert snippet*/ 
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
>  **Prefix:** cmtvf  OR  create.multistatementfunction  
```sql
 /*Write down  cmtvf  OR  create.multistatementfunction    and press Tab to insert snippet*/ 
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
>  **Prefix:** aif  OR  alter.inlinefunction  
```sql
 /*Write down  aif  OR  alter.inlinefunction    and press Tab to insert snippet*/ 
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
>  **Prefix:** df  OR  drop.function  
```sql
 /*Write down  df  OR  drop.function    and press Tab to insert snippet*/ 
 USE DatabaseName

DROP FUNCTION IF EXISTS functionName ;
 
```  
> ## Creates basic body of procedure
>  **Prefix:** createproc  OR  create.procedure  OR  cproc  
```sql
 /*Write down  createproc  OR  create.procedure  OR  cproc    and press Tab to insert snippet*/ 
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
>  **Prefix:** dp  OR  drop.procedure  OR  dproc  
```sql
 /*Write down  dp  OR  drop.procedure  OR  dproc    and press Tab to insert snippet*/ 
 USE DatabaseName

DROP PROCEDURE procedureName ;
GO
 
```  

## ***Useful Scripts***
*** 

> ## Inserts `6 random Base-10 digits number` 
>  **Prefix:** random  OR  r  
```sql
 /*Write down  random  OR  r    and press Tab to insert snippet*/ 
 RANDOM
 
```  
> ## Inserts Block with Comments  
>  **Prefix:** bc  OR  blockcomment  
```sql
 /*Write down  bc  OR  blockcomment    and press Tab to insert snippet*/ 
 BLOCK_COMMENT_START
	yourCommentHere
BLOCK_COMMENT_END
 
```  
> ## Inserts Line Comments // 
>  **Prefix:** lc  OR  linecomment  
```sql
 /*Write down  lc  OR  linecomment    and press Tab to insert snippet*/ 
 LINE_COMMENT  yourCommentHere
 
```  
> ## Inserts current date 
>  **Prefix:** today  OR  currentdate  OR  currd  
```sql
 /*Write down  today  OR  currentdate  OR  currd    and press Tab to insert snippet*/ 
 'CURRENT_YEARCURRENT_MONTHCURRENT_DATE'
 
```  
> ## Inserts current datetime 
>  **Prefix:** now  OR  currentdatetime  OR  currdt  
```sql
 /*Write down  now  OR  currentdatetime  OR  currdt    and press Tab to insert snippet*/ 
 'CURRENT_YEARCURRENT_MONTHCURRENT_DATE CURRENT_HOUR:CURRENT_MINUTE:CURRENT_SECOND'
 
```  
> ## Inserts UNIX timestamp 
>  **Prefix:** unix  
```sql
 /*Write down  unix    and press Tab to insert snippet*/ 
 'CURRENT_SECONDS_UNIX'
 
```  
> ## TRY CATCH 
>  **Prefix:** try  OR  trycatch  OR  catch  OR  tc  
```sql
 /*Write down  try  OR  trycatch  OR  catch  OR  tc    and press Tab to insert snippet*/ 
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

> ## Insert delay of execution of batch or procedure 
>  **Prefix:** delay  OR  waitfor  OR  wait  
```sql
 /*Write down  delay  OR  waitfor  OR  wait    and press Tab to insert snippet*/ 
 WAITFOR DELAY 'hoursminutesseconds' ;
 
```  
> ## Begins transaction 
>  **Prefix:** tran  OR  transaction  OR  begin.transaction  OR  begin.tran  
```sql
 /*Write down  tran  OR  transaction  OR  begin.transaction  OR  begin.tran    and press Tab to insert snippet*/ 
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
>  **Prefix:** dsql  OR  dynamic  OR  dynamicsql  
```sql
 /*Write down  dsql  OR  dynamic  OR  dynamicsql    and press Tab to insert snippet*/ 
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



## Known Issues

Currently there are no known issues.

## Release Notes

### 0.2.0

Update documentation
    
### 0.0.1

First release of extension
    
## License

[MIT](LICENSE.txt)

**Enjoy!**,  
**[M. Eng. R. Batinov](https://radoslav-batinov.bss.design/)**
