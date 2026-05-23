# Social Video Script Creator Skill

**A brief-first Codex skill for turning raw ideas, X posts, transcripts, articles, and news into researched Chinese self-media video spoken scripts.**

[中文文档](./README.zh-CN.md)

---

## What Is This?

`social-video-script-creator` is a script creation skill for self-media creators. It treats every script request like a lightweight creative brief: before writing, the agent clarifies the creator's intent, audience, point of view, source material, research needs, and quality bar.

It is designed for creators who often start from:

- one-line topic ideas
- X posts or social media discourse
- YouTube transcripts or existing narration
- articles, news, tutorials, product updates, or rough notes
- multiple reference materials that need synthesis

The final goal is a usable Chinese spoken script, not a video production package.

## Core Ideas

- **Brief before writing** — the agent first acts like an Account/Strategist, not a copywriter.
- **Score the brief** — weak inputs are not hidden; the skill gives a readiness score and warns when it is continuing with assumptions.
- **Research before structure** — current events, public claims, creator discourse, and outside references should be checked before outlining.
- **Outline before script** — the agent proposes 2-3 routes, recommends one, and pauses before drafting.
- **口播 comes first** — scripts should sound natural when spoken, not like reports or generic AI essays.
- **Review is a gate** — final output is checked for brief alignment, source risk, audience value, structure, and AI-flavor.

## Workflow

```text
Phase 1  Input intake
Phase 2  Build and score content-brief.md
Phase 3  Research and create research-pack.md
Phase 4  Propose outline-options.md and confirm route
Phase 5  Write script.md
Phase 6  Review with content-review.md
```

## Generated Output

```text
my-script-project/
├── source-material.md       # optional preserved source material
├── content-brief.md         # brief, missing context, score, assumptions
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
