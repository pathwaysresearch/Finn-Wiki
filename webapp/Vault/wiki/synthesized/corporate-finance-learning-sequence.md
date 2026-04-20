---
type: synthesized
aliases: ["Corporate Finance Roadmap", "How to Learn Corporate Finance"]
tags: ["corporate-finance", "learning-path", "beginner"]
relationships:
  - target: corporate-finance
    type: extends
  - target: valuation
    type: extends
  - target: discounting
    type: extends
  - target: net-present-value
    type: extends
  - target: capital-budgeting
    type: extends
  - target: capital-asset-pricing-model
    type: extends
  - target: market-portfolio
    type: extends
---

# Corporate Finance Learning Sequence

# Corporate Finance Learning Sequence

Corporate finance builds on a small set of core ideas, each of which depends on the one before it. A learner new to the field should follow this logical progression rather than jumping between topics.

## Recommended Learning Order

### 1. Time & Risk — The Two Foundational Ideas
Everything in corporate finance rests on two primitive concepts:
- **Time**: A dollar today is worth more than a dollar in the future.
- **Risk**: Uncertain future cash flows must be compensated with a higher expected return.

Without internalising these two ideas, none of the subsequent techniques make sense.

### 2. Discounting — Translating Future Value to Present Value
Once you accept the time value of money, [[discounting|Discounting]] is the mathematical tool that converts future cash flows into today's equivalent. Master the mechanics of discount factors, interest rates, and compounding before moving on.

### 3. Valuation — Pricing Financial Assets
[[valuation|Valuation]] applies discounting to price stocks, bonds, and real assets. You will learn how to build cash flow forecasts and choose an appropriate discount rate. This is the practical skill that underlies nearly all of corporate finance.

### 4. Net Present Value (NPV) — The Decision Rule
[[net-present-value|Net Present Value (NPV)]] is the single most important decision rule in finance. It aggregates discounted cash flows into one number: if NPV > 0, the project creates value; if NPV < 0, it destroys value. NPV is presented in the MIT 15.401 lecture series as the correct economic method for evaluating any investment.

### 5. Capital Budgeting — Applying NPV to Real Decisions
[[capital-budgeting|Capital Budgeting]] is where theory meets practice. A financial officer uses NPV (and sometimes competes against flawed alternatives like the payback period method) to decide which projects a firm should undertake. At this stage you also encounter strategic considerations such as [[synergies|Synergies]] that go beyond standalone NPV.

### 6. Portfolio Theory & CAPM — Where Does the Discount Rate Come From?
The discount rate used in NPV is not arbitrary — it reflects the riskiness of the cash flows. [[capital-asset-pricing-model|Capital Asset Pricing Model (CAPM)]] provides a principled answer: the required return on any asset equals the risk-free rate plus a premium proportional to the asset's systematic (market) risk. The [[market-portfolio|Market Portfolio]] is central to this framework. CAPM builds on Modern Portfolio Theory, which shows how diversification eliminates idiosyncratic risk, leaving only systematic risk to be priced.

## How the Concepts Fit Together


Time + Risk
    └─► Discounting
            └─► Valuation
                    └─► Net Present Value (NPV)
                                └─► Capital Budgeting
                                            └─► CAPM (determines the discount rate)


## Practical Tips
- Start with the MIT 15.401 lecture series (Sessions 1–3 for foundations, Sessions 15–18 for portfolio theory and capital budgeting).
- Always anchor new concepts back to the NPV rule — it is the unifying framework.
- When studying CAPM, treat it as answering the question: *"What discount rate should I use in my NPV calculation?"*
- Be aware of NPV alternatives (payback period, IRR) — understanding *why* they are inferior deepens your grasp of NPV itself.