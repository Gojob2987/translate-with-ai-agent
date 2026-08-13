# Translation Co-Workflow

*Licensed under MIT — full license text at the end of this document.*

> **What this is.** Co-translation: a human translator and an AI agent produce a literary translation as an **engineering project** — resumable from files alone, auditable decision-by-decision, with knowledge and workflow extracted as first-class byproducts.
>
> **Human-in-the-loop (read first).** This workflow differs from typical agent skills: it **requires intensive human intervention throughout**. The agent never produces the translation alone. The agent is the *environment* — dictionary, discussion peer, idea housekeeper, pen, memory. The human is the *engine* — context, lived feeling, the ear for the common tongue, commitment to finish.

---

## Getting Started (Hook)

How a session begins:

1. **The agent reads this file first** — it is the procedure source of truth (plus the living docs, see Knowledge Management).
2. **The human asks:** "what do I do / where do we start?"
3. **The agent answers with the plan** derived from the phases below: current position + next action (e.g. "Phase 1: draft the first chapter; I'm your dictionary on call — ask me anything").
4. **They progress together**; the question loop (below) drives the work.

A project can be resumed anywhere: the phases + session logs answer "where are we" with no conversation history.

---

## Pattern: Question Loop + Pending Change Ledger

```
Human: "Polish line L52" (or: "resume")
    │
    ▼
Human writes annotations / logs questions (Q1, Q2, …)
    │
    ▼
Agent: reads annotation + original → writes analysis
  ├── review-report.md  (Context / Rationale / Options ← recommended / Editor note)
  └── multi-language semantic verification (semantics only, never wording)
    │
    ▼
Human: verdicts in the question log's decisions record, per batch (~10 questions)
  ├── "keep option N" / "change, option M" / own wording
  └── dwell discussions until concluded
    │
    ▼
Agent: confirmed changes → Pending Change Ledger (# | line | current | verdict | new)
    │
    ▼
Human: one final check of the ledger → lands edits personally
    │
    └── (loop until no open questions)
```

---

## Why This Pattern (Rationale)

Translation is treated as software engineering, and the pattern follows:

- **Persistent storage over living memory.** The human's memory is finite and degrading; every question, analysis, verdict, and change is written down, so machines and sessions are interchangeable. A project can resume from files alone after a machine switch.
- **Log pruning is standard procedure.** Documents grow like codebases; concluded content rolls to an archive (bulk write per roll), keeping the living files small. Git history is the permanent record — pruning is maintenance, not loss.
- **I/O byproduct model.** Input = base text + human annotation; output = the translation; byproducts = background knowledge, writing-craft vocabulary, workflow itself. Byproducts are first-class deliverables, not accidents.
- **Auditable decisions.** Every change traces to question → analysis → verdict → ledger row; diffs are reviewable, blame is possible.
- **Cheap decisions, human judgment.** The agent's options serve as scaffolding; the human's native ear and taste decide. Agents propose, humans decide — no silent changes.

---

## The Artifact Model (I/O)

Three buckets — named for what they hold, no engineering background needed:

```
{project}/
├── input/        ← what goes in: the base text — READ-ONLY
├── output/       ← what comes out: the translation + its published forms
│   └── publish/  ← publishable copy + LICENSE
└── by-product/   ← what we produced along the way:
    ├── annotation/   ← the translator's essay/annotations — AI READ-ONLY
    ├── reference/    ← AI-extracted background knowledge; other-language translations (semantics only)
    └── logs/         ← living docs + archive/ (see Knowledge Management)
```

Investigations and other research belong in `by-product/` too — nothing in this layout assumes multiple projects per repo.

Rules:
- **Base text is fixed** (decide the source edition once; a revised edition serves as *semantic reference only*, never as a second base text or naming source).
- **input/ and output/ are off-limits to the AI** without explicit permission (editing red line). Changes flow discussion → verdict → human lands them personally.
- **Knowledge is extracted, not written**: the annotation file → AI extracts questions (question log) and knowledge (background notes); the annotation file itself is never rewritten.

---

## Translation Phases

**Annotation is a continuous stream, not a phase.** It grows incrementally from the first reading to the last review — draft-time marks, polishing marginalia, review-time reflections — kept in a persistent file, referable back at any time. Modularity (annotation vs draft as separate files) is a freedom of instantiation; in practice they are produced together: annotate as you read / draft.

| # | Phase | Who does what | Input | Output |
|---|---|---|---|---|
| 0 | **Discovery** | Human: finds the text interesting, makes notes, looks up words, forms a draft/doodle (on the base text or separately) | a text | interest + notes → the decision to translate |
| 1 | **Draft & annotation** | Human translates; agent on call as dictionary (word/context questions on demand) | base text | first draft, annotations growing alongside |
| 2 | **Worldview alignment** | Agent reads base text + draft, extracts from annotations/reference, asks the human about worldview and critical background; human answers | original + draft | aligned understanding (background knowledge) |
| 3 | **Line-by-line polishing** | Agent proposes candidates/perspectives per line; human contemplates and decides; repeat until natural | draft + annotations + review-report | verdicts → Pending Change Ledger → landed edits |
| 4 | **Coherence re-read** | Both re-read the whole work; annotations updated (deep polishing exposes missing links); inconsistencies found, better coherence suggested | polished draft | fixed links, updated annotations |
| 5 | **Lint** | Agent: mechanical check — grammar, punctuation, formatting, special symbols, term/name consistency | final draft | lint report, cleanup fixes |
| 6 | **Publication** | Both: prepare the publish copy and the license (see below) | translation + byproducts | publish copy, LICENSE, repository |

Phases 4 and 5 split the review into substance (both) and mechanics (agent): verdict batches for meaning, quote/format fixes for lint.

---

## Review Loop Details

### Analysis format (review-report.md appendix entries)

Every answered question follows the same block:

- **Context** — original quote + current translation (with line numbers). **Quote the full sentence** (or the whole paragraph when the thought spans it) — never a truncated fragment; local excerpts mislead analysis
- **Rationale** — independent analysis from the original
- **Options** — 1. 2. 3., one marked ← **recommended**
- **Editor note** — extra considerations (register, foreshadowing, multi-language consensus)

**Global best over local best (principle).** Every rendering must fit the sentence, the paragraph, the character, the scene, the entire work — not just the excerpted fragment. Tradeoffs between local polish and global coherence always resolve toward the whole; context quotes must therefore be complete enough for that judgment (full-sentence minimum).

**File state is truth (principle).** Analysis contexts must be checked against the actual output file, never the agent's in-memory text — stale contexts once produced a false verdict. When a verdict seems to target a rendering the file doesn't contain, re-read the file before deciding.

### Verdict conventions (question-log.md, decisions record)

- `keep option N` / `change, option M` / the translator's own wording (often beats the agent's literals — options are scaffolding)
- Dwell discussions: the translator probes apparent contradictions in the original; resolve the source's logic first, then choose wording
- Batch size ~10 questions; larger batches OK
- **Story-logic reading:** probes narrative coherence across distant lines — a seeming contradiction between two passages may be the intended story beat (e.g. a character's memory being erased), not a translation error. Story mechanics first, wording second.

### Pending Change Ledger

Confirmed changes accumulate in a table: `# | line | current | verdict | new wording`. **Verdicts are not applied immediately** — the translator does one consolidated final check, then lands the edits personally.

### Multi-language semantic verification (routine when a word's sense is in doubt)

1. AI self-checks from the original first (dictionary sense, context, structure)
2. Download reference translations via the original page's "In Other Languages" module (if the platform provides one) into `by-product/reference/other-language-translations/`
3. If the AI cannot download, hand the link list to the human (a web clipper works well)
4. Use them **for semantics only — never copy wording**; verification results go into the analysis
5. ⚠️ Some language branches may not exist or be dead (404) — verify by actual fetch results

**Reference editions:** consulted only for semantics (author revisions clarify intent). Adopt the *clarification*, keep the base text's text and naming.

---

## Knowledge Management (Living Docs + Archive)

Two kinds of documents — **living** (loaded every session) and **archive** (on demand):

| Living file (keep small) | Holds |
|---|---|
| `question-log.md` | open-items tracker (Q# / 1-line topic / status) + the translator's decisions record (accumulating verdicts) |
| `review-report.md` | header/status, Pending Change Ledger, active discussions, proposals awaiting verdicts, glossary |
| `session-log.md` | latest dated sections: status, pending items, user habits, implicit worldview consensus |

| Archive (`logs/archive/`) | Holds |
|---|---|
| dated/round files | concluded report sections, concluded question lists, superseded session-log sections |

**Expiration rule (when to roll):**
- **Primary — batch conclusion:** when a verdict batch is fully decided and the ledger is updated, that batch's analysis rolls (its conclusions live in ledger/verdicts)
- **Backstop — size:** living file too large → roll whatever is concluded
- **Manual override:** the human says "archive" at any time
- **Guard:** nothing with open questions or pending verdicts ever rolls; living files always contain every undecided item
- Archive writes are **bulk and rare** (one per roll), never per item; git history is the ultimate safety net; living files carry pointers into the archive

---

## Progress Persistence (Save / Resume)

**Save** (triggered by "save progress / wrap up / switching environment", or session end):
1. Update `session-log.md` (status %, completed work, pending items, habit notes, implicit consensus)
2. Prune (archival step, per expiration rule above)
3. `git add -A && git commit` (message: `Update session log for <date>: <key points>`)
4. `git push` (multi-machine sync; the log is the sole basis for resuming)
5. Report: commit hash + next resume point

**Resume** (new session or "continue"):
1. Read living files: `session-log.md` latest section → `question-log.md` open items → `review-report.md` ledger + active proposals
2. Consult `archive/` only on demand (when a living pointer says details live there)
3. Continue per the pending-items list

**Cross-machine note:** generated artifacts are gitignored — re-render after `git pull`; the render script is the source of truth.

---

## Policies & Red Lines

- **Plagiarism red line (hard):** if an official translation exists, never reference, imitate, or copy its wording/structure. All suggestions start from the current translation or are produced independently from the original.
- **Editing red line (hard):** never modify `input/` or `output/` content without explicit permission.
- **Annotation file:** human-written essay, AI read-only.
- **Language policy:** meta layer (rules, workflow, logs, reports, process discussion) in English; artifact layer (the translation) in the work's language; line-by-line discussion may quote source/translation text in the work language.
- **License:** license the translation according to the source text's license; original byproducts (essays, workflow) are yours to license. For small byproduct artifacts published on GitHub: in a gist, clients title it after its first file (alphabetical order) — name the primary file first, let the license file sort last; in a repository, the README acts as the landing page.
- **Methods changes:** workflow documents update only with manual approval.

---

## When to Use

- Literary/creative translation projects (any language pair) where the human translates and the agent polishes/reviews
- Long-form translation needing multiple sessions across machines
- Any translation where decisions must be auditable and resumable from files alone

## When NOT to Use

- One-shot quick translations the human finishes in a single interaction
- Projects where the human wants the agent to produce the entire translation autonomously (this workflow is co-translation by design)
- Simple phrase lookups (use a dictionary; don't build a pipeline)

---

## Keyword Tracker (Perpetual Glossary)

| Term | Definition | IPA | Defined in |
|---|---|---|---|
| base text | the authoritative source text a translation is built on | /beɪs tekst/ | Artifact Model |
| co-translation | human + AI agent producing a translation together, with defined roles | /kəʊ trænzˈleɪʃən/ | Pattern |
| verdict | the translator's decision on a proposal (keep/change/own wording) | /ˈvɜːdɪkt/ | Review Loop |
| Pending Change Ledger | accumulating table of confirmed changes awaiting one final check | /ˈpendɪŋ tʃeɪndʒ ˈledʒə/ | Review Loop |
| living document | the small active-state file loaded every session | /ˈlɪvɪŋ ˈdɒkjʊmənt/ | Knowledge Mgmt |
| archive | concluded content moved off the living files, consulted on demand | /ˈɑːkaɪv/ | Knowledge Mgmt |
| roll / prune | the act of moving concluded content to the archive (log pruning) | /rəʊl / pruːn/ | Knowledge Mgmt |
| semantic reference | an edition consulted only to confirm meaning, never for wording | /sɪˈmæntɪk ˈrefrəns/ | Multi-language |
| register | the level of formality/style of language chosen | /ˈredʒɪstə/ | Policies |
| callback | deliberate repetition of an earlier phrase for effect | /ˈkɔːlbæk/ | Review Loop |
| global best | a rendering must fit the whole work (sentence → paragraph → character → scene → article), not just the quoted fragment | /ˈɡləʊbl best/ | Review Loop |
| story-logic reading | resolving wording doubts via narrative coherence across distant lines before picking words | /ˈstɔːri ˈlɒdʒɪk/ | Review Loop |
| annotation stream | the annotation habit that accompanies every phase, kept in a persistent file | /ˌænəˈteɪʃən striːm/ | Phases |

---

## License (MIT)

```
MIT License

Copyright (c) 2026 Gojob

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
