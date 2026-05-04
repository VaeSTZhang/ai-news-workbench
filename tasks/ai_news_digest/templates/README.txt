模板目录说明

本目录包含 AI 新闻摘要任务的所有模板文件。

模板文件列表：

1. daily_ai_news_task_prompt.txt
   - 用途：日报任务提示词
   - 说明：定义日报生成的规则、格式、来源要求等

2. monthly_ai_news_task_prompt.txt
   - 用途：月报任务提示词
   - 说明：定义月报生成的规则、去重要求、来源要求等

3. AUTOMATION_DAILY_COPY_THIS.txt
   - 用途：日报自动化复制模板
   - 说明：可直接复制到自动化工具中执行的日报生成命令

4. AUTOMATION_MONTHLY_COPY_THIS.txt
   - 用途：月报自动化复制模板
   - 说明：可直接复制到自动化工具中执行的月报生成命令

5. COMMAND_UPDATE_NEWS.txt
   - 用途：手动执行"更新新闻"的命令模板
   - 说明：定义手动触发新闻更新的执行规则

6. HTML_STYLE_GUIDE.txt
   - 用途：HTML 报告样式规范
   - 说明：定义 HTML 报告的结构、样式、卡片格式等

安全要求：
- 不要在模板中写入 API Key、token、cookie、密码、本机路径或个人隐私
- 修改模板后要同步检查 RUNBOOK 和 README 中的路径/规则是否一致
