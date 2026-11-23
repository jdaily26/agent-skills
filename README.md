# Agent Skills

Installable skills for Codex. Each skill lives in its own folder and can be installed independently. Play Chess and Think Deeper need no additional tools. The PR agents use public web access to verify current opportunities and prepare pitch drafts.

| Skill | Use it when |
| --- | --- |
| [Play Chess](skills/playchess/SKILL.md) | You need to choose a next move and prepare for how others might respond. |
| [Think Deeper](skills/thinkdeeper/SKILL.md) | You want to find the mechanism behind a problem and test a better approach. |
| [CCPRAgent](skills/ccpragent/SKILL.md) | You want to find interview leads for CC Studio and pitch a specific piece or making technique. |
| [NayewayPRAgent](skills/nayeway-pr-agent/SKILL.md) | You want to find interview leads for Nayeway or *Visual Silence* and pitch an angle tailored to each outlet. |

## Play Chess

Use Play Chess for negotiations, partnership decisions, difficult conversations, or decisions with competing goals. It compares possible moves against your immediate objective and the position you want afterward. It recommends one action, anticipates the most likely response, gives you a reply, and explains what the move may teach others about working with you.

Paste this installation prompt into Codex.

```text
$skill-installer Install https://github.com/jdaily26/agent-skills/tree/main/skills/playchess
```

**Example prompts**

- `$playchess A partner wants exclusivity before committing resources. Help me choose my next move and write what I should say.`
- `$playchess My team keeps accepting last-minute scope changes. What should I do on the next request, and how should I handle pushback?`

## Think Deeper

Use Think Deeper to diagnose a recurring problem, improve a design, or challenge the premise of a plan. It looks for shared causes, borrows structural analogies from distant fields, and tests promising explanations against alternatives. When the insight changes the decision, it suggests a small experiment and identifies what evidence would support or weaken it.

Paste this installation prompt into Codex.

```text
$skill-installer Install https://github.com/jdaily26/agent-skills/tree/main/skills/thinkdeeper
```

**Example prompts**

- `$thinkdeeper New members finish onboarding but rarely return. Find a plausible shared cause and design a small test that could disprove it.`
- `$thinkdeeper Help me simplify this approval process. Look for a pattern from another field that fits our constraints, then turn it into a reversible trial.`

## CCPRAgent

Find and rank local blogs, craft publications, and podcast hosts that interview independent makers. For each recommendation, the skill verifies recent work and a public contact route, then drafts a full pitch around a piece or technique CC Studio can show.

Paste this installation prompt into Codex.

```text
$skill-installer Install https://github.com/jdaily26/agent-skills/tree/main/skills/ccpragent
```

**Example prompt**

- `$ccpragent Find three active jewelry or craft podcasts that recently interviewed an independent maker. Rank them and write a full pitch for each.`

## NayewayPRAgent

Find and rank interviews for Nayeway’s design work and *Visual Silence*. The skill checks whether an outlet books comparable guests and drafts a pitch around a specific idea Nayeway can discuss or demonstrate.

Paste this installation prompt into Codex.

```text
$skill-installer Install https://github.com/jdaily26/agent-skills/tree/main/skills/nayeway-pr-agent
```

**Example prompt**

- `$nayeway-pr-agent Find independent design newsletters and home podcasts that book emerging designers or first-time authors. Draft a full pitch for each using a verified Visual Silence angle.`

Run each install prompt once. Invoke the installed skill on a subsequent turn. If the skill is missing from the skill picker, start a new Codex session.

## Add a skill

1. Create `skills/<name>/SKILL.md`. Use a lowercase, hyphenated folder name that matches the YAML `name` field. Add a `description` that explains when the skill applies.
2. Include the MIT license in the folder so it ships with standalone installs. Keep dependencies inside that folder where possible. Link to supporting `references/`, `scripts/`, or `assets/` from `SKILL.md`, and document any external requirements.
3. Review the entire folder for personal information, secrets, and machine-specific paths. Validate it with Codex's `$skill-creator` and try a representative prompt in a workspace that has only the public skill files.
4. Add a catalog entry, use cases, sample prompts, and an install prompt using the GitHub URL for the new folder.

## License

[MIT](LICENSE)
