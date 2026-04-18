---
type: synthesized
aliases: ["unlevering volatility for real options", "asset volatility in real options"]
tags: ["real-options", "volatility", "leverage", "valuation", "derivatives"]
relationships:
  - target: real-options-framework
    type: extends
  - target: capital-asset-pricing-model
    type: related
  - target: adjusted-present-value
    type: related
  - target: beta-sensitivity
    type: related
---

# Real Options Volatility Unlevering

## Core Insight

When applying real options valuation, the volatility input must be **asset volatility** (σ_A), not the observed **equity volatility** (σ_E). Observed stock return volatility reflects leverage — it is the volatility of the equity claim, which is itself a call option on the firm's assets. Plugging σ_E directly into an option pricing model double-counts leverage and systematically overstates option value.

## Why the Bias Arises

Equity is a levered residual claim. Even holding asset volatility constant, higher debt amplifies equity volatility. Formally, under Modigliani-Miller:

$$\sigma_E = \sigma_A \cdot \frac{V_A}{V_E}$$

where V_A is total asset value and V_E is equity value. Because V_A / V_E > 1 for any levered firm, σ_E > σ_A. The gap grows monotonically with the debt-to-value ratio (D/V).

When a real option's underlying asset is the **firm's project or asset value** — not the equity itself — the correct volatility is σ_A. Using σ_E inflates the option value because higher volatility always increases option value (positive vega), and the inflation scales with leverage.

## The Unlevering Procedure

1. **Observe** equity volatility σ_E from stock return data (historical or implied).
2. **Estimate** the market-value debt-to-equity ratio D/E and compute V_A = V_E + V_D.
3. **Unlever** via:
   $$\sigma_A = \sigma_E \cdot \frac{V_E}{V_A} = \sigma_E \cdot (1 - D/V)$$
   This mirrors the logic of unlevering beta in CAPM: β_A = β_E · (E/V) + β_D · (D/V), with β_D ≈ 0 for investment-grade debt.
4. **Use σ_A** as the volatility input in Black-Scholes or the binomial model for the real option.

## Magnitude of the Bias

| D/V | σ_E (observed) | σ_A (unlevered) | Overstatement if σ_E used |
|-----|----------------|-----------------|---------------------------|
| 0%  | 30%            | 30%             | None                      |
| 30% | 30%            | 21%             | ~43% excess volatility    |
| 50% | 30%            | 15%             | 100% excess volatility    |
| 70% | 30%            | 9%              | 233% excess volatility    |

Because option value is convex in volatility (vega > 0), option value overstatement is nonlinear — highly levered firms or projects with high D/V ratios face the most severe valuation distortion.

## Practical Complications

- **Debt is not risk-free at high leverage**: at very high D/V, debt itself carries significant volatility; the simple formula above underestimates σ_A slightly. A Merton-model iterative solution may be needed.
- **Comparable company approach**: when estimating σ_A for a private project, use the asset volatilities of comparable public firms (unlever their equity volatilities first), not their raw stock return volatilities.
- **Options on equity vs. options on assets**: employee stock options, warrants, and convertible debt are options on equity — σ_E is correct for those. Real options on projects, licenses, or entry/exit decisions are options on assets — σ_A is correct.

## Connection to Beta Unlevering

The volatility unlevering procedure is the direct analogue of **beta unlevering** in CAPM. Just as one unleveres observed equity beta to asset beta before using it in project discount rates, one must unlever equity volatility to asset volatility before using it in real options pricing. The underlying principle is identical: strip out the mechanical amplification of financial leverage before making economic inferences about the underlying asset.

## Key Takeaway

Failing to unlever volatility is one of the most common errors in real options practice. The overstatement of option value is not a second-order rounding issue — at debt ratios typical of capital-intensive industries (40–60% D/V), the bias routinely doubles or triples the estimated volatility input, producing option valuations that are economically meaningless.