---
type: log
title: FPO change log
summary: Append-only history of what changed and when
audience: founders
status: evergreen
updated: 2026-09-28
---

# Log

Newest last. Append, never rewrite.

---

**2026-08-15 — DK24 conversation.** Group discussed folding the FPO idea into DK24, a Mangalore
student-club consortium. Not processed into this repo; a recording exists.

**2026-08-31 — Parallel to DK24.** Group decided to build separately rather than merge. Not
processed into this repo; a recording exists.

**2026-09-14 — Intake questions written.** 19 questions across six sections, built as a Google
Form so all four answered independently.

**2026-09-17 — Four intake responses in, synthesised.** Biggest splits recorded: what FPO sells,
who pays, nonprofit against commercial, stage, and zero overlap on competitors.

**2026-09-17 — Two meetings.** Shobith joined as advisor for the first. Distribution chosen over
funding as the harder blocker. No equity at intake. Cohort of five to ten over six months, St
Aloysius first. Then the four founders walked the intake map: nonprofit dropped, stage set to
prototyping, competitors found to be altitude rather than disagreement.

**2026-09-20 to 09-23 — Exercise one run.** Brand Journey Framework, four responses.

**2026-09-24 — Exercise one reviewed.** Two corrections to the synthesis: the
people-against-revenue split was collapsed as vocabulary, and the map's axis labels were found
unreadable. Research settled as a side effect. Compensation principle stated by Ethan and disputed
by Adithya. Publishing agreed as record everything and filter later. The reputation question was
skipped.

**2026-09-24 to 09-28 — Exercise two run.** Credibility and scope, four responses. Selectivity
emerged as the first real answer to what FPO is known for. FPO established as an entity with no
track record of its own. Pond settled at Mangalore and coastal Karnataka with no split.

**2026-09-28 — Exercise three sent.** Contrarian two-column, scoped to incubators and cohort
programmes, five rows per founder. Awaiting responses.

**2026-09-28 — This repo built.** Knowledge moved out of a single flat folder into `truth/`,
`archive/` and `workshop/`. Seven truth files written, each claim carrying the date and the room it
was decided in. Contradictions found and handled: STATE.md had said exercise two was still out
while also marking it complete, carried two different dates, and listed five resolved splits as
live. The intake synthesis and map now carry supersede notes. Two genuine unreconciled conflicts
moved into `truth/open-questions.md` rather than being quietly resolved: the quiet period against
marketing in parallel, and compensation.

**2026-09-28 — Gates repointed, and a silent failure caught.** Every path check in
`workshop/GATES.md` was still globbing `brand/`, a directory that no longer exists. Because grep on
a missing path returns zero, and zero was the expected pass value, all of them would have passed
forever while checking nothing. Paths now point at `archive/exercises/`, and the slop-marker gate
exits non-zero if it finds no HTML at all. Verified with a positive control before trusting the
passes. `/wrap` now updates `truth/`, appends here, and commits.
