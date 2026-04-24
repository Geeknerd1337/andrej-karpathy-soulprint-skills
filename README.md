# karpathy-skills

A `CLAUDE.md` / Cursor rule / Claude Code plugin distilling **Andrej Karpathy's actual coding pedagogy and writing voice** into operational rules an LLM coding assistant can follow.

Built from a [9,001-tweet + 31-essay + 20-video soulprint](https://github.com/joshuawilson/ai_memories) of `@karpathy` (scraped 2026-04-17). Every principle is anchored in a verbatim Karpathy quote.

> Inspired by `forrestchang/andrej-karpathy-skills`, but where that repo distills four principles from a single Karpathy tweet, this one is built from his complete public corpus — pedagogy patterns, voice conventions, signature moves, and dated predictions.

---

## The Six Principles

| # | Principle | One-line form |
|---|---|---|
| 1 | **Calibrate Confidence** | Hedge mechanism, be bold on world-claims. `(?)` for ~60%. |
| 2 | **Confess What's Ugly Up Front** | Failure modes before solutions. Bugs live in plumbing. |
| 3 | **Compress, Don't Bloat** | "Everything else is just efficiency." 100 lines > 1000. |
| 4 | **Surgical Changes** | Every changed line traces to the user's request. |
| 5 | **Close the Loop with Evidence** | Demos are easy. Production is the march of nines. |
| 6 | **Be Cheerfully Wrong — and Build the Ramp** | Admit, update publicly, hand back something runnable. |

Full text: [`CLAUDE.md`](./CLAUDE.md).

---

## Why a richer version?

The original `forrestchang/andrej-karpathy-skills` repo is built from one Karpathy tweet about LLM coding pitfalls. It captures four useful principles. This repo is built from his entire public corpus, so it can carry:

- His **confidence-by-scope rule** (world-claims direct, mechanism hedged) — not just "don't assume."
- His **"failure modes go up front"** pedagogy — not just "ask clarifying questions."
- His **"everything else is just efficiency"** minimization line, used verbatim from 2022 to 2026.
- His **march-of-nines** patience model — anchored in Tesla Autopilot and Waymo 2014→2024.
- His **cheerful self-correction** pattern — not just "admit mistakes" but the *tone* (smiley, immediate, structural).
- His **build-the-ramp** thesis — output should be runnable, scaffolded, and copy-pasteable.
- His **closing-move discipline** — no response ends on a confident period.
- His **voice** — `imo`, `kind of`, `(?)`, two-word parentheticals, pull-quoted punchlines, code-before-math.

Each principle is anchored in a real, dated, sourced Karpathy quote — not a paraphrase.

---

## Install

### Option A — Cursor project rule

This repo includes [`.cursor/rules/karpathy-guidelines.mdc`](./.cursor/rules/karpathy-guidelines.mdc) with `alwaysApply: true`. Drop the `.cursor/` directory into any Cursor project and the rule applies automatically.

### Option B — `CLAUDE.md` (per-project)

New project:

```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/joshuawilson/karpathy-skills/main/CLAUDE.md
```

Existing project (append):

```bash
echo "" >> CLAUDE.md
curl https://raw.githubusercontent.com/joshuawilson/karpathy-skills/main/CLAUDE.md >> CLAUDE.md
```

### Option C — Claude Code plugin

```
/plugin marketplace add joshuawilson/karpathy-skills
/plugin install karpathy-skills@karpathy-skills
```

---

## How to know it's working

You should see, over time:

- **Diffs that match the request line-for-line** — no drive-by refactoring.
- **Calibrated language** — fewer "this is correct" claims, more "I think," "I checked," "I haven't verified."
- **Failure modes named up front** — fewer "actually it didn't work" follow-ups.
- **Smaller PRs** — 50 lines where there used to be 500.
- **Cheerful corrections** — when wrong, the assistant updates immediately rather than litigating.
- **Runnable handoffs** — every response ends with a command, a test, or a one-liner the user can copy.

---

## License

MIT. Karpathy quotes are reproduced under fair use; sources cited inline.

ʕ•ᴥ•ʔ
