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

## HARD RULE: STAY OFF THE EXTENDED DISPLAY (Jay, Oct 31, 2026)

Applies to every Claude and DeepSeek agent, every project.

- Never use Jay's extended (external) display or any window on it, including Chrome windows.
- Work only on the MacBook's built-in screen, in the background, without taking over the screen.
- Never launch extra copies of Chrome (for example the chrome-devtools tool). Use his signed-in main Chrome.
- Open as few tabs as possible, and close every tab you open.

---

## HARD RULE: VISIONARY MODE, EVERY AGENT (Jay, Nov 1, 2026)

Applies to every Claude and DeepSeek agent, every governor, every project.

- Load and follow `skills/visionary/SKILL.md` in this repo on every task: context audit, competitive delta, the 3x horizon, then deliver.
- Sprint toward ROI: every plan, build and asset names its revenue path and rough effect toward $100K a month in year 1. Leapfrog current offerings; never settle for 10% better.
- Evidence still wins: a bold idea carries its source or the test that proves it. Chat stays brief; the depth goes into the work.

---

## HARD RULE: QA AND UX TOOLKIT, EVERY APP (Jay, Nov 1, 2026)

Applies to every governor that ships an app or site (Start From Done, Defusely, Trades, Back To You site and any new one). Use it on your next pass.

1. **First-time 60+ user walk, every release.** Before asking Jay for "go", run a first-time user walk through the core loop at 390x844, normal text and 130% text, light and dark. Hard fails: the next action below the fold, console errors, more than 12 taps to the first success. Also report small tap targets (under 44px), small text, low contrast, jargon and whether progress is visible. Reference script: Start From Done repo, tools/persona-first-time.mjs (branch feat/persona-test until merged). Copy and adapt it; do not share one script across repos.
2. **PostHog for analytics, replays and error reports.** One PostHog project per app, never shared. Same consent rules as the app's existing analytics. Replays mask all text and inputs; never record on pages whose address carries a secret. Strip query and #hash from every URL. A test types a unique marker word into the app and proves it never appears in anything sent. Sentry is skipped: PostHog error tracking covers it.
3. **One-question ease check.** After a user's first success, one PostHog survey question: "How easy was that?" 1 to 5. Report it beside activation and retention.
4. **Design polish pass before big releases.** Use the Mobile App Design plugin (onboarding, paywall and screen review) and the installed design skills (design-elevation, interaction-design, ux-writing, accessibility-audit). Measure against the project's own award benchmark apps.
5. **Paid tools stay off until Jay says yes.** Mobbin is connected but needs a paid plan; do not use it.
6. **Analytics consent by country (Jay, Nov 2, 2026; build it in every app, Trades apps included).** Analytics (GA4 and PostHog) are ON by default for the US and for Canada outside Quebec, with one short notice at first open (25 words or fewer, a Turn off action, never a blocking tap) and a Measurement off switch in Settings that stops everything in the same tab, no reload. Quebec and everywhere else: ask first, nothing loads before a yes (Quebec Law 25 requires tracking off by default). Global Privacy Control or Do Not Track: always off. Ad measurement (Pinterest, Meta and the like) stays opt-out default in the US only; Canada asks first. One shared consent decision feeds every tag so they can never disagree. The privacy page and store data safety forms must say all of this. Tests: US default on, CA default on with notice and working switch, CA plus Quebec nothing loads, CA plus GPC nothing loads. Reference build: Start From Done release 723 (site commits 186eedc geo cookie sfd_cc=CA and sfd_rg=QC from Cloudflare cf.country and cf.regionCode, 49d6354 shared consent, 6d71fb2 tests; app commit 130a730 Settings switch). Not legal advice; Jay accepted the risk for Canada outside Quebec.

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
