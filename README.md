# claude-seed

The global `CLAUDE.md` — the rules Claude Code follows in every session, plus the
definitions of the two lower-level `CLAUDE.md` files so a new project can be set up
without explaining the system each time.

## Three levels

| file | scope | holds |
|---|---|---|
| `~/.claude/CLAUDE.md` | the machine, every session | the rules, and the shape of the other two |
| `<repo>/CLAUDE.md` | one project | that project's **answers** — commands, paths, hierarchy, quirks |
| `<feature-dir>/CLAUDE.md` | one feature | that feature's **spec** — purpose, flow, and what it does NOT do |

The rules live only at the top level. A repo file that restates them is a second copy
to keep right, so the lower two carry answers and specs — never rules.

## Installing it

Copy `CLAUDE.seed.md` to `~/.claude/CLAUDE.md`. Anything personal to that machine —
paths to local skills, tooling only you have — goes at the end under a
`# This machine only` heading, so the general rules stay portable.

Once it is in place, Claude already knows how to set up a new project: when a repo has
no `CLAUDE.md`, it works out what it can from the repo, asks about what it cannot, and
writes the file. Both templates are in the seed itself.

## What's in it

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

**Setting up a project** — when to write a repo `CLAUDE.md`, what to determine before
asking, what to ask, and the templates for both the repo file and a feature spec.
