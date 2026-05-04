# AI 新闻工作台

工具无关的 AI 新闻自动化工作台，专注于全球 AI 新闻与中国短剧趋势报告。

本项目最初由 Codex Desktop 辅助搭建，现设计为工具无关的工作区。可由 OpenCode、Codex、其他本地自动化代理或人工脚本执行。

## 命令入口

输入以下命令触发每日新闻更新流程：
- `更新新闻`

该命令执行固定的每日流水线，同时处理两个栏目，遵循：
- `tasks/ai_news_digest/RUNBOOK_UPDATE_NEWS.txt`

## 当前栏目

- `global_ai`：全球 AI 热点头条情报
- `chinese_short_drama`：国内爆款短剧排行榜与流行趋势情报

## 输出文件

每次运行生成：
- `.docx` - 可下载的 Word 格式报告
- `.html` - 可直接在浏览器中打开的完整报告
- `sources.json` - 结构化来源记录
- `task_log.txt` - 执行日志

## 质量基准

- 日报范围：仅前一天
- 月报范围：仅上一个自然月
- `global_ai` 日报目标：10-15 条
- `chinese_short_drama` 日报目标：≥8 条
- 如果公开可核验信息不足，允许少于目标条数，但必须在 `task_log.txt` 中说明原因

## 安全原则

- 仅在项目根目录内操作
- 不读取、复制或提交此仓库外的文件
- 不提交密钥或未授权资料，包括 API Key、token、cookie、密码、SSH key、环境文件、本地配置、公司项目、私有仓库或个人数据

## 当前可审阅样例

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
