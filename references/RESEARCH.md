# Research

`research-pack.md` expands the brief with outside context, verification, discourse, and inspiration. It should make the eventual script more accurate, less generic, and more aware of how the topic is being discussed.

## When Research Is Required

Use web research when the topic includes:

- Recent news, product updates, platform changes, regulations, prices, policies, market data, or release timing.
- Public companies, public figures, institutions, creators, or named products.
- Claims about what "people are saying", trends, backlash, user comments, or community reaction.
- A strong factual claim that would shape the script's main argument.
- A source the agent has not been given in full.

If web access is unavailable, state the limitation and mark the related claims as `needs-source`.

## Research Targets

Search across these layers as relevant:

| Layer | Purpose |
|---|---|
| Original source | Confirm what the source actually says. |
| Primary source | Company post, official doc, original video, paper, filing, policy, dataset. |
| Credible reporting | Establish timeline, context, and factual frame. |
| Creator discourse | See how self-media creators frame, simplify, dramatize, or teach the topic. |
| User reactions | Capture questions, confusion, objections, praise, and skepticism. |
| Counterarguments | Avoid one-sided scripts and find tension. |
| Adjacent examples | Find analogies, cases, demos, or useful comparisons. |
| Language inspiration | Collect useful phrases, hooks, terms, and structure patterns without copying. |

Prefer primary and official sources for factual claims. Use social posts and comments for discourse signals, not as factual proof unless they are the original claim being discussed.

## `research-pack.md` Template

```markdown
# Research Pack

## Research Goal

- Brief question:
- What needs verification:
- What needs inspiration:

## Source Map

| id | source | type | link | reliability | useful for |
|---|---|---|---|---|---|
| s1 | <title/name> | primary/reporting/social/commentary | <url> | high/medium/low | <fact/opinion/inspiration> |

## Fact Notes

| claim | source_id | status | note |
|---|---|---|---|
| <specific fact> | s1 | confirmed/needs-source/conflicting | <short note> |

## Discourse Signals

- What creators/users are excited about:
- What creators/users are skeptical about:
- Common misunderstanding:
- Common question:
- Useful counterargument:

## Angle Inspiration

| angle | source / signal | why useful | risk |
|---|---|---|---|
| <angle> | <s1 or discourse> | <script value> | <risk> |

## Useful Lines and Structures

- Potential hook:
- Useful phrase:
- Example / analogy:
- Structure pattern:

## Brief Update

- New or changed insight:
- Stronger content promise:
- Evidence to use:
- Claims to avoid or mark:
- Remaining research gaps:
```

## Classification Rules

Separate every useful item into one of three buckets:

- `fact`: A verifiable claim. Needs source.
- `opinion`: A viewpoint, interpretation, critique, or creator take.
- `inspiration`: Hook, phrase, analogy, structure, or framing idea. Do not copy directly.

Do not turn opinions or comments into facts. Do not imply "the internet thinks" unless there is clear evidence and enough examples.

## Source Quality

Use this reliability language:

- `high`: Official/primary source, original publication, direct transcript, dataset, reputable reporting with named sources.
- `medium`: Established media, expert analysis, creator with direct experience, well-supported secondary summary.
- `low`: Comments, anonymous posts, unverified screenshots, reposted claims, engagement-bait summaries.

Low-reliability sources can inspire questions or angles but should not support factual claims.

## Research Output Standards

- Include source links for anything factual or source-derived.
- Note publication dates for time-sensitive topics.
- Mark conflicting claims instead of forcing certainty.
- Keep direct quotes short and only when the exact wording matters.
- Do not over-research. Stop when the brief has enough evidence, tension, and usable angles.

## When Updating the Brief

Update or append to `content-brief.md` when research changes:

- The working insight.
- The recommended angle.
- The evidence list.
- The risk or red-line list.
- The readiness verdict.

If research disproves the original premise, say so clearly and propose a revised angle.
