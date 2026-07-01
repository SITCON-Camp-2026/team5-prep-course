# SITCON Camp 2026 Prep Course Team Showcase Template

這是一份給 **SITCON Camp 2026 Day 1 Prep Course** 使用的小隊 repo template。

這個 repo 只專注於第一天先導課程：協助學員測通 GitHub、VS Code、Coding Agent 與基本前端展示流程，並為後續課程建立共同工作方式。

第一天 Prep Course 的目標不是做出完整專案，而是讓每位學員完成一次最小閉環：

```text
自然語言描述
→ Coding Agent 轉成結構化 JSON
→ schema 檢查
→ 前端頁面展示
→ 看 diff
→ commit / PR
```

最後每個小隊會有一個可以公開瀏覽的展示頁，包含：

- GitHub 頭貼與小隊成員卡片
- 自動輪播展示
- 滑鼠 hover / click 互動
- OS、瀏覽器、編輯器陣營統計
- 適合 SITCON Camp 2026 的科技社群視覺風格

---

## 誰應該讀哪份文件？

如果你是學員，從這份 `README.md` 開始，接著照 `tasks/01-create-profile.md` 操作即可。

如果你是助教或講師，建議先看：

- `docs/README.md`：文件導覽與閱讀順序
- `docs/day1-flow.md`：先導課程流程
- `docs/teaching-method.md`：教學方法與設計取捨
- `docs/privacy.md`：公開資料與隱私提醒

如果你是 Coding Agent，請優先閱讀 `AGENTS.md` 與使用者指定的 `tasks/*.md`。

---

## 快速開始

請在 VS Code 開啟這個資料夾，接著在 Terminal 執行：

```bash
npm install
npm run dev
```

啟動後，瀏覽器會顯示本機預覽網址。通常會是：

```text
http://localhost:5173/
```

---

## 常用指令

```bash
npm run dev       # 本機預覽展示頁
npm run validate  # 檢查 profiles/*.json 是否符合規格
npm run stats     # 統計各陣營人數
npm run build     # 產生可部署的靜態網站
```

---

## 專案結構

```text
.
├── AGENTS.md                  # 給 Coding Agent 閱讀的英文規則
├── README.md                  # 你現在正在看的文件
├── data/
│   └── faction-options.json   # OS / 瀏覽器 / 編輯器陣營代號
├── docs/
│   ├── README.md              # 文件導覽與閱讀順序
│   ├── day1-flow.md           # 先導課程流程
│   ├── privacy.md             # 公開資料注意事項
│   ├── repo-structure.md      # 專案結構說明
│   └── teaching-method.md     # 教學方法與設計取捨
├── notes/
│   ├── README.md              # 自然語言草稿填寫說明
│   └── profile-note.template.md
├── profiles/
│   └── README.md              # profile JSON 說明
├── schemas/
│   └── profile.schema.json    # profile JSON 規格
├── scripts/
│   ├── validate-profiles.mjs  # 檢查 profile 資料
│   └── faction-stats.mjs      # 統計 faction
├── src/
│   ├── main.js                # 前端主程式
│   └── styles.css             # 視覺與互動樣式
└── tasks/
    ├── 01-create-profile.md   # 任務一：建立個人 profile
    └── 02-build-showcase.md   # 任務二：更新展示頁
```

---

## Prep Course 你會做什麼？

### 1. 寫一份自然語言草稿

從 `notes/profile-note.template.md` 複製一份，填入你願意公開的內容。

你不用手寫 JSON，也不用一開始就知道格式怎麼寫。

### 2. 請 Coding Agent 幫你轉成 JSON

請 Agent 閱讀你的草稿，根據 `schemas/profile.schema.json` 和 `data/faction-options.json`，產生：

```text
profiles/<你的 GitHub 帳號>.json
```

### 3. 檢查 Agent 改了什麼

在 VS Code 的 Source Control 裡看 diff。

你要確認：

- GitHub 帳號是否正確
- 顯示名稱是否是你想公開的名稱
- 一句話介紹是否符合你的意思
- 興趣有沒有被亂改或亂加
- 陣營是否合理
- 有沒有出現你不想公開的個人資料

### 4. 執行檢查

```bash
npm run validate
npm run stats
```

### 5. 預覽展示頁

```bash
npm run dev
```

看到自己出現在小隊展示頁上，就完成 Prep Course 的核心任務。

---

## 公開資料提醒

這個展示頁可能會被公開瀏覽。請只填你願意公開的內容。

不要填：

- 電話、Email、LINE、Discord
- 學校、班級、住址
- 生日、年齡
- 不想公開的社群帳號
- 任何你不希望陌生人看到的資訊

可以填：

- GitHub 帳號
- 暱稱或顯示名稱
- 一句話介紹
- 1 到 3 個興趣主題
- 你想代表自己的 OS / 瀏覽器 / 編輯器陣營

---

## 重要觀念

Coding Agent 不是答案產生器，而是會修改 repo 的協作者。

所以每次 Agent 改檔後，都要看 diff：

```text
Agent 產生修改
→ 人類檢查 diff
→ 確認沒有問題
→ 才 commit / PR
```

這就是 Prep Course 最重要的練習：先學會讓 Agent 修改檔案，也學會由人類負責檢查與確認。
