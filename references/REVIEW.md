# 审核

`content-review.md` 是最终质量闸门，用来判断逐字稿是否可以继续使用、只能作为草稿，还是必须返工。

所有内容默认使用中文。

## 审核输入

审核必须对照：

- `source-material.md`
- `content-brief.md`
- `research-pack.md`，如果存在
- `outline-options.md`
- `script.md`
- 用户在各断点的确认和修改意见

## `content-review.md` 模板

```markdown
# 内容审核

## 结论

- 状态：ready / usable-for-draft-only / blocked
- 主要原因：
- 最小修改项：

## Brief 对齐

| brief 元素 | 状态 | 说明 |
|---|---|---|
| 目标受众 | pass / warn / fail |  |
| 用户 POV | pass / warn / fail |  |
| 内容目标 | pass / warn / fail |  |
| 核心冲突 / 洞察 | pass / warn / fail |  |
| 平台 / 时长 | pass / warn / fail |  |
| 语气 / 红线 | pass / warn / fail |  |

## 来源与事实

| claim / 来源需求 | 状态 | 说明 |
|---|---|---|
| <claim> | confirmed / needs-source / opinion / risky | <说明> |

## 观众价值

- 观众收益是否清楚：pass / warn / fail
- 是否有实用价值：pass / warn / fail
- 是否区别于普通摘要：pass / warn / fail
- 最强的一段：
- 最弱或最泛的一段：

## 结构与口播

- Hook：pass / warn / fail
- 推进：pass / warn / fail
- 例子：pass / warn / fail
- 结尾：pass / warn / fail
- 口播自然度：pass / warn / fail

## AI 味检查

- 假共情：pass / warn / fail
- 假深刻：pass / warn / fail
- 自我加权：pass / warn / fail
- 模板化表达：pass / warn / fail
- 空排比：pass / warn / fail
- 需要改写的句子：

## 假设与风险

- 已采用的假设：
- 事实风险：
- 语气风险：
- 缺失素材：

## 修改建议

1. <具体修改>
2. <具体修改>
```

## 状态判断

`ready`：

- 稿件符合 brief。
- 事实 claim 有来源、是明确观点，或已安全标注。
- hook 和结构可用。
- 口播自然。
- 没有严重 AI 味。

`usable-for-draft-only`：

- 结构和方向可用，但仍有来源、例子或假设需要确认。
- 可以内部讨论，但不建议直接发布。

`blocked`：

- 主论点依赖未确认或高风险 claim。
- 稿件不符合已确认 brief 或用户 POV。
- 受众、目标或平台没有解决，导致写稿方向失真。
- AI 味严重，需要重写。
- 调研已经推翻原角度，但脚本没有修正。

## 审核后的停止

生成 `content-review.md` 后必须停下，给用户简短汇报：

- 当前状态。
- 最强部分。
- 最大风险。
- 下一步建议。

如果是 `blocked`，不能说稿件可以发布。
