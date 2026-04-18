---
type: synthesized
aliases: ["Hedge Fund Returns", "Distributional Properties of Hedge Funds"]
tags: ["hedge-funds", "return-distributions", "risk-management", "portfolio-theory", "statistics"]
relationships:
  - target: hedge-fund
    type: extends
  - target: hedge-funds
    type: extends
  - target: mean-variance-framework
    type: extends
  - target: mean-variance-analysis
    type: extends
  - target: capital-structure-arbitrage
    type: extends
---

# Hedge Fund Return Distributions

# Hedge Fund Return Distributions

## Overview

Hedge fund returns exhibit distributional properties that are fundamentally different from the normal (Gaussian) distributions assumed by classical mean-variance analysis. Understanding these properties is essential for evaluating hedge fund performance and risk, and explains why standard portfolio theory tools are insufficient for this asset class.

## Key Distributional Characteristics

### Non-Normality

Hedge fund returns are generally **non-normal**, displaying significant skewness and excess kurtosis. This means the probability of extreme outcomes — both gains and losses — is higher than a normal distribution would predict.

### Skewness

- **Negative skewness** is common among strategies that collect premiums by selling optionality or providing liquidity (e.g., merger arbitrage, convertible arbitrage, short volatility strategies). These strategies generate frequent small gains but are exposed to rare, large losses — a payoff profile sometimes described as "picking up nickels in front of a steamroller."
- **Positive skewness** may appear in strategies with asymmetric upside, such as certain global macro or trend-following approaches.

### Excess Kurtosis (Fat Tails)

Most hedge fund strategies exhibit **leptokurtosis** — fatter tails than the normal distribution. This means:
- Extreme loss events occur more frequently than mean-variance models predict.
- Value-at-Risk (VaR) and other normal-distribution-based risk measures systematically underestimate tail risk.

### Serial Correlation

Many hedge fund return series display **positive serial correlation** (autocorrelation), particularly strategies involving illiquid or hard-to-price assets (e.g., distressed debt, private credit). This arises from:
- **Stale pricing**: Positions marked to model or to infrequent market prices smooth reported returns.
- **Smoothed NAVs**: Managers may have discretion in how they mark illiquid positions.

Serial correlation artificially **understates measured volatility**, making Sharpe ratios appear higher than the true risk-adjusted performance warrants.

## Strategy-Specific Distributional Profiles

| Strategy | Skewness | Kurtosis | Serial Correlation | Notes |
|---|---|---|---|---|
| Merger Arbitrage | Negative | High | Low | Crash risk from deal failures |
| Convertible Arbitrage | Negative | High | Moderate | Liquidity crises cause blowups |
| Capital Structure Arbitrage | Negative | High | Low | Uses options theory; tail risk from credit events |
| Long/Short Equity | Near-zero | Moderate | Low | More symmetric |
| Global Macro | Positive/Mixed | Variable | Low | Asymmetric upside possible |
| Managed Futures (CTA) | Positive | Moderate | Low | Trend-following provides crisis alpha |
| Distressed Debt | Negative | High | High | Illiquidity drives autocorrelation |
| Fixed Income Arbitrage | Negative | Very High | Moderate | LTCM-style blowup risk |

## Why Mean-Variance Analysis Fails

Classical mean-variance analysis, which underpins the Capital Asset Pricing Model (CAPM) and standard portfolio construction, assumes:
1. Returns are normally distributed, OR
2. Investors have quadratic utility functions.

Neither assumption holds well for hedge funds:

- **Non-normality** means that variance alone does not capture the full risk profile; skewness and kurtosis matter independently to investors.
- **Negative skewness + excess kurtosis** is particularly dangerous: strategies that look attractive on a mean-variance basis (high Sharpe ratio) may carry hidden crash risk.
- **Serial correlation** distorts standard deviation estimates downward, inflating apparent Sharpe ratios.
- Investors generally exhibit **loss aversion** and care about downside risk asymmetrically, which quadratic utility does not capture.

## Better Risk Measures for Hedge Funds

Given these distributional issues, practitioners supplement or replace mean-variance metrics with:

- **Sortino Ratio**: Penalizes only downside deviation.
- **Maximum Drawdown**: Measures worst peak-to-trough loss.
- **Conditional Value-at-Risk (CVaR / Expected Shortfall)**: Captures expected loss in the tail beyond VaR.
- **Omega Ratio**: Uses the full return distribution.
- **Higher-moment adjusted Sharpe ratios**: Incorporate skewness and kurtosis corrections.
- **Autocorrelation-adjusted volatility**: Corrects standard deviation for serial correlation before computing Sharpe ratios.

## Implications for Portfolio Allocation

- Hedge funds with negative skewness may **appear** to be diversifiers in normal markets but **co-crash** with equity portfolios in crises, reducing their diversification value precisely when it is most needed.
- Strategies like managed futures (CTAs) have historically provided **positive skewness in crises**, making them genuine diversifiers.
- Allocators using mean-variance optimization will systematically **over-allocate** to negatively skewed strategies due to understated risk.

## Connection to Broader Themes

The failure of mean-variance analysis for hedge funds parallels its limitations in other contexts: the paper by Chowdhry and Schwartz (Paper CFR) demonstrates that minimizing variance is not the same as minimizing the probability of financial distress — an analogous insight at the firm level. Similarly, at the portfolio level, minimizing return variance is not the same as managing the risk of catastrophic loss, which is the dominant concern for strategies with fat-tailed, negatively skewed distributions.

## Summary

Hedge fund return distributions are characterized by non-normality, negative skewness (for many arbitrage strategies), excess kurtosis (fat tails), and serial correlation (for illiquid strategies). These properties collectively render mean-variance analysis inadequate for hedge fund evaluation. Proper assessment requires higher-moment statistics, downside risk measures, and autocorrelation adjustments to avoid systematically mispricing the true risk profile of hedge fund investments.