# ⚔️ Life Quest — 人生任務冒險公會

將日常生活待辦變成 RPG 任務。完成任務獲得 XP、升級並解鎖成就。

## 功能
- RPG 風格響應式首頁與冒險者檔案
- 學習、健康、生活、創意四種任務分類
- 完成任務、XP 累積、等級提升與三種成就
- localStorage 保存完成進度與確認式重設
- 任務內容與頁面分離，AI 可依 `AGENTS.md` 擴充

## 本機執行
在專案根目錄執行：
```bash
python -m http.server 8000
```
瀏覽 `http://localhost:8000/`。不要直接用 `file://` 開啟，因為任務資料使用 `fetch` 載入。

## 新增任務
閱讀 `AGENTS.md`，在 `data/quests.json` 增加符合契約的任務即可；不需複製 HTML。驗證：
```bash
python -m json.tool data/quests.json
```

## 部署 GitHub Pages
1. 建立 GitHub 公開 Repository，例如 `life-quest`。
2. 將本資料夾內所有檔案上傳至 Repository 根目錄。
3. 到 Repository → Settings → Pages → Build and deployment。
4. Source 選 `Deploy from a branch`，Branch 選 `main`，Folder 選 `/(root)`，儲存。
5. 等部署完成後，網站通常位於 `https://你的帳號.github.io/life-quest/`（以 Pages 畫面顯示的實際 URL 為準）。

## 技術
HTML5 / CSS3 / JavaScript / JSON / localStorage；無框架、無後端。

## 注意
任務完成進度只保存在目前瀏覽器，不會跨裝置同步；清除網站儲存資料後會失去進度。
