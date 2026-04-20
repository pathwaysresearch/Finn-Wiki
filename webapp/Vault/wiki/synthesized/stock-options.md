---
type: concept
aliases: []
tags: ["options", "equity", "compensation"]
relationships:
  - target: options
    type: is_a_type_of
  - target: warrants
    type: contrasted_with
---

# Stock Options

Stock options are contracts that give the holder the right, but not the obligation, to buy (call) or sell (put) a specified number of shares of a corporation's stock at a predetermined price (the strike price) before a set expiration date.

They are zero‑net‑supply instruments on exchanges: every long position is matched by a short position, making them pure side bets between two parties with no net creation or destruction of shares. This contrasts with warrants, which are issued by the company itself; when a warrant is exercised the company issues new shares, increasing the total shares outstanding.

Because the payoff of a call option is kinked at the strike price — zero below the strike and linear one‑for‑one above — it has an asymmetric, non‑linear shape. This same asymmetry appears when we view a firm’s equity as a call option on its assets: equity holders receive the residual value of the firm after debt is paid, which is exactly the payoff of a call option with strike equal to the face value of debt. Consequently, stock options inherit this asymmetric payoff property, and the valuation of options (via Black‑Scholes or binomial methods) provides the same intuition used to value equity in a levered firm.

Thus, understanding stock options helps bridge derivative pricing and corporate finance: the option‑theoretic view of equity underlies models of capital structure, credit risk, and strategies such as capital‑structure arbitrage.