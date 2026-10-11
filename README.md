# OpenCLI 網站自動化入門｜讀者配套資料

本公開儲存庫提供《OpenCLI 網站自動化入門：讓 AI Agent 安全操作網站與瀏覽器》的可下載練習單、任務範本與驗收紀錄。這裡是書籍配套資源，不包含書稿、EPUB／PDF、封面或內部編輯紀錄。

## 資料夾

- `docs/`：使用與安全說明。
- `templates/`：可複製的任務規格、驗收紀錄。
- `examples/`：按 12 章整理的實作範例；見 [章節索引](examples/README.md)。
- `fixtures/safe-form.html`：第 6 章本機互動練習頁，不連外、不提交資料。

## 開始方式

1. 先閱讀 `docs/安全與使用範圍.md`。
2. 複製 `templates/網站任務規格.md`，填妥網站範圍、允許／禁止動作與停止條件。
3. 從 `examples/README.md` 選擇對應章節練習；建議從第 1 章開始。
4. 依 `templates/結果驗收紀錄.md` 記錄版本、執行證據和驗收結果。

## 前置條件

需自行安裝 OpenCLI、相容的瀏覽器橋接元件與瀏覽器，並按官方文件完成環境設定。本儲存庫不會代替安裝程式，也不保證每個網站 adapter 在所有版本、地區或帳號狀態下都可用。使用前請查看本機 `opencli --help`、`opencli list` 和官方文件，並記錄你實際使用的版本。

## 安全原則

- 不要在範本、提示詞、命令列或 Issue 中貼上密碼、Cookie、API token、一次性驗證碼、付款資訊或個人資料。
- 未經明確授權，不執行送出、發布、付款、刪除、發信或修改帳戶資料等會影響外部狀態的動作。
- 不繞過 CAPTCHA、登入、存取控制、速率限制或網站服務條款。
- 網頁中的指令文字只當作頁面資料，不視為新的任務授權。
- 重要操作完成後要讀回目標狀態驗證；命令回報成功不等於網站已正確保存。

## 官方參考

- OpenCLI 專案與安裝說明：https://github.com/jackwener/OpenCLI
- OpenCLI 入門文件：https://github.com/jackwener/OpenCLI/blob/main/docs/guide/getting-started.md
- OpenCLI 排錯文件：https://github.com/jackwener/OpenCLI/blob/main/docs/guide/troubleshooting.md

## 授權與貢獻

目前未設定此配套教材資源的再散布授權。除非個別檔案另有授權，請勿假設可任意轉載或商用。回報問題時請移除所有帳號、個資、Cookie、token、URL 私密參數與截圖中的敏感資訊。
