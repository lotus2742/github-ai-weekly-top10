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

> "这周 GitHub 周榜几乎被 AI 刷屏了——Google 刚开源的 Agent 编排项目 ax，一周接近一万颗星；DeepSeek 官方 Harness 和 Cloudflare 安全 Skill 也集体冲进前五档。Agent 基础设施大战，正式开打。"

**画面动效**：

```
帧0-2秒：
  深色背景（#0d1117，GitHub暗色风格）
  中央大数字 "9,995" 从0滚动到9995（数字滚动动画）
  数字颜色：金色渐变（#FFD700 → #FFA500）
  右上角小字："⭐ stars this week"
  下方小字："google/ax · Google 下场"

帧2-4秒：
  数字缩小移到左侧
  右侧滑入三张卡片纵向排列：
    "DeepSeek Harness +6,962"
    "Cloudflare Skill +5,232"
    "hindsight 记忆 +9,863"
  卡片带轻微脉冲发光

帧4-6秒：
  卡片淡出
  中央弹出问题文字："Agent 基础设施大战？"
  文字带打字机效果

帧6-8秒：
  文字向上滑出
  底部滑入："GitHub AI 项目 Star 增速 Top 10"
  "第7期 | 2026年第39周"
```

**字幕**：与配音同步，底部居中，白色文字+半透明黑底

**音效**：

- 0秒：低沉的"咚"（吸引注意）
- 2秒：数字滚动时的"滴滴滴"快速音效
- 6秒：文字弹出时的"叮"

---

### Scene02：榜单总览（0:08 - 0:18）

**配音**：

> "先看本周 Top 10 全貌。数据来源 star-history.com，统计周期 9 月 20 号到 9 月 26 号。前 10 名本周新增从四千五到接近一万，第一名和第十名差距大约两倍。说明头部项目仍在加速吸星，但门槛已经抬到四千星以上。"

**画面动效**：

```
帧8-10秒：
  标题滑入："📊 本周 Top 10 全貌"
  副标题："star-history.com | 9.20 - 9.26"

帧10-15秒：
  柱状图从左到右依次生长（每个柱子0.4秒）
  柱子颜色：渐变色（第1名金色，2-3名橙色，4-5名蓝色，6-10名灰色）
  每个柱子顶部显示项目名+Star数
  第1名柱子明显最高，带发光效果

帧15-17秒：
  柱状图上方弹出标注："≈2.2x"
  箭头从第10名指向第1名，标注"第1名 ≈ 第10名的2倍多"

帧17-18秒：
  柱状图整体向左移出画面
```

**字幕**：底部，关键数字高亮

**音效**：

- 柱状图生长时每个柱子配一个轻微的"噔"音
- "≈2.2x"弹出时配"叮"

---

### Scene03：第1名 Google ax 深度解读（0:18 - 0:38）

**配音**：

> "第一名，Google 的 ax。全称是 Agentic Orchestration Runtime，说白了就是——官方出品的 Agent 编排运行时。不是再做一个聊天机器人，而是帮你把多个 Agent、多步任务串起来，能观测、能调度、能工程化落地。为什么一周能涨将近一万星？我觉得两点：一是 Google 品牌背书，二是大家等了很久的「编排层」终于有开源标杆。总星才一万二，但增速说明它正处在爆发早期，值得盯紧后续文档和示例。"

**画面动效**：

```
帧18-20秒：
  大标题从底部弹入："🥇 第1名"
  项目名 "Google ax" 带发光效果
  右侧大数字 "+9,995⭐" 金色脉冲动画
  下方小字："google/ax · Go · Apache-2.0"

帧20-24秒：
  标题上移到顶部
  中央展示编排流程动画（左→右）：
  "任务输入" → "Agent A" → "Agent B" → "合并输出"
  节点之间粒子流动，表示 orchestration
  底部标签："Agentic Orchestration Runtime"

帧24-28秒：
  流程图淡出
  中央对比：
    左侧："单轮 Chat"（灰色，打叉）
    右侧："多 Agent 编排"（金色，打勾）
  Google logo 小图标出现在右上角

帧28-32秒：
  对比淡出
  中央大字弹出："编排层"
  下方文字逐行出现：
  "多步任务串联"
  "可观测、可调度"
  "工程化落地"

帧32-36秒：
  文字淡出
  Star 增长曲线图从左到右陡峭上升
  曲线末端标注："总星 12,168 · 早期爆发"
  曲线下方填充金色渐变

帧36-38秒：
  曲线图淡出，过渡到下一场景
```

**字幕**：底部，关键词高亮（"编排""Google""近一万"）

**音效**：

- 节点流动时配轻柔"嗖"声
- "编排层"大字弹出时配重音"咚"
- Star曲线绘制时配计数器声

---

### Scene04：第2名 Hindsight（0:38 - 0:50）

**配音**：

> "第二名，Hindsight，本周加星九千八百多，几乎和 ax 并列。它解决的是 Agent 最头疼的事——记性差。普通 Agent 聊完就忘，Hindsight 做可学习的记忆层，能积累、检索、更新长期知识。标签里直接写 Agent Memory That Learns。总星三万七，Python 技术栈，MIT 协议。记忆加上编排，才是能上岗的 Agent。"

**画面动效**：

```
帧38-40秒：
  标题弹入："🥈 第2名"
  "Hindsight" + vectorize-io 小图标
  "+9,863⭐" 银色

帧40-44秒：
  中央大脑+数据库图标动画：
  对话气泡进入 → 写入记忆库 → 下次对话时检索亮起
  循环播放一次

帧44-47秒：
  动画缩小
  关键词标签弹出："agentic-ai" "ai-memory" "agents"
  每个标签0.3秒淡入

帧47-50秒：
  底部弹出："总星 37,320 | MIT | Python"
  过渡到下一场景
```

**音效**：

- 记忆写入时配"叮"
- 检索亮起时配"嗖"

---

### Scene05：第3名 DeepSeek Harness（0:50 - 1:02）

**配音**：

> "第三名，DeepSeek 官方 Harness，加星六千九百多，总星已经二十三万七。口号是 Everything is a Plugin——一切皆插件。TypeScript 写的底座，把 Cordis、DSH 这些能力模块化，让开发者像装扩展一样装 Agent 能力。本周 archify 画图 Skill 也涨了四千七，说明插件生态开始转起来。"

**画面动效**：

```
帧50-52秒：
  标题弹入："🥉 第3名"
  "DeepSeek Harness" + DeepSeek logo
  "+6,962⭐" 铜色

帧52-58秒：
  中央插件总线动画：
  核心方块 "Harness" 居中
  四周插件卡片飞入并吸附：archify / skills / tools ...
  卡片标注 "dsh-plugin"

帧58-60秒：
  插件图缩小
  底部大字："Everything is a Plugin"

帧60-62秒：
  底部弹出："总星 237,710 | MIT"
  过渡
```

**音效**：

- 插件吸附时配"咔嗒"声
- 口号弹出时配"叮"

---

### Scene06：第4名 Paperclip（1:02 - 1:14）

**配音**：

> "第四名，Paperclip，加星六千九百一十八。定位很直白——大家在公司里管理 Agent 用的开源 App。不是个人玩具，而是团队看板、任务分派、多 Agent 协作。TypeScript，总星快九万。说明 Agent 正在从「极客玩具」变成「上班工具」。"

**画面动效**：

```
帧102-104秒：
  标题弹入："④ 第4名"
  "Paperclip" + "+6,918⭐" 蓝色

帧104-108秒：
  中央办公场景 mock UI：
  左侧成员列表，中间 Agent 任务列，右侧状态灯
  任务卡片从「待办」拖到「进行中」动画

帧108-112秒：
  UI 上方弹出标签："团队级" "多 Agent" "上班用"

帧112-114秒：
  底部："总星 89,904 | MIT"
  过渡
```

**音效**：

- 拖拽任务时配轻微摩擦音
- 标签弹出时配"pop"

---

### Scene07：第5名 Orca（1:14 - 1:28）

**配音**：

> "第五名，Orca，加星六千三百多。它是并行 Agent 舰队的 ADE——Agent Development Environment。桌面、手机、远程运行时都能用，还能并行跑 Claude Code、Codex、Cursor Agent、OpenCode。支持 worktree 和终端工作流。总星七万九。和 Paperclip 一个管人一个管并行，正好凑成「团队+舰队」。"

**画面动效**：

```
帧114-116秒：
  标题弹入："⑤ 第5名"
  "Orca" + "+6,328⭐" 蓝色

帧116-122秒：
  中央舰队动画：5 个终端窗口同时跑 Agent
  每个窗口顶部不同 logo（Claude/Codex/Cursor…）
  进度条同步推进

帧122-126秒：
  舰队缩小
  设备图标行：桌面 / 手机 / 远程云
  标注 "parallel-agents"

帧126-128秒：
  底部："总星 79,612 | MIT | ADE"
  过渡
```

**音效**：

- 多窗口亮起时配节奏加快的"噔噔噔"
- 设备图标淡入时配"叮"

---

### Scene08：后5名快闪（1:28 - 1:53）

**配音**：

> "后五名快速过一遍。第六 univer，给 Agent 用的 Office 运行时，表格文档幻灯片 PDF 一体。第七 ECC，二十六万总星的编码 Agent 元优化。第八 Cloudflare 安全审计 Skill，企业级安全也能装进 Agent。第九 archify，Harness 生态里的架构图 Skill。第十 mattpocock skills，二十七万星的工程师向 Claude Code 技能库。"

**画面动效**：

```
每个项目5秒，统一模板：

帧128-133秒：⑥ univer
  左侧大编号 "⑥" 弹入
  项目名 "univer" + "+5,315⭐"
  右侧闪过 Sheet/Doc/Slide/PDF 四图标旋转
  关键词标签："Office Harness" "Agent 文档" "Apache-2.0"
  → 滑出

帧133-138秒：⑦ ECC
  左侧大编号 "⑦" 弹入
  项目名 "ECC" + "+5,262⭐"
  右侧闪过技能/记忆/安全三图标
  关键词标签："268k⭐" "跨工具" "Harness 优化"
  → 滑出

帧138-143秒：⑧ security-audit-skill
  左侧大编号 "⑧" 弹入
  项目名 "Cloudflare Skill" + "+5,232⭐"
  右侧安全扫描雷达动画
  关键词标签："多阶段审计" "机器可读" "Cloudflare"
  → 滑出

帧143-148秒：⑨ archify
  左侧大编号 "⑨" 弹入
  项目名 "archify" + "+4,769⭐"
  右侧架构图 HTML 预览缩放
  关键词标签："dsh-plugin" "动效图" "可验证"
  → 滑出

帧148-153秒：⑩ mattpocock/skills
  左侧大编号 "⑩" 弹入
  项目名 "skills" + "+4,554⭐"
  右侧 .agents 目录树展开动画
  关键词标签："Real Engineers" "270k⭐" "Claude Code"
  → 滑出
```

**画面风格**：

- 每个项目用**不同的主题色**（⑥青 ⑦橙 ⑧红 ⑨紫 ⑩绿）
- 背景统一深色，项目色作为强调色
- 切换时用**横向滑动**过渡，节奏感强

**音效**：

- 每个项目切入时配"噔"音
- 背景BGM节奏加快

---

### Scene09：趋势分析（1:53 - 2:13）

**配音**：

> "看完这 10 个项目，三个趋势很清楚。第一，大厂和官方一起做基础设施——Google ax、DeepSeek Harness、Cloudflare Skill，增速全是五千到一万档。第二，记忆、并行、管理铁三角——Hindsight、Orca、Paperclip 把 Agent 往生产环境推。第三，插件生态飞轮——Harness 加 archify 这类 Skill，平台越厚，开发者越愿意来。"

**画面动效**：

```
帧153-155秒：
  标题弹入："📈 本周三大趋势"
  背景变为深蓝色渐变

帧155-163秒：趋势一
  左侧大数字 "01" 弹入
  标题："官方基础设施集体爆发"
  中央：Google / DeepSeek / Cloudflare logo 三角排列
  每个 logo 下方周增数字滚动
  右侧统计："5k–10k 档"

帧163-173秒：趋势二
  左侧大数字 "02" 弹入
  标题："记忆 · 并行 · 管理"
  中央：三图标连线三角形
    Hindsight（记忆） / Orca（并行） / Paperclip（管理）
  连线粒子流动

帧173-183秒：趋势三
  左侧大数字 "03" 弹入
  标题："Harness 插件飞轮"
  中央：Harness 核心 + 插件环旋转
  archify 等插件名环绕亮起
  底部文字："Everything is a Plugin"

帧183-185秒：
  三个趋势缩小排列，整体淡出
```

**音效**：

- 每个趋势数字弹出时配"咚"
- 飞轮旋转时配轻柔机械声
- 插件名亮起时配"叮叮叮"

---

### Scene10：互动+CTA（2:13 - 2:21）

**配音**：

> "完整榜单和所有 GitHub 链接我放在评论区置顶了。Google ax 和 DeepSeek Harness 你更想试哪个？评论区聊聊。每周一更新 GitHub AI 项目周报，关注不迷路，我们下期见。"

**画面动效**：

```
帧213-215秒：
  深色背景
  中央弹出："完整榜单 ⬇️"
  下方箭头指向"评论区"图标

帧215-217秒：
  文字变为："ax 还是 Harness？"
  下方两个按钮动画左右摇摆

帧217-219秒：
  文字变为："每周一更新"
  下方弹出关注按钮动画 + 铃铛图标

帧219-221秒：
  最终画面：
  "GitHub AI 项目 Star 增速 Top 10"
  "第7期 | 2026年第39周"
  底部小字："数据来源：star-history.com"
  画面静止2秒后淡出
```

**音效**：

- 215秒：轻柔的"叮"
- 219秒：结束音效（短促的"叮咚"）

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
| **6-10名强调色** | 青 / 橙 / 红 / 紫 / 绿 |
| **Google 品牌点缀** | #4285F4 |
| **DeepSeek 点缀** | #4D6BFE |
| **Cloudflare 点缀** | #F38020 |
| **字体** | 标题用粗体无衬线（如 Inter Bold），正文用常规 |
| **圆角** | 12px（卡片）/ 8px（标签） |
| **阴影** | 卡片用 0 4px 20px rgba(0,0,0,0.3) |

---

## 🔊 音频设计规范

| 类型 | 说明 |
|------|------|
| **BGM** | 科技感电子乐，80-100 BPM，不抢配音 |
| **配音** | AI TTS，语速适中（约3字/秒），语气带点兴奋 |
| **音效库** | 数字滚动、弹出、滑动、切换、插件吸附各有对应音效 |
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
│   └── RankingList.tsx           // 排名列表
├── project/
│   ├── ProjectHero.tsx           // 项目展示头部（名次+名称+Star）
│   ├── OrchestrationFlow.tsx     // Agent 编排流程（ax）
│   ├── MemoryLoop.tsx            // 记忆写入/检索（hindsight）
│   ├── PluginBus.tsx             // Harness 插件总线
│   ├── TeamBoard.tsx             // Paperclip 团队看板
│   ├── AgentFleet.tsx            // Orca 并行舰队
│   ├── OfficeIcons.tsx           // univer 办公图标组
│   ├── SecurityRadar.tsx         // 安全扫描雷达
│   └── TagCloud.tsx              // 关键词标签
├── trend/
│   ├── TrendCard.tsx             // 趋势卡片
│   ├── TriangleDiagram.tsx       // 铁三角连线图
│   └── PluginFlywheel.tsx        // 插件飞轮
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
| Google ax README 架构图 | PNG | 第1名展示 | GitHub README |
| Hindsight 记忆示意图 | PNG | 第2名展示 | GitHub README |
| DeepSeek Harness 插件示意 | PNG | 第3名展示 | GitHub README |
| Paperclip 产品截图 | PNG | 第4名展示 | GitHub README |
| Orca 并行终端截图 | PNG | 第5名展示 | GitHub README |
| univer Office 界面 | PNG | 第6名快闪 | GitHub README |
| archify 动效图导出 | MP4/GIF | 第9名快闪 | 项目 demo |
| 各项目 logo/icon | SVG/PNG | 排名卡片 | GitHub Avatar API |
| Google / DeepSeek / Cloudflare logo | SVG | 趋势分析 | 官方 brand kit |
| Star 增长曲线 | PNG | 各项目 | star-history.com 截图 |
| BGM 音频 | MP3 | 背景音乐 | 免版权音乐库 |
| 音效包 | WAV | 动效音效 | 免版权音效库 |
| AI 配音音频 | MP3/WAV | 旁白 | TTS 生成后人工审核 |

---

## ⏱ 时间分配总览

| 部分 | 内容 | 时长 |
|------|------|:---:|
| Scene01 | 开场钩子 | 8秒 |
| Scene02 | 榜单总览 | 10秒 |
| Scene03 | 第1名 Google ax 深度 | 20秒 |
| Scene04 | 第2名 Hindsight | 12秒 |
| Scene05 | 第3名 DeepSeek Harness | 12秒 |
| Scene06 | 第4名 Paperclip | 12秒 |
| Scene07 | 第5名 Orca | 14秒 |
| Scene08 | 后5名快闪 | 25秒 |
| Scene09 | 趋势分析 | 20秒 |
| Scene10 | 互动+CTA | 8秒 |
| **合计** | | **约2分21秒** |
