# Friendly Reviewer2 - Claude Skill

A Claude skill that turns Claude into a strict but constructive senior reviewer for Q1 (top-quartile) journals — across any discipline. The friendly Reviewer 2. Tough, but every point lands.

## What it does

Produces a standard reviewer report on an academic manuscript, draft, abstract, or section:

- **Summary of the manuscript** — proof the reviewer understood what the paper is doing
- **Overall assessment** — the headline judgement and the single most important issue
- **Major comments** — substantive issues, each following a *what's wrong → why it matters → what to do* pattern
- **Minor comments** — smaller fixes
- **Recommendation** — reject, major revision, minor revision, or accept, with justification

Calibrated to Q1 standards. Field-agnostic — works for education, social sciences, sciences, humanities. If the field meaningfully changes the bar, it asks once before reviewing.

## When it triggers

Phrases such as `review my manuscript`, `critique this`, `be my Q1 reviewer`, `would this survive peer review`, `tear this apart`, or just `friendlyR2`. Also fires when academic prose is pasted in with a request to assess its quality.

It deliberately does *not* trigger on copy-editing, reference formatting, or style polishing.

## Installation

Place the `SKILL.md` (or the packaged `.skill` file) in your Claude skill directory, or upload it through the Claude skills interface.

## Usage

```
friendlyR2, review this introduction.
```

```
Be my Q1 reviewer for this methods section.
```

```
Would this discussion survive peer review at a top-tier journal?
```

Paste the manuscript text below the request. For revisions, mention any previous reviewer comments — the skill will weight the review toward whether the revision addresses them.

## Design notes

The skill enforces:

- A fixed five-section report structure, so output is consistent across runs
- A guard against the default-to-major-revision habit — reject is allowed when warranted
- Explicit anti-patterns: no sandwiching, no vagueness, no reviewer fan fiction, no performative cruelty, no AI disclaimers
- A constructive principle — every major comment must point at a plausible direction the author could take

## License

MIT. See `LICENSE`.

## Author

Chuah Kee Man — *The Sepet Educator*  
[github.com/keemanxp](https://github.com/keemanxp)
