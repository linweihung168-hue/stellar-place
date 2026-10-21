# 札幌站店鋪查詢：使用與更新說明

收錄 Stellar Place、APIA、東急百貨店、大丸的店鋪樓層。放在 GitHub Pages 上，任何人打開網址就能用，不用登入，也能加到手機主畫面當 App。

網址：https://linweihung168-hue.github.io/stellar-place/

## 一、從舊版更新到這版

1. 打開 GitHub 的 `stellar-place` repository 頁面。
2. 點「Add file」→「Upload files」。
3. 把這個資料夾裡的**所有檔案**一起拖進去（同名檔案會自動取代）。
4. 按「Commit changes」。
5. 舊的 `shops.json` 已經用不到了，可以留著，也可以刪除：點進 `shops.json` →右上「⋯」→「Delete file」→「Commit changes」。
6. 等 1–2 分鐘，重新打開網址。手機上已安裝的 App，關掉再開一次就會更新。

## 二、第一次放上網路（新的 repository 才需要）

1. 到 https://github.com 建立新的 repository，選 **Public**。
2. 點「uploading an existing file」，把所有檔案拖進去，按「Commit changes」。
3. 「Settings」→「Pages」→ Source 選「Deploy from a branch」，Branch 選「main」與「/ (root)」，按「Save」。
4. 等 1–2 分鐘，Pages 頁面上方會顯示網址。

## 三、加到手機主畫面

- **iPhone**：用 Safari 打開網址 →「分享」→「加入主畫面」。
- **Android**：用 Chrome 打開網址 → 右上「⋮」→「安裝應用程式」或「加到主畫面」。

打開過一次之後，沒有網路也能查詢。

## 四、購買清單與行李清單

畫面最下方有三個分頁：店鋪查詢、購買清單、行李清單。

- **購買清單**：輸入要買的東西或店名，會自動找出在哪個商場哪一樓，並依樓層排成逛街順序。點項目可以填數量、單價、幫誰買。
- **行李清單**：選國外或國內、天數和加購包（日本、北海道冬季、溫泉、親子、商務），自動列出要帶的東西。可以建立多份。
- **分享**：兩種清單右上都有「分享」，產生連結傳給旅伴，對方點開就能匯入。

清單存在各自的手機或電腦裡，不需要登入；更新 App 或店鋪資料也不會清掉。清除瀏覽器資料或換手機會不見，重要的清單可以先用「分享」傳給自己備份。

## 五、更新店鋪資料

每個商場各有一個資料檔，哪家有變動就只換那一個：

| 商場 | 資料檔 |
| --- | --- |
| Stellar Place | stellar.json |
| APIA | apia.json |
| 東急百貨店 | tokyu.json |
| 大丸 | daimaru.json |

1. 在網頁最下方按「編輯資料」，修改、新增或刪除店鋪。
2. 在上方選好那個商場，按下方的「匯出資料檔」，會下載對應的 json 檔。
3. 到 GitHub repository →「Add file」→「Upload files」→ 上傳這個檔案（會取代舊的）→「Commit changes」。
4. 約 1 分鐘後生效，大家重新打開就會看到新資料。

只按「儲存」的話，修改只存在你自己這台手機或電腦上。

## 檔案說明

| 檔案 | 用途 |
| --- | --- |
| index.html | 網頁本體（內含一份資料備份） |
| stellar.json、apia.json、tokyu.json、daimaru.json | 各商場店鋪資料 |
| sw.js | 讓網頁離線也能用 |
| manifest.webmanifest、icon-*.png、apple-touch-icon.png | 加到主畫面時的名稱與圖示 |

資料來源：各商場官方網站（2026-10-19 整理）。
