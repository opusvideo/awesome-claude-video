# Implementation guides / 完整实现方式

These guides reorganize the details that creators publicly disclosed into reproducible checklists. They are faithful summaries rather than claims that the results were independently reproduced. When a creator published only a one-line prompt, the guide says so explicitly instead of inventing missing settings.

本文把作者公开的提示词和流程整理成可执行清单，并不代表项目已独立复现。若作者只公开一句提示词，条目会明确注明，不补造未披露的参数。

## English

<a id="case-2102787937482252537"></a>
### Inference startup launch explainer

1. Provide the product name, logo, interface captures and the core inference benefit.
2. Use the creator's complete public direction: “make a modern slick and punchy video for a modern startup that works on inference.” No additional shot list or render settings were disclosed.
3. Have the agent turn the value proposition into a short hook–proof–payoff sequence, render a preview, and correct unreadable copy or weak pacing before export.

<a id="case-2103315922098470926"></a>
### A 15-second motion-design showreel

1. Request a dynamic 15-second motion-graphics résumé showreel and explicitly give the model permission to “go all out.”
2. Let the agent choose the visual system, typography, transitions and music; the creator did not publish further constraints.
3. Review a low-resolution preview for an immediate opening hook, continuous motion and a strong final frame, then export the 15-second master.

<a id="case-2103273003555402193"></a>
### A seamless UI morph loop

1. Supply 8–12 UI states, choose monochrome or one accent color, and provide a royalty-free track near 120 BPM.
2. Use one continuously morphing element on a warm-gray canvas with Geist type. A visible cursor must cause every click and drag. Use restrained springs and camera zooms; ban bounce easing, particles, glow, chrome gradients, mismatched icons, dead time and template-like styling.
3. Map seven bars beat by beat: button → loader → check → dynamic island → player → scrubber → overextended volume slider → toggle → liquid tab indicator → self-drawing chart/tooltips → command palette/filter → Enter → toast → starting button.
4. Build one 1440×1440 HTML file. Compute every property from `seek(t)` with no CSS transitions, timers or carried frame state. Implement closed-form spring responses; use independent edge springs for tabs/toggles and cursor-position-driven direct manipulation for drags.
5. Analyze the song in NumPy, start on a downbeat, and place UI sounds at measured peaks. Render via Playwright using four subframes per output frame, then blend with FFmpeg `tmix` for 60 fps motion blur.
6. Render one still per beat before the full pass. Fix off-grid timing, crowding and text legibility. Avoid `will-change` on camera-scaled elements, give outgoing/incoming text separate timing, and make the last frame—including cursor position and velocity—identical to the first.

<a id="case-2103557735086428547"></a>
### Motion-design and sound-engineering demo

1. Ask Claude Opus 5.5 for a 90-second motion-design and sound-engineering demo with an original piano score.
2. The creator disclosed no scene list, source assets or render settings. A faithful recreation therefore leaves composition and visual direction to the agent.
3. Review picture and score together, correct sync and loudness, and export one continuous 90-second master.

<a id="case-2102591147927654847"></a>
### Interactive Camera Lens Lab

1. Ask Opus to explain camera focus by building an interactive lens laboratory.
2. Implement a focus-ring control whose movement changes the glass elements and visibly moves the sharp plane through a scene.
3. Verify the control across its full range and make the optical cause-and-effect readable without narration. The creator published no further stack or prompt details.

<a id="case-2102583898865873225"></a>
### 5,000 Years of Chinese History

1. Ask for an engaging, light and entertaining line-art animation that rapidly reviews five thousand years of Chinese history, with suitable music.
2. Have the agent research and outline the eras, reduce them to a readable timeline, and assign a distinct visual beat to each transition.
3. Check chronology, names, subtitle legibility and music timing before export. No additional public technical settings were disclosed.

<a id="case-2102606609574941028"></a>
### Atmospheric Circulation Explained

1. Choose a TTS provider, save its API documentation as `TTS.md`, and put `APIKEY`, `VOICE` and other settings in `.env`.
2. Add `"deny": ["Read(./.env)"]` to `.claude/settings.json` so the agent cannot read the secret directly.
3. Ask for an engaging line-art animation explaining high-school atmospheric circulation, with music, bilingual Chinese/English subtitles, TTS narration, watermark removal when the API supports it, and a directly exportable final video. Point the agent to `TTS.md` and the environment-variable names.
4. Review the meteorology, narration/subtitle sync and pronunciation, then export the final video.

<a id="case-2102853258582880547"></a>
### Cocktail Recipe Motion Graphic

1. Supply the reference image and the exact cocktail recipe with measurements.
2. Ask for a 30-second JavaScript/HTML explainer that starts with an empty glass and shows every ingredient and measurement as it enters, ending on the completed drink.
3. Build a timed scene, validate the pour order and quantities, render a preview, then capture the browser animation to video.

<a id="case-2103116235009347650"></a>
### The Battle of Austerlitz

1. Ask for a 4–5 minute cinematic film about the 1805 battle, built entirely in code. Require research, historical accuracy, dramatic but understandable strategy and exceptional visuals.
2. Use the supplied paintings as inspiration for scale, atmosphere, smoke, skies, cavalry, formations, landscape and chaos—without copying them literally or falling back to a generic infographic/game look.
3. Give the agent creative control over research, story structure, pacing and the code-rendered visual language.
4. Validate the chronology and maneuvers, review the film for cinematic pacing and clarity, and iterate before the final render. The public repository is linked from the source post.

<a id="case-2102680453912449223"></a>
### Physics Competition Problem Walkthrough

1. Start from the creator's earlier educational-animation prompt and replace the broad topic with the exact competition problem.
2. Require the solution to expose assumptions, diagram the forces/geometry, derive each equation in order and synchronize narration, labels and animation.
3. Independently check the final numeric/symbolic answer and review the video at phone size. The creator did not disclose a longer case-specific prompt.

<a id="case-2102827887732932956"></a>
### Talking-head video to animated B-roll

1. Give Claude Code the source vertical MP4 in safe mode with high effort, no preloaded skills and no outside assets.
2. Ask it to keep the original audio, subtitles and duration unchanged; shrink the speaker into a readable circular picture-in-picture at bottom right without covering captions.
3. Replace the main picture with light, humorous line-art B-roll that illustrates each spoken concept. The reported workflow used Python to draw frames and split the 83-second source into roughly 30 subtitle-aligned shots.
4. Verify every subtitle boundary, picture-in-picture placement, audio preservation and exact duration, then export under a new filename.

<a id="case-2103511590884815282"></a>
### 81 Years of Indonesian History

1. Ask for a résumé-quality dynamic motion-graphics reel and grant broad creative freedom.
2. Specialize the reel into an impressive story of Indonesia from the first president to the present, and ask the model to surprise you with the storyboard.
3. Fact-check the presidential timeline, balance screen time across eras, add readable dates/names, and review rhythm before export. No further implementation details were published.

<a id="case-2102476258948927543"></a>
### Pixel Wizard

1. Build a single offline HTML file with vanilla JavaScript and Canvas 2D. Draw at 128×96 on an offscreen canvas, integer-scale it to the window, disable smoothing, snap all drawing to integer coordinates and use a fixed ~24-color palette.
2. Construct a procedural ~24×32 wizard from rectangles/pixel runs with a bent hat, beard, shaded robe, staff and gem. Parameterize pose, interpolate smoothly, then quantize to an 8–12 fps sprite feel.
3. Implement the seamless state machine `IDLE → CHARGE → CAST → RECOVER`, with staff movement, spiraling sparks, projectile, 1–2 px shake and settling motion.
4. Preallocate a particle pool, step colors through palette indices, use a fixed 60 Hz update and allocate nothing in the loop.
5. Add the minimal night scene, rim light and readable silhouette; test integer scaling, stable 60 fps and the loop seam.

<a id="case-2102495989194236158"></a>
### The Life of Opus

1. Ask Claude Opus 5.5 to animate its own life from day zero to the present.
2. Constrain the visuals to JavaScript-drawn brush strokes: no video model and no source images.
3. Let the agent choose milestones and symbolism, then review continuity and historical claims. No longer public prompt or renderer settings were disclosed.

<a id="case-2102493303388475855"></a>
### Oktoberfest

1. Capture a screenshot of the character you want to use and attach it as the identity reference.
2. The public text stops after saying this is the exact prompt and “Have fun”; no production prompt or technical recipe is visible in the cited post.
3. To avoid inventing author instructions, preserve the character's silhouette/colors, define the Oktoberfest setting and actions yourself, then test identity consistency shot by shot.

<a id="case-2102515055116063144"></a>
### Rainbow Road Pixel Animation

1. Create one offline vanilla-JS/Canvas HTML file at a 160×90 logical resolution, integer-scaled with smoothing off. Use only integer coordinates and a fixed ~32-color palette; ban gradients, rotation, blur and antialiasing.
2. Reproduce the specified 12×8 orange four-legged sprite, add highlight/shadow pixels and a quantized four-frame run cycle with squash, stretch and lean.
3. Build a seven-color sinusoidal road with fast scrolling divisions, gaps and ramps; add three parallax star layers, planets/nebulae and speed lines.
4. Author deterministic attack patterns for meteors and telegraphed beams. Map each to jump, double-jump, slide or rainbow-afterimage dash with near-miss hit stops, slow motion and seeded shake.
5. Drive `RUN → WARN → DODGE → NEAR_MISS → RUN`, ending with `BOOST → WARP` into the opening frame. Use a pooled, allocation-free particle system and fixed 60 Hz updates.
6. Test silhouette clarity, exact looping, stable performance and whether every dodge reads as fast, close and stylish.

<a id="case-2102573127192727704"></a>
### New Zealand in Acrylic

1. Provide the New Zealand trip photos and ask Claude Opus 5.5 to redraw them in an acrylic-paint style entirely in JavaScript.
2. Extract a shared palette and brush vocabulary, recreate each photograph as layered procedural strokes, and keep composition recognizable across scenes.
3. Animate transitions and camera moves, then compare representative frames against the photos. The creator published no longer prompt or render recipe.

<a id="case-2102801274173587569"></a>
### Claude Pop: Hybrid Music Video

1. Supply the original MP4/audio, lyrics, source repository and reference folders. Keep the exact audio track while independently redesigning the full music video.
2. Research contemporary motion/K-pop/internet-brutalist references; make a coherent style sheet and a personified Claude-inspired protagonist plus supporting characters. Avoid generic Pixar-like output.
3. Generate consistent character sheets, sets and Seedance 2.5 base shots; use the song or cut references to validate timing and lip sync. Mix performance shots with non-lip-synced inserts and topical AI-progress imagery.
4. Treat generated video as motion reference, then redraw/overlay it in JavaScript with a papery handcrafted look. Plan compositions so kinetic lyrics alternate between subtitle scale and large hook typography.
5. Use ElevenLabs for sound design if needed, preserve the song, and design the first seconds as a strong social-feed hook.
6. Rewatch the whole cut repeatedly, inspect stills, check composition/timing/continuity and redo weak scenes before the final export. Keep API keys outside the published project.

<a id="case-2103304514329854102"></a>
### A five-minute superintelligence documentary

1. Give the Claude agent access to Figma and Runway through MCP.
2. Ask for a high-end, Netflix-style documentary that explains superintelligence to a general audience.
3. Have the agent research, script, storyboard, design graphics, create footage and assemble the cut; verify every factual claim and review pacing for non-experts. No more detailed public prompt was disclosed.

<a id="case-2103381720410333314"></a>
### Anthropic's Rise, Rendered in Code

1. Ask for an animation about Anthropic's philosophy and rise, including music and sound effects; permit any suitable tool/technique but prohibit existing skills and reuse of earlier videos or copy.
2. The creator later disclosed WebGL and Canvas for visuals and code-synthesized music/SFX. Build an original timeline, generate visuals and audio deterministically, and synchronize both in a scripted render.
3. Fact-check the company history, review mobile legibility and mix levels, then export. No more detailed shot list was made public.

<a id="case-2102471841046786153"></a>
### Procedural Blender Shot and Build Timelapse

1. Use one prompt: Blender only, fully procedural; create and render a 10-second shot and record the build process as a timelapse.
2. Build geometry, materials, lights, camera and animation through reproducible Blender operations/scripts; save milestones while recording the viewport.
3. Render the final ten-second shot and separately accelerate the build recording into a timelapse. No scene-specific art direction was disclosed.

<a id="case-2102450239923720440"></a>
### Prehistoric Island Comparison

1. Deliver one standalone Three.js/WebGL HTML file containing a polished miniature island: varied terrain, forest, waterfall, pond, volcano, research station, nests and a transparent underwater cross-section.
2. Add anatomically readable dinosaur species and pterosaurs. Use hierarchical rigs, stance/swing gait phases, terrain sampling, inverse kinematics, weight shifts and obstacle-safe paths; prevent sliding, floating and intersections.
3. Build water as a deep visible volume with seabed life, animated waves, Fresnel reflection, caustics, foam and splashes while avoiding transparency gaps/artifacts.
4. Implement camera orbit/zoom/follow, food placement, drinking/resting/calling/herd behaviors, hatching, marine surfacing, day/sunset/night, weather/volcano controls, pause and reset. Make every action repeatable and visually obvious.
5. Add responsive compact UI, user-gated audio, instanced vegetation, efficient geometry, restrained post-processing and suitable shadows.
6. Open the final HTML directly in desktop Chrome, inspect screenshots and console, exercise all controls, and fix loading, collision, gait, water and camera defects before delivery.

<a id="case-2102913101926731879"></a>
### Lip-balm ad: Opus and Astra comparison

1. Supply the same brand assets and music to each model.
2. Ask each to create a 20-second product video in After Effects timed to the music.
3. Keep the After Effects project editable, review brand accuracy and beat sync, then compare the creative choices. The creator reported that Opus used travel/lifestyle scenes while Astra favored bold type, shapes and product close-ups; no longer prompt was published.

<a id="case-2103918792845963545"></a>
### Pocketsflow motion-graphics promo

1. Ask for a dynamic 15-second résumé-quality motion-graphics video about Pocketsflow and give the model broad creative freedom.
2. Provide an ElevenLabs key securely through the environment (the public post used a redacted placeholder), and request a speaking character who explains what Pocketsflow is, how people use it and what it enables.
3. Build a concise hook–features–payoff sequence, synthesize narration, synchronize character/action/type to the voice, then check the whole 15-second cut for mobile readability and audio peaks.

<a id="case-2103099194693271874"></a>
### Pip in an AI-generated world

1. Study `reference/pip_sheet.png`; write a character bible and extract the exact cream/yellow/orange/graphite/brown/mint palette with PIL. Lock Pip's helmet/visor silhouette, antenna flag, trim, claws and four wheels across every style.
2. Use Remotion with React/TypeScript at 1920×1080, 30 fps, H.264 around CRF 14. Build a hierarchical SVG cutout rig with procedural visor expressions, spring antenna/suspension, wheel rotation, pose cycles, a chest hatch/sprout and a style-skin interface. Pass a turnaround/expression lineup review before continuing.
3. Build layered worlds (base overgrown city, anime Tokyo, clay village, medieval battlefield, toy-brick city, underwater and pencil sketch) with low macro-scale camera framing. Keep the sprout as the emotional through-line.
4. Create an 8–12-frame diffusion-style `RegenTransition`: old world dissolves to structured noise, new world denoises, Pip lags one beat in a half-old/half-new skin, and the visor glitches for two frames.
5. Follow the six-act beat sheet: good morning (0–3s), rapid worlds (3–14s), escalating prompt gags (14–30s), Pip protects the sprout and types “let me out” (30–38s), freeze/pull-back phone reveal (38–47s), then a second Pip receives the first prompt and cuts seamlessly to frame one (47–50s).
6. Add a seeded virtual camera, four-plus parallax layers, macro depth cues, motion blur and per-world lighting. Keep all prompt text phone-readable and type it with human timing.
7. Synthesize Pip's chirps, servos, footsteps, score variants and effects in Python/Web Audio; mix with FFmpeg to about −14 LUFS and keep replaceable stems.
8. Work through plan → rig → world contact sheet → transition test → 960×540 animatic → animation → polish → finish → audio → final. For every shot, review 3–5 stills at least three times and score identity, emotion, joke, composition, scale, depth, lighting, polish and phone readability to at least 8/10.
9. Deliver the final MP4, a twice-concatenated loop check, poster frame, cross-world lineup and documented source. The public finished post is 75 seconds although the disclosed brief targets roughly 50 seconds, so treat timing as the produced variant rather than an exact match.

## 中文

<a id="case-2102787937482252537-zh"></a>
### 推理服务创业公司发布解释视频

1. 提供产品名称、Logo、界面截图和核心推理卖点。
2. 使用作者公开的完整要求：“为一家做推理服务的现代创业公司制作现代、精致、节奏鲜明的视频。”作者没有公开额外分镜或渲染参数。
3. 让 Agent 把内容组织为开场钩子—能力证明—结果，先出预览，再修正小字和节奏后导出。

<a id="case-2103315922098470926-zh"></a>
### 15 秒动态图形作品集

1. 要求制作 15 秒、适合作为求职作品集的高水平动态图形短片，并明确“尽情发挥”。
2. 视觉系统、字体、转场和配乐均交给 Agent 自主决定；作者未公开其他限制。
3. 低清预览检查前两秒钩子、连续运动和结尾记忆点，再导出 15 秒母版。

<a id="case-2103273003555402193-zh"></a>
### 无缝 UI 形态变换循环

1. 准备 8–12 个 UI 状态、黑白或单一强调色，以及约 120 BPM 的免版税音乐。
2. 在暖灰画布上让同一个元素连续改变尺寸、圆角和颜色，内容以短模糊切换；所有变化必须由可见光标真实点击/拖拽触发。使用 Geist、轻微过冲弹簧和跟随状态的镜头缩放；禁止弹跳缓动、粒子爆发、发光、UI 渐变、图标线宽不一致、空等和模板感。
3. 七小节逐拍排列：按钮→加载→勾选→灵动岛→播放器与播放/暂停→拖动进度→超限拉伸音量条→开关→液态 Tab 指示器→自绘图表与提示框→⌘K→输入过滤→Enter→通知→回到按钮。
4. 只做一个 1440×1440 HTML；每个样式都由 `seek(t)` 计算，不用 CSS transition、计时器或跨帧状态。弹簧采用闭式阶跃响应，多次目标变化用响应叠加；Tab 两边和开关旋钮使用独立弹簧；按住拖拽时数值由光标位置直接决定，释放后从当前位置回弹。
5. 用 NumPy 分析音乐节拍，从强拍起步，并让每个 UI 音效落在测得的峰值。Playwright 每个输出帧渲染 4 个子帧，再用 FFmpeg `tmix` 合成为带运动模糊的 60 fps。
6. 全片渲染前先每拍输出一帧，修正偏拍、拥挤和难读内容。被镜头缩放的元素不要用 `will-change`；容器内文字分别设置出入时间；最后一帧连同光标位置与速度必须和第一帧完全一致。

<a id="case-2103557735086428547-zh"></a>
### 动态设计与声音工程演示

1. 让 Opus 5.5 制作 90 秒动态设计与声音工程演示，并原创钢琴配乐。
2. 作者没有公开场景表、素材或渲染设置，因此复现时应让 Agent 自主完成构图和视觉方向。
3. 画面与音乐一起审看，修正同步和响度后输出连续的 90 秒母版。

<a id="case-2102591147927654847-zh"></a>
### 交互式相机镜头实验室

1. 要求 Opus 通过交互镜头实验室解释相机对焦。
2. 制作对焦环控制：拖动时镜片组移动，同时画面中的清晰平面前后移动。
3. 遍历控制范围，确保用户无需旁白也能理解因果；作者没有公开更多技术栈或提示词。

<a id="case-2102583898865873225-zh"></a>
### 五千年中国历史

1. 要求快速回顾中华五千年历史，风格轻松有趣、线稿动画、配合适音乐并保持吸引力。
2. 先研究并按时代整理时间线，再把每次朝代/时代变化变成清晰视觉节拍。
3. 导出前核对年代、名称、字幕可读性和配乐同步；作者未公开其他参数。

<a id="case-2102606609574941028-zh"></a>
### 大气环流讲解

1. 选择任意 TTS 服务，把接口文档保存成 `TTS.md`；在 `.env` 写入 `APIKEY`、`VOICE` 及其他配置。
2. 在 `.claude/settings.json` 加入 `"deny": ["Read(./.env)"]`，禁止 Claude 直接读取密钥。
3. 要求制作高中地理“大气环流”线稿动画：轻松有趣、配乐、中英双语字幕、TTS 解说；接口支持时关闭水印；提示 Agent 查阅 `TTS.md` 并使用环境变量名，最终视频须可直接导出。
4. 审核气象知识、发音以及旁白/字幕同步后导出。

<a id="case-2102853258582880547-zh"></a>
### 鸡尾酒配方动态图

1. 提供参考图、完整配方和准确用量。
2. 要求用 JavaScript/HTML 做 30 秒说明动画，从空杯开始，按顺序显示每种原料和用量，最后得到成品。
3. 建立时间轴，核对倒入顺序和数值，浏览器预览后录制/渲染为视频。

<a id="case-2103116235009347650-zh"></a>
### 奥斯特里茨战役

1. 要求用代码制作 4–5 分钟、讲述 1805 年奥斯特里茨战役的电影感短片；必须充分研究、史实准确、战略易懂且视觉出色。
2. 附图仅作为规模、烟雾、天空、骑兵、阵列、地形和混乱感参考，不照抄，也不能做成普通信息图或策略游戏。
3. 叙事结构、节奏和代码视觉语言交给 Agent；完成后核对时间线与战术，反复看片修节奏再终渲染。

<a id="case-2102680453912449223-zh"></a>
### 物理竞赛题讲解

1. 沿用作者此前的知识动画提示词，把宽泛知识点换成具体竞赛题。
2. 要求明确假设、画出受力/几何图、逐步推导公式，并同步旁白、标注和动画。
3. 独立复核答案并以手机尺寸检查；作者没有公开更长的本题提示词。

<a id="case-2102827887732932956-zh"></a>
### 真人口播转动画 B-roll

1. 在 Claude Code 的 safe mode、high effort 下输入竖屏源 MP4，不加载 Skill，也不给外部素材。
2. 要求原声、原字幕和时长完全不变；把人物缩成右下角可看清讲话、且不挡字幕的圆形画中画。
3. 主画面改为轻松有趣的线稿 B-roll，讲到什么概念就画什么。公开流程使用 Python 逐帧绘制，并按字幕切约 30 个镜头。
4. 逐个字幕边界检查画面、画中画、音轨和总时长，再以新文件名导出。

<a id="case-2103511590884815282-zh"></a>
### 印尼 81 年历史

1. 先要求做求职作品集级的动态设计短片，并允许充分发挥。
2. 把主题限定为印度尼西亚从第一任总统至今的历史，要求给出有趣、出人意料的故事板。
3. 核对总统时间线，平衡各时代篇幅，补充清晰日期/姓名并审查节奏；作者未公开更多技术细节。

<a id="case-2102476258948927543-zh"></a>
### 像素巫师

1. 单个离线 HTML，原生 JavaScript + Canvas 2D；在 128×96 离屏画布绘制后整数倍放大，关闭平滑，全部坐标取整，使用约 24 色固定色板。
2. 用矩形/像素段程序化搭建约 24×32 的巫师，参数化法杖角度、手臂、头部和袍摆；连续插值后量化成 8–12 fps 的像素动作感。
3. 做 `IDLE→CHARGE→CAST→RECOVER` 无缝状态机，包含蓄力火花、法术弹、1–2 px 震屏和恢复。
4. 预分配粒子池，以色板索引控制颜色变化；固定 60 Hz 更新，循环中零分配。
5. 加入简洁夜景与宝石轮廓光，验证整数缩放、稳定 60 fps、轮廓可读和循环接缝。

<a id="case-2102495989194236158-zh"></a>
### Opus 的一生

1. 让 Claude Opus 5.5 从诞生之日开始动画化讲述自己的一生。
2. 视觉只允许 JavaScript 绘制的笔触，不用视频模型和图片素材。
3. 让 Agent 自主选择里程碑和象征，之后检查连续性与历史表述；没有公开更长提示词或渲染参数。

<a id="case-2102493303388475855-zh"></a>
### 慕尼黑啤酒节

1. 截取目标角色截图并作为身份参考图输入。
2. 引用帖只写到“这是完整提示词”“Have fun”，未显示实际制作说明；因此不能把未公开内容当作作者提示词。
3. 复现时自行定义节庆环境与动作，但要逐镜头保持角色轮廓和配色一致。

<a id="case-2102515055116063144-zh"></a>
### 彩虹道路像素动画

1. 单个离线 Canvas HTML；160×90 逻辑分辨率、整数倍放大、关闭平滑，全部整数坐标，约 32 色固定色板，禁用渐变/旋转/模糊/抗锯齿。
2. 严格重现 12×8 橙色四足角色，增加高光/阴影像素和量化的四帧跑步循环、挤压、拉伸、前倾。
3. 构建七色波浪道路、分隔线、缺口与跳台；加入三层星空视差、星球/星云和随速度增加的速度线。
4. 以固定攻击序列生成流星和带预警线的光束；分别分配跳跃、二段跳、滑铲或彩虹残影冲刺，并加入擦边定格、慢动作和确定性震屏。
5. 状态机为 `RUN→WARN→DODGE→NEAR_MISS→RUN`，结尾 `BOOST→WARP` 接回开头；粒子池预分配、60 Hz 固定更新且循环中零分配。
6. 验证轮廓、无缝循环、帧率，以及每次闪避是否同时表现“快、险、酷”。

<a id="case-2102573127192727704-zh"></a>
### 新西兰丙烯画

1. 输入新西兰旅行照片，要求 Opus 5.5 全部用 JavaScript 重绘成丙烯画风。
2. 提取统一色板和笔触系统，把每张照片拆成多层程序化笔触，同时保持构图可识别。
3. 加入转场和镜头运动，与原图对比代表帧；作者没有公开更长提示词或渲染配方。

<a id="case-2102801274173587569-zh"></a>
### Claude Pop 混合流程音乐视频

1. 提供原 MP4/音轨、歌词、源代码仓库和参考资料；保留完全相同的音轨，独立重做完整 MV。
2. 调研当代动态图形、K-pop 和互联网粗野主义，制作统一风格表、拟人化 Claude 主角及配角，避免千篇一律的 Pixar 感。
3. 生成一致的角色表、场景和 Seedance 2.5 基础镜头；用歌曲切片或参考音频校验时序/口型。表演镜头与非对口型插叙混合，并融入当下 AI 进展语境。
4. 把生成视频当运动参考，再以 JavaScript 重新描摹/叠加成纸张手工感。构图预留歌词空间，让小字幕和大型钩子文字交替出现。
5. 需要时用 ElevenLabs 做音效但保留原歌曲；前几秒必须有信息流钩子。反复通看、截帧检查构图/时序/连续性，弱镜头返工后再导出；API Key 不进入公开项目。

<a id="case-2103304514329854102-zh"></a>
### 五分钟超级智能纪录片

1. 为 Claude Agent 接入 Figma 和 Runway MCP。
2. 要求制作高端 Netflix 风格、面向普通观众解释超级智能的纪录片。
3. 由 Agent 研究、写稿、故事板、图形设计、生成素材并剪辑；逐条核实事实，为非专业观众检查节奏。作者没有公开更多提示词。

<a id="case-2103381720410333314-zh"></a>
### 用代码呈现 Anthropic 的崛起

1. 要求围绕 Anthropic 的理念与发家史制作动画，包含音乐和音效；可用任意技术，但不能使用已有 Skill，也不能参考过去的视频或文案。
2. 作者后来说明画面由 WebGL/Canvas 生成，音乐和音效也由代码合成。制作原创时间线，以确定性方式生成视听并同步渲染。
3. 核对公司史，以手机尺寸检查文字并校正混音后导出；未公开更多分镜。

<a id="case-2102471841046786153-zh"></a>
### Blender 程序化镜头与制作延时

1. 单条任务：仅用 Blender、全部程序化；制作并渲染 10 秒镜头，同时录制自己的搭建过程。
2. 通过可复现操作/脚本完成模型、材质、灯光、相机和动画，录制视口并保存里程碑。
3. 渲染 10 秒成片，另将搭建录像加速为延时视频；作者没有公开具体场景美术方向。

<a id="case-2102450239923720440-zh"></a>
### 史前岛屿交互场景

1. 交付单个 Three.js/WebGL HTML：包含丰富岛屿地形、森林、瀑布、池塘、火山、研究站、巢穴和透明水下剖面。
2. 制作可辨识的多种恐龙/翼龙；使用层级骨骼、支撑/摆动步态、地形采样、IK、重心变化和避障路径，杜绝滑步、漂浮和穿模。
3. 水体要有可见深度、海床生物、波浪、Fresnel 反射、焦散、泡沫和水花，同时避免透明排序裂缝。
4. 实现旋转/缩放/跟随相机、投食、饮水/休息/鸣叫/群体移动、孵化、海生爬行动物出水、昼夜、天气/火山、暂停和重置；所有交互可重复且反馈明确。
5. 加入紧凑响应式界面、用户操作后才播放的音频、实例化植被、高效几何和克制后期。最终直接在桌面 Chrome 打开，检查截图/控制台并遍历全部交互，修复加载、碰撞、步态、水体和相机问题。

<a id="case-2102913101926731879-zh"></a>
### 润唇膏广告模型对比

1. 给两个模型完全相同的品牌素材和音乐。
2. 要求在 After Effects 制作 20 秒、与音乐同步的产品视频。
3. 保持工程可编辑，检查品牌一致性和踩点后比较创意。作者说明 Opus 使用旅行/生活方式场景，Astra 偏向粗体字、形状和产品特写；未公开更长提示词。

<a id="case-2103918792845963545-zh"></a>
### Pocketsflow 动态图形宣传片

1. 要求制作 15 秒、求职作品集级的 Pocketsflow 动态图形宣传片，并允许充分发挥。
2. 通过环境变量安全提供 ElevenLabs Key（公开帖只放了占位符），让角色讲清 Pocketsflow 是什么、如何使用以及能做什么。
3. 组织为钩子—功能—收益，生成旁白并把角色、文字和运动与声音对齐，最后检查手机可读性和音频峰值。

<a id="case-2103099194693271874-zh"></a>
### 被困在 AI 世界里的 Pip

1. 研究 `reference/pip_sheet.png`，写角色圣经，用 PIL 从色卡提取奶油/黄/橙/石墨/棕/薄荷蓝；所有风格必须锁定头盔屏幕轮廓、天线旗、黄边、爪臂和四轮。
2. 使用 Remotion + React/TypeScript，1920×1080、30 fps、H.264、约 CRF 14。建立 SVG 层级骨骼、程序化屏幕表情、弹簧天线/悬挂、轮子、动作循环、胸舱幼苗和样式皮肤接口；先通过四视图+表情 lineup 验收。
3. 制作基础废墟城市、动漫东京、黏土村庄、中世纪战场、积木城、水下、铅笔稿七类多层世界；低机位微距构图，小幼苗作为跨世界情感锚点。
4. `RegenTransition` 用 8–12 帧：旧画面从边缘扩散成结构噪声，新画面由粗到细去噪；Pip 延迟一拍保持半新半旧样式，屏幕故障 2 帧。
5. 六幕时间表：0–3 秒日常；3–14 秒快速跨世界；14–30 秒提示词逐级荒诞；30–38 秒 Pip 收好幼苗并输入 “let me out”；38–47 秒冻结并拉远揭示手机；47–50 秒第二只 Pip 收到第一条提示并无缝切回首帧。
6. 使用带种子虚拟相机、至少四层视差、微距景深、运动模糊和分世界灯光；提示框采用自然打字节奏并保证手机可读。
7. 用 Python/Web Audio 合成 Pip 鸣叫、伺服/轮子、分世界配乐和音效，再以 FFmpeg 混音到约 −14 LUFS，并保留可替换 stems。
8. 流程必须为计划→骨骼→世界联系表→转场测试→960×540 animatic→正式动画→润色→成片效果→声音→终版。每镜至少三轮、每轮检查 3–5 张静帧，对角色一致、情绪、笑点、构图、尺度、深度、灯光、精致度和手机可读性评分，全部达到 8/10 才继续。
9. 交付终版 MP4、连续播放两遍的循环检查、海报帧、跨世界 lineup 和带说明的源码。公开成片为 75 秒，而提示词目标约 50 秒，应视为制作过程中的时长扩展版本。
