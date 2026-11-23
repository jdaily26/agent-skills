# Agent Skills

Installable skills for Codex. Each skill lives in its own folder and can be installed independently. Both skills are instruction-only and require no additional tools, credentials, or services to use.

| Skill | Use it when |
| --- | --- |
| [Play Chess](skills/playchess/SKILL.md) | You need to choose a next move and prepare for how others might respond. |
| [Think Deeper](skills/thinkdeeper/SKILL.md) | You want to find the mechanism behind a problem and test a better approach. |

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

Run each install prompt once. Use the corresponding `$playchess` or `$thinkdeeper` prompt on a subsequent turn. If the skill is missing from the skill picker, start a new Codex session.

## Add a skill

1. Create `skills/<name>/SKILL.md`. Use a lowercase, hyphenated folder name that matches the YAML `name` field. Add a `description` that explains when the skill applies.
2. Include the MIT license in the folder so it ships with standalone installs. Keep dependencies inside that folder where possible. Link to supporting `references/`, `scripts/`, or `assets/` from `SKILL.md`, and document any external requirements.
3. Review the entire folder for personal information, secrets, and machine-specific paths. Validate it with Codex's `$skill-creator` and try a representative prompt in a workspace that has only the public skill files.
4. Add a catalog entry, use cases, sample prompts, and an install prompt using the GitHub URL for the new folder.

## License

[MIT](LICENSE)
