# 網站資料庫程式設計 (Website Database Programming 

# 基本資料
 項目 | 描述 
:-------:| --- 
課程編號 | CSX2003 
學分數   | 1學分 
課程類型 | 微課程 
授課老師 | 陳琨 (kchen [at] csie.org)
課程助教 | 夏維良 (r05922075 [at] ntu.edu.tw) <br> 林修平 (twedusuck [at] gmail.com) <br> 陳宣毅 (r03126005 [at] ntu.edu.tw)
臉書社團 | https://www.facebook.com/groups/kchen.club
讀書會 | 星期五晚上 (教室會在 3月6日公告)


---

# 課程介紹

Node.js 是 Ryan Dahl 基於 Google 的 V8 引擎於 2009 年釋出的一個 JavaScript 開發平台、開放原始碼、跨平台的、可用於伺服器端和網路應用的執行環境。 

由於Node.js以單執行緒執行，使用非阻塞I/O呼叫，這樣既可以支援數以萬計的並行連線，又不會因多執行緒本身的特點而帶來麻煩。眾多請求只使用單執行緒的設計意味著可以用於建立高並行應用程式。 
MongoDB 是種 NoSQL 資料庫，將資料儲存為一個文件，資料結構由鍵值(key=>value)成對組成。MongoDB 文件類似於 JSON 物件，欄位值可以包含其他文件，陣列及文件陣列。由於採用JSON格式儲存資料，可以完美的與 Node.js 結合，大大提升資料表示的可能性，同時相符於前端開發對於資料需求的格式，有效的資料格式規劃，將可大大降低開發複雜度，並有利於網路資料上的交換。 

本堂課會提供每位學生一個 Azure 帳號使用，於發放日至 6/30 之間可免費使用

---

# 上課教室及時間
   週 |   日 | 時間 | 班級 | 教室 |
:----:| :----:| :---: | --- | --- 
第01週 | 2/22 |星期三 10,A,B | 01班 02班 上課，拿授權碼 | 普202 
第02週 | 3/01 |星期三 10,A,B | 01班 | 普202 
第03週 | 3/08 |星期三 10,A,B | 01班 | 普202 
第04週 | 3/15 |星期三 10,A,B | 01班 | 普202 
第05週 | 3/22 |星期三 10,A,B | 01班 | 普202 
第06週 | 3/29 |星期三 10,A,B | 01班（02班 同學也可以來看） | 普202 
<font color=red>第07週</font> | <font color=red>4/05</font> | <font color=red>放假</font> | <font color=red>放假</font> | <font color=red>放假</font> 
第08週 | 4/12 |星期三 10,A,B | 02班 | 普202 
第09週 | 4/19 |星期三 10,A,B | 02班 | 普202 
第10週 | 4/26 |星期三 10,A,B | 02班 | 普202 
第11週 | 5/03 |星期三 10,A,B | 02班 | 普202 
第12週 | 5/10 |星期三 10,A,B | 02班（01班 同學也可以來看） | 普202 

---

# 加選規則

1. 非電機資訊學院學生優先加選。
 * 本課程的設計是讓更多非本科系的學生能接觸到程式設計，在人數有限的情況下，才會如此限制，希望能照顧到更多非本科系的學生。
2. 能確定每次上堂課都能參與，並且樂於在上課時與老師及其它同學互動優先。
3. 如選課人數過多，確定要選的同學先簽名，最後再由老師根據HW0的成績寄信發授權碼
4. <font color=red>02班仍有名額，歡迎加選 (2/28)</font>

---

# HW0 要求

1. 註冊 Github 和安裝 GitHub Desktop
2. 註冊 Microsoft 帳戶，才能在下週上課前幫忙開通 Azure 主機 
 * 網址 https://portal.azure.com
 * 未註冊的同學請使用 hotmail 或 gmail 申請
 * 目前使用學校信箱註冊會有問題
3. 利用 Node.js 撰寫 Hello Word，並且將程式碼發佈至 Github 上
4. HW0繳交位址：https://goo.gl/forms/hE8rRRkBa4YjGEqt1

---

# 對學生的要求

* 希望學生不要有太多課程（大學生頂多 18 學分，研究生頂多 9 學分）
* 願意每週課後花 8 小時以上來練習程式，及使用 Azure 開發專案
* 每週都要帶充滿電的筆電，最好自備延長線

---

# 上課時會使用的軟體

 項目 | 內容
:---:| ------
作業系統 | Windows 7 以上
瀏覽器 | Google Chrome (https://www.google.com/chrome)
編輯軟體 | Visual Studio Code (https://code.visualstudio.com/)
編譯程式 | Node.js v7.5.0 (https://nodejs.org/en/)
版本控制 | GitHub Desktop (https://desktop.github.com)
資料庫 | MongoDB 3.4.2 (https://www.mongodb.com/)

---
   
# 評分方式

* 上課參與: 20%
  * 在課堂與老師的互動
  * 最後一堂課參與合照 
  * 上台 Demo
* 隨堂練習: 10%
  * 於上課現場完成者，下課後不再收此練習。
* 回家作業: 35%
  * 完成老師指定作業
* 期末報告: 40% 
  * 最後經老師認可，具資格參加CS+X期末發表的組別，期末報告成績為A
  * 若參加期末發表會獲得獎項，則期末報告成績為A+
  * 其餘依照完成度斟酌給分


---

# 問與答

Q: 請問「遊戲程式設計初階」和「網站資料庫程式設計」是同一個時間上課，我能否選擇一個是 01 班；另一個02班呢?

> 可以的，只要時間不衝突即可

Q: 那再請問，因這兩門課都要求01班和02班要能在第一週上課，但無法同時間到兩間教室該怎麼辦呢?

>關於 「網站資料庫程式設計」 只要符合加選規則，能完成HW0，可在第一週下課再來索取授權碼，若修課人數過多則改寄信通知。


---

# 參考教材

項目|內容
:---:|---
書名|不一樣的Node.js：用JavaScript打造高效能的前後台網頁程式 第二版
作者|錢逢祥, 蔡政崇, 林政毅 
出版社|松崗 
出版日|2015年11月23日 
ISBN|9789572244753 
語言|中文繁體 
參考網址|http://www.books.com.tw/products/0010697535 

