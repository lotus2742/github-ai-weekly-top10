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

> "这周 GitHub 周榜有点夸张——一个本地语音 AI 项目，七天涨了 1.5 万颗星；第二名 Agent 记忆项目也破了 1.1 万。整个 AI 开源圈的增速，像是直接按下了快进键。"

**画面动效**：

```
帧0-2秒：
  深色背景（#0d1117，GitHub暗色风格）
  中央大数字 "15,134" 从0滚动到15134（数字滚动动画）
  数字颜色：金色渐变（#FFD700 → #FFA500）
  右上角小字："⭐ stars this week"
  下方小字："VoiceStudio · 本地语音AI"

帧2-4秒：
  数字缩小移到左上
  右下弹入第二数字 "11,694" 快速滚动
  标签："hindsight · Agent记忆"
  两数字之间闪电连接线，表示「双线爆发」

帧4-6秒：
  双数字淡出
  中央打字机文字："增速跳档的一周"
  背景出现轻微「快进」扫描线动效

帧6-8秒：
  文字向上滑出
  底部滑入："GitHub AI 项目 Star 增速 Top 10"
  "第7期 | 2026年第40周"
```

**字幕**：与配音同步，底部居中，白色文字+半透明黑底

**音效**：

- 0秒：低沉的"咚"（吸引注意）
- 2秒：数字滚动时的"滴滴滴"快速音效
- 4秒：闪电连接时的短促"滋"
- 6秒：标题滑入时的"叮"

---

### Scene02：榜单总览（0:08 - 0:18）

**配音**：

> "先看一眼本周 Top 10 全貌。数据来源 star-history.com，统计周期 9 月 27 号到 10 月 3 号。前 10 名本周新增 Star 从 4776 到 15134，第一名大约是第十名的 3.2 倍。语音、记忆、职场 Agent 管理三条线同时冲高。"

**画面动效**：

```
帧8-10秒：
  标题滑入："📊 本周 Top 10 全貌"
  副标题："star-history.com | 9.27 - 10.3"

帧10-15秒：
  柱状图从左到右依次生长（每个柱子0.4秒）
  柱子颜色：渐变色（第1名金色，2-3名橙色，4-5名蓝色，6-10名灰色）
  每个柱子顶部显示项目名+Star数（缩写：VoiceStudio / hindsight / paperclip…）
  第1名柱子明显最高，带发光效果

帧15-17秒：
  柱状图上方弹出标注："3.2x"
  箭头从第10名 ECC 指向第1名 VoiceStudio

帧17-18秒：
  底部三条标签滑入："🎙 本地语音" "🧠 Agent记忆" "💼 职场编排"
  柱状图整体向左移出画面
```

**字幕**：底部，关键数字高亮

**音效**：

- 柱状图生长时每个柱子配一个轻微的"噔"音
- "3.2x"弹出时配"叮"

---

### Scene03：第1名 VoiceStudio 深度解读（0:18 - 0:38）

**配音**：

> "第一名 VoiceStudio，一句话：在你自己电脑上跑一套 ElevenLabs。语音克隆、语音设计、视频配音、听写转写、有声书，一条龙，而且强调全本地、646 种语言。为什么能一周 1.5 万星？我觉得核心是两点：成本和隐私。云端 TTS 按字符计费，做视频、做有声书很容易烧穿预算；同时很多人不想把声音样本和文稿交给第三方。VoiceStudio 用 Python + Tauri 做桌面端，CUDA 和 MLX 走本地推理， AGPL 协议也提醒你要认真看商用边界。总 Star 已经 5 万多，说明不是 Demo，是有人真在拿来干活。"

**画面动效**：

```
帧18-20秒：
  排名徽章 "🥇 #1" 弹入
  项目名 "VoiceStudio" 大字 + GitHub 仓库路径
  右侧 Star 计数器："+15,134 this week"

帧20-24秒：
  功能图标环状排列：克隆 / 配音 / 转写 / 有声书 / 多语言
  中央麦克风图标脉冲发光
  标签 "Local-first" 闪烁

帧24-28秒：
  左右对比卡片：
  左："☁️ 云端 TTS · 按量计费"
  右："💻 本地 VoiceStudio · 数据不出机"
  右卡片放大、左卡片变暗

帧28-32秒：
  技术栈标签云：Python · Tauri · CUDA · MLX · Hugging Face
  底部小字：AGPL-3.0

帧32-36秒：
  总 Star "53,170" 数字滚动
  背景波形动画（模拟语音）

帧36-38秒：
  卡片缩小上移，为下一场景过渡
```

**字幕**：关键词「本地」「1.5万」「隐私」高亮

**音效**：

- 20秒：徽章弹出"叮"
- 24秒：波形低频环境音（很轻）
- 28秒：对比切换"嗖"

---

### Scene04：第2名 hindsight（0:38 - 0:50）

**配音**：

> "第二名 hindsight，定位很直白：Agent Memory That Learns。不是简单把聊天记录塞进向量库，而是强调记忆会学习、会演化。多 Agent、多会话的场景里，没有记忆层，Agent 每次都像失忆。hindsight 一周 1.17 万星，说明大家已经公认——记忆是 Agent 的下半场基础设施。"

**画面动效**：

```
帧38-40秒：
  排名 "🥈 #2" + 项目名 hindsight
  "+11,694 ⭐" 数字强调

帧40-44秒：
  大脑轮廓线框 + 多个会话气泡汇入中央「记忆核心」
  文字："Memory That Learns"

帧44-48秒：
  时间轴动画：Day1 → Day7，记忆节点逐渐变亮、连线变密
  标注："跨会话 · 可演化"

帧48-50秒：
  与 paperclip / orca 图标虚线连接，暗示「编排 + 记忆」
  场景淡出
```

**音效**：

- 40秒：柔和"嗡"声（科技感）
- 46秒：节点点亮"叮叮"

---

### Scene05：第3名 paperclip（0:50 - 1:02）

**配音**：

> "第三名 paperclip， slogan 是 manage agents at work。说白了，就是开源的「上班用 Agent 管理台」。个人玩 Agent 很容易，团队里怎么分工、怎么审计、怎么协作，才是难题。paperclip 一周 9 千多星，总 Star 快 10 万了，说明职场场景的真需求被击中了。"

**画面动效**：

```
帧50-52秒：
  排名 "🥉 #3" + paperclip Logo 占位
  "+9,071 ⭐"

帧52-56秒：
  办公室桌面俯视图（简化插画）
  多个 Agent 头像卡片在工位上，中央 dashboard 连线调度

帧56-60秒：
  弹窗列表：任务分配 / 状态看板 / 团队共享
  英文标语滑入："manage agents at work"

帧60-62秒：
  总 Star 97,203 滚动，接近 100k 进度条快满
  淡出
```

**音效**：

- 52秒：办公室环境轻噪（极低）
- 58秒：通知"叮"

---

### Scene06：第4名 ponytail（1:02 - 1:14）

**配音**：

> "第四名 ponytail，老面孔加速。上期我们讲过它教 AI 像最懒的高级工程师一样写代码，贯彻 YAGNI。这周在全站榜冲到第四，周增 7428，总 Star 破 15 万。开发者厌倦了 Agent 堆抽象、堆配置，开始奖励「少写代码」的哲学。"

**画面动效**：

```
帧62-64秒：
  "#4 ponytail" + "+7,428"
  紫色 YAGNI 徽章弹出

帧64-68秒：
  左右代码行对比：
  左：冗长 Agent 生成代码（红色高亮多余行）
  右：精简实现（绿色勾选）
  中间剪刀动画剪掉冗余

帧68-72秒：
  文字："The best code is the code you never wrote."
  总 Star 154,896 数字滚动

帧72-74秒：
  标签 "↑ 从黑马到 Top4" 闪过
  淡出
```

**音效**：

- 66秒：剪刀"咔嚓"
- 70秒：勾选"叮"

---

### Scene07：第5名 deepseek-harness（1:14 - 1:28）

**配音**：

> "第五名 deepseek-harness，DeepSeek 官方的 Agent Harness，口号 Everything is a Plugin。总 Star 已经 24 万级别，本周还有 6 千多新增。这意味着插件生态——架构图、工具链、第三方 Skill——都会往这个底座上长。落选榜里的 archify 就是 DSH 插件，一周也有 4 千多星。Harness 战争，官方队和社区队都在加速。"

**画面动效**：

```
帧74-76秒：
  "#5 deepseek-harness" + DeepSeek 标识（文字）
  "+6,276 ⭐"

帧76-80秒：
  中央六边形底座 "DSH"
  四周插件模块卡扣式接入动画
  文字："Everything is a Plugin"

帧80-84秒：
  小窗预览 archify 插件卡片 "+4,570" 飞入又飞出（呼应落选）

帧84-88秒：
  总 Star 243,408 强调
  插件轨道旋转一圈后定格
  淡出
```

**音效**：

- 78秒：卡扣"咔哒"
- 82秒：插件飞入"嗖"

---

### Scene08：后5名快闪（1:28 - 1:53）

**配音**：

> "第六到第十名快速过一遍。NVIDIA OpenShell，Agent 安全私有运行时，Rust 写的，单周近 6 千星。Orca，并行 Agent 舰队的 ADE，桌面手机都能调度。mattpocock 的 skills，总 Star 27 万，工程师技能包仍是硬通货。ai-engineering-from-scratch，系统学 Agent 和 LLM 工程。ECC，跨工具的 Harness 元优化层，守住 Top 10 门槛 4776 星。"

**画面动效**：

```
帧88-93秒（#6 OpenShell）：
  卡片 5 秒：NVIDIA 绿边 + 盾牌图标 "Safe Runtime"
  关键词：Rust · 沙箱 · 自主 Agent

帧93-98秒（#7 orca）：
  多窗口网格，每个窗口一个 Agent 头像并行闪烁
  标签：ADE · 舰队编排

帧98-103秒（#8 skills）：
  文件夹树展开 `.agents/skills`
  总 Star 276,195 大字

帧103-108秒（#9 ai-engineering-from-scratch）：
  学习路径阶梯：LLM → Agent → MCP → Ship
  "+4,880" 角标

帧108-113秒（#10 ECC）：
  多工具 Logo 环：Claude Code / Codex / Cursor
  中央 "ECC" 枢纽旋转
  门槛线标注 "+4,776 守门"

帧113-115秒：
  #6-#10 五张卡片扇形叠放后收起
```

**字幕**：每个项目 2–3 个关键词快闪

**音效**：

- 每个项目切换时短促"嗒"一声（共5次）

---

### Scene09：趋势分析（1:53 - 2:13）

**配音**：

> "总结三个趋势。第一，增速跳档——对比上期 Top 1 只有 414 星，这周榜首 1.5 万，整个市场热度完全不一样。第二，语音和记忆接棒 Coding Agent——本地 VoiceStudio 加上 hindsight，一个管「说」，一个管「记得住」。第三，Harness 与运行时军备竞赛——DeepSeek 官方 Harness、NVIDIA OpenShell、ECC 元层，再加上 paperclip 和 orca 的职场编排，Agent 从玩具进厂了。"

**画面动效**：

```
帧113-123秒：趋势一
  左侧大数字 "01"
  标题："增速跳档"
  对比柱：第6期 414 vs 第7期 15134
  箭头向上爆发粒子

帧123-133秒：趋势二
  左侧大数字 "02"
  标题："语音 × 记忆"
  麦克风图标 + 大脑图标握手动画
  文字："说得好 · 记得牢"

帧133-143秒：趋势三
  左侧大数字 "03"
  标题："Harness 军备赛"
  中央擂台：DSH / OpenShell / ECC 三角站位
  背景 paperclip + orca 工厂流水线剪影

帧143-145秒：
  三趋势卡片缩小排列，淡出
```

**音效**：

- 每个趋势数字弹出时配"咚"
- 趋势二握手时配"叮"
- 趋势三擂台出现时低频鼓点

---

### Scene10：互动+CTA（2:13 - 2:21）

**配音**：

> "完整榜单和所有 GitHub 链接我放在评论区置顶了。这周 10 个项目你最想试哪个？评论区聊聊。每周一更新 GitHub AI 项目周报，关注不迷路，我们下期见。"

**画面动效**：

```
帧213-215秒：
  深色背景
  中央弹出："完整榜单 ⬇️"
  下方箭头指向"评论区"图标

帧215-217秒：
  文字变为："你用过几个？"
  下方出现数字 1-10 的按钮动画（模拟评论选择）

帧217-219秒：
  文字变为："每周一更新"
  下方弹出关注按钮动画 + 铃铛图标

帧219-221秒：
  最终画面：
  "GitHub AI 项目 Star 增速 Top 10"
  "第7期 | 2026年第40周"
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
| **6-10名强调色** | 各不相同（NV绿/青/紫/橙/粉） |
| **YAGNI标签色** | #A371F7（紫色） |
| **安全/运行时色** | #76B900（NVIDIA绿） |
| **记忆主题色** | #79c0ff（浅蓝） |
| **字体** | 标题用粗体无衬线（如 Inter Bold），正文用常规 |
| **圆角** | 12px（卡片）/ 8px（标签） |
| **阴影** | 卡片用 0 4px 20px rgba(0,0,0,0.3) |

---

## 🔊 音频设计规范

| 类型 | 说明 |
|------|------|
| **BGM** | 科技感电子乐，85-100 BPM，不抢配音 |
| **配音** | AI TTS，语速适中（约3字/秒），前半兴奋、趋势段略沉稳 |
| **音效库** | 数字滚动、弹出、滑动、卡扣、波形环境音 |
| **混音** | 配音 > BGM > 音效，配音清晰度优先 |

---

## 📦 Remotion 组件拆分建议

```
components/
├── layouts/
│   ├── DarkBackground.tsx
│   ├── SubtitleBar.tsx
│   └── SceneTransition.tsx
├── ranking/
│   ├── RankingCard.tsx
│   ├── BarChart.tsx
│   ├── MultiplierBadge.tsx      // 3.2x 等倍数标注
│   └── RankingList.tsx
├── project/
│   ├── ProjectHero.tsx
│   ├── WaveformVisualizer.tsx   // VoiceStudio 波形
│   ├── MemoryGraph.tsx          // hindsight 记忆图
│   ├── OfficeDashboard.tsx      // paperclip 职场视图
│   ├── YAGNIComparison.tsx
│   ├── PluginHub.tsx            // DSH 插件底座
│   ├── AgentFleetGrid.tsx       // orca 并行窗口
│   └── HarnessRing.tsx          // ECC 多工具环
├── trend/
│   ├── TrendCard.tsx
│   ├── WeekCompareBars.tsx      // 第6期 vs 第7期对比
│   └── ArenaDiagram.tsx         // Harness 军备赛
├── numbers/
│   ├── CountUp.tsx
│   └── StarCounter.tsx
└── outro/
    ├── CTAButton.tsx
    └── EndCard.tsx
```

---

## 📋 素材准备清单

| 素材 | 格式 | 用途 | 来源 |
|------|------|------|------|
| VoiceStudio 界面/功能示意图 | PNG | 第1名展示 | GitHub README |
| hindsight 架构/记忆示意图 | PNG | 第2名展示 | GitHub README |
| paperclip 产品截图 | PNG | 第3名展示 | GitHub README |
| ponytail YAGNI 对比图 | PNG | 第4名展示 | GitHub README |
| deepseek-harness 插件示意图 | PNG | 第5名展示 | GitHub README |
| OpenShell / orca Logo | SVG/PNG | 快闪场景 | GitHub Avatar API |
| skills 目录结构截图 | PNG | 第8名快闪 | GitHub README |
| 各项目 avatar | SVG | 排名卡片 | GitHub Avatar API |
| 第6期 vs 第7期增速对比图 | PNG | 趋势分析 | 自制 |
| BGM音频 | MP3 | 背景音乐 | 免版权音乐库 |
| 音效包 | WAV | 动效音效 | 免版权音效库 |
| AI配音音频 | MP3/WAV | 旁白 | TTS 生成后人工审核 |

---

## ⏱ 时间分配总览

| 部分 | 内容 | 时长 |
|------|------|:---:|
| Scene01 | 开场钩子 | 8秒 |
| Scene02 | 榜单总览 | 10秒 |
| Scene03 | 第1名 VoiceStudio 深度 | 20秒 |
| Scene04 | 第2名 hindsight | 12秒 |
| Scene05 | 第3名 paperclip | 12秒 |
| Scene06 | 第4名 ponytail | 12秒 |
| Scene07 | 第5名 deepseek-harness | 14秒 |
| Scene08 | 后5名快闪 | 25秒 |
| Scene09 | 趋势分析 | 20秒 |
| Scene10 | 互动+CTA | 8秒 |
| **合计** | | **约2分21秒** |
