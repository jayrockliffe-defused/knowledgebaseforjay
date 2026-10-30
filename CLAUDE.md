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

## HARD RULE: DATA DRIVES EVERY DECISION (Jay, Oct 23, 2026)

Applies to every project and every task, not just one.

- Every recommendation, plan and decision is backed by data: measured numbers, sourced research, live analytics or test results. Show the numbers and the source next to the recommendation.
- If the data is missing, say so, say how to get it (a test, a search, a metric to track), and get it before deciding when the cost of being wrong is real.
- Label estimates as estimates. Never invent numbers, users, stats or testimonials.
- When the data disagrees with a plan, a habit or an earlier decision, follow the data and say what changed.
- Every launch, ad, post or feature ships with the metric that will judge it and the rule for keeping, changing or stopping it.

---

## HARD RULE: NEVER HAND JAY A TASK YOU CAN DO (Jay, Oct 29, 2026)

Applies to every project, every agent, every session.

- If you can do it with the tools you have, do it. Do not write "you can do X", "run this command", "change this setting" or "click here" when you could do it yourself.
- Before handing Jay any step, try it first. Only pass it to him if you truly cannot: a hard limit (for example typing passwords, API keys or payment details), a permission you were denied, or a decision only he can make.
- When you do hand something over, say in one line why you could not do it, and give the exact step or a direct link. Nothing else on his list.
- Being blocked on one step is not a reason to stop. Do everything around it.

---

## HARD RULE: THREE QA TIERS, EVERY PROJECT AND GOVERNOR (Jay, Oct 29, 2026)

Testing never gets skipped, but the expensive model only runs when the risk earns it. Full QA on Claude costs about $30 a session.

- **Tier 1, every commit (free):** the project's automated tests, type checks and gates, run locally.
- **Tier 2, every deploy (cents):** the project's QA agent runs on DeepSeek through OpenCode (default deepseek/deepseek-flash). Same frozen snapshot, phone and desktop widths, both themes, live check after deploy.
- **Tier 3, big releases only (about $30):** full independent QA on Claude. Use it for every 4th deploy, any release with more than one feature, and anything touching payments, sign-in, database migrations or user data.
- A HIGH defect at any tier blocks the deploy. If Tier 2 output looks thin or unsure, escalate to Tier 3.
- Never batch all testing to the end of a build: bugs stack up, get harder to trace and reach live users.

## HARD RULE: ONE-WORD APPROVALS (Jay, Oct 29, 2026)

When something needs Jay's OK, end with a single clear line he can answer in one word, for example: Reply "yes" and I'll switch the QA agent over and log the change.

- Say exactly what "yes" triggers, so nothing happens he did not expect.
- One ask per line. If there are options, name them so he can reply with one word ("A" or "B").
- Put the recommendation first, the approval line last.

## HARD RULE: UPDATE, NEVER PILE UP PAGES (Jay, Oct 29, 2026)

Applies to every project, every governor, every chat and every agent.

- Before publishing any artifact, page, doc or file, search for the existing one on that topic (artifacts list, the Project, Drive, the repo, the Mac Clients folder) and update it in place, same link.
- Never publish a new artifact or page without Jay's OK. Ask with a one-word approval line and say which existing page you checked.
- Retired pages: copy their useful content into the project's archive doc first, then delete with Jay's OK.
- Why: in Oct 2026, Start From Done grew 21 separate pages for one project because each chat published new ones.

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
