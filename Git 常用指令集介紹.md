###Git 常用指令集介紹

####config

|  指令  |  執行動作  |
|  ---- |  ---- |
|git config --list | 查看設定|
|git config --local user.name "(userName)"	| 設定帳號
|git config --local user.email "(e-mail)"| 設定E-mail
|git config --global user.name "(userName)"	|設定帳號
|git config --global user.email "(e-mail)" |設定E-mai

####init / clone

  指令  |  執行動作  |
|  ---- |  ---- |
|git clone | 抓遠端儲存庫下來|
|git init | Git 初始化
|rm -rf .git| 移除 Git

####pull / push / add / commit / status

 指令  |  執行動作  |
|  ---- |  ---- |
|git status | 檢查本機檔案狀態|
|git add| 將指定的檔案（或資料夾）加入版本控制
|git commit| 提交目前的異動
|git push| 將本機Repository的commit發佈到遠端
|git pull|擷取並合併遠端儲存庫

####branch / merge / stash

 指令  |  執行動作  |
|  ---- |  ---- |
|git branch | 顯示本機所有分支|
|git branch -a| 顯示儲存庫所有分支
|git branch <branch_name>| 新增分支
|git branch -d <branch_name>| 刪除分支
|git checkout <branch_name>|切換分支
|git stash|新增暫存
|git stash list|顯示查看所有暫存
|git stash apply|提取暫存
|git stash clear|清除全部暫存
|git stash pop|還原暫存
|git merge <branch_name>|將 branch_name 合併到當前分支
|git merge (branch)	| 合併分支
|git merge --abort| 取消 merge

####tag
指令  |  執行動作  |
|  ---- |  ---- |
|git tag|查詢標籤
|git tag -n|查詢詳細標籤
|git tag -d <tag_name>|刪除標籤
|git tag -am "備註文字" tag_name|新增標示標籤

####diff
指令  |  執行動作  |
|  ---- |  ---- |
|git diff |比較 目前位置 與 staging area
|git diff master|查看與 Master 有哪些資料不同
|git diff --cached|比較 staging area 跟本來的 Repository
|git diff new-branch|比較目前位置 與 branch(new-branch) 的差別
|git diff HEAD|比較目前位置 與 Repository 差別

####log
指令  |  執行動作 |
|  ---- |  ---- |
|git log |顯示所有 log 
|git log -p |顯示所有 log 和修改過得檔案內容
|git log --all | 顯示所有的 log (含 branch)
|git log --name-only|顯示此次 log 有哪些檔案被修改
|git log --stat --summary|顯示每個版本間的更動檔案和行數

####reset
指令  |  執行動作 |
|  ---- |  ---- |
|git reset --hard HEAD^|拆掉最近一次 commit
|git reset --hard ORIG_HEA|取消剛剛拆掉的 commit
|git reset --soft HEAD^|拆掉最近一次commit但保留異動內容

####commit
指令  |  執行動作 |
|  ---- |  ---- |
|git commit|新建版本
|git commit -m "message"| 提交staging area所修改的內容，並設定 commit message
|git commit --amend| 將目前staging area的修改內容與上一次的 commit合併，如果沒有修改內容，則單純修改上一次的commit內容
|git commit -am + (message)|新建版本且可留言
|git commit -a**|省略 git add 的步驟，直接提交變更
|git commit --amend**|將變更合併到上次提交中