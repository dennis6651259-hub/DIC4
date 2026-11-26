# 王鼎昌 7115064172 DIC4 DietSense 投稿草稿

本作業延續 [DIC3 DietSense](https://github.com/dennis6651259-hub/1111-DoI3)，完成英文學術論文初稿及修訂稿，並用 OpenSpec 記錄修稿要求。使用者未指定投稿場域，採通用 article 格式。本 repository 為 DIC4 獨立交付入口，論文、規格及匯入檔均由下方連結取得。

## 修改前／修改後 PDF 對照

下表 PDF 為實際從 Overleaf 編譯後下載的版本；點擊即可在 GitHub 閱讀。

| 項目 | 修改前：英文初稿 v0 | 修改後：修訂稿 v1 |
| --- | --- | --- |
| **PDF 閱讀** | **[開啟修改前 PDF](validation/overleaf/DietSense_DIC4_Before.pdf)** | **[開啟修改後 PDF](validation/overleaf/DietSense_DIC4_After.pdf)** |
| 頁數 | 2 頁 | 6 頁 |
| 版本用途 | 本次依 DIC3 整理的英文基準稿 | 依 OpenSpec 修稿規格完成的學術論文草稿 |
| 修改重點 | 作為後續修訂的比較基準 | 強化 Abstract、Introduction、Related Work，補充研究問題、評估協定與限制 |
| LaTeX 原始檔 | [before/main.tex](paper/before/main.tex) | [after/main.tex](paper/after/main.tex) |
| Overleaf 專案 | [DietSense DIC4 Before](https://www.overleaf.com/project/6b07e4d866226db300e5848a) | [DietSense DIC4 After](https://www.overleaf.com/project/6b07e69a0b58b245f496dacc) |
| Overleaf 編譯 | 0 錯誤、0 警告 | 0 錯誤、0 警告 |

詳細修改理由見 [修改對照說明](revision-notes.md)，逐行差異見 [LaTeX revision.diff](paper/revision.diff)。修改前是本次新建立的英文稿；兩版均為研究提案，尚未完成實驗。

## 閱讀順序

1. [教授要求與目標](goal.md)
2. [修改後論文 PDF 6 頁](paper/after/main.pdf) 與 [修改前初稿 PDF 2 頁](paper/before/main.pdf)
   - [修訂稿 LaTeX](paper/after/main.tex) 與 [初稿 LaTeX](paper/before/main.tex)
3. [修改對照](revision-notes.md)
4. [設計](design.md)、[任務狀態](task.md)、[OpenSpec 變更](openspec/changes/dic4-paper-draft/)
5. [Overleaf 專案與操作紀錄](OVERLEAF_GUIDE.md)

## 內容與邊界
論文核心為 Abstract、Introduction、Related Work，補有支撐方法、評估、限制與結論。before 是本次從 DIC3 整理的新英文初稿，不是既存 Overleaf 歷史。500 筆資料、20 人研究及 85%／60%／70 門檻皆是待驗證計畫，沒有宣稱實驗已完成。

## LaTeX
兩個版本各自只有 main.tex，內含可點擊參考文獻。Overleaf 選 pdfLaTeX；本地可用 `latexmk -pdf main.tex`。paper/references.bib 為另外提供的 BibTeX 書目資料，現有 main.tex 使用內嵌書目，不需要 BibTeX。

## OpenSpec 重現
固定 CLI 1.17.0，執行環境需符合該版套件 engines。可在本目錄執行：

```sh
npx --yes @fission-ai/openspec@1.17.0 --version
npx --yes @fission-ai/openspec@1.17.0 status --change dic4-paper-draft
npx --yes @fission-ai/openspec@1.17.0 validate dic4-paper-draft --strict
```

實際執行紀錄見 validation/。OpenSpec 格式通過不表示原型測試通過。task.md 區分文件完成、交付驗證、外部操作與後續研究。

## Overleaf 實際專案

- [修改前：DietSense DIC4 Before](https://www.overleaf.com/project/6b07e4d866226db300e5848a)（2 頁）
- [修改後：DietSense DIC4 After](https://www.overleaf.com/project/6b07e69a0b58b245f496dacc)（6 頁）
- [Overleaf 下載的修改前 PDF](validation/overleaf/DietSense_DIC4_Before.pdf)／[修改後 PDF](validation/overleaf/DietSense_DIC4_After.pdf)

已透過一般 Chrome 完成兩份 ZIP 匯入、命名、編譯檢查及 PDF 下載，兩份均為 Errors 0、Warnings 0。專案連結需要擁有者登入或授權；PDF 可從本 repository 閱讀。

## Overleaf MCP

已安裝 overleaf-web-mcp 1.4.1 並完成握手與工具列舉，但 MCP 登入未成功；尚未完成經 MCP 的專案讀寫／編譯。使用者指定改用一般 Chrome，所以上述實際操作不冒充 MCP 證據。詳見 [操作與限制紀錄](validation/overleaf-evidence.md)。

## Overleaf 匯入檔

- [修改前 ZIP](overleaf/DIC4_Overleaf_Before.zip)
- [修改後 ZIP](overleaf/DIC4_Overleaf_After.zip)

解壓或直接 Upload Project 後以 main.tex 為主檔。實際專案與編譯紀錄已補入 OVERLEAF_GUIDE.md；MCP 已安裝，驗證登入後的操作仍待完成。
