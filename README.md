# Nekobasu：使用與更新說明

旅行小幫手：旅程倒數、出發前待辦、購買清單、行李清單、匯率，加上札幌站四商場（Stellar Place、APIA、東急百貨店、大丸）的店鋪指南。放在 GitHub Pages 上，任何人打開網址就能用，不用登入，也能加到手機主畫面當 App。

網址：https://linweihung168-hue.github.io/stellar-place/

## 一、從舊版更新到這版

1. 打開 GitHub 的 `stellar-place` repository 頁面。
2. 點「Add file」→「Upload files」。
3. 把這個資料夾裡的**所有檔案**一起拖進去（同名檔案會自動取代）。
4. 按「Commit changes」。
5. 舊的 `shops.json` 已經用不到了，可以留著，也可以刪除：點進 `shops.json` →右上「⋯」→「Delete file」→「Commit changes」。
6. 等 1–2 分鐘，重新打開網址。手機上已安裝的 App，關掉再開一次就會更新。主畫面圖示和名稱要刪掉再重新「加入主畫面」才會換成 Nekobasu。

## 二、第一次放上網路（新的 repository 才需要）

1. 到 https://github.com 建立新的 repository，選 **Public**。
2. 點「uploading an existing file」，把所有檔案拖進去，按「Commit changes」。
3. 「Settings」→「Pages」→ Source 選「Deploy from a branch」，Branch 選「main」與「/ (root)」，按「Save」。
4. 等 1–2 分鐘，Pages 頁面上方會顯示網址。

## 三、加到手機主畫面

- **iPhone**：用 Safari 打開網址 →「分享」→「加入主畫面」。
- **Android**：用 Chrome 打開網址 → 右上「⋮」→「安裝應用程式」或「加到主畫面」。

打開過一次之後，沒有網路也能查詢。

## 四、各分頁

畫面最下方有五個分頁：首頁、店鋪、購物、行李、設定。

- **首頁**：目前旅程的倒數（旅行中會顯示第幾天和店家搜尋）、小工具、出發前待辦、當地提醒、我的旅程。點主視覺的「編輯」改城市和日期；日期可以填確切日期、只填月份或未定。右上「編輯」可以隱藏或排序小工具。
- **指南**：上方切換札幌站和小樽。札幌站是四個商場的店家，點樓層標題可以收起那一層；小樽有示意圖、17 個地點和兩條推薦路線（資料在 index.html 內的 otaru-data，來源：小樽觀光協會、北海道官方觀光網站）。
- **購物**：每趟旅程各自一份。輸入要買的東西或店名，會自動找出在哪個商場哪一樓，並依樓層排成逛街順序。分類自己建，可以切換「逛街順序」或「依分類」來看。填單價會換算台幣。
- **行李**：從空白開始，自己建分類和物品，可以建立多份。勾「記住」的物品會變成「我的常用物品」，建立新清單時可以一次帶入。
- **設定**：店名顯示、深淺色、匯率、備份與還原、店鋪資料編輯。
- **分享**：購物和行李清單右上的「分享」會產生連結，傳給旅伴點開就能匯入。

更新到這一版不會清掉原本的清單，原本的購買清單會自動變成「札幌」旅程的清單。資料存在各自的手機裡，換手機前請到「設定 → 備份所有資料」，再到新手機「從備份還原」。

## 五、更新店鋪資料

每個商場各有一個資料檔，哪家有變動就只換那一個：

| 商場 | 資料檔 |
| --- | --- |
| Stellar Place | stellar.json |
| APIA | apia.json |
| 東急百貨店 | tokyu.json |
| 大丸 | daimaru.json |

1. 到「設定 → 店鋪資料」，修改、新增或刪除店鋪。
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
| manifest.webmanifest、icon-*.png、apple-touch-icon.png、favicon-32.png | 加到主畫面時的名稱與圖示 |

資料來源：各商場官方網站（2026-10-19 整理）。
