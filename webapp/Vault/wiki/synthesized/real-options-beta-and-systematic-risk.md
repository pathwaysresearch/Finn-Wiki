---
type: synthesized
aliases: ["real options beta", "growth option beta", "PVGO beta decomposition"]
tags: ["real-options", "beta", "systematic-risk", "valuation", "growth-options", "capm", "corporate-finance"]
relationships:
  - target: real-options-framework
    type: extends
  - target: real-options-volatility-unlevering
    type: related
  - target: bernardo-and-chowdhry-2002
    type: related
  - target: exploration-risk
    type: related
  - target: systematic-risk-versus-systemic-risk
    type: related
  - target: portfolio-theory
    type: related
---

# Real Options Have Higher Betas Than Assets-in-Place

# Real Options Have Higher Betas Than Assets-in-Place

## Core Insight

Real options — the embedded rights to expand, enter, or pivot — carry **higher betas** than assets-in-place. This is not an empirical curiosity; it follows directly from the structure of contingent claims. A real option is a levered, nonlinear bet on the underlying asset value, so its systematic risk is mechanically amplified relative to the asset it is written on.

This has two major practical consequences:
1. **Growth firms have higher betas** than mature firms, even holding underlying asset risk constant, because a larger fraction of their value is option-like.
2. **Different components of the same project must be discounted at different rates** — the option component demands a higher discount rate than the cash-generating component.

## Why Options Amplify Systematic Risk

An option is a contingent claim: it pays off only when the underlying asset value exceeds the exercise price. This contingency creates implicit leverage. Even if the underlying asset has moderate systematic risk (moderate β_A), the option has high sensitivity to market movements because:

- When markets rise, the option moves deeper in-the-money; the option's delta increases, amplifying upside.
- When markets fall, the option goes out-of-the-money; the option loses value faster than the underlying asset.

Formally, the beta of a call option on an asset is:

$$\beta_{option} = \beta_A \cdot \frac{\partial V_{option}}{\partial V_A} \cdot \frac{V_A}{V_{option}} = \beta_A \cdot \Delta \cdot \frac{V_A}{V_{option}}$$

where Δ (delta) is the option's sensitivity to the underlying and the ratio V_A / V_{option} > 1 is the implicit leverage. Because the option is worth less than the underlying asset, the leverage ratio exceeds one, so β_option > β_A always.

## PVGO Decomposition and Beta Inflation in Growth Firms

Stock price can be decomposed as:

$$P = \underbrace{\frac{EPS}{r}}_{\text{assets-in-place}} + \underbrace{PVGO}_{\text{growth options}}$$

where PVGO (Present Value of Growth Opportunities) is the option-like component. Because the PVGO component has a higher beta than the assets-in-place component, the observed equity beta is a value-weighted average:

$$\beta_E = \frac{V_{AIP}}{V_E} \cdot \beta_{AIP} + \frac{PVGO}{V_E} \cdot \beta_{PVGO}$$

with β_PVGO > β_AIP. This directly explains the well-documented empirical pattern: **high-PVGO (growth) firms have higher betas** than low-PVGO (value) firms, even in the same industry. The beta premium of growth stocks is not a market anomaly — it is the mechanical consequence of option-like payoff structures.

Conversely, as a firm matures and growth options are exercised or expire, its PVGO shrinks, and its equity beta gradually converges toward the beta of assets-in-place. This is why value stocks have lower betas than growth stocks.

## Project-Level Implications: Exploration vs. Production

The same logic applies within a single project. Consider a natural resource investment with two components:

| Component | Nature | Risk type | Appropriate discount rate |
|-----------|--------|-----------|---------------------------|
| Exploration (right to drill) | Option on finding oil | Non-systematic (idiosyncratic) + option amplification | Risk-free rate for pure exploration risk; higher for systematic component |
| Production (cash flows if oil found) | Asset-in-place | Systematic commodity price risk | CAPM-implied rate with oil-sector beta |

This is the key insight from the MIT Finance lecture on oil project valuation: **exploration risk** is largely idiosyncratic (whether oil is present is independent of the market cycle), so it carries a beta near zero and should be discounted close to the risk-free rate. But the *option value* of the exploration right — which scales with oil prices, which are correlated with the market — does carry systematic risk. Conflating these two components by applying a single discount rate to the whole project produces a biased valuation.

## Magnitude of the Effect

The beta amplification scales with how far out-of-the-money the option is:

- **Deep in-the-money options** behave like the underlying asset; delta ≈ 1, leverage ratio ≈ 1, so β_option ≈ β_A.
- **At-the-money options** have significant leverage; β_option is typically 2–4× β_A.
- **Deep out-of-the-money options** have very low delta and very high implicit leverage; β_option can be 5–10× β_A or more.

For early-stage firms or projects in nascent industries, the growth option is far out-of-the-money relative to current asset value — amplifying the beta premium substantially.

## Connection to Volatility Unlevering

The beta amplification of options is the systematic-risk analogue of the volatility amplification discussed in real options volatility unlevering. Both arise from the same implicit leverage structure of a contingent claim:

- **Volatility dimension**: σ_option > σ_A (option volatility exceeds asset volatility)
- **Systematic risk dimension**: β_option > β_A (option beta exceeds asset beta)

Just as practitioners must unlever equity volatility to asset volatility before using it as the real options input, they must also recognize that the *discount rate* applied to the option component must reflect the option's own elevated beta — not simply the firm's or project's average beta.

## Practical Implications

1. **Do not apply a single WACC to a growth project**: the WACC reflects the average beta of assets-in-place. The option component of the project has a higher required return and will be undervalued if discounted at WACC.
2. **Decompose firm value before estimating cost of capital**: when using comparables to estimate a project's discount rate, select mature (low-PVGO) firms in the same industry, whose betas more closely reflect asset-in-place risk.
3. **Expect the beta of a startup or growth firm to decline over time**: as growth options are exercised and converted into assets-in-place, the equity beta should fall — this is normal and expected, not a sign of reduced business risk.
4. **Use option pricing, not DCF, for the option component**: the correct way to handle the variable discount rate of an option (which changes as delta changes over time) is to use an option pricing model directly, rather than trying to apply a fixed risk-adjusted discount rate.

## Key Takeaway

Real options have higher betas than assets-in-place because they are contingent, levered claims. This single insight unifies three apparently separate observations: growth firms have higher equity betas, PVGO-rich stocks earn higher expected returns, and different project components demand different discount rates. The underlying mechanism is identical in all three cases — the implicit leverage of a call-like payoff structure amplifies systematic risk monotonically.