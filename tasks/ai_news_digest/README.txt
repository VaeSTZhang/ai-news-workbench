AI 新闻自动化任务工作区（任务专属）

本工作区用于集中管理 AI 新闻自动化任务。

1) 公开仓库核心输出：
- 全量日报/月报文件位于
  - tasks/ai_news_digest/news_reports/global_ai/
  - tasks/ai_news_digest/news_reports/ai_film_video/
- 输出必须包含 .docx + .html + sources.json + task_log.txt。

2) 目录职责：
- daily：按 `YYYY-MM/YYYY-MM-DD` 存放每天的公开日报。
- monthly：按 `YYYY/MM` 存放每月日报。
- 模板与任务规则：templates/
- 任务日志：logs_txt/
- 旧产物归档：archive_old_outputs/

3) 安全约束
- 严禁在 `codex_Project` 根目录存放 AI 新闻日报/月报。
- 仅在 `tasks/ai_news_digest` 写入任务相关文件。
- 禁止生成 Markdown 报告，禁止生成图片。
- 公开仓库应避免上传敏感文件。

4) 任务目标
- 每日 11:00（北京时间）总结前一天：global_ai + ai_film_video。
- 每月 1 日（北京时间）总结上一个自然月。
