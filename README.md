# Social Video Script Creator Skill

**A brief-first Codex skill for turning raw ideas, X posts, transcripts, articles, and news into researched Chinese self-media video spoken scripts.**

[中文文档](./README.zh-CN.md)

---

## What Is This?

`social-video-script-creator` is a script creation skill for Chinese self-media creators. It treats every script request like a lightweight creative brief: before writing, the agent preserves the source material locally, clarifies the creator's intent, audience, point of view, research needs, and quality bar.

It is designed for creators who often start from:

- one-line topic ideas
- X posts or social media discourse
- YouTube transcripts or existing narration
- articles, news, tutorials, product updates, or rough notes
- multiple reference materials that need synthesis

The final goal is a usable Chinese spoken script, not a video production package. All generated project artifacts are Chinese-first.

## Core Ideas

- **Source material before brief** — the agent must create `source-material.md` before building the brief.
- **Brief as the master document** — `content-brief.md` accumulates source summary, user answers, research insights, final outline, and next step.
- **Hard checkpoints** — every stage stops for user confirmation; a high brief score never bypasses confirmation.
- **Research before structure** — current events, public claims, creator discourse, and outside references are checked before outlining.
- **Outline before script** — the agent proposes 2-3 routes, recommends one, waits for selection, then writes the final outline back into the brief.
- **口播 comes first** — scripts should sound natural when spoken, not like reports or generic AI essays.
- **Review is a gate** — final output is checked for brief alignment, source risk, audience value, structure, and AI-flavor.

## Workflow

```text
Phase 1  Create source-material.md, then stop at the brief gate
Phase 2  Build and score content-brief.md, then stop for confirmation
Phase 3  Research, create research-pack.md, write key findings back to content-brief.md, then stop
Phase 4  Propose outline-options.md, then stop for route selection
Phase 5  Write the final outline back to content-brief.md, then stop
Phase 6  Write script.md, then stop before review
Phase 7  Review with content-review.md
```

## Generated Output

```text
my-script-project/
├── source-material.md       # required local source center
├── content-brief.md         # cumulative master brief, score, next step
├── research-pack.md         # source links, discourse signals, fact/opinion/inspiration split
├── outline-options.md       # 2-3 routes and recommendation
├── script.md                # Chinese spoken script
└── content-review.md        # final QA and readiness status
```

These files are generated inside the user's project. They are not sample files shipped in this skill repository.

## Reference Map

- [BRIEF.md](./references/BRIEF.md) — intake questions, brief template, scoring standards, minimum viable brief
- [RESEARCH.md](./references/RESEARCH.md) — research targets, source quality, fact/opinion/inspiration classification
- [OUTLINE.md](./references/OUTLINE.md) — outline options, route types, recommendation logic, checkpoint rules
- [SCRIPT.md](./references/SCRIPT.md) — spoken Chinese standards, information fidelity, anti-AI-flavor rules
- [REVIEW.md](./references/REVIEW.md) — final QA, verdict rules, on-brief checks, fix guidance

## Relationship To Social Video Planner

This skill focuses on **briefing, research, outlining, and spoken script creation**.

`social-video-planner` is a downstream planning skill for video production and HyperFrames handoff. Use this skill when the main job is getting the口播稿 right. Use `social-video-planner` when the script needs to become a video planning package with scene mapping and HyperFrames handoff.

This skill does not create video design, HyperFrames handoff documents, animation, audio, HTML/CSS/GSAP, or rendered video.
