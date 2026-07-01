# 專案結構說明

這份 template 把「給人讀的文件」、「給 Agent 讀的規則」、「給程式讀的資料」分開。

更完整的閱讀順序請先看 `docs/README.md`。如果要理解教學設計取捨，請看 `docs/teaching-method.md`。

---

## 根目錄

```text
AGENTS.md
README.md
package.json
index.html
```

- `AGENTS.md`：給 Coding Agent 看的英文執行規範，不放教學推演。
- `README.md`：給學員、助教、講師的專案入口。
- `package.json`：npm 指令與開發依賴。
- `index.html`：前端展示頁入口。

---

## notes/

學員先用自然語言寫草稿。

```text
notes/<GitHub 帳號>.md
```

這是給 Coding Agent 理解偏好的輸入。

---

## profiles/

Coding Agent 會根據 `notes/` 產生 JSON：

```text
profiles/<GitHub 帳號>.json
```

這是前端展示頁會讀取的資料。

---

## schemas/

```text
schemas/profile.schema.json
```

這份檔案定義 profile JSON 的規格。

VS Code 會根據它提示 JSON 格式問題。

---

## data/

```text
data/faction-options.json
```

這份檔案定義 faction 可以使用的固定代號。

例如：

```json
"editor": "vscode"
```

顯示時才轉成：

```text
VS Code
```

---

## src/

```text
src/main.js
src/styles.css
```

前端展示頁的主要程式和樣式。

`src/main.js` 會讀取 `profiles/*.json`，產生：

- 主輪播
- 成員卡片牆
- faction 統計
- 點擊展開的 profile dialog

---

## scripts/

```text
scripts/validate-profiles.mjs
scripts/faction-stats.mjs
```

用來檢查資料與統計陣營。

```bash
npm run validate
npm run stats
```

---

## docs/

```text
docs/README.md
docs/day1-flow.md
docs/teaching-method.md
docs/privacy.md
docs/repo-structure.md
docs/agent-prompt-examples.md
```

- `docs/README.md`：文件導覽，說明不同角色應該讀哪些文件。
- `docs/day1-flow.md`：先導課程流程，適合講師與助教課前閱讀。
- `docs/teaching-method.md`：教學方法與設計取捨，保留高層次課程設計，不記錄私人對談脈絡。
- `docs/privacy.md`：公開資料與隱私提醒。
- `docs/repo-structure.md`：你現在正在看的文件。
- `docs/agent-prompt-examples.md`：可複製使用的 Coding Agent prompt 範例。

---

## tasks/

放給學員和 Coding Agent 使用的任務說明。

建議照順序做：

1. `tasks/01-create-profile.md`
2. `tasks/02-build-showcase.md`
