# Sanrio Character Wiki 專案維護指南 (AGENTS.md)

本專案結合 **Andrej Karpathy LLM Wiki 知識庫架構** 與 **GitHub Pages 靜態夢幻粉彩網頁**，所有原始資料存於 `raw/`，結構化 Markdown 知識節點存於 `wiki/`，並同步呈現在根目錄的 `index.html`、`style.css`、`script.js` 與教學簡報 `presentation.html` 中。

---

## 1. 目錄結構規範
```text
sanrio-character-wiki/
├── AGENTS.md           # 本專案維護規範與 Graph 簡報生成準則
├── index.html          # 夢幻粉彩知識庫主網頁
├── presentation.html   # 新手教學型粉彩互動 HTML 簡報
├── style.css           # 粉彩漸層、漂浮裝飾與響應式樣式
├── script.js           # 角色資料庫、篩選、彈窗與扭蛋互動邏輯
├── index.md            # 知識庫總目錄索引 (Obsidian / GitHub 雙用)
├── log.md              # 知識庫與簡報變更歷程日誌
├── README.md           # GitHub 專案與 Pages 部署說明
├── raw/                # [唯讀原始資料層] 原始文章與資料備份，不可修改
│   └── articles/       # 維基百科與官方資料存檔
├── wiki/               # [Markdown 知識庫層] 結構化角色、誕生故事與編年史筆記
└── slides-work/        # [Graph 簡報工作區] 簡報產製之中間產物
    ├── sources.md      # 知識庫來源對齊表
    ├── cards/          # 獨立事實證據卡
    ├── outline.md      # 簡報故事線與大綱
    └── drafts/         # 逐頁逐字稿
```

---

## 2. 標準更新工作流 (`Ingest` & `Sync`)
1. **歸檔原文 (`raw/`)**：凡貼上或上傳新的三麗鷗相關文章，先保存至 `raw/articles/`。
2. **更新知識庫 (`wiki/` 與 `index.md`)**：在 `wiki/` 對應子目錄建立或更新 Markdown 筆記（使用 `[[Wikilinks]]` 連結），並同步更新根目錄的 `index.md` 與 `log.md`。
3. **同步網頁資料 (`script.js` / `index.html`)**：將新增的角色、誕生故事或排名數據同步更新至前端頁面。

---

## 3. Graph 簡報生成工作規範 (Presentation Workflow)
利用本知識庫製作針對「三麗鷗與角色文化新手」之教學型簡報時，必須嚴格遵守以下流程與限制：
1. **中間產物集中化**：所有過程檔案全部收錄於 `slides-work/` 目錄。
2. **單一事實來源（SSOT）**：所有簡報內容、年代、角色設定與排名數據 100% 來自 `wiki/` 條目，嚴禁外部預訓練腦補。
3. **強制來源引用**：每頁投影片底部必須明確標註引用的 `wiki/` 檔案路徑（例如：`引用來源：wiki/brand-story.md`）。
4. **設計風格契合**：採用三麗鷗經典夢幻粉彩（Pastel Dream）視覺風格，支援鍵盤切換與響應式閱讀體驗。
