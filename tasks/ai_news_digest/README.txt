AI 新闻自动化任务工作区（任务专属）

本工作区用于集中管理新闻自动化任务。

1) 公开仓库核心输出：
- `tasks/ai_news_digest/news_reports/global_ai/`
- `tasks/ai_news_digest/news_reports/chinese_short_drama/`
- 每次输出必须包含 `.docx + .html + sources.json + task_log.txt`

2) 目录职责：
- `daily/`：按 `YYYY-MM/YYYY-MM-DD` 存放日报
- `monthly/`：按 `YYYY/MM` 存放月报
- `templates/`：任务模板
- `logs_txt/`：任务日志
- `archive_old_outputs/`：历史归档

3) 安全约束：
- 仅在项目目录内读写
- 禁止生成 Markdown 新闻报告与图片
- 公开仓库仅提交可公开内容

4) 任务目标：
- 每日 11:00（北京时间）总结前一天：`global_ai + chinese_short_drama`
- 每月 1 日 11:30（北京时间）总结上一个自然月
