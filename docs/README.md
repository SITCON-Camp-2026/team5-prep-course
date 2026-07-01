# 文件導覽

這個 repo 的文件不是全部都要從頭讀完。不同角色在不同時間點，需要看的文件不同。

---

## 這個 repo 的文件分層

| 層次 | 主要讀者 | 目的 | 代表文件 |
|---|---|---|---|
| 入口導覽 | 所有人 | 快速理解這個 repo 是什麼、要怎麼開始 | `README.md` |
| Agent 執行規範 | Coding Agent、講師、助教 | 告訴 Agent 可以做什麼、不能做什麼、要遵守哪些資料規格 | `AGENTS.md` |
| 學員操作文件 | 學員、助教 | 讓學員照著完成先導課程任務 | `tasks/`、`notes/README.md`、`profiles/README.md` |
| 教學設計紀錄 | 講師、助教、未來維護者 | 說明為什麼這堂先導課程要這樣設計 | `docs/teaching-method.md` |
| 專案維護文件 | 助教、未來維護者、Coding Agent | 說明 repo 結構、資料規格、隱私邊界 | `docs/repo-structure.md`、`docs/privacy.md` |

---

## 不同角色應該怎麼讀？

### 學員

上課時主要看：

1. `README.md`
2. `tasks/01-create-profile.md`
3. `notes/profile-note.template.md`
4. `profiles/README.md`

學員不需要先理解整個 repo，也不需要閱讀完整教學設計。

---

### 助教

課前先看：

1. `README.md`
2. `docs/day1-flow.md`
3. `docs/privacy.md`
4. `docs/repo-structure.md`
5. `tasks/01-create-profile.md`
6. `tasks/02-build-showcase.md`

課中協助排除問題時，優先使用：

```bash
npm run validate
npm run stats
npm run dev
```

---

### 講師

課前建議先看：

1. `docs/teaching-method.md`
2. `docs/day1-flow.md`
3. `README.md`
4. `docs/agent-prompt-examples.md`

講師需要掌握的不只是操作步驟，而是這堂先導課程背後的教學意圖：

```text
自然語言
→ 結構化資料
→ Agent 修改 repo
→ 人類檢查 diff
→ 可視化成果
```

---

### Coding Agent

Coding Agent 應優先閱讀：

1. `AGENTS.md`
2. 使用者指定的 `tasks/*.md`
3. 需要修改的相關檔案
4. `schemas/profile.schema.json`
5. `data/faction-options.json`

Coding Agent 不需要知道講師的設計討論脈絡，也不應把教學設計文件改寫成冗長背景故事。

---

### 未來維護者

如果未來要複製或改版這份 template，建議先看：

1. `docs/teaching-method.md`
2. `docs/repo-structure.md`
3. `AGENTS.md`
4. `src/main.js`
5. `src/styles.css`

改版時請優先保持：

- 先導課程範圍清楚
- 學員操作負擔低
- Agent 任務可檢查
- profile 資料可公開
- 前端展示有成就感但不過度複雜

---

## 文件撰寫原則

這個 repo 的文件應該遵守：

1. **不要把對談脈絡寫進文件。** 文件應該像課程材料，而不是會議紀錄。
2. **不要讓學員讀不必要的背景。** 學員文件要短、可操作、低壓力。
3. **不要讓 Agent 猜教學意圖。** Agent 需要的是明確規格、限制和任務。
4. **把教學方法留下來，但寫成設計原則。** 讓未來講師與助教知道為什麼這樣安排。
5. **每份文件都要有清楚讀者。** 寫文件前先想：誰會在什麼時候讀？讀完要做什麼？
