AI News Digest workspace (task-local)

1) Output folders
- `tasks/ai_news_digest/news_reports/global_ai/`
- `tasks/ai_news_digest/news_reports/chinese_short_drama/`

2) Required output bundle
- `.docx`
- `.html`
- `sources.json`
- `task_log.txt`

3) Daily vs Monthly boundary
- Daily: only the previous day.
- Monthly: only the previous natural month.
- Do not mix daily and monthly scopes.

4) Daily hard rules
- Daily main list must contain only previous-day verifiable news.
- No methodology/process/rules entries in daily main list.
- If news is insufficient, allow fewer than target counts and explain in task_log.txt.
- Never fill with old-month items.

5) Monthly hard rules
- De-dup is mandatory.
- If verifiable items are insufficient, record the gap in task_log.txt instead of padding.

6) Source rules
- Every main-list item must have directly supporting, publicly accessible sources.
- Source-insufficient items must stay out of main list and be logged in task_log.txt.
