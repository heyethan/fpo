# Founder-facing output gates

Every artifact the four founders read must pass these before it is called done.

**In scope:** `archive/exercises/*.html`, and the text actually typed into a Google Form (title, question
titles, question descriptions).

**Out of scope:** the question draft files (`archive/exercises/*-journey.md`, `archive/exercises/*-credibility.md`,
`archive/exercises/founder-intake.md`), synthesis files, meeting records, `STATE.md`, `CLAUDE.md`. These are
working documents. Sourcing, adaptation notes and bookkeeping belong there, and the draft files
carry them deliberately. The founder-facing surface is the form, not the draft.

**Grandfathered:** `archive/exercises/exercise-1-map.html` and `archive/exercises/intake-divergence-map.html` predate these
gates and stay as the record of those exercises. Excluded from every check below.

Run from `/Users/Ethan/FPO`.

---

G1. No em dashes or en dashes in founder-facing output
    CHECK: grep -l '—\|–' archive/exercises/*.html 2>/dev/null | grep -v 'exercise-1-map.html' | grep -v 'intake-divergence-map.html' | wc -l | tr -d ' '
    EXPECT: 0

G2. No author or textbook names on founder pages
    CHECK: grep -il 'ralston\|harry dry\|perell\|scott norton\|munger\|wes anderson\|sir kensington' archive/exercises/*.html 2>/dev/null | grep -v 'exercise-1-map.html' | grep -v 'intake-divergence-map.html' | wc -l | tr -d ' '
    EXPECT: 0

G3. No internal file paths or working-doc references on founder pages
    CHECK: grep -l 'archive/exercises/\|STATE\.md\|synthesis\|CLAUDE\.md' archive/exercises/*.html 2>/dev/null | grep -v 'exercise-1-map.html' | grep -v 'intake-divergence-map.html' | wc -l | tr -d ' '
    EXPECT: 0

G4. Every founder-facing HTML carries a dated slop-pass marker
    CHECK: node -e "const fs=require('fs'),p=require('path');const d='archive/exercises';const skip=['exercise-1-map.html','intake-divergence-map.html'];const html=fs.readdirSync(d).filter(f=>f.endsWith('.html'));if(html.length===0){console.log('NO_HTML_FOUND');process.exit(1)}let bad=0;for(const f of html.filter(f=>!skip.includes(f))){if(!/<!--\s*slop-checked:\s*\d{4}-\d{2}-\d{2}\s*-->/.test(fs.readFileSync(p.join(d,f),'utf8'))){console.log('MISSING: '+f);bad++}}console.log(bad===0?'ALL_MARKED':'UNMARKED='+bad)"
    EXPECT: ALL_MARKED

G5. Every founder-facing diagram passes the diagram self-check
    CHECK: python3 /Users/Ethan/.claude/plugins/cache/diagram-design/diagram-design/2.3.5/skills/diagram-design/scripts/self_check.py archive/exercises/exercise-2-map.html && echo SELFCHECK_OK
    EXPECT: SELFCHECK_OK

G6. No grading of founder answers back to them
    Manual. Read every sentence. If it assesses, ranks or scores what a founder wrote
    ("the only real answer", "still at the wrong altitude", "the first answer that works"),
    cut it. State the finding, not the mark.

G7. No workshop bookkeeping
    Manual. No round numbers, no "this round did not touch it", no "open since the 24th", no
    note of which exercise produced what, no commentary on how the graphic was built.

G9. Form text is checked before it is typed, not after
    Before calling create_form or add_*_question, run the intended title and every question
    title and description through G1, G2, G6, G7 and G8. The form title cannot be edited after
    creation through this MCP, so a bad title is permanent for that form.
    After building, verify with get_form and read every string back.

    ABANDON: G9-retro — the exercise-two form shipped with an em dash in its title
    ("FPO — Exercise Two: Credibility and Scope") and a bookkeeping line in the Q5 description
    ("Two answers came up on the 24th and neither got written down"). All four founders have
    already answered. Rebuilding the form would orphan the responses, so this one stands as is.
    The gate applies from the next form onward.

G8. Every line answers "what is true about FPO?"
    Manual. If a sentence is about the method, the textbook, the process or my own reasoning,
    it does not belong on the page. The founders came for their company, not the workshop.

---

## The rule that forced this

`/slop-editor` is mandatory on every founder-facing artifact. G4 makes it checkable: no dated
marker means the pass did not happen, and the gate fails.

Gates exist because all of G1, G2, G6, G7 and G8 were violated in `exercise-2-map.html` on its
first build, and the slop pass was skipped entirely. Intentions did not catch any of it.
