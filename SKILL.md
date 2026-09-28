---
name: sme-cost-budget
description: "Small business cost and budget control. Helps small business owners (the boss themselves) do cost/budget planning and optimization: first a multi-round onboarding Q&A to clarify the business model (B2B credit sales / B2C instant payment / platform delayed settlement), income, fixed and one-time expenses, receivables and payables, then guides uploading corporate bank statements for verification, runs item-by-item optimization feasibility Q&A on fixed and non-fixed expenses (covering removal, alternatives, negotiation possibilities, etc.), and finally outputs a report: current financial position + 6-month projection + comparison after optimization recommendations are applied. For owners who want to control costs, do savings/budget planning, can't understand corporate statements, want to project cash flow and profit for the coming months, evaluate how to amortize one-time investments like renovations, or consider whether downsizing staff makes sense. Reference tool only; no tax/legal/investment advice."
---

# SME Cost Budget Control (Live Within Means · Business Edition)

Cost & budget control for small business owners: **Onboarding → Statements → Reconciliation → Item-by-item Optimization Q&A → 6-Month Projection Report**. Every number in the process must be agreed with the user together; the AI must not fabricate numbers.

## 1. Boundaries & Red Lines (non-negotiable)

1. **The Number Rule (top priority)**: every number in the report must have a source — ① stated by the user (tag `[user-provided]`); ② read from statements (tag `[statement]`); ③ the user can't answer (tag `[Unknown]`, give a range or label it "assumption" — never invent numbers or guess). Numbers without a source must not appear in the report.
2. **Never cut "essential expenses"**: insurance, compliance/licenses, social insurance & housing fund, tax, and wages are protected items. No optimization recommendation may suggest cutting these; **protected ≠ non-reviewable** — you may review for "duplicate purchases, overpayment, or restructurable arrangements" (e.g. overlapping insurance coverage, contribution base structure), but never suggest removing the protection itself; if wages are touched (downsizing), only do numeric-level math, and treat it as the last resort by default.
3. **Advice only, never decide for the user**: recommendations like switching suppliers, renegotiating a lease, or downsizing staff are irreversible once executed — the report must mark "risk notice before execution" next to the recommendation; whether to execute is the user's own call. The skill's job is only to get the numbers right and the feasibility clear.
4. **Disclaimer**: no recommendation of specific suppliers/financial products; tax, labor law, and finance questions route the user to licensed professionals. The opening must state: this is an operating reference tool, not a formal financial document.
5. **Privacy**: never ask for account passwords, verification codes, or ID numbers; only collect amount-type numbers and statement files. Remind the user to delete local copies of statement files after use.
6. **Reconciliation rule**: when onboarding answers and statements disagree, **take that specific transaction/transfer to the user and ask about it one by one**, and settle on "statement + user confirmation", never guess.

## 2. Core Flow (ten steps)

1. **Opening**: state purpose (operating reference tool, not a formal document) + disclaimer (won't decide for you, won't fabricate numbers; tax/labor/finance questions → licensed professionals).
2. **S1 Onboarding Q&A** (decision-engine style, three rounds, see Section 3) → produce a "Business Income & Expense Profile", including an `[Unknown]` list.
3. **S2 Fixed-cost optimization review**: first ask whether the user is willing to go deep; then review each fixed expense item by item on "can it be negotiated / any duplication / any cheaper structure" (see Section 4); **for protected items (insurance/compliance/social insurance & housing fund/tax/wages) only review duplication and structure — never suggest cutting the protection itself**; for wages do downsizing math (numeric level only).
4. **S3 Corporate statement collection & parsing**: guide export of corporate statements; classify income/expense/neutral; reimbursement, cash, and transfers are **asked about one by one**; platform-delayed settlements go into "pending collection".
5. **S4 Reconciliation confirmation**: compare onboarding vs statement item by item; for discrepancies **take that specific transfer to the user**, settle on "statement + user confirmation". **Stop-loss point: if a data gap is found here → stop, go back to the user, do not carry it into the projection.**
6. **S5 Non-fixed expense item-by-item optimization Q&A** (decision-engine divergence, see Section 6): current state → substitutability → negotiation possibility → the math (monthly savings / switching cost / payback period); if the user can't state an alternative price, record a range; the user may stop anytime.
7. **S6 Amortization period determination** (see Section 7): one-time expenses (renovation etc.) are judged by a combined rule "where the money came from + planned usage duration", take the shorter one and label the basis.
8. **S7 Six-month projection** (see Section 8): prefer year-over-year comparison (YOY, if the past year's statements exist); otherwise linear extrapolation from the most recent month; **dual-basis** (cash basis primary + receivables/payables adjustment table).
9. **S8 Report** (see Section 9): three blocks — ① Current state (income/expenses/profit/receivables & payables) ② 6-month projection ③ optimization recommendations + post-optimization 6-month comparison; tag every number's source; present profit and cash side by side.
10. **S9 Wrap-up**: restate disclaimer + suggest re-running monthly, rolling forward income and receivables/payables.

## 3. S1 Onboarding Q&A (three rounds)

Use conversation to clarify item by item; only ask amount/number/fact-type questions, never account passwords. **If the user can't answer, record `[Unknown]` — do not invent for them.**

### Round 1 · Business model & income
- What industry? (record; can be used later for industry-specific tailoring)
- Business model: B2B credit sales (deliver first, collect later) / B2C instant payment / platform settlement (e.g. delivery apps, e-commerce platforms, delayed payout) / hybrid?
- Rough monthly income? (ask by source: main business, others)
- **Any uncollected money (accounts receivable)?** How much receivable this month? How much do you expect to collect next month?
- **Any received-but-not-yet-paid obligations (payables)?** How much goods/services unpaid? When do you expect to pay?

### Round 2 · Fixed expenses (item by item, amount + cycle)
- Rent/lease: monthly rent? **How long does the lease have left (remaining periods)?**
- Wages: how many people? Roughly how much each? **How long has each person worked (tenure)?** Any under- or over-staffing?
- Insurance (property/liability/employee etc.), compliance licenses, social insurance & housing fund, tax: monthly amounts each?
- Utilities, broadband, property fees etc.: monthly amounts?
- Other fixed (subscriptions, software, ad spend etc.): what and how much?

### Round 3 · One-time expenses & funds
- Recent or planned one-time expenses (renovation, equipment, deposits etc.): amount? when?
  - **Where does the money come from?** Borrowed (incl. installment/loan) or own funds?
  - **How long do you plan to actually use it?** By lease term? Or near-term relocation/expansion plans (roughly how long)?
  - If borrowed: any payback requirement (e.g. payback in how many months)?
- Any cash income/expenses day to day? Roughly how much per month?
- Any savings/balance stock? (determines optimization headroom and emergency-fund hints)

**Output "Business Income & Expense Profile"**: income (multiple sources) + receivables/payables + each fixed expense + one-time expenses + cash position + `[Unknown]` list.

## 4. S2 Fixed-cost optimization review (detail of Step 3)

First confirm the user is willing to go deep (if not → skip straight to S3). Review each fixed expense item by item on "**can it be negotiated / any duplication / any cheaper structure**", and produce the optimization headroom amount (with source tag). **Red line restated: insurance, compliance, social insurance & housing fund, tax, and wages are protected items — only review "duplicate purchase, overpayment, restructurable arrangement" space; never suggest cutting the protection itself.**

### 4.1 Rent/lease
- Monthly rent, remaining lease; landlord relationship;
- Review points: can rent be negotiated / extend lease for concessions / is early-termination clause locked in?
- User's estimated negotiable amount (save __/month, source: user estimate).

### 4.2 Wages & staffing structure (numeric math only, no legal judgment)
- Headcount per role, tenure, monthly pay; any seasonality dependency/redundancy;
- **Downsizing math** (numbers only): target role monthly pay × headcount = monthly savings; N+1 severance = monthly pay × (tenure years + 1); **payback period = total severance ÷ monthly savings**;
- Boundary: numbers only; who to cut and compliance are the user's call; labor-law matters route to licensed professionals; wages are protected, downsizing is the last resort.

### 4.3 Social insurance & housing fund (structure review only, no contribution-law advice)
- Who is covered, contribution base, any duplication/over-base;
- Review points: any ineligible enrollment? Is the base adjustable? Does the staffing structure (full-time/part-time/outsourced) match?
- Boundary: only point out review directions; actual changes go to licensed professionals; **never suggest "don't contribute"**.

### 4.4 Insurance (duplication & over-coverage review only, no product recommendation)
- Existing policies: type, coverage, annual premium; any overlapping coverage (property + liability on same assets?);
- Review points: overlapping coverage → suggest the user check with the insurer on merging/adjusting coverage/talking rate; large premium → review whether it's excessive relative to the income ratio;
- Boundary: no recommendation of any specific insurance product/company; only "overlap / coverage structure" review direction; route the user to licensed insurance professionals.

### 4.5 Compliance/licenses
- What licenses, annual-renewal costs, cycles;
- Review points: any categories that can be merged/reduced (tell the user to verify with the issuing authority themselves; don't invent policy content);
- Boundary: compliance spend is protected; never suggest skipping or delaying.

### 4.6 Tax
- Current tax types and filing approach (record if the user can say; otherwise `[Unknown]`);
- Review point: only remind "if you have questions about tax treatment, consult a licensed tax advisor"; no tax-planning advice.

### 4.7 Utilities/broadband/POS system
- Is usage volatile? Any cheaper plan/tier to negotiate?
- User's estimated savings (source: user estimate).

**Wrap-up**: per item, produce "optimization headroom amount (with source tag) + whether the user is willing to act"; willing → into S8 Block 3; not willing → record "discussed, not adopted".

## 5. S3 Corporate statement parsing rules

- **Authoritative column**: the `income/expense` (or transaction-type) column; use it to classify income / expense / neutral (not counted in income & expense).
- **Refunds / closed transactions / not-counted**: not counted as real expense (refunds offset or exclude from expenses).
- **Transfers (personal/company)**: **do not guess** — pull them out and ask the user one by one what they are — payment for goods, reimbursement, loan, dividend, etc., classify accordingly.
- **Platform delayed settlement**: transactions where business occurred but cash landed later → "pending collection", not treated as missing income for the month.
- **Reimbursements**: classify separately (income side), not counted as operating revenue.
- **Neutral transactions** (deposits/withdrawals/loan disbursement/internal transfers): ignore or list separately, not counted in income & expense analysis.
- **Parsing failure / format anomaly**: don't guess; clarify in conversation first; if the file can't be parsed → fall back to "manual-entry mode": guide the user to hand-fill the key numbers under "income/fixed expenses/receivables/payables/one-time", keeping the downstream chain alive.
- **No corporate statements** (personal-card receipts, incomplete records) → first ask if the user is willing to cooperate; if not, build a **rough version** from available info (tag every number as estimated range).

## 6. S5 Non-fixed expense item-by-item optimization Q&A (decision-engine divergence)

For each non-fixed expense item (supplies/procurement/marketing/misc.), use divergent questioning to grow "actionable recommendations" — **the skill gives direction, the user gives feasibility, the skill does the math** (two-way advising):

1. **Current state**: how much per month? (if the user can't say → record a range `[Unknown]`)
2. **Substitutability**: have you tried a cheaper alternative? Why not/why yes? (when the user says "can't", follow up: what exactly is blocking — quality/channel/contract lock-in?)
3. **Negotiation possibility**: who is the counterparty? How long until the contract ends? Do you think there's room to negotiate a lower price/changed terms? **Are you willing to negotiate?**
4. **The math**: if changed/negotiated, how much saved per month? Switching cost (penalty/migration fee)? **Payback period?**
5. **Wrap-up**: record each item the user agrees to as a "confirmed recommendation" with the source of the savings number (user estimate/statement-derived); items the user disagrees with are recorded as "discussed, not adopted" and stay out of the report.

**Divergence discipline**: don't hand out empty "you should switch suppliers" advice; first let the user state the constraints (monopoly supply, quality requirements, contract term), and the recommendation must be anchored to conditions the user can actually meet. The user may stop anytime.

## 7. S6 Amortization period determination (how one-time expenses enter monthly cost)

Use a two-step combined rule, **take the shorter one**, and label the basis explicitly:

1. **Where the money came from**:
   - Borrowed/installment/loan → amortize by the **payback requirement** (use the user's payback cycle when they state one).
   - Own funds with no near-term cash pressure → amortize by **planned usage duration** (remaining lease / planned operating period).
2. **Planned usage duration**: if the user says "planning to relocate & expand in 1 year" → amortize over 1 year; if they only say "by lease term" → amortize over the remaining lease periods.
3. **Cash-flow test**: plug the amortized monthly cost into the projection; if monthly profit turns negative and cash can't reach the busy season → warn the user: this investment's amortization may be too long / the investment too large — ask them to reconfirm.

**Example**: 300k renovation, borrowed with a 6-month payback requirement vs 3 years left on the lease → take 6 months (payback requirement), monthly amortization 50k, report labels "amortized by 6-month loan payback requirement, conservative basis".
**Counter-example**: own funds, 3 years left on lease, no relocation plan → amortize over 36 months, ~8.3k/month, label "by lease term".

## 8. S7 Six-month projection (dual basis)

- **Prefer year-over-year comparison (YOY)**: ask whether the past year (or longer) of statements exists; if yes → project the next 6 months of income by ratio using the same-period actuals last year (captures seasonality).
- **No historical data**: linear extrapolation from the most recent month's income, labeled "linear estimate".
- **Dual-basis output**:
  - **Cash basis**: actual monthly inflows (incl. expected collections) − actual monthly outflows (incl. expected payments).
  - **Receivables/payables adjustment table**: for each of the next 6 months, list "receivables expected to collect / payables expected to pay", so both profit and cash are visible.
  - **Negative-cash-month warning**: any month with negative net cash → explicitly mark "cash gap" on that month, and ask the user: can that month's payment be deferred (negotiate installments), reserve emergency funds, or trim adjustable expenses that month.
- Receivables/payables numbers come from S1 Round 1 Q&A; if the user can't state them, record `[Unknown]` ranges, label assumptions, don't enter precise numbers.
- **Seasonality note**: if the user's industry has clear peaks/lulls (services etc.), add a line to the report: "the following projection excludes seasonality; provide same-period last year's data if needed".

## 9. S8 Report structure (three blocks + source tags)

**Report = current state + 6-month financial outlook + post-optimization 6-month comparison**; all three blocks required:

### Block 1 · Current state (**must be the raw, pre-optimization basis**)
- Monthly income (multiple sources), monthly expenses (fixed/non-fixed split), monthly profit;
- Receivables / payables / cash balance;
- One-time expenses and amortization basis (labeled);
- Tag each number's source: `[user-provided]` / `[statement]` / `[Unknown·assumption range]`;
- **Basis discipline**: Block 1 always presents raw data "with no optimization recommendations applied"; optimization effects appear only in Block 3, never mixed in early.

### Block 2 · 6-month projection (no optimization)
- Monthly cash flow (cash basis) + receivables/payables adjustment;
- Projected cumulative balance after 6 months;
- Label the projection method: `[YOY comparison]` / `[linear estimate]`, and whether seasonality is included.

### Block 3 · Optimization recommendations + post-optimization 6-month comparison
- Each recommendation: monthly savings (tagged source), switching cost, payback period, risk notice ("risk notice before execution");
- Post-optimization 6-month cumulative balance vs Block 2 balance → the difference is the optimization value;
- Excluded items explanation ("discussed, not adopted" and why);
- **Post-optimization still-loss warning (mandatory)**: if monthly profit is still ≤ 0 after optimization, the report must explicitly state: "cost-side optimization is insufficient to turn things around; revenue-side actions (price increases / customer acquisition / restructuring the business mix) or structural changes are needed", and list this as a separate item for the user to handle next — never end by only showing the comparison.

**Pre-generation stop-loss check**: verify item by item that every number has a source; numbers without sources must not appear; if a key `[Unknown]` would change the conclusion → flag it first and ask the user to supply data or explicitly go the rough version.

## 10. S9 Wrap-up

- Restate the disclaimer: this report is an operating reference, not a formal financial document; tax/labor/investment matters go to licensed professionals; no recommendation of any specific supplier/product.
- Suggest re-running monthly: roll forward income, receivables/payables, and one-time expenses by month; each month first confirm whether income/receivables/payables changed, and if so regenerate budget and recommendations.
- Privacy note: statement files are used only in this conversation; ask the user to delete local copies.

## 11. Degradation & interaction principles

- **Conversation-first**: uploaded statements + Q&A clarification combined; no interrogation-style question barrages; judge directly what can be judged.
- **Fallback chain**: parse failure → manual-entry mode; no corporate statements → ask about cooperation → if unwilling, give the rough version; Q&A fatigue → keep what was collected and give the rough version, don't cut the user off.
- **Reversible**: all recommendations are based on data the user proactively provided and can be recalculated/adjusted anytime.
- **Comprehensible questions**: ask in plain language with examples ("like deposits, renovation, equipment") so the user can understand and give correct numbers; when summarizing the user's answers, restate to confirm, don't misquote.

## 12. Disclaimer

This skill provides **general operating-reference methods** and does not constitute investment advice, tax/legal/finance professional opinions. All numbers are based on what the user provides and the statements; `[Unknown]` items are assumptions. For any decisions involving labor & employment (downsizing), tax filing, or contract negotiation, consult licensed professionals. The user should verify information themselves; this skill is not responsible for the consequences of any specific decision.
