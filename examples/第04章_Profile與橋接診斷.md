# 第 4 章實作｜診斷 Browser Bridge 與 profile

## 目標
辨認 CLI 是否看到瀏覽器橋接、有哪些 profile 已連線，以及是否必須先由使用者指定目標 profile。

## 診斷

```bash
opencli doctor
opencli profile list
```

若環境同時連線多個 Chrome profile，先讓使用者選定哪個 profile 可供本次任務使用；本例不替使用者擅自選擇或切換。只有在已確認正確 profile 後，才可設定別名：

```bash
opencli profile rename <contextId> work
opencli profile use work
```

`<contextId>` 是佔位說明，請以 `profile list` 的實際值替換；不要照貼尖括號。

## 判讀分支
- 擴充功能未連線：檢查是否已安裝並啟用官方 Browser Bridge，再重跑 `doctor`。
- 無 profile：先完成官方橋接設定，不要進行 browser 操作。
- 多個 profile 且未指定：停止，請使用者選擇。
- 目標 profile 明確且診斷正常：才進入下一章的唯讀頁面觀察。

## 完成條件
記錄診斷摘要與下一步，不記錄真實帳號、Cookie 或私密頁面內容。設定 profile 是本機持續設定變更；操作前必須確認目標。
