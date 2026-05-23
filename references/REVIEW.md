# Review

`content-review.md` is the final quality gate. It decides whether the script is ready, draft-only, or blocked.

## Review Inputs

Review against:

- `content-brief.md`
- `research-pack.md` if present
- `outline-options.md`
- `script.md`
- User confirmations and assumptions

## `content-review.md` Template

```markdown
# Content Review

## Verdict

- Status: ready / usable-for-draft-only / blocked
- Main reason:
- Minimum fixes:

## Brief Alignment

| brief element | status | note |
|---|---|---|
| Audience | pass/warn/fail |  |
| Creator POV | pass/warn/fail |  |
| Content objective | pass/warn/fail |  |
| Core tension / insight | pass/warn/fail |  |
| Platform / length | pass/warn/fail |  |
| Tone / red lines | pass/warn/fail |  |

## Research and Source Use

| claim/source need | status | note |
|---|---|---|
| <claim> | confirmed/needs-source/opinion/risky | <note> |

## Audience Value

- Clear viewer payoff: pass/warn/fail
- Practical usefulness: pass/warn/fail
- Differentiation from generic summary: pass/warn/fail
- Strongest useful moment:
- Weakest or most generic moment:

## Structure and口播

- Hook: pass/warn/fail
- Flow: pass/warn/fail
- Examples: pass/warn/fail
- Ending: pass/warn/fail
- Spoken naturalness: pass/warn/fail

## AI Flavor Check

- Fake empathy: pass/warn/fail
- Hollow profundity: pass/warn/fail
- Self-importance: pass/warn/fail
- Template-heavy phrasing: pass/warn/fail
- Empty parallelism: pass/warn/fail
- Lines to revise:

## Assumptions and Risks

- Assumptions made:
- Factual risks:
- Tone risks:
- Missing material:

## Recommended Fixes

1. <specific fix>
2. <specific fix>
```

## Verdict Rules

Use `ready` only when:

- The script matches the brief.
- Factual claims are confirmed, clearly framed as opinion, or safely caveated.
- The hook and structure are usable.
- The script sounds speakable.
- No critical AI-flavor issue remains.

Use `usable-for-draft-only` when:

- The concept and structure are useful, but some assumptions, sources, or examples still need confirmation.
- The script can be discussed internally but should not be published as-is.
- The topic is not high-risk and missing claims are not central to the argument.

Use `blocked` when:

- The main argument depends on an unverified or risky claim.
- The script does not match the confirmed brief or creator POV.
- The audience, objective, or platform was never resolved and assumptions would distort the work.
- The script contains serious AI flavor that would require rewriting.
- The research contradicts the proposed angle and the script ignores that contradiction.

## On-Brief Questions

Ask:

- Does the script serve the selected audience?
- Does it express the creator's POV, not just a neutral summary?
- Does it deliver the promised viewer payoff?
- Does it use research to sharpen the angle?
- Does it avoid claims the brief marked as red lines or risky?

## Audience Value Questions

Ask:

- What does the viewer get that they would not get from reading the original source?
- Is there at least one concrete takeaway, example, warning, or method?
- Is the content specific enough to be memorable?
- Does it respect the viewer's time?

## AI Flavor Fixing

When AI flavor appears, do not merely label it. Rewrite the specific lines or list exact replacements.

Examples:

| Weak line | Better direction |
|---|---|
| "在这个快速变化的时代..." | Start with the specific event or problem. |
| "这背后的底层逻辑是..." | State the mechanism directly. |
| "你是不是也经常..." | Use a concrete creator experience or observed problem. |
| "总结一下..." | End with the practical takeaway or memory point. |

## Final Reporting

When reporting back to the user, include:

- Final status.
- The strongest part of the script.
- The biggest remaining risk.
- The next recommended action.

If status is `blocked`, do not present the script as ready to publish.
