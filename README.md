# 花東縱谷．一日行旅 電子雜誌

一份 8 小時的花東縱谷一日遊行程，以雜誌風格呈現。

## 🚀 部署到 GitHub Pages（三步驟）

### 步驟 1：建立 GitHub Repository

登入 GitHub → 右上角 `+` → `New repository`

- **Repository name**：`hualien-magazine`（或任何名字）
- **Public**：✅ 一定要選 Public（Private 需要付費才能開 Pages）
- **不用勾** Add a README
- 點 `Create repository`

### 步驟 2：上傳檔案

有兩種方式，選一種：

#### 方式 A：網頁拖拉（最簡單，推薦）

1. 進入你剛建立的 repository 頁面
2. 點畫面中的 `uploading an existing file` 連結
3. 把整個 `hualien-magazine` 資料夾內的檔案（`index.html` + `images/` 資料夾）拖進去
4. 下方 `Commit changes` 按綠色按鈕

#### 方式 B：Git 指令（進階）

```bash
cd hualien-magazine
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/你的帳號/hualien-magazine.git
git push -u origin main
```

### 步驟 3：啟用 GitHub Pages

1. 進入 repository 頁面 → 上方 `Settings`
2. 左邊選單找 `Pages`
3. `Source` 選 `Deploy from a branch`
4. `Branch` 選 `main`，資料夾選 `/ (root)`
5. 按 `Save`
6. 等 1-2 分鐘，頁面上方會出現你的網址：
   ```
   https://你的帳號.github.io/hualien-magazine/
   ```

這個網址就可以分享給任何人！

---

## 📷 加入景點照片（選擇性）

網頁預設沒有實景照片時會顯示漸層色塊（也很好看）。若想放入真實照片：

1. 把照片放到 `images/` 資料夾
2. 檔名按下方對照命名：

| 檔名 | 對應景點 |
|------|---------|
| `cover.jpg` | 封面山景（建議寬幅） |
| `intro.jpg` | 序頁縱谷風景 |
| `1_liyu_lake.jpg` | 鯉魚潭 |
| `2_lintianshan.jpg` | 林田山 |
| `3_sugar_factory.jpg` | 光復糖廠 |
| `4_yunshanshui.jpg` | 雲山水 |
| `5_starbucks.jpg` | 理想星巴克 |
| `6_pacific_park.jpg` | 太平洋公園 |
| `restaurant.jpg` | 太巴塱風味餐 |

**照片建議**：
- 尺寸：1200 x 900px 以上（橫式）
- 大小：每張建議 200-500KB
- 格式：`.jpg` 為主

放好後重新 push 到 GitHub 即可。

### 免費照片來源

- **[Unsplash](https://unsplash.com)** - 搜尋 "Hualien"、"Taroko"、景點英文名
- **[Pexels](https://www.pexels.com)** - 同上
- **[Wikimedia Commons](https://commons.wikimedia.org)** - 搜尋景點名稱

---

## 🔧 常見問題

**Q1：GitHub Pages 網址打不開？**
- 通常需要等 2-5 分鐘部署完成
- 確認 Settings → Pages 有顯示 "Your site is live at..."
- 網址結尾記得加 `/`

**Q2：照片沒顯示？**
- 檢查檔名是否完全一致（大小寫敏感）
- 檢查照片是否放在 `images/` 資料夾內
- 用瀏覽器開啟 `https://你的帳號.github.io/hualien-magazine/images/1_liyu_lake.jpg` 看能否直接載入

**Q3：想修改內容？**
- 直接編輯 `index.html`，重新 push 就會更新
- 或在 GitHub 網頁上直接點檔案 → 鉛筆圖示編輯

**Q4：想換色系或字型？**
- `index.html` 開頭的 `:root` 區塊定義了所有顏色變數
- 修改 `--moss`、`--clay`、`--gold` 等就能改主色調

---

## 📄 分享方式

部署完成後，你可以：
- **傳連結**：LINE、FB、Email 直接貼網址
- **QR Code**：用 [QR Code Monkey](https://www.qrcode-monkey.com/) 產生 QR
- **列印**：瀏覽器 Ctrl+P，可存成 PDF 或紙本

---

## 📁 檔案結構

```
hualien-magazine/
├── index.html          ← 網頁本體
├── images/             ← 景點照片資料夾
│   ├── cover.jpg
│   ├── intro.jpg
│   ├── 1_liyu_lake.jpg
│   ├── 2_lintianshan.jpg
│   ├── 3_sugar_factory.jpg
│   ├── 4_yunshanshui.jpg
│   ├── 5_starbucks.jpg
│   ├── 6_pacific_park.jpg
│   └── restaurant.jpg
└── README.md           ← 這份說明
```
