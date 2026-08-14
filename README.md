# claude-seed

A starting `CLAUDE.md` for new projects — work and personal.

`CLAUDE.md` is the file Claude Code reads at the start of every session in a repo. This
is the version to begin from, so a new project inherits a working style instead of
being written from scratch each time.

## How to use it

1. Copy `CLAUDE.seed.md` into the new project's root, renamed to `CLAUDE.md`.
2. Fill in every `<TODO: ...>` slot — test command, doc paths, log location, and the
   document hierarchy. An unfilled slot is a rule nobody can follow.
3. Delete the instruction comment at the top.
4. Delete any section the project genuinely does not have. A rule that describes
   something nonexistent is worse than no rule.

Everything in the file loads into every session, so keep it short as it grows.
Long-form detail belongs in the project's `README.md`, its architecture doc, or its
build log — not here.

## What's in it

Fifteen sections, in four groups.

**How to work and communicate**
- Partner, not subordinate — push back on bad ideas, then defer
- Write plainly — plain words, conclusion first, in every message
- Ship whole, never in phases — deferral is the user's call, not the agent's
- Ask before writing to anything outside the repo

**Judgement**
- Quality is the number one priority — never weaken a check to make something pass
- Never work from memory — measurements and opened sources only, never recall
- Check upward before changing anything — a change is checked against the plan above it

**Docs**
- README.md is always current
- The architecture doc is updated in the same change
- Every real feature has a spec, and the user owns it
- Build and decision logs are append-only

**Engineering**
- TDD, plus: a command reporting success is not proof it did the thing, and a check
  that did not run must never report success
- Detailed logging on every feature
- PR review paradigm — build agent and review agent, never self-approve
- Task-completion recap — what shipped, what is still running, what is left

