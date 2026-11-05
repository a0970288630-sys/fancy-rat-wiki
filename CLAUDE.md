# CLAUDE.md - FancyRat-Wiki 專案開發規範

歡迎參與 **FancyRat-Wiki** 專案！本文件是用於指導 AI 如何在此專案中新增、修改或維護內容與網頁結構的核心規則。

## 1. 專案核心架構與目錄規範
專案採用純前端靜態網頁架構（HTML5 + Tailwind CSS + marked.js），所有文章內容均透過 Markdown 檔案編寫，並由前端動態載入渲染。

- `index.html`：網站主頁面（包含響應式側邊欄與動態 Markdown 解析區）
- `content/index.json`：文章清單與分類索引（**AI 新增文章時必須同步更新此檔**）
- `content/intro/`：基礎認識與品種介紹
- `content/care/`：籠舍佈置與日常照護

## 2. 新增內容時要遵守的格式規範
1. **檔名規則**：必須使用 **kebab-case**（小寫英文與連字號），例如 `safe-food-list.md`。
2. **YAML Frontmatter**：每篇 Markdown 文章頂部必須包含以下格式：
   ```markdown
   ---
   title: "文章標題"
   category: "分類名稱"
   date: "YYYY-MM-DD"
   summary: "一句話簡短摘要"
   ---