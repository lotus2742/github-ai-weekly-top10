# GitHub AI 周榜 — 每周一定时任务指令

> 本文件供 Cursor Automation 参考。格式样例见 `GitHub_AI项目增速Top10/第3期_*.md`。

## 期数规则

- 扫描 `/Users/yanqing/Documents/github周榜/GitHub_AI项目增速Top10/` 目录中已有 `第X期_*.md` 文件，取最大期数 +1 作为当本期数
- 第3期已生成，若目录中无更高期数，则从第4期开始
- 周次编号：根据 star-history.com 页面标注的统计周期，计算对应的 ISO 年+周（与第3期写法一致）

## 任务1：生成 GitHub AI 项目 Star 增速 Top 10 周榜报告

1. 访问 star-history.com Weekly 排行榜，获取本周数据（统计周期以页面标注的 "Updated MM DD, YYYY – MM DD, YYYY" 为准，不要自行推算）
2. 获取排行榜前20名项目的完整 GitHub 仓库路径（通过点击链接获取 URL 中的 owner/repo）
3. 通过 GitHub API (`api.github.com/repos/owner/repo`) 获取每个项目的：full_name、description、stargazers_count、language、license.spdx_id、topics
4. 筛选与 AI 强相关的项目，按本周新增 Star 数从高到低排序，取 Top 10
5. 生成 Markdown 报告，保存到 `/Users/yanqing/Documents/github周榜/GitHub_AI项目增速Top10/`，文件名：`第X期_YYYY年第YY周.md`

### 报告格式（与第3期一致）

- 标题、统计周期、数据来源、筛选条件、排名依据
- 榜单总览表格（排名、项目、本周新增、总 Star、语言、许可证、简介）
- Top 10 项目详情（每个含仓库链接、描述、上榜理由）
- 趋势观察（3–5 条）
- 落选项目列表（star-history 第 11–20 名中的 AI 相关项目，剔除非 AI）
- 报告生成时间与声明

报告生成后，将**完整报告内容**输出到对话框。

## 任务2：生成 Remotion 视频分镜脚本

基于当期周榜数据，生成完整 Remotion 分镜脚本，保存到同目录，文件名：`第X期_Remotion分镜脚本.md`

### 脚本格式（与第3期脚本一致）

- 总时长约 2 分 30 秒
- 10 个 Scene：开场钩子(8s) → 榜单总览(10s) → Top1深度(20s) → Top2(12s) → Top3(12s) → Top4(12s) → Top5(14s) → 后5名快闪(25s) → 趋势分析(20s) → 互动CTA(8s)
- 每个 Scene：配音文案、画面动效（每 2 秒帧级描述）、字幕说明、音效说明
- 视觉设计规范、音频设计规范、Remotion 组件拆分建议、素材准备清单、时间分配总览表

脚本生成后，将**完整脚本内容**输出到对话框。

## 重要规则

- 不得使用第三方博客、CSDN、自媒体文章作为数据来源
- 数据来源仅限：star-history.com（主）+ GitHub API（辅）
- 所有输出使用中文
- 两份文件均保存到 `/Users/yanqing/Documents/github周榜/GitHub_AI项目增速Top10/`
