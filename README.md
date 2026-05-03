# Codex AI Automation Workbench

## 项目简介

这是一个独立的 Codex 自动化任务工作台仓库（与公司内部工程文件隔离）。

当前仓库用于在 Codex 桌面端内承载自动化任务，目前的核心任务是：
- AI 新闻可视化日报
- AI 新闻可视化月报

该仓库面向“多任务自动化实验”场景，不是生产系统，不包含公司代码与内部工程内容。

## 当前任务

### AI 新闻自动化

- 全球 AI 热点新闻日报（月度可选）
- AI 影视化 / AI 视频 / AI 短剧 / AI 电影行业日报（月度可选）

## 目录结构

```text
/tasks/ai_news_digest
  /templates
  /news_reports
    /global_ai
      /daily
      /monthly
    /ai_film_video
      /daily
      /monthly
  /logs_txt
  /archive_old_outputs
```

## 输出格式

- `.docx`：用于老板、同事、合作方的正式阅读与转发
- `.html`：单文件可视化速览页（可直接在浏览器打开）
- `sources.json`：来源与来源级别留档
- `task_log.txt`：任务执行记录与核验说明

## 安全边界

- 本仓库仅允许在：`/Users/zhangtritsen/Desktop/Code/codex_Project` 内操作
- 禁止访问：
  - `/Users/zhangtritsen/Desktop/Code` 下除本仓库外的目录
  - `/Users/zhangtritsen/Desktop/Code/ManJuFlow`
  - `/Users/zhangtritsen/Desktop`
  - `/Users/zhangtritsen/Documents`
  - `/Users/zhangtritsen/Downloads`
  - `/Users/zhangtritsen/.ssh`
  - `/Users/zhangtritsen/.env`
  - `/Users/zhangtritsen/.config`
  - `/Users/zhangtritsen/.codex`
- 遵循任务内局部边界（`tasks/ai_news_digest/AGENTS_TASK_RULES.txt`）

## 自动任务计划

- 每日：北京时间每天 11:00，总结前一天新闻
- 月度：每月 1 日 11:30，总结上一个自然月新闻

## 注意事项

- 不提交 API Key、Token、密码、密钥、证书等敏感信息
- 不提交公司内部文件与个人隐私文件
- 不生成/提交图片作为新闻输出
- 不使用 Markdown 作为新闻正式输出（采用 `.docx + .html + sources.json + task_log.txt`）
