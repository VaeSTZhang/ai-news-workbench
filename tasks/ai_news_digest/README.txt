AI News Digest workspace (task-local)

1) Command entry
- Input: `更新新闻`
- Command file: `tasks/ai_news_digest/templates/COMMAND_UPDATE_NEWS.txt`
- Runbook: `tasks/ai_news_digest/RUNBOOK_UPDATE_NEWS.txt`

This project can be executed by OpenCode, Codex, other local automation agents, or manual scripts.

2) Output tracks (must be processed together)
- `global_ai`
- `chinese_short_drama`

3) Required output bundle per track
- `.docx`
- `.html`
- `sources.json`
- `task_log.txt`

4) Scope boundary
- Daily: previous day only.
- Monthly: previous natural month only.
- Never mix daily and monthly scopes.

5) Daily reporting rules
- Daily main list must contain only previous-day verifiable items.
- No methodology/process/template/safety-rule text as news entries.
- If daily signals are limited, use reader-friendly formal explanation in report body.
- Do not use internal QA phrases such as “主列表为空/整改版/见task_log”.

6) Monthly reporting rules
- De-dup is mandatory.
- Same event or same trend cannot be split into padded rewrites.
- If verifiable coverage is insufficient, record the shortfall in task_log.txt.

7) Source rules
- Every main-list item must have directly supporting publicly accessible sources.
- Source-insufficient items must stay out of main list and be recorded in task_log.txt.


8) Target structure
- tasks/ai_news_digest/README.txt
- tasks/ai_news_digest/AGENTS_TASK_RULES.txt
- tasks/ai_news_digest/RUNBOOK_UPDATE_NEWS.txt
- tasks/ai_news_digest/templates/
- tasks/ai_news_digest/news_reports/global_ai/{daily,monthly}/
- tasks/ai_news_digest/news_reports/chinese_short_drama/{daily,monthly}/
- tasks/ai_news_digest/logs_txt/
- tasks/ai_news_digest/archive_old_outputs/

9) Current tracks and deprecated tracks
- 当前正式栏目只有 global_ai 和 chinese_short_drama
- 旧 ai_film_video 已废弃并归档到 archive_old_outputs/deprecated_ai_film_video/
- archive_old_outputs 为本地忽略归档，不提交到 GitHub

10) Quality control
- 正式 reports 目录只保留质量达标报告
- 信息不足时不生成伪新闻卡片
- 0 条真实可核验内容时只生成 task_log.txt，不生成正式 HTML/DOCX
- 低质量试运行产物移入 archive_old_outputs 并记录 CLEANUP_NOTES.txt

11) Current reviewable examples / 当前可审阅样例
- 2026-04 global_ai 月报：tasks/ai_news_digest/news_reports/global_ai/monthly/2026/04/
- 2026-04 chinese_short_drama 月报：tasks/ai_news_digest/news_reports/chinese_short_drama/monthly/2026/04/
- 每个样例包含：HTML、DOCX、sources.json、task_log.txt
