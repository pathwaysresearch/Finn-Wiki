---
type: concept
aliases: ["Expected Cash Flow and Risk Separation Principle"]
tags: ["DCF", "risk-adjusted discount rates", "expected cash flows", "valuation principle"]
relationships:
  - target: discounted-cash-flow-valuation
    type: relates_to
  - target: risk-adjusted-discount-rates
    type: relates_to
  - target: certainty-equivalent-models
    type: relates_to
---

# Separation of Expected Cash Flows and Risk Adjustment in DCF

In discounted cash flow (DCF) valuation, a core principle is to keep the expected cash flow forecast as an unbiased, probability‑weighted estimate of future outcomes, while all risk adjustments are placed in the discount rate. Baking risk adjustments directly into the cash flow forecasts (e.g., by using conservative or \"haircut\" estimates) breaks this separation and can lead to double‑counting of risk or to forecasts that no longer represent true expectations. The discount rate, derived from asset‑pricing models such as the CAPM, already incorporates the market’s price for bearing risk; therefore the cash flows should reflect the mean of the probability distribution conditional on available information. This approach preserves the linearity of expectation and ensures that the risk premium is captured consistently via the opportunity cost of capital.\n\nSources: MIT15_401F08_ses08_300k.srt.md, MIT15_401F08_ses17_300k.srt.md