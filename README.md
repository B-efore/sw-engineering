# GitHub Flavored Markdown Spec

#### 강의 : 소프트웨어공학
#### 학부 : 컴퓨터학부
#### 학번 및 이름 : 20202914 이지원

---

## Tables
- **How to** : Use `|` to divide the columns and `-` for the header of each column.
- **Note** : Don't need to match length and trailing pipes may be inconsisetent.

        | Header 1 | Header 2 |
        | -------- | ------ |
        | cell | cell |
        | cell | cell |
        
        or
        
        Header 1 | Header 2
        -------- | ------
        cell | cell
        cell | cell

    *Result :*
    
    Header 1 | Header 2
    -------- | ------
    cell | cell
    cell | cell
 
 <br>

- **Plus 1** : Use `:` to the left, right, or both sides of the `-` to align.

        | Header 1 | Header 2 | Header 3 |
        | :-- | :--: | --: |
        |left | middle | right |

    *Result :*

     | Header 1 | Header 2 | Header 3 |
     | :-- | :--: | --: |
     |left | middle | right |
     
 <br>

- **Plus 2** : Use `\` to include a pipe in the cell.

        | Header 1 |
        | -------- |
        | \| pipe  |
        
    *Result :*
    
    | Header 1 |
    | -------- |
    | \| pipe  |
    
 <br>
 
- **Plus 3** : The table can be finished with **the beginning of the first empty line** or **another block-level structures**.

        | Header 1 | Header 2 |
        | -------- | ------ |
        | cell | cell |
        | cell | cell |
        
        **end**
        
        and
        
        | Header 1 | Header 2 |
        | -------- | ------ |
        | cell | cell |
        | cell | cell |
        >**end**

    *Result :*
    
    
    | Header 1 | Header 2 |
    | -------- | ------ |
    | cell | cell |
    | cell | cell |
        
    **end**
        
    and
        
    | Header 1 | Header 2 |
    | -------- | ------ |
    | cell | cell |
    | cell | cell |
    >**end**

<br>

- **Plus 4** : The header row **must match** the delimiter row in the number of cells.

        | Header 1 | Header 2 |
        | -------- |
        | cell     |
        
        or
        
        | Header 1 |
        | -------- | -------- |
        | cell     |          |
        
    *Result :*
   
    | Header 1 | Header 2 |
    | -------- |
    | cell     |
        
    or
        
    | Header 1 |
    | -------- | -------- |
    | cell     |          |
    
    *This is **not recognized** as a table.*
    
<br>

- **Plus 5** : If the number of cells is **fewer** than the number of header, *an empty cells are inserted*, and if it is **greater**, *the excess is ignored*.

        | Header 1 | Header 2 |
        | -------- | -------- |
        | cell     |
        | cell     | cell     | ignored |
    
   *Result :*
   
   | Header 1 | Header 2 |
   | -------- | -------- |
   | cell     |
   | cell     | cell     | ignored |
   
---

## Task list items

 - **How to** : Form is `- [ ] list` and checkbox is `- [x] list`.
 - **Note** : Don't forget **a whitespace** between the list and brackets.
 
        - [x] first
        - [ ] second
             - [x] 1
             - [ ] 2
        - [ ] Third

    *Result :*
    
   - [x] first
   - [ ] second
        - [x] 1
        - [ ] 2
   - [ ] Third

## Strikethrough

- **How to** : Wrap the text with `~~`.
- **Note** : It *cannot be used continuously with a new paragraph.*

        I want to draw a line on ~~this~~.
        
        I want to draw a line on ~~here
        
        and here~~.
        
    *Result :*
    
    I want to draw a line on ~~this~~.
    
    I want to draw a line on ~~here

    and here~~.
 
## Autolinks

- **How to 1** : URL will be automatically converted into a link. When the text **http://** or **https://** is found followed by **a valid domain**.
- **How to 2** : WWW link will be automatically converted into a link. When the text **www** is found followed by **a valid domain**.
- **Note 1** : **Trailing punctuation** will *not be considered part of the autolink*.
- **Note 2** : Using `<` means the **end of the autolink**.


        http://myclass.ssu.ac.kr/
        www.naver.com
        
    
     *Result :*
     
     http://myclass.ssu.ac.kr/  
     www.naver.com  

<br>

- **How to 3** : Email link will be automatically converted into a link.
    - Include characters (Alphanumeric, or `.`, `-`, `_`, or `+`).
    - An `@` symbol.
    - Include characters (Alphanumeric, or `-` or `_`, seperated by `.`) and there must be at least one `.` and last character must not be `-` or `_`.
    
- **Note 1** : `+` can occur **before** the `@`, but not after.
- **Note 2** : `.`, `-`, `_` can occur on both sides of the `@`.
- **Note 3** : `.` at the end of the email address is *not considered part of the address*.


          ljw010512@naver.com
          ljw010512naver.com
          ljw010512@nav+er.com
          ljw010512@naver.com.

     *Result :*  
    
     ljw010512@naver.com
     ljw010512naver.com
     ljw010512@nav+er.com
     ljw010512@naver.com.
    
    
## Disallowed Raw HTML
