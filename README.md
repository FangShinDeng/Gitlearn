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

### 版本還原
1. 使用HEAD指標還原至指定版本, 最簡單的方法就是在SourceTree上連續點擊兩下, 看到了HEAD就對了!
2. 若想透過指令來執行HEAD的版本還原要進行以下步驟
    #### 1. git log 查看到要還原的commit
    #### 2. git checkout "1eff26" (可以用tab補齊, 但注意要使用git bash才能補齊, powershell無法補齊)
3. git checkout master 能直接還原到最新的版本

### Branch 本地分支用法, 將develop merge到master
1. git branch "分支名稱", 即可在本地端創建一隻分支
2. git branch, 能查看目前在哪條分支上, 正常會看到(master, develop)
3. git checkout develop, 能切換至本地的develop支線(用git bash的話, 會在後方看見master->develop)
4. git branch, 重新查看一次, 發現支線轉到了develop上
5. 在分支上新增檔案並留下commit 'develop分支的第一個commit, 新增all.css'
6. 查閱sourceTree上的變化
7. git checkout master, 測試回到本地端的master, 在使用git checkout develop回到本地端的develop
8. 先確保在master的分支上, 使用git merge develop

## 最大學習推薦：
1. 六角學院的Youtube，0基礎真的是能學會 https://w3c.hexschool.com/git/cfdbd310
2. 為你自己學Git，擁有很多情境題，在實務中一定要學會的　https://gitbook.tw/

## 一定要會的Git圖形化介面軟體: SourceTree