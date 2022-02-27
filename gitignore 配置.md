###.gitignore 配置

gitignore顧名思義就是叫git忽略掉特定的檔案，不只是比較機密的檔案，有些程式編譯的中間檔或暫存檔，只要一編譯就等於產生一次新的檔案，對專案來說通常沒有實質的利用價值，像這樣的檔案通常都會忽略掉，所以git提供了.gitignore這個方法，只需要在工作區新建一個名稱為.gitignore的文件，把要忽略的文件名填進去，Git就會自動忽略這些文件。

####.gitignore忽略規則的順序
在.gitingore 文件中，Git檢查忽略規則的時候有多個來源，當決定是否要忽略某一路徑時，git會從多個文件源檢查gitignore模式，依照下列順序進行匹配


1.命令行中讀取可用的.gitignore 
2.依照.gitignore文件的目前的位置（project中都會有一個.gitignore文件，因為他在目錄中層次最低，所以優先級最高）
3.$GIT_DIR/info/exclude
4.被core.excludesFile配置變量指定的文件
