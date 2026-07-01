# Day 1 Prep Course 流程

這份文件描述 **SITCON Camp 2026 Day 1 Prep Course** 的兩小時建議流程。

這個 repo 只服務第一天先導課程，不是後續正式專案的 repo。

目標不是提前完成後續課程的專案，而是讓大家先完成一次：

```text
Google Docs 共編
→ 結構化文字
→ VS Code 開啟 repo
→ Coding Agent 產生 profile JSON
→ 看 diff
→ 展示頁呈現
```

---

## 0. 開場觀念

今天不是要考大家會不會寫程式。

今天要確認三件事：

1. 帳號和工具能不能用。
2. 你能不能把想法寫成 Agent 看得懂的文字。
3. 你能不能看懂 Agent 改了哪些檔案。

---

## 1. Google Docs 共編自我介紹

先在 Google Docs 裡用簡單 Markdown 寫自我介紹。

建議格式：

```markdown
## 暱稱

## 一句話介紹

## 我有興趣的主題

- AI
- 前端
- 開放資料

## 我的技術陣營

- OS：Linux
- Browser：Firefox
- Editor：VS Code
```

這一步的重點不是 Markdown 語法，而是理解：

> 有結構的文字，比一大坨文字更容易被人和 AI 理解。

---

## 2. Google Docs 版本紀錄

看 Google Docs 的版本紀錄，理解：

- 誰改了什麼
- 什麼時候改的
- 如何回到舊版本

接著帶到 Git / GitHub：

| Google Docs | 程式專案 |
|---|---|
| 文件 | repo 裡的檔案 |
| 版本紀錄 | commit history |
| 建議模式 | pull request |
| 誰改了哪裡 | diff |

---

## 3. VS Code 開啟小隊 repo

在 VS Code 中開啟這個小隊 repo。

只需要先認識：

- Explorer：看檔案
- Editor：編輯檔案
- Terminal：執行指令
- Source Control：看 diff
- Coding Agent：協助修改 repo

---

## 4. 寫 profile note

複製：

```text
notes/profile-note.template.md
```

成為自己的檔案：

```text
notes/<GitHub 帳號>.md
```

填寫願意公開的內容。

---

## 5. 請 Coding Agent 產生 JSON

請 Coding Agent 依照 `tasks/01-create-profile.md` 建立：

```text
profiles/<GitHub 帳號>.json
```

---

## 6. 看 diff

不要直接相信 Agent 的結果。

請在 Source Control 檢查：

- 新增了哪些檔案
- JSON 內容是否正確
- 有沒有出現不該公開的資訊
- faction 代號是否合理

---

## 7. 執行檢查與預覽

```bash
npm run validate
npm run stats
npm run dev
```

看到自己出現在展示頁上，就完成 Prep Course 核心任務。

---

## 8. 收束

今天走過的流程：

```text
想法
→ 結構化文字
→ Agent 產生檔案
→ 人類檢查 diff
→ 前端展示
```

後續課程會延續這個工作方式，但這個 repo 的任務只到 Prep Course 的工具測通、profile 建立、展示頁預覽與 diff 檢查。
