# 任務二：更新小隊 Showcase 頁面

這個任務的目標是讓 `profiles/*.json` 變成公開網頁上的小隊展示。

目前前端已經會自動讀取：

```text
profiles/*.json
```

並產生：

- 主視覺輪播
- 成員卡片牆
- faction 技術陣營統計
- 點擊卡片展開細節
- 滑鼠 hover 動效

---

## 可以給 Coding Agent 的 prompt

```text
請閱讀 src/main.js、src/styles.css、data/faction-options.json 和 profiles/*.json，協助改善小隊 Showcase 頁面。

目標：
- 保持 SITCON Camp 2026 的科技社群感：深色底、亮色點綴、幾何線條、年輕 hacker / builder 氣質。
- 保留主輪播、成員卡片牆、faction 統計三個主要區塊。
- 讓滑鼠 hover / click 有明顯但不干擾閱讀的互動效果。
- 不要新增大型框架。
- 不要使用 innerHTML 插入學員提供的文字。
- 修改後請說明改了哪些檔案，以及我應該檢查哪些互動。
```

---

## 檢查重點

請檢查：

- `npm run dev` 是否能正常啟動
- 頁面是否顯示每位成員
- GitHub 頭貼是否正常顯示
- faction 統計是否合理
- 輪播是否會自動播放
- 滑鼠移到卡片上是否有互動
- 點擊卡片是否能展開
- 手機尺寸是否不會爆版

---

## 完成標準

```bash
npm run validate
npm run stats
npm run build
```

三個指令都能通過，才算完成。
