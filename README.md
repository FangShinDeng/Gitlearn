## 複習Git的用法
1. git init  (新建一個數據庫)
2. git add . (新增至索引)
3. git commit -m "內容" (新增至本地數據庫)
4. 上傳至遠端(Push代碼), 可以直接複製github上的遠端上傳代碼

### commit修改練習(尚未push到遠端)
1. 先新增一個index.html
2. 接著留下一組commit "WTF"
3. 使用 --amend 最新提出的git  git commit --amend -m "Welcome To Facebook"
4. git log重新看一次最新提交git的內容修改成功!

### 少放一個檔案到commit裡面
1. 假設少放一個style.css的檔案進來，最近一次的commit為"Welcome To Facebook"
2. 新增一個style.css
3. git add . 先新增到索引
4. 使用git commit --amend -m "Welcome To Facebook2"
5. git log重新查看一次最新提交的git的內容修改成功!

### Branch 分支用法
1. 新增一個遠端數據庫 gitlearn-1
2. 連結遠端數據庫，git remote add origin git@github.com:FangShinDeng/gitlearn-1.git, 但要把"origin"給換成"分支名稱"
3. 我們取一個分支名稱為 dev, 執行 git remote add dev git@github.com:FangShinDeng/gitlearn-1.git
4. 在SourceTree上會看到新的dev分支就代表成功了
5. 用不同的分支管理版本, 把origin當作正式主機, dev當作測試主機
6. 假設收到一個新的功能開發, 我們要進行開發, 我們先在本地端開發完畢後push到測試環境, 測試環境正常再更新到正式環境. 我們進行一個app.js的當作範例實作
7. 新增app.js, git到本地數據庫, push到dev, dev測試正常
8. push到origin


## 最大學習推薦：
1. 六角學院的Youtube，0基礎真的是能學會 https://w3c.hexschool.com/git/cfdbd310
2. 為你自己學Git，擁有很多情境題，在實務中一定要學會的　https://gitbook.tw/

## 一定要會的Git圖形化介面軟體: SourceTree