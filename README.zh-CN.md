# Social Video Script Creator Skill

**一个 brief-first 的 Codex Skill，用来把灵感、X 推文、字幕、文章、新闻或参考资料，变成经过调研和审核的中文自媒体视频口播稿。**

[English](./README.md)

---

## 这是什么？

`social-video-script-creator` 是一个面向中文自媒体创作者的口播脚本创作 skill。它会把每次写稿请求当成一个轻量 creative brief 来处理：在正式写文案之前，先把原始素材落成本地素材中心，再帮助创作者明确选题意图、目标观众、个人观点、素材边界、调研需求和质量标准。

它适合处理：

- 只有一句话的选题灵感
- X 推文或社交媒体讨论
- YouTube 字幕、已有口播稿或访谈稿
- 文章、新闻、教程、产品更新或零散笔记
- 多份需要整合的参考资料

最终目标是产出一篇可用的中文视频口播逐字稿，而不是视频制作包。所有项目产物默认中文优先。

## 核心理念

- **先素材入库，再 brief**：创建 brief 前必须先创建 `source-material.md`，保存原始输入、链接、可读取正文或获取失败说明。
- **brief 是主文档**：`content-brief.md` 会持续累积素材摘要、用户补充、调研洞察、最终大纲和 next step。
- **强制断点**：每个阶段结束后必须停下让用户确认，即使 brief 得分很高，也不能自动跳过确认。
- **给 brief 打分**：输入不完整时不会假装没问题，而是给 readiness score，并说明继续推进会基于哪些假设。
- **先调研，再定结构**：涉及新闻、公开人物 / 公司、外部观点、社媒讨论或强事实 claim 时，要先搜索和查证。
- **先大纲，再脚本**：AI 先给 2-3 个讲法路线，推荐一个；用户确认后，还要把最终大纲写回 brief，再停下确认写稿。
- **口播优先**：稿子要能自然说出口，而不是像报告、新闻稿或通用 AI 小作文。
- **审核是闸门**：最终检查是否 on brief、事实是否有风险、对观众是否有价值、结构是否顺、AI 味是否过重。

## 工作流

```text
Phase 1  创建 source-material.md，保存素材中心，然后进入 brief
Phase 2  生成并评分 content-brief.md，停下让用户确认
Phase 3  调研并生成 research-pack.md，把核心发现回写到 content-brief.md，然后停下
Phase 4  生成 outline-options.md，停下让用户选择讲法路线
Phase 5  把最终大纲写回 content-brief.md，再停下确认是否写稿
Phase 6  撰写 script.md，停下确认是否审核
Phase 7  用 content-review.md 做最终审核
```

## 使用时生成的产出

```text
my-script-project/
├── source-material.md       # 必须：本地素材中心
├── content-brief.md         # 累积式主 brief、评分、next step
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
