# JSON Snippet File Converter /to .md file with block of codes/

Това е разширение за VS Code, което може да конвертира фрагменти от JSON файл към документация в .md формат.

Може да намери приложение на разработчици на разширения за VS Code фрагменти. 
Това разширение ще помогне на всеки, който иска автоматизирано да генерира документация с префикси и техните фрагменти. 

![Демо на разширението](./images/demo.gif)

## Характеристики

- Конвертира JSON файл с фрагменти в .md файл.
- Визуализира префиксите и фрагментите, асоциирани с тях, в блокове, форматирани на съответния програмен език. 
- Коментари могат да бъдат използвани - разширението ги пропуска при конвертиране. 
- Използвай `description property`, за да може да бъде генерирано заглавие за фрагмента в документацията. 
- За един фрагмент са позволени няколко префикса.  - в документацията ще се покажат като `prefix 1 ИЛИ prefix 2 ИЛИ prefix N`.
- В `body property` се съхранява фрагмента на кода.

## Изисквания

- Трябва Ви инсталиран VS Code и това разширение, разбира се.
- За правилна визуализация на блока с код, то името на файлът трябва да бъде с името на програмния език -> `languageName.json`

> Например `sql.json` ще се визуализира така:  

```sql
SELECT *   
FROM table;
```  
  
> `html.json` ще се визуализира така:

```html
<div>
    <p>Hello World</p>
</div>
```  


## Как да използваме

1. Инсталиране на разширението: 
    - от [Marketplace](https://marketplace.visualstudio.com/items?itemName=MEngRBatinov.json-snippet-to-md-documentation&ssr=false#overview).  
    ![Как изглежда разширението в Marketplace](./images/extension-marketplace.png)  
    - от VS Code
        1. Отворете VS Code.
        2. Изберете `Extensions` от левия панел или изберете клавишна комбинация `Ctrl + Shift + X`.
        3. Напишете `json-snippet-to-md-documentation`. Разширението с име `JSON Snippets file to beautiful .MD file Documentation` ще се покаже.   
        ![Разширението в търсачката на VS Code](./images/extension-search.png)  
        4. Може да разгледате информация за разширението като кликнете върху него.  
        ![Как изглежда разширението във VS Code](./images/extension-overview.png)  
        5. Изберете `Install` и разширението ще се инсталира.

2. Отворете snippet.json файлът.  
3. Въведете клавишна комбинация `Ctrl + Shift + P` и напишете:

* `export to .md file documentation`  
Изберете командата и нов .md файл със конвертираното съдържание ще се покаже.

4. Ако желаете да промените настройките по подразбиране:
    1. Отидете на `VS Code Settings`
        - File > Preferences > Settings
    2. Изберете `User Tab`
    3. Разгърнете `Extensions Section` 
    4. Изберете `JSON Snippets Configurations`
    5. Списък с опции ще се зареди /в *italics* са визуализирани настройките по подразбиране, които могат да бъдат променени/:
        - `Multiple Prefixes Delimiter`
            - Ако някой фрагмент има повече от един префикса, то това е параметърът разделител, който ще се визуализира в документацията.
                > ## select-statement
                >  **Prefix:** sel OR select
                
                > ### Multiple Prefixes Delimiter
                >
                >   Delimiter for multiple Prefixes
                >
                >   *OR*       
        - `Code Block Comment Message /before Prefixes/`
            - Това е първият ред от блока с команди, в който е вграден коментар, описващ префиксите. 
                ```sql
                 /*Write down sel OR select OR s and press Tab to insert snippet*/ 
                ```
                > ### Code Block Message Start 
                >
                >   Code Block Comment Message /before Prefixes/
                >
                >   *Write down*       
        - `Code Block Comment Message /after Prefixes/`
            - Това е първият ред от блока с команди, в който е вграден коментар, описващ префиксите. 
                ```sql
                 /*Write down sel OR select OR s and press Tab to insert snippet*/ 
                ```
                > ### Code Block Message End 
                >
                >   Code Block Comment Message /after Prefixes/
                >
                >   *and press Tab to insert snippet*

        - `File Header Name with H1 heading`
            - Това е заглавието на документацията в новоъздадения .md файл.
                # JSON Snippets to MD File

                > ### MDHeader 
                >   
                >   File Header Name with H1 heading
                >
                >   *JSON Snippets to MD File*

        - `File Description`
            - Това е кратко описание на документацията в новосъзадения .md файл.
                # JSON Snippets to MD File
                This is a simple documentation of prefixes with their associated snippets.

                > ### MDdescription
                >
                >   File Description
                >
                >   *This is a simple documentation of prefixes with their associated snippets.*



## Проблеми

За сега няма открити проблеми.

## Версии

### 0.4.0

Промяна на логото

### 0.0.1

Публикуване на разширението
    
## Лиценз

[MIT](LICENSE.txt)

**Enjoy!**,  
**[Маг. Инж. Р. Батинов](https://radoslav-batinov.bss.design/)**
