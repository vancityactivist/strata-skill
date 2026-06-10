# Strata Agent Assistant

A [Claude skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills) that helps strata agents and strata managers in **British Columbia, Canada** perform their professional duties — grounded in the Strata Property Act (SBC 1998, c. 43), the Strata Property Regulation, and the Real Estate Services Act licensing framework.

## What it does

- **Strata Property Act reviews** — checks meeting notices, expenditures, bylaws, fines, and repair-responsibility questions against the specific SPA sections that govern them, and states a clear compliant / non-compliant conclusion with the path to fix problems.
- **Best-practice recommendations** — advises on the professionally defensible approach, clearly separating what the SPA *requires* from what good practice *adds*.
- **Meeting support** — AGM/SGM/council meeting prep: notice periods, quorum, voting thresholds (majority vs. 3/4 vs. unanimous), and drafting resolutions and minutes that survive CRT challenge.
- **Correspondence and disputes** — drafts ready-to-send letters to owners, council, and contractors, citing the statutory or bylaw basis, and maps the escalation pathway (s. 135 process → Civil Resolution Tribunal).
- **Compliance calendar** — tracks recurring obligations keyed to fiscal year end: AGM timing, Form B/F turnaround, depreciation report cycles, record retention, insurance appraisals.

## Structure

```
strata-skill/
├── SKILL.md                           # Entry point: triggering description + 5 core workflows
├── references/
│   ├── strata-property-act.md         # SPA/Regulation thresholds, deadlines, section numbers
│   ├── act-review-checklist.md        # Structured checklists for common compliance reviews
│   ├── best-practices.md              # Beyond-minimum professional practice + legal-escalation flags
│   ├── privacy-and-accommodation.md   # PIPA obligations + Human Rights Code duty to accommodate
│   ├── choa-guidance.md               # Topic index to CHOA bulletins (fetched live, never copied)
│   ├── key-cases.md                   # Leading authorities (Terry, Dollan, Weir) + when to cite them
│   └── roberts-rules.md               # Robert's Rules adapted to the SPA: chairing, motions, s. 50(2)
└── assets/templates/
    ├── notice-to-comply.md            # s. 135 bylaw-complaint notice
    ├── arrears-demand.md              # Formal demand (lien / non-lienable variants)
    ├── agm-notice.md                  # AGM notice meeting s. 45 requirements
    └── hearing-decision.md            # Written decision after s. 135 response / s. 34.1 hearing
```

`SKILL.md` is what Claude loads when the skill triggers; the reference files are read on demand depending on the question (progressive disclosure).

## Installation

**Claude Code (direct install)** — no clone needed:

```
/plugin marketplace add vancityactivist/strata-skill
/plugin install strata-agent-assistant@strata-skills
```

Updates arrive via `/plugin marketplace update strata-skills`.

**Claude Desktop / claude.ai** — download `strata-skill.skill` from the [latest release](https://github.com/vancityactivist/strata-skill/releases/latest), then double-click it (Desktop) or upload it via Settings → Capabilities → Skills (claude.ai).

**Manual (Claude Code)** — clone this repo into your skills directory:

```bash
git clone https://github.com/vancityactivist/strata-skill.git ~/.claude/skills/strata-skill
```

## Important disclaimer

This skill supports licensed professionals; **it is not legal advice**. Statutory section numbers and thresholds reflect the author's knowledge at the time of writing — the SPA and Regulation are amended frequently. Always verify against the current consolidated legislation at [bclaws.gov.bc.ca](https://www.bclaws.gov.bc.ca) before relying on a citation, and obtain legal advice for contested or high-stakes matters.

## License

MIT
