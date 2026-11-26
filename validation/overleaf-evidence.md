# Overleaf 與 MCP 證據狀態

日期：2026-11-26，Asia/Taipei。

| 版本 | 實際 Overleaf 專案 | PDF | 編譯檢查 |
| --- | --- | --- | --- |
| 修改前 v0 | [DietSense DIC4 Before](https://www.overleaf.com/project/6b07e4d866226db300e5848a) | [2 頁](overleaf/DietSense_DIC4_Before.pdf) | Compile finished；Errors 0；Warnings 0 |
| 修改後 v1 | [DietSense DIC4 After](https://www.overleaf.com/project/6b07e69a0b58b245f496dacc) | [6 頁](overleaf/DietSense_DIC4_After.pdf) | Compile finished；Errors 0；Warnings 0 |

## 實際操作
使用者要求改用平常已登入的 Chrome。Agent 透過 Computer Use 操作一般 Chrome：在專案列表選 New project → Existing project (.zip)，分別匯入 Before／After ZIP、重新命名、檢查編譯與 PDF 預覽、開啟 View logs 核對錯誤／警告，並下載兩份 PDF。以上是真實 Overleaf 網站操作，並非本機編譯。編譯紀錄另有 underfull hbox 的排版資訊；修改後為 3 則 Info，不影響 PDF 產生。

下載檔案的頁數、SHA256、Git blob SHA 及專案連結見 [下載驗證](overleaf-downloads.json)。網站畫面曾在操作過程中目視確認；未另外保存可繳交的螢幕截圖。專案連結為擁有者的編輯入口，未開啟匿名分享，其他帳號可能需要授權；GitHub 上的 PDF 可直接閱讀。

## MCP 安裝及限制
已安裝 overleaf-web-mcp 1.4.1，註冊為 overleaf，完成 stdio initialize 與 tools/list，列出 32 個工具，協定版本 2025-11-25。去識別安裝紀錄見 [mcp-installation.json](mcp-installation.json)。

MCP 專用瀏覽器的登入遭 Google 安全機制阻擋，auth_status 沒有取得有效登入。因此沒有經 MCP 讀取、寫入或編譯 Overleaf 專案的成功紀錄。依使用者指示改由一般 Chrome 完成匯入與編譯；這不能視為教授「Agent + Overleaf MCP」要求已全部完成。

沒有上傳 cookie、token、瀏覽器 profile、登入內容或原始 session log。before 是本次依 DIC3 新建立的英文基準稿，不是先前既存的 Overleaf 歷史版本。
