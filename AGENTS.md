# AGENTS.md — Repository Safety Boundary and Task Rules

## 1) Safety Boundary

- Work only inside this repository root and its subdirectories.
- If a task requires reading or writing outside this repository, refuse and explain why.
- Do not scan, read, copy, modify, or delete external paths.

## 2) Command Discipline

- Before any shell operation, confirm working directory with `pwd`.
- Stop immediately if the command would target paths outside this repository.
- Do not use command forms that implicitly traverse upward or external locations.

## 3) AI News Digest Scope

All AI news automation assets must remain under:
- `tasks/ai_news_digest/`

Current active report tracks:
- `global_ai`
- `chinese_short_drama`

Deprecated track:
- `ai_film_video` (archive only; not an active output target)

## 4) Public-Repo Security Requirements

Public files must never include:
- machine usernames
- absolute local filesystem paths
- local desktop/document/download/config/cache locations
- API keys, tokens, cookies, passwords, SSH keys
- env files, local configuration files, private/internal project data, or unauthorized materials

## 5) Report Quality Baseline

- No fabricated news, data, links, or quotes.
- If reliable public evidence is insufficient, explicitly state:
  - `公开可核验信息不足，未纳入主列表`.
- Enforce de-duplication in monthly reports and record results in `task_log.txt`.
