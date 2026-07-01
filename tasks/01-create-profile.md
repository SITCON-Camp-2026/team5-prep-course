# 任務一：請 Coding Agent 建立我的 profile JSON

這個任務的目標是：

```text
自然語言草稿
→ Coding Agent 產生 JSON
→ schema 驗證
→ 人類檢查 diff
```

---

## 你要先做什麼？

1. 複製 `notes/profile-note.template.md`。
2. 改成自己的檔案，例如：

```text
notes/<你的 GitHub 帳號>.md
```

3. 填完你願意公開的內容。

---

## 可以給 Coding Agent 的 prompt

你可以把下面這段貼給 Coding Agent：

```text
請閱讀我的 notes/<我的 GitHub 帳號>.md，並根據 schemas/profile.schema.json 和 data/faction-options.json，建立 profiles/<我的 GitHub 帳號>.json。

要求：
- github 必須使用我的 GitHub 帳號。
- displayName 使用我想公開顯示的名稱。
- tagline 壓成一句話，不要超過 40 字。
- interests 保留 1 到 3 個主題。
- faction.os、faction.browser、faction.editor 必須使用 data/faction-options.json 裡的代號。
- 如果我的描述不明確，請選最接近的代號，並在回覆中說明你的判斷。
- 如果真的無法判斷，請使用 other。
- 不要新增電話、Email、學校、班級、年齡、生日或其他個人資料。
- 建立完成後，請列出你建立了哪個檔案，以及我需要檢查哪些欄位。
```

---

## 建立完成後請檢查

請在 VS Code Source Control 裡看 diff。

你要確認：

- GitHub 帳號是否正確
- 顯示名稱是不是你想公開的名稱
- 一句話介紹有沒有被改得不像你
- interests 是否只有 1 到 3 個
- faction 是否符合你的偏好
- 有沒有出現你不想公開的個人資料

---

## 執行檢查

```bash
npm run validate
```

如果出現錯誤，請請 Coding Agent 修正。

---

## 完成標準

你完成這個任務時，repo 裡應該會多出：

```text
profiles/<你的 GitHub 帳號>.json
```

而且：

```bash
npm run validate
```

應該要通過。
