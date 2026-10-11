# 第 3 章實作｜查詢 Hacker News 公開熱門文章

## 目標
用唯讀 adapter 擷取最多 3 筆公開熱門文章，使用 JSON 格式供後續核對。

## 先確認參數

```bash
opencli hackernews top --help
```

本機 OpenCLI 1.8.8 顯示 `--limit` 用於設定筆數，並支援 `-f json`。

## 執行

```bash
opencli hackernews top --limit 3 -f json
```

## 驗收欄位
輸出應為 JSON 陣列，依實際回應檢查是否包含 `rank`、`id`、`title`、`score`、`author`、`comments`、`url`。資料會變動，請勿將任何一次查詢的故事內容或排名當作固定答案。

## 加做：儲存本次結果

```bash
opencli hackernews top --limit 3 -f json > hackernews-top.json
```

這會在目前資料夾建立或覆寫 `hackernews-top.json`。先確認目錄與檔名，再執行；不要把私人工作目錄或憑證資料納入公開 repo。

## 完成條件
解析 JSON、確認筆數不超過 3、核對一筆來源 URL。若網站/API 暫時無回應，記錄未完成，不要偽造輸出。

## 驗證狀態
`opencli hackernews top --limit 3 -f json` 已在 OpenCLI 1.8.8 實際執行成功；只核實命令與當次回應格式，不保證未來資料內容一致。
