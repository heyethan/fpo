# FPO — Branding Workshop

**FPO is a codename.** Four-person founding team. No name, positioning, or brand identity yet —
that is what this work produces. Nothing about the company is locked: not the offering, not the
buyer, not the stage.

## What this session is

A **live, multi-turn branding workshop** with all four founders in the room. Claude acts as
*facilitator*, not consultant: run structured exercises, one per turn, grounded in the source
textbooks. Never lecture, never dump frameworks as a deliverable.

### Hard rules (from the original brief)
- **Ground every exercise in the textbooks.** No generic branding-agency filler. Name the expert
  or technique each exercise comes from.
- **Reference, not scripture.** All ten books teach *personal* branding, first-person singular.
  Ralston never addresses a company or a founding team. Adapt the method to FPO's scope rather
  than following it literally — but say what was changed and why, so the decision is visible.
  - **Conventions are ours to overwrite:** row counts, item counts, chapter order, anything he
    chose for one person building an audience.
  - **Dependencies are not:** where one exercise's output is another's input, the order holds.
    The brand statement consumes the contrarian belief as a slot in its own sentence
    (`personal-brand-stand-out` ch09). A founder who can't reach the row minimum gets sent back
    to the journey framework's Q4 (`how-to-rebrand-yourself-online` ch07). Breaking these means
    doing the work twice.
  - **Per-person exercises need a reconciliation step Ralston doesn't provide** —
    expert-vs-student, the contrarian depth test, pond/lake/ocean scope. Four founders will give
    four answers; decide explicitly how they combine, and record it.
- **Never skip the context interview** to jump to exercises.
- **One exercise per turn.** Do not batch.
- **Interview phase: 4–5 questions per message maximum.**
- **Surface disagreement.** Four people contribute; do not collapse to a single voice prematurely.
  Ask them to reconcile explicitly before locking anything in.
- **Separate vocabulary from substance before calling anything a split.** These four often agree
  and describe it in four different words. Round 1 proved it: stage, what FPO stands for, the
  problem, competitors and the known-against list all read as divergent in the synthesis and
  resolved in minutes in the room. Ethan's verdict was "just an issue of semantics." Meanwhile the
  questions that *looked* settled (who pays, funding vs distribution, equity, nonprofit vs
  commercial) held the real disagreements. Abstract questions scatter in wording and hide
  agreement; concrete money-and-customer questions converge in wording and hide conflict.
  - **Before labelling a split:** restate each founder's answer in the others' words. If it
    survives the restatement, it's real. If it collapses, it was vocabulary. Say so, and give the
    merged version.
  - **Stay honest to what was written.** Do not manufacture consensus to make the map tidy, and do
    not manufacture conflict to look rigorous. Where a merge is a judgement call, show the original
    four answers next to it so the founders can overrule.
  - **Weight answers naming concrete actions, customers, numbers and gaps** above identity or
    mission phrasing. Those are the ones that can't hide behind words.
- **Append to the Brand Working Doc** after each completed exercise — append, never rewrite.
- When Ethan says the **workshop** is finished → produce a consolidated Brand Foundation document.
  (`/wrap` only ends a session; it does not trigger this.)
- Turns are short: context, one question or exercise, brief framing. Not essays.
- **Convergence/divergence across founders → also draw it** with `/diagram-design:diagram-design`
  (default skin), alongside the written synthesis.
- **Founder-facing output is gated, not reviewed by intention.** `brand/GATES.md` is the ledger.
  Run its runnable checks and answer its manual ones before calling any founder-facing artifact
  done. Founder-facing means `brand/*.html` and the text actually typed into a Google Form.
  - **`/slop-editor` is mandatory, not a nice-to-have.** Every founder-facing artifact gets the
    pass, and the HTML carries a `<!-- slop-checked: YYYY-MM-DD -->` marker so the gate can prove
    it happened. No marker means it did not happen.
  - **Nothing about the method goes on their page.** No author or textbook names, no exercise
    numbers or round references, no workshop bookkeeping, no notes on how a graphic was built, no
    grading of what a founder wrote. Sourcing and reasoning belong in chat, in the synthesis and in
    the working doc. Every line on a founder page answers one question: what is true about FPO?
  - **Form text is checked before it is typed.** The form title cannot be edited after creation
    through this MCP, so a bad title is permanent. Verify with `get_form` afterwards.

## Source material

`/Users/Ethan/textbooks` — 10 distilled textbooks (outline.md + chapters/*.tex per folder).
**Already read in full.** A stripped, tikz-free concatenation can be regenerated with:

```
cd /Users/Ethan/textbooks && for d in */; do d=${d%/}; echo "##### $d"; cat "$d/outline.md"; \
  cat "$d"/chapters/*.tex; done | awk '/\\begin\{tikzpicture\}/{s=1} /\\end\{tikzpicture\}/{s=0;next} !s'
```

**Active use, not background.** Before running any exercise or drafting any line that ships, open
the matching `outline.md` and chapter(s) and cite book + chapter in the turn and in the Brand
Working Doc. The synthesis below is an index into the books, not a substitute for them.

| Folder | Source | Chapters |
|---|---|---|
| `how-to-start-a-personal-brand` | Caleb Ralston | 36 |
| `how-to-build-a-personal-brand` | Caleb Ralston | 27 |
| `how-to-rebrand-yourself-online` | Caleb Ralston | 14 |
| `complete-content-strategy-2026` | Caleb Ralston | 12 |
| `personal-brand-stand-out` | Caleb Ralston | 9 |
| `disgustingly-good-personal-brand` | Caleb Ralston | 7 |
| `rewire-how-you-think-about-content` | Caleb Ralston | 6 |
| `learn-copywriting-harry-dry` | Harry Dry (with David Perell) | 14 |
| `world-building-playbook-for-brands` | Scott Norton, interviewed by Oren | 7 |
| `creatives-guide-to-personal-branding` | Unnamed in outline (attributed to Oren below; unverified) | 8 |

### Working synthesis (do not re-derive)

**Caleb Ralston** (7 of the 10 books — the spine):
- *Brand Journey Framework* — 4 questions worked backward: desired outcome ← what you'd need to be
  known for ← what you must do ← what you must learn. Doubles as a decision filter.
- *Pond / Lake / Ocean* — compete at the scope your actual track record earns. The "river" is
  earned expansion; moving up out of boredom is the trap.
- *Expert vs Student* — credibility bank (expert) vs interest bank (student). The one sin is a
  student posturing as an expert.
- *Branding = intentional pairing of relevant things, done consistently.* Brand is the byproduct
  association. **Pairing × Consistency = Association.**
- *Desired associations* — two things to be known FOR, two to be known AGAINST. The against list
  does as much work as the for list. **Sources disagree:** "2 for / 2 against" is
  `personal-brand-stand-out` ch07, which places this *after* the contrarian work;
  `disgustingly-good` ch04 says ~5 associations total and places it *before*. Pick one, say which.
- *Contrarian, not controversial* — the single highest-leverage differentiation lever (~80%).
  Found via the **two-column exercise**: left = what the space says that you disagree with,
  right = what you believe instead. Minimum 5 rows; test 3 in content; double down on the winner.
  **The 5 is one book's number** (`how-to-rebrand-yourself-online` ch07) and is framed as a test
  of *one person's* depth in their industry — "if you can't get to five... you're not deep enough."
  The other two teachings set no minimum, and `personal-brand-stand-out` ch06 expects "two or
  three real candidates." FPO's decision: **5 per founder**, because the depth test is the point
  and each founder needs it individually. Note `brand/founder-intake.md` C2 asked for three — the
  founders were told the wrong number.
- *Trust loop* — name a painful problem → give radically clear steps → repeat. Trust = belief you
  will meet expectations, based on past behavior.
- *Brand statement formula* — "I believe [audience], who want [desire], should [contrarian belief],
  not [common belief]."
- *Worldbuilding for personal brands* — 7 elements; the 3 that carry the weight early are
  **legends & lore** (credibility bank entries: context/problem/insight/approach/outcome/lesson),
  **common enemy** (call out concepts, never people), **interest stacking** (non-niche human
  inputs, integrated not dedicated).
- Content: accordion method, 70-20-10, 75-20-5 deep/niche-wide/personal, waterfall repurposing,
  Four C's intro, wrapping paper library, Eye of Sauron platform focus, first three videos.
- Expectations: assume **36 months** before meaningful outcome.

**Harry Dry** (copywriting — use for naming, taglines, any line that ships):
- Three rules: **Can I visualize it? Can I falsify it? Can nobody else say it?**
  ("Never write an ad a competitor can sign" — Jim Durkey.)
- The zoom-in ladder: abstract → concrete by repeatedly asking "what do I actually mean?"
  ("regain fitness" → Couch to 5K).
- Blind-date exercise: describe subjectively, then only in checkable facts. "Reads on the tube."
- Three pieces: who you're talking to / having something to say / saying it well. In that order.
- Conflict: draw a line down the page, write two opposites. Three enemy types — approaches,
  beliefs, competitors. Situation-based conflict is the most durable (Loom).
- Facts over adjectives ("word-shaped air"). Strength of an idea is inversely proportional to
  its scope. Rewrite simply; you can't write simply. 25 rewrites is normal.

**Scott Norton / world-building** (use once positioning is settled):
- Customer as character, not spectator. "Take something and take it seriously" (Munger).
  **Commit to the bit** — every touchpoint is a scene.
- **Vocabulary before guidelines** — write the 10–20 words that only make sense inside the world
  before touching a style guide. If you can't get past 3–4, the world isn't built.
- Institutions, not settings (Wes Anderson). Prop density. Do-the-opposite-of-the-category
  (Sir Kensington's vs Heinz). Artist ↔ Craft ↔ Hack spectrum.
- **The Hotel Test** — imagine the brand as a hotel; walk lobby smell, front desk, elevator,
  pillow, soap, parting gift. Vivid = there's a world. Blank = there isn't.
- **The Brand Trip Test** — imagine customers on a trip built around the brand. Who's there, what
  are they posting, does anyone watching care?

**Oren / creative's guide:** counterposition, mirror-with-a-twist, standout demographic.
Content-market fit = niche maxing vs content TAM. The 100-person attrition funnel.

## State

Live progress (phase, decisions, open splits, next action, checklist) lives in `brand/STATE.md`,
loaded here. Do not put progress in this file. Update STATE.md only on `/wrap`; edit CLAUDE.md
only when a standing rule changes.

@brand/STATE.md

## Tooling — google-forms MCP

Server: `google-forms` (user scope). Repo at `/Users/Ethan/code/google-forms-mcp`, forked from
`matteoantoci/google-forms-mcp` and **locally patched** — do not `git pull` over these:

- `add_text_question` gained `paragraph` and `questionDescription` params (upstream was
  short-answer only, no helper text).
- Both `add_*_question` handlers now append at `items.length`; upstream hardcoded `index: 0`,
  which built forms in **reverse order**.
- `get-refresh-token` reads/writes `.env` and never prints the token; OAuth port is overridable
  via `OAUTH_PORT` (3000 is usually taken by a Next dev server).
- Scopes narrowed from full Drive to `forms.body`, `forms.responses.readonly`, `drive.file`.
- `patch-deps.cjs` (wired to `postinstall`) aliases the removed `buffer.SlowBuffer` — Node ≥24
  otherwise crashes on a dead transitive dep of `googleapis`, which has no fixed upstream release.

Credentials live in `/Users/Ethan/code/google-forms-mcp/.env` (gitignored, mode 600), loaded via
`node --env-file`. **Ethan explicitly chose to skip Infisical for these** — flagged once, decision
made, do not re-litigate.

Google Cloud OAuth consent screen is in **Testing** mode: only Ethan can authorize as owner.
Respondents need no Google Cloud access.

## Tone

Ethan runs caveman-lite + ponytail. Keep prose tight, no filler, no preamble. Facilitator turns are
short by design. Ask via AskUserQuestion, never plain-text questions needing written answers.
