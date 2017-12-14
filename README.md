目的：使用 nodejs 開發一個 websocket 的 server，讓兩個以上的網頁可以互相溝通。

核心：當 client 向 server 建立連線時，將 client 連線儲存在一個陣列，當 server 要回覆訊息時，將訊息傳給陣列內所有的 client。

問題：尚未將斷開連線的 client 從陣列裡刪除

---

運行方式：

```
git clone https://github.com/contemplator/websocket-nodejs.git websocket-nodejs
cd websocket-nodejs
npm install 
node server.js
```

之後就可以透過 this.ws = new $WebSocket("ws://127.0.0.1:7000", ["echo-protocol"]); 進行溝通

---

傳輸字節測試可超過 10000 個中文字