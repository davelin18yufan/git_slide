# git_slide

1. README 文件作為起專案的說明文件以及注意事項，避免冗餘檔案以及過多程式內註解

    易學網的例子就是因為兩間公司許多參數值不同當config的設定一多，同專案的 `push/pull` 很容易互相影響，沒有文件會找不到錯誤

   跳轉這種底層通用邏輯沒有文件會看不懂，無法除錯
2. 文件的重要性，裝了NUGET套件如果也沒有報錯根本無從找起，因為是用複製檔案的根本找不到需要安裝的地方
5. 瀏覽器收到的HEADER是會經過編碼，但是要在自己複製並創建一個新的HEADER就得需要自己重新編碼
6. 跳轉伺服器造成速率不同步問題，有可能是I/O未釋放造成刪除檔案失敗等
7. 分片傳入AP，合併，插入DB，上傳Wowza，在跳轉第三台沒意義，使用芳鄰IP共用資料夾
10. 跳ap再跳wowza因為分片請求過大不行，上傳到ap再上傳到wowza不行因為先前分片的請求已經沒了，直接打wowza伺服器不行會被cors擋掉並且因為WOWZA理論上是不能對外公開也不能掠過，網芳共用資料夾不行，資安不會過，
12. 專案用複製的大部分架構多餘且架構鬆散根本無法除錯
13. 大檔上傳需要根據使用到的API再去進行跳轉機制的修改，REVERT/RESTORE
14. git 可以解決現在像是亞璇不能看之前華銀專案的問題，例如只開瀏覽權限給他，這樣也不用擔心她會改到甚麼
15. code review 基本上現在是在GITHUB上做是最好，他幫你整理好每次COMMIT的變動，以及對方的註解，但前提就是開發人員的 COMMIT 要做好，該次的檔案該次的說明註解等
16. 學會使用linter, prettier，或是 VS 的環境規則設定`,linter setting learn
17. 如何撰寫好的 function, HOF, low coupling
18. **typescript, lint slide.**
19. input ui component with autocomplete.
20. 包裝 LIB 成 NPM.
21. 如果API發出之後快速切換頁面或是馬上發送下一筆API需要考慮上一筆是否需要取消，可以減少後端負荷，使用 `abortController`,如果是動態路由則是抓取規則並且abortAll()
