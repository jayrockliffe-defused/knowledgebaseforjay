# Agent brief template (brain to hands)

Claude (the brain) fills this in. A cheaper agent (the hands: OpenCode + DeepSeek, or Copilot cloud agent) does the work.
The hands see nothing else, so every field must stand on its own. Copy, fill, send.

---

## GOAL
One sentence. What exists when you are done that does not exist now.

## REPO AND BRANCH
- Repo path:
- Work on a new branch: `agent/<short-slug>`. Never commit to main. Never push to main.

## CONTEXT (read first)
- Read `CLAUDE.md` in the repo root and follow its hard rules.
- Files that matter:
- Do not touch: (LOCKED areas, other people's uncommitted changes, anything outside scope)

## CONSTRAINTS
- Scope is exactly the goal. No extra refactors, renames or "while I was here" changes.
- No em dashes or en dashes in any user-facing text.
- No placeholder content. Real values only. If a value is unknown, stop and say so.
- No new dependencies unless the brief says so.

## DONE MEANS
- [ ] Concrete, checkable outcome 1
- [ ] Concrete, checkable outcome 2
- [ ] `./scripts/flight-check.sh pre` prints `FLIGHT PRE: PASS`

## HOW TO VERIFY
Run `./scripts/flight-check.sh pre`. If any line says FAIL, read its log, fix, rerun. Repeat up to 5 times.
If it still fails after 5 tries, stop and report the failing line. Do not weaken or skip a check to make it pass.

## REPORT (your final answer, nothing else)
```
STATUS: done | blocked
BRANCH: agent/<slug>
COMMITS: <short sha> <message>
FLIGHT PRE: PASS | FAIL <which check>
CHANGED: <files, one per line>
NOTES: <max 3 lines: risks, anything the reviewer must look at>
```

---

## Rules for the brain (Claude)
1. Write the brief. Send it. Do not read logs; read the REPORT.
2. Review the diff in proportion to risk. Run nothing the hands already ran.
3. Copilot reviews the PR first. Claude reads Copilot's comments, not the whole diff, unless risk is high.
4. Merge only on `FLIGHT PRE: PASS`. After deploy, run `./scripts/flight-check.sh post`. Deploy is done only on `FLIGHT POST: PASS`.
5. Post fails: roll back first (`git revert` + push), report to Jay, then fix.

## Who does what
| Job | Tool |
|---|---|
| Plan, brief, go/no-go | Claude |
| Build, iterate, run pre-flight | OpenCode + DeepSeek V4 Flash (V4 Pro for hard bugs) |
| Night jobs from GitHub issues | Copilot cloud agent |
| First review on every PR | Copilot code review |
| Post-flight live checks | flight-check.sh post (Playwright, curl) |
