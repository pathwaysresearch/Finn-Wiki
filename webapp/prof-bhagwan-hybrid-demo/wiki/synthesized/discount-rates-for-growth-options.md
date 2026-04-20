---
type: synthesized
aliases: ["Growth Option Discount Rates", "Risk and Growth Options"]
tags: ["valuation", "risk", "options", "capm", "corporate-finance"]
relationships:
  - target: risk-adjusted-discount-rates
    type: extends
  - target: idiosyncratic-risk
    type: uses
  - target: exploration-risk
    type: uses
  - target: options-theory
    type: uses
  - target: multiplicative-uncertainty-effect
    type: uses
  - target: convexity
    type: uses
---

# Discount Rates for Growth Options

# Discount Rates for Growth Options

## Core Claim

Growth options may warrant higher discount rates than assets-in-place, but **not** simply because they are generically 'riskier.' The correct reasoning requires decomposing the option's risk into its systematic and idiosyncratic components — and applying fundamentally different discount rates to each.

## Why Option-Like Convexity Raises Effective Beta

A growth option's payoff is convex in the underlying firm or market value. By the logic of options theory, convexity amplifies exposure to systematic movements: when the market rises, the option's delta increases, meaning each marginal dollar of market movement has a larger-than-linear effect on option value. This mechanical amplification raises the option's effective beta relative to the underlying asset, justifying a higher risk-adjusted discount rate for the systematic component.

This is consistent with the principle that higher volatility widens the right tail of an option's payoff without increasing the bounded downside, making the expected payoff more sensitive to systematic risk realizations.

## Why Idiosyncratic Risk Should NOT Raise the Discount Rate

The second, equally important insight is that much of the uncertainty embedded in a growth option is **idiosyncratic** — technical feasibility, regulatory approval, exploration success, R&D outcomes. This risk is:

- Firm-specific and uncorrelated across the market
- Diversifiable in a large portfolio (by the law of large numbers)
- Not priced by CAPM or any risk-and-return model that only prices systematic risk

For a textbook example: the probability of striking oil is an idiosyncratic risk with a beta near zero. It should be discounted at (or near) the **risk-free rate**, not at a risk-premium-inflated rate. Applying a high discount rate to idiosyncratic uncertainty overpenalizes these cash flows and systematically undervalues growth options.

## Required Decomposition

Correct valuation therefore requires splitting the growth option's cash flows or risk factors:

1. **Systematic component** — market-correlated uncertainty, amplified by option convexity → discount at a rate reflecting elevated beta (risk-free rate + market risk premium × elevated beta)
2. **Idiosyncratic component** — firm-specific uncertainty → discount at or near the risk-free rate

This decomposition mirrors the approach used in certainty-equivalent models, which are mathematically equivalent to risk-adjusted discount rate models when risk premiums are derived from proper risk-and-return models.

## Practical Implications

- Blanket application of a high discount rate to all growth option cash flows (because 'growth is risky') conflates systematic and idiosyncratic risk and is theoretically incorrect.
- The multiplicative interaction of market and idiosyncratic uncertainty over long horizons (see multiplicative uncertainty effect) further complicates simple beta-based discounting, reinforcing the need for explicit decomposition.
- This framing also has implications for hedging: firms should not over-hedge idiosyncratic components of growth option value, as that risk is not priced by the market.

## Connection to Broader Valuation Framework

Risk-adjusted discount rates and certainty-equivalent models yield the same present value only when risk premiums are correctly specified. For growth options, the error typically arises not in the choice of framework but in the incorrect identification of which risks are systematic — leading to inflated discount rates applied to idiosyncratic uncertainty that the market does not price.