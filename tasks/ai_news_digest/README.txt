AI 新闻自动化任务工作区（任务专属）

一、输出目录
- `tasks/ai_news_digest/news_reports/global_ai/`
- `tasks/ai_news_digest/news_reports/chinese_short_drama/`

二、四件套（必需）
- `.docx`
- `.html`
- `sources.json`
- `task_log.txt`

三、单条新闻写作标准（A）
每条必须包含：
1. 事件标题（具体）
2. 发生了什么（2-4 句，含主体/时间/动作/结果）
3. 为什么重要（1-3 句，具体到业务或流程）
4. 对 ManJuFlow 的启发（1-3 句）
5. 来源链接（条目紧邻来源）

四、禁止废话标准（B）
禁止空话：如“值得关注”“具有重要意义”等；如使用必须立即解释影响对象、流程、成本或能力。

五、月报去重标准（C）
- global_ai：30 条互不重复事件；同一事件后续需并入同一条。
- chinese_short_drama：20-30 条互不重复观察；同一案例不可拆条凑数。
- task_log.txt 必须记录去重检查结果。

六、来源标准（D）
- 每条都要来源。
- 趋势观察至少 2 个来源。
- 来源不足写“来源不足，未纳入主列表”。
- sources.json 字段：id/category/title/url/publisher/published_date/accessed_date/used_in_section/reliability_note。

七、数量标准（E）
- global_ai 日报 >=10。
- chinese_short_drama 日报 >=8。

八、Git 常规提交默认允许（F）
在项目根目录内，以下命令视为可信常规流程：
`git status` `git add` `git commit` `git pull --rebase origin main` `git push origin main` `git remote -v` `git diff` `git log`
执行前仍需确认不提交敏感文件与归档目录。
