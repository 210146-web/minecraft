# minecraft

個人 Minecraft 首頁專案 - 一個可部署到 GitHub Pages 的靜態網站。

## 快速開始

### 本機檢視
1. 直接在瀏覽器中開啟 `index.html`：
   ```bash
   open index.html  # macOS
   # 或用其他方式在瀏覽器中開啟該檔案
   ```

2. 或使用簡單的本機伺服器（需要 Python）：
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   ```
   然後在瀏覽器中造訪 `http://localhost:8000`

### 驗收測試
在瀏覽器中開啟 `test-runner.html` 可查看結構驗收測試結果。

## GitHub Pages 部署

### 方案 A：使用根目錄
1. 在 GitHub 中 fork 或建立新倉庫
2. 推送此專案到 `main` 分支
3. 進入 Settings → Pages
4. 選擇 "Deploy from a branch"，設定為 `main` 分支，根目錄
5. 數分鐘後網站將發佈至 `https://[username].github.io/minecraft`

### 方案 B：使用 docs 資料夾（若需要）
1. 將所有 HTML、CSS、JS 檔案複製至 `docs/` 資料夾
2. 進入 Settings → Pages，設定為 `main` 分支，`/docs` 資料夾
3. 網站將發佈至相同網址

## 檔案結構
```
minecraft/
├── index.html                    # 首頁
├── styles.css                    # 樣式表
├── test-runner.html              # 驗收測試頁面
├── README.md                     # 本檔案
├── speckit.constitution          # 開發規範
├── specs/
│   └── 001-personal-minecraft-homepage/
│       ├── spec.md              # 功能規格
│       ├── plan.md              # 實作計畫
│       └── tasks.md             # 工作清單
```

## 功能
- 靜態前端網站，純 HTML/CSS/JavaScript
- 響應式設計（RWD），支援桌機與手機瀏覽
- 無後端依賴，可直接部署到 GitHub Pages
- 至少 3 個 Minecraft 相關內容區塊

## 開發工作流
基於 TDD（Test-Driven Development）與 speckit 框架：
1. 先寫失敗測試（Red）
2. 實作最小功能使測試通過（Green）
3. 進行必要重構（Refactor）

詳見 `speckit.constitution` 與 `specs/001-personal-minecraft-homepage/` 資料夾。
