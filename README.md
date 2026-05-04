# AI News Workbench

Tool-agnostic AI news automation workbench for global AI news and China short-drama trend reports.

This project was initially bootstrapped with Codex Desktop assistance, but is now designed as a tool-agnostic workspace. It can be executed by OpenCode, Codex, other local automation agents, or manual scripts.

## Command Entry

Trigger the daily update workflow with a single command:
- `更新新闻`

This command runs the fixed daily pipeline for both tracks together and follows:
- `tasks/ai_news_digest/RUNBOOK_UPDATE_NEWS.txt`

## Current Tracks

- `global_ai`: global AI headline intelligence
- `chinese_short_drama`: China short-drama ranking and trend intelligence

## Outputs

Each track run produces:
- `.docx`
- `.html`
- `sources.json`
- `task_log.txt`

## Quality Baseline

- Daily scope: previous day only
- Monthly scope: previous natural month only
- `global_ai` daily target: 10-15
- `chinese_short_drama` daily target: >=8
- If verifiable signals are insufficient, keep fewer items and explain in `task_log.txt` without padding

## Security Principles

- Operate only inside the project root.
- Do not read, copy, or commit files outside this repository.
- Never commit secrets or unauthorized materials, including API keys, tokens, cookies, passwords, SSH keys, environment files, local configs, internal company projects, private repositories, or personal data.

## Current Reviewable Examples / 当前可审阅样例

当前公开仓库中可审阅的正式报告样例：

### 2026-04 global_ai 月报
- 路径：`tasks/ai_news_digest/news_reports/global_ai/monthly/2026/04/`
- 文件：
  - `2026-04_global_ai_monthly.html` - 可直接在浏览器中打开的完整报告
  - `2026-04_global_ai_monthly.docx` - 可下载的 Word 格式报告
  - `sources.json` - 结构化来源记录，包含 id、category、title、url、publisher、published_date、accessed_date、used_in_section、reliability_note
  - `task_log.txt` - 执行日志，记录去重检查、剔除原因、最终纳入条目数

### 2026-04 chinese_short_drama 月报
- 路径：`tasks/ai_news_digest/news_reports/chinese_short_drama/monthly/2026/04/`
- 文件：
  - `2026-04_chinese_short_drama_monthly.html` - 可直接在浏览器中打开的完整报告
  - `2026-04_chinese_short_drama_monthly.docx` - 可下载的 Word 格式报告
  - `sources.json` - 结构化来源记录，包含 id、category、title、url、publisher、published_date、accessed_date、used_in_section、reliability_note
  - `task_log.txt` - 执行日志，记录去重检查、剔除原因、最终纳入条目数

### 样例说明
- 正式报告目录只保留可核验、可阅读、可分享的报告
- 日报低质量试运行产物已从正式目录清理，归档到本地忽略目录
- 信息不足时不生成伪新闻卡片；0 条真实可核验内容时只生成 task_log.txt
- 本项目是工具无关的自动化工作区，可由 OpenCode、Codex、其他本地自动化代理或人工脚本执行
