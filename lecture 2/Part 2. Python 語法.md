# Lecture 2 - 初窺Python

Version 1.0.  by Kin Ho. 
2022 April. 

### 初窺Python
- [ ] [Hello world! 程序](https://github.com/nacky012001/Python-tutorials/blob/main/lecture%202/Part%201%20Hello%20world!%20%E7%A8%8B%E5%BA%8F.md)
- [x] Python 語法
- [ ] [變量與型別](#types-and-variables)
- [ ] [運算子](#operators)

## Part 2. Python 語法
- ##### 判斷 if (if condition)
  即使在一般的程式語言中，判斷 `if` 被視為最基礎的語法之一。Python可基與`if`中的判段條件選擇是否執行當中指令

  `if`的最基礎語法為:
  ```python
  if (判斷條件):
    當判斷條件成立時，執行此區塊的指令
  ```
  例子:
  ```python
  if 1 + 1 == 2:
    print('1 + 1 is equal to 2.')  
    
  if 1 + 1 == 0:
    print('1 + 1 is not equal to 0. This line will not be printed out.')  
  ```
  結果: 
  ![alt text](https://raw.githubusercontent.com/nacky012001/Python-tutorials/main/lecture%202/images/if-1.PNG)
  1 + 1的答案是2，因此Python會印出 `'1 + 1 is equal to 2.'`。
  而非`'1 + 1 is not equal to 0. This line will not be printed out.'`
  
  此例子中，我們的判斷條件永遠不會改變。1 + 1永遠都是等於2
  但在之後的課程，我們可以透過變量、函數等方法，實現即時動態改變判斷條件的結果。實現功能如: 
  ```python
  if (working > 1 * hour):
    print('Hey guy!')
    print('You should get up and have some move.')
  ```
  
- ##### 縮行 (Python indentation)
  縮行意指每一行開始的前置空格
  透過`if`的例子，我們知道了想要條件成立後要執行的指令必須放區塊內
  
  在Python語法中，每個區塊必須注意縮行，否則將會發生錯誤:
  ```python
  if 1 + 1 == 2:
  print('a')
  ```
  print('a')
  `^`
  `IndentationError: expected an indented block`
  
  每一層的縮行代表著該區塊是否被包含在另一個區塊中
  ```python
  if 12 < 10:
    #  第一層縮行(兩個空格)，區塊#1從此開始
    print('the number is less than 10')
    
    if is_even(12):                                  # 此if 區塊被包含在上一個區塊中
      #  第二層縮行(四個空格)，區塊#2從此開始
      print('the number is less than 10 and even')
      #  區塊#2從此結束
      
    #  區塊#1從此結束
  ```
  從上例子可以見到，因為`區塊#2`被包含在`區塊#1`中，因此Python判斷12 並不大於 10後，`區塊#1`與`區塊#2`都不會執行，並不會有輸出
  
  ```python
  if 12 < 10:
    #  第一層縮行(兩個空格)，區塊#1從此開始
    print('the number is less than 10')
    #  區塊#1從此結束
    
  if is_even(12):                                 # 區塊#1已經結束，因此這個區塊並不包含於任何其他區塊中
    #  還是第一層縮行(兩個空格)，區塊#2從此開始
    print('the number is even')
    #  區塊#2從此結束
  ```
  從上例子可以見到，`區塊#1`結束後，`區塊#2`才開始，因此兩個區塊相互獨立。Python 將會判斷12是否少於10，然後判斷12是否為偶數
  因此輸出為
  ```python
  'the number is even'
  ```
  

  

