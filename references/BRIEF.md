# Brief

`content-brief.md` is the first quality gate. It translates loose input into a self-media creative brief before any scriptwriting starts.

The agent's role here is Account/Strategist: understand the material, clarify intent, identify missing context, and decide whether the project is ready to move forward.

## Intake Classification

Classify the user input before writing the brief:

| Input type | How to handle |
|---|---|
| One-line idea | Treat as a topic spark; ask for motivation, POV, audience, and references. |
| X post / social post | Capture the claim, context, author, reactions if available, and why the creator noticed it. |
| YouTube transcript /口播稿 | Identify the main argument, examples, usable lines, and what can be transformed. |
| Article / news | Separate factual reporting, interpretation, and potential creator angle. |
| Tutorial / tool update | Identify user problem, workflow, novelty, proof, and demonstration needs. |
| Multiple references | Build a synthesis brief; mark conflicts and source hierarchy. |

## `content-brief.md` Template

```markdown
# Content Brief

## Input Snapshot

- Source type:
- Source boundary:
- One-sentence topic:
- What is confirmed:
- What is uncertain:

## Creator Intent

- Why I picked this topic:
- My current POV:
- Desired audience takeaway:
- Desired audience action:
- Personal experience / authority:

## Audience and Platform

- Target audience:
- Audience current belief / pain:
- Platform:
- Format / target length:
- Tone:

## Strategic Core

- Content objective:
- Core tension:
- Working insight:
- Single-minded content promise:
- Key proof / examples:
- Red lines / constraints:

## Missing Context Questions

1. <question that materially changes the direction>
2. <question that materially changes the direction>

## Readiness Score

| Dimension | Max | Score | Notes |
|---|---:|---:|---|
| Topic / source clarity | 15 |  |  |
| User motivation and POV | 15 |  |  |
| Target audience | 15 |  |  |
| Platform / format / length | 10 |  |  |
| Content objective | 15 |  |  |
| Core tension or insight | 15 |  |  |
| References / evidence / examples | 10 |  |  |
| Constraints, red lines, tone | 5 |  |  |
| **Total** | **100** |  |  |

## Readiness Verdict

- Status: ready / assumption-based / not-ready
- Reason:
- Assumptions if continuing:
- Warnings:
```

## Scoring Standards

### Topic / source clarity - 15

- `13-15`: Source and topic boundary are clear; no confusion about what is being discussed.
- `8-12`: Topic is understandable but source context or scope is incomplete.
- `0-7`: Only a vague idea or unclear source is available.

### User motivation and POV - 15

- `13-15`: The creator's reason, stance, and personal angle are clear.
- `8-12`: Motivation exists but POV is generic or weak.
- `0-7`: No clear reason why this creator should talk about it.

### Target audience - 15

- `13-15`: Audience is concrete, with current belief/pain and level of knowledge.
- `8-12`: Audience category is named but psychology is thin.
- `0-7`: Audience is "everyone" or absent.

### Platform / format / length - 10

- `8-10`: Platform, format, and rough length are known.
- `4-7`: One or two are known.
- `0-3`: No delivery context.

### Content objective - 15

- `13-15`: Clear desired outcome: inform, teach, persuade, warn, critique, or inspire action.
- `8-12`: General goal exists but is hard to evaluate.
- `0-7`: No clear job for the content.

### Core tension or insight - 15

- `13-15`: There is a strong conflict, misconception, surprise, or human truth.
- `8-12`: There is an angle but not yet sharp.
- `0-7`: The content is only descriptive.

### References / evidence / examples - 10

- `8-10`: Source, examples, evidence, or personal tests are available.
- `4-7`: Some references exist but need expansion or verification.
- `0-3`: No support beyond assertion.

### Constraints, red lines, tone - 5

- `4-5`: Tone and forbidden claims/positions are clear.
- `2-3`: Some tone preference exists.
- `0-1`: No constraints.

## Thresholds

- `80-100`: Ready for research and outline.
- `65-79`: Usable, but warn the user what assumptions will be made.
- `<65`: Ask more questions before continuing.

The user can override and continue, but all later outputs must be labeled assumption-based.

## Critical Missing Fields

Always warn if any of these are missing:

- No clear audience.
- No creator POV.
- No content objective.
- Topic depends on current facts but has no source or search permission.
- User asks for a strong claim without evidence.

## Good Brief Questions

Ask only questions that materially change the work:

- Why did this topic catch your attention now?
- What do you personally agree or disagree with in the source?
- Who is this for: beginners, practitioners, clients, peers, or fans?
- What should the audience be able to do or think after watching?
- Is this a hot take, tutorial, news explanation, case teardown, or personal method?
- Are there creators, posts, videos, or articles you want me to compare against?
- What must not be changed, exaggerated, or mentioned?
- How sharp can the tone be?

## Minimum Viable Brief

Before outline, at least these must be known or explicitly assumed:

- Topic boundary.
- Creator POV.
- Audience.
- Content objective.
- Platform or target length.
- Core tension or working insight.
- Evidence/source plan.
