# profiles 資料夾

這個資料夾會放每位學員的公開 profile JSON。

檔名建議使用：

```text
profiles/<GitHub 帳號>.json
```

例如：

```text
profiles/octocat.json
```

---

## 重要：你不需要手寫 JSON

第一天的建議流程是：

1. 先在 `notes/` 裡寫自然語言草稿。
2. 請 Coding Agent 根據草稿產生 JSON。
3. 用 `npm run validate` 檢查。
4. 在 VS Code Source Control 裡看 diff。
5. 確認內容沒問題後再 commit。

---

## profile JSON 格式

```json
{
  "$schema": "../schemas/profile.schema.json",
  "github": "octocat",
  "displayName": "小火龍",
  "tagline": "想把點子做成可以互動的網頁",
  "interests": ["AI", "前端", "開放資料"],
  "faction": {
    "os": "linux",
    "browser": "firefox",
    "editor": "vscode"
  }
}
```

---

## faction 欄位請使用固定代號

請不要填顯示名稱，例如不要填 `VS Code`。

應該填固定代號：

```json
"editor": "vscode"
```

可用代號請看：

```text
data/faction-options.json
```

---

## 公開資料提醒

這個資料夾裡的內容可能會出現在公開網頁上。

請不要放：

- 電話、Email、LINE、Discord
- 學校、班級、住址
- 生日、年齡
- 不想公開的個人資訊
