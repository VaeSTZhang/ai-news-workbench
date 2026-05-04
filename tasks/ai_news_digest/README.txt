AI News Digest workspace (task-local)

1) Command entry
- In Codex Desktop, input: `更新新闻`
- Command file: `tasks/ai_news_digest/templates/COMMAND_UPDATE_NEWS.txt`
- Runbook: `tasks/ai_news_digest/RUNBOOK_UPDATE_NEWS.txt`

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
