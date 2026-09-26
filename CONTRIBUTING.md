# Contributing

Thanks for helping document useful Claude video and animation examples. English is the default language; every case also needs a Chinese title and description.

## Submit a case

Open an issue or pull request with the proposed case, its category, and the evidence below. Follow the existing data format when editing the catalog.

- **Original work:** Link the creator's original video post as `https://x.com/<author>/status/<id>`. Confirm that the post contains the work, rather than only commentary or a link to someone else's work.
- **More than 10,000 views:** Record the original post's exact integer view count, the snapshot time in UTC ISO 8601 format, and the source URL used to verify it. The count must be strictly greater than 10,000 at the recorded time. Likes, reposts, followers, or a thread's combined views do not qualify. Missing views are unverified, not zero; omit the case until evidence is available.
- **Bilingual text:** Supply an English and Chinese title and a concise description in both languages. Describe what the work demonstrates without repeating promotional claims as facts.
- **Creator and demonstration:** Include the creator's name or handle, original post URL, original MP4 URL, and public thumbnail URL. Also provide a GitHub video attachment URL (`https://github.com/user-attachments/assets/<uuid>`) so the case plays within both README pages. Put that URL on its own line outside tables. Check that the playback copy, original video and thumbnail show the same work; keep the original post and media links as fallbacks. Record any compression and available playback-file details in `cases.json`.
- **Model and tools:** Provide the creator's explicit model attribution, a brief evidence excerpt, and its source URL. State other tools or models when disclosed. Distinguish code-rendered animation from workflows using image, video, voice, or music generation services. Attribution is the creator's claim, not an independent audit.
- **Prompt and code:** Link a prompt or source repository only after checking that it is public and belongs to this work. Use JSON `null` when either is unknown; do not invent a link or treat “prompt in replies” as verification. Label partial instructions or a reusable template accurately.
- **Category and originality:** Choose a category that reflects the output. Check existing entries by post ID and by the work itself. A prompt reply, tutorial about the same output, repost, alternate upload, or quoted post is not another case. A substantial remake may be separate if it is clearly labeled and credits the original.

## Media and corrections

This collection uses GitHub-hosted playback copies for in-page video demonstrations. Copies may be compressed for upload and playback; preserve the complete work, creator attribution, original post and original media URL. Keep thumbnails linked to their original platform. Do not imply that inclusion grants a new license or changes the creator's rights.

For corrections, identify the case and provide replacement evidence. Report broken links, mistaken attribution, duplicated work, and incorrectly recorded metrics. Preserve the date of a view snapshot; never imply that an old count is current. Creators can also open an issue to request a credit correction or removal.

---

# 贡献说明

欢迎补充有价值的 Claude 视频与动画案例。项目默认使用英文，每条案例同时需要中文标题和描述。

## 提交案例

通过 Issue 或 Pull Request 提交候选案例、分类及以下证据。直接编辑目录数据时，请沿用现有格式。

- **原创作品：**提供创作者发布视频的原帖，格式为 `https://x.com/<author>/status/<id>`。确认帖子包含该作品，而不只是评论或引用他人的作品。
- **浏览量严格超过 10,000：**记录原帖的精确整数浏览量、UTC ISO 8601 格式的采集时间，以及核验来源 URL。采集时必须大于 10,000；点赞、转发、粉丝数和整个讨论串的合计浏览量均不能替代。缺失表示尚未核验，不等于零；请取得证据后再收录。
- **中英双语：**提供英文、中文标题及两种语言的简短描述。说明作品展示了什么，不把宣传表述写成已证实的事实。
- **作者与演示：**提供作者名称或账号、原帖链接、原始 MP4 链接及公开缩略图链接。同时提供 GitHub 视频附件链接（`https://github.com/user-attachments/assets/<uuid>`），让中英文 README 都能直接播放；附件链接须独占一行，放在表格之外。确认播放副本、原视频和缩略图对应同一作品，并保留原帖及原始媒体链接作为备用入口。在 `cases.json` 中记录压缩情况及可用的播放文件信息。
- **模型与工具：**提供作者明确说明模型的依据、简短证据摘录和来源链接。披露其他已知工具或模型，区分代码渲染动画与调用图片、视频、语音或音乐生成服务的混合流程。模型归因来自作者陈述，不代表独立审计。
- **提示词与源码：**只有确认公开且属于该作品后，才填写提示词或源码仓库链接。未知项使用 JSON `null`；不要猜测链接，也不要把“提示词见回复”当作已经核实。部分指令和通用模板应如实标注。
- **分类与去重：**按作品内容选择分类，并同时检查帖子 ID 和作品本身。提示词回复、同一作品的教程、转帖、重复上传和引用帖不能另算案例。明显不同的重制作品可单独收录，但须标注重制并注明原作。

## 媒体与更正

本合集使用上传至 GitHub 的播放副本，供读者在页面内观看。为便于上传和播放，副本可能经过压缩；须保留完整作品、作者署名、原帖及原始媒体链接。缩略图继续引用原平台链接。收录不代表素材获得新的许可，也不改变创作者的权利。

提出更正时，请指明案例并附替代证据。欢迎反馈失效链接、错误归因、重复作品和指标记录错误。保留浏览量快照的采集时间，不把历史数字当作当前值。创作者也可通过 Issue 请求修改署名或移除案例。
