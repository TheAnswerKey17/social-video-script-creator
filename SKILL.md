---
name: social-video-script-creator
description: >
  将一句选题灵感、X 推文、YouTube 字幕、文章、新闻、教程、粗略笔记或参考资料，
  通过 brief-first 工作流转化为中文自媒体视频口播逐字稿。使用时 AI 必须先像
  Account/Strategist 一样整理素材中心、生成并评分 content-brief.md、在每个关键节点
  停下向用户确认，再进行调研、大纲、逐字稿和审核。本 skill 以 content-brief.md 为
  核心累积文档，所有项目产物默认使用中文；不负责视频设计、HyperFrames handoff、
  动画、音频、HTML/CSS/GSAP 或最终视频渲染。
---

# Social Video Script Creator

这是一个 **以 brief 为核心的中文自媒体视频口播稿创作 skill**。它不是一上来写文案，而是先把用户输入的灵感、链接、字幕、文章或资料整理成可追踪的素材中心，再逐步补充 brief、调研、大纲、脚本和审核。

默认模式：**文件 + 对话确认**。每个阶段都要写入 Markdown 文件，并在强制断点停下，等待用户确认后才能进入下一阶段。

## 最高规则

- **所有项目产物默认用中文写**：`source-material.md`、`content-brief.md`、`research-pack.md`、`outline-options.md`、`script.md`、`content-review.md` 都必须以中文为主。
- **`content-brief.md` 是主文档**：它不是一次性文件，而是从素材、用户补充、调研、最终大纲到下一步状态持续累积更新。
- **不能一次性跑完整流程**：除非用户在每个断点之后明确回复继续，否则不得直接从 brief 跳到 research、outline、script 或 review。
- **任何评分都不能绕过确认**：即使 brief 得分是 90 分，也必须停下让用户确认 brief 内容和缺失信息。
- **不得只把链接放进 brief**：原文、摘录、字幕、用户原始输入、可读取的网页正文或获取失败说明，必须先写入 `source-material.md`。
- **最终目标是中文口播逐字稿**：不要输出视频设计、视觉方案、HyperFrames handoff、动画或渲染内容。

## 标准产物

```text
source-material.md    # 素材中心：用户原始输入、原文/摘录/字幕、链接、本地索引、获取限制
content-brief.md      # 主 brief：持续累积素材摘要、目标、问题、调研洞察、最终大纲、next step
research-pack.md      # 调研包：来源、原文摘录、观点、评论、金句、结构灵感、事实状态
outline-options.md    # 大纲选项：2-3 个讲法路线、推荐路线、需要用户确认的问题
script.md             # 中文口播逐字稿
content-review.md     # 最终审核：on brief、事实风险、口播自然度、AI 味、可用状态
```

## 强制断点协议

每个阶段结束时都必须停止，不能继续执行下一阶段。

| 阶段 | 必须完成 | 停下时必须问 |
|---|---|---|
| 1. 素材入库 | 创建/更新 `source-material.md`，保存原始输入和可获取素材 | 是否认可素材边界？是否还有补充资料？ |
| 2. 初版 brief | 创建/更新 `content-brief.md`，包含评分、缺失问题和 `Next Step` | brief 架构是否准确？请回答哪些缺失问题？ |
| 3. 调研 | 创建/更新 `research-pack.md`，并把核心发现写回 `content-brief.md` | 是否认可调研结论？是否继续进入大纲？ |
| 4. 大纲选项 | 创建/更新 `outline-options.md`，给 2-3 个方向和推荐 | 选哪个方向？要改 hook、观点、结构或语气吗？ |
| 5. 最终大纲入 brief | 用户确认方向后，把最终大纲写回 `content-brief.md`，`Next Step` 改为写逐字稿 | 是否按此 brief 开始写逐字稿？ |
| 6. 逐字稿 | 创建 `script.md` | 是否进入最终审核？ |
| 7. 审核 | 创建 `content-review.md` | 给出状态和下一步修改建议 |

如果用户要求“继续”，只代表进入**下一阶段**，不代表授权连续完成后面所有阶段。

## 工作流

### Phase 1 - 素材入库

先阅读 [`references/BRIEF.md`](references/BRIEF.md) 的素材中心规则。

必须先创建或更新 `source-material.md`：

- 保留用户原始输入。
- 记录所有原始链接。
- 如果能读取全文、字幕、文章正文或关键摘录，写入本地文件。
- 如果不能读取，写明失败原因、可替代来源和当前只能使用的内容。
- 为每个素材分配本地编号，供 brief 引用。

素材入库后，可以创建初版 `content-brief.md`，但完成 brief 后必须停下。

### Phase 2 - 初版 Brief

先阅读 [`references/BRIEF.md`](references/BRIEF.md)。

`content-brief.md` 必须包含：

- 素材摘要与本地素材链接。
- 用户目标、期许、个人观点、目标受众、平台、内容目标。
- 关键洞察、核心冲突、可能角度。
- 缺失信息问题。
- 100 分 readiness score。
- `Next Step`：明确用户需要回答什么，或下一步是否进入调研。

无论分数多高，都必须停下给用户确认。

### Phase 3 - 调研并回写 Brief

先阅读 [`references/RESEARCH.md`](references/RESEARCH.md)。

调研结束必须：

- 创建/更新 `research-pack.md`。
- 把核心调研结论、可用亮点、争议、事实风险、可借鉴结构写回 `content-brief.md`。
- 如果发现原 brief 方向有问题，更新 brief 中的洞察和风险。
- 将 `content-brief.md` 的 `Next Step` 改为“确认调研结论，进入大纲选项”。

然后停下等待用户确认。

### Phase 4 - 大纲选项

先阅读 [`references/OUTLINE.md`](references/OUTLINE.md)。

创建/更新 `outline-options.md`，给出 2-3 个中文讲法路线，并明确推荐一个。

完成后必须停下，让用户选择路线或修改方向。不能直接写 `script.md`。

### Phase 5 - 最终大纲写回 Brief

用户确认路线后：

- 把最终路线、hook、核心洞察、段落结构、关键例子、结尾动作写回 `content-brief.md`。
- 将 `content-brief.md` 的 `Next Step` 改为“按最终 brief 撰写中文口播逐字稿”。

然后再次停下，等待用户确认开始写稿。

### Phase 6 - 写中文口播逐字稿

先阅读 [`references/SCRIPT.md`](references/SCRIPT.md)。

创建 `script.md`：

- 必须是中文逐字稿。
- 必须能自然说出口。
- 必须遵守已确认的 `content-brief.md`。
- 未确认事实要保留风险提示，不得写成确定事实。

写完停下，询问是否进入最终审核。

### Phase 7 - 最终审核

先阅读 [`references/REVIEW.md`](references/REVIEW.md)。

创建 `content-review.md`，给出：

- brief 对齐度。
- 来源和事实风险。
- 观众价值。
- 结构和口播自然度。
- AI 味检查。
- 状态：`ready`、`usable-for-draft-only` 或 `blocked`。

## 协作规则

- 问题必须具体，围绕会改变内容方向的决策，不问泛泛的“你觉得怎么样”。
- 每次对话只推进一个阶段。
- 继续下一阶段前，必须先确认上一阶段的文件已经更新。
- 用户可以要求修改任意阶段文件；修改后仍然回到当前断点。
- 如果用户明确要求跳过某个断点，仍要在回复中提醒这会降低质量，并在 `content-brief.md` 记录为假设或用户覆盖。
