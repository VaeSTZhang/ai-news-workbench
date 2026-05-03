AI 新闻自动化任务工作区（任务专属）

本文件夹用于集中管理 AI 新闻自动化任务相关文件。

项目说明：
1. codex_Project 会承载多个任务，AI 新闻自动化任务不得将文件散落到仓库根目录。
2. 所有 AI 新闻任务输入、输出、归档与日志均应保存在此文件夹内。

任务时间与范围：
1. 每日任务：每天北京时间 11:00。
2. 每日任务内容：总结前一天的
   - 全球 AI 热点新闻
   - AI 影视化 / AI 视频 / AI 短剧 / AI 电影新闻
3. 月度任务：每月 1 日北京时间 11:30。
4. 月度任务内容：总结上一个自然月的
   - 全球 AI 热点新闻
   - AI 影视化 / AI 视频 / AI 短剧 / AI 电影新闻

输出格式要求：
1. 主报告为 .docx。
2. 同步输出可读性 HTML（单文件）。
3. 来源归档为 sources.json。
4. 执行日志为 task_log.txt。

统一约束：
1. 禁止生成 .md。
2. 禁止生成图片。
3. 目录统一为：
   tasks/ai_news_digest/news_reports/
4. 自动任务 prompt 在：
   tasks/ai_news_digest/templates/
5. 任务日志在：
   tasks/ai_news_digest/logs_txt/
6. 历史旧文件归档到：
   tasks/ai_news_digest/archive_old_outputs/
