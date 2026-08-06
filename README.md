# 葉面積與環境感測器散布圖分析 Dashboard

本專案使用 Python 與 Plotly 讀取 Excel（`葉面積.xlsx`）中的「大葉子」與「小葉子」數據，自動繪製環境感測器對比 XY 散布圖，並轉換為可於 **GitHub Pages** 部署的互動式網頁圖表。

---

## 📊 圖表內容說明

頁面展示三層動態感測器對比散布圖（採用 `plotly_white` 白底主題）：
1. **溫度 (°C) & 濕度 (%)**：比較大葉子與小葉子環境之溫濕度變化。
2. **CO2 (ppm) & VOC (ppb)**：比較二氧化碳與揮發性有機物濃度變化。
3. **照度 (Lux)**：比較光照強度變化。

---

## 🚀 如何部署至 GitHub Pages (靜態網頁託管)

請按照以下簡單步驟，將專案上傳至 GitHub 並啟用免費網頁託管：

### 步驟 1：在 GitHub 建立新 Repository (儲存庫)
1. 登入 [GitHub](https://github.com/) 並點擊右上角 **+** -> **New repository**。
2. 設定專案名稱（例如：`leaf-area-dashboard`），權限設為 `Public`。
3. 點擊 **Create repository**。

### 步驟 2：將檔案推送到 GitHub
開啟命令提示字元 (cmd) 或 Terminal，切換至此資料夾並執行：

```bash
git init
git add .
git commit -m "Initial commit for leaf area scatter dashboard"
git branch -M main
git remote add origin https://github.com/您的帳號名稱/leaf-area-dashboard.git
git push -u origin main
```

### 步驟 3：開啟 GitHub Pages 免費雲端網頁託管
1. 進入您在 GitHub 建立的 Repository 頁面。
2. 點選上方頁籤 **Settings** (設定)。
3. 在左側選單中找到 **Pages**。
4. 在 **Build and deployment** 下方的 **Branch** 選項：
   - 將分支改選擇為 **`main`**
   - 資料夾選擇 **`/(root)`**
   - 點擊 **Save**。
5. 等待 1~2 分鐘後，GitHub 就會為您產生專屬的線上圖表網址：
   `https://您的帳號名稱.github.io/leaf-area-dashboard/`

---

## 🛠️ 本地重新生成圖表

若修改了 `葉面積.xlsx` 數據，可在本地執行：

```bash
python 大葉子小葉子散布圖程式.py
```

即可自動更新 `index.html`。
