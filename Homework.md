# 回家作業與上課練習

## 作業一


本次的課後練習為在今日的AZURE專案的public資料夾中，新增一個自我介紹的網頁，同學可使用自己之前做過的任何相關作品。本次作業的目的在於了解同學們的前台製作能力，

* 作業繳交：https://goo.gl/kr5SR6
* 作業截止日：<font color="red">2017-03-17 23:59</font>

---

## 作業二

### 第一部分：insert 練習

練習在mongoDB中插入一筆資料

* 連線主機 `140.112.28.194` port 為 `27017`
* database 為 `student`
* collection 為 `profiles`
* 新增一個 document 其內容如下

```json
{
    "sid" : "你的學號", 
    "name" : "你的姓名",
    "favorites" : ["喜好1", "喜好2", ...]
}
```
* 其中 favorites 需列3個以上


### 第二部分：update 練習

練習在mongoDB中更新資料

* 在 Azure 主機新增一台 mongoDB 並記錄其連接設定
* 連接 `140.112.28.194` 主機 
* database 為 `homework`
* collection 為 `hw2`
* 根據你的學號或姓名，找出其對應 document
* 並將其Azure的連接設定更新 

```json
{
    "student_id" : "BXXXXXXXX",
    "name" : "XXX",
    "azure_url" : "",
    "azure_port" : "",
    "username" : "",
    "password" : ""
}
```

### 作業截止日

* 作業截止日：<font color="red">2017-03-25 23:59</font>
* 遲交一天分數乘上0.9，依此類推

### 參考資料

* 官網資料：https://docs.mongodb.com/manual/crud/
* 中文資料：http://www.runoob.com/mongodb/mongodb-tutorial.html

