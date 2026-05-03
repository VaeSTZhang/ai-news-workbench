# Codex AI News Workbench

## 项目简介

用于自动化生成两类公开新闻与趋势报告：
1. `global_ai`：全球 AI 热点新闻。
2. `chinese_short_drama`：国内爆款短剧排行榜与流行趋势。

## 核心输出

核心公开内容位于 `tasks/ai_news_digest/news_reports/`：
- `.docx`（可对外分享）
- `.html`（单文件速览）
- `sources.json`（来源留档）
- `task_log.txt`（执行日志）

## 内容边界

### global_ai
关注模型、Agent、多模态、推理、算力、政策、监管、投融资、企业落地、安全与版权治理。

### chinese_short_drama
仅关注国内短剧平台榜单与流行趋势：平台热剧变化、热门题材、热门人设、剧情钩子、平台运营偏好、商业化与投流趋势，以及对 ManJuFlow 的启发。

## 安全与公开提交原则

- 仅在项目目录内操作。
- 不访问未授权资料，不处理敏感凭据。
- 报告与日志仅使用项目相对路径。
- `news_reports` 是公开仓库核心内容，可上传。
- 禁止上传敏感文件、公司文件、个人隐私、本地配置、旧混乱中间产物。
