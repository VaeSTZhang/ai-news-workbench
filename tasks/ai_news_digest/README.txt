AI News Digest workspace (task-local)

1) Output tracks (must be processed together)
- `global_ai`
- `chinese_short_drama`

2) Required output bundle per track
- `.docx`
- `.html`
- `sources.json`
- `task_log.txt`

3) Scope boundary
- Daily: previous day only.
- Monthly: previous natural month only.
- Never mix daily and monthly scopes.

4) Daily reporting rules
- Daily main list must contain only previous-day verifiable items.
- No methodology/process/template/safety-rule text as news entries.
- If daily signals are limited, use a reader-friendly formal explanation block.
- Do not use internal QA phrases such as “主列表为空/整改版/见task_log”.

5) Monthly reporting rules
- De-dup is mandatory.
- Same event or same trend cannot be split into padded rewrites.
- If verifiable coverage is insufficient, record the shortfall in task_log.txt.

6) Source rules
- Every main-list item must have directly supporting publicly accessible sources.
- Source-insufficient items must stay out of main list and be recorded in task_log.txt.
