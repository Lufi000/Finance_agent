# CLAUDE.md — finance_agent 研究笔记库

这是一个 **Obsidian vault + 深度研究知识库**，主题聚焦金融市场与行业研究。
Claude 负责研究、写作、维护笔记；Obsidian 负责浏览、双链、图谱。

## 目录结构约定

```
deepsearch/<行业>/<子主题>/          # 深度研究笔记，如 deepsearch/semiconductor/industry_chain/
  <报告名>.md                       # 主报告
  <report>/img/                     # 配图（图表 PNG），与报告同级的资源目录
deepsearch/<领域>/concepts/          # 概念原子笔记（如 IV_crush.md），供所有研究复用
deepsearch/<领域>/<领域>_MOC.md      # 领域概念图谱索引
strategies/<策略名>/                 # 可执行策略：PLAYBOOK + watchlist + templates + journal
```

- 新研究按 `deepsearch/行业/子主题/` 归档，不要堆在根目录
- **反复出现的概念（≥2 篇研究会引用）应沉淀为 `concepts/` 原子笔记**，并在 MOC 登记；研究笔记通过 `[[wikilink]]` 挂接概念，让图谱自然生长
- 图片统一放报告旁边的 `*/img/` 目录，用**相对路径**引用：`![描述](semireport/img/c1_market.png)`

## 笔记格式规范

### Frontmatter（新笔记必须包含）
```markdown
---
title: 标题
date: YYYY-MM-DD
tags: [行业, 主题, deepsearch]
status: draft | final
---
```

### 正文风格（参照半导体报告的既有风格）
- 中文写作，专业术语保留英文原文（如 CoWoS、HBM、WFE）
- **所有数据必须标注来源**，用脚注格式 `[^N^]`，文末列出来源链接与日期
- 行情/估值数据注明数据截止日（如"截至 2026-07-31 收盘"）
- 报告开头用 `> 引用块` 写明：报告日期、数据来源、**"仅供研究参考，不构成投资建议"**
- 关键结论加粗，结构化呈现（执行摘要 → 分章节 → 催化节点/风险）

### 双链
- 提及有独立笔记的概念、公司、行业时，用 `[[wikilink]]` 语法
- 即使目标笔记还不存在也可以链接，方便日后回填

## 研究工具

- **行情/持仓/实时数据**：优先使用 `longbridge` skill（支持美股、港股、A 股、新加坡、加密货币）
- **图表**：生成图表前先读 `dataviz` skill 的规范；图表存为 PNG 到 `*/img/`
- **联网研究**：WebSearch/WebFetch 获取最新数据，引用时保留 URL 和访问日期

## Git 工作流

- 完成阶段性研究后主动提示用户提交 commit
- commit message 用中文，说明研究主题（如 `研究: 半导体产业链未来两年深度拆解`）
- 不要提交 `.obsidian/workspace*.json` 等本地状态文件（见 .gitignore）

## 红线

- 研究报告**不构成投资建议**，涉及具体标的时必须有免责声明
- 数据不得编造：查不到的数据明确说"未找到"，不要估算后伪装成真实数据
- 引用来源需真实可访问，禁止虚构 URL
