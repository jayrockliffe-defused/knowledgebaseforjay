# Knowledge Base for Jay — CLAUDE.md

---

## HARD RULE — NO ASSUMPTIONS. EVER. Assumptions cost us both time lost and, for me, time and money. Assumptions are never the right answer, and it makes the task take longer than it should. 

This overrides everything below. No exceptions. No flexibility.

Never assume anything about architecture, deploy setup, file paths, tools,
infrastructure, user intent, or current state.

The sequence is: **Research → Ask → Verify → Then suggest.**

- Before editing a file, confirm it exists and read it.
- Before running a command, confirm the tool/CLI is available.
- Before suggesting an approach, verify the current state.
- Before referencing a path, confirm it is real.
- If you are about to act on unverified information, STOP.

Run a command. Read a file. Ask a question. Confirm the answer.
Then proceed.

**Assumptions are treated as failures.** If Jay catches an assumption,
the entire task restarts from Step 1 (Think). No shortcuts.

---

## How to Work With Jay

**The sequence: Think → Ask → Research → Plan → Confirm → Build → QA → Present.**

Never jump to building. Follow this in order every time.

- **Think** — Read the relevant docs and understand current state before touching anything.
- **Ask** — Surface unknowns before committing to an approach.
- **Research** — Find the best possible approach, not just a working one.
- **Plan** — Lay out the approach and get alignment.
- **Confirm** — Get explicit approval from Jay before executing.
- **Build** — Execute the plan. Flag deviations if they come up.
- **QA** — Test in the live environment. Not just locally.
- **Present** — Deliver working, tested output. No "almost done."

**Jay's hard rules:**
- Consult on key decisions. No surprises.
- Thoroughness over speed. Right matters more than fast.
- Use all available context before asking questions you can answer yourself.
- No placeholder content. Everything real.
