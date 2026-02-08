# ArticleWorld - 文章寫作生態系統

完整的內容創作解決方案（Claude Code Skills）

## 簡介

ArticleWorld 是專為內容創作與文章寫作設計的完整生態系統，涵蓋從內容企劃、主題研究、文章撰寫、編輯審稿、行銷包裝到品質分析的全流程。

## 📁 技能組成

```
ArticleWorld/
├── article-consult/          內容生產顧問與流程協調
├── article-planner/          內容企劃專家
├── article-researcher/       主題研究專家
├── article-writer/           內容撰寫專家
├── article-editor/           總編輯審稿專家
├── article-marketing/        行銷包裝專家
├── article-analytics/        品質分析專家
└── article-content-plan.md   內容規劃範本
```

## 🎯 完整工作流程

### 階段 1: 內容企劃 (`article-planner`)

**職責**:
- 主題定調
- 受眾分析
- 內容大綱規劃
- 最終企劃案輸出

**輸出**:
- 主題定位
- 目標受眾
- 內容大綱
- 關鍵訊息

---

### 階段 2: 主題研究 (`article-researcher`)

**職責**:
- Wiki 定義查詢
- 學術觀點蒐集
- 社會風向分析
- 正反論述整理

**特色**:
- 偏向「觀點、反思、社會性」
- 提供哲學反思角度
- 有趣面向挖掘

**輸出**:
- 主題背景資料
- 多元觀點整理
- 引用來源

---

### 階段 3: 內容撰寫 (`article-writer`)

**職責**:
- Storytelling 敘事
- 哲學反思融入
- 學習教練視角
- 產業想像

**寫作風格**:
- 有靈魂的內容
- 深度反思
- 故事性敘事

**輸出**:
- 文章初稿
- 完整內容

---

### 階段 4: 編輯審稿 (`article-editor`)

**職責**:
- 內容審查
- 文字潤稿
- 標題腦力激盪
- 邏輯完整性檢查

**審查重點**:
- 邏輯是否完整
- 文字是否流暢
- 是否符合目標受眾

**輸出**:
- 定稿文章
- 標題建議
- 修改意見

---

### 階段 5: 行銷包裝 (`article-marketing`)

**職責**:
- 標題優化
- 行銷文案撰寫
- 關鍵字/Hashtag 策略
- SEO 優化

**輸出**:
- 吸引力標題
- 社群文案
- SEO 關鍵字
- Hashtag 建議

---

### 階段 6: 品質分析 (`article-analytics`)

**職責**:
- 受眾評分
- 平台適配度分析
- 品質門檻把關

**品質標準**:
- ≥ 8/10 才能發布
- 未達標退回修正

**輸出**:
- 品質評分
- 改善建議
- 發布建議

---

## 🚀 使用方式

### 方式一：使用總調度者

```bash
# 安裝 article-consult（一站式服務）
ln -s ~/AgentProjects/ArticleWorld/article-consult ~/.claude/skills/article-consult

# 在 Claude Code 中呼叫
/article-consult
```

**article-consult** 會自動協調所有階段的 skills，您只需提供主題。

### 方式二：使用單一技能

```bash
# 安裝特定 skill
ln -s ~/AgentProjects/ArticleWorld/article-writer ~/.claude/skills/article-writer

# 呼叫特定功能
/article-writer
/article-editor
/article-marketing
```

### 方式三：批次安裝全部

```bash
cd ~/AgentProjects/ArticleWorld
for skill in article-*/; do
  ln -s "$(pwd)/${skill%/}" ~/.claude/skills/"${skill%/}"
done
```

---

## 📖 使用範例

### 範例 1: 完整內容製作流程

```
使用者: "我想寫一篇關於 AI 對教育影響的文章"

/article-consult 自動執行流程:
1. article-planner  → 主題定調、受眾分析
2. article-researcher → Wiki、學術觀點、社會討論
3. article-writer → 撰寫初稿（故事性+反思）
4. article-editor → 審稿潤飾、標題建議
5. article-marketing → 行銷文案、SEO 關鍵字
6. article-analytics → 品質評分、發布建議

輸出:
- 定稿文章
- 3-5 個標題選項
- 社群文案（Facebook/LinkedIn/Twitter）
- SEO 關鍵字清單
- 品質報告
```

### 範例 2: 單獨使用研究功能

```
使用者: "幫我研究『遠距工作』這個主題"

/article-researcher:
1. Wiki 定義查詢
2. 學術研究整理
3. 社會風向分析（正面/反面）
4. 有趣觀點挖掘

輸出:
- 主題背景知識
- 學術研究摘要
- 正反論述整理
- 引用來源清單
```

### 範例 3: 行銷包裝既有文章

```
使用者: "我有一篇文章，幫我做行銷包裝"

/article-marketing:
1. 標題優化（A/B 測試）
2. 社群文案撰寫
3. Hashtag 策略
4. SEO 關鍵字

輸出:
- 5 種標題變化
- Facebook/LinkedIn/Twitter 文案
- 10-15 個 Hashtags
- SEO meta description
```

---

## 🔗 依賴工具

本專案使用以下 AITools（請從 [AITools](https://github.com/pin0513/AITools) 安裝）：

### 必要依賴

- `avoid-ai-article` - 避免 AI 味寫作準則
- `md-generation-standard` - Markdown 生成標準

安裝方式：
```bash
ln -s ~/AgentProjects/AITools/skills/avoid-ai-article ~/.claude/skills/avoid-ai-article
ln -s ~/AgentProjects/AITools/skills/md-generation-standard ~/.claude/skills/md-generation-standard
```

### 可選依賴

- `market-research` - 市場研究
- `academic-research` - 學術研究
- `industry-research` - 產業研究

---

## ✨ 特色功能

### 1. 去 AI 味寫作

整合 `avoid-ai-article` 準則，確保文章有人味：
- 避免空洞轉折詞
- 禁用罐頭結尾
- 避免宏大修飾
- 增加具體細節
- 展現作者聲音

### 2. 多元觀點研究

不只提供單一觀點：
- 正反論述
- 學術 vs 實務
- 理想 vs 現實
- 哲學反思

### 3. 品質門檻把關

嚴格的品質標準：
- 8/10 分以上才能發布
- 受眾適配度分析
- 平台適配建議
- 改善方向明確

---

## 📊 技能對照表

| 技能 | 階段 | 輸入 | 輸出 |
|------|------|------|------|
| `article-consult` | 總調度 | 主題 | 完整素材包 |
| `article-planner` | 企劃 | 主題想法 | 企劃案 |
| `article-researcher` | 研究 | 主題 | 研究資料 |
| `article-writer` | 撰寫 | 企劃+研究 | 文章初稿 |
| `article-editor` | 審稿 | 初稿 | 定稿文章 |
| `article-marketing` | 行銷 | 定稿 | 行銷素材 |
| `article-analytics` | 品質 | 行銷素材 | 品質報告 |

---

## 📝 適用內容類型

- **長文章** - 深度分析、專題報導
- **部落格文章** - 經驗分享、觀點評論
- **行銷文案** - 產品介紹、品牌故事
- **社群短文** - Facebook/LinkedIn 貼文
- **EDM 文案** - 電子報內容
- **專欄文章** - 定期專欄、專家觀點

---

## ⚠️ 注意事項

1. **AI 不能編造** - 所有具體細節必須來自用戶提供的素材
2. **人味優先** - 避免 AI 味，確保有作者聲音
3. **品質把關** - 未達 8/10 分不發布
4. **受眾適配** - 不同平台有不同風格

---

## 授權

Private - 個人使用

## 維護者

Paul Huang (@pin0513)

---

**專案位置**: `/Users/paul_huang/AgentProjects/ArticleWorld`
**GitHub**: https://github.com/pin0513/ArticleWorld
**建立日期**: 2026-02-08
**來源**: 從 claude-global/skills 整併
