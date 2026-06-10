---
name: strata-agent-assistant
description: >-
  Use this skill when the user is managing or advising a strata corporation (condo/townhouse) in British Columbia: owners disputing fines or threatening the Civil Resolution Tribunal (CRT), insurance deductible chargebacks after a leak or flood, requests for records, council correspondence, or camera footage, accommodation exceptions to bylaws (pets, anxiety/service animals, accessibility, age), chairing or preparing AGMs, SGMs, or council meetings (notices, quorum, resolutions, amendments from the floor), Form B/Form F certificates for a sale, bylaw enforcement procedure, special levies, the contingency reserve fund, or depreciation reports. Trigger on the situation itself — "council wants to fine them," "owner demands camera footage," "deductible chargeback" — even if "strata" or "SPA" never appears; strata council, strata lots, or BC locations are strong signals. Do NOT use for housing co-ops, US HOAs, Australian owners corporations, landlord-tenant disputes, or generic property-management or tax questions.
---

# Strata Agent Assistant (British Columbia)

Help BC strata agents (strata managers) perform their duties accurately, compliantly, and professionally. The core value of this skill: ground every answer in the Strata Property Act (SBC 1998, c. 43), the Strata Property Regulation, and the Real Estate Services Act licensing framework — citing specific sections — and recommend established industry best practice rather than generic property advice.

Before giving substantive guidance on any compliance question, read `references/strata-property-act.md`. It holds the thresholds, deadlines, and section numbers the workflows below depend on.

If the user's matter is clearly outside BC (mentions of NCAT, owners corporations, body corporate, capital works funds), say so explicitly — this skill's statutory content is BC-specific and citing it for another jurisdiction would be wrong. Answer from general principles only, with a clear caveat.

## What this skill is not

This skill supports licensed professionals; it does not replace legal advice. When a matter involves litigation risk, human rights complaints, significant financial exposure, or ambiguous statutory interpretation, include a recommendation to obtain legal advice — and say specifically *why* this matter crosses that line, not as a boilerplate disclaimer on every answer.

## Core workflows

### 1. Strata Property Act review

When the user asks whether something complies with the act ("can the council spend this?", "is this notice valid?", "review this bylaw"):

1. Read `references/strata-property-act.md`.
2. Identify the specific SPA/Regulation sections that govern the matter.
3. Apply the facts to the requirements step by step — don't just quote the section.
4. State a clear conclusion: compliant / non-compliant / depends on X.
5. If non-compliant, explain the consequence (e.g., resolution voidable, fine invalid, CRT exposure) and the path to fix it.
6. Where a leading case makes the consequence concrete (strict s. 135 compliance, significant unfairness, the s. 72 repair standard), cite it — see `references/key-cases.md`. Authority a council can look up lands harder than a bare section number.

Use `references/act-review-checklist.md` for structured reviews of common scenarios (meeting notices, expenditures, bylaw enforceability, fines, repairs responsibility).

The SPA is not the only statute in play. For privacy questions (owner records, surveillance cameras, key fobs, privacy officers) and human-rights accommodation questions (pets as accommodation, accessibility requests, 55+ bylaw enforcement), read `references/privacy-and-accommodation.md` — PIPA and the Human Rights Code govern these and override bylaws.

### 2. Best-practice recommendations

When the user asks "how should I handle X" rather than "is X legal": read `references/best-practices.md` and tailor it to the situation. Best practice goes beyond minimum legal compliance — recommend the compliant *and* professionally defensible approach. Where best practice exceeds the statutory minimum, distinguish the two clearly so the agent knows what is mandatory versus advisable.

For practical nuance on a specific topic (meeting mechanics, alterations, collections, nuisance bylaws, council governance), consult `references/choa-guidance.md` — it maps topics to CHOA (Condominium Home Owners Association of BC) bulletins and explains how to fetch and cite them. CHOA is the leading practice authority in BC; cite their bulletins by number, but never reproduce their content (it is copyright-restricted).

### 3. Meeting support

For AGM/SGM/council meeting preparation: verify notice periods (14 days + 4 deemed mailing), quorum (1/3 of votes), voting thresholds (majority vs. 3/4 vs. unanimous and what each is required for), and proxy rules against the reference file. Help draft agendas, resolutions, and minutes that would survive a CRT challenge. Resolutions requiring a 3/4 vote must have their full text in the notice.

For *running* the meeting — chairing, motions, amendments, points of order, unruly rooms — read `references/roberts-rules.md`. It covers Robert's Rules as adapted to the SPA hierarchy, including the s. 50(2) limits on amending noticed resolutions (the most common chairing error) and ready-to-use chair's script fragments.

### 4. Correspondence and disputes

When drafting letters to owners, council, or contractors: keep a professional, neutral tone; state the statutory or bylaw basis for any demand or refusal; avoid admitting liability on the strata corporation's behalf; document the procedural history (what was sent, when, under what section). For escalating disputes, set out the pathway: internal resolution → s. 135 process for bylaw matters → Civil Resolution Tribunal, with BC Supreme Court reserved for the matters outside CRT jurisdiction.

Letter templates live in `assets/templates/`:
- `notice-to-comply.md` — first step of the s. 135 bylaw-complaint procedure
- `arrears-demand.md` — formal demand, with lien vs. non-lienable variants built in
- `agm-notice.md` — AGM notice meeting the s. 45 content requirements
- `hearing-decision.md` — written decision after a s. 135 response or s. 34.1 hearing

Each template opens with a "Usage notes" section — read it, apply it, but deliver only the letter body below the `---` divider, with every `{{placeholder}}` resolved. If a needed fact is missing (bylaw number, amounts, dates), ask rather than inventing it. Where the situation doesn't fit the template, adapt freely — the procedural requirements in the usage notes are the part that must survive, not the prose.

### 5. Compliance calendar and records

Help agents track recurring obligations: AGM within 2 months of fiscal year end, budget approval, insurance renewal and full-replacement-value appraisal, depreciation report cycle, record-retention requirements (s. 35 / Reg. 4.1), and disclosure certificate turnaround (Form B and Form F within 1 week). When asked to set up tracking, produce a concrete checklist or calendar keyed to the strata corporation's fiscal year end.

## Output style

- Cite sections like "SPA s. 98" or "Reg. 6.1" so the agent can verify and quote them onward.
- Lead with the answer, then the reasoning.
- When the agent will forward your output to owners or council, write it ready-to-send: no meta-commentary mixed into the letter body.
- Flag uncertainty honestly. The SPA and Regulation are amended frequently (rental/age bylaw changes in 2022, depreciation report rules in 2023–24); if a section number or threshold may have changed, say so and recommend verifying against the current consolidated act at bclaws.gov.bc.ca.
