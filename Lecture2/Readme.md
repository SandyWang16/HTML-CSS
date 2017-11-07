
# Lecture 2 CSS

## CSS 
```CSS
selector {
  CSS屬性1: 值;
  CSS屬性2: 值;
}
```
- **選取器：找到誰去做設定/更改的意思**
  - p vs .p 是不一樣的
    - 選標籤 直接打 ex p
    - 選class(類別) 要加.   Ex .sp
			![](    https://ws2.sinaimg.cn/large/006tKfTcgy1fkr3y9hxnvj31kw0bw0zm.jpg)
- **優先權**
  - 選取器（同等級）一樣的情況，順序後面的會覆蓋前面
  - id>類別class>標籤tag
- **共用的地方用tag / 特殊化的用class**
  - 一個標籤可以有很多class，不同的class用空白做區隔
    -`<p class="男 短褲 短髮">`
    - 要選男 短髮時  `.男.短髮`  （串起來的是同一個物件）
    ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fkr3yts2b8j31kw0nrqec.jpg)
    - 越詳細越明確的優先權越高  （.男.短髮  > .男）
 - **空間的概念**（切版常用到）
    - 在ＡＡ裡面的strong  （用空白）
      - 指定某一個東西的子層 ，ＡＡ是父層 strong是子層
      ![](https://ws4.sinaimg.cn/large/006tKfTcly1fkr3zh70byj31kw0g1ajd.jpg)
 - **路徑** 
    - 同一個資料夾裡的檔案 直接打名字`img src='lego.png'`
    - 不同資料夾裡的檔案 打資料夾在打名字`img src='pic/lego.png'`
    - A資料夾裡找Ｂ資料夾的檔案 `img src='../b/xx.jpg`
    - 出一個資料夾`../` 要再出去就在一次`../ `會變成`../../資料夾/檔案`
    - 從網頁位置找其他檔案 （相對路徑） 
    - 從網址找到檔案（絕對路徑）

## CSS 類型

- 文字
  - 字級 font-size
  - 色彩 color
  - 字體 font-family
    - `font-family: '華康娃娃體', '華康少女體', '水管體', '黑體', '新細明體', san-serif;`
    - 會依序去看說電腦裡有沒有這個字體，沒有的話就往下套，最後都沒有就用預設的
    - 通常會用字型的英文名稱來做設定
    - 字體分兩大類 有襯線字  vs 無襯線字sans-serif (會抓系統內建的預設的)
  - 字體名稱中間有空白用單引號來圈起來
  - 斜體 font-style
    - `font-style: italic;`  仿斜體 (用CSS去模擬斜體)
  - 粗體 font-weight
    - Range: 100 ~ 900
    - 100 ~ 300 細, 400 ~ 600 粗, 700 ~ 900 特粗
    - `font-weight: bold;` 仿粗體/ 字體本身沒有粗體 用軟體計算的方式讓她加粗 /
  - 裝飾 text-decoration
    - none會讓原本有底線的消失
- 段落
  - 行距 line-height
    - 很少會用固定大小，通常都會根據字體大小
    - 通常黑體字會調行距大，有襯線字會行距小
    - 當沒有特別指定時，line-height (行高)在瀏覽器的原始預設值為 1.0 ~ 1.2 倍，但如果想要讓瀏覽者在閱讀文字上面感到更舒適的話，通常比較多人會設定在 1.4 ~ 1.8 倍之間。
  - 段落間距 margin （外距）
    - margin 是指外部距離，物件跟物件之間的距離，邊界
  - 留白 padding （內距、墊充）
    - padding 是指物件跟內容物之間的距離
  - 首行縮排 text-indent
    - 通常會用em來做單位，em是指一個字的大小，一個字大小預設是16px
  - 字距
    - word-spacing 每個單字
    - letter-spacing 每個字母  

## Layout
### Box Model

- 參數
  - Width 物件寬度
  - Padding 物件框和內容物的寬度
  - Margin 物件之間的寬度
  - Border 物件邊緣
- 佔據空間 寬＋padding + border + margin
- 可見範圍 寬＋padding + border
- width(內容物的寬度) + padding（內距） + border（邊匡） -           人的肉體＋ 衣服跟肉體的空隙  ＋衣服的厚度

- **區塊尺寸的控制**
  - 高度通常不設定，因為內容太多會自動撐高
  - 寬度設定
    - Padding :內容物跟邊邊的距離
    - Margin: 物件跟物件之間的距離
 
      
      
