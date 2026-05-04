正式报告目录说明

本目录是 AI 新闻摘要任务的正式报告目录。

当前正式栏目：

1. global_ai
   - 用途：全球 AI 热点新闻
   - 内容：大模型、AI 公司动态、Agent、多模态、算力、芯片、政策监管、投融资、AI 安全等

2. chinese_short_drama
   - 用途：国内爆款短剧排行榜与流行趋势
   - 内容：平台榜单变化、爆款短剧案例、题材趋势、人设趋势、钩子趋势、平台动向、商业化观察

注意：旧栏目 ai_film_video 已废弃，不应作为正式栏目出现。

目录结构：

news_reports/
├── global_ai/
│   ├── daily/YYYY-MM/YYYY-MM-DD/
│   └── monthly/YYYY/MM/
└── chinese_short_drama/
    ├── daily/YYYY-MM/YYYY-MM-DD/
    └── monthly/YYYY/MM/

每个正式报告目录应包含：
- YYYY-MM-DD_{category}_daily.html 或 YYYY-MM_{category}_monthly.html
- YYYY-MM-DD_{category}_daily.docx 或 YYYY-MM_{category}_monthly.docx
- sources.json
- task_log.txt

特殊情况：
- 如果某天 0 条真实可核验内容，只生成 task_log.txt，不生成 HTML/DOCX/sources.json
- 低质量试运行产物应移入 archive_old_outputs/，且 archive_old_outputs 不提交到 GitHub

来源要求：
- 正式报告不能使用首页、频道页、搜索页作为来源
- 每条内容必须有具体文章页、公告页、产品发布页、监管文件页、研究报告页或可核验数据页
