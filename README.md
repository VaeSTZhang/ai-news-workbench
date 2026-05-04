# Codex AI News Workbench

Codex-powered intelligence workbench for global AI news and China short-drama trend reports.

## Command Entry

In Codex Desktop, you can trigger the daily update workflow with a single command:
- `更新新闻`

This command runs the fixed daily pipeline for both tracks together and follows:
- `tasks/ai_news_digest/RUNBOOK_UPDATE_NEWS.txt`

## Current Tracks

- `global_ai`: global AI headline intelligence
- `chinese_short_drama`: China short-drama ranking and trend intelligence

## Outputs

Each track run produces:
- `.docx`
- `.html`
- `sources.json`
- `task_log.txt`

## Quality Baseline

- Daily scope: previous day only
- Monthly scope: previous natural month only
- `global_ai` daily target: 10-15
- `chinese_short_drama` daily target: >=8
- If verifiable signals are insufficient, keep fewer items and explain in `task_log.txt` without padding

## Security Principles

- Operate only inside the project root.
- Do not read, copy, or commit files outside this repository.
- Never commit secrets or unauthorized materials, including API keys, tokens, cookies, passwords, SSH keys, environment files, local configs, internal company projects, private repositories, or personal data.
