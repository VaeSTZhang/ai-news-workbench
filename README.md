# Codex AI News Workbench

## 项目简介

这是一个用于 Codex 桌面端自动化任务实验的公开仓库，当前主要任务是 AI 新闻日报/月报自动整理。

## 当前任务

- 全球 AI 热点新闻日报/月报
- AI 影视化 / AI 视频 / AI 短剧 / AI 电影行业日报/月报
- .docx（可共享给老板、同事、合作方）
- .html（浏览器可视化速览）
- sources.json（来源留档）
- task_log.txt（执行日志）

## 目录结构

- tasks/
  - ai_news_digest/
    - README.txt
    - AGENTS_TASK_RULES.txt
    - templates/
    - news_reports/
    - logs_txt/

其中 `news_reports/` 是仓库核心公开内容之一。

## 输出格式

- `.docx`：适合线下分享与汇报
- `.html`：单文件可视化速览页，双击即可打开
- `sources.json`：记录每条新闻来源（含 title/url/publisher/published_date/accessed_date/reliability_note）
- `task_log.txt`：执行日志、去重记录、安全边界执行记录

## 内容边界

- `global_ai`：全球 AI 行业主线（模型、基础设施、政策、产业、监管、投资、通用技术）。
- `ai_film_video`：AI 影视化、AI 视频、AI 短剧、AI 电影、AI 生成角色与影视版权、影视制作工作流。
- 两类内容必须严格去重，不得用另一类内容复制凑数。

## 自动任务计划

- 每日任务：北京时间每天 11:00，总结前一天新闻。
- 月度任务：每月 1 日 11:30，总结上一个自然月新闻。

## 安全边界

- 仅在 `/Users/zhangtritsen/Desktop/Code/codex_Project` 内操作。
- 禁止访问：
  - `/Users/zhangtritsen/Desktop`、`Documents`、`Downloads`
  - `/Users/zhangtritsen/.ssh`、`/.env`、`/.config`、`/.codex`
  - 公司内部工程文件、ManJuFlow

## 公开仓库提交原则

- 公开仓库可提交的核心是任务说明、模板、`news_reports` 以及说明性日志。
- 不提交 API Key、token、password、cookie、SSH key、敏感本地配置与个人隐私。
- 不提交旧混乱归档与无价值本地中间产物。
- `news_reports` 下的 `.docx`/`.html`/`sources.json`/`task_log.txt` 为核心输出，可直接上传。
