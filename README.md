---
title: "final exam"
author: "Sally"
date: "2020/1/4"
output: html_document
---


## **R的初學者說明** 
請按照以下步驟進行操作，本內容會教您如何創建 **R Markdown** 並建立 **python** 物件。



## **R Markdown**
### ●創建R Markdown：File>New File>R Markdown
![](https://i.imgur.com/6oYxMkN.png)
### ●設定主題與作者
![](https://i.imgur.com/UXBCkv2.png)
### ●設定輸出格式
![](https://i.imgur.com/6usfx8a.png)

這樣R Markdown就算初步創建完成囉~~~~
現在我們就去輸入內容吧！！！


## **建立Python程式碼** 

### ●程序1：
以R Studio的 **reticulate** 程式套件中的 **repl_python** 函數產生Python interpreter，REPL。



```{r}　
#建立環境
install.packages("knitr")
library(knitr)
install.packages("reticulate")
library(reticulate)
py_available()
```


如果出現FALSE 那安裝keras會解決這個問題
install.packages("kreas")
library(kreas)
出現TURE我們就可以開始操作囉！




```{r}
#產生Python interpreter
repl_python( )
```


注意提示符號改為Python的”>>>”。以下可不需要改寫Python的程式。


### ●程序２：
以 **REPL** 執行Python程式碼建立新物件。

```{python}
#今天就做一個簡單的英文句子吧
A=("Sally ","Angle ","Eva ")
B="is"
C=(" girl"," pretty"," nice")
D="."
Z1=A[0]+B+C[0]+D
Z2=A[1]+B+C[1]+D
Z3=A[2]+B+C[2]+D
```
將Z1、Z2和Z3打印出來會是長這樣
>Z1
'Sally is girl.'
> Z2
'Angle is pretty.'
>Z3
'Eva is nice.'

### ●程序３：
在R Studio中讀取程序2所建立的新物件。

```{r}
#先按ESC挑出來回到R Studio的環境
#py$後面輸入要讀取的物件，就能叫出新物件
#class() 裡面輸入py$及讀取的物件，就能判別物件的屬性
```


> py$Z1;class(py$Z1)
[1] "Sally is girl."
[1] "character"
> py$Z2;class(py$Z2)
[1] "Angle is pretty."
[1] "character"
> py$Z3;class(py$Z3)
[1] "Eva is nice."
[1] "character"


## **R Markdown小技巧** 
1. headers - 使用一個或者多個 # 在文本的開始階段，例如： # Say Hello to markdown. 單個#意味著文本是一級標題，兩個#代表二級標題，以此類推.
2. 斜體和加粗字體 - 對文本兩側加一個星號得到斜體字體，例如上文中：*without realizing it*. 用雙星號包圍文本得到加粗字體, 例如：**easy to use**.
3. lists - 每個要點之前用星號，正文與要點之間留空行
4. hyperlinks - 1.用中括弧包圍網站名稱，2.用括弧包圍具體連結，然後連接在一起使用，例如：[Github](Build software better, together).

*我把這次學習的心得都放在Github上  [108-2Programming-for-R] (git@github.com:10732040/108-2Programming-for-R.git)
