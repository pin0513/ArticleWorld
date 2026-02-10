# ArticleWorld - 文章撰寫生態系統

> **v2.0** - 整合七大寫作風格系統與完整工作流

完整的內容創作解決方案（Claude Code Skills），從企劃、研究、撰寫、編輯到品質把關。

---

## ✨ v2.0 新特性

### 🎯 完整整合
- ✅ 整合 team002 和 article-* 技能
- ✅ 整合七大寫作風格系統（教練/故事/商業/勵志/厚黑學/哲學反思/Blog）
- ✅ 整合去 AI 味機制
- ✅ 整合品質門檻把關（≥8/10）

### 📁 新架構（符合 A-Team 規範）

```
ArticleWorld/
├── CLAUDE.md                         ← 團隊通用指示
├── SKILL.md                          ← 入口檔案
├── README.md                         ← 本檔案
├── .claude/
│   ├── agents/
│   │   ├── article-consult.md        ← 總協調者
│   │   ├── planning/
│   │   │   ├── article-planner.md
│   │   │   └── article-researcher.md
│   │   ├── writing/
│   │   │   ├── article-writer.md
│   │   │   └── copywriter.md
│   │   └── quality/
│   │       ├── article-editor.md
│   │       └── article-analytics.md
│   ├── skills/
│   │   ├── writing-styles/SKILL.md   ← 七大風格系統
│   │   ├── anti-ai-writing/SKILL.md  ← 去 AI 味準則
│   │   └── content-formulas/SKILL.md ← 內容公式集
│   └── rules/
│       ├── quality-gate.md           ← 品質門檻 ≥8/10
│       └── content-integrity.md      ← 內容誠信
└── references/
    └── writing-style.md              ← 七大風格大師對照表（完整版）
```

---

## 🚀 快速開始

### 安裝

```bash
# 建立符號連結到全域 skills
ln -s /Users/paul_huang/AgentProjects/ArticleWorld ~/.claude/skills/ArticleWorld

# 或使用相對路徑
cd ~/.claude/skills
ln -s ~/AgentProjects/ArticleWorld ArticleWorld
```

### 使用

```bash
# 在 Claude Code 中呼叫
/ArticleWorld 寫一篇關於 AI 團隊的文章

# 或提供素材
/ArticleWorld
我有以下對話記錄：
[貼上素材]
請幫我整理成文章
```

---

## 📖 核心功能

### 1. 七大寫作風格系統

| 風格 | 核心問句 | 適用場景 |
|------|---------|---------|
| 教練 | 「你自己怎麼看？」 | 提問引導、自我覺察 |
| 故事 | 「然後呢？」 | 細節沉浸、情感共鳴 |
| 商業 | 「怎麼做才有效？」 | 數據驅動、框架清晰 |
| 勵志 | 「怎麼活才有意義？」 | 情感賦能、信念改變 |
| 厚黑學 | 「人性的真相是什麼？」 | 揭露人性、冷靜分析 |
| 哲學反思 | 「這一切意味著什麼？」 | 深度思考、拆解重建 |
| Blog | 「我怎麼看這件事？」 | 個人觀點、靈活表達 |

**完整大師對照表**：`references/writing-style.md`

涵蓋 20+ 位英文與華文世界代表作者，包含：
- Michael Bungay Stanier、Brene Brown、Marshall Goldsmith（教練）
- Malcolm Gladwell、Peter Hessler、柴靜（故事）
- Jim Collins、Seth Godin、劉潤（商業）
- Paul Graham、Joel Spolsky、萬維鋼（Blog）
- 等等...

---

### 2. 去 AI 味機制

**禁用句型自動檢測**：
- ❌ 「不是...而是...」「在某種程度上」
- ❌ 「總的來說」「讓我們共同期待」
- ❌ 「多維度」「賦能」「範式轉換」

**人味三問檢查**：
1. 有沒有具體細節？（時間/地點/數字）
2. 有沒有作者的聲音？（立場/情緒）
3. 敢不敢不完美？（承認不確定）

---

### 3. 品質門檻把關

所有內容必須達到 **8/10 分**以上：

| 評分維度 | 說明 |
|----------|------|
| 受眾吸引力 | 目標受眾是否會點開並讀完 |
| 非受眾擴散力 | 非目標受眾是否也會分享 |
| FB 適配度 | 標題/分段/互動性 |
| IG 適配度 | 視覺/前150字/Hashtag |
| Blog 適配度 | 深度/SEO/收藏價值 |
| LinkedIn 適配度 | 專業度/洞察/職涯價值 |

**未達標自動退回對應階段修正。**

---

### 4. 內容誠信保證

**AI 絕對不會編造**：
- 場景、故事
- 對話、經驗
- 時間、地點、人物
- 情緒反應

**所有具體細節必須來自用戶提供的素材。**

沒有素材時：
- ✅ 使用技術事實
- ✅ 標註留白 `[此處可加入您的經驗]`
- ❌ 不編造故事

---

## 🎯 工作流程

```
使用者提供主題/素材
          ↓
┌─────────────────────┐
│  Phase 1: 企劃與研究  │
│  • article-planner  │
│  • article-researcher│
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│  Phase 2: 撰文與編輯  │
│  • article-writer   │
│  • copywriter       │
│  • article-editor   │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│  Phase 3: 品質把關   │
│  • article-analytics│
│  → 評分 ≥ 8/10 ?    │
└──────────┬──────────┘
           ├─ 通過 → 交付用戶
           └─ 未達標 → 退回修正
```

---

## 📊 適用內容類型

| 內容類型 | 推薦風格 | 長度 |
|----------|---------|------|
| 深度分析文章 | 商業/哲學反思 | 2000+ 字 |
| 個人經驗分享 | 故事/教練 | 1500+ 字 |
| 行銷文案 | 商業/勵志 | 800-1500 字 |
| 社群短文 | Blog/故事 | 300-800 字 |
| 專業部落格 | 商業/教練 | 1500+ 字 |

---

## 📦 最終交付物

```markdown
# 內容企劃案：[主題]

## 基本資訊
- 目標受眾：[...]
- 發布平台：[...]
- 寫作風格：[...]
- 品質評分：8.5/10 ✅

## 標題選項
1. [長標題 - SEO優化，60-80字]
2. [短標題 - 社群吸睛，15-25字]
3. [...]

## 社群文案
### Facebook
[150-300字文案 + #hashtags]

### Instagram
[文案 + 10-30個 #hashtags]

### LinkedIn
[300-500字專業文案 + #hashtags]

## 文章正文
### Meta 描述
[SEO用，150字內]

### 正文
[完整文章內容，1500-3000字]

## 品質評估
[各維度評分 + 改善建議]
```

---

## 🔧 技術細節

### 部署模式
**Subagent Mode** - 透過 Task tool 調度各 agents

### 團隊組成
- **Coordinator**: article-consult
- **Planning**: article-planner, article-researcher
- **Writing**: article-writer, copywriter
- **Quality**: article-editor, article-analytics

### 共用資源
- **Skills**: writing-styles, anti-ai-writing, content-formulas
- **Rules**: quality-gate, content-integrity
- **References**: writing-style.md（完整大師對照表）

---

## 📝 版本歷史

### v2.0 (2026-02-10)
- ✅ 整合 team002 和 article-* 技能
- ✅ 整合七大寫作風格系統
- ✅ 採用 A-Team 規範架構
- ✅ 建立完整的 agents/skills/rules 結構
- ✅ 整合 writing-style.md（7大風格大師對照表）

### v1.0 (2026-02-08)
- 初始版本，基礎工作流程

---

## 🤝 相關專案

- **A-Team** - AI Agent 團隊設計系統
- **Team002** - 文章撰寫團隊（已整合到本專案）

---

## 📄 授權

Private - 個人使用

## 👤 維護者

Paul Huang (@pin0513)

---

## 📍 專案位置

- **本地路徑**：`/Users/paul_huang/AgentProjects/ArticleWorld`
- **GitHub**：https://github.com/pin0513/ArticleWorld
- **全域 Skill**：`~/.claude/skills/ArticleWorld`

---

**開始使用**：`/ArticleWorld 寫一篇關於 [主題] 的文章`
