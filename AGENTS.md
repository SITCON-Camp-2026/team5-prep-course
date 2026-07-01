# AGENTS.md

This repository is a team template for the **SITCON Camp 2026 Day 1 Prep Course**.

This repo is intentionally scoped to the preparatory session only. It is not the full Day 2 software engineering project repo.

The Prep Course goal is not to build a full project. The goal is to let students complete a minimal, safe workflow:

1. describe themselves and their preferences in natural language;
2. let a Coding Agent convert that description into structured JSON;
3. validate the JSON against a schema and fixed faction options;
4. render a public-facing showcase page with GitHub avatars, member cards, carousel interactions, and faction statistics;
5. inspect the diff before committing.

## Language rules

- Keep this `AGENTS.md` in English so Coding Agents can follow it reliably.
- Student-facing documents must be written in Traditional Chinese used in Taiwan.
- Keep explanations beginner-friendly. The target audience is mostly high-school students with some programming exposure.
- Avoid PRC vocabulary. Use Taiwan terms such as「資料夾」「檔案」「設定」「執行」「作業系統」「瀏覽器」「編輯器」.

## Repository purpose

This repo should remain a lightweight template for each camp team during the Day 1 Prep Course. It should be easy to clone, run, inspect, and modify during a two-hour prep session.

Do not turn this into the main camp project or a large framework-heavy project. Prefer simple, inspectable HTML, CSS, and JavaScript.

Keep documentation audience separation clear:

- `AGENTS.md` is the execution contract for Coding Agents.
- `README.md`, `tasks/`, `notes/`, and `profiles/` are student-facing or student-adjacent.
- `docs/teaching-method.md` records teaching design principles for instructors and TAs.
- Do not add private conversation history or meeting-style reasoning traces to repository documents.

## Privacy and safety rules

The final page may be publicly viewable. Treat all profile data as public.

Never add or infer the following fields:

- real name, unless the student explicitly says they want it public;
- school, class, grade, age, birthday;
- email, phone, LINE, Discord, private social accounts;
- address or location;
- health, religion, politics, family background, or other sensitive information;
- weaknesses or embarrassing self-disclosures.

Use GitHub username only for avatar and profile link. Students may choose a display name or nickname.

If the student's note contains private data, do not copy it into JSON. Tell the student which information was intentionally excluded.

## Profile workflow

Students should not manually write JSON as the default path.

Expected flow:

1. The student writes a natural-language note using `notes/profile-note.template.md`.
2. The agent reads that note, `schemas/profile.schema.json`, and `data/faction-options.json`.
3. The agent creates `profiles/<github>.json`.
4. The agent checks that all faction values use fixed lowercase IDs.
5. The student reviews the diff before commit.

Profile JSON format:

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

## Faction mapping rules

Use IDs from `data/faction-options.json`, not display labels.

Examples:

- Use `vscode`, not `VS Code`, `vscode `, `Visual Studio Code`, or `vs code`.
- Use `macos`, not `Mac`, `macOS`, or `Mac OS`.
- Use `firefox`, not `Firefox`.

If a student's answer is ambiguous:

1. choose the closest listed ID if reasonable;
2. explain the assumption in the response;
3. use `other` only when no listed option fits.

Do not infer faction values from the classroom computer. The classroom machines are preinstalled for the course and may not represent the student's actual preference. Ask the student to describe what they usually use or what faction they want to represent.

## Coding and design rules

- Keep the frontend visually rich but understandable.
- Prefer vanilla HTML/CSS/JavaScript unless the instructor explicitly asks for more.
- Do not introduce new runtime dependencies without a clear reason.
- Keep animations performant and accessible.
- Respect `prefers-reduced-motion`.
- Do not use `innerHTML` for student-provided text. Use `textContent` and DOM APIs.
- GitHub avatar URLs may use `https://github.com/<github>.png`.
- GitHub profile links may use `https://github.com/<github>`.

## Agent behavior rules

- Read the relevant task file in `tasks/` before editing.
- Keep changes small and reviewable.
- Explain which files were changed and why.
- Tell students what to inspect in the diff.
- Do not commit, push, merge, or deploy unless the user explicitly asks.
- Do not delete student profile files unless explicitly requested.
- Do not rewrite the entire project to make a small change.
- If validation fails, fix the data or explain the issue clearly.

## Useful commands

```bash
npm install
npm run dev
npm run validate
npm run stats
npm run build
```

Use `npm run validate` after adding or editing profiles.
Use `npm run stats` to preview faction counts in the terminal.
Use `npm run dev` to preview the showcase locally.
