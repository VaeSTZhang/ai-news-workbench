# Codex AI News Workbench

Codex-powered intelligence workbench for global AI news and China short-drama trend reports.

## Current Tracks

- `global_ai`: global AI headline intelligence
- `chinese_short_drama`: China short-drama ranking and trend intelligence

## Outputs

Each run produces:
- `.docx`
- `.html`
- `sources.json`
- `task_log.txt`

## Quality Baseline

- `global_ai` daily: at least 10 items
- `global_ai` monthly: 30 non-duplicate key events
- `chinese_short_drama` daily: at least 8 valid observations
- `chinese_short_drama` monthly: 20-30 non-duplicate market observations

Each item must include: title, what happened, why it matters, implications for ManJuFlow, and source links.

## Security Principles

- Operate only inside the project root.
- Do not read, copy, or commit files outside this repository.
- Never commit secrets or unauthorized materials, including API keys, tokens, cookies, passwords, SSH keys, environment files, local configs, internal company projects, private repositories, or personal data.
