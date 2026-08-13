# Investigation Report: Co-Translation With AI Agent (2026-08-05)

## 1. Overview & Objectives

**Goal:** consolidate the translator's findings on co-translating with an AI agent into an essay. The raw seed thoughts live in `../My Thoughts on Coauthoring With AI Agent.md` (the translator's file, kept as-is). This report organizes them into a structured skeleton the essay can grow from, and grounds each point with evidence from the case project (translating *Introductory Antimemetics*, qntm, EN→ZH, ~1.5 months, rounds 1-5 of review).

**Draft thesis (tentative):** AI-agent co-translation is not automation that replaces the translator — it is an *environment*: dictionary, peer reviewer, idea housekeeper, and pen — while the human supplies context, taste, and commitment. The workflow (not the model) is the product.

**Thesis (confirmed 2026-08-10, Q2):** "AI co-translation is an environment, not a replacement." The "workflow is the product" tail is dropped — the output includes much more than a workflow, so the thesis must not reduce it to one.

## 2. The Real-Life Baseline — what translation actually needs

The translator's deduction from real life: translating (intensive reading + writing) needs:

1. **A quiet, ordered house** — housekeeping done, dishes washed; the fewer real-life interruptions, the better. Working with AI agent really helps you enter this mindflow, because you are describing ideas to agent, what you do is to keep your idea flowing.
2. **A discussion peer** — a friend, a peer, an editor. Translation differs from personal writing: there is a base text to follow → guesswork → cross-examination and validation. (Map: the question-log ↔ review-report loop with the agent as the cross-examining peer.)
3. **An idea-housekeeper** — like the Karpathy LLM Wiki doing housekeeping, but for ideas and writings instead of dishes. (Map: annotation essay → extraction into background/question-log; the investigation-index keeps every line of research findable.)
4. **A dictionary** — glossaries you don't know, ambiguous context needing clarification; an agent dictionary is highly customizable (ask for meaning, pronunciation, IPA, register — not just a fixed entry).
5. **Paper and pen — cheap, abundant** — Obsidian as the paper (markdown, readable, organizable); **OpenCode + DeepSeek as the pen**: open-source, easy to obtain, no content lock-in; DeepSeek open-sourced with a price advantage (off-hours discounts). Tools are swappable by choice — customization again.

**Keyword: customization.** Three of the five needs converge on it: the dictionary, the pen, and the workflow itself are all configurable.

## 3. Translation as an Engineering Project

- **I/O model**: input = raw text + human annotation; output = translated text; byproducts = knowledge, workflow, ideas for new stories (this project's byproducts: background.md knowledge base, the four-phase workflow, and the writing-craft vocabulary in the Glossary Tracker).
- **Ideas and routines are capturable**: when the mind is messed up with ideas, write them down; workflows and routines can be described by words, therefore written down; iterate, adjust, experiment with different ways of working.
- **"It's like polishing code"**: this project's evidence — the four-phase workflow itself was iterated (rounds 1-5, the three-file split 2026-08-04, the batch verdict protocol 2026-08-05, the Pending Change Ledger). Rules got generalized (editing red line, language policy) exactly like refactors.
- **Consequences of the engineering view**: version control (git) becomes natural; diffs are reviewable; decisions are auditable; a translation project can be resumed from logs alone (no conversation history needed — the session resume workflow).

## 4. The Value of the Human (what the agent cannot supply)

1. **Huge pre-linked context** — automatically linked for the subject the translator is interested in and familiar with (reading the whole series, knowing the SCP wiki, the spider foreshadowing — context the agent must be *told*, the translator already has).
2. **Real-life experience, feeling, emotion — the indescribable** — the AI can find a *description* for it, but it is always off by a bit; only the translator can express their own experience. It's the uniqueness. (Evidence: the annotation essay — machine-room associations, Spectre/Meltdown memories, 打针前 dread — every one of the project's best touches traced to a translator memory.)
3. **"The common tongue"** — how people talk, how people in a certain environment do things; mostly *experienced*, not learnt; the subtleties that make people people. (Evidence: every 口语化 verdict — 我爸 vs 父亲, 要命 vs 见鬼 — was decided by the translator's native ear, not by the agent's option lists.)
4. **Passion and commitment — the doujin culture** — willingness to stick to the end; fan-translation culture (doujinshi) as the engine that pays in love, not money. (Evidence: the project's unpaid labor across months, and the publishing-strategy investigation showing the love-driven path into the industry.)

**The division of labor, one line**: agent = housekeeping, cross-examination, dictionary, pen, memory; human = context, feeling, ear for the common tongue, commitment.

## 5. Grounding — the case project's concrete evidence (for the essay's examples)

| Agent role       | Case evidence                                                                                                                                                                                                     |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Peer/editor      | review-report appendices: options + rationale + editor notes; verdict flow (translator decides, agent records)                                                                                                    |
| Dictionary       | 术语考证 tables (20+ entries with IPA); multi-language semantic verification (11 languages); Glossary Tracker                                                                                                         |
| Idea housekeeper | annotation.md → background.md extraction; question-log (66 questions across 5 rounds); investigation-index (5 active lines)                                                                                       |
| Pen              | four-phase workflow; 底本 decisions; red lines (plagiarism, edit-permission)                                                                                                                                        |
| Memory           | session-log resume workflow — full state restored from files alone after machine switches. Since translation is so text oriented, everything can be expressed in text, and ai agent can keep its history as text. |

## 6. Essay decisions (open — see question log)

Thesis sharpening, audience, language, length, publication venue (Rednote / Github), how much case evidence to expose, whether to include the Translation Direction Matrix diagram. Also: whether the essay should include a "how to set this up" practical section (toolchain: Obsidian + opencode + DeepSeek + git).

### 6.1 Three-layer design (proposal, 2026-08-10)

**Framing: one body of ideas, two renderings for different clients.** The investigation's content is a single conceptual core; the two essays are renderings of that core, not separate idea sets. The failure mode to avoid: the same ideas drifting in two copies (the workflow doc once drifted from practice; a human essay maintaining its own phase descriptions would drift the same way).

```
conceptual core (this report)          ← single source of truth for ideas
   ├── agent rendering                 ← artifacts/translation-workflow.md (rules, English, imperative)
   └── human rendering                 ← the essay (principles, Chinese, narrative) — not yet built
```

- **The report is the core**: organized facts + grounded evidence. Rule: ideas live here; both essays *derive* from it; changes land in the report, then propagate to renderings.
- **Agent rendering** = interface of executable rules: "do X when Y" (imperative, second-person), project-agnostic, versioned by git. Status: v2 (synced 2026-08-10).
- **Human rendering** = interface of insight: "this is why translation needs X" (declarative, first-person), abstract like llm-wiki, storytelling with case color. Raw material: seed thoughts + this report. Not yet built.

| | Agent essay | Human essay |
|---|---|---|
| Carries | the model (roles, phases, red lines) | the *meaning* (why, felt experience, doujin culture) |
| Voice | imperative rules | narrative insight |
| Language | English | Chinese (Rednote) |
| Abstraction | executable specifics | general direction |
| Update cadence | lives, iterates (git log tracks) | snapshot, published once |
| Role in pair | what you hand the agent | what you hand the reader (llm-wiki model: idea first, agent builds specifics) |

**Development order:** ① resolve open decisions (question log Q2-7: thesis, audience, length, case exposure) → ② freeze the core in the report → ③ human essay: structure from report skeleton → draft → iterate via the question-log loop (translator-owned, like the annotation essay) → ④ anti-drift rule: workflow changes go to the agent doc; the essay stays a snapshot.

### 6.2 Essay decisions — verdicts (2026-08-10)

| Q | Decision | Verdict |
|---|---|---|
| Q2 | Thesis | **"AI co-translation is an environment, not a replacement"** — drop the "workflow is the product" tail; the product is much more than a workflow. |
| Q3 | Audience | **Both communities.** Non-technical readers must be able to follow → use real-life everyday examples explicitly to nail the connection. Publication twofold: Rednote first (hobby / traffic), then Github (serious work, community contribution, career proof). |
| Q4 | Language | **English first** — software-engineering ideas are expressed in English, and the agent essay must be English for high compilability. Translator writes the Chinese version personally after the idea core is polished in English. |
| Q5 | Length | No hard limit (Rednote supports ~10k chars/post). Principle governs: tell human readers a story vs show the agent executable rules. |
| Q6 | Case exposure | **Everything in the project is usable** (the whole project will be open-sourced) — but don't overwhelm readers with examples. |
| Q7 | Setup section | **Brief mention only** — give readers freedom of instantiation (their own tool choices), not a prescribed stack. |
| Q8 | Structure | Polish the report first, then discuss rendering. |
| Q9 | Publish timing | **Don't wait for ThinKingDom** — proceed on our own. |

**Open decisions remaining:** ~~Q10 (closed — global best already covered in the workflow)~~, ~~Phase-1 Q1 (three-layer design approved 2026-08-10)~~, ~~translation-workflow Q1-4 (Gojob/agnostic/English applied; three-bucket structure implemented 2026-08-11)~~.

### 6.3 Essay outline — approved (2026-08-11)

**Working title:** *AI Co-Translation Is an Environment, Not a Replacement*

| # | Section | Content |
|---|---|---|
| 1 | Hook — what translating actually needs | Everyday start: quiet house, a discussion peer, a dictionary, paper and pen. Translation = guesswork against a base text; nobody does it alone. |
| 2 | The agent as environment | Each real-life need maps to an agent role: peer (cross-examiner), idea housekeeper (annotations → question log), customizable dictionary (IPA, register, multi-language), pen (Obsidian + opencode + DeepSeek). Keyword: customization. |
| 3 | Translation as an engineering project | Input / output / by-product; ideas and routines capturable; iterate like polishing code; version control, auditable decisions, resume from files alone. |
| 4 | The value of the human | Agent can't supply: pre-linked context, lived feeling ("off by a bit" descriptions), the common tongue, commitment / doujin culture. Division of labor: agent = housekeeping/cross-examination/dictionary/pen/memory; human = context/feeling/ear/commitment. |
| 5 | Freedom of instantiation | Brief: tools swappable, choices yours (Obsidian, opencode, DeepSeek, git), costs incl. off-hours discounts — a paragraph, not a tutorial. |
| 6 | Close — environment, not replacement | Thesis lands: the agent surrounds the translator; only the translator stands in the middle. |

**Outline verdicts (question log Phase 2, 2026-08-11):**
- Structure approved as-is.
- **Standalone essay**: readers may not know the case project → every case example gets a brief explainer of what it does; examples are not limited to the Antimemetics project.
- **Case evidence in English only.**
- **Translator-written**: the essay is the translator's own writing (like the annotation essay) — writing is a different craft from translating, the writer's identity is not the translator's, and in writing form and ideas are equally important. Agent draft v0.1 (`artifacts/co-translation-essay.md`) is demoted to reference material: idea core, examples, structure bank.

### 6.4 The creative-writing line (2026-08-11)

The project is drifting from translation toward creative writing: the human essay turns the translator into a *writer*, a different identity with a different craft (in writing, form and ideas are equally important). Anticipated: a separate `creative-writing-workflow` diverging from `translation-workflow`, possibly in the same repo — it's all reading and writing anyway.

**Verdict (question log Q12):** the current goal stands — consolidate the translation work and finish the essay. Creative-writing thoughts are parked in this investigation; when this line concludes (or diverges too much), start a separate investigation for the creative-writing line.

### 6.5 Publication & licensing (Phase 3, 2026-08-11)

**Q1 — which license for the two articles.** Discussion:

- **Essay (human-oriented):** CC BY 4.0 — literary/non-fiction piece, written personally; the translator's instinct, agreed.
- **Workflow (agent-oriented):** three candidates:
  - **CC BY 4.0** (recommended) — uniform with the essay; any use with attribution; readers can copy it into their own AGENTS.md/skills freely.
  - **MIT** — code-ecosystem native (most skill packs are MIT); attribution optional in practice; maximum adoption.
  - **CC BY-SA 4.0** — share-alike: derivatives must stay under the same license; protects lineage but burdens adapters — usually the wrong fit for a workflow doc.
- **Constraints:** the workflow and essay are original content → free license choice; the fiction translation must stay CC BY-SA (wiki-derived text). Methods/ideas are not copyrightable — a license covers the expression, and practically enforces attribution.

**Q1.1 — what are "copyrightable" and "attribution"? (translator new to copyright law):**

- **Copyrightable** — whether a work qualifies for copyright protection. Copyright protects the *expression* — the specific words, structure, and arrangement — never the underlying idea, method, or facts. The workflow's *text* is copyrightable; the *method* it describes (question loop, verdicts, living docs) is not — anyone may use the method and write their own doc. Copyright arises automatically at creation (no registration), grants exclusive rights (copy/distribute/adapt), and lasts author's life + ~70 years. A license is how the author grants others permission to use those rights — default is "all rights reserved". Original content (essay, workflow) = free choice; a translation is a *derivative work* of its source, so its license is constrained by the source's (here: CC BY-SA from the wiki).
- **Attribution** — giving credit: naming the author and the source when using the licensed work (author name, title, link, license notice). CC BY's only condition is attribution — reuse, remix, and commercial use are all allowed as long as credit is given (practically: "«Translate with AI Agent» by Gojob, CC BY 4.0" + link — exactly the card footer already rendered). Attribution is the main enforceable point of CC BY and the currency of the system (no royalties involved); MIT makes credit optional in practice.

**Q1.1.2 — mixing licenses: CC BY 4.0 (essay) + MIT (workflow)?** The translator's intent: the workflow is about conveying the idea and letting end users adapt as they wish — no attribution burden; the essay is personal writing where form and idea are both important.

- **What CC BY buys over MIT, practically:** only attribution — users must credit you. Both permit commercial use, modification, redistribution; neither is share-alike. So CC BY's value is name recognition/discoverability; without the credit requirement, MIT is strictly more adoption-friendly.
- **Same gist, two licenses:** legally fine (licensing is per-file), but gists are usually consumed as single-licensed units — mixed licenses invite confusion and need per-file notices.
- **Separate gists:** cleanest — one license per gist, one LICENSE file each, two links. (MIT's only residual duty: the copyright notice stays inside the file when redistributed — not a prominent credit.)

**Verdict: pending** — leaning CC BY 4.0 (essay gist, as-is) + MIT (workflow, separate home/gist). Also recorded as a process rule (question log Q1.1.1): **the question log is translator-owned — never edit it unless explicitly asked; agent answers live in the report.**

**Q1.1.2.1 — what is the MIT license?** One of the most permissive open-source licenses (originated at MIT, 1980s, via the X11/X Consortium license). Plain terms: anyone may use, copy, modify, merge, publish, distribute, sublicense, and sell the work — including commercially — for free, forever, provided all copies or substantial portions carry the original copyright and permission notice. No copyleft: derivatives may be re-licensed any way (even closed-source). No warranty, no liability ("as is"). Practically: the notice requirement lives *inside* the copy (file header or LICENSE file) — no prominent credit, no registration, no payment, no permission needed.

**Q1.1.2.2 — using a MIT-licensed skill in one's own project.** Yes — copy-paste is exactly what MIT permits. Obligations: ① keep the original copyright notice + license text with the copied material (header comment in the file, or a LICENSE/NOTICE file for extracted parts); ② don't claim sole authorship of the unmodified MIT work (the notice preserves the original author's name) — you may add your own copyright line for your modifications; ③ if you rewrite it fully, it becomes your own new work (keeping the notice remains good practice). No need to ask permission, register, pay, credit prominently, or publish your changes. Mirror case: licensing your own workflow under MIT grants everyone exactly these same freedoms.

**Q1.1.2.2.1 — separate LICENSE file vs license embedded in the article?** Both patterns exist; convention depends on the artifact:

- **Code / repos:** separate `LICENSE` file at the root is the overwhelming convention (GitHub displays it, tooling reads it).
- **Standalone documents / articles:** the *embedded notice* is the practical norm — a footer/header line ("«Title» by Gojob, CC BY 4.0" + link). Reason: the article file travels alone (copied, shared, re-hosted); a separate LICENSE file is the first thing lost when the article is copied by itself. The essay gist already does this (footer notice + separate LICENSE = belt and suspenders).
- **MIT specifically:** the full license text must accompany copies or substantial portions — either embedded at the file end or shipped as a sibling LICENSE file. **CC BY 4.0 specifically:** a one-line attribution notice suffices; linking to the license deed is standard (no need to embed the legal code).
- **Recommended pattern:** notice line embedded in the article (travels with the file) + LICENSE file in the gist/repo (machine-readable).

**Q1.1.2.2.1.1 — traceability, license-file content, stale links.** Three parts:

1. **The model is exactly right:** embedded line stays with the article as it spreads; users trace back to the canonical terms via the link. That is how CC licenses are designed — the deed URL is the standard pointer, and attribution survives because it's baked into the file.
2. **Content vs type:** what identifies the legal terms is the *license identifier* (type + version), not the file. For **CC BY 4.0**, the deed URL (creativecommons.org/licenses/by/4.0/) *is* the license reference — a line + link suffices completely; the LICENSE file is a convenience copy of the standard text. For **MIT**, there is no canonical URL — "MIT" alone is only near-unambiguous; the full standard text should ride along (embedded or as LICENSE file). General rule: the file must be a verbatim copy of the standard text; the identifier is what binds the terms.
3. **Stale links / changed content:** CC deed URLs are permanent and version-locked (4.0 fixed at publication — cannot be retroactively changed); MIT has no URL but a stable, fixed historical text. If a link dies, the identifier still resolves the terms. If the LICENSE file's content later diverges, the binding terms remain those declared at publication (the embedded identifier) — but keeping the file verbatim avoids disputes. A future re-license by the author would apply to new copies, not already-distributed ones.

**Q2 — linking between differently-licensed own works (CC BY 4.0 essay → MIT workflow).** Yes, unconditionally: a hyperlink is not "use" of the licensed work in the copyright sense, and as the author of both you may do so regardless. Licenses govern each file separately — linking neither merges the works nor changes either license. Practical notes: keep each artifact's own license notice visible at its destination (no confusion about which terms govern what); don't *embed* one into the other without carrying its notice (embedding the MIT workflow text into the essay would make that copy part of the CC BY 4.0 work — legal for the author, but per-file notices keep it unambiguous for third parties).

### 6.6 Workflow file restructure (question log translation-workflow Q1-4, 2026-08-11)

**Q1 — lead with goal and the human-in-the-loop framing.** The current file opens directly with the Pattern. Restructure to open with: (a) one-paragraph identity — co-translation: the human translates, the agent is the environment (dictionary / peer / housekeeper / pen / memory); (b) the division-of-labor one-liner; (c) an explicit banner that this workflow differs from most skills — **intensive human intervention required; the agent never produces the translation alone; the human is the engine**. Then: pattern → artifact model → phases → loop details → knowledge management → save/resume → red lines.

**Q1.1 — setup/hook section (proposal).** New "Getting started" section after the identity: ① the agent reads this file first (it is the procedure source of truth); ② the human asks "what do I do / where do we start"; ③ the agent answers with a plan derived from the phases — current position + next action (e.g. "Phase 1: draft chapter 1; I'm your dictionary on call"); ④ they progress together, the question loop driving. Effect: the workflow becomes executable — "where are we" is answered from the doc + session logs, with no conversation history needed.

**Q2 — two versions (proposed split).**
- `artifacts/translation-workflow.md` → **private version** (current file): adapted to this project, records choices/habits — three-bucket with Research/ at root, omnibus chapter, Rednote publication detail, CC BY-SA notes, Antimemetics provenance.
- **public version** (new file, e.g. `artifacts/translation-workflow.public.md` or under `publish/`): project-agnostic, MIT, destined for the gist.
- **Anti-drift rule:** private is the source of truth; changes land there first, then propagate to the public version (same rule as report → renderings).

**Q3 — public version droppables (agreed, one nuance each):**
- **Meta data** (status / created / extracted-from / owner): drop.
- **CC BY-SA**: don't hardcode a license; generalize to "match the source text's license; original byproducts are yours to license".
- **Research/ at root**: fold into `by-product/` — the public workflow assumes one fiction per repo; multi-fiction hosting is a private-repo choice.
- **Omnibus / collected edition chapter**: drop the chapter; keep the concept in one line under multi-language verification ("reference editions: semantics only") — already captured by the *semantic reference* glossary entry.

**Q4 — phases: participants, input, output per step.** Restructure the phase list into per-phase blocks. **Q4.3** — each block names the doer per sub-activity (who reads, who extracts, who proposes, who decides), not just "Human + Agent".

**Q4.4 — annotation is a stream, not a phase (translator's leaning).** Agreed: annotation grows incrementally through the whole project (in this project it started as draft-time marks and only concluded with the 译后记). Restructure the model: **annotation accompanies every phase** — draft-time notes, polishing marginalia, review-time reflections — kept in a persistent file, referable back at any time. Modularity (annotation and draft as separate files) stays a freedom of instantiation for the translator; in practice the two are produced together — "annotate as you read / draft". The hard requirement: both stay persistent files.

**Q4.5 — the translator's envisioned phase model (idealized from practice, trial-and-error removed).** Seven steps, adopted as the model to encode (differs from the project's actual history only in cleanups):

| # | Phase | Who does what |
|---|---|---|
| 0 | **Discovery** | Human: finds the text interesting, makes notes, looks up words, forms a draft/doodle (on the base text or separately) |
| 1 | **Draft & annotation** | Human translates, produces the first draft; annotation grows alongside (agent on call as dictionary) |
| 2 | **Worldview alignment** | Agent reads base text + draft, extracts from annotations/reference, asks the human about worldview and critical background; human answers |
| 3 | **Line-by-line polishing** | Agent + human contemplate each line until natural; agent proposes candidates/perspectives, human decides |
| 4 | **Coherence re-read** | Both re-read the whole work, update annotations (deep polishing exposes missing links), find inconsistencies, suggest better coherence |
| 5 | **Lint** | Agent: mechanical check (grammar, punctuation, formatting, symbol handling, term/name consistency) |
| 6 | **Publication** | Agent + human prepare the publish copy, license, repo/gist |

Notes: Phase 4+5 split the current "Full review" into substantive coherence (both) and mechanical lint (agent) — matching how the project actually ran (verdict batches vs quote/format fixes). Phase 0 is new and covers how a project starts — connects to the hook section.

**Verdicts (question log translation-workflow Q5, 2026-08-11 — all approved):**

| #   | Decision          | Verdict                                                                                                                                                    |
| --- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| V1  | Workflow license  | **Separate MIT gist** (workflow); essay stays CC BY 4.0                                                                                                    |
| V2  | Top structure     | **Goal-first + human-in-the-loop banner**                                                                                                                  |
| V3  | Hook section      | **Add**                                                                                                                                                    |
| V4  | Two-version split | **Split**; public file = `translation-workflow-public.md` (avoid `.public` reading as a file extension)                                                    |
| V5  | Public droppables | **Drop all 4** + sweep for other project-agnostic violations (Crom API, Afterwords Selection, wikidot artifacts, Antimemetics numbers, base-text examples) |
| V6  | Phase model       | **7-step** (Discovery → Draft&annotation → Worldview → Polish → Coherence re-read → Lint → Publication) + annotation-as-stream                             |
| V7  | Publication       | **Condense** even in private; public = GitHub only                                                                                                         |
| V8  | License placement | **Embedded MIT notice + LICENSE file in the gist**                                                                                                         |

### 6.7 Wrap-up: keep licensing/publication integrated (2026-08-11)

**Q (question log Phase 3 Q3):** extract licensing/publication into its own line, or keep it in this investigation?

**Verdict: keep integrated.** The 7-step workflow is end-to-end by design (Discovery → … → Publication) — licensing belongs to Phase 6 + red lines, and the essay's arc is "first reading to published work". Knowledge is already filed where used (§6.5 licensing primer/verdicts; public workflow's generalized license rule). Publication questions are grounded in this project's concrete artifacts (essay gist, workflow gist, card footer), not diverging — the Q12 split criterion doesn't fire. The next planned divergence is creative writing, which inherits this licensing knowledge when it starts.

**Extraction criterion (future):** when publishing becomes a portfolio concern (multiple works, licenses per artifact), seed a separate publication/licensing line.

**Next step:** translator writes the human-oriented essay in Chinese; agent feedback to come in a new session.

### 6.8 信、达、雅——中国古典翻译标准（问题日志 Q11，2026-08-12）

译者撰写随笔中文版时提出的背景知识问题。

**出处：** 严复（1854-1921），1898 年《天演论》（赫胥黎《Evolution and Ethics and Other Essays》的译本）序言《译例言》：

- **信 xìn** —— 忠实：忠实于原文的意义与内容。
- **达 dá** —— 通达：信息传递到位；译文在目标语言中清晰自然、读得通（达 = 到达、通达）。
- **雅 yǎ** —— 雅正：文辞优雅。对严复而言特指秦汉以前的古文（汉以前字法句法）——即使在当时也已是古语。

**所引文句：**

> 译事三难：信、达、雅。求其信已大难矣，顾信矣不达，虽译犹不译也，则达尚焉。

= "翻译有三件难事：信、达、雅。要做到'信'已经很难了；但如果'信'而'不达'，那么虽然译了，也等于没译——所以在二者之间，'达'应当被放在前面（尚 = 崇尚、推崇）。"

论证链条：信是最难的底线 → 但信而不达，翻译就失去了目的（沟通）→ 因此二者之中达优先。完整序言补全了三元组："信达而外，求其尔雅"——在信与达之外，再追求雅——并以经典为依据（《易》：修辞立诚；孔子：辞达而已；言之无文，行之不远），称这三者为一切文章的正轨，也是翻译的楷模。同一篇序言里还有那句著名的"一名之立，旬月踟蹰"——为一个术语定名，竟踌躇十天到一个月。

**值得注意的细节：**

- **理论与实践脱节：** 严复自己的《天演论》以"不忠实"著称——删节、改写、掺入自己的议论。实践中"雅"压倒了"信"。
- **"雅"备受争议：** 从鲁迅起，批评者反对把翻译拴死在古文语域上；后继者重新定义目标——鲁迅"宁信而不顺"、钱锺书"化境"、傅雷"神似"、许渊冲"三美"（音美/形美/意美）。如今"信达雅"作为通用简写留存：忠实 / 通顺 / 优雅——"达"读作"中文读得自然"，"雅"读作"语域与品味"，而非拟古。
- **现代层级：** 信 = 底线（意义忠实）；达 = 不可妥协（读不懂的译文就是失败）；雅 = 天花板（风格/语域）。

**与本项目的对应（可写进随笔）：**

- **信** ↔ 忠实性工作：多语言语义核验、字面义/联想义核查、语义偏移裁决——智能体是"信"最强的核查者（对照底本的交叉盘问）。
- **达** ↔ 口语化裁决（我爸 vs 父亲，见鬼 vs 要命）：智能体给候选，译者的母语耳朵定夺。
- **雅** ↔ 语域选择（文件部分的公文腔、金的"收工"、"薄薄一层厚玻璃"的矛盾修辞）——人的品味。"雅" = 语域，不是拟古。
- **与主题共鸣：** "AI 是环境，不是替代"恰好对应信达雅——智能体负责核验"信"、生成"达"的候选；"雅"仍然靠人的耳朵（同 §4 的"总是差一点"论证）。另外"一名之立，旬月踟蹰"——本项目 20+ 条带音标的术语考证表，就是现代版的智能体辅助劳动。

### 6.9 生僻字/指定字词术语追踪表（2026-08-12）

> 记录译者在写作中遇到的生僻字，或主动要求查证的字词（随问随增，与 §6.8 等章节同步成长）。
> 姊妹表：审校报告 Appendix 8（小说译文的难读写词汇）；此表服务随笔/报告写作语境——如重复出现，按需合并。

| 字词 | 释义（中文） | 拼音 | 英译 |
|---|---|---|---|
| 踟蹰 | 徘徊不前，犹豫不决 | chí chú | to hesitate / to waver |

### 6.10 随笔中文版初稿 lint 报告（2026-08-13）

> 对 `artifacts/与人工智能体一起翻译.md`（127 行，定稿）的语法/标点/事实核查。译者手工修复。无严重（severe）问题。行号基于当前稿，修复时行号会漂移，请按内容定位。

**事实核查（中，发布前必查）：**

| 行 | 现状 | 问题 | 建议 |
|---|---|---|---|
| L5 | 原文于2008年起在社区连载 | 本系列（逆模因部）约2019年起连载；2008 更可能是作者入驻社区/作者页的时间 | 核实具体年份（建议改为 2019 年左右），另"于…起"冗余，可改"自2019年起" |
| L12 | 第一次读的时候还在念书，差不多是10年前 | 10年前≈2016，早于本系列（2019+） | 核实真实初读时间/作品（或读者通过 qntm 其他作品初识） |

**语法/用词（中）：**

| 行 | 现状 | 建议 |
|---|---|---|
| L50, L52 | 引号方向错误：`”自然语言“`、`”猜对“`、`”原文这里是什么意思呢？"` 等 5+ 处，开引号用了右引号 `”` | 全部改为 `“…"` 成对（其余行引号方向均正确，此两行为输入习惯所致） |
| L52 | 抓紧**把他们**写下来 | 想法是物：**它们** |
| L52 | 想法**来的**快，**去的**也快 | 来得快，去得也快（补"得"） |
| L91 | 不再**赘诉** | 赘述（错别字） |
| L50 | 需要核对、交叉检验、第三方意见等手段**辅佐进行** | 辅佐（辅佐君主/上级）误用：借助核对、交叉检验、第三方意见等手段 |
| L10 | （又一次）**面对自己提问** | 问自己 / 对自己提问 |
| L83 | 让我对整个工程**有一个建模** | "建模"是动词：让我能对整个工程建模（或"建立一个整体概念"） |
| L3 | 能够在**跨越数年的每一次重读中**都吸引我 | 语序生硬：在跨越数年的时光里，每一次重读都能吸引我 |
| L46 | …说话方式（“师爷，给翻译翻译”） | 句末缺句号 |

**标点/格式（低）：**

| 行 | 现状 | 建议 |
|---|---|---|
| L8 | 感兴趣 。 | 句号前有多余空格（半角） |
| L10 | `]`） （*How to Read a Book*） | 链接与括号之间多余空格 |
| L3 | “信”，“达” | 引号间顿号/不用逗号：“信”“达” |
| L46 | 深度的阅读，思考和写作 | 顿号：阅读、思考和写作 |
| L50 | 朋友、网友、同事、或者编辑 | 顿号列表"或者"前不加逗号：同事或者编辑 |
| L99 | 规则明确，评价维度清晰，结果可度量 | 并列定语用顿号 |
| L125-127 | 参考引用格式不统一（` - ` 与 `：` 混用、URL 前有空格） | 统一格式，URL 用 markdown 链接 |

**措辞（低，可改可不改）：**

| 行 | 现状 | 建议 |
|---|---|---|
| L3 | 翻译了一则小说 | 一篇小说（"则"多用于新闻/短篇） |
| L15 | 将与受害者相关的信息**与世隔绝** | 隔绝于世（与世隔绝多用于人） |
| L16 | 在一个会话**专注**干一件事情 | 在一个会话**中** |
| L18 | 提供的信息很多，很快 | 又多又快 |
| L18 | 限制成一个问题一个问题的交流 | 一次只交流一个问题 |
| L33 | 一定程度地保持了身心健康 | 一定程度上 |
| L35 | 开展翻译工作过程中的经验与发现 | 开展翻译工作的过程中的经验与发现 |
| L41 | 并非文学、翻译、哲学、历史、AI研究专业 | 并非……专业出身 |
| L48 | 抛开爆炸的科技 | 日新月异/爆炸式发展的科技 |
| L52 | 翻译还是猜想 | 翻译说到底是一种猜想 |
| L56 | 带入上文的框架 | 代入 |
| L80 | 特别（也许是）对于文科生而言 | 尤其是对文科生而言 |
| L95 | 结论有些不可证伪 | 难以证伪/无法证伪 |
| L97 | 最有可能发生的答案 | 最有可能的答案 |
| L101 | 新人培训会讲一些参考材料 | 易歧义（培训会/培训 会）：新人的培训会讲一些参考材料 |
| L104 | 翻译只读原文是不够的 | 翻译时只读原文是不够的 / 对翻译而言 |
| L105 | 而人工智能体是很难通过推导发现的 | 缺主语：而这些东西人工智能体很难通过推导发现 |
| L119 | 单独拉起一条调查 | 单独开展一项调查 |

**风格备注（主观，保留与否都行）：**
- L65 "动力装甲软件"比喻有趣，括注已自解释，可保留。
- L105 "俺寻思之力"（战锤梗）——若面向小红书非读者群体，可加一行括注。

#### 6.10.1 第二轮复查（2026-08-13，译者已手工修复后）

**事实核查 — 撤回第一轮两条（译者修正正确）：** 作者页（qntm-s-author-page）白纸黑字：`2015-04-12 - Introductory Antimemetics`、`2015-01-31 - We Need To Talk About Fifty-Five`、`2015-02-01 - qntm's author page`——系列确实自2015年起在社区连载；"10年前"（2016 前后首次阅读）也成立。第一轮两条"事实核查"是我误判，撤回。

**已修复 ✓（对照 §6.10）：** L50 辅佐→借助、L52 它们/来得快、L91 赘述、L10 对自己提问、L46 句号（师爷，给翻译翻译。）、L8 空格、L10 空格、L3 一篇、L15 隔绝于世、L16 会话中、L18 又多又快/一次只交流一个问题、L33 一定程度上、L35 重写、L41 专业出身、L50 同事或者编辑、L52 猜想句、L56 代入、L80 尤其是、L95 难以证伪、L97 答案、L99 顿号、L101 入职培训重写、L104 对翻译而言、L119 展开、参考引用新增《如何阅读一本书》与 Obsidian 两条。

**未改（译者有意保留，待确认理由）：**

| 行 | 现状 | 我原建议 | 疑问 |
|---|---|---|---|
| L50, L52 | 引号方向 `”…"` 5+ 处 | 改为 `“…"` | 全文其它引号方向均正确，仅这两行反向——发布前请确认是否有意（如 IME 习惯可统一替换） |
| L83 | 有一个建模 | 让我能对整个工程建模 | 保留理由？ |
| L3 | 跨越数年的每一次重读中都吸引我 | 在跨越数年的时光里，每一次重读都能吸引我 | 保留理由？ |
| L3 | “信”，“达” | “信”“达”（顿号/无逗号） | 保留理由？ |
| L48 | 爆炸的科技 | 日新月异/爆炸式发展 | 若为"科技爆炸"双关可保留 |
| L46 | 深度的阅读，思考和写作 | 阅读、思考和写作（顿号） | 保留理由？ |

**新发现（本轮）：**

| 行 | 现状 | 建议 |
|---|---|---|
| L105 | 文章的一些细微之处**可以被人类译者能**敏锐地感觉到 | 双重能愿动词"可以…能"——去掉其一：可以被人类译者敏锐地感觉到 / 人类译者能敏锐地感觉到（后半句"而人工智能体很难通过推导发现"已修好） |

**参考引用（仍有遗漏）：** L5 正文链接了社区作者页（scp-wiki.qntm-s-author-page），参考引用未收录；另外 L125-127 为裸 URL + "： " 格式，L128-129 为 markdown 链接，两种格式并存，建议统一。

#### 6.10.2 译者裁决 + 引号订正 + 参考引用格式建议（2026-08-13）

**裁决记录（question log「personal essay」#1-8）：**

| # | 事项 | 裁决 |
|---|---|---|
| 1 | L50/52 引号方向 | 确认是错误 → **AI 直接订正**（5 处反向引号已修复；起因：Obsidian 微软雅黑下引号方向不明显，已记入用户习惯） |
| 2 | L83 有一个建模 | 保留。"建模"兼顾名词（建立的模型）与动词（建模这个行为）；此处强调动作本身作为名词——行为比结果更值得写 |
| 3 | L3 跨越数年的每一次重读 | 保留。希望一口气读完、不断句、更紧凑；"时光"太抒情 |
| 4 | L3 "信"，"达" | 保留。逗号分隔三个评价维度（信/达/雅），逐维评估 |
| 5 | L48 爆炸的科技 | 保留。确认含"科技爆炸"双关 |
| 6 | L46 阅读，思考 | **待改（唯一一处）**：并列三项用顿号 → "深度的阅读、思考和写作" |
| 7 | L105 可以…能 | 已由译者修改 ✓（"可以被人类译者敏锐地感觉到"） |
| 8 | 参考引用 | 已补社区连载链接（选用 scp-wiki-cn 中文版作者页）、统一为 Obsidian markdown 链接格式；格式规范见下 |

**参考引用格式建议（#8 答复）：** 学术通行做法（GB/T 7714-2015 电子资源条目）为 `作者. 题名[EB/OL]. (出版/更新日期)[引用日期]. URL.` —— 随笔可以简化，但建议四要素齐全且全篇一致：**作者 - 题名 - 日期 - URL**。按此补齐的条目（日期如不确定可留空）：

- qntm. 个人网站[EB/OL]. https://qntm.org/
- qntm. 逆模因学入门（社区连载，作者页：qntm的人事档案）[EB/OL]. 2015-04-12. https://scp-wiki-cn.wikidot.com/qntm-s-author-page
- Andrej Karpathy. 使用大语言模型构建个人知识库（Karpathy LLM Wiki）[EB/OL]. https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- Gojob. 与人工智能体共事的翻译工作流[EB/OL]. 2026-08-11. https://gist.github.com/Gojob2987/c60efcef24b47e18b1c9bdabf12d4381
- Mortimer J. Adler. 如何阅读一本书（How to Read a Book）[EB/OL]. 1940. https://en.wikipedia.org/wiki/How_to_Read_a_Book
- Obsidian（笔记软件）[EB/OL]. https://obsidian.md

**遗留小提醒：** 正文 L5 的社区链接指英文站（scp-wiki.wikidot.com），参考引用指中文站（scp-wiki-cn）——同一内容的两个站点，建议统一（正文链接也换成 CN 版，中文读者更友好）。

**#8.1 答复（[EB/OL] 是什么）：** [EB/OL] 是 GB/T 7714 文献类型标识码——EB = Electronic Bulletin（电子公告），OL = Online（联机），组合起来表示"联机电子公告/网络资源"，用于标注文献载体类型（同类还有 [J]期刊、[M]专著/书、[C]会议、[D]学位论文、[R]报告、[S]标准、[P]专利）。这是学术引文数据库与论文参考文献列表的约定，供检索归类用，**随笔读者完全不需要看到它**。你的直觉正确：**作者 - 题名 - 日期 - URL** 四要素就足够规范了，全篇统一即可。

**#9 同 gist 还是分 gist（2026-08-13，译者问）：** **同 gist 发布**（中文版加入既有英文版 gist `f017a3a9`）。
- 两文同为 CC BY 4.0——§6.5 关于"同 gist 混合许可证易混淆"的顾虑不适用（那是 CC BY 随笔 + MIT 工作流分开的裁决）；一份 LICENSE 覆盖两文。
- 单一 URL 即可回链（译者需求）；文件名锚点（#file-…）可直达各版本。
- 中文文件名（CJK 码点）在 ASCII 之后排序，gist 标题保持 "Translate with AI Agent" 不变。
- 执行：footer 已按英文版格式补进中文版（© 2026 Gojob + CC BY 4.0 + 发布地址 + 英文版锚点链接）；git clone gist → 添加 `与人工智能体一起翻译.md` → push（commit 4ce42c3）。gist 现有 3 文件：license.md / Translate_with_AI_Agent.md / 与人工智能体一起翻译.md。
- 参考引用已由译者按 作者. 题名. 日期. URL. 格式统一（6 条，无 [EB/OL] 后缀）。

### 6.11 Gist 发布形态评估（question log Phase 4 Q1-3，2026-08-13）

**Q1 文件顺序（license → 中文版 → 英文版 → 图片）：** gist 页面按文件名（大小写不敏感）**字母序**展示，无法手动拖动排序。可行手段只有改文件名加序前缀（如 `0-license.md`、`1-与人工智能体一起翻译.md`、`2-Translate_with_AI_Agent.md`、`3-Pasted …png`），代价：正文图片 raw URL、footer 锚点链接全部要跟着改，且"数字前缀"观感不佳——治标不治本。

**Q2 gist 目录（TOC）：** gist 没有目录功能（GitHub 仓库的 README 才有渲染 + 大纲按钮）。gist 单文件平铺展示，没有"首页"概念；硬做只能加一个排在文件列表最前的 index 文件，手工维护链接，体验一般。

**Q3 换仓库（repo）代替 gist：** **推荐——换。** 译者直觉正确：当前用途（两种语言的文章 + 许可证 + 图片，同一个链接下组织展示）已经超出 gist 的适用场景（gist = 单文件代码/脚本片段）。repo 一次性解决三个问题：
- **顺序**：目录/文件名自由组织，无需数字前缀 hack；
- **首页/TOC**：README.md 在仓库根渲染（可双语索引 + 两文链接 + 工作流链接），markdown 文件自带大纲按钮；
- **混合文件**：LICENSE（CC BY 4.0）自动被识别显示在侧栏，图片放 `images/` 用相对路径引用（`![alt](images/x.png)`，repo 里原生渲染，不再需要 gist raw URL hack）。
- 额外好处：star/fork/issue/发布记录齐全；后续若做多语种版本或出版物，仓库可扩展。
- 成本：essay footer 的"发布地址"从 gist URL 改为 repo URL（`github.com/Gojob2987/<repo>`），正文图片改相对路径。gist 刚建一天，没有外部引用，迁移成本几乎为零。
- **保留工作流 gist 不变**（单文件 MIT 技能文档——正是 gist 的本职场景）。
- 提议结构：`Gojob2987/translate-with-ai-agent` 仓库（README.md 双语索引 / LICENSE / 与人工智能体一起翻译.md / Translate_with_AI_Agent.md / images/×3）。
- 待译者裁决：① 是否迁移到 repo；② 仓库名是否用 `translate-with-ai-agent`；③ 旧 gist 删除还是保留。

## 7. Keyword Tracker

| Term | Definition | IPA | Defined in |
|------|-----------|-----|-----------|
| co-translation | human + AI agent producing a translation together, with defined roles | /kəʊ trænzˈleɪʃən/ | §1 |
| base text (底本) | the authoritative source text a translation is built on | /beɪs tekst/ | §2 |
| cross-examination | systematically challenging interpretations against the source text | /krɒs ɪɡˌzæmɪˈneɪʃən/ | §2 |
| corpus | a body of texts used as reference (here: multi-language translations) | /ˈkɔːpəs/ | §2 |
| customization | adapting tools/workflows to the user's needs (the essay's recurring keyword) | /ˌkʌstəmaɪˈzeɪʃən/ | §2 |
| byproduct | knowledge/workflow captured alongside the main output | /ˈbaɪˌprɒdʌkt/ | §3 |
| doujin culture | fan-produced creative works driven by love, not money | /ˈdəʊdʒɪn/ | §4 |
| register | the formality/style level of language (formal/colloquial) | /ˈredʒɪstə/ | §4 |
| I/O model | input-process-output framing of the translation task | /ˌaɪˈəʊ mɒdəl/ | §3 |
| freedom of instantiation | giving readers the freedom to choose their own tools/setup rather than prescribing a stack | /ˈfriːdəm əv ɪnˌstænʃɪˈeɪʃən/ | §6.2 |

## 8. Investigation Change Log

- **2026-08-05** — Initial. Seed thoughts (`My Thoughts on Coauthoring With AI Agent.md`) organized into a report skeleton + question log; index updated. Essay drafting itself remains the translator's work, to be iterated via the question log.
- **2026-08-06** — Phase-3-style conclusion (methodology extraction): **`artifacts/translation-workflow.md`** created — the standardized co-translation workflow distilled from the case project (artifact I/O model, roles, four phases, review loop with batches + Pending Change Ledger, living/archive knowledge management, save/resume, red lines, engineering principles, long-term learning). Written in the investigation-workflow style; changes require the translator's manual approval. Also wired into the project: AGENTS.md (save/resume/prune workflow + archive pointers) and the living-docs restructure of `knowledge/logs/` (question-log 68 lines, review-report 464 lines, session-log 200 lines; 5 archive files in `logs/archive/`).
- **2026-08-10** — Three-layer design (proposal) added as §6.1: conceptual core (report) → agent rendering (translation-workflow.md, synced to v2) + human rendering (essay, to be built). Question log Phase 1 Q1 answered with this framing; translator reviewing.
- **2026-08-10** — Q2-7 verdicts recorded as §6.2: thesis confirmed (environment, not replacement; product tail dropped); audience = both communities with everyday examples; English first (translator writes the Chinese version herself later); no length constraint; full project usable as case evidence (not overwhelming); setup = brief mention (freedom of instantiation); polish report before rendering; don't wait for ThinKingDom.
- **2026-08-11** — Three-bucket restructure implemented in the project (input / output+publish / by-product; Research stays at root); workflow artifact model updated (both copies, byte-identical). Outline for the human essay drafted and approved (§6.3): standalone essay, case examples explained briefly, English-only case evidence.
- **2026-08-11** — Essay drafting begins: agent draft v0.1 written to `artifacts/co-translation-essay.md` (6 sections per §6.3). Verdicts (question log Q11-12): the essay is translator-written, draft demoted to reference material; future creative-writing line recorded as §6.4 — separate workflow and investigation later, current goal unchanged.
- **2026-08-11** — Translator's own essay draft written in person, in progress (not finished): `Translate with AI Agent.md` (investigation root). Opens with a foreword (Antimemetic Division memories, LLM Wiki, story–AI connections), then re-derives the report's structure (what translation needs → agent as environment → engineering project). Pending: sections after §Engineering (human value, freedom of instantiation, close), polish, iteration via question log.
- **2026-08-11** — Essay completed, polished, and published (other session): CC BY 4.0 + LICENSE, gist `f017a3a9...` as canonical link, Rednote card renderer `publish/render_essay_cards.py` (single-post layout, proof-before-batch). File organization: essay → `artifacts/Translate with AI Agent.md`; seed thoughts + agent reference draft → `artifacts/draft/`. Gist title fix: primary file `Translate_with_AI_Agent.md` first (clients title gists after the first file, alphabetical), `license.md` sorts last. Workflow artifact rendered to v2.1: stale `knowledge/reference` path fixed, Phase 5 generalized (CC BY 4.0 for original content, gist naming rule). Translator next: write the Chinese version of the essay personally.
- **2026-08-11** — Phase 3 licensing discussion recorded (§6.5): two-article license options (CC BY 4.0 recommended / MIT / CC BY-SA), Q1.1 primer on copyrightable & attribution (question log), verdict pending.
- **2026-08-11** — Licensing discussion extended (§6.5 Q1.1.2): CC BY vs MIT tradeoff = attribution only; per-gist vs per-file licensing; leaning CC BY 4.0 (essay) + MIT (workflow) in separate gists, verdict pending. Process rule (Q1.1.1): question log is translator-owned — agent never edits it; answers live in the report.
- **2026-08-11** — Licensing primer extended (§6.5 Q1.1.2.1-2): MIT license explained (permissive, notice-inside-copy, no copyleft); using MIT skills in own projects (copy-paste OK, keep notice, add own copyright line for modifications).
- **2026-08-11** — Licensing primer extended (§6.5 Q1.1.2.2.1): separate LICENSE file vs embedded notice — embedded notice for standalone articles (travels with the file), LICENSE file for repos/gists (machine-readable); MIT needs full text nearby, CC BY 4.0 needs only a notice + link.
- **2026-08-11** — Licensing primer extended (§6.5 Q1.1.2.2.1.1): traceability model confirmed (embedded line + link back); license identifier (type+version) binds the terms, file must be verbatim; CC deed URLs permanent & version-locked, MIT text stable, re-license applies to future copies only.
- **2026-08-11** — Licensing Q2 answered (§6.5): linking between differently-licensed own works is unconditionally fine (link ≠ use; author of both); keep per-file notices, don't embed without notice.
- **2026-08-11** — Workflow restructure planned (§6.6, question log translation-workflow Q1-4): lead with goal + human-in-the-loop banner; setup/hook section ("what do I do / where do we start"); two versions (private adapted / public project-agnostic MIT for gist, private = source of truth); public droppables (meta data, hardcoded CC BY-SA, Research/→by-product, omnibus chapter); phase table with participants/input/output; Phase 1 AI-as-dictionary; Phase 5 condensed, public = GitHub only. Verdicts pending.
- **2026-08-11** — Workflow restructure extended (§6.6 Q4.3-4.5): per-step doers explicit; annotation reframed as a continuous stream (not a phase), merged with drafting, persistent-file requirement; translator's 7-step phase model adopted (Discovery → Draft&annotation → Worldview → Polish → Coherence re-read → Lint → Publication; Phase 0 new, review split into substantive + mechanical). Verdicts pending.
- **2026-08-11** — Verdicts V1-V8 recorded (§6.6) and executed: workflow restructured to v2.2 (private: goal-first + human-in-the-loop banner, hook section, 7-step phase table, annotation-stream, condensed publication); public version created `artifacts/translation-workflow-public.md` (project-agnostic sweep: meta data, CC BY-SA hardcode, Research/, omnibus chapter, Crom API, Afterwords Selection, wikidot artifacts, Rednote all removed; MIT embedded + LICENSE file for the gist). Pending: MIT gist creation.
- **2026-08-11** — MIT gist published: https://gist.github.com/Gojob2987/c60efcef24b47e18b1c9bdabf12d4381 (single file `translation-workflow-public.md`, MIT embedded at end; standalone `z_license.md` dropped as duplicative). Translator to link it from the personal essay's footer.
- **2026-08-11** — Wrap-up verdict (§6.7, question log Phase 3 Q3): licensing/publication stays integrated in this investigation (workflow is end-to-end by design; knowledge filed where used; next divergence = creative writing). Extraction only if publishing becomes a portfolio concern. Next step: translator writes the Chinese human essay; agent feedback in a new session.
- **2026-08-12** — Question log Q11 answered (§6.8): 信达雅 primer — origin (严复, 《天演论》 preface, 1898), the three characters (信/达/雅), the quoted passage explained (信 is the hard baseline; 达 takes priority because an unreadable translation fails its purpose; 雅 sought last, per the classics); nuances (theory-practice gap — 天演论 itself unfaithful; modern successors 鲁迅/钱锺书/傅雷/许渊冲; modern hierarchy baseline/non-negotiable/ceiling); mapping to this project (agent = 信 verification + 达 candidates; human = 雅 register taste; 一名之立旬月踟蹰 ↔ 术语考证 tables). Asked while the translator drafts the Chinese essay. §6.8 rewritten in Chinese same day (translator request — bilingual reply preference; English version superseded).
- **2026-08-12** — §6.9 added: 生僻字/指定字词术语追踪表 (Chinese-character glossary tracker) — columns: 字词 / 释义（中文）/ 拼音 / 英译; seeded with 踟蹰; grows on demand; sibling note pointing to review-report Appendix 8. Same day: requirement propagated into `<personal wiki>/investigation-workflow.md` (Keyword Tracker rules + report structure §6 + iteration log) per translator request.
- **2026-08-13** — Chinese essay draft finished by translator (`artifacts/与人工智能体一起翻译.md`, 127 lines, all 6 outline sections + 参考引用). Agent lint added as §6.10 (no severe issues; 2 fact-check items — series start year L5 "2008" and first-read year L12 "10年前", both predate the 2019+ series; medium: inverted quote marks L50/52, 他们→它们, 来得快, 赘述, 辅佐误用, 面对自己提问, 有一个建模; lows: punctuation/format/wording list). Translator fixes manually. Also flagged: 参考引用 missing 3 of the essay's 6 unique links (scp-wiki author page, How to Read a Book, Obsidian).
- **2026-08-13** — Second lint round (§6.10.1): fact-check flags **retracted** — qntm's author page confirms `2015-04-12 - Introductory Antimemetics`, so "自2015年起" and "10年前" are both correct. ~24 items verified fixed; 6 items kept by translator for reasons (inverted quotes L50/52, 有一个建模, 跨越数年的每一次重读, “信”，“达” comma, 爆炸的科技, 阅读，思考 commas); 1 new issue found (L105 可以…能 double modal); 参考引用 still missing the scp-wiki author-page link; link format inconsistent (bare URLs vs markdown links).
- **2026-08-13** — Verdicts recorded (§6.10.2, question log personal-essay #1-8): quotes confirmed errors and fixed by agent (5 spots; Obsidian YaHei renders quote directions indistinctly — habit note); 建模/跨越数年的每一次重读/信达逗号/爆炸的科技 all kept with translator's rationales; L46 pending single fix (顿号: 阅读、思考和写作); L105 double-modal fixed by translator; reference section updated by translator (community link added — CN author page chosen; Obsidian link format unified); agent proposed GB/T 7714-lite reference format (作者. 题名[EB/OL]. 日期. URL) with filled entries; flagged L5 vs 参考引用 link site mismatch (EN vs CN author page) for alignment.
- **2026-08-13** — Question log #6.1: L46 顿号 fixed by translator (verified 阅读、思考和写作). #8.1 answered: [EB/OL] is a GB/T 7714 document-type code (EB = electronic bulletin, OL = online; also [J]/[M]/[C]/[D] for journals/books/conferences/dissertations) — a citation-database convention invisible to essay readers; confirmed translator's instinct: 作者-题名-日期-URL suffices, just stay uniform.
- **2026-08-13** — Chinese essay published (§6.10.2 #9): **same gist as the EN version** (`f017a3a9`, both CC BY 4.0 — the mixed-license concern from §6.5 doesn't apply). CC BY 4.0 footer added to CN essay (mirrors EN: © 2026 Gojob + license + 发布地址 + EN-version anchor link); reference section reformatted by translator to 作者. 题名. 日期. URL. (6 entries, no [EB/OL]); published via gist git push (commit 4ce42c3) — gist now: license.md / Translate_with_AI_Agent.md / 与人工智能体一起翻译.md. Gist title unchanged (CJK filename sorts after ASCII).
- **2026-08-13** — Essay cross-links landed both ways (gist commit 6cabc17): EN footer → 中文版 anchor; CN footer → English version anchor. Then gist images fixed (commit 3b0bdeb): Obsidian `![[...]]` embeds are non-standard — converted to markdown `![alt](raw-url)` (width-constrained one → `<img width="539">`), 3 screenshots pushed into the gist (raw URLs verified 200). Lesson: gists don't render Obsidian embeds; images must live in the gist and be referenced by raw URL.
- **2026-08-13** — Publication migrated gist → **repo** (§6.11, question log Phase 4 Q1-3): `github.com/Gojob2987/translate-with-ai-agent` created (root commit e1b0550) — README.md (bilingual index + workflow gist link), LICENSE (CC BY 4.0 full text), 与人工智能体一起翻译.md, Translate_with_AI_Agent.md, images/ (qntm-author-page.png / question-tree.png / deepseek-release.png, relative paths). Old essay gist `f017a3a9` kept, description updated to point to the repo (deletable anytime). Local artifacts: images restored to Obsidian `![[...]]` embeds (user moved them to `artifacts/pictures/`), footers point to repo URLs. Workflow gist unchanged (MIT, single-file — gist-native). Repo copy is a publish snapshot; future essay edits land locally then re-push.
- **2026-08-13** — Publication consolidated (question log Phase 4 Q2-4): repo cloned to **`<local workspace>/translate-with-ai-agent`** (local home); **workflow moved into the repo** (`translation-workflow-public.md`, MIT embedded — dual license: essays CC BY 4.0 + workflow MIT, noted in README; repo commit 1ef004f); essays' embedded workflow URLs updated from gist to repo paths (CN L3/L32/参考引用, EN L2/L98); workflow-public License line generalized "published on GitHub" (gist vs repo landing notes), private workflow "repo/gist"→"repo"; **both stale gists deleted** (workflow c60efcef + essay f017a3a9 — nothing references them; Karpathy's gist stays as external source).
