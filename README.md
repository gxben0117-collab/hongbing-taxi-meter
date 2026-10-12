# 紅兵計程車計費表

手機開著用的計程車跳表網頁：GPS 抓位置，按「開始計費」後依里程＋低速時間跳表，附語音播報與導航。

- 線上版：https://gxben0117-collab.github.io/hongbing-taxi-meter/
- 主檔：`index.html`（單檔，無建置流程）；舊版放 `versions/`

## 功能
- 費率：台北／台中／高雄範本＋自訂（起跳、續跳、低速計時、夜間加成）
- 計費：里程每滿續跳距離 +續跳金額；時速低於門檻累計，每滿秒數 +續跳金額；夜間依上車時間加成
- 語音（瀏覽器 Web Speech，zh-TW）：開始/暫停/結束、每 N 元報價、導航轉彎提示、偏離路線重新規劃
- 導航：OSM Nominatim 搜尋、OSRM 路線、Leaflet 地圖；可跳轉 Google／Apple 地圖
- 螢幕常亮（Wake Lock）、重新整理不遺失行程（localStorage）、模擬行駛測試

## 限制
- 定位需 HTTPS；手機鎖螢幕或切到別的 App 時瀏覽器會暫停 GPS，回來後補算時間但缺段里程不補
- Nominatim／OSRM 為公用免費服務，有流量限制，不保證可用
