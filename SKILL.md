---
name: social-video-script-creator
description: Turn a raw idea, X post, YouTube transcript, article, news item, rough notes, or reference document into a structured self-media video spoken script through a brief-first workflow. Use when the user wants AI to act like an Account/Strategist before writing: clarify intent, create and score a content brief, research the topic, propose outline options, draft a Chinese口播稿, and review it against brief, sources, usefulness, and AI-flavor standards. This skill focuses on video script creation and does not create video design, HyperFrames handoff, animation, or rendered video.
---

# Social Video Script Creator

This skill is a **brief-first self-media video script creation harness**. It helps a creator turn loose material into a usable spoken script while keeping every step anchored to intent, evidence, audience value, and review standards.

Default mode: **files + conversation**. Write stage artifacts as Markdown files, but pause in conversation at decision gates.

## Scope

Use this skill for:

- One-line ideas, topic sparks, rough notes, articles, X posts, news, transcripts, tutorials, reference docs, or mixed source packs.
- Self-media content about industry news, creator techniques, tool updates, tutorials, observations, and personal takes.
- Chinese spoken scripts for platforms such as Bilibili, YouTube, video accounts, Xiaohongshu, Douyin, podcasts, or creator newsletters.

Do not use this skill to:

- Create video design systems, HyperFrames handoff docs, animations, HTML/CSS/GSAP, audio, or rendered videos.
- Fabricate facts, quotes, audience reactions, screenshots, metrics, or source claims.
- Skip brief and research gates when the topic depends on current facts or public claims.

## Standard Artifact Set

Create or update these files for a project:

```text
content-brief.md      # intake, account-style brief, readiness score, assumptions
research-pack.md      # external/source research, discourse, inspiration, source links
outline-options.md    # 2-3 routes, recommendation, discussion checkpoint
script.md             # final or draft spoken Chinese script
content-review.md     # on-brief, source, usefulness, structure, and AI-flavor QA
```

If the user provides original material, preserve it as `source-material.md` or a clearly named source file when useful.

## Workflow

### Phase 1 - Input Intake

First act as an Account/Strategist, not a copywriter.

- Identify the input type, source boundary, current certainty, likely audience, and missing context.
- If the input is only an idea, do not invent a complete episode. Build a lightweight brief and ask for the missing decisions.
- If the input is current, factual, public, controversial, or references real people/companies/products, plan for research before writing.

Read [`references/BRIEF.md`](references/BRIEF.md) before producing `content-brief.md`.

### Phase 2 - Brief Building

Produce `content-brief.md` with:

- Source understanding and topic boundary.
- Creator motivation and POV.
- Audience, platform, objective, core tension, evidence, constraints, tone.
- Targeted questions for missing context.
- 100-point brief readiness score.

Brief gate:

- `80-100`: continue to research and outline.
- `65-79`: continue only after warning the user what assumptions will be made.
- `<65`: ask more questions before continuing unless the user explicitly overrides.

Critical missing fields always require a warning: no clear audience, no creator POV, no content objective, current-fact topic without source/search, or strong claim without evidence.

### Phase 3 - Research Expansion

Read [`references/RESEARCH.md`](references/RESEARCH.md) before producing `research-pack.md`.

Use web search when the topic involves:

- Current news, public-company or public-figure claims, product updates, regulations, platform changes, prices, or time-sensitive facts.
- Public discourse, creator reactions, comments, examples, or how other self-media creators frame the same topic.
- Claims that need verification before becoming a script backbone.

Research should separate fact, opinion, and inspiration. Update `content-brief.md` with research-backed insight or assumptions when research changes the angle.

### Phase 4 - Outline Development

Read [`references/OUTLINE.md`](references/OUTLINE.md) before producing `outline-options.md`.

Offer 2-3 content routes and recommend one. Each route must include:

- Hook direction.
- Core insight.
- Argument path.
- Examples/evidence.
- Viewer payoff.
- Ending action or memory point.
- Tradeoffs and risks.

Pause for user confirmation before drafting unless the user explicitly authorizes autonomous continuation.

### Phase 5 - Script Writing

Read [`references/SCRIPT.md`](references/SCRIPT.md) before producing `script.md`.

Write natural spoken Chinese:

- Conversational, specific, short, and easy to say aloud.
- Strong hook, clear rhythm, concrete examples, and useful takeaways.
- Low AI flavor: no fake empathy, hollow profundity, self-importance, template-heavy phrasing, or empty parallelism.
- Preserve important facts and mark unverified claims rather than smoothing them into certainty.

### Phase 6 - Final Review

Read [`references/REVIEW.md`](references/REVIEW.md) before producing `content-review.md`.

Review:

- On-brief alignment.
- Research and source use.
- Factual risk and unsupported claims.
- Audience usefulness and originality.
- Structure, spoken naturalness, and AI flavor.
- Readiness for next step.

Final status must be one of:

- `ready`
- `usable-for-draft-only`
- `blocked`

If blocked, state the minimum fixes needed before the script can be used.

## Collaboration Rules

- Ask targeted questions that change the content direction; avoid generic "what do you think" questions.
- When proceeding with assumptions, label them inside the relevant artifact.
- Recommend a direction instead of only listing options.
- Do not write the final script before brief and outline gates are satisfied or explicitly overridden.
- Keep the user aware of tradeoffs in plain language.
