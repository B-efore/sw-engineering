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

## Task list items

## Strikethrough

## Autolinks

## Disallowed Raw HTML

