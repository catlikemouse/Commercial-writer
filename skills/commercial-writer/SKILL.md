---
name: commercial-writer
description: "写番茄/起点风格的商业网文（男频爽文为主）：新书立项、黄金三章、章节大纲与正文生成、改稿、节奏与爽点设计、设定集与坑位管理。也用于从现有 state/output 文件续写、做章节评估、修复毒点与断裂。"
---

# Commercial Writer（商业网文写作引擎）

目标：以**高留存 + 强爽点 + 可持续日更**为优先级，产出适合番茄分发的章节稿。

## 工作流（默认）

1) **写作/审稿前先读状态**（必须）
- `state/book.json`：立项与定位
- `state/series_bible.md`：设定集/角色卡/规则
- `state/plot_memory.json`：剧情记忆（已发生事件/未回收坑/人物关系）

2) **需要回忆旧内容时**（节省 token）
- 优先用 qmd 在 workspace 里检索：
  - `qmd search "关键词" -c openclaw --json -n 10`
  - 再用 `qmd get ...` 抽取必要片段

3) **写完一章后更新剧情记忆**（必须）
- 把“本章发生了什么/新增坑/回收坑/战力变更/人物关系变更”写入 `state/plot_memory.json`

## 指令（你可以这样叫我做）

- `新书立项`：生成/完善 `state/book.json`（定位、卖点、题材、金手指规则）
- `黄金三章`：输出 1~3 章的章纲或正文（危机→金手指→第一次兑现→强钩子）
- `推演剧情`：给出 N 章大纲（每章爽点与钩子明确）
- `生成正文`：按指定字数（例如 2500/4000/6000）生成单章正文
- `章节评定`：按量表打分并给“可执行改稿清单”
- `心理诊断`：找毒点（信息密度/节奏/逻辑/爽点脱敏/人设崩）并给修复方案
- `设定集`：更新 `state/series_bible.md`
- `剧情记忆更新`：更新 `state/plot_memory.json`

## 参考模板/知识库（按需读取）

- 模板：
  - `templates/golden_three_chapters.md`
  - `templates/outline_chapter.md` / `templates/outline_chapter_4_5.md` / `templates/outline_6_20.md`
  - `templates/chapter_rubric.md`
  - `templates/series_bible.md`
- 知识：
  - `knowledge/psychology.md`（钩子/期待/未闭环）
  - `knowledge/pacing.md`（张弛/节奏）
  - `knowledge/tropes.md`（套路库）
  - `knowledge/trends_2026.md`（番茄趋势）
  - `knowledge/income_strategy.md`（全勤/留存/收费点思路）
