# Contributing

Thanks for helping document useful Claude video and animation examples. English is the default language; every case also needs a Chinese title and description.

## Submit a case

Open an issue or pull request with the proposed case, its category, and the evidence below. Follow the existing data format when editing the catalog.

- **Original work:** Link the creator's original video post as `https://x.com/<author>/status/<id>`. Confirm that the post contains the work, rather than only commentary or a link to someone else's work.
- **More than 10,000 views:** Record the original post's exact integer view count, the snapshot time in UTC ISO 8601 format, and the source URL used to verify it. The count must be strictly greater than 10,000 at the recorded time. Likes, reposts, followers, or a thread's combined views do not qualify. Missing views are unverified, not zero; omit the case until evidence is available.
- **Bilingual text:** Supply an English and Chinese title and a concise description in both languages. Describe what the work demonstrates without repeating promotional claims as facts.
- **Creator and demonstration:** Include the creator's name or handle, original post URL, a playable demo URL, and a public thumbnail URL. Check that the demo and thumbnail show the same work. Keep the original post as a fallback if a direct media URL expires.
- **Model and tools:** Provide the creator's explicit model attribution, a brief evidence excerpt, and its source URL. State other tools or models when disclosed. Distinguish code-rendered animation from workflows using image, video, voice, or music generation services. Attribution is the creator's claim, not an independent audit.
- **Prompt and code:** Link a prompt or source repository only after checking that it is public and belongs to this work. Use JSON `null` when either is unknown; do not invent a link or treat “prompt in replies” as verification. Label partial instructions or a reusable template accurately.
- **Category and originality:** Choose a category that reflects the output. Check existing entries by post ID and by the work itself. A prompt reply, tutorial about the same output, repost, alternate upload, or quoted post is not another case. A substantial remake may be separate if it is clearly labeled and credits the original.

## Media and corrections

Keep demonstrations and thumbnails hosted by their creators or their publishing platforms. Link to them; do not upload or rehost videos without permission. Public availability does not grant a redistribution license.

For corrections, identify the case and provide replacement evidence. Report broken links, mistaken attribution, duplicated work, and incorrectly recorded metrics. Preserve the date of a view snapshot; never imply that an old count is current. Creators can also open an issue to request a credit correction or removal.

---

# 贡献说明

欢迎补充有价值的 Claude 视频与动画案例。项目默认使用英文，每条案例同时需要中文标题和描述。

## 提交案例

通过 Issue 或 Pull Request 提交候选案例、分类及以下证据。直接编辑目录数据时，请沿用现有格式。

- **原创作品：**提供创作者发布视频的原帖，格式为 `https://x.com/<author>/status/<id>`。确认帖子包含该作品，而不只是评论或引用他人的作品。
- **浏览量严格超过 10,000：**记录原帖的精确整数浏览量、UTC ISO 8601 格式的采集时间，以及核验来源 URL。采集时必须大于 10,000；点赞、转发、粉丝数和整个讨论串的合计浏览量均不能替代。缺失表示尚未核验，不等于零；请取得证据后再收录。
- **中英双语：**提供英文、中文标题及两种语言的简短描述。说明作品展示了什么，不把宣传表述写成已证实的事实。
- **作者与演示：**提供作者名称或账号、原帖链接、可播放的演示链接及公开缩略图链接。确认演示和缩略图对应同一作品；保留原帖作为直接媒体链接失效时的备用入口。
- **模型与工具：**提供作者明确说明模型的依据、简短证据摘录和来源链接。披露其他已知工具或模型，区分代码渲染动画与调用图片、视频、语音或音乐生成服务的混合流程。模型归因来自作者陈述，不代表独立审计。
- **提示词与源码：**只有确认公开且属于该作品后，才填写提示词或源码仓库链接。未知项使用 JSON `null`；不要猜测链接，也不要把“提示词见回复”当作已经核实。部分指令和通用模板应如实标注。
- **分类与去重：**按作品内容选择分类，并同时检查帖子 ID 和作品本身。提示词回复、同一作品的教程、转帖、重复上传和引用帖不能另算案例。明显不同的重制作品可单独收录，但须标注重制并注明原作。

## 媒体与更正

演示视频和缩略图保留在作者或其发布平台托管，仅引用链接。未经授权，不上传或重新托管视频。公开可访问不等于获得转载许可。

提出更正时，请指明案例并附替代证据。欢迎反馈失效链接、错误归因、重复作品和指标记录错误。保留浏览量快照的采集时间，不把历史数字当作当前值。创作者也可通过 Issue 请求修改署名或移除案例。
