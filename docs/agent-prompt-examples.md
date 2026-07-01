# Coding Agent Prompt 範例

這份文件提供學員可以直接複製修改的 prompt。

---

## 建立我的 profile

```text
請閱讀 notes/<我的 GitHub 帳號>.md，根據 schemas/profile.schema.json 和 data/faction-options.json，建立 profiles/<我的 GitHub 帳號>.json。

請注意：
- faction 欄位要使用固定代號，不要使用顯示名稱。
- 不要加入電話、Email、學校、班級、生日、年齡或其他個人資料。
- 如果我的描述不明確，請選最接近的代號並說明你的判斷。
- 建立完成後請告訴我改了哪些檔案，以及我應該檢查哪些欄位。
```

---

## 修正 profile 錯誤

```text
npm run validate 顯示 profiles/<我的 GitHub 帳號>.json 有錯誤。請根據錯誤訊息修正，但不要改動其他人的 profile。

修正後請說明：
- 錯誤原因
- 你修改了哪些欄位
- 我應該重新檢查哪些地方
```

---

## 改善 Showcase 視覺效果

```text
請改善這個展示頁的視覺效果，但保持現有功能：主輪播、成員卡片牆、faction 統計、點擊展開卡片。

視覺方向：
- 深色背景
- 亮色科技感點綴
- 幾何線條
- 年輕 hacker / builder 氣質
- 符合 SITCON Camp 2026 的社群感

限制：
- 不要新增大型框架。
- 不要用 innerHTML 插入學員提供的文字。
- 不要破壞 npm run validate、npm run stats、npm run build。
- 修改後請列出我應該手動測試的互動。
```

---

## 看 diff 後請 Agent 解釋

```text
請根據目前 git diff，說明你剛剛做了哪些修改。

請分成：
- 新增或修改的檔案
- 每個檔案修改目的
- 有哪些地方需要我人工確認
- 有沒有任何你不確定的假設
```
