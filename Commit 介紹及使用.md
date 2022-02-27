###Commit 介紹及使用

當開發者為軟體增加一個新功能時，可能會同時在許多檔案的不同地方修改程式碼，因此軟體就會出現的版本差異，在版本控制系統中，稱呼這組更動為commit，commit在Git中就是個節點，這些節點就是日後可以回朔及追蹤的參考
![](/圖片/Feature.png)

在Local中分為working directory（工作資料夾）、staging area（暫存區）和 repositories（檔案庫）三個區域，通常開發者會先在工作資料夾工作，當要進入檔案庫之前會先將檔案加入暫存區，確認沒問題則commit到檔案庫中，最後push上去remote（遠端）環境。
![](/圖片/operations.png)

就輸入git commit -m 來提交版本後，系統如果回饋以下訊息，就代表透過 Git 建立出第一個版本出來了。
![](/圖片/commit.png)