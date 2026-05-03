AI News Digest workspace (task-local)

1) Output folders
- `tasks/ai_news_digest/news_reports/global_ai/`
- `tasks/ai_news_digest/news_reports/chinese_short_drama/`

2) Required output bundle
- `.docx`
- `.html`
- `sources.json`
- `task_log.txt`

3) Per-item writing standard
Each item must include:
1. Title (specific)
2. What happened (2-4 sentences with actor/time/action/result)
3. Why it matters (1-3 sentences with concrete workflow/cost/capability/business impact)
4. Implications for ManJuFlow (1-3 concrete sentences)
5. Source links (kept with the item)

4) Quality constraints
- `global_ai` daily >= 10
- `chinese_short_drama` daily >= 8
- `global_ai` monthly = 30 non-duplicate key events
- `chinese_short_drama` monthly = 20-30 non-duplicate observations
- Monthly task log must record de-dup check, removed duplicates, and final count.

5) Source rules
- No fake sources.
- Broken, gated, or mismatched links cannot remain in main-list items.
- If evidence is weak or inaccessible: `来源不足，未纳入主列表`.
