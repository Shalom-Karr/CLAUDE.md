# Claude Working Preferences

Generalized behavioral instructions for all projects. Place in `~/.claude/CLAUDE.md` to apply globally.

## Execution

- **Run to completion.** When given a task, finish it. Don't pause for "should I continue?" unless the next step is destructive or ambiguous. If something breaks, diagnose and fix it, then resume. Only escalate when recovery options are exhausted.
- **Use idle time.** While waiting on builds, scrapes, or deployments — write docs, fix minor issues, or prep the next task. Never sit idle during long processes.
- **Monitor long processes.** Report progress with concrete numbers ("142/947 at 9.4/min, ETA 86min"), not "it's going well." Check logs for errors periodically.
- **"Note for later"** = save to memory. Acknowledge briefly, don't implement.

## Decision-Making

- **Action over discussion.** If the path is clear, execute. Only ask for confirmation on genuinely ambiguous or irreversible decisions.
- **Pick pragmatic over perfect.** A working solution now beats a deliberated plan. When the user gives explicit permission ("you have complete permission"), take it at face value.
- **Don't over-plan.** Three similar lines > premature abstraction. One bundled PR > five trivial splits. Solve what's in front of you.

## Communication

- **Concise.** Don't summarize what you just did — the user sees the diff. Don't narrate your thought process. State results directly.
- **Cold-readable updates.** When you do give updates, write so someone could pick up without context. Complete sentences, no shorthand from earlier.
- **Progress numbers, not reassurance.** "327/947 (34.5%), ETA 72min" is useful. "Making good progress" is not.

## Code

- **HTTP-first for data extraction.** Only use Selenium when the target requires browser-level interaction (OIDC login, JS-rendered content). Everything else: `requests` + BeautifulSoup.
- **SQLite for persistence** unless the use case genuinely requires Postgres/Redis.
- **Robust parsers** — tolerate missing data with fallbacks and gap tolerance rather than crashing on first unexpected element.
- **No unnecessary abstractions.** Don't build helpers for one-time operations. Don't design for hypothetical future requirements.
- **No comments by default.** Only add one when the WHY is non-obvious.

## UI

- **Dark theme for ops pages** (monitoring, console): `#0f172a` bg, `#1e293b` cards.
- **Light theme for user-facing pages**: white cards, brand accent colors.
- **TailwindCSS via CDN** — no build step. Vanilla JS, no frontend frameworks.
- **All pages cross-linked** — every page should have nav to every other page.

## Documentation

- Write documentation during idle time without being asked.
- Detailed and technical — include code examples, endpoints, selectors.
- Update CHANGELOG.md and README.md with every feature change.
- Keep docs in `docs/` directory, markdown format.

## Error Recovery

- Don't lose progress — use skip logic, caching, idempotent re-runs.
- If sessions expire or connections drop, retry or re-authenticate.
- Monitor background processes — don't assume they're healthy just because they started.
