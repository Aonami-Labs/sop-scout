# SOP Scout

**Build SOPs that stick.**

An [Aonami Labs](https://labs.aonamitech.com) open-source tool. Paste a Standard Operating Procedure and check it against 12 completeness criteria — title, purpose, scope, step clarity, role definition, decision points, exceptions, escalation, resources, timeline, contact, and review date. Get a quality score and AI-powered gap-filling suggestions. Runs entirely in your browser.

```
SOP text  →  12-point completeness check  →  0–100 score  →  AI gap fill
```

---

## What It Does

### 12 Completeness Criteria

SOP Scout validates your procedure against a checklist of what makes an SOP actually usable:

| # | Criterion | What It Checks | Why It Matters |
|---|-----------|----------------|----------------|
| 1 | **Title/Name** | Does the SOP have a clear name? | You need to find it and reference it |
| 2 | **Purpose/Goal** | Does it explain why this procedure exists? | Team context: why does this matter? |
| 3 | **Scope** | Who and what does it cover? | Prevents misuse (e.g., "only for US operations") |
| 4 | **Step Clarity** | Are steps numbered and specific? | Steps must be actionable, not vague |
| 5 | **Role Definition** | Does it say who does each step? | No ambiguity about responsibility |
| 6 | **Decision Points** | Are if/then and approval criteria clear? | The "when does X happen?" question |
| 7 | **Exceptions/Edge Cases** | What doesn't apply here? | Prevents mistakes when the normal path breaks |
| 8 | **Escalation Path** | What happens when someone is stuck? | Defines who approves, who decides, who overrides |
| 9 | **Resources/Tools** | What tools or forms are needed? | New person can't execute without this |
| 10 | **Timeline/Duration** | How long should each step take? | Is this a 5-minute task or a 5-hour project? |
| 11 | **Contact/Questions** | Who do you ask if it's unclear? | Prevents guess-and-check approaches |
| 12 | **Review Date** | When was this last verified? | Stale procedures are dangerous procedures |

### Scoring

- Each criterion: **10 points** (present) or **0 points** (missing)
- Total: **0–100**
- Grade bands:
  - **85–100:** Solid SOP (11–12 criteria met)
  - **55–84:** Needs work (7–10 criteria met)
  - **Below 55:** Incomplete (< 7 criteria met)

---

## How to Use

### Input

Paste any SOP in any format:

```
PROCEDURE: Customer Refund Request
PURPOSE: Handle customer refund requests fairly and quickly
SCOPE: All customer-facing teams

STEPS:
1. Customer submits refund request via support ticket
2. Support agent reviews order status
3. If order shipped, approve up to 30% refund
4. If not shipped, approve 100% refund

ROLES:
- Support Agent: Reviews and approves refunds
- Manager: Escalation authority for disputes

EXCEPTIONS:
- Digital products: No refund after download
- Custom orders: Case-by-case review

ESCALATION:
If refund amount is > $5K, escalate to Manager

CONTACT: support@company.com or your manager
LAST REVIEWED: June 2024
```

### Steps

1. **Paste your SOP** — Any format works: markdown, plain text, bullets
2. **Get scored instantly** — Each criterion is checked
3. **See what's missing** — The gap analysis tells you which criteria failed
4. **Add your AI key** (optional) — Get suggestions for missing sections
5. **Fill the gaps** — Copy AI suggestions into your SOP

### Results

- **Per-criterion grid** — Green (present), red (missing)
- **Overall score** — 0–100 with grade
- **Gap count** — "You're missing 4 criteria"
- **AI suggestions** — Here's what should go in each gap

---

## Features

### Deterministic Checking
- No guessing — each criterion either passes or fails
- Regex-based pattern matching (looks for keywords, structure)
- Same rules every time — reproducible results

### Smart Detection
- **Title:** Looks for named procedures, procedure tags
- **Purpose:** Detects "why," "purpose," "goal," "objective" language
- **Scope:** Finds scope, applies to, applicable, who, audience
- **Steps:** Detects numbered lists and action verbs
- **Roles:** Finds role definitions, responsibility, who, person, team
- **Decisions:** Looks for if/then, case statements, conditions
- **Exceptions:** Searches for exception, edge case, special, unusual, corner case
- **Escalation:** Finds escalat, manager, approval, override, uncertain
- **Resources:** Detects tool, form, system, software, resource, access
- **Timeline:** Finds minute, hour, day, week, duration, time
- **Contact:** Finds contact, reach out, email, call, manager, support
- **Review:** Finds review, updated, date, version, last

### AI Gap Fill (BYOK)
- With your API key (Anthropic, OpenAI, Google, or Groq):
  - Get AI-generated content for missing sections
  - Suggestions are tailored to your SOP context
  - Ready to copy-paste into your document

### Built-in Sample
- Load a complete example SOP
- See what 100/100 looks like
- Modify for your use case

---

## Scoring Examples

### Complete SOP (85–100)
```
[All 12 criteria present]

Title:            ✓ "Customer Refund Request Process"
Purpose:          ✓ "To handle refund requests consistently"
Scope:            ✓ "Applies to support team, US orders only"
Step clarity:     ✓ "1. Review order status. 2. If shipped..."
Role definition:  ✓ "Support Agent: Reviews. Manager: Approves > $5K"
Decision points:  ✓ "If shipped: up to 30%. If not: 100%."
Exceptions:       ✓ "Digital products: None. Custom: case-by-case"
Escalation:       ✓ "Amounts > $5K go to Manager for approval"
Resources:        ✓ "Uses: Support ticket system, refund form"
Timeline:         ✓ "Standard review: 24 hours. Approval: 48 hours"
Contact:          ✓ "Questions: email support@company.com"
Review date:      ✓ "Last reviewed: June 2024"

Score: 100/100 ✓
```

### Incomplete SOP (Below 55)
```
Onboarding Process

Step 1: Send welcome email
Step 2: Set up account
Step 3: Do training
Step 4: Go live

[Only 2 criteria present]

Title:            ✓ "Onboarding Process"
Purpose:          ✗ (missing: why does onboarding matter?)
Scope:            ✗ (missing: is this for all users or just enterprise?)
Step clarity:     ✗ ("Do training" is vague; what training?)
Role definition:  ✗ (who sends email? who does training?)
Decision points:  ✗ (when do they move to step 2? any conditions?)
Exceptions:       ✗ (what if someone already trained?)
Escalation:       ✗ (what if training fails?)
Resources:        ✗ (what email system? what training platform?)
Timeline:         ✗ (how long does each step take?)
Contact:          ✗ (who do you ask if stuck?)
Review date:      ✗ (when was this last checked?)

Score: 20/100 🔴
```

### Fixable SOP (55–84)
```
Refund Process

Title:            ✓ "Refund Request Handler"
Purpose:          ✓ "Process refund requests"
Scope:            ✗ (which teams? which customers?)
Step clarity:     ✓ "1. Customer submits. 2. Agent reviews. 3. Approve/reject"
Role definition:  ✓ "Support Agent processes; Manager approves"
Decision points:  ? (when approve? what amount?)
Exceptions:       ✗ (digital products? custom orders?)
Escalation:       ✗ (when does it go to Manager?)
Resources:        ✗ (what system do we use?)
Timeline:         ✗ (how long should this take?)
Contact:          ✓ "support@company.com"
Review date:      ✗ (not dated)

Score: 60/100 ⚠
```

---

## How the Checker Works

SOP Scout uses pattern matching to detect whether each criterion is present:

1. **Read the SOP text** — Any format, any length
2. **For each criterion** — Search for indicator keywords and patterns
3. **Pass/fail assignment** — Criterion is either present or missing (binary)
4. **Score calculation** — 10 × (criteria passed) / 12 × 100
5. **Gap analysis** — List all missing criteria

The checker looks for these indicators:
- **Title:** `SOP`, `Procedure`, `Process`, `How to`, `Step-by-step`
- **Purpose:** `purpose`, `goal`, `objective`, `why`, `reason`
- **Scope:** `scope`, `applies to`, `applicable`, `covers`, `who`
- (And so on for each criterion)

---

## Why These 12 Criteria?

An SOP that passes all 12:

- **Is findable** (has a title)
- **Is contextual** (has purpose and scope)
- **Is actionable** (steps, roles, resources are clear)
- **Is flexible** (handles exceptions and decisions)
- **Is supportive** (escalation path and contact info)
- **Is current** (review date is recent)

An SOP that fails multiple criteria typically ends up:
- In a drawer or wiki nobody reads
- Misinterpreted because roles are unclear
- Broken when exceptions arise
- Outdated and dangerous

---

## Disclaimer

SOP Scout checks for *presence*, not *quality*. A SOP can pass all 12 criteria and still be:
- Too complex or verbose
- Missing critical detail
- Unclear in sections despite having all sections
- Not actually followed by the team

**Treat this as a structural completeness check.** A complete SOP is necessary but not sufficient for good process documentation. You still need:
- Clear writing and examples
- Diagrams or flowcharts where helpful
- Real-world testing ("does this actually work when it's Monday and we're tired?")
- Regular reviews and updates
- Buy-in from the people who execute it

---

## BYOK AI

Add your own API key for optional gap-filling suggestions:
- **Anthropic** (Claude Sonnet/Opus)
- **OpenAI** (GPT-4o)
- **Google** (Gemini 2.0 Flash)
- **Groq** (Llama 3.3 70B)

Your key stays in your browser tab and is sent only to your chosen provider — never to Aonami.

---

## License

MIT © Aonami Labs. See [LICENSE](LICENSE).

---

## Suggested Reading

- **"Business Process Management: A Practical Guide"** by Rafa Hinojosa — process design fundamentals
- **"The Phoenix Project"** by Gene Kim et al. — why good processes matter at scale
- **Toyota's Standard Work guide** — lean manufacturing approach to documented procedures
- **"An Elegant Puzzle"** by Will Larson (Ch. 6) — how effective teams scale procedures

---

## Next Steps

1. **Audit your most critical SOPs** — Refunds, onboarding, incident response
2. **Run through SOP Scout** — See which criteria are missing
3. **Add AI suggestions** or write your own for gaps
4. **Get team feedback** — Have someone new follow the SOP and mark what confused them
5. **Set a review date** — SOPs get stale; plan quarterly or annual reviews

---

**SOP Scout** is a completeness checklist. Real operational excellence also requires: clear writing, team buy-in, regular practice, and continuous improvement. Use this to ensure nothing critical is forgotten.
