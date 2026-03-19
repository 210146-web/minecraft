# Plan：個人 Minecraft 首頁

## 範圍
依照 spec 實作一個可部署到 GitHub Pages 的前端靜態首頁。

## 技術決策（最小可行）
1. 使用原生 HTML、CSS、JavaScript。
2. 不引入建置工具與第三方框架。
3. 檔案放在專案根目錄，方便 GitHub Pages 直接發佈。

## 交付物
1. index.html：頁面結構與內容。
2. styles.css：視覺樣式與 RWD。
3. main.js：最小互動（如無必要可維持極簡）。
4. tests/ 或 scripts：可在本機執行的前端驗收測試。

## TDD 計畫
1. Red：先建立失敗測試，驗證必要結構與內容（標題、簡介、至少 3 個項目、RWD 相關檢查）。
2. Green：新增最小實作使測試通過。
3. Refactor：僅在不改變行為下做必要整理。

## 風險與控管
1. 避免套用模板覆蓋 spec 與 constitution：實作前後檢查規格檔仍存在。
2. 避免過度設計：只做 spec 明確要求。

## Git 檢查點
1. plan 完成後執行 git status 與 git diff --name-only。
2. implement 期間依 Red/Green/Refactor 每階段檢查一次。
