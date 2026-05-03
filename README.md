# Codex AI News Workbench

## 项目简介

这是一个用于 Codex 桌面端自动化任务实验的公开仓库，当前主要任务是 AI 新闻日报/月报自动整理。

## 当前任务

- 全球 AI 新闻日报/月报
- AI 影视化 / AI 视频 / AI 短剧 / AI 电影行业日报/月报
- 每条输出包含 `.docx`、`.html`、`sources.json`、`task_log.txt`

## 目录结构

```text
tasks/
  ai_news_digest/
    README.txt
    AGENTS_TASK_RULES.txt
    templates/
    news_reports/
    logs_txt/
```

## 输出格式

- `.docx`：适合给老板、同事、合作方直接分享
- `.html`：可直接双击打开的可视化速览页
- `sources.json`：来源留档（含来源链接与来源级别）
- `task_log.txt`：执行日志与核验说明

## 自动任务计划

- 每日任务：北京时间每天 11:00，固定总结前一天新闻
- 月度任务：每月 1 日 11:30，总结上一个自然月新闻

## 内容边界

- `global_ai`：全球 AI 行业主线（模型、基础设施、政策、产业化等）
- `ai_film_video`：AI 影视化 / AI 视频 / AI 短剧 / AI 电影、AI 生成角色与版权、影视制作工作流
- 两类内容必须去重，避免重复、避免互相复制凑数

## 安全边界

本仓库内脚本与任务仅在以下范围内操作：`/Users/zhangtritsen/Desktop/Code/codex_Project`

严禁访问与提交：
- `/Users/zhangtritsen/Desktop/Code` 下除 codex_Project 外内容
- 公司内部工程文件、`ManJuFlow`
- `/Users/zhangtritsen/Desktop`
- `/Users/zhangtritsen/Documents`
- `/Users/zhangtritsen/Downloads`
- `/Users/zhangtritsen/.ssh`
- `/Users/zhangtritsen/.env`
- `/Users/zhangtritsen/.config`
- `/Users/zhangtritsen/.codex`

## 公开仓库注意事项

- 不提交 API Key、token、密码
- 不提交公司文件
- 不提交个人隐私
- 不提交本地敏感配置
- 不提交无用中间产物与旧归档
