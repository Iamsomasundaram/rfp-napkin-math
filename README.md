# IT Services RFI/RFP Napkin Math Cheat Sheet

A practical back-of-the-envelope estimation guide for IT services proposals, RFI responses, RFP estimates, managed services deals, application support, AI/automation proposals, and transformation programs.

This is not a replacement for detailed estimation. It is a quick-reference framework to check whether effort, staffing, pricing, and business case assumptions are directionally reasonable.

---

## 0. Core Idea

In system design, we use napkin math to estimate traffic, storage, latency, throughput, and scaling.

In IT services RFI/RFP preparation, we need similar napkin math for:

* Effort conversion
* Team sizing
* Volumetric assumptions
* Resource loading
* QA / PM / DevOps ratios
* Support sizing
* Pricing
* Margin
* ROI / payback
* Transition
* SLA exposure
* Bid/no-bid decisions
* Commercial assumptions

The overall flow is:

```text
Volumetrics
→ Sizing
→ Effort
→ Resource Loading
→ Cost
→ Price
→ ROI
→ Commercial Protection
```

---

# 1. Effort Conversion

## 1.1 Standard conversions

| Unit                |           Conversion |
| ------------------- | -------------------: |
| 1 person-day, PD    |              8 hours |
| 1 person-month, PM  |                20 PD |
| 1 person-month      |            160 hours |
| 1 FTE for 6 months  |   120 PD / 960 hours |
| 1 FTE for 12 months | 240 PD / 1,920 hours |

## 1.2 Formulas

```text
Hours = Person Days × 8

Person Days = Hours ÷ 8

Person Months = Person Days ÷ 20

FTE required = Total Person Days ÷ Duration in working days

Working days = Number of months × 20
```

## 1.3 Example

```text
Total effort = 1,200 PD
Duration = 6 months
Working days = 6 × 20 = 120 days

Required average FTE = 1,200 ÷ 120 = 10 FTE
```

So, **1,200 PD over 6 months requires around 10 average FTE**.

---

# 2. Effort vs Duration vs Team Size

This is one of the most important proposal sanity checks.

```text
Total Effort = Team Size × Duration in Months × Working Days per Month
```

Example:

```text
Team size = 8 FTE
Duration = 6 months
Working days/month = 20

Total capacity = 8 × 6 × 20 = 960 PD
```

If someone claims that **8 people can deliver 1,500 PD in 6 months**, the plan is not realistic unless they assume overtime, higher team size, or a longer duration.

---

# 3. PD / PM / Hours Reference Table

| Effort Type   | Person-days | Person-months |      Hours |
| ------------- | ----------: | ------------: | ---------: |
| Small work    |       20 PD |          1 PM |    160 hrs |
| Medium work   |      100 PD |          5 PM |    800 hrs |
| Large work    |      500 PD |         25 PM |  4,000 hrs |
| Program size  |    1,000 PD |         50 PM |  8,000 hrs |
| Large program |    5,000 PD |        250 PM | 40,000 hrs |

---

# 4. Full Delivery Effort Composition

Development effort is not total project effort.

A proper estimate usually includes:

```text
Total Effort =
Development
+ QA
+ BA
+ Architecture
+ DevOps
+ PM / Scrum
+ Documentation
+ UAT support
+ Hypercare
+ Contingency
```

## 4.1 Common effort ratios

| Workstream                |            Napkin Ratio |
| ------------------------- | ----------------------: |
| Development               |           100% baseline |
| QA / Testing              |   15%–30% of dev effort |
| BA / Requirement Analysis |   10%–20% of dev effort |
| Solution Architecture     |    5%–10% of dev effort |
| DevOps / Release          |    5%–10% of dev effort |
| PM / Scrum Master         | 10%–15% of total effort |
| UAT Support               |      5%–10% of dev + QA |
| Documentation / KT        |   3%–8% of total effort |
| Contingency               | 10%–20% of total effort |

## 4.2 Example

```text
Development effort = 1,000 PD

QA @ 25% = 250 PD
BA @ 15% = 150 PD
Architecture @ 8% = 80 PD
DevOps @ 7% = 70 PD

Subtotal = 1,550 PD

PM @ 12% = 186 PD
Documentation @ 5% = 78 PD
Contingency @ 15% = 272 PD

Total effort ≈ 2,086 PD
```

So a **1,000 PD development estimate** can easily become a **2,000+ PD full delivery estimate**.

---

# 5. QA Effort Rule of Thumb

| Situation                                           |          QA Ratio |
| --------------------------------------------------- | ----------------: |
| Minor enhancement / low-risk change                 |    10%–15% of dev |
| Normal application enhancement                      |    20%–25% of dev |
| Complex workflow / integration-heavy                |    25%–35% of dev |
| Regulated / banking / healthcare / compliance-heavy |    30%–50% of dev |
| AI agent / automation validation                    | 25%–35% or higher |

Formula:

```text
QA Effort = Development Effort × QA %
```

Example:

```text
Dev effort = 800 PD
QA @ 25% = 200 PD
```

---

# 6. Contingency and Risk Buffer

## 6.1 Contingency range

| Risk Level                           | Contingency |
| ------------------------------------ | ----------: |
| Clear scope, known technology        |      5%–10% |
| Normal RFP uncertainty               |     10%–15% |
| Multiple integrations / unknown APIs |     15%–25% |
| Legacy systems / poor documentation  |     20%–30% |
| Fixed-price bid with unclear scope   |        20%+ |

Formula:

```text
Contingency = Base Effort × Contingency %
```

Example:

```text
Base effort = 1,500 PD
Contingency @ 15% = 225 PD

Total = 1,725 PD
```

## 6.2 Contingency vs risk premium

| Item               | Meaning                                          |
| ------------------ | ------------------------------------------------ |
| Contingency        | Handles normal estimation uncertainty            |
| Risk premium       | Handles commercial / contractual / delivery risk |
| Management reserve | Internal buffer, not always shown to client      |

Avoid double-counting contingency, risk premium, and margin.

---

# 7. Volumetric Assumptions

Volumetrics are general RFI/RFP sizing assumptions. They are not only for AI ROI.

They are used to estimate:

* Support team size
* Ticket handling capacity
* Shift coverage
* Testing capacity
* BPO transaction capacity
* Command center load
* SLA feasibility
* Pricing bands
* Delivery model

## 7.1 Proposal lifecycle usage

| Stage                | How to use volumetrics                                            |
| -------------------- | ----------------------------------------------------------------- |
| RFI                  | Use industry benchmark assumptions for indicative sizing          |
| RFP                  | Replace assumptions with client-provided actuals                  |
| BAFO / final pricing | Lock assumptions, volume bands, exclusions, SLA and pricing basis |

## 7.2 Safe wording

Use this type of wording:

> Since actual monthly volumes are not available at this stage, we have assumed 300–500 L1 tickets per agent per month for indicative sizing. This assumption should be validated during discovery / due diligence.

Avoid saying:

> Industry standard is 400 tickets per agent.

Benchmarks vary based on ticket complexity, tooling maturity, geography, automation, SLA, documentation quality, and support process maturity.

---

# 8. Service Desk / Application Support Volumetrics

| Metric                                 | Indicative Assumption |
| -------------------------------------- | --------------------: |
| L1 tickets / agent / month             |               300–500 |
| L2 tickets / engineer / month          |               100–200 |
| L3 tickets / engineer / month          |                 30–80 |
| L1 first-contact resolution            |               60%–80% |
| Productive support hours / FTE / month |           120–140 hrs |
| Full working hours / FTE / month       |               160 hrs |
| Simple ticket AHT                      |            10–20 mins |
| Medium ticket AHT                      |            30–60 mins |
| Complex ticket AHT                     |               2–8 hrs |

## 8.1 Ticket-based sizing

```text
Required FTE =
Monthly Ticket Volume ÷ Tickets per FTE per Month
```

Example:

```text
Monthly L1 tickets = 3,000
Productivity assumption = 400 tickets / L1 agent / month

L1 FTE = 3,000 ÷ 400 = 7.5

Round to 8 L1 FTE
```

## 8.2 AHT-based sizing

```text
Required FTE =
Monthly Volume × Average Handling Time
÷ Productive Hours per FTE
```

Example:

```text
Monthly tickets = 4,000
Average handling time = 20 mins = 0.33 hrs
Productive hours/FTE/month = 130

FTE = 4,000 × 0.33 ÷ 130
    = 10.15

Round to 10–11 FTE
```

---

# 9. Command Center / NOC / SOC Volumetrics

| Metric                             | Indicative Assumption |
| ---------------------------------- | --------------------: |
| FTE per pod / shift                |                  6–10 |
| Alert-to-actionable-incident ratio |        100:1 or worse |
| Actionable incidents               |       1%–5% of alerts |
| Alert noise reduction potential    |      30%–50% year one |
| Auto-remediation of known issues   |      20%–40% year one |
| P1 MTTR                            |             1–4 hours |
| P2 MTTR                            |             4–8 hours |
| P3 MTTR                            |              1–3 days |

For command centers, do not look only at FTE reduction. The value drivers are usually:

```text
Alert noise reduction
+ Faster triage
+ Auto-remediation
+ Lower MTTR
+ Reduced escalations
+ Fewer SLA breaches
+ Improved operational visibility
```

---

# 10. QA / Testing Volumetrics

| Metric                             |              Indicative Assumption |
| ---------------------------------- | ---------------------------------: |
| Manual test cases / tester / day   |                              40–80 |
| Automated scripts / engineer / day |                                3–8 |
| Automation maintenance             | 15%–25% of automation build effort |
| Regression automation target       |           60%–80% of critical path |
| Defect leakage target              |                                <5% |
| QA effort vs dev effort            |                            20%–30% |

## 10.1 Test execution sizing

```text
Tester Days =
Number of Test Cases ÷ Test Cases Executed per Tester per Day
```

Example:

```text
Regression test cases = 2,000
Productivity = 50 cases / tester / day

Tester effort = 2,000 ÷ 50 = 40 tester-days
```

With 5 testers:

```text
Duration = 40 ÷ 5 = 8 working days
```

---

# 11. BPO / Back-office Volumetrics

| Metric                   | Indicative Assumption |
| ------------------------ | --------------------: |
| Transactions / FTE / day |                50–150 |
| Medium-complexity AHT    |             5–15 mins |
| Semi-automated STP rate  |               40%–60% |
| Mature STP rate          |                  80%+ |
| Rework rate              |                5%–15% |

## 11.1 Transaction-based sizing

```text
Required FTE =
Daily Transaction Volume ÷ Transactions per FTE per Day
```

Example:

```text
Monthly transactions = 60,000
Working days = 22

Daily transactions = 60,000 ÷ 22 = 2,727

Productivity = 100 transactions / FTE / day

Required FTE = 2,727 ÷ 100 = 27.3

Round to 28 FTE
```

---

# 12. Shift Coverage Math

Useful for 8x5, 16x5, 24x7, command center, service desk, NOC and SOC deals.

| Coverage Requirement | Rule of Thumb |
| -------------------- | ------------: |
| 8x5 one seat         |     1–1.2 FTE |
| 16x5 one seat        |   2.2–2.5 FTE |
| 24x7 one seat        |   4.5–5.5 FTE |

Example:

```text
Need 2 people available 24x7

Required FTE = 2 × 5 = 10 FTE
```

---

# 13. Application Development / Enhancement Sizing

## 13.1 Change request sizing

| CR Size       | Typical Effort |
| ------------- | -------------: |
| Small CR      |         3–5 PD |
| Medium CR     |        8–15 PD |
| Large CR      |       20–40 PD |
| Very large CR |         50+ PD |

## 13.2 Monthly enhancement capacity example

```text
10 small CRs × 4 PD = 40 PD
5 medium CRs × 12 PD = 60 PD
2 large CRs × 30 PD = 60 PD

Monthly enhancement effort = 160 PD
```

Required team:

```text
160 PD ÷ 20 working days = 8 FTE
```

---

# 14. Resource Loading

Aggregate FTE tells whether effort is possible. Resource loading tells who is needed and when.

Real delivery is usually an S-curve:

```text
Ramp up
→ Peak delivery
→ Ramp down
```

## 14.1 Monthly loaded PD formula

```text
Loaded PD in a month =
FTE allocation × Working days in that month
```

Example:

```text
1 full-time person in a 20-working-day month = 20 PD
50% allocation = 10 PD
25% allocation = 5 PD
```

## 14.2 Average FTE vs peak FTE

| Metric            | Meaning                                  |
| ----------------- | ---------------------------------------- |
| Average FTE       | Total effort / duration view             |
| Peak FTE          | Maximum delivery capacity needed         |
| Monthly loading   | Staffing by month                        |
| Role-wise loading | PM, BA, Dev, QA, DevOps, Architect split |
| Location loading  | Onsite / offshore / nearshore split      |

Rule of thumb:

```text
Peak FTE ≈ Average FTE × 1.2 to 1.5
```

Example:

```text
Average FTE = 10
Peak multiplier = 1.3

Peak FTE = 13
```

So a proposal may show **10 average FTE**, but delivery may need **13 people at peak**.

## 14.3 Example loading curve

For a 6-month project:

| Month | Loading Pattern |
| ----- | --------------: |
| M1    |         40%–60% |
| M2    |         70%–90% |
| M3    |            100% |
| M4    |            100% |
| M5    |        80%–100% |
| M6    |         40%–70% |

---

# 15. Role-wise Resource Loading

A proper RFP resource plan should show who is needed by month.

Example:

| Role               | M1 |  M2 |  M3 |  M4 |  M5 | M6 | Total PD |
| ------------------ | -: | --: | --: | --: | --: | -: | -------: |
| PM / Scrum Master  | 10 |  15 |  20 |  20 |  20 | 15 |      100 |
| Solution Architect | 15 |  15 |  10 |   5 |   5 |  5 |       55 |
| BA                 | 20 |  20 |  15 |  10 |   5 |  5 |       75 |
| Developers         | 40 | 100 | 160 | 160 | 140 | 60 |      660 |
| QA                 | 10 |  30 |  80 | 100 | 100 | 60 |      380 |
| DevOps             |  5 |  10 |  15 |  20 |  20 | 15 |       85 |

This helps validate:

* Is architecture front-loaded?
* Is QA starting early enough?
* Is DevOps included?
* Is PM/governance realistic?
* Is hypercare covered?
* Is the peak month achievable?

---

# 16. Pyramid and Blended Rate

A blended rate is calculated from role mix, location mix, experience pyramid, and rate card.

## 16.1 Formula

```text
Blended Rate =
Σ(Role Mix % × Role Rate)
```

## 16.2 Example

| Level  |  Mix | Rate/hr | Weighted Rate |
| ------ | ---: | ------: | ------------: |
| Junior |  50% |     $25 |        $12.50 |
| Mid    |  35% |     $40 |        $14.00 |
| Senior |  15% |     $65 |         $9.75 |
| Total  | 100% |         |     $36.25/hr |

So the blended rate is **$36.25/hr**.

## 16.3 Onsite-offshore blended rate

| Location | FTE | Rate/month | Monthly Billing |
| -------- | --: | ---------: | --------------: |
| Onsite   |   2 |    $12,000 |         $24,000 |
| Offshore |   8 |     $4,000 |         $32,000 |
| Total    |  10 |            |         $56,000 |

Blended monthly rate:

```text
Blended Monthly Rate =
Total Monthly Billing ÷ Total FTE

= 56,000 ÷ 10
= $5,600 per FTE/month
```

Blended hourly rate:

```text
Blended Hourly Rate =
Monthly Rate ÷ 160

= 5,600 ÷ 160
= $35/hr
```

---

# 17. Utilization vs Loading vs Billability

| Term         | Meaning                                            |
| ------------ | -------------------------------------------------- |
| Loading      | How much a person is allocated to a project        |
| Utilization  | How much available capacity is productive/billable |
| Billability  | Whether the client is charged for the time         |
| Productivity | Output delivered per unit of time                  |

Example:

```text
Client needs 10 billable FTE
Expected utilization = 85%

Internal headcount needed =
10 ÷ 0.85
= 11.76

Round to 12 people
```

So to bill 10 FTE consistently, the vendor may need around 12 people on payroll.

---

# 18. Attrition and Backfill

Mostly used for internal planning and managed service contracts.

## 18.1 Hidden backfill gap

```text
Hidden backfill gap =
Average FTE × Attrition % × Backfill months ÷ 12
```

Example:

```text
Average FTE = 10
Attrition = 20%
Backfill time = 2 months

Hidden gap =
10 × 20% × 2 ÷ 12
= 0.33 FTE
```

## 18.2 Re-KT effort

```text
Re-KT effort = 3–5 PD per exit
```

---

# 19. Pricing Models

## 19.1 Common pricing models

| Model                 | Formula                             | Best Used When                        |
| --------------------- | ----------------------------------- | ------------------------------------- |
| T&M                   | Hours × Rate                        | Scope is evolving                     |
| Monthly FTE           | FTE × Monthly Rate × Duration       | Staff augmentation / managed capacity |
| Fixed Price           | Fully Loaded Cost ÷ (1 − Margin %)  | Scope is well defined                 |
| NTE                   | T&M capped at ceiling               | Flexibility with budget control       |
| Managed Service       | Base monthly fee + variable volume  | Support / operations                  |
| Per-ticket / Per-unit | Unit price × Volume                 | Service desk, BPO, transaction work   |
| Outcome-based         | Base fee + share of value delivered | Automation / transformation           |
| Subscription          | Monthly platform/service fee        | AI agent / SaaS-like service          |
| Hybrid                | Base fee + variable component       | Uncertain or changing volumes         |

---

# 20. T&M and Monthly FTE Billing

## 20.1 Hourly billing

```text
Billing = Hours × Hourly Rate
```

Example:

```text
Effort = 1,000 PD
Hours = 1,000 × 8 = 8,000 hrs
Rate = $35/hr

Billing = 8,000 × 35 = $280,000
```

## 20.2 Monthly FTE billing

```text
Billing =
FTE Count × Monthly Rate × Duration
```

Example:

```text
Team = 10 FTE
Rate = $5,000 / FTE / month
Duration = 6 months

Billing = 10 × 5,000 × 6
= $300,000
```

---

# 21. Fixed Price Pricing

## 21.1 Recommended formula

```text
Fixed Price =
Fully Loaded Cost ÷ (1 − Target Margin %)
```

Fully loaded cost may include:

```text
Base delivery cost
+ Contingency
+ Transition cost
+ Tooling cost
+ Governance cost
+ Risk premium
```

Example:

```text
Base delivery cost = $700,000
Contingency = $100,000
Risk premium = $50,000

Fully loaded cost = $850,000

Target margin = 30%

Fixed price =
850,000 ÷ 0.70
= $1,214,286
```

## 21.2 Fixed-price risk premium

| Situation                        | Premium |
| -------------------------------- | ------: |
| Clear scope                      |  5%–10% |
| Normal fixed-price risk          | 10%–20% |
| Unclear scope / integration risk |    20%+ |

---

# 22. Managed Service / Volume-band Pricing

Useful for support, BPO and operations.

## 22.1 Formula

```text
Monthly Price =
Base Fee + Additional Volume × Unit Rate
```

## 22.2 Example

|      Monthly Volume | Price Model                  |
| ------------------: | ---------------------------- |
|     0–3,000 tickets | Base fee                     |
| 3,001–5,000 tickets | Base fee + per-ticket charge |
|      5,001+ tickets | Repricing / change control   |

Example calculation:

```text
Base fee covers 3,000 tickets = $50,000/month
Actual volume = 3,500 tickets
Additional tickets = 500
Extra ticket rate = $8

Monthly price =
50,000 + 500 × 8
= $54,000
```

---

# 23. Change Request Pricing

CRs often cost more than planned BAU work because they involve context switching, analysis, regression, release coordination and governance.

```text
CR Rate =
BAU Rate × 1.2 to 1.5
```

Example:

```text
BAU blended rate = $35/hr
CR premium = 1.3

CR rate = 35 × 1.3 = $45.50/hr
```

---

# 24. Margin vs Markup

This is a must-know commercial concept.

## 24.1 Margin

```text
Margin % =
(Price − Cost) ÷ Price
```

## 24.2 Markup

```text
Markup % =
(Price − Cost) ÷ Cost
```

## 24.3 Example

```text
Cost = $100
Target margin = 30%

Price =
100 ÷ (1 − 0.30)
= 100 ÷ 0.70
= $142.86
```

Here:

```text
Margin = 30%
Markup = 42.86%
```

If someone applies 30% markup:

```text
Price = 100 × 1.30 = $130
```

Then margin is only:

```text
Margin =
(130 − 100) ÷ 130
= 23.1%
```

Always clarify whether people mean **margin** or **markup**.

---

# 25. Revenue, Cost and Margin

## 25.1 Gross margin

```text
Gross Margin % =
(Revenue − Delivery Cost) ÷ Revenue × 100
```

Example:

```text
Revenue = $300,000
Delivery cost = $210,000

Gross Margin =
(300,000 − 210,000) ÷ 300,000 × 100
= 30%
```

## 25.2 Price from cost and target margin

```text
Price =
Cost ÷ (1 − Target Margin %)
```

Example:

```text
Cost = $210,000
Target margin = 30%

Price =
210,000 ÷ 0.70
= $300,000
```

---

# 26. Escalation, Inflation and FX

Useful for multi-year deals.

## 26.1 Escalation formula

```text
Year N Rate =
Year 1 Rate × (1 + Escalation %) ^ (N − 1)
```

Example:

```text
Year 1 rate = $40/hr
Escalation = 6%

Year 2 = 40 × 1.06 = $42.40
Year 3 = 40 × 1.06² = $44.94
```

## 26.2 Typical assumptions

| Item                             | Napkin Assumption |
| -------------------------------- | ----------------: |
| Annual escalation                |             3%–7% |
| Offshore salary inflation buffer |             5%–8% |
| FX buffer                        |             3%–5% |
| Fixed-price risk premium         |           10%–20% |
| Multi-year discount              |            5%–10% |
| Strategic discount               |           10%–20% |

Discounts should always be checked against margin impact.

---

# 27. ROI / Payback Math

Used to validate whether the investment makes business sense.

## 27.1 Payback

```text
Payback in months =
Investment ÷ Net Monthly Benefit
```

Where:

```text
Net Monthly Benefit =
Monthly Savings or Gain − Monthly Run Cost
```

Example:

```text
Investment = $2,000,000
Monthly savings = $54,000
Monthly run cost = $15,000

Net monthly benefit =
54,000 − 15,000
= $39,000

Payback =
2,000,000 ÷ 39,000
= 51.3 months
```

This is a weak payback if the only benefit is labor saving.

## 27.2 Adjusted benefit with ramp and confidence

More realistic for AI, automation and transformation programs:

```text
Adjusted Monthly Benefit =
Gross Monthly Benefit × Ramp % × Confidence %
− Monthly Run Cost
```

Example:

```text
Gross monthly benefit = $100,000
Ramp = 70%
Confidence = 80%
Run cost = $15,000

Adjusted Monthly Benefit =
100,000 × 0.70 × 0.80 − 15,000
= 56,000 − 15,000
= $41,000
```

## 27.3 Three-year ROI

```text
3-Year ROI % =
(3-Year Net Benefit − Investment) ÷ Investment × 100
```

Example:

```text
Investment = $1,000,000
Adjusted monthly net benefit = $60,000

3-year net benefit =
60,000 × 36
= $2,160,000

3-Year ROI =
(2,160,000 − 1,000,000) ÷ 1,000,000 × 100
= 116%
```

---

# 28. Benefit Archetypes

The investment side often looks similar across proposals. The benefit side changes by use case.

| Archetype              | Formula                                        | Caution                                  |
| ---------------------- | ---------------------------------------------- | ---------------------------------------- |
| Headcount takeout      | Team size × Automation % × Cost/FTE/month      | Strong only if cost is actually removed  |
| Avoided hiring         | Avoided hires × Cost/FTE/month                 | Often easier to justify than layoffs     |
| Productivity gain      | Hours saved × Cost/hour                        | Soft benefit unless capacity is reused   |
| Revenue enablement     | Incremental revenue × Gross margin %           | Use margin, not top-line revenue         |
| SLA / quality          | Avoided penalties + rework reduction           | Needs historical data                    |
| Risk avoidance         | Probability × Incident cost × Risk reduction % | Use realistic probability                |
| Transaction automation | Volume × Saving/unit                           | Best for BPO / claims / invoices / docs  |
| Platform reuse         | Reused benefit across teams/sites              | Important for large platform investments |

---

# 29. Hard vs Soft Benefits

| Benefit Type      | Example                                                  | How to Treat                   |
| ----------------- | -------------------------------------------------------- | ------------------------------ |
| Hard benefit      | Vendor cost reduction, license reduction, avoided hiring | Count in ROI                   |
| Semi-hard benefit | Lower overtime, fewer escalations, reduced rework        | Count with discount            |
| Soft benefit      | Better user experience, faster reporting                 | Mention separately             |
| Risk benefit      | Avoided outage, avoided audit issue                      | Use probability-adjusted value |

Important rule:

```text
Productivity saving is not always financial saving.
```

Example:

```text
10 people save 1 hour/day
= 10 × 1 × 22
= 220 hours/month saved
```

This becomes financial value only if:

```text
Cost is actually reduced
or hiring is avoided
or more work is completed with same team
or SLA penalties are avoided
or revenue-generating work increases
```

---

# 30. AI / Automation TCO

AI run cost should not be ignored. Tokens are only one part of the cost.

## 30.1 Token cost formula

```text
Token Cost =
Requests/month × Tokens/request ÷ 1,000 × Cost per 1K tokens
```

Example:

```text
Requests/month = 50,000
Tokens/request = 3,000
Cost = $0.01 per 1K tokens

Token Cost =
50,000 × 3,000 ÷ 1,000 × 0.01
= $1,500/month
```

## 30.2 Full AI run cost

```text
AI Monthly Run Cost =
LLM token cost
+ Embedding cost
+ Vector DB
+ Hosting
+ Storage
+ Monitoring
+ LLM gateway
+ Guardrails
+ Evaluation runs
+ Human review
+ Prompt/model maintenance
+ Security monitoring
+ Support team
```

| Cost bucket   | What to include                                               |
| ------------- | ------------------------------------------------------------- |
| LLM inference | Input tokens, output tokens, cached tokens if applicable      |
| Embeddings    | Document indexing, query embeddings, re-indexing              |
| Vector DB     | Storage, compute, search/query cost                           |
| Orchestration | Agent runtime, workflow engine, tool-calling layer            |
| Hosting       | App servers, containers, serverless, API gateway              |
| Monitoring    | Logs, traces, prompt observability, dashboards                |
| Evaluation    | Regression prompt sets, hallucination checks, quality scoring |
| Guardrails    | PII masking, policy checks, content filters                   |
| Security      | Access control, audit logs, secrets, vulnerability scanning   |
| Human review  | HITL queue, SME validation, fallback support                  |
| Maintenance   | Prompt tuning, model upgrades, KB refresh, retraining         |
| Support       | L2/L3 support, incident handling, runbook updates             |

Total Agent Monthly Run Cost =
Token Cost
+ Platform Cost
+ Data / Vector Cost
+ Monitoring Cost
+ Human Review Cost
+ Support & Maintenance Cost

Do not price AI agents only on build effort.
Agent proposals need both:
1. Build cost
2. Recurring run cost / TCO 

---

# 31. Transition / KT Math

Used for support takeover, AMS, managed services and vendor transition.

| Transition Complexity               |   Duration |
| ----------------------------------- | ---------: |
| Small app support                   |  2–4 weeks |
| Medium portfolio                    |  4–8 weeks |
| Large multi-app portfolio           | 8–12 weeks |
| Complex legacy / poor documentation |  12+ weeks |

Common phases:

```text
KT
Shadow support
Reverse shadow
Runbook creation
Access setup
Tool onboarding
SLA baseline period
Stabilization
Hypercare
```

## 31.1 KT effort example

```text
KT Effort =
Number of Apps × KT Effort per App
```

Example:

```text
30 apps × 5 PD per app = 150 PD
```

---

# 32. Hypercare / Warranty Effort

| Phase                    |              Rule of Thumb |
| ------------------------ | -------------------------: |
| Warranty                 |     5%–10% of build effort |
| Hypercare                |    10%–20% of build effort |
| Production stabilization | 1–2 months of partial team |

Example:

```text
Build effort = 1,000 PD
Hypercare @ 10% = 100 PD
```

---

# 33. SLA Credit Exposure

Used for managed service contracts.

```text
Maximum SLA Credit Exposure =
Monthly Fee × SLA Credit Cap %
```

Example:

```text
Monthly fee = $100,000
SLA credit cap = 10%

Maximum monthly exposure =
100,000 × 10%
= $10,000
```

If SLA penalties are aggressive, pricing should include a risk buffer.

---

# 34. Bid / No-Bid Math

Used before investing heavily in a proposal.

```text
Expected Value =
Win Probability × Expected Margin − Cost of Bid
```

Example:

```text
TCV = $3,000,000
Expected margin = 20%
Margin value = $600,000
Win probability = 25%
Bid cost = $60,000

Expected Value =
25% × 600,000 − 60,000
= 150,000 − 60,000
= $90,000
```

If win probability is 10%:

```text
Expected Value =
10% × 600,000 − 60,000
= 60,000 − 60,000
= $0
```

That becomes a judgment call unless there is strategic value.

---

# 35. Cash Flow / Milestone Billing

For fixed-price deals, revenue timing matters.

Example milestone structure:

| Milestone        | Billing % |
| ---------------- | --------: |
| Contract signing |       10% |
| Design sign-off  |       20% |
| Build complete   |       30% |
| UAT sign-off     |       25% |
| Go-live          |       10% |
| Warranty closure |        5% |

A deal can look profitable on paper but still create cash-flow pressure if billing is back-loaded.

---

# 36. Assumption Register

Every RFP estimate should include an assumption register.

| Category     | Assumption                | Impact if Wrong               |
| ------------ | ------------------------- | ----------------------------- |
| Volume       | 3,000 tickets/month       | FTE and pricing change        |
| Productivity | 400 L1 tickets/FTE/month  | Staffing changes              |
| SLA          | 8x5 support               | Shift model changes           |
| Scope        | 30 applications           | Portfolio size changes        |
| Integration  | APIs available            | Build effort changes          |
| Environment  | Client provides access    | Timeline changes              |
| Data quality | Ticket data is clean      | Analytics / automation impact |
| Tooling      | Client licenses available | Cost impact                   |
| Travel       | Excluded unless stated    | Commercial impact             |
| Cloud cost   | Pass-through              | Pricing impact                |

---

# 37. Commercial Assumptions

Clearly state commercial assumptions in the proposal.

| Area                     | Example Assumption                    |
| ------------------------ | ------------------------------------- |
| Working days             | 20 days/month                         |
| Working hours            | 8 hours/day                           |
| Productive support hours | 120–140 hours/FTE/month               |
| Currency                 | USD / INR / GBP                       |
| FX                       | Fixed or variable                     |
| Taxes                    | Excluded unless stated                |
| Travel                   | Excluded / included separately        |
| Tools                    | Client-provided or vendor-provided    |
| Licenses                 | Charged separately                    |
| Cloud cost               | Pass-through or included              |
| SLA penalties            | Capped or excluded                    |
| Volume                   | Pricing valid up to defined threshold |
| Change requests          | Priced separately                     |
| Warranty                 | Included for defined period           |
| Hypercare                | Included or separately priced         |
| Payment terms            | Monthly / milestone / quarterly       |

---

# 38. RFP Sanity Checks

## 38.1 Effort checks

| Question                                      | Why It Matters                  |
| --------------------------------------------- | ------------------------------- |
| Is total effort converted correctly into FTE? | Avoid impossible delivery plans |
| Is peak FTE shown, not just average FTE?      | Delivery readiness              |
| Is QA effort realistic?                       | Quality risk                    |
| Is PM/governance included?                    | Program control                 |
| Is DevOps/release effort included?            | Deployment risk                 |
| Is UAT/hypercare included?                    | Go-live risk                    |
| Is contingency visible?                       | Risk management                 |

## 38.2 Volumetric checks

| Question                             | Why It Matters     |
| ------------------------------------ | ------------------ |
| Are ticket volumes known or assumed? | Sizing accuracy    |
| Are L1/L2/L3 splits available?       | Team structure     |
| Are peak volumes considered?         | SLA feasibility    |
| Are support hours clear?             | Shift sizing       |
| Are volume bands defined?            | Pricing protection |

## 38.3 Pricing checks

| Question                                     | Why It Matters         |
| -------------------------------------------- | ---------------------- |
| Is pricing model aligned to scope certainty? | Commercial risk        |
| Are margin and markup clearly separated?     | Pricing accuracy       |
| Are discounts shown with margin impact?      | Commercial discipline  |
| Is escalation included for multi-year deals? | Future cost protection |
| Is FX risk handled?                          | Cross-currency risk    |
| Are tooling and license costs included?      | TCO accuracy           |

## 38.4 ROI checks

| Question                                          | Why It Matters              |
| ------------------------------------------------- | --------------------------- |
| Is run cost included?                             | ROI accuracy                |
| Is ramp applied to benefits?                      | Realistic payback           |
| Are hard and soft benefits separated?             | Client trust                |
| Is revenue benefit based on margin, not top line? | Avoid inflated ROI          |
| Is labor saving actually realizable?              | Prevent false business case |
| Is platform reuse considered?                     | Large build justification   |

## 38.5 Commercial protection checks

| Question                          | Why It Matters       |
| --------------------------------- | -------------------- |
| Are assumptions documented?       | Protects estimate    |
| Are exclusions clear?             | Prevents scope creep |
| Are SLA penalties capped?         | Limits exposure      |
| Is change control defined?        | Protects margin      |
| Is transition separately priced?  | Avoids underpricing  |
| Is bid/no-bid economics positive? | Sales discipline     |

---

# 39. Useful Number Conversions

|       Value |             Equivalent |
| ----------: | ---------------------: |
|       1,000 |             1 thousand |
|     100,000 |                 1 lakh |
|   1,000,000 |              1 million |
|  10,000,000 |   10 million / 1 crore |
| 100,000,000 | 100 million / 10 crore |

Examples:

```text
$250,000 = $0.25M
$1,500,000 = $1.5M
₹50,00,000 = ₹50 lakh
₹1,00,00,000 = ₹1 crore
₹10 crore = ₹100 million
```

Shortcut:

```text
To convert to million:
Amount ÷ 1,000,000

2,750,000 = 2.75M
```

---

# 40. Final RFP Napkin Math Summary

| Area                     | Quick Rule                          |
| ------------------------ | ----------------------------------- |
| PD to hours              | PD × 8                              |
| PD to PM                 | PD ÷ 20                             |
| PM to hours              | PM × 160                            |
| Average FTE              | Total PD ÷ working days             |
| Peak FTE                 | Average FTE × 1.2 to 1.5            |
| QA effort                | 20%–30% of dev                      |
| BA effort                | 10%–20% of dev                      |
| DevOps effort            | 5%–10% of dev                       |
| PM effort                | 10%–15% of total                    |
| Contingency              | 10%–20%                             |
| L1 productivity          | 300–500 tickets/FTE/month           |
| L2 productivity          | 100–200 tickets/FTE/month           |
| L3 productivity          | 30–80 tickets/FTE/month             |
| Support productive hours | 120–140 hrs/FTE/month               |
| 24x7 one-seat coverage   | 4.5–5.5 FTE                         |
| Manual testing           | 40–80 test cases/tester/day         |
| Automation scripting     | 3–8 scripts/engineer/day            |
| BPO productivity         | 50–150 transactions/FTE/day         |
| Blended rate             | Σ(Role mix % × Role rate)           |
| Fixed price              | Fully loaded cost ÷ (1 − margin %)  |
| Margin                   | (Price − Cost) ÷ Price              |
| Markup                   | (Price − Cost) ÷ Cost               |
| Payback                  | Investment ÷ net monthly benefit    |
| ROI                      | (Benefit − Investment) ÷ Investment |
| SLA exposure             | Monthly fee × SLA credit cap %      |
| Bid expected value       | Win probability × margin − bid cost |

---

# 41. Final Guidance

This cheat sheet is best used for:

* Early RFI sizing
* RFP effort validation
* Proposal review
* Resource loading sanity checks
* Commercial model review
* Pricing discussions
* ROI challenge sessions
* Delivery feasibility checks
* Bid/no-bid decision support

This sheet should not be used blindly. For final proposals, replace the indicative assumptions with:

```text
Client-provided volumes
Internal rate card
Delivery location mix
Role pyramid
Actual support hours
Confirmed SLA model
Known integration complexity
Tooling and license cost
Cloud cost
Legal and commercial terms
Target margin
Price-to-win strategy
```

The most important principle:

```text
Do not confuse effort saved with value realized.
Do not confuse average FTE with peak FTE.
Do not confuse margin with markup.
Do not confuse assumptions with facts.
```

A strong RFP estimate clearly shows:

```text
Scope
Assumptions
Volumetrics
Effort
Resource loading
Pricing basis
Risks
Exclusions
ROI logic
Commercial protection
```
