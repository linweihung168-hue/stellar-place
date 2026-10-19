# Stellar Place 店鋪查詢：上架與使用說明

照下面步驟放上 GitHub Pages，任何人打開網址就能用，不用登入，也能加到手機主畫面當 App 使用。

## 一、放上網路（約 10 分鐘，只需做一次）

1. 到 https://github.com 註冊一個免費帳號（已有帳號可跳過）。
2. 登入後，點右上角「＋」→「New repository」。
   - Repository name 填：`stellar-place`
   - 選 **Public**
   - 按「Create repository」
3. 在新的 repository 頁面，點「uploading an existing file」。
4. 把這個資料夾裡的**所有檔案**一起拖進去（不是拖整個資料夾）：
   `index.html`、`shops.json`、`sw.js`、`manifest.webmanifest`、`icon-192.png`、`icon-512.png`、`icon-maskable-512.png`、`apple-touch-icon.png`
   （`README.md` 可傳可不傳）
5. 拉到下方按「Commit changes」。
6. 點上方「Settings」→ 左側「Pages」。
   - Source 選「Deploy from a branch」
   - Branch 選「main」、資料夾選「/ (root)」，按「Save」
7. 等 1–2 分鐘，重新整理 Pages 頁面，上方會出現網址：
   `https://你的帳號.github.io/stellar-place/`

把這個網址傳給朋友就可以了。

## 二、加到手機主畫面（每個人自己做）

- **iPhone**：用 Safari 打開網址 → 下方「分享」按鈕 → 「加入主畫面」。
- **Android**：用 Chrome 打開網址 → 右上「⋮」→「安裝應用程式」或「加到主畫面」。

加入後會出現星星圖示，點開就是全螢幕的 App 畫面。打開過一次之後，沒有網路也能查詢。

## 三、更新資料

在網頁最下方按「編輯資料」，可以修改、新增、刪除店鋪。

- 按「儲存」：修改只存在**這台手機／電腦**上。
- 要讓**所有人**看到修改：
  1. 按「匯出資料檔」，會下載 `shops.json`。
  2. 到 GitHub 的 repository 頁面 → 點「Add file」→「Upload files」→ 上傳這個 `shops.json`（會取代舊的）→「Commit changes」。
  3. 約 1 分鐘後生效，大家重新打開就會看到新資料。

建議用電腦做第三步比較順手。

## 檔案說明

| 檔案 | 用途 |
| --- | --- |
| index.html | 網頁本體（內含一份資料備份） |
| shops.json | 店鋪資料，更新資料時只要換這個檔 |
| sw.js | 讓網頁離線也能用 |
| manifest.webmanifest、icon-*.png | 加到主畫面時的名稱與圖示 |

資料來源：札幌ステラプレイス官方樓層地圖與店鋪頁（2026-10-19 整理）。
