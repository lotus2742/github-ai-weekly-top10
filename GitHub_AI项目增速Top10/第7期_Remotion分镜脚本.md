# 🎬 Remotion 视频分镜脚本 — 第7期

> **总时长**：约2分30秒
>
> **规格**：1080×1920（竖屏）/ 1920×1080（横屏）
>
> **音频**：AI配音 + 背景BGM + 音效
>
> **核心原则**：画面动画承担信息展示，配音承担情绪引导，字幕做 reinforcement

---

## 📐 Remotion 组件结构总览

```
RootComposition
├── Scene01_Hook          // 开场钩子（8秒）
├── Scene02_Overview      // 榜单总览（10秒）
├── Scene03_Top1          // 第1名深度（20秒）
├── Scene04_Top2          // 第2名（12秒）
├── Scene05_Top3          // 第3名（12秒）
├── Scene06_Top4          // 第4名（12秒）
├── Scene07_Top5          // 第5名（14秒）
├── Scene08_Top6_10       // 后5名快闪（25秒）
├── Scene09_Trend         // 趋势分析（20秒）
└── Scene10_Outro         // 互动+CTA（8秒）
```

---

## 🎬 逐场景分镜

---

### Scene01：开场钩子（0:00 - 0:08）

**配音**：

> "这周 GitHub 周榜有点夸张——一个叫 i-have-adhd 的 Agent 技能，七天涨了 1.6 万颗星，把 DeepSeek 官方 Harness 和微软 markitdown 全甩在后面。说白了：大家终于忍不了 AI 把答案藏在废话里了。"

**画面动效**：

```
帧0-2秒：
  深色背景（#0d1117，GitHub暗色风格）
  中央大数字 "16,476" 从0滚动到16476（数字滚动动画）
  数字颜色：金色渐变（#FFD700 → #FFA500）
  右上角小字："⭐ stars this week"
  下方小字："i-have-adhd · 断层第一"

帧2-4秒：
  数字缩小移到左侧
  右侧依次快闪三张卡片（各0.6秒）：
    "archify +10,299" "deepseek-harness +8,842" "markitdown +5,120"
  三张卡片被左侧大数字「压下去」的动画（向下位移+透明度降低）

帧4-6秒：
  对比卡片淡出
  中央弹出问题文字："Agent 话太多，答案在哪？"
  文字带打字机效果，关键词 "答案" 高亮黄色

帧6-8秒：
  文字向上滑出
  底部滑入："GitHub AI 项目 Star 增速 Top 10"
  "第7期 | 2026年第37周"
```

**字幕**：与配音同步，底部居中，白色文字+半透明黑底

**音效**：

- 0秒：低沉的"咚"（吸引注意）
- 2秒：数字滚动时的"滴滴滴"快速音效
- 4秒：卡片被压下时的"砰"轻音
- 6秒：文字弹出时的"叮"

---

### Scene02：榜单总览（0:08 - 0:18）

**配音**：

> "先看本周 Top 10 全貌。数据来自 star-history.com，统计周期 9 月 6 号到 9 月 12 号。前 10 名本周新增从 5120 到 16476，第一名大约是第十名的 3 倍。更关键的是：第十名都要 5000 多星，说明 AI 开源这周整体在加速，不是个别项目偶然爆红。"

**画面动效**：

```
帧8-10秒：
  标题滑入："📊 本周 Top 10 全貌"
  副标题："star-history.com | 9.6 - 9.12"

帧10-15秒：
  柱状图从左到右依次生长（每个柱子0.4秒）
  柱子颜色：渐变色（第1名金色，2-3名橙色，4-5名蓝色，6-10名灰色）
  每个柱子顶部显示项目名+Star数
  第1名 i-have-adhd 柱子极高，带发光效果
  第3名 deepseek-harness 柱子标注 "DeepSeek 官方" 徽章

帧15-17秒：
  柱状图上方弹出标注："≈3x"
  箭头从第10名 markitdown 指向第1名
  底部弹出："Top10 门槛：+5,120⭐"

帧17-18秒：
  柱状图整体向左移出画面
```

**字幕**：底部，关键数字高亮

**音效**：

- 柱状图生长时每个柱子配一个轻微的"噔"音
- "3x"与门槛数字弹出时配"叮"

---

### Scene03：第1名 i-have-adhd 深度解读（0:18 - 0:38）

**配音**：

> "第一名，i-have-adhd。别被名字吓到，它不是医学软件，而是一套 Claude Code 技能：专门治 Agent『把结论埋在最后、前面全是铺垫』的毛病。ADHD 友好输出，说白了就是——先给答案，再给细节，别让人翻半天日志。一周 1.6 万星，说明这不是小众痛点，是几乎所有用编码 Agent 的人都在骂的事。总星 4.4 万，传播速度已经验证过了。"

**画面动效**：

```
帧18-20秒：
  大标题从底部弹入："🥇 第1名 · 断层领跑"
  项目名 "i-have-adhd" 带发光效果
  右侧大数字 "+16,476⭐" 金色脉冲动画
  下方小字："ayghri/i-have-adhd"

帧20-24秒：
  标题上移到顶部
  中央对比两种 Agent 回复结构：
    左侧："❌ 冗长铺垫"（长文本块，答案在底部，红色）
    右侧："✅ 答案前置"（顶部高亮结论，下方折叠细节，绿色）
    中间箭头："Stop burying the answer"

帧24-28秒：
  对比图缩小
  三个标签依次弹入："claude-skills" "productivity" "developer-tools"
  下方文字："先结论 · 后细节"

帧28-32秒：
  中央展示 Star 增长曲线（陡峭上升）
  曲线上标注 "本周 +16476"
  对比虚线："第6期 Top1 仅 +414"（灰色）

帧32-36秒：
  中央大字弹出："可读性 = 生产力"
  下方逐行出现：
  "Claude Code 插件" "结构化输出" "4.4万总星"

帧36-38秒：
  文字淡出，过渡到下一场景
```

**字幕**：底部，关键词高亮（"答案前置""16476""4.4万"）

**音效**：

- 对比切换时配"嗖"
- 曲线爬升时配上升音调
- "断层领跑"弹出时配重音"咚"

---

### Scene04：第2名 archify（0:38 - 0:50）

**配音**：

> "第二名 archify，+10299 星。它干的事很具体：让 Agent 画出能进评审、能导出的架构图、时序图、数据流图，自包含 HTML，还带动效。和 Mermaid 比，它强调的是『好看、可验证、能交付』。而且它是 DeepSeek Harness 插件生态里的明星，这周 Harness 官方仓库也进了前三，说明插件经济真的起来了。"

**画面动效**：

```
帧38-40秒：
  标题弹入："🥈 第2名 · 万星技能"
  "archify" + "DSH Plugin" 标签
  "+10,299⭐" 橙色
  下方小字："tt-a1i/archify"

帧40-44秒：
  中央展示架构图卡片从模糊到清晰（focus 动画）
  图类型轮播：架构图 → 时序图 → 数据流图（各1秒）
  右下角 "Export HTML" 按钮闪烁

帧44-47秒：
  左侧 Mermaid 示意图（灰、打叉 "slop"）
  右侧 archify 示意图（彩色、打勾 "editorial"）
  中间 "diagram-as-code" 标签

帧47-50秒：
  archify 卡片与 deepseek-harness logo 连线动画
  文字："Harness 生态 · 插件飞轮"
  淡出
```

**音效**：

- 图类型切换时配轻"咔哒"
- 连线动画配"叮"

---

### Scene05：第3名 deepseek-harness（0:50 - 1:02）

**配音**：

> "第三名，DeepSeek 官方的 deepseek-harness，+8842 星，总星已经 22 万级别。口号是 Everything is a Plugin——把 Agent 运行时做成操作系统，技能、工具全是插件。这周 archify 暴涨，本质上就是用户在给这套 OS 装应用。如果你还在单独追某个 Skill 仓库，可能要开始看 Harness 这条主线了。"

**画面动效**：

```
帧50-52秒：
  标题："🥉 第3名 · 官方 Harness"
  DeepSeek logo + "deepseek-harness"
  "+8,842⭐"
  总星徽章："222K+ total"

帧52-56秒：
  中央 OS 隐喻动画：
    内核圆环 "Harness / Cordis"
    外围插件图标轨道旋转（archify、ponytail、skills 等简化图标）
  文字："Everything is a Plugin"

帧56-58秒：
  插件图标其中一个放大为 archify，标注 "+10,299 本周"
  箭头回到内核："生态反哺运行时"

帧58-62秒：
  三个关键词弹出："TypeScript" "MIT" "ai-agents"
  画面淡出
```

**音效**：

- 轨道旋转时低频嗡嗡
- 插件弹出时"叮叮"

---

### Scene06：第4名 ponytail（1:02 - 1:14）

**配音**：

> "第四名 ponytail，+8698 星，老面孔了但增速一点没慢。理念还是那句：让 Agent 像最懒的高级工程师，YAGNI，别过度设计。和第一名的 i-have-adhd 一对照——一个管『少说废话』，一个管『少写废话代码』，工程师想要的 Agent 越来越像人。"

**画面动效**：

```
帧62-64秒：
  标题："第4名 ponytail"
  "+8,698⭐" 紫色
  "YAGNI" 徽章脉冲

帧64-68秒：
  左右对比：复杂类图（叉） vs 最小实现（勾）
  引用句淡入："The best code is the code you never wrote."

帧68-72秒：
  双卡片并列：
    左 "i-have-adhd：输出结构"
    右 "ponytail：代码克制"
  中间 "=" "像资深同事"

帧72-74秒：
  淡出
```

**音效**：

- YAGNI 徽章配"咚"
- 对比切换配"嗖"

---

### Scene07：第5名 skills（1:14 - 1:28）

**配音**：

> "第五名，mattpocock 的 skills，+7814 星，总星 26 万+。这是『从真实 .agents 目录里抠出来的技能』，不是演示型 prompt。Top 10 里一半都在卖 Skills，但 skills 这个仓库一直是很多人的复制起点——你 fork 一份，改成自己的工程规范，比从零写 system prompt 省事太多。"

**画面动效**：

```
帧74-76秒：
  标题："第5名 skills"
  "+7,814⭐"
  头像区：mattpocock 风格占位图 + "from .agents/"

帧76-80秒：
  目录树动画展开：
    skills/
    ├── real-engineering-rule-1
    ├── real-engineering-rule-2
    └── ...
  每行 0.3 秒淡入

帧80-84秒：
  中央 "Fork → Customize" 流程三步图标
  总星数字滚动到 "261,265"

帧84-88秒：
  Top10 条形高亮：6/10 项目带 "Skills" 标签
  文字："Skills = 新依赖管理"
  淡出
```

**音效**：

- 目录展开配键盘敲击
- 总星滚动配计数器

---

### Scene08：后5名快闪（1:28 - 1:53）

**配音**：

> "快速过后面五名。第六 ECC，跨工具的 Agent 元优化，记忆、安全、研究一体，+7403。第七 diagram-design，38 种编辑级图表，拒绝 Mermaid slop，+7174。第八 VoiceStudio，本地 ElevenLabs 替代，配音克隆转写一条龙，+5818。第九 orca，并行 Agent 舰队的 ADE，桌面移动都能用，+5177。第十微软 markitdown，文件转 Markdown 的 RAG 老基建，+5120——注意，它这周只能当第十名门槛。"

**画面动效**：

```
帧88-93秒（#6 ECC）：
  左侧大 "6" 金色描边
  卡片：ECC +7403⭐
  图标环：Claude / Cursor / Codex / MCP
  关键词："memory · security · harness"

帧93-98秒（#7 diagram-design）：
  大 "7"
  38 个迷你图表图标雨（简化）
  "+7,174⭐" "No Mermaid slop"

帧98-103秒（#8 VoiceStudio）：
  大 "8"
  波形 + 麦克风图标
  标签："local TTS · voice clone · 646 langs"
  "+5,818⭐"

帧103-108秒（#9 orca）：
  大 "9"
  多窗口 Agent 并行示意图（3个终端）
  "ADE · parallel agents"
  "+5,177⭐"

帧108-113秒（#10 markitdown）：
  大 "10"
  Microsoft logo + PDF→MD 箭头
  "+5,120⭐"
  门槛线动画："Top10 floor"

帧113-115秒：
  #6-#10 五卡扇形排列，整体滑出
```

**字幕**：每个项目名与 Star 数底部快闪

**音效**：

- 每个名次切换配短促"噔"
- #10 门槛线配"叮"

---

### Scene09：趋势分析（1:53 - 2:13）

**配音**：

> "说三个趋势。第一，万星周增速成为新常态，Top 10 底线跳到五千以上。第二，DeepSeek Harness 加插件，正在复制『操作系统加应用商店』的故事，archify 就是样板。第三，体验类 Skills 爆发——可读输出、少写废代码、能交付的图，和 orca 这种并行编排、VoiceStudio 这种本地语音，一起把 Agent 从聊天框推向真实工作流。"

**画面动效**：

```
帧113-123秒：趋势一
  左侧大数字 "01"
  标题："万星周增速"
  中央：门槛线从 "+152" 跳到 "+5,120" 的动画
  文字："整体加速，非偶然"

帧123-133秒：趋势二
  左侧 "02"
  标题："Harness · 插件飞轮"
  中央：deepseek-harness 内核 + 插件轨道
  archify 高亮连线

帧133-143秒：趋势三
  左侧 "03"
  标题："体验 + 编排 + 多模态"
  三图标三角布局：
    i-have-adhd / ponytail / diagram（体验）
    orca（编排）
    VoiceStudio（语音）
  下方："从 Chat 到 Workflow"

帧143-145秒：
  三个趋势缩小排列，淡出
```

**音效**：

- 每个趋势数字弹出时配"咚"
- 门槛跳跃时配"嗖"
- 结束配轻柔和弦

---

### Scene10：互动+CTA（2:13 - 2:21）

**配音**：

> "完整榜单和所有 GitHub 链接我放在评论区置顶了。这周 10 个项目你最想试哪个？评论区聊聊。每周一更新 GitHub AI 项目周报，关注不迷路，我们下期见。"

**画面动效**：

```
帧133-135秒（注：时间轴 2:13 对应 133秒自0:00，此处按场景内 0-8秒描述）：
  深色背景
  中央弹出："完整榜单 ⬇️"
  下方箭头指向"评论区"图标

帧135-137秒：
  文字变为："你用过几个？"
  下方出现数字 1-10 的按钮动画（模拟评论选择）

帧137-139秒：
  文字变为："每周一更新"
  下方弹出关注按钮动画 + 铃铛图标

帧139-141秒：
  最终画面：
  "GitHub AI 项目 Star 增速 Top 10"
  "第7期 | 2026年第37周"
  底部小字："数据来源：star-history.com"
  画面静止2秒后淡出
```

**音效**：

- 135秒：轻柔的"叮"
- 139秒：结束音效（短促的"叮咚"）

---

## 🎨 视觉设计规范

| 属性 | 值 |
|------|---|
| **背景色** | #0d1117（GitHub暗色） / 深色渐变 |
| **主文字色** | #FFFFFF |
| **副文字色** | #8b949e |
| **第1名强调色** | #FFD700（金色） |
| **第2名强调色** | #C0C0C0（银色） |
| **第3名强调色** | #CD7F32（铜色） |
| **4-5名强调色** | #58A6FF（蓝色） |
| **6-10名强调色** | 各不相同（粉/绿/紫/蓝/橙） |
| **Harness/插件色** | #4D6BFE（DeepSeek 蓝紫） |
| **YAGNI标签色** | #A371F7（紫色） |
| **本地语音色** | #3FB950（绿色） |
| **字体** | 标题用粗体无衬线（如 Inter Bold），正文用常规 |
| **圆角** | 12px（卡片）/ 8px（标签） |
| **阴影** | 卡片用 0 4px 20px rgba(0,0,0,0.3) |

---

## 🔊 音频设计规范

| 类型 | 说明 |
|------|------|
| **BGM** | 科技感电子乐，80-100 BPM，不抢配音 |
| **配音** | AI TTS，语速适中（约3字/秒），语气带点兴奋 |
| **音效库** | 数字滚动、弹出、滑动、切换、轨道旋转各有对应音效 |
| **混音** | 配音 > BGM > 音效，配音清晰度优先 |

---

## 📦 Remotion 组件拆分建议

```
components/
├── layouts/
│   ├── DarkBackground.tsx        // 统一深色背景
│   ├── SubtitleBar.tsx           // 底部字幕栏
│   └── SceneTransition.tsx      // 场景过渡动画
├── ranking/
│   ├── RankingCard.tsx           // 排名卡片（编号+项目名+Star数）
│   ├── BarChart.tsx              // 柱状图组件
│   ├── ThresholdLine.tsx         // Top10 门槛线动画（新增）
│   └── RankingList.tsx           // 排名列表
├── project/
│   ├── ProjectHero.tsx           // 项目展示头部（名次+名称+Star）
│   ├── AnswerFirstCompare.tsx    // 答案前置对比（新增）
│   ├── DiagramCarousel.tsx       // 架构图轮播（新增）
│   ├── HarnessOrbit.tsx          // Harness 插件轨道（新增）
│   ├── YAGNIComparison.tsx       // YAGNI 对比视图
│   ├── DirectoryTree.tsx         // skills 目录树
│   ├── WaveformMic.tsx           // VoiceStudio 波形
│   ├── ParallelTerminals.tsx     // orca 并行终端
│   └── TagCloud.tsx              // 关键词标签
├── trend/
│   ├── TrendCard.tsx             // 趋势卡片
│   └── TriangleLayout.tsx        // 三角趋势布局（新增）
├── numbers/
│   ├── CountUp.tsx               // 数字滚动动画
│   └── StarCounter.tsx           // Star计数器
└── outro/
    ├── CTAButton.tsx             // 关注/评论CTA
    └── EndCard.tsx               // 结尾卡片
```

---

## 📋 素材准备清单

| 素材 | 格式 | 用途 | 来源 |
|------|------|------|------|
| i-have-adhd 输出对比示意图 | PNG | 第1名展示 | GitHub README / 自制 |
| archify 导出图示例 | PNG | 第2名展示 | GitHub README |
| DeepSeek Harness 架构示意 | PNG/SVG | 第3名展示 | 官方文档 / README |
| ponytail YAGNI 对比图 | PNG | 第4名展示 | GitHub README |
| skills 目录结构截图 | PNG | 第5名展示 | GitHub 仓库 |
| ECC 工具环 logo | SVG | 第6名快闪 | 各产品 brand kit |
| diagram-design 图表样例 | PNG | 第7名快闪 | README |
| VoiceStudio 界面截图 | PNG | 第8名快闪 | README |
| orca 多 Agent 界面 | PNG | 第9名快闪 | 官网 / README |
| markitdown 转换示意 | PNG | 第10名快闪 | 微软文档 |
| 各项目 avatar | PNG | 卡片头像 | GitHub Avatar API |
| Star 增长曲线 | PNG | 钩子/趋势 | star-history.com |
| BGM音频 | MP3 | 背景音乐 | 免版权音乐库 |
| 音效包 | WAV | 动效音效 | 免版权音效库 |
| AI配音音频 | MP3/WAV | 旁白 | TTS 生成后人工审核 |

---

## ⏱ 时间分配总览

| 部分 | 内容 | 时长 |
|------|------|:---:|
| Scene01 | 开场钩子 | 8秒 |
| Scene02 | 榜单总览 | 10秒 |
| Scene03 | 第1名 i-have-adhd 深度 | 20秒 |
| Scene04 | 第2名 archify | 12秒 |
| Scene05 | 第3名 deepseek-harness | 12秒 |
| Scene06 | 第4名 ponytail | 12秒 |
| Scene07 | 第5名 skills | 14秒 |
| Scene08 | 后5名快闪 | 25秒 |
| Scene09 | 趋势分析 | 20秒 |
| Scene10 | 互动+CTA | 8秒 |
| **合计** | | **约2分21秒** |
