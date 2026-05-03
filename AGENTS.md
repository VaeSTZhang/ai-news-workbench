# AGENTS.md — codex_Project 安全边界与任务规范

## 0. 最高优先级安全规则

本项目根目录是：

/Users/zhangtritsen/Desktop/Code/codex_Project

你只能在这个目录及其子目录内读取、创建、修改、删除文件。

绝对禁止访问、扫描、读取、修改、删除以下目录或文件：
- /Users/zhangtritsen/Desktop/Code 目录下除 codex_Project 以外的任何内容
- /Users/zhangtritsen/Desktop/Code/ManJuFlow
- /Users/zhangtritsen/Desktop/Code 下任何公司内部工程文件
- /Users/zhangtritsen/Desktop
- /Users/zhangtritsen/Documents
- /Users/zhangtritsen/Downloads
- /Users/zhangtritsen/.ssh
- /Users/zhangtritsen/.env
- /Users/zhangtritsen/.config
- /Users/zhangtritsen/.codex
- 任何不在本项目根目录内的绝对路径

如果任务需要访问本项目根目录之外的任何路径，必须拒绝执行，并说明原因。

## 1. 命令执行规则

每次执行任何 shell 命令前，必须先确认当前目录：

pwd

如果 pwd 的结果不是：
/Users/zhangtritsen/Desktop/Code/codex_Project
或其子目录，必须立即停止。

禁止执行以下命令形态：
- cd ..
- cd /Users/zhangtritsen/Desktop/Code
- find ..
- find /Users/zhangtritsen
- grep -R .. 
- rg .. 
- ls ..
- cat ../*
- open ..
- rm -rf ..
- 任何包含本项目目录之外路径的命令

允许的文件操作范围仅限：
/Users/zhangtritsen/Desktop/Code/codex_Project/**

## 2. 符号链接规则

如果发现项目内有 symlink，必须先检查其真实路径。
如果 symlink 指向项目根目录之外，禁止读取、跟随、修改它。

## 3. 日常自动任务

每天晚上 22:00，基于公开网络资料整理两份 Markdown 文件：

1. 全球 AI 热点新闻日报
输出目录：
reports/global_ai/YYYY-MM-DD_global_ai_daily.md

2. AI 影视化 / AI 视频 / AI 短剧 / AI 电影爆款作品与相关新闻日报
输出目录：
reports/ai_film_video/YYYY-MM-DD_ai_film_video_daily.md

## 4. 报告要求

每份报告必须包含：
- 日期
- 摘要
- 重要事件列表
- 为什么重要
- 对 ManJuFlow / AI 影视化内容生产的启发
- 来源链接列表
- 不确定信息说明

禁止编造新闻、数据、链接、引用。
如果没有可靠来源，必须写“未找到可靠公开来源”，不能硬写。

## 5. 文件命名规则

月报：
reports/global_ai/YYYY-MM_global_ai_monthly.md
reports/ai_film_video/YYYY-MM_ai_film_video_monthly.md

日报：
reports/global_ai/YYYY-MM-DD_global_ai_daily.md
reports/ai_film_video/YYYY-MM-DD_ai_film_video_daily.md

资料留档：
sources/YYYY-MM-DD_sources.md

日志：
logs/YYYY-MM-DD_task_log.md

## 6. 输出语言

默认使用简体中文。
面向老板、投资人、合作方时，语言要专业、清晰、克制，不夸大。
