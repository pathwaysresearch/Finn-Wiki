

[Page 1]
Critical Finance Review, 2016, 5: 399–415

# How Should Firms Hedge Market Risk?

Bhagwan Chowdhry  
Eduardo Schwartz

¹University of California, Los Angeles, Anderson School of Management, USA;  
bhagwan@anderson.ucla.edu

²University of California, Los Angeles, Anderson School of Management, USA;  
eschwart@anderson.ucla.edu

***

**ABSTRACT**

Consider a firm whose stock returns are affected by market returns and an idiosyncratic market-orthogonal factor. The *level* of the firm's cash flows depends on the *level* of the market and the *level* of the idiosyncratic factor multiplicatively because of compounding. Although a large hedge against the market index minimizes the variance of cash flows, such a hedge does not minimize the costs of financial distress associated with low cash flow realizations below a debt threshold. A hedge ratio based on asset-rate-of-return regression estimates is then incorrect. This holds even in continuous time and with dynamic hedging policies. Our paper provides a simple heuristic for corporations wishing to hedge out the adverse consequences of market risk.

***

**Keywords:** Finance

**JEL Codes:** G30

***

We thank Jeremy Stein, René Stulz (who also told us about Fischer Black's critique), and Ivo Welch for many insightful conversations. We also thank seminar participants at UCLA Anderson brown-bag seminar series and at the UCLA-Lugano Finance Conference. We thank anonymous referees for many useful comments, and are deeply grateful to one who helped provide the analytical proof for the main result in the paper.

ISSN 2164-5744; DOI 10.1561/104.00000023  
©2016 B. Chowdhry and E. Schwartz

[Page 2]
400
Bhagwan Chowdhry and Eduardo Schwartz

# 1 Introduction

There is an extensive literature that shows that firms can, under some circum-
stances, increase shareholder wealth by reducing the volatility of their cash flows.
In particular, firms that face significant costs of financial distress if they experience
abnormally low cash flows can decrease the present value of financial distress
through hedging. In a seminal paper, Froot et al. (1993) show that firms that
have to finance their investments out of their cash flows are forced to give up
positive net present value projects if they experience poor cash flows. Such firms
benefit from hedging because it enables them to take advantage of investment
opportunities they would have to forsake or give up otherwise. A number of other
reasons for why firms can benefit from decreasing total cash flow volatility have
been discussed in the literature.¹

Total cash flow volatility is a function both of firm idiosyncratic volatility and
of volatility induced by systematic risk. Consequently, it would seem that firms
could also create shareholder wealth by reducing their exposure to systematic risk.
However, we do not observe firms hedging their exposure to the market either
by shorting a market index or by using financial derivatives on the market index.
Nor do many academics² or practitioners recommend that firms do that. Fischer
Black pointed out this embarrassing fact many years ago.

We show that the simple intuition which would suggest that a firm with positive
exposure to market movements (i.e., a positive beta) hedge by taking an offsetting
position in the overall market requires careful consideration when more than one
source of uncertainty affects the variability of the firm's cash flow. This is because
the effects of different sources of uncertainty on a firm's level of cash flows at a
distant date in the future are multiplicative even when these effects appear to be
separable in stock returns over short horizons.

The intuition for the main insight in the paper can be illustrated by the following
simple example. Suppose a firm's cash flow in 5 years is $100 on average. Suppose
that the realized cash flow is determined by a factor that is idiosyncratic to the firm
and also by overall market conditions. Assume that the idiosyncratic factor alone
can make the realized cash flow go up or down by 60% with equal probability, and
that the market factor alone can make the realized cash flow go up or down by
50% with equal probability. When both factors are present and are uncorrelated,
the realized cash flows can take four different values:

---
¹For instance, Smith and Stulz (1985) show that lower cash flow volatility can reduce the present
value of taxes; Stulz (1984) makes the case that high cash flow volatility can make the firm's insiders
more risk-averse; using different mechanisms, Breeden and Viswanathan (1998), and DeMarzo and
Duffe (1995) show that lower cash flow volatility can help outsiders in assessing the performance of
firms.

²See Bolton et al. (2011) for an exception.

[Page 3]
How Should Firms Hedge Market Risk?
401

| Idiosyncratic factor | Market up by 50% | Market down by 50% |
| :--- | :--- | :--- |
| up by 60% | $100 × 1.60 × 1.50 = $240 | $100 × 1.60 × 0.50 = $80 |
| down by 60% | $100 × 0.40 × 1.50 = $60 | $100 × 0.40 × 0.50 = $20 |

Suppose now that the firm shorts $100 of the market to hedge market risk, so that when the market goes up, it loses $50; but when the market goes down, it gains $50. The hedged cash flows are shown as follows.

| Idiosyncratic factor | Market up by 50% | Market down by 50% |
| :--- | :--- | :--- |
| up by 60% | $240 - $50 = $190 | $80 + $50 = $130 |
| down by 60% | $60 - $50 = $10 | $20 + $50 = $70 |

Hedging has reduced the range of cash flows from $80–$240 to $130–$190 when the idiosyncratic factor is up. However, the worst cash flow realization has deteriorated from $20 to $10 when the idiosyncratic factor is down. If the firm had debt of $15, it would be bankrupt with the market hedge but not without. Our paper shows that the optimal market hedge is much more conservative than hedging $100 of market risk. In our example, with $15 worth of debt, the optimal hedge is $15.

The intuition is as follows. Suppose the firm takes a short position in the market assuming the average realization of cash flow. Then, if the realized cash flow turns out to be low, the short market hedge would have been excessive and in fact may lead to significant losses if the market goes up. This could be devastating. On the other hand, if the realized cash flow turns out to be high, the market hedge based on the average cash flow would have been inadequate, but this is not so critical. Thus, the asymmetric payoff should induce the firm to be more (though not completely) conservative in hedging its market risk.³

If the firm's objective were to minimize the total variance of the cash flow, then the appropriate market hedge would be large. This large hedge would reduce variance both when cash-flow realizations are large as well as when they are small. However, because bankruptcy deadweight costs are relevant only when the cash-flow realizations are low, the firm's objective should be to minimize the total variance of the cash flow only when its cash flows are likely to be low. It does not matter that this low a hedge increases the unconditional variance or the variance when cash flows tend to be high.

This intuition also suggests that Shiller's 2004 suggestion that individuals hedge more (market) risk requires the caveat that their optimal hedge ratio is

***

³That there is a tradeoff between financing and risk management is identified in Holmstrom and Tirole (2000) and Mello and Parsons (2000), and Rampini and Viswanathan (2010, 2013). Dynamic models of such tradeoffs are developed in Bolton et al. (2011) and Rampini et al. (2013).

[Page 4]
not the sensitivity of their welfare with respect to the market, but potentially considerably lower.

Interestingly, the optimal market-risk hedge has an easy heuristic. Managers should choose a hedge ratio equal to the firm's contractual obligations as a fraction of expected cash flows, multiplied by the firm's market beta. The hedge ratio does not depend on the firm's own volatility and the market volatility.

## 2 The Model

### 2.1 The Firm

Consider a firm and a market index whose short-run return dynamics are
$$
r_t = \alpha + \beta \cdot r_t^M + v_t,
$$
$$
r_t^M = \alpha^M + v_t^M,
$$
where $r_t$ is a stock return, $r_t^M$ is the contemporaneous return on the market index, $\beta$ is the exposure to systematic risk, and $v_t$ and $v_t^M$ are mean-zero idiosyncratic components. When $\beta$ is positive and the variance of $v_t$ is large, this is a canonical example in which exposure to $r_t^M$ is significant and therefore an offsetting market hedge would appear to be helpful. Textbooks often suggest rate-of-return regressions to estimate a coefficient $\beta$, which is then argued to be the optimal hedge ratio, because this hedge ratio minimizes the variance of returns. We will show that this is incorrect if the goal is to avoid financial distress.

To simplify, assume that $\beta = 1$. The return dynamics over a finite period of, say, one year, $R_t$ and $R_t^M$, have to be exponentiated,
$$
(1+R_t^M) = e^{(r_t^M)},
$$
$$
(1+R_t) = e^{(r_t)}.
$$
The economy is risk-neutral,[^4] so
$$
E(R_t) = E(R_t^M) = R^f,
$$
where $R^f$ is the rate for a risk-free investment. Then, it follows that
$$
e^{(r_t^M)} = (1 + R_t^M) = (1 + R^f) \cdot (1 + \epsilon_t^M)
$$
$$
e^{(r_t)} = (1 + R_t) = (1 + R^f) \cdot (1 + \epsilon_t^M) \cdot (1 + \epsilon_t),
$$
and $E(\epsilon_t) = E(\epsilon_t^M) = 0$. If $r_t, r_t^M, v_t$ and $v_t^M$ are normally distributed, then $R_t$, $R_t^M$, $\epsilon_t$ and $\epsilon_t^M$ are log-normally distributed.

[^4]: The firm's incentive to hedge in our model will arise from its desire to avoid financial distress, and not from risk-aversion.

[Page 5]
Now, consider a two-date model in which a firm generates one cash flow at date 1, $C_1$. Because we are assuming risk neutrality, the value of the firm at date 0 is
$$
S_0 = \frac{E_0(C_1)}{1 + R^f}
$$
Because the gross rate of return over one period $(1 + R_1) = C_1/S_0$,
$$
C_1 = S_0 \cdot (1 + R^f) \cdot (1 + \epsilon_1^M) \cdot (1 + \epsilon_1).
$$
Notice that the cash flow depends on the market risk $(1 + \epsilon_1^M)$ and the idiosyncratic risk $(1 + \epsilon_1)$ multiplicatively.

## 2.2 The Hedge
Now consider hedging the firm's cash flow by shorting forward contracts on a market index. Consider a market index with current value $Z_0$. Its value at date 1 is
$$
Z_1 = Z_0 \cdot (1 + R_1^M) = Z_0 \cdot (1 + R^f) \cdot (1 + \epsilon_1^M).
$$
The forward price at date 0 of the market index is
$$
F = Z_0 \cdot (1 + R^f).
$$
If the firm goes short one forward contract on the market index (or, equivalently, shorts the market index and invests the proceeds to earn the risk-free rate of return on the proceeds), then the cash flow on date 1 will be
$$
H_1 = F - Z_1 = -Z_0 \cdot (1 + R^f) \cdot \epsilon_1^M.
$$
The expected value of the market hedge is zero. $H_1$ is positive if the market falls and negative if the market rises.

Define $y_0 = (S_0/Z_0) \cdot h_0$ to be the number of market hedges (short the forward contracts) and $h_0$ the fraction of the market-risk hedged. Then the hedged cash flow for the firm is
$$
C_1 + y_0 \cdot H_1 = S_0 \cdot (1 + R^f) \cdot [(1 + \epsilon_1^M)(1 + \epsilon_1) - h_0 \epsilon_1^M]
$$
$$
= E_0(C_1) \cdot [1 + \epsilon_1 + \epsilon_1 \cdot \epsilon_1^M + (1 - h_0)\epsilon_1^M].
$$
If $B_1$ denotes the contractual obligations to firm's creditors or bondholders, then the firm will be bankrupt if its hedged cash flow at date 1 is
$$
C_1 + y_0 \cdot H_1 < B_1.
$$
The bankruptcy condition above can be rewritten as
$$
\epsilon_1 + \epsilon_1 \epsilon_1^M + (1 - h_0)\epsilon_1^M < -(1 - \phi), \quad \text{(BC)}
$$

[Page 6]
where
$$ \phi = \frac{B_1}{E_0(C_1)} (< 1) $$
is the contractual obligations of the firm as a fraction of its expected cash flow at date 1.

## 2.3 Hedged Firm Risk
The variance of the hedged cash flows is proportional to the variance of $\epsilon_1 + \epsilon_1 \cdot e_1^M + (1-h_0) \cdot e_1^M$. Lemma 1 states that a hedge that offsets 100% of the variability in cash flows minimizes the variance of the hedged cash flows.

**Lemma 1.** The hedge $h_0 = 1$ minimizes the variance of $\epsilon_1 + \epsilon_1 \cdot e_1^M + (1-h_0) \cdot e_1^M$.

**Proof.** $\epsilon_1$ and $e_1^M$ have means equal to zero and are independent of each other. Therefore
$$ \text{Var}(\epsilon_1 + \epsilon_1 \cdot e_1^M + (1-h_0) \cdot e_1^M) \\ = \text{Var}(\epsilon_1) + \text{Var}(\epsilon_1) \cdot \text{Var}(e_1^M) + (1-h_0)^2 \cdot \text{Var}(e_1^M). $$
Setting $h_0 = 1$ minimizes the right-hand side (RHS). $\Box$

However, the firm would want to minimize the variance of its cash flows only if minimizing the variance also minimizes the likelihood that its hedged cash flow will fall below a certain threshold. This is the case if the firm has no idiosyncratic risk, but not usually otherwise.

**Lemma 2.** A hedge $h_0$ where $\phi \le h_0 \le 1$ can eliminate financial distress if the firm has no idiosyncratic risk ($e_1 = 0$).

**Proof.** Zero idiosyncratic risk implies that $e_1 = 0$. Setting $\epsilon_1 = 0$ in the bankruptcy condition (BC), and then noting that
$$ \phi \le h_0 \le 1 \Rightarrow (1-h_0) \cdot e_1^M > (1-h_0) \cdot (-1) = -(1-h_0) \ge -(1-\phi) $$
proves that such a firm will avoid bankruptcy in all states of the world. $\Box$

The firm can minimize the likelihood of financial distress by taking an offsetting short position in the market. However, this result does not generalize when its own idiosyncratic risk is positive and significant. Instead, a more conservative market hedge, i.e., $h_0 < 1$, can increase the conditional variance when $e_1$ is positive and reduce it when $e_1$ is negative. This increases the overall variance but reduces the likelihood that the firm will face financial distress.

[Page 7]
**Assumption 1.** The firm minimizes a cost associated with financial distress that is proportional to the difference between its contractual obligation and its hedged cash flow in states in which it is bankrupt.[^5]

The firm minimizes
$$
\min_{y_0} K \cdot \int_{-\infty}^{B_1} (B_1 - x) \cdot f(x)dx,
$$
where
$$
x = C_1 + y_0 \cdot H_1.
$$
$f(x)$ is the density function of the hedged cash flow $x$, and $K$ is a scaling constant that parameterizes the cost of financial distress.[^6] Normalizing all cash flow numbers by $E_0(C_1)$, and setting $K = 1$, the firms' objective function can be rewritten as
$$
\Gamma = \min_{h_0} \int_{h_0}^{\infty} \int_{-1}^{\infty} \max[-(1-\phi) - \{\epsilon_1 + (\epsilon_1 + 1 - h_0) \cdot \epsilon_1^M\}, 0]
$$
$$
\times f(\epsilon_1^M) \cdot f(\epsilon_1) d\epsilon_1^M d\epsilon_1.
$$
Notice that when the hedged cash flow is higher than the threshold, the maximum in the integrand sets bankruptcy cost to zero.

**Theorem 1.** *If the firm has contractual obligations of $B_1$, expected cash flows of $E_0(C_1)$, sensitivity of cash flows to market returns of $\beta = 1$, and the distress cost is proportional to the shortfall in cash flows to the contractual obligations, then the firm minimizes the expected cost of bankruptcy for*
$$
h_0 = \phi = \frac{B_1}{E_0(C_1)}.
$$
*Proof.* See Appendix.
$\square$

[^5]: We do not posit that the firm minimizes the probability of bankruptcy for two reasons. First, minimizing the probability of bankruptcy introduces a discontinuity when the firm is just at the boundary of bankruptcy. Second, in some states of the world when the firm's unhedged cash flow $C_1 < B_1$, the firm may have a perverse incentive to have a speculative short position on the market index.

[^6]: Notice that because we allow the hedged cash flow to become negative, we are in effect assuming that the firm has unlimited liability and thus it will honor its obligations on the short market hedge. Thus the pricing of the forward contract that assumed no default is appropriate. Assuming limited liability complicates the analysis - the derivative short position must be priced to account for default and an additional perverse incentive to hold a speculative position. This additional complexity does not lead to any additional insights that have not already been analyzed in the related papers mentioned in the introduction. Therefore we stay with the simpler formulation of unlimited liability.

[Page 8]
This is a simple yet remarkable result. The optimal market hedge (when the firm's return sensitivity to market factor is one-to-one) is equal to the level of the firm's contractual obligations as a fraction of expected cash flow. The optimal hedge does not depend on idiosyncratic volatility, market volatility, and exact distribution of returns as long as the shocks have zero means. This means that corporate managers can estimate and implement this hedge relatively easily.

## 3 Numerical Simulations

We now plot firm's hedged cash flow for various parameter values. We assume log-normal distributions for the idiosyncratic shock $e_i$ and the systematic shock $e_m^s$ with means equal to zero. We vary the bankruptcy threshold $\phi$.

Figure 1 shows a case in which the firm's contractual obligations are 30%, 40%, or 50% of its expected cash flows. The curvature of the functions is based on $\sigma(e_i) = \sigma(e_m^s) = 40\%$, which are plausible estimates over a four-year horizon.

The top panel shows the probabilities of bankruptcy. These are plausibly low. For a small hedge, the probability is rapidly declining. At least a little market-risk hedging is clearly superior. For $\phi = 0.3$, it is fairly flat (very close to zero) from 25% to 50%. For $\phi = 0.5$, it is minimized at 60%.

The bottom panel shows the expected cost of bankruptcy as a function of the hedge ratio. Figure 1 confirms that the optimal hedge that minimizes the expected cost of bankruptcy $h_0$ is equal to $\phi$ for each of the three values of $\phi$. In general, minimizing the probability of bankruptcy leads to a higher hedge ratio than the hedge that minimizes the expected cost of bankruptcy. This is because minimizing the probability of bankruptcy, in some states of the world when the firm's unhedged cash flow $C_1 < B_1$, may provide a perverse incentive to have a speculative short position on the market index. This is seen more clearly for $\phi = 0.5$ where the hedge that minimizes the probability of bankruptcy is 60% instead of the optimal 50%.

Figure 2 shows the distribution of the hedged cash flow with a 100% hedge and the optimal hedge of 30%. Notice that the firm is bankrupt for values less than $-(1-\phi) = -0.70$. The optimal hedge creates more values in the upper tail and reduces values in the lower tail. The standard deviation, however, is higher with the optimal hedge (51%) than with a 100% hedge (43%). This confirms that the hedge that minimizes the bankruptcy costs or the probability of bankruptcy is less than the hedge that minimizes the variance.

The analytical results in our paper were derived assuming beta was equal to 1. When the beta is different from one, the optimal hedge that minimizes the expected cost of bankruptcy is approximately equal to the product of $\beta$ and $\phi$. This is seen in Figure 3 which plots firm's hedged cash flow for beta of 0.5, 1 and 1.5 when $\phi = 0.5$. The optimal hedge ratios are 25%, 50% and 70% respectively.

[Page 9]
[CHART: This is a figure with two panels, A and B.
Panel A is a line graph titled "Probability". The y-axis is "Probability of Bankruptcy" ranging from 0.00 to 0.18. The x-axis is "Hedge Ratio" ranging from 0% to 100%. There are three downward-curving lines, each representing a different value of φ. The top curve is labeled "φ=50%", the middle curve is "φ=40%", and the bottom curve is "φ=30%". A label in the top right of the plot area reads "σ(ε) = σ(ε^M) = 40%". Each curve has a minimum point. The minimum for the φ=30% curve is at a hedge ratio of approximately 45%. The minimum for the φ=40% curve is at a hedge ratio of approximately 55%. The minimum for the φ=50% curve is at a hedge ratio of approximately 65%.

Panel B is a line graph titled "ExpectedCost". The y-axis is "Cost of Bankruptcy (x10^4)" ranging from 0 to 200. The x-axis is "Hedge Ratio" ranging from 0% to 100%. There are three downward-curving lines. The top curve is labeled "φ = 50%", the middle curve is "φ = 40%", and the bottom curve is "φ = 30%". A label in the top right of the plot area reads "σ(ε) = σ(ε^M) = 40%". Each curve has a minimum point. The minimum for the φ=30% curve is at a hedge ratio of 30%. The minimum for the φ=40% curve is at a hedge ratio of 40%. The minimum for the φ=50% curve is at a hedge ratio of 50%.]

**Figure 1: Probability and Expected Cost of Bankruptcy as a function of the Hedge Ratio**
**Description:** The firm's contractual obligations are 30%, 40%, or 50% of its expected cash flows. The curvature of the functions is based on $\sigma(\epsilon_1) = \sigma(\epsilon^M) = 40\%$.

**Interpretation:** The optimal hedge that minimizes the expected cost of bankruptcy $h_0$ is equal to $\phi$ for each of the three values of $\phi$. Minimizing the probability of bankruptcy leads to a higher hedge ratio than the hedge that minimizes the expected cost of bankruptcy.

[Page 10]
[CHART: A histogram showing two overlapping probability distributions of hedged cash flow. The taller, narrower distribution is labeled "100% Hedge sd=43%". The shorter, wider distribution is labeled "30% Hedge (Optimal) sd=51%".]

**Figure 2: Distribution of Hedged Cash Flow**

**Description:** The figure shows the probability distribution with a 100% hedge and with optimal hedge for $\sigma(\epsilon_1) = \sigma(\epsilon^T) = 40\%$ and $\phi = 0.3$.

**Interpretation:** The optimal hedge creates more values in the upper tail and reduces values in the lower tail.

[CHART: A line graph showing the "Cost of Bankruptcy (x10⁴)" on the y-axis versus the "Hedge Ratio" on the x-axis. The x-axis ranges from 0% to 100%. The y-axis ranges from 0 to 400. There are three U-shaped curves. The top curve, labeled "β=0.5", has its minimum around a 25% hedge ratio. The middle curve, labeled "β=1.0", has its minimum around a 50% hedge ratio. The bottom curve, labeled "β=1.5", has its minimum around a 75% hedge ratio. A label inside the chart reads "σ(ε₁) = σ(εᵀ) = 40% Φ = 50%".]

**Figure 3: Optimal Hedge Ratios for different Betas**

**Interpretation:** The optimal hedge that minimizes the expected cost of bankruptcy is approximately equal to the product of $\beta$ and $\phi$.

[Page 11]
To summarize our results from the numerical simulations, we find that (a) when beta is equal to one the optimal hedge that minimizes the cost of financial distress is equal to the fraction of contractual debt obligations to expected cash flows which is often smaller than 100%, a variance minimizing hedge, (b) a hedge that minimizes the probability of bankruptcy is typically higher than the hedge that minimizes the expected cost of bankruptcy, and (c) the optimal hedge when beta is different from one is approximately equal to $\phi \cdot \beta$.

## 4 Continuous-Time Hedging

Our theoretical analysis proved that because date 1 cash flow
$$
C_1 = S_0 \cdot (1 + R^f) \cdot (1 + \epsilon_1^M) \cdot (1 + \epsilon_1)
$$
is affected by the idiosyncratic shock $\epsilon_1$ and the market-related shock $\epsilon_1^M$ in a multiplicative fashion, a 100% market hedge is not optimal. One might wonder if this result arises because we have imposed a requirement that the hedge be put in place at the beginning of date 0 and have not allowed the hedge to change at more frequent intervals. We now show that allowing the hedge to change dynamically does not alter the conclusion that a 100% hedge is not optimal.

Suppose we were to subdivide the period from 0 to 1 into $N$ sub-periods. As $N$ approaches infinity, the approximation turns into continuous time. A 100% hedge at the beginning of sub-period $t$
$$
Y_{t-1} = \frac{S_{t-1}}{Z_{t-1}}
$$
results in a hedge profit at time $t$ of
$$
H_t = -S_{t-1} \cdot (1 + r') \cdot \epsilon_t^M,
$$
where $(1 + r') = (1 + R^f)^{1/N}$ and $\epsilon_t^M$ is the (much smaller) shock to the market for one sub-period. If $H_t$ is invested in the risk free asset until date 1, its future value will be
$$
H_t \cdot (1 + r')^{N-t}
$$
$$
= -S_{t-1} \cdot (1 + r')^{N-t+1} \cdot \epsilon_t^M
$$
$$
= -S_0 \cdot (1 + r')^{t-1} \cdot \left[ \prod_{i=1}^{t-1} (1 + \epsilon_i)(1 + \epsilon_i^M) \right] \cdot (1 + r')^{N-t+1} \cdot \epsilon_t^M
$$
$$
= -S_0 \cdot (1 + R^f) \cdot \left[ \prod_{i=1}^{t-1} (1 + \epsilon_i)(1 + \epsilon_i^M) \right] \cdot \epsilon_t^M,
$$

[Page 12]
410
Bhagwan Chowdhry and Eduardo Schwartz

where $e_t$ is the (much smaller) idiosyncratic shock for one sub-period. The total hedged cash flow at date 1 then is
$$
C_1 - S_0 \cdot (1+R') \cdot \sum_{t=1}^{N} \left[ \prod_{i=1}^{t-1} (1+\epsilon_i)(1+e_i^M) \right] \cdot \epsilon_t^M. \quad (1)
$$

Because
$$
C_1 = S_0 \cdot (1+R') \cdot \prod_{i=1}^{N} (1+\epsilon_i)(1+e_i^M),
$$
substituting in the hedged cash flow from equation (1), simplifying, and keeping only terms that have the product of at most two e terms, the hedged cash flow is equal to
$$
S_0 \cdot (1+R') \cdot \sum_{t=1}^{N} \left( \epsilon_t + \sum_{i=1}^{t} e_i^M \right)
$$
Therefore, even though each second-order product term is small in the above expression, the number of these terms is of the order of $N \cdot (N+1)/2$. Our simulations confirm that the standard deviation of the hedged cash flow is of a similar order of magnitude as the yearly standard deviation of return on the market.

We also considered a second scenario in which the cash flow is also generated continuously, but the firm needs to hedge its accumulated cash flow at some date in the future. Even in this case, we confirm that even though the market sensitivity of the firm's cash flow at any given instant could be perfectly hedged by the market hedge, the fact that the hedge for both near and distant cash flows must be determined in advance at date 0 precludes the possibility of completely eliminating the sensitivity to market movements.

# 5 Discussion

It has been a long standing puzzle in the risk-management literature that firms do not seem to hedge many important risks to their cash flows. The most obvious such risk is the exposure to market conditions. Our paper resolves a part of this puzzle. It shows that the naive suggestion of a full variance-minimizing hedge overstates the optimal hedge ratio. This is because exposure to market risks interacts multiplicatively with other idiosyncratic risks that firms face. If a firm were to take a short position in the market index and if the firm's realized cash flow were to be low because of its idiosyncratic factors, then it could face much larger net losses if the market turned out to be high. Instead, firms should be rather conservative in hedging their exposure to the market.

Our analysis clarifies that a hedge that minimizes the variance of the cash flow is not equivalent to a hedge that minimizes the costs associated with financial

[Page 13]
# How Should Firms Hedge Market Risk?

distress. Textbooks often recommend stock return regressions on various risk
factors to determine the exposure to risks and then equate this with an optimal
hedge ratio to avoid such risks. This approach has several problems:

1. Hedges that minimize cash-flow variance do not minimize the costs of
financial distress. Typically, the optimal hedge is smaller. This was the key
point of our paper.

2. Stock return dynamics may already anticipate that managers hedge the firms'
risk exposures (and thus a regression coefficient would tend to underestimate
the true exposure).

3. The sensitivity of firms' stock returns to overall market returns may arise
not because cash flows are particularly sensitive to market movements, but
because discount rates have a large common component. This would make
a simple regression of stock returns on market returns indicate significant
sensitivity, but an attempt to hedge cash flows by shorting the market would
turn out to be misguided.⁷

Our arguments also shed some light on discussions in the risk management
literature in which it is argued that firms should attempt to hedge their total
economic exposure⁸ rather than focusing only on transaction exposure. Our
analysis suggests that economic exposures are likely to be multiplicative and
identification of these exposures using regression methods, as is often advocated,
and then determining optimal hedges based on regression coefficients is likely to
lead to incorrect results.

Survey evidence presented in Bodnar et al. (2011) indicates that the most
common risks that are managed using financial instruments are interest rate risk,
foreign exchange risk, energy price risk, commodity price risk and credit risk. The
evidence also suggests that foreign exchange risk that is managed arises largely
from transaction exposures caused by contractual commitments. We suspect that
interest rate, energy price, commodity and credit risks also arise largely from
known transaction exposure whose cash flow value is known in advance and
therefore hedging them using financial instruments is straightforward. Although
market risk is considered to be the most important concern for firms surveyed,
markets risks are rarely hedged using financial instruments.

Finally, our analysis offers a more conservative perspective to the suggestions
that people hedge too little and should use the financial markets to hedge many
different types of risks, such as risks of housing price declines and unemployment
risks (see Shiller, 2004).⁹ The problem with these recommendations is that

---
⁷We thank René Stulz for discussing this insight with us.

⁸Total economic exposure includes transaction exposure, which is caused by contracts denominated
in foreign currencies, and competitive operating exposure induced by relative price changes caused by
exchange rate movements. See Shapiro (2009).

⁹We thank Jeremy Stein for discussing these ideas with us.

[Page 14]
they do not appreciate that risks that affect people's lives arise interactively and
multiplicatively. Simple financial instruments that hedge these risks may in fact
leave people more vulnerable, if they then have to fund a large cash outflow
precisely when their own idiosyncratic capacity to pay has diminished, too. Instead,
individuals should likely hedge only very modestly.¹⁰

# 6 Conclusion
Hedging market risk depends crucially on why the firm wants to hedge. If the
goal of the firm is to minimize the variance of its cash flows, perhaps because
the owner-manager is risk averse, then fully hedging market risk is appropriate.
However, if the goal is to minimize the costs associated with financial distress,
then more moderate hedging of market risk is prudent. A key determinant of how
much market risk should be hedged is the level of a firm's contractual obligations
that may trigger financial distress. For instance, a firm with only 25% debt in its
capital structure (a typical U.S. manufacturing firm) should hedge market risk
roughly half as much as a firm that has 50% debt in its capital structure (for
instance, an airline company).

Of course, the amount of market risk hedging also depends on the sensitivity
of a firm's cash flows to overall market conditions. For example firms in industries
such as automobiles, retail, telecommunications, tend to have higher cash flow
sensitivity to the market conditions, and therefore should hedge more than firms in
industries such as food, tobacco, oil and gas, which have lower cash flow sensitivity
to the market conditions.

Our paper has suggested a simple rule for hedging market risk when the goal
is to avoid financial distress. First, a firm should estimate the sensitivity of its cash
flows to market movements. Second, the firm should estimate its fixed obligations
as a proportion of expected cash flows. Then, its optimal market hedge as a
proportion of expected cash flows is the product of these two estimates.

Although our analysis has suggested that there are potentially large gains to
the first dollar hedged, the optimal hedge is likely to be far more conservative
than the more naïve full-variance hedge. We can help explain why firms do not
fully hedge their market exposure, although it remains a puzzle why most firms
do not hedge their market exposure, at all.

---
¹⁰If one could write contracts that are simultaneously contingent on several risk factors, significant
risk reductions may be possible. However, the feasibility of such complex instruments is doubtful. Not
only would this require an accurate quantification of risk exposures, which are likely to be different
for each individual, but also the instruments' contingencies would have to involve variables that can
be easily measured and cannot be manipulated. The possibility of misusing financial instruments to
speculate rather than hedge, for personal profit at the risk of putting the organization in peril, and
thus the costs of instituting internal controls and systems that can minimize or prevent such abuse,
make the case for hedging with financial instruments even more tenuous.

[Page 15] [DIGITIZATION FAILED]


[Page 16]
For 0 < $h_0 < \phi$, the integral is
$$
\int_{\epsilon_1 \le -(1-h_0)} \int_{e_1^M \ge -1} e_1^M f(\epsilon_1) f(e_1^M) de_1^M d\epsilon_1 \\
+ \int_{\epsilon_1 \ge -(1-h_0)} \int_{e_1^M \le \frac{\epsilon_1}{1-h_0}} e_1^M f(\epsilon_1) f(e_1^M) de_1^M d\epsilon_1.
$$
The first term is zero. The second term is negative because
$$
\frac{\partial e_1^M}{\partial \epsilon_1} = \frac{h_0 - \phi}{(\epsilon_1 + 1 - h_0)^2} < 0 \quad \text{for } h_0 < \phi.
$$
Hence the derivative decreases for $h_0 < \phi$, increases for $h_0 > \phi$, and is zero at $h_0 = \phi$.

## References
Bodnar, G. M., J. Graham, C. R. Harvey, and R. C. Marston. 2011. “Managing Risk Management”. Working paper.

Bolton, P., H. Chen, and N. Wang. 2011. “A Unified Theory of Tobin's Q, Corporate Investment, Financing and Risk Management”. *The Journal of Finance*. 66: 1545–1578.

Breeden, D. T. and S. Viswanathan. 1998. “Why Do Firms Hedge? An Asymmetric Information Model”. Working paper, Duke University.

DeMarzo, P. M. and D. Duffe. 1995. “Corporate Incentives for Hedging and Hedge Accounting”. *Review of Financial Studies*. 8: 743–771.

Froot, K. A., D. S. Scharfstein, and J. C. Stein. 1993. “Risk Management: Coordinating Corporate Investment and Financing Policies”. *The Journal of Finance*. 5: 1629–1658.

Holmstrom, B. and J. Tirole. 2000. “Liquidity and Risk Management”. *Journal of Money, Credit and Banking*. 32: 295–319.

Mello, A. S. and J. E. Parsons. 2000. “Hedging and Liquidity”. *Review of Financial Studies*. 13: 127–153.

Rampini, A. A., A. Sufi, and S. Viswanathan. 2013. “Dynamic Risk Management”. *Journal of Financial Economics*. Forthcoming.

Rampini, A. A. and S. Viswanathan. 2010. “Collateral, Risk Management, and the Distribution of Debt Capacity”. *The Journal of Finance*. 65: 2293–2322.

Rampini, A. A. and S. Viswanathan. 2013. “Collateral and Capital Structure”. *Journal of Financial Economics*. 109: 466–492.

Shapiro, A. 2009. *Multinational Financial Management*, Ninth Edition, Chapter 11. New York, NY: John Wiley & Sons Inc.

[Page 17]
Shiller, R. J. 2004. *The New Financial Order: Risk in the 21st Century*. Princeton, NJ: Princeton University Press.

Smith, C. W. and R. M. Stulz. 1985. “The Determinants of Firms' Hedging Policies". *Journal of Financial and Quantitative Analysis*. 20: 391–405.

Stulz, R. M. 1984. “Optimal Hedging Policies”. *Journal of Financial and Quantitative Analysis*. 19: 127–140.