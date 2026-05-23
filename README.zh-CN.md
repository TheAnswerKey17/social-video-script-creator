# Social Video Script Creator Skill

**一个 brief-first 的 Codex Skill，用来把灵感、X 推文、字幕、文章、新闻或参考资料，变成经过调研和审核的中文自媒体视频口播稿。**

[English](./README.md)

---

## 这是什么？

`social-video-script-creator` 是一个面向自媒体创作者的口播脚本创作 skill。它会把每次写稿请求当成一个轻量 creative brief 来处理：在正式写文案之前，先帮助创作者明确选题意图、目标观众、个人观点、素材边界、调研需求和质量标准。

它适合处理：

- 只有一句话的选题灵感
- X 推文或社交媒体讨论
- YouTube 字幕、已有口播稿或访谈稿
- 文章、新闻、教程、产品更新或零散笔记
- 多份需要整合的参考资料

最终目标是产出一篇可用的中文视频口播稿，而不是视频制作包。

## 核心理念

- **先 brief，再写稿**：AI 一开始不是 copywriter，而是 Account / Strategist。
- **给 brief 打分**：输入不完整时不会假装没问题，而是给 readiness score，并说明继续推进会基于哪些假设。
- **先调研，再定结构**：涉及新闻、公开人物 / 公司、外部观点、社媒讨论或强事实 claim 时，要先搜索和查证。
- **先大纲，再脚本**：AI 先给 2-3 个讲法路线，推荐一个，并在正式写稿前暂停确认。
- **口播优先**：稿子要能自然说出口，而不是像报告、新闻稿或通用 AI 小作文。
- **审核是闸门**：最终检查是否 on brief、事实是否有风险、对观众是否有价值、结构是否顺、AI 味是否过重。

## 工作流

```text
Phase 1  接收输入，识别素材边界
Phase 2  生成并评分 content-brief.md
Phase 3  调研并生成 research-pack.md
Phase 4  生成 outline-options.md，确认讲法路线
Phase 5  撰写 script.md
Phase 6  用 content-review.md 做最终审核
```

## 使用时生成的产出

```text
my-script-project/
├── source-material.md       # 可选：保留原始素材
├── content-brief.md         # brief、缺失上下文、评分和假设
├── research-pack.md         # 来源链接、舆论信号、事实/观点/灵感拆分
├── outline-options.md       # 2-3 个讲法路线和推荐方向
├── script.md                # 中文视频口播稿
└── content-review.md        # 最终审核和可用状态
```

这些文件是在用户的脚本项目里生成的产物，不是本 skill 仓库自带的示例文件。

## Reference Map

- [BRIEF.md](./references/BRIEF.md)：输入澄清、brief 模板、评分标准、最低可用 brief
- [RESEARCH.md](./references/RESEARCH.md)：调研对象、来源质量、事实 / 观点 / 灵感分类
- [OUTLINE.md](./references/OUTLINE.md)：大纲选项、讲法类型、推荐逻辑、确认关口
- [SCRIPT.md](./references/SCRIPT.md)：中文口播标准、信息保真、去 AI 味规则
- [REVIEW.md](./references/REVIEW.md)：最终 QA、状态判断、on-brief 检查和修改建议

## 与 Social Video Planner 的关系

本 skill 聚焦 **brief、调研、大纲和口播脚本创作**。

`social-video-planner` 更偏下游的视频前期策划和 HyperFrames 交接。当核心任务是把口播稿写好，用这个 skill；当脚本已经准备好，需要进一步拆成 scene map、素材需求和 HyperFrames handoff 时，再用 `social-video-planner`。

本 skill 不生成视频设计、HyperFrames handoff、动画、音频、HTML/CSS/GSAP 或最终渲染视频。
