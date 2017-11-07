# Lecture 1 HTML

##**什麼是ＨＴＭＬ？**
超文件標示語言（英語：HyperText Markup Language，簡稱：HTML）
是一種用於建立網頁的標準標示語言。
網頁瀏覽器可以讀取HTML檔案，並轉換成視覺化網頁。
HTML描述了一個網站的結構語意隨著線索的呈現，實際上html只是一種**標記式語言**而已。

    > 因為瀏覽器沒眼睛，是認文字去轉成網頁基本結構視覺化，所以網頁用文字去**記述**。

## First Layout
```html
<html>
  <head>
    <!--  這邊主要是瀏覽器看的一些設定/ 會放title，關鍵字或網站描述 -->
  </head>
  <body>
    <!--  這邊主要是給使用者看的內容-->
  Hello HTML!
  </body>
</html>
```

## Title 標題
```html
<html>
  <head>
    <title>First Step to HTML</title>
  </head>
  <body>
  </body>
</html>

```
除了網頁標題，做好一點的網站，
會在某個子網頁的標題顯現 `子畫面 - 網站`，
ex: `某某產品 - 某某購物網站`，
來增加 SEO 的 RANK


## Header and Paragraph 標題和段落
```html
<html>
  <head>
    <title>First Step to HTML</title>
  </head>
  <body>
    <h1>標題</h1>
    <h2>標題</h2>
    <h3>標題</h3>
    <h4>標題</h4>
    <h5>標題</h5>
    <h6>標題</h6>
    <p>aajdoifo ajsdapd foirnv </p>
  </body>
</html>
```
有六種大小的標題
- h1是最重要的標題，其次則是h2，以此類推。
- 不要被視覺（眼睛）矇騙，網頁看標籤而不是看顯示出來的字體大小來辨別重要性。
- Ex：h1標籤是大的重要的 雖然文字看起來是最大的，但其實可以用別的方式讓字變小，但對瀏覽器來說h1標籤仍是最優先的。

## List 清單
-  有序清單(ordered-list)  ex：有ＳＯＰ的料理步驟 （會影響網頁搜尋）
-  無序清單(unordered-list) ex：購物車內的東西
-  有序清單(ol) 會顯示12345  / 無序清單（ul）
### unorder list
```html
<ul>
  <!-- unorder list -->
  <li>我是一筆清單</li>
  <li>我是一筆清單</li>
  <li>我是一筆清單</li>
  <li>我是一筆清單</li>
  <li>我是一筆清單</li>
</ul>
```
### order list
```html
<ol>
  <!-- order list -->
  <li>有順序的清單</li>
  <li>有順序的清單</li>
  <li>有順序的清單</li>
  <li>有順序的清單</li>
  <li>有順序的清單</li>
</ol>
```

## Tag

```html
<tag attribute1="value" attribute2="value"></tag>
```

### 粗體
```html
<strong>Lorem</strong> <b>Ipsum</b>
```

**`<strong>` v.s. `<b>`**

`strong`是去強調這個內容，`b`是去讓文字外觀變成粗體(bolic)。

對於可以一般用視覺讓上網的使用者是沒有太大的差異，但是對於用一些視障人士，用聽的來看這個網站時，`strong`會讓讀報軟體聲音變大聲，強調了那個字

另外還有搜尋引擎在搜尋的時候，也會去認這些標籤，來達到辨識語意，知道 `strong` 是要強調的意思。

### 斜體
`<em>` for emphasize, `<i>` for italic
```html
<em>issimply</em>
<i>dummy</i>
```

**`<em>` V.S. `<i>` (italic)**

跟前面的  `strong` 和 `b` 的關係類似，`<em>`比`<i>`更有強調的意思。此外 `<strong>` 的強調度也大於 `<em>`。

在HTML5的標準裡面，這四個標籤都可以用。

## 超連結
`<a>` for `anchor`
- a標籤 ->顯示是超連結用
- href(參照) 是屬性 ,瀏覽器帶你到目的地
- 開新視窗 用target 的屬性
- 屬性跟屬性之間用空白間隔，屬性跟值之間不能用空白間隔
- `<a href="http://tw.yahoo.com" target="_blank">yahoo</a>`

```html
<a href="http://google.com">連到Google</a>
```
最簡單的形式

```html
<a href="http://google.com" target="_blank">連到Google</a>
```
會打開新視窗，還是在原本視窗跳到新網站

```html
<a href="http://google.com" target="_blank" title="此標題會開啟新視窗">連到Google</a>
```
title 可以有個小tooltip顯示說這個連結會做什麼事情
target 可以控制說按下這個連結後，是開新視窗還是在原視窗更換

## div and span
`div` for division
比較是分區的概念，會框出一個區塊，span比較是範圍的意思

假設我在段落裡面，想要標記一段文字來做特別效果，通常會使用span，如果使用div，如下
```
<p>
Lorem Ipsum has been the <div>industry's standard</div>dummy text ever since
</p>
```
通常會瀏覽器糾正為
```html
<p>
Lorem Ipsum has been the
</p>
<div>industry's standard</div>
"dummy text ever since"
<p>
</p>
```

## 表格
- 表格結構
  - table 外框/ tr 列 / td列裡面的格子
  ![](https://ws1.sinaimg.cn/large/006tKfTcgy1fkr3qb2v28j311s0iydq8.jpg)
- 表頭 thead / 表身tbody 
  -![](https://ws1.sinaimg.cn/large/006tKfTcgy1fkr3gyo7saj30js0jsq4t.jpg)
- 表格標題
  - caption 大表格標題
  - th 表格內的標題 
  - scope col 欄標題 / Scope row 列標題
  ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fkr3hvqvvwj30rm0fitb9.jpg)

最簡單3*3表格
```html
<table>
  <caption>我是表格標題</caption>
  <tr>
    <td>我是資料</td>
    <td>我是資料</td>
    <td>我是資料</td>
  </tr>
  <tr>
    <td>我是資料</td>
    <td>我是資料</td>
    <td>我是資料</td>
  </tr>
  <tr>
    <td>我是資料</td>
    <td>我是資料</td>
    <td>我是資料</td>
  </tr>
</table>
```
簡單地把加上每欄每列的標題
```html
<table>
  <caption>我是表格標題</caption>
  <tr>
    <td>我是資料</td>
    <td>我是資料</td>
    <td>我是資料</td>
  </tr>
  <tr>
    <td>我是資料</td>
    <td>我是資料</td>
    <td>我是資料</td>
  </tr>
  <tr>
    <td>我是資料</td>
    <td>我是資料</td>
    <td>我是資料</td>
  </tr>
</table>
```
現在有比較仔細劃分表頭跟表內容的方式
```html
<table>
  <caption>我是表格標題</caption>
  <thead>        
    <tr>
      <th>我是標題</th>
      <th>我是標題</th>
      <th>我是標題</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>我是資料</td>
      <td>我是資料</td>
      <td>我是資料</td>
    </tr>
    <tr>
      <td>我是資料</td>
      <td>我是資料</td>
      <td>我是資料</td>
    </tr>
    <tr>
      <td>我是資料</td>
      <td>我是資料</td>
      <td>我是資料</td>
    </tr>
  </tbody>
</table>
```
## 表單
### Label and Input
Label 和 Input 有兩種寫法
第一種，把input包在label裡，通常用在radio 和 checkbox
```html
<div>
  <label>
      女
      <input type="radio" id="female">
  </label>
</div>
```
第二種，input跟label拆開，通常文字欄位會是這個寫法
```html
<div>
  <input type="radio" id="male">
  <label for="male">
      男
  </label>
</div>
```
然後你會發現，明明我們通常是男跟女會擇一，可是若合併上面兩塊（如下），兩個選項卻可以都同時選
```html
<div>
  <label>
    <input type="radio" id="female">
    女
  </label>
</div>
<div>
  <input type="radio" id="male">
  <label for="male">
    男
  </label>
</div>
```
此時為兩者都加上同一個name，就會變成只能選其中一個了
```html
<div>
  <label>
    <input type="radio" name="gender" id="female">
    女
  </label>
</div>
<div>
  <input type="radio" name="gender" id="male">
  <label for="male">
    男
  </label>
</div>
```
### button
button 有兩種寫法，要選擇哪一種，可能就看你後端那邊喜歡怎麼接，或者是在做DOM操作或寫CSS哪個比較方便再挑。(這裡是我暫時查到的說明兩者不同的[文章](http://web.archive.org/web/20110721191046/http://particletree.com/features/rediscovering-the-button-element/
)
```html
<div>
  <input type="button" value="我是按鈕">
</div>
```
```html
<button></button>
```
## Image `<img src="" alt="">`
- 網頁是純文字欓，無法直接丟給他圖片 -> 告訴網頁這是圖片 ->去哪裡抓這張圖    
```html
<img src="https://lh6.googleusercontent.com/-8hF1HXdXYJU/AAAAAAAAAAI/AAAAAAAAjuU/-h954DPX_v8/s0-c-k-no-ns/photo.jpg" width="300" alt="樂高標誌">
```
- src ：圖片來源 
  - 如果圖片來源在網路上，直接複製網址（絕對路徑）/ 從網頁位置找圖片在哪 （相對路徑）
- width ：設定圖片的寬
- alt(altennate) ： 圖片替代文字
1.如果圖片無法顯示的時候顯示的文字
2.搜尋引擎可以透過替代文字知道是什麼圖片
3.跟無障礙網頁有關 ex 視障朋友上網是用閱讀機等輔助設備，「唸」出來，讓視障朋友們了解網頁。而念圖片時會念
## TAG 整理
```
標題 h1~h6
內文 p

清單
ul
ol
li

連結 a

表格
table 表格
thead 表頭
tbody 表內容
tfoot 表尾
tr
th 每一欄或每一列的標題
td
caption 大表格標題

表單（傳統）
form                  表單
lable                 標籤
input type="checkbox" 方塊打勾/複選
input type="radio"    圓圈/單選
input type="text"     單行文字
input type="password" 密碼
input type="button"   按鈕
input type="file"     上傳檔案
textarea              多行文字/留言
select                下拉式選單
  option              選單的選項


article               最主要的內容
section               章節
                      上面兩個可以互包，譬如說首頁裡面可以有很
                      多個section放不同的 article，一個長的
                      article也可以裡面放很多section
header                文章前言
footer                
nav                   導覽(整個網站應該只會有一個)
```
emmet快速外掛(3乘3表格):  `table>tr*3>td*3`
