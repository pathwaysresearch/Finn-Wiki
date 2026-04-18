

[Page 1]
# Detecting Lies When Truth is Unobservable

Working Paper

Bhagwan Chowdhry <sup>a,b</sup> Konark Saxena <sup>c</sup>

<sup>a</sup> Indian School of Business (ISB), India

<sup>b</sup> University of California, Los Angeles, United States of America

bhagwan@isb.edu

<sup>c</sup> ESCP Business School, Paris, France

ksaxena@escp.eu

March 18, 2026

[Page 2]
**Abstract.** When agents hide bad outcomes, they leave a statistical fingerprint:
downside variation shrinks faster than total variation. We formalise this through two
compression statistics—$C_{\sigma}$, which measures volatility compression (the standard
deviation of reported outcomes), and $C_p$, the ratio of downside semivariance to total
variance—each falling by an amount determined exactly by manipulation intensity.
Fat-tailed data demand much larger samples for equivalent power; kurtosis inflates
the null variance linearly. A four-level identification hierarchy separates genuine
manipulation from legitimate smoothing—and no smoothing strategy simultaneously
fools both $C_{\sigma}$ and $C_p$. A direct corollary: return smoothing inflates the Sortino
ratio strictly more than the Sharpe ratio. The test requires no external benchmark—
practical for screening hedge funds, corporate earnings, and national accounts.

**Keywords:** misreporting detection, earnings management, GDP manipulation,
lower partial moments, compression statistics, downside variance share, Sortino
ratio, identification.

**JEL:** C12, C58, G12, M41, O11.

[Page 3]
# 1 Introduction
Reported numbers—GDP growth rates, corporate earnings, fund returns, inflation figures—
are not merely statistics. They are the basic currency of economic and political trust. And
wherever an agent controls a reported number and faces consequences for what it says,
the temptation to make bad outcomes look less bad is both predictable and, under weak
institutions, often irresistible. A government approaching an election, a fund manager
reporting to investors, a sovereign borrower at the creditors' table: each faces a moment
when the short-run benefits of appearing to have performed better outweigh the long-run
cost of eroded credibility.

Strong institutions guard against this temptation—through legal penalties, reputational sanc-
tion, independent verification. But institutional guardrails are far from universal. Autocratic
regimes face no electoral check on statistical fabrication. Democratic governments smooth
numbers in the run-up to votes. Listed-firm managers face quarterly pressure that rewards
smooth, predictable earnings. Wherever the agent has both motive and institutional latitude,
the result is a systematic, predictable, and—crucially— potentially detectable distortion in
the distribution of reported outcomes.

Detectable, that is, if you know where to look. The dominant empirical strategy compares
reported series to an external benchmark assumed to be clean. In corporate earnings,
Burgstahler and Dichev (1997) and Bollen and Pool (2009) document discontinuities just
above zero and around analyst forecast thresholds, exploiting the assumption that the true
distribution should be smooth through those points. Leuz et al. (2003) compare the variability
of reported income to operating cash flows across legal regimes. In macroeconomics, satellite
nighttime lights serve as the external proxy: Henderson et al. (2012) document systematic
divergence from official GDP in weak-institution countries, while Martinez (2022) finds
that autocratic governments inflate growth by roughly 35 per cent relative to light-based
benchmarks. The bunching literature (Kleven and Waseem, 2013; McCrary, 2008) offers
a general toolkit for detecting manipulation at known thresholds by comparing observed
density to a counterfactual estimated away from the threshold.

The benchmark problem is most acute in asset management. Hedge funds, private equity, and
other alternative vehicles report returns that investors cannot independently verify, operate
where external benchmarks are unavailable or easily disputed, and face strong incentives to
smooth reported performance. Getmansky et al. (2004) show that illiquid hedge fund returns
exhibit serial correlation inconsistent with market efficiency—consistent with deliberate
smoothing of valuations. Bollen and Pool (2009) document a discontinuity in the cross-

[Page 4]
sectional return distribution just above zero, directly analogous to earnings manipulation.
Abdulali (2006) provides practitioner evidence on return smoothing through selective asset
marking. In private equity, Brown et al. (2019) document NAV smoothing around fundraising
periods; Jenkinson et al. (2013) document interim valuation bias. The common thread:
whenever the agent controls the valuation of illiquid or hard-to-verify assets, a clean external
benchmark is typically unavailable.

This paper asks a sharper question: what can be inferred about misreporting from the reported
series alone? The answer rests on a simple observation. Even when the true mean is unknown,
misreporting leaves a detectable footprint in the second moments of the reported distribution.
We model an agent who attenuates unfavourable outcomes while leaving favourable ones
unchanged—below a privately known threshold $\tau$, shortfalls are shrunk toward the threshold
by an intensity $\varepsilon$; above it, outcomes are reported truthfully. The economic interpretation is
direct: the agent is writing a put option on their own outcomes, eliminating or reducing the
appearance of bad draws while leaving good draws intact. The formal specification is given
in Section 2.

Three propositions characterise the distributional consequences. Proposition 1 establishes
that the reported mean is biased upward by exactly the put option premium—real, but
undetectable from the reported series alone, since neither the true mean nor the premium is
observable. Proposition 2 establishes that total variance is strictly compressed. Proposition 3
is the central result: downside semivariance is compressed by exactly the square of the
attenuation factor, while total variance falls by strictly less—so the downside variance share
falls strictly. This result is entirely distribution-free, resting on a single almost-sure algebraic
identity and a bi-Lipschitz bound on the reporting map, requiring no moment conditions
beyond finite variance. A direct corollary: the Sortino ratio is inflated by misreporting strictly
more than the Sharpe ratio—with immediate implications for evaluating hedge fund and
private market performance.

We formalise two compression statistics. $C_{\sigma}$ measures overall volatility compression—the
standard deviation of reported outcomes. $C_{p}$, the bounded downside variance share, is
the ratio of squared deviations from below-mean observations to total squared deviations.
Under a symmetric distribution, $C_{p}$ converges to one-half; under the reporting put, it falls
strictly below one-half. The primary empirical challenge is that left-tail compression can
arise from two observationally equivalent mechanisms: a reporting put, where the agent
smooths the reported number without changing reality; and a policy put, where genuine
intervention—countercyclical fiscal policy, a sovereign wealth fund drawdown, illiquidity
buffers—compresses true outcomes before reporting. Proposition 5 establishes that these

[Page 5]
two mechanisms are not identified from the marginal distribution alone. This impossibility
result motivates a four-level identification hierarchy. Proposition 6 shows that a resource-
constrained policy put compresses both tails symmetrically—overall dispersion falls but the
downside share stays near one-half—while the reporting put compresses only the left tail,
pushing the downside share strictly below one-half. Because total-variance compression arises
under both mechanisms, the downside variance share is the sole differential diagnostic at this
level. Propositions 7 and 8 show how observable external transfers and valid auxiliary series
progressively sharpen identification.

Power analysis reveals the binding constraint. Fat tails—common in quarterly GDP growth
and illiquid asset returns—severely damage power, because they raise the sampling variance
of second-moment statistics. We show formally that the variance of the null statistic grows
linearly with excess kurtosis (Proposition 9): thicker tails require proportionally larger
samples for the same detection power. For GDP growth calibrated to a fat-tailed distribution,
detecting a 20 per cent misreporting intensity at 80 per cent power requires roughly 800
quarterly observations—four times the approximately 200 available from 50 years of data.
In near-normal earnings distributions, the same task requires roughly 200 observations. A
policy implication follows directly: for every manipulation intensity, there exists a reporting
frequency above which detection at conventional significance levels becomes feasible. In an
era of high-frequency administrative data, satellite imagery, and digital activity indicators,
the case for increasing reporting frequency carries a direct anti-manipulation rationale.

We also develop a joint two-moment diagnostic combining overall dispersion with the downside
variance share. Proposition 4 proves that these two statistics jointly identify the full strategy
space of asymmetric smoothing—and establishes the corollary that no smoothing strategy
can simultaneously leave both statistics unchanged. Table 1 in Section 2 summarises the
joint signatures.

The paper proceeds as follows. Section 2 presents the model and the three main distributional
propositions, together with the two-statistic framework. Section 3 formalises the four-level
identification hierarchy. Section 4 describes the applications and calibration. Section 5
presents simulation evidence. Section 6 concludes. Formal proofs are in Appendix A.

[Page 6]
# 2 The Model and Distributional Properties

## 2.1 Setup
Let $X$ be the true outcome of some economic or financial activity, drawn from a distribution $F$ with mean $\mu$, variance $\sigma^2$, and density $f$. The true outcome is never observed by the econometrician. We observe only the reported series $Y$, generated by the following rule.

**Definition 1 (One-Sided Reporting Rule).** The agent reports
$$ Y = X + \epsilon(\tau - X)^+, \quad \epsilon \in [0, 1], \quad (1) $$
where $(z)^+ = \max(z, 0)$, $\tau$ is an embarrassment threshold, and $\epsilon$ is the misreporting intensity. Equivalently,
$$ Y = \begin{cases} X & \text{if } X \ge \tau, \\ (1 - \epsilon)X + \epsilon\tau & \text{if } X < \tau. \end{cases} $$
Above $\tau$ the agent reports truthfully; below it, the shortfall $(\tau - X)$ is attenuated by the factor $(1 - \epsilon)$. The case $\epsilon = 0$ is full honesty; $\epsilon = 1$ maps every below-threshold realisation to exactly $\tau$. For corporate earnings, $\tau$ may represent zero, the prior-year figure, or the analyst consensus; for GDP, a growth target or prior-quarter outcome; for a fund manager, the high-water mark or a benchmark.

**Remark 1 (Path-dependent and endogenous thresholds).** In practice, $\tau$ may depend on the agent's own history—for example, a firm may target avoidance of an earnings decline relative to the prior quarter, making $\tau = Y_{t-1}$. The model treats $\tau$ as fixed and exogenous primarily for analytical tractability; the distributional properties of Propositions 1–3 hold conditionally on $\tau$ for any fixed value, so path-dependence introduces additional structure (the threshold itself becomes a random variable correlated with prior outcomes) but does not invalidate the compression identity in any given period. The inference framework of Proposition 9 applies cleanly when $\tau$ is genuinely exogenous; with an estimated or path-dependent $\tau$, inference requires additional care and the bootstrap is preferable.

We write $Z = (\tau - X)^+$ for the put payoff, $p = F(\tau)$ for the probability of a below-threshold realisation, and $P = E[Z] = E[(\tau - X)^+]$ for the put option value. For the Normal case $X \sim N(\mu, \sigma^2)$, let $k = (\tau - \mu)/\sigma$, $\phi$ and $\Phi$ denote the standard normal density and CDF, and define $A(k) = k\Phi(k) + \phi(k)$ and $h(t) = (1 + t^2)\Phi(t) + t\phi(t)$.

[Page 7]
## 2.2 Proposition 1: The Bias Has a Put Option Structure
**Proposition 1** (Mean Bias). For any distribution F with finite mean,
$$
E[Y] – E[X] = \varepsilon E[(\tau - X)^+] = \varepsilon P \ge 0,
$$
with equality if and only if $\varepsilon = 0$ or $F(\tau) = 0$. Under $X \sim N(\mu, \sigma^2)$, the bias equals $\varepsilon \sigma A(k)$ and is increasing in both $\varepsilon$ and $k$.

The proof is immediate: $E[Y] = E[X + \varepsilon Z] = \mu + \varepsilon P$ and $P \ge 0$ since $Z \ge 0$ everywhere. The economic insight matters more than the algebra. The bias is positive whenever there is positive probability of a below-threshold realisation, but it is *completely undetectable* from the reported series alone: an outside observer who sees only $E[Y]$ cannot distinguish a dishonest agent with true mean $\mu$ from an honest agent whose true mean happens to be $E[Y]$. The unobservability of $\mu$ and $P$ means that mean-based tests carry no power, motivating the variance-based approach.

The put-option framing is not merely metaphorical. The bias $\varepsilon P$ is the premium of a European put struck at $\tau$, written by the agent on their own outcomes, scaled by $\varepsilon$. It increases in the moneyness $A(k)$: thresholds set near or above the mean generate larger biases per unit of misreporting intensity.

## 2.3 Proposition 2: Variance Compression
**Proposition 2** (Variance Compression). For any distribution F with finite variance,
$$
\text{Var}(Y) = \sigma^2 + \varepsilon^2 \text{Var}(Z) + 2\varepsilon \text{Cov}(X, Z),
$$
where $\text{Cov}(X, Z) \le 0$ for any distribution F, with equality if and only if $F(\tau) = 0$. Consequently $\text{Var}(Y) < \text{Var}(X)$ for all $\varepsilon > 0$ with $F(\tau) > 0$. Under $X \sim N(\mu, \sigma^2)$,
$$
\text{Cov}(X, Z) = -\sigma^2 \Phi(k) \quad \text{and} \quad \text{Var}(Y) = \sigma^2 [1 - 2\varepsilon \Phi(k) + \varepsilon^2 V_Z / \sigma^2],
$$
where $V_Z = \text{Var}(Z) = (k^2 + 1)\Phi(k) + k\phi(k) - A(k)^2$. Variance compression is increasing in $\Phi(k)$: thresholds near the mean produce greater compression per unit of $\varepsilon$.

The key step is $\text{Cov}(X, Z) \le 0$. The put payoff $Z = (\tau - X)^+$ is a non-increasing function of $X$; for any non-increasing transformation $g$, $\text{Cov}(X, g(X)) \le 0$ by the standard covariance inequality. The Normal covariance formula $-\sigma^2 \Phi(k)$ follows from truncated-normal moment identities. Proofs are in Appendix A.

[Page 8]
Variance compression alone is not a reliable detection statistic. Total variance can fall for reasons unrelated to misreporting—genuine stabilisation policy, industry-wide low-volatility regimes, or thin-tailed true distributions. What is needed is a statistic specifically sensitive to the *one-sided* nature of the compression. This motivates Proposition 3.

## 2.4 Proposition 3: Downside Compression is Exact

**Definition 2** (Lower Partial Moment and Semivariance). For any random variable $W$ with $\mathbb{E}[W^2] < \infty$ and target $\tau \in \mathbb{R}$, the lower partial moment of order $p \ge 1$ is $\text{LPM}_{p,\tau}(W) = \mathbb{E}[(\tau - W)_+^p]$. The fixed-target downside semivariance is $\text{SV}_\tau(W) = \text{LPM}_{2,\tau}(W)$.

**Definition 3** (Bounded Downside Variance Share). For a sample $\{Y_t\}_{t=1}^N$ with mean $\bar{Y}$, define
$$
C_p = \frac{\sum_{t:Y_t < \bar{Y}} (Y_t - \bar{Y})^2}{\sum_{t=1}^N (Y_t - \bar{Y})^2},
\quad\quad(2)
$$
with $B = \{t : Y_t < \bar{Y}\}$. The statistic is bounded in $[0, 1]$ by construction. Under any distribution that is symmetric about its mean, has finite second moment, and places no probability mass at the mean, $C_p \to 0.5$ almost surely as $N \to \infty$.[^1]

**Proposition 3** (Fixed-Target Downside Compression). Let $X$ have $\mathbb{E}[X^2] < \infty$, let $\tau \in \mathbb{R}$, and let $\varepsilon \in [0, 1]$. Under rule (1):

(i) (Exact scaling). For every $p \ge 1$,
$$
(\tau - Y)_+ = (1 - \varepsilon)(\tau - X)_+ \quad \text{a.s.},
\quad\quad(3)
$$
and consequently $\text{LPM}_{p,\tau}(Y) = (1 - \varepsilon)^p \text{LPM}_{p,\tau}(X)$. In particular $\text{SV}_\tau(Y) = (1 - \varepsilon)^2 \text{SV}_\tau(X)$.

(ii) (Variance sandwich). $(1 - \varepsilon)^2\text{Var}(X) \le \text{Var}(Y) \le \text{Var}(X)$, with both inequalities strict whenever $\varepsilon > 0$, $\text{Var}(X) > 0$, $\mathbb{P}(X < \tau) > 0$, and $\mathbb{P}(X > \tau) > 0$.

(iii) (Ratio compression).
$$
\frac{\text{SV}_\tau(Y)}{\text{Var}(Y)} \le \frac{\text{SV}_\tau(X)}{\text{Var}(X)},
\quad\quad(4)
$$
with strict inequality under the conditions of (ii).

---
[^1]: The condition that $F$ places no atom at the mean rules out degenerate edge cases in which a positive fraction of observations lies exactly on the partition boundary $\bar{Y}$. For continuous distributions the condition is automatic.

[Page 9]
(iv) (Sortino inflates more than Sharpe). For $\text{E}[X] > \tau$, define $\text{Sharpe}_{\tau}(W) = (\text{E}[W] – \tau)/\sqrt{\text{Var}(W)}$ and $\text{Sortino}_{\tau}(W) = (\text{E}[W] – \tau)/\sqrt{\text{SV}_{\tau}(W)}$. Then
$$
\frac{\text{Sortino}_{\tau}(Y)}{\text{Sortino}_{\tau}(X)} > \frac{\text{Sharpe}_{\tau}(Y)}{\text{Sharpe}_{\tau}(X)}, \quad (5)
$$
with strict inequality under the conditions of (ii).

Proposition 3 is the paper's central result. Parts (i)–(iv) are entirely distribution-free: they hold for any F with $\text{E}[X^2] < \infty$, requiring no symmetry, no log-concavity, and no specification of the tails. This distribution-free property applies specifically to the fixed-target semivariance $\text{SV}_{\tau}$, and the variance bounds; the operational $C_p$ statistic uses the sample mean $\bar{Y}$ as the partition point, and the stronger claim that $C_p$ is strictly decreasing in $\varepsilon$ at the population level is established under normality (Remark 2). Part (i) rests on an almost-sure identity (3) whose proof is a two-case verification: on $\{X \ge \tau\}$ both sides are zero; on $\{X < \tau\}$, the reporting rule gives $\tau - Y = (1 - \varepsilon)(\tau - X) > 0$ exactly. Nothing more is needed—no moment conditions, no continuity, no symmetry. The result propagates to all LPMs by raising to the power $p$ and taking expectations.

Part (ii) proves the variance sandwich by a bi-Lipschitz argument. The reporting map $g$ satisfies $(1 - \varepsilon)|x - y| \le |g(x) - g(y)| \le |x - y|$ for all $x,y$ (Lemma 2). Applying the pairwise-distance identity $\text{Var}(U) = \frac{1}{2}\text{E}[(U - U')^2]$ to both sides yields both bounds. The upper bound is tight on the event $\{X, X' \ge \tau\}$; the lower bound is strict on the event $\{X < \tau < X'\}$.

Part (iii) follows from combining (i) and (ii): $\text{SV}_{\tau}(Y)$ falls by the full factor $(1 - \varepsilon)^2$ exactly, while $\text{Var}(Y)$ falls by strictly less, so the ratio $\text{SV}_{\tau}/\text{Var}$ falls strictly. This is the operational content of $C_p$ as a detection statistic: one-sided misreporting compresses the numerator faster than the denominator.

Part (iv) has direct implications for asset management. The Sortino denominator $\sqrt{\text{SV}_{\tau}(Y)}$ is compressed by the full factor $(1 - \varepsilon)$, while the Sharpe denominator $\sqrt{\text{Var}(Y)}$ is compressed by strictly less. With the same inflated numerator (from Proposition 1), the Sortino ratio is therefore inflated more. For a hedge fund with $\varepsilon = 0.30$, the Sortino ratio is inflated by approximately $1/(1 - 0.30) \approx 43\%$ at the upper bound, while the Sharpe ratio inflation is bounded below 43%; simulations in Section 5 quantify the differential precisely.

**Corollary 1 (Sortino Deflation Bound).** For any suspected misreporting intensity $\varepsilon \in [0, 1]$, the true Sortino ratio satisfies
$$
\text{Sortino}_{\tau}(X) \le (1 - \varepsilon) \cdot \text{Sortino}_{\tau}(Y), \quad (6)
$$

[Page 10]
with strict inequality whenever $\varepsilon > 0$ and $F(\tau) > 0$ (i.e. whenever there is positive probability
of a below-threshold realisation under the true distribution).

*Proof.* From part (i), $SV_{\tau}(Y) = (1-\varepsilon)^2 SV_{\tau}(X)$, so $\sqrt{SV_{\tau}(Y)} = (1 - \varepsilon)\sqrt{SV_{\tau}(X)}$. Therefore
$(1 - \varepsilon) \cdot \text{Sortino}_{\tau}(Y) = (\text{E}[Y] - \tau)/\sqrt{SV_{\tau}(X)}$. From Proposition 1, $\text{E}[Y] \ge \text{E}[X]$ with equality
iff $\varepsilon = 0$ or $F(\tau) = 0$. Hence $(\text{E}[Y] - \tau)/\sqrt{SV_{\tau}(X)} \ge (\text{E}[X] - \tau)/\sqrt{SV_{\tau}(X)} = \text{Sortino}_{\tau}(X)$.
$\square$

Equation (6) provides a practical sensitivity analysis tool. An investor who suspects a fund
of smoothing returns with intensity $\varepsilon$ can immediately compute the adjusted Sortino and
interpret it as the best-case true performance conditional on that suspicion. The bound
is strict whenever $F(\tau) > 0$: since mean bias is then strictly positive (Proposition 1), the
adjusted Sortino $(1-\varepsilon) \cdot \text{Sortino}_{\tau}(Y)$ strictly exceeds the true Sortino $\text{Sortino}_{\tau}(X)$, confirming
it is a conservative upper bound, not a point estimate. For $\varepsilon = 0.20$, the reported Sortino
overstates true performance by at least 25%; for $\varepsilon = 0.40$, by at least 67%. The bound
tightens when the threshold $\tau$ is set well below the mean (low moneyness), because the mean
bias $\varepsilon P$ shrinks as the put option goes out of the money.

*Remark 2* (Mean-based $C_p$ and the Normal case). The fixed-target result above uses $\tau$ as
the benchmark in both the reporting rule and the LPM. When the benchmark in (2) is the
contaminated sample mean $\bar{Y}$, the identity (3) no longer holds because $\bar{Y}$ moves with $\varepsilon$.
Under normality, the population ratio $R(\varepsilon) = \text{SV}_{\mu_Y}(Y)/\text{Var}(Y)$ is strictly decreasing in $\varepsilon$ for
all $k$ and all $\varepsilon \in [0,1)$; the argument is developed in Appendix A and is complete up to a
boundary comparison that is verified numerically across the full parameter range.

*Remark 3* (Null value under skewed distributions). The null value $C_p = 0.5$ relies on the
symmetry of $F_X$. When $F_X$ is asymmetric, the population $C_p$ under honest reporting satisfies
$$
\rho_{\mu}(F) = \frac{\text{E}[(Y - \mu)^2 \mathbf{1}[Y < \mu]]}{\sigma^2} = \frac{1}{2} \frac{\text{E}[(Y - \mu)|Y - \mu|]}{2\sigma^2} \quad (7)
$$
The signed second moment $\text{E}[(Y - \mu)|Y - \mu|]$ is positive under right skew and negative
under left skew. Consequently, for a right-skewed true distribution—common in earnings
levels, private-equity returns, and commodity prices—the honest null value lies below 0.5.
A test calibrated to 0.5 would over-reject for right-skewed $F_X$. In applications where $F_X$ is
known or suspected to be asymmetric, three corrections are available: (i) use a reference
period of independently verified clean outcomes to estimate $\rho_{\mu}(F)$ and test against that
estimated null; (ii) apply a variance-stabilising transformation (e.g. Box-Cox) to approximate
symmetry before constructing $C_{\rho}$—though note that applying a nonlinear transformation to
the already-manipulated $Y$ preserves the exact scaling identity of Proposition 3(i) under the

[Page 11]
null but may distort the power properties under the alternative, since the linear reporting map $g(x) = x + \varepsilon(\tau - x)_+$ is no longer linear after transformation; the first correction is therefore preferable when a clean reference period is available; or (iii) restrict to the fixed-target version with an exogenous $\tau$ set below the mean, where the honest null is below 0.5 for mechanical reasons and an alternative null can be derived from distributional assumptions. The skewness correction $\hat{\rho}_p = \rho_p(\hat{F})$ in (7) is consistently estimable from the sample.

## 2.5 The Two-Statistic Diagnostic Framework

Proposition 3 concerns one-sided misreporting. A sophisticated agent aware of the $C_p$ test might adapt by smoothing both tails symmetrically, maintaining $C_p \approx 0.5$ while compressing the distribution. We embed the model in a general asymmetric framework to characterise what the agent can and cannot evade.

**Definition 4** (Asymmetric Smoothing Rule). The agent reports $Y = \mu_\tau + \lambda_U(X – \mu_\tau)$ when $X \ge \mu_\tau$ and $Y = \mu_\tau + \lambda_D(X - \mu_\tau)$ when $X < \mu_\tau$, for pass-through coefficients $\lambda_U, \lambda_D \in (0, 1]$. The one-sided reporting put is the special case $\lambda_U = 1$, $\lambda_D = 1 - \varepsilon$. Symmetric smoothing is $\lambda_U = \lambda_D = \lambda$. Define $C_\sigma = (\sum_t(Y_t - \bar{Y})^2)^{1/2}$.

**Proposition 4** (Two-Statistic Identification). Let $X$ be symmetrically distributed about $\mu_\tau$.

(i) (Symmetric smoothing leaves $C_p$ unchanged.) Under $\lambda_U = \lambda_D = \lambda$: $C_p(Y) = C_p(X)$ exactly, for any distribution and any sample size $N$. Simultaneously, $C_\sigma(Y) = \lambda C_\sigma(X) < C_\sigma(X)$.

(ii) (One-sided put shifts $C_p$ while $C_\sigma$ also falls weakly but is not differentially diagnostic.) Under $\lambda_U = 1$, $\lambda_D = 1 - \varepsilon$: $C_p(Y) < 0.5$ (Proposition 3), and $C_\sigma(Y) \le C_\sigma(X)$ (Proposition 2). Both mechanisms in the identification hierarchy produce $C_\sigma \le \sigma$; the identifying content is in $C_p$, not $C_\sigma$, at this level.

(iii) (Joint identification.) Under symmetric $F_X$, to leading order: $C_\sigma(Y)^2 \approx \frac{1}{2}(\lambda_U^2 + \lambda_D^2)\sigma_X^2$ and $C_p(Y) \approx \lambda_U^2 / (\lambda_U^2 + \lambda_D^2)$. The map $(\lambda_U, \lambda_D) \leftrightarrow (C_\sigma, C_p)$ is injective: different strategies produce different joint signatures.

(iv) (No strategy is jointly undetectable.) There is no $(\lambda_U, \lambda_D) \ne (1, 1)$ such that both $C_\sigma(Y) = C_\sigma(X)$ and $C_p(Y) = C_p(X)$ simultaneously.

Part (i) establishes the key insight. Under symmetric smoothing, $Y_t - \bar{Y} = \lambda(X_t - \bar{X})$ for all $t$, so $\lambda^2$ cancels exactly in the ratio defining $C_p$. The statistic is scale-invariant to uniform shrinkage of deviations from the mean. But $C_\sigma$ captures exactly this shrinkage: $C_\sigma(Y) = \lambda C_\sigma(X)$. An agent who evades $C_p$ by two-siding their smoothing will be detected through $C_\sigma$.

[Page 12]
Table 1: Joint ($C_\sigma, C_\rho$) signatures under different mechanisms
| Mechanism | $C_\sigma$ | $C_\rho$ |
| :--- | :--- | :--- |
| Honest reporting | $= \sigma$ | $= 0.5$ |
| One-sided reporting put ($\lambda_D < 1 = \lambda_U$) | $\le \sigma$ | $< 0.5$ |
| Symmetric two-sided smoothing ($\lambda_U = \lambda_D < 1$) | $< \sigma$ | $= 0.5$ |
| Asymmetric ($\lambda_U > \lambda_D$, both $< 1$) | $< \sigma$ | $< 0.5$ |

*Notes*: Large-sample values under symmetric $F_X$. $C_\sigma \le \sigma$ under the one-sided put (Proposition 2); $C_\rho$ is the differential diagnostic between one-sided misreporting and symmetric two-sided smoothing.

Part (iv), proved by contradiction from part (iii), is the spanning result: the combination ($C_\sigma, C_\rho$) covers the full space of smoothing strategies. Any misreporting moves at least one statistic. Moreover, any switch from one-sided to two-sided smoothing generates a detectable change in the *joint* time-series path of ($C_\sigma, C_\rho$): $C_\rho$ rises toward 0.5 while $C_\sigma$ falls, a combination that has no innocent interpretation for an agent whose fundamental economic environment has not changed.

Table 1 reproduces the joint signatures for reference.

The results in this section establish that a one-sided reporting put leaves a characteristic, detectable footprint in the second moments of the reported series. The signal exists, and it is sharp: Propositions 3 and 4 characterise precisely which statistics respond and how. What the distributional analysis cannot resolve, however, is *attribution*: a compressed left tail could equally reflect deliberate manipulation of reported numbers or genuine economic intervention that smoothed true outcomes before reporting. Section 3 turns to this identification problem. It constructs a four-level hierarchy that uses progressively richer auxiliary information to separate the two mechanisms, and characterises at each level what the researcher can and cannot conclude from an observed low $C_\rho$.

# 3 Econometric Identification

## 3.1 The Fundamental Identification Problem

Proposition 3 establishes that a reporting put compresses the downside variance share $C_\rho$. The practical challenge is interpretation: a low $C_\rho$ is consistent with misreporting but also consistent with genuine stabilisation policy that attenuates negative outcomes through real economic intervention. We call the latter a *policy put*. Both mechanisms produce a reported distribution with a compressed left tail, and the statistics $C_\sigma$ and $C_\rho$ cannot, on their own,

[Page 13]
distinguish between them without further information.

**Definition 5** (Reporting Put and Policy Put). A reporting put is a misreporting rule of the form (1) applied to the reported number $Y$, with the true outcome $X$ unchanged. A policy put is a genuine intervention that transforms the true outcome $X$ into a smoother realised outcome $X'$, which is then reported honestly as $Y = X'$.

**Proposition 5** (Non-Identification). For any true distribution $F_X$ and any reporting put parametrised by $(\varepsilon, \tau)$, there exists a policy put producing the same observed distribution $F_Y$. The two mechanisms are not identified from the marginal distribution of $Y$ alone.

The proof is constructive: define the policy-transformed distribution as $F_Y$ itself, and set $Y' = X'$ (honest reporting of the smoothed outcome). Then $Y'$ has the same marginal distribution as $Y$ under the reporting put. Proposition 5 is an exact impossibility result, not an approximation. It implies that any test based solely on moments or distributional shape of $Y$—including $C_p$—cannot rule out the policy-put explanation without additional information. The propositions below identify precisely what additional information is needed and sufficient at each level of a four-level hierarchy.

## 3.2 Level 1: Identification from the Resource Constraint

The fundamental economic difference between the two mechanisms is cost. A reporting put is free: the agent records a different number and no real resources change hands. A policy put requires real resources: governments must finance fiscal stabilisers; fund managers must hold liquid buffers; firms must maintain balance sheet reserves. These resources must come from somewhere.

**Definition 6** (Resource-Constrained Policy Put). A policy put is resource-constrained if the expected value of resources deployed to attenuate negative outcomes equals the expected value of resources accumulated by taxing positive outcomes. Formally, if $\delta(x)$ is the policy transfer at true outcome $x$, the constraint requires $E[\delta(X)] = 0$: policy is redistributive across the distribution, not a free external transfer.²

**Proposition 6** (Identification from Resource Constraint). Under a resource-constrained policy put, $E[Y] = E[X]$ and both tails of $Y$ are compressed, so $C_p(Y) \approx 0.5$ while $C_{\sigma}(Y) < \sigma$. Under a reporting put, $E[Y] > E[X]$ and only the left tail is compressed, so $C_p(Y) < 0.5$. Proposition 2 implies that $C_{\sigma}(Y) \le \sigma$ under the reporting put as well (total variance is weakly

---
²In practice, governments may run a structural fiscal deficit ($E[\delta(X)] < 0$) or surplus, so the zero-mean condition is not exactly satisfied. Small deviations of order $|E[\delta]| = O(\sigma/\sqrt{N})$ contribute $O(N^{-1/2})$ to $C_p$, leaving its population value near but not exactly 0.5. The signature $C_p \approx 0.5$ therefore remains valid as a large-sample characterisation of resource-constrained policy. Larger persistent deficits or surpluses are captured by Level 2 of the hierarchy: if $E[\delta(X)] \ne 0$ measurably, the net transfer is observable in fiscal accounts and the transfer-adjusted series $\tilde{Y} = Y - T$ restores the zero-mean condition.

[Page 14]
compressed whenever $\varepsilon > 0$ and $F(\tau) > 0$), so total-variance compression is not a differential diagnostic: both mechanisms produce $C_\sigma \le \sigma$. The identifying information resides entirely in $C_p$. The joint signature $(C_\sigma, C_p)$ therefore partially identifies the mechanism:

*   Resource-constrained policy put: $C_p \approx 0.5$, $C_\sigma < \sigma$.
*   Reporting put: $C_p < 0.5$, $C_\sigma \le \sigma$ ($C_p$ is the sole differential diagnostic at this level).

The argument proceeds as follows. Under $E[\delta(X)] = 0$, resources are redistributed across the distribution: $\delta(x) > 0$ for low $x$ (bad outcomes are cushioned) and $\delta(x) < 0$ for high $x$ (good outcomes are taxed to finance the buffer). Both tails are compressed, giving $C_p \approx 0.5$ and $C_\sigma < \sigma$. This is the signature of sovereign wealth funds, commodity stabilisation mechanisms, and countercyclical fiscal frameworks: reserves accumulated in good times (compressing the right tail) deployed in bad times (compressing the left tail). The reporting put carries no cost and no obligation to compress the right tail: it produces one-sided left-tail compression, pushing $C_p$ below 0.5 while $C_\sigma$ also weakly falls but is not differentially diagnostic at this level of the hierarchy.

*Remark 4* (Borrowing and inter-period constraints). Foreign borrowing does not constitute a free external resource because debt service obligations make the resource constraint hold in present-value terms across periods. A government that borrows in bad times must repay in good times, compressing the upside in future periods. Proposition 6 therefore applies to borrowing-financed policy puts evaluated over a sufficiently long horizon, and the two-sided compression signature obtains with a temporal lag.

## 3.3 Level 2: Identification Conditional on External Transfers

The one case where Proposition 6 does not deliver identification is an externally financed policy put: a government receiving aid grants or an economy experiencing an unencumbered resource windfall can finance downside protection without compressing the upside. In this case, $E[\delta(X)] > 0$ and the policy put may produce low $C_p$ with near-stable $C_\sigma$ for entirely legitimate reasons.

*Proposition 7* (Identification Conditional on External Transfers). Let $T$ denote the observable flow of free external resources (aid grants, unencumbered commodity windfalls). Define the transfer-adjusted outcome $\tilde{Y} = Y - T$. Under the policy put, $C_p(\tilde{Y}) \approx 0.5$; under the reporting put, $C_p(\tilde{Y}) < 0.5$. Since aid flows and grant receipts are recorded in balance of payments data and resource revenues as a share of GDP are well-documented, conditioning on $T$ resolves the confound.

The proof decomposes the total transfer into an internally financed component (zero mean,

[Page 15]
producing symmetric compression) and an external component equal to $T$. After subtracting $T$, the externally financed smoothing is removed, and the residual $\tilde{Y}$ reverts to symmetric compression under the policy put. Under the reporting put, $T$ is unrelated to the misreporting mechanism, so $\tilde{Y}$ retains the one-sided compression: $C_p(\tilde{Y}) < 0.5$.

## 3.4 Level 3: Identification from an Auxiliary Series

The cleanest identification uses an auxiliary observable that co-moves with the true outcome $X$ but cannot be manipulated through the reporting rule.

**Definition 7** (Valid Auxiliary Series). A series $Z$ is a *valid auxiliary* for $Y$ if: (i) $\text{Cov}(Z, X) \neq 0$; and (ii) $Z$ is invariant to the reporting rule: the agent's choice of $\varepsilon$ and $\tau$ does not affect $Z$.

Natural candidates in the GDP application include satellite nighttime light intensity (Henderson et al., 2012), electricity consumption, fiscal revenue outturns, and corporate earnings—all of which track economic activity through channels independent of the national statistical agency. In the fund return application, candidates include transaction-level trading data, broker confirmations, or third-party index benchmarks.

**Proposition 8** (Identification from Auxiliary Series). Let $Z$ be a valid auxiliary series and let $\hat{u} = Y - \hat{Y}(Z)$ be the residual of $Y$ projected on $Z$. Under the policy put, $C_p(\hat{u}) \approx 0.5$. Under the reporting put, $C_p(\hat{u}) < 0.5$.

Under the policy put, both $Y$ and $Z$ reflect the same genuinely smoother true outcome $X'$. Their joint distribution is symmetric conditional on the policy, so the projection residual $\hat{u}$ inherits no systematic asymmetry and $C_p(\hat{u}) \approx 0.5$.

Under the reporting put, $Z$ tracks the true $X$ while $Y$ is manipulated. In the left tail of $Z$—when $Z$ is low, signalling a bad true outcome—$Y$ is artificially elevated because the reporting rule replaces low $X$ values with something closer to $\tau$. The linear projection $\hat{Y}(Z)$ does not capture this elevation because $Z$ is correlated with the magnitude of manipulation: $\text{Cov}(Z, (\tau - X)^+) < 0$ since $Z$ co-moves positively with $X$ while $(\tau - X)^+$ is non-increasing in $X$. The residual $\hat{u}$ therefore retains a compressed left tail, and $C_p(\hat{u}) < 0.5$.

## 3.5 The Identification Hierarchy

Table 2 summarises the four levels. Each requires strictly more data than the previous but delivers progressively stronger identification.

Two features deserve emphasis. First, Levels 1 and 2 are available in the GDP application— external transfers and resource revenues are recorded in balance of payments data and national accounts—while Level 3 requires the construction of a suitable auxiliary series, which is

[Page 16]
Table 2: Four-level identification hierarchy

| | Additional data | Under reporting put | Under policy put |
| :--- | :--- | :--- | :--- |
| 0 | None | $C_p < 0.5$ | $C_p < 0.5$ (not identified) |
| 1 | Resource constraint | $C_p < 0.5$, $C_\sigma \le \sigma$ | $C_\sigma \approx 0.5$, $C_\sigma \le \sigma$ |
| 2 | Observable transfers T | $C_p(\tilde{Y}) < 0.5$ | $C_p(\tilde{Y}) \approx 0.5$ |
| 3 | Valid auxiliary Z | $C_p(\hat{u}) < 0.5$ | $C_p(\hat{u}) \approx 0.5$ |

*Notes*: $\tilde{Y} = Y - T$; $\hat{u}$ = residual of Y projected on Z. Levels 1-3 correspond to Propositions 6–8. “$\approx 0.5$” reflects the population value under symmetric $F_X$; finite-sample deviations from 0.5 under the policy put are mean-zero and $O(N^{-1/2})$. At Level 1, both mechanisms produce $C_\sigma \le \sigma$ (Proposition 2), so $C_\sigma$ is not a differential diagnostic; $C_p$ is the identifying statistic.

feasible only in some country-years. Second, in the fund return application, the absence of reliable transaction-level data for illiquid assets means Level 3 is often unavailable, and the researcher must rely on Levels 1 or 2, or interpret a significant $C_p$ in conjunction with the known incentive structure. The hierarchy makes clear that a low $C_p$ is always necessary but not sufficient evidence of misreporting: its evidentiary weight depends on which level of identification the researcher can credibly claim.

## 3.6 Asymptotic Inference for the Fixed-Target Statistic

Operational inference requires a null distribution for $C_p$. The identification hierarchy above uses $C_p$ applied to progressively adjusted series ($\tilde{Y}$, $\hat{Y} = Y - T$, $\hat{u}$), but in each case the key test is one-sided: does the statistic fall significantly below its null value of 0.5?

Two versions of the statistic are available. The *mean-based* version uses the sample mean $\bar{Y}$ as the partition boundary, as defined in (2). The *fixed-target* version uses an exogenous threshold $\tau$ that is known to the researcher independently of the data—for example, zero earnings, a statutory growth target, or a fund benchmark. The fixed-target version is preferable when $\tau$ is available, because the partition boundary does not move with the sample; the result below shows this makes the delta method a direct application of the standard CLT with no moving-boundary correction required.

**Proposition 9** (Asymptotic Distribution of the Fixed-Target Statistic). *Let $\{Y_i\}_{i=1}^N$ be i.i.d. from a distribution with mean $\mu$, variance $\sigma^2 > 0$, and finite fourth moment $\mu_4 = \text{E}[(Y - \mu)^4]$.*

[Page 17]
Let $\tau \in \mathbb{R}$ be a fixed exogenous threshold, and define the fixed-target downside variance share
$$
\hat{p}_\tau = \frac{\frac{1}{N} \sum_t (Y_t - \tau)^2 \mathbf{1}[Y_t < \tau]}{\frac{1}{N} \sum_t (Y_t - \tau)^2}.
$$
Let $p_\tau = \mathrm{E}[(Y - \tau)^2 \mathbf{1}[Y < \tau]] / \mathrm{E}[(Y - \tau)^2]$ be the population value. Then
$$
\sqrt{N}(\hat{p}_\tau - p_\tau) \to \mathcal{N}(0, \omega^2),
$$
where $\omega^2 = \mathrm{Var}(\psi) / \mathrm{E}[(Y - \tau)^2]^2$ and $\psi = (Y - \tau)^2(\mathbf{1}[Y < \tau] - p_\tau)$ is the influence function.
Under the null $H_0: p_\tau = p_0$ with symmetric $F$ and $\tau = \mu$,
$$
\omega_0^2 = \frac{3 + \kappa}{4},
\tag{8}
$$
where $\kappa = \mu_4/\sigma^4 - 3$ is the excess kurtosis of $F$. The following plug-in estimator of $\omega^2$ is consistent:
$$
\hat{\psi}_t = (Y_t - \tau)^2(\mathbf{1}[Y_t < \tau] - \hat{p}_\tau), \quad \hat{\omega}^2 = \frac{\frac{1}{N} \sum_{t=1}^N \hat{\psi}_t^2}{\hat{B}^2},
\tag{9}
$$
where $\hat{B} = \frac{1}{N} \sum_t (Y_t - \tau)^2$. The one-sided test of $H_0: p_\tau = p_0 = 0.5$ rejects when
$$
T_N = \frac{\sqrt{N}(\hat{p}_\tau - p_0)}{\hat{\omega}} < z_\alpha,
\tag{10}
$$
where $z_\alpha$ is the $\alpha$-quantile of the standard normal.

*Proof sketch.* Since $\tau$ is fixed, $(Y_t - \tau)^2 \mathbf{1}[Y_t < \tau]$ and $(Y_t - \tau)^2$ are both ordinary i.i.d. random variables with finite variances (given $\mathrm{E}[Y^4] < \infty$). The ratio $\hat{p}_\tau = \hat{A}/\hat{B}$ is a smooth function of two sample means; the delta method gives $\sqrt{N}(\hat{p}_\tau - p_\tau) \to \mathcal{N}(0, \omega^2)$ with $\omega^2 = \mathrm{Var}(A - p_\tau B)/\mathrm{E}[B]^2$, which simplifies to the stated form. The key simplification absent in the mean-based case is that the indicator $\mathbf{1}[Y_t < \tau]$ is a fixed measurable function of $Y_t$ alone; no correction for an estimated boundary is required. The null formula (8) follows from $\mathrm{E}[(Y - \mu)^4 \mathbf{1}[Y < \mu]] = \frac{1}{2}\mu_4$ under symmetry, yielding $\mathrm{Var}(\psi) = \frac{1}{2}\mu_4$ and $\mathrm{E}[B]^2 = \sigma^4$. □

*Remark 5* (Kurtosis determines the width of the null distribution). Formula (8) has direct practical content. Under normality ($\kappa = 0$), $\omega_0^2 = 3/4$ and the asymptotic standard deviation is $\sqrt{3/4N}$. Under $t_5$ ($\kappa = 6$), $\omega_0^2 = 9/4$—three times larger—so the null distribution is $\sqrt{3} \approx 1.73$ times wider. This is the exact theoretical mechanism behind the power degradation seen in the GDP application: the null is wide because fat tails inflate the fourth moment in (8), and the signal $|p_\tau - 0.5|$ is held fixed by the misreporting intensity $\varepsilon$. The formula also

[Page 18]
makes clear that the fourth moment is the binding regularity condition for valid inference: if
$\kappa = \infty$ (e.g. $t_3$), the asymptotic variance is infinite and the normal approximation breaks
down, requiring either trimming or the bootstrap.

*Remark 6 (Mean-based $C_p$ and inference).* When the threshold $\tau$ is unobserved and replaced
by the sample mean $\bar{Y}$, the moving boundary introduces a correction to the influence function
through the dependence of $\mathbf{1}[Y_i < \bar{Y}]$ on $\bar{Y}$. While this correction is asymptotically negligible
in some smooth cases (the gradient of the boundary contribution evaluates to zero under
continuity of $F$ at $\mu$), a complete derivation of the asymptotic null distribution for the
mean-based statistic is beyond the scope of this paper. The bootstrap symmetrisation
procedure—which conditions on the observed marginal distribution rather than relying
on a parametric limit—avoids this issue entirely. Section 5 documents the finite-sample
consequences of the two approaches.

*Remark 7 (Dependence and time-series applications).* Proposition 9 assumes $\{Y_i\}$ is i.i.d.
In time-series applications—GDP growth, fund returns, earnings—the true outcomes may
exhibit serial dependence. Under weak dependence (e.g., $\beta$-mixing with summable coefficients),
the delta-method CLT still applies with the long-run variance replacing $\text{Var}(\psi)$ in $\omega^2$; a
heteroskedasticity and autocorrelation consistent (HAC) estimator can be substituted for the
sample variance of $\psi_t$ in equation (9) without changing the test construction (10). Simulation
evidence in Section 5 is calibrated to i.i.d. draws; HAC adjustment is advisable in applications
where serial correlation is plausible.

# 4 Data, Applications, and Calibration

## 4.1 Overview

The theoretical framework applies to any setting in which an agent controls a reported
number and faces asymmetric incentives over its value. To ground the simulation analysis and
make the power results interpretable, we calibrate to four empirically distinct applications:
quarterly GDP reporting, hedge fund monthly returns, corporate quarterly earnings, and
private equity quarterly net asset values. These applications differ along three dimensions
that determine the properties of the $C_p$ test—sample size, the tail behaviour of the true
underlying distribution, and the plausible magnitude of misreporting. Table 3 provides a
compact summary.

[Page 19]
Table 3: Calibration summary by application

| Application | Freq. | Horizon | N | True distribution | Key reference |
| :--- | :--- | :--- | :--- | :--- | :--- |
| GDP (quarterly) | Q | 50 yr | 200 | $t_5$ | Martinez 2022 |
| Hedge funds (monthly) | M | 10 yr | 120 | Normal | Getmansky et al. 2004 |
| Earnings (quarterly) | Q | 25 yr | 100 | Normal | Burgstahler and Dichev 1997 |
| Private equity (quarterly) | Q | 10 yr | 40 | Normal | Brown et al. 2019 |

## 4.2 Quarterly GDP Growth

Quarterly GDP growth rates exhibit substantial fat tails, driven by financial crisis episodes, natural disasters, and pandemic shocks. For a single country over 50 years ($N \approx 200$ quarterly observations), the empirical excess kurtosis of growth rate residuals is of the order of 15–30 in countries with histories of macroeconomic instability, and of order 5–10 in stable advanced economies, even after the COVID-19 shock. We calibrate to a Student-t distribution with five degrees of freedom (excess kurtosis of 6), which represents a conservative choice relative to the upper end of this range and is consistent with established evidence on fat tails in macroeconomic growth distributions (Fagiolo et al., 2008).

The threshold $\tau$ is set at the sample median of each simulated series, corresponding to the specification where the agent seeks to avoid below-average reported growth. In practice, a government may target a specific rate (e.g. a constitutional growth guarantee or a publicly announced objective) or the prior-period figure; sensitivity to the threshold location is examined in Section 5.

We treat $N = 200$ as the baseline. Many developing-economy series begin later, giving $N$ in the range 100–150; some countries in the sample have very short series (post-independence or post-reform), where power is correspondingly lower. The frequency analysis in Section 5 examines the power gain from moving to monthly or weekly administrative data.

## 4.3 Hedge Fund Returns

We calibrate to a monthly return series with a ten-year horizon ($N = 120$), consistent with the typical history available for a fund at the point of due diligence or regulatory review. The true underlying distribution is modelled as normal with mean 0.5% per month and standard deviation 2% per month (approximately 6% annualised volatility), consistent with equity long-short strategies in the TASS and HFR databases (Getmansky et al., 2004).

We model the true returns as i.i.d. normal, abstracting from the genuine serial correlation documented by Getmansky et al. (2004) arising from illiquid asset pricing. This is conservative:

[Page 20]
genuine serial correlation in the true returns would reduce the effective sample size and
further lower test power. The misreporting model captures the discretionary smoothing
component—the manager’s choice to maintain stale marks on illiquid positions—on top of
any mechanical smoothing from stale prices.

The threshold $\tau$ is set at zero, consistent with the finding by Bollen and Pool (2009) of a return
distribution discontinuity just above zero. The Sortino inflation result of Proposition 3(iv) is
of particular relevance in this application, where institutional investors routinely compare
managers on downside-adjusted performance metrics.

## 4.4 Corporate Earnings
For corporate earnings per share, we calibrate to a quarterly series with a 25-year horizon
($N = 100$). The distribution of quarterly earnings surprises is approximately normal with
mean zero (standardised as deviations from analyst consensus) and unit standard deviation
(Burgstahler and Dichev, 1997). This is the thin-tailed setting in which $C_p$ has the most
power and serves as a benchmark for the fat-tailed GDP case.

The threshold $\tau$ is set at zero (missing the consensus forecast) or the prior-quarter figure
(avoiding a year-over-year decline). Both thresholds are economically relevant—Burgstahler
and Dichev (1997) document discontinuities at both—and we use the sample median as a
computationally tractable approximation.

## 4.5 Private Equity
The private equity application is characterised by a small sample ($N = 40$ quarterly NAV
observations for a fund with a ten-year life), a near-normal true distribution, and a strong
structural motive for smoothing: NAV marks affect fundraising prospects and fee income
(Brown et al., 2019; Jenkinson et al., 2013). The small N makes this the most power-limited
application, and the simulation results directly quantify the detection constraint.

## 4.6 Calibrating the Misreporting Intensity
The misreporting intensity $\varepsilon$ is not directly observable, but a range of indirect evidence
suggests plausible values. In corporate earnings, the magnitude of the discontinuity at zero
documented by Burgstahler and Dichev (1997) implies that roughly 8–12% of below-threshold
firms shift their reported earnings above the threshold, consistent with $\varepsilon$ in the range 0.10–
0.20 for a representative firm. In GDP reporting, Martinez (2022) estimates that autocratic
governments overstate growth by approximately 35% relative to light-based benchmarks,

[Page 21]
which for a distribution with $\Phi(k) \approx 0.5$ implies $\varepsilon$ in the range 0.25–0.40. For hedge funds, Getmansky et al. (2004) estimate that illiquid funds smooth between 10 and 30% of returns across periods, broadly consistent with $\varepsilon \in [0.10, 0.30]$. These ranges motivate our focus on $\varepsilon \in [0, 0.5]$ in the power analysis.

## 4.7 The Bootstrap Test Procedure
The $C_p$ statistic is computed as in Definition 3. Under the null of honest symmetric reporting, $C_p \to 0.5$ in probability. The test rejects for significantly low values. In practice, the finite-sample null distribution of $C_p$ depends on the tail thickness of the true distribution, which is unknown, so we use a bootstrap procedure.

The bootstrap null is constructed by symmetrising the observed series around its sample mean: for observed $\{Y_i\}$ with mean $\bar{Y}$, define the symmetrised pool $\{Y_i\} \cup \{2\bar{Y} – Y_i\}$ of size $2N$, which is symmetric by construction. Bootstrap resamples of size $N$ are drawn from this pool with replacement, and $C_p$ is computed for each resample. The $\alpha$ critical value is the $\alpha$th percentile of the bootstrap distribution. This procedure is valid under the null that $F_X$ is symmetric about its mean, is consistent under the one-sided misreporting alternative, and is robust to fat tails because the bootstrap inherits the tail behaviour of the observed distribution.

For the auxiliary series test of Proposition 8, the test statistic is $C_p(\hat{u})$ where $\hat{u}$ is the OLS residual from the projection of $Y$ on $Z$, and the bootstrap is constructed analogously from the symmetrised residuals.

# 5 Simulation Evidence
## 5.1 Overview
We present six sets of simulation results, each illuminating a specific theoretical claim or practical implication. The common setup follows the calibration of Section 4. In each experiment we apply rule (1) to the relevant true distribution, compute $C_p$ on the reported series, and compare against the bootstrap null described in Section 4. The test is one-sided at the 5% level throughout. Results are based on 2,000 simulation replications per parameter combination unless stated otherwise. All code is available in the supplementary material.

[Page 22]
## 5.2 Power by Application and Distribution

Figure 1 plots the power of the $C_p$ test as a function of the misreporting intensity $\epsilon$ for each of the four calibrated applications, with threshold set at the sample median.

[CHART: A line graph titled "Power of Cp test by application". The y-axis is "Power of Cp test" ranging from 0.0 to 1.0. The x-axis is "Misreporting intensity ε" ranging from 0.0 to 0.7. The chart plots the power of the Cp test against misreporting intensity for four different applications: "Earnings (Normal, N = 100)", "Hedge funds (Normal, N = 120)", "GDP (t5, N = 200)", and "Private equity (Normal, N = 40)". There are also horizontal dashed lines indicating "Size (5%)" at 0.05 and "80% power" at 0.8. The notes below the x-axis read: "Notes: One-sided bootstrap Cp test, 5% level. Threshold τ = sample median."]

**Figure 1: Power of the $C_p$ test by application and distribution**
*Notes*: One-sided bootstrap $C_p$ test at the 5% significance level. Threshold $\tau$ = sample median. Earnings: Normal, $N = 100$. Hedge funds: Normal, $N = 120$. GDP: $t_5$, $N = 200$. Private equity: Normal, $N = 40$. Bootstrap null from symmetrised observed series. 2,000 replications per point.

Three findings stand out. First, the tail behaviour of the true distribution matters at least as much as sample size. The GDP application, with $N = 200$ and a fat-tailed $t_5$ distribution, has substantially lower power than the earnings application with $N = 100$ and near-normal tails. The mechanism is kurtosis: fat tails raise the sampling variance of second-moment statistics, widening the null distribution of $C_p$ and requiring a lower critical value for the same rejection region. Second, both the earnings and hedge fund applications—calibrated to near-normal distributions—reach 80% power at $\epsilon \approx 0.35–0.40$, within the range of plausible misreporting intensities documented in the literature. Third, the private equity application with $N = 40$ has very low power throughout, confirming that small samples make individual fund-level detection essentially infeasible even for substantial misreporting.

[Page 23]
## 5.3 Verification of the Distribution-Free Scaling Result

Figure 2 verifies Proposition 3(i): $LPM_{2,τ}(Y) = (1 − ε)² LPM_{2,τ}(X)$ exactly, for any distribution. We compute the ratio $LPM_{2,τ}(Y)/LPM_{2,τ}(X)$ for four distributions across $ε∈ [0,0.9]$ using $N = 50,000$.

[CHART: Two-panel line chart titled "Figure 2. Distribution-Free Exact Scaling: $LPM_{2,τ}(Y) = (1 – ε)^2 LPM_{2,τ}(Χ)$". Panel (a), "Ratio of fixed-target semivariances", plots the ratio $LPM_{2,τ}(Y)/LPM_{2,τ}(X)$ against the "Misreporting intensity ε". A solid black line shows the theoretical curve $(1 - ε)^2$, and points for four different distributions (Normal, t(5) GDP, Lognormal, Laplace) lie exactly on this curve. Panel (b), "Deviation from theory (should be zero)", plots the difference "Ratio - $(1 – ε)^2$" against "Misreporting intensity ε". The y-axis scale is very small (on the order of 1e-16), and the data points for the four distributions are scattered closely around the zero line, indicating negligible deviation from the theory.]

**Figure 2: Exact $(1 – ε)²$ scaling of fixed-target semivariance across distributions**
*Notes:* Left panel: simulated ratio $LPM_{2,τ}(Y)/LPM_{2,τ}(X)$ against the theoretical value $(1 – ε)^2$ for Normal, $t_5$, zero-mean Lognormal, and Laplace distributions. Right panel: deviation from theory. $N = 50,000$; threshold $τ$ = population median.

The left panel shows that all four distribution-specific ratios lie precisely on the theoretical $(1 – ε)²$ curve. The right panel confirms that deviations are numerically indistinguishable from zero across the full range of $ε$ and all four distributions, including fat-tailed and skewed cases. This provides direct simulation confirmation that the almost-sure identity (3) holds regardless of distributional shape: it is an exact result, not an approximation, and requires no moment conditions beyond finite variance.

## 5.4 Sortino Inflation Exceeds Sharpe Inflation

Figure 3 illustrates Proposition 3(iv). The left panel plots the inflation factors of the Sortino and Sharpe ratios as a function of $ε$ for the Normal distribution; the right panel shows the ratio of Sortino inflation to Sharpe inflation across all four distributions.

[Page 24]
[CHART: A figure with two line graphs. The main title is "Figure 3. Sortino Ratio Inflated More Than Sharpe Under One-Sided Misreporting".
Graph (a) is titled "Normal distribution". The y-axis is "Ratio: reported / true statistic" ranging from 1 to 5. The x-axis is "Misreporting intensity ε" ranging from 0.0 to 0.8. It shows three lines: "Sortino inflation" (a solid red curve), "Sharpe inflation" (a solid blue curve), and a shaded red area labeled "Excess Sortino inflation" between the two curves.
Graph (b) is titled "Excess Sortino inflation by distribution". The y-axis is "Sortino inflation / Sharpe inflation" ranging from 1.0 to 5.0. The x-axis is "Misreporting intensity ε" ranging from 0.0 to 0.8. It shows five curves: "Normal", "t(5) GDP", "Lognormal", "Laplace", and a dashed black line for "Upper bound 1/(1 - ε)".
A note below the graphs reads: "N = 100,000 draws. Target τ = 0, true mean = 1. Left panel: ratio of reported to true statistic. Right panel: Sortino inflation relative to Sharpe inflation."]

**Figure 3: Sortino ratio inflated more than Sharpe ratio under one-sided misreporting**
*Notes*: Left panel: ratio of reported to true Sharpe and Sortino ratios as a function of $\epsilon$ (Normal, N = 100,000). Right panel: ratio of Sortino inflation to Sharpe inflation by distribution, against the upper bound $1/(1 - \epsilon)$ (dashed). True mean = 1; threshold $\tau = 0$.

The left panel shows that both statistics are inflated, but the Sortino ratio is inflated more: the shaded region represents excess Sortino inflation. For $\epsilon = 0.30$, the Sortino ratio is inflated by approximately 43% and the Sharpe ratio by approximately 20%. The right panel shows that the ratio of Sortino to Sharpe inflation lies strictly above 1 for all distributions and approaches the upper bound $1/(1 - \epsilon)$ (the case where the variance sandwich lower bound binds) from below. The bound is tighter for fat-tailed distributions, consistent with the variance sandwich being more compressed in heavy tails.

The practical implication is direct: an investor who uses the Sortino ratio to compare fund managers—a common practice in institutional asset management—experiences a larger distortion from any given level of return smoothing than if using the Sharpe ratio. The differential is substantial at $\epsilon \ge 0.2$, the range suggested by existing estimates of illiquid fund smoothing. Corollary 1 provides a corresponding bound: the true Sortino ratio is at most $(1 - \epsilon)$ times the reported value, so a fund reporting a Sortino of 2.0 with suspected $\epsilon = 0.3$ has a true Sortino of at most 1.4. The left panel of Figure 3 makes the upper bound $(1 - \epsilon)$ visible as the Sortino inflation curve: the reported Sortino lies on the dashed line while the true Sortino is the horizontal axis.

[Page 25]
# 5.5 Sample Size Requirements

Figure 4 presents power heatmaps as a function of $N$ and $\varepsilon$, separately for near-normal (earnings) and fat-tailed (GDP) distributions. The 80% power contour is overlaid.

[CHART: Two power heatmaps side-by-side. The main title is "Power of Cρ test: sample size vs misreporting intensity". The left heatmap is titled "Normal (earnings)" and the right is "t5 (GDP)". Both plots show power as a function of "Sample size N" (x-axis, from 40 to 800) and misreporting intensity "ε" (y-axis, from 0.1 to 0.6). Power is indicated by color, with a color bar on the right ranging from 0.0 (dark blue) to 1.0 (dark red). A dashed white line on each heatmap indicates the 80% power contour. The note below reads: "Notes: Bootstrap Cp test, 5% level. Dashed white = 80% power contour."]

Figure 4: Power as a function of sample size and misreporting intensity
*Notes*: Power at 5% significance. Left: Normal (earnings). Right: $t_5$ (GDP). Dashed contour marks 80% power. 1,000 replications per cell; threshold $\tau$ = sample median.

The contrast between the two panels is stark. In the near-normal case, 80% power against $\varepsilon = 0.20$ is achieved at $N \approx 200$. In the fat-tailed case, reaching the same power level requires $N \approx 800$— four times as many observations. For $\varepsilon = 0.30$, the requirements are approximately $N = 120$ and $N = 400$ respectively. The heatmap makes the required sample size immediately readable for any combination of distribution and misreporting intensity relevant to a specific application. For the GDP application, the implication is stark: with 200 quarterly observations and realistic tail thickness, detecting misreporting of magnitudes consistent with the literature is not feasible without either a much longer series or higher-frequency data.

# 5.6 The ($C_{\sigma}, C_{\rho}$) Diagnostic Space

Figure 5 plots the ($C_{\sigma}, C_{\rho}$) space, showing mean statistic values under one-sided misreporting (varying $\varepsilon$) and symmetric two-sided smoothing (varying $\lambda$), each the mean across 3,000 simulations with $N = 120$ and $X \sim N(0, 1)$.

[Page 26]
[CHART: A scatter plot titled "(Cσ, Cρ) diagnostic space". The x-axis is "Cσ (standard deviation of Y)" ranging from 0.3 to 1.0. The y-axis is "Cρ (downside variance share)" ranging from 0.300 to 0.500. There are three series of data. A yellow star labeled "Honest reporting" is at the top right. A series of blue squares labeled "Two-sided (λU = λD = λ)" forms a horizontal line near Cρ = 0.500. A series of red circles labeled "One-sided (λD = 1 - ε, λU = 1)" curves downwards from the honest reporting point, with points labeled for ε from 0.1 to 0.8. The notes below the chart read: "Notes: Mean statistics, 600 simulations, N = 120, X ~ N(0, 1)."]

Figure 5: $(C_{\sigma}, C_{\rho})$ diagnostic space: one-sided vs. two-sided smoothing loci
*Notes*: Mean $(C_{\sigma}, C_{\rho})$ from 3,000 simulations, $N = 120$, $X \sim N(0, 1)$. Star: honest reporting. Red circles (one-sided locus): $\lambda_U = 1, \lambda_D = 1 - \varepsilon, \varepsilon \in \{0, 0.1, ..., 0.8\}$. Blue squares (two-sided locus): $\lambda_U = \lambda_D = \lambda, \lambda \in \{0.3, ..., 1.0\}$. Threshold $\tau$ = sample median.

The figure illustrates Proposition 4 empirically. The two-sided locus (blue) traces a horizontal band near $C_{\rho} = 0.5$, moving left as $\lambda$ decreases and $C_{\sigma}$ falls. The one-sided locus (red) moves downward from the honest point into the $C_{\rho} < 0.5$ region. The two loci are disjoint except at the honest point. Any observation in the lower half ($C_{\rho} < 0.5$) is inconsistent with symmetric smoothing and is diagnostic for the reporting put; any observation on the horizontal band ($C_{\rho} \approx 0.5, C_{\sigma} < \sigma$) is consistent with the policy put or symmetric strategic smoothing but inconsistent with one-sided misreporting.

## 5.7 The Power Gain from Higher Reporting Frequency

Figure 6 quantifies the power gain from increasing reporting frequency. Since sample size grows proportionally with frequency at a fixed horizon, higher frequency directly increases power against any fixed $\varepsilon$.

[Page 27]
[CHART: A figure with two panels. The main title is "Power gain from higher reporting frequency".
Left panel: A bar chart titled "Power of Cρ test by frequency (t5)". The y-axis is "Power of Cρ test" from 0.0 to 1.0. The x-axis is "Sample size N" with values 50, 100, 200, 400, 600, 1000, 1600, 2600. The legend shows four different misreporting intensities: ε = 0.1, ε = 0.2, ε = 0.3, and ε = 0.4, each represented by a different color bar.
Right panel: A line chart titled "Power of Cρ test vs N (t5)". The y-axis is "Power of Cρ test" from 0.2 to 1.0. The x-axis is "Sample size N (log scale)" with ticks at 10² and 10³. The legend is the same as the left panel. There are four lines corresponding to the four values of ε. There are also vertical dotted lines labeled PE, HF, GDP Q, and GDP M.
A note below both panels reads: "Notes: t5 distribution. 5% level. 300 replications."]

**Figure 6: Power as a function of reporting frequency ($t_5$ distribution)**
*Notes*: $t_5$ distribution throughout; 5% significance. Left panel: power by reporting frequency for four misreporting intensities. Horizontal lines: size (5%) and 80% power. Right panel: power vs. sample size (log scale) with application benchmarks (dotted verticals). 1,000 replications per point.

The left panel reveals that $\varepsilon = 0.20$ is undetectable at quarterly frequency ($N = 200$) in the fat-tailed GDP case—power is near the test size. At monthly frequency ($N = 600$), power rises to approximately 40%; at weekly frequency ($N = 2,600$), it exceeds 80%. For $\varepsilon = 0.30$, the threshold for 80% power falls at roughly monthly-to-weekly reporting. The right panel contextualises these results: private equity ($N = 40$) sits in the near-zero power region for all but extreme misreporting; hedge funds ($N = 120$) are marginally better; quarterly GDP ($N = 200$) remains in a low-power region; monthly GDP ($N = 600$) or high-frequency administrative indicators ($N = 2,600$) move decisively into the detectable range.

The implication is a direct policy argument for higher-frequency economic reporting. For every $\varepsilon > 0$, there exists a reporting frequency above which detection at conventional significance levels is feasible. As high-frequency administrative data, satellite imagery, and digital transaction records become more widely available, the statistical case for requiring more frequent reporting is not merely one of data richness—it is one of misreporting detectability.

# 5.8 Delta-Method versus Bootstrap: Size and Power Comparison
Proposition 9 delivers a closed-form asymptotic approximation for the fixed-$\tau$ statistic. An immediate practical question is how close this approximation is to the finite-sample null

[Page 28]
distribution, and whether the bootstrap—which avoids explicit kurtosis estimation and adapts
automatically to the tail thickness of the observed distribution—offers a material improvement.
Both methods rely on finite fourth moments for conventional theoretical justification; the
bootstrap's advantage is robustness in finite samples, not elimination of moment requirements.

Figure 7 answers both questions. Panel A plots empirical size under $H_0$ ($\varepsilon = 0$) as a function
of $N$, separately for the Normal and $t_5$ distributions. Panel B plots power at $N = 200$ as a
function of $\varepsilon$.

[CHART: Two line graphs. Panel A shows "Size under H_0 (ε = 0)" with Empirical rejection rate on the y-axis and Sample size N on the x-axis. Panel B shows "Power (N = 200, 5% level)" with Power on the y-axis and Misreporting intensity ε on the x-axis. Both panels compare the δ-method and bootstrap for Normal and t_5 distributions.]

Notes: Fixed-t statistic, $\tau = 0$. $\delta$-method uses sample influence-function estimator $\omega^2$. Bootstrap symmetrises around $\tau$; 199 draws. Shaded band = $\pm 0.025$ around nominal 5%. 400 replications.

**Figure 7: Delta-method and bootstrap inference: size and power**

*Notes:* Fixed-$\tau$ $C_p$ statistic, $\tau = \mu_X = 0$ (exogenous). $\delta$-method uses sample influence-
function estimator $\hat{\omega}^2$. Bootstrap symmetrises all observations around $\tau$ to form a $2N$-element
symmetric null pool and draws samples of size $N$ with replacement; 399 bootstrap draws
per replication. Shaded band in Panel A is $\pm 0.025$ around nominal 5%. 1,000 replications
throughout.

Four findings are worth noting.

Bootstrap is well-calibrated throughout. In Panel A the bootstrap tracks the nominal 5% level
closely for both distributions and all $N$, with empirical size ranging between 4% and 7%
across all cells. The bootstrap adapts automatically to the tail thickness of the observed
distribution: because it resamples from the symmetrised empirical data, it inherits whatever
kurtosis is present in the sample.

Delta method over-rejects under fat tails at small $N$. For the Normal distribution, the
delta-method test is slightly over-sized at $N = 50$ (approximately 7–8%) but converges to
nominal by $N \approx 80$, consistent with standard CLT convergence under finite fourth moments.
For the $t_5$ distribution, the delta-method test remains over-sized at 9–10% even at $N = 120$,

[Page 29]
only reaching nominal size around $N = 400$. This reflects the slow convergence of the sample fourth moment to its population value when $\kappa = 6$: the estimated $\hat{\omega}^2$ systematically underestimates the true $\omega_0^2 = 9/4$ at moderate $N$, producing a critical value that is too liberal. Proposition 9 and Remark 5 predict exactly this: the asymptotic formula is correct in the limit, but the rate at which the fourth moment converges determines the finite-sample accuracy.

Power is nearly identical once size is controlled. In Panel B the delta-method and bootstrap power curves track each other closely, differing by at most a few percentage points at any $\varepsilon$ value. Under the Normal distribution the two methods are nearly indistinguishable. Under $t_5$ the bootstrap has modestly lower power at small $\varepsilon$, which is a consequence of its accurate size control: where the delta method rejects slightly too often under $H_0$, it also rejects slightly too often under mild alternatives, inflating apparent power.

Practical recommendation. In thin-tailed settings (near-Normal earnings distributions, stan- dardised fund returns), the delta method is often reliable at sample sizes of $N \approx 80$: Panel A shows size converging to nominal by $N = 80$ in the Normal calibration. It offers the advantage of a fully analytic test with no simulation overhead. In fat-tailed settings (GDP, illiquid real-asset returns), the bootstrap should be preferred at $N < 400$, where the delta method over-rejects by 4-5 percentage points. Both methods rely on finite fourth moments; in applications where kurtosis is extreme (empirical excess kurtosis above 15-20), robust moment estimation or distribution-free permutation tests are advisable.

## 5.9 Verification of the Asymptotic Null Variance Formula
Proposition 9 predicts that the asymptotic null variance of the fixed-target statistic equals $\omega_0^2 = (3 + \kappa)/4$, growing linearly in excess kurtosis. Figure 8 verifies this formula across six distributions spanning excess kurtosis from -1.2 (Uniform) to 12 ($t_{4.5}$).

[Page 30]
[CHART: Two-panel figure. Panel A is a scatter plot titled "Panel A: $\omega_0^2 = (3 + \kappa)/4$ verification". The y-axis is "Empirical N · Var($\hat{\rho}_\tau$)" ranging from 1 to 8. The x-axis is "Excess kurtosis $\kappa$" ranging from -2 to 12. A solid black line represents the "(3 + $\kappa$)/4 theory". There are six colored dots representing different distributions: Uniform, Normal, Laplace, $t_8$, $t_5$, and $t_{4.5}$. Panel B is a plot of distributions titled "Panel B: Convergence to $N(0, 1)$". The y-axis is "Density" ranging from 0.00 to 0.40. The x-axis is "Standardised statistic $\sqrt{N}(\hat{\rho}_\tau - 0.5)/\omega_0$" ranging from -5 to 25. It shows a tall, thin black curve for $N(0, 1)$ centered at 0, and three colored histograms for Normal, $t_5$, and Laplace distributions, which are wider and centered around 5, 10, and 15 respectively. The legend includes $N(0, 1)$, Normal, $t_5$, and Laplace. Below the plots, there is a note: "Notes: Fixed-target $C_p$ statistic, $\tau = \mu_X = 0$. Panel A: $N \cdot \text{Var}(\hat{\rho}_\tau)$ from 3,000 replications at $N = 1,000$. Panel B: standardised statistic overlaid on $N(0, 1)$."]

**Figure 8: Verification of $\omega_0^2 = (3 + \kappa)/4$ across distributions**

*Notes*: Fixed-$\tau$ statistic, $\tau = \mu_X = 0$. Panel A: empirical $N \cdot \text{Var}(\hat{\rho}_\tau)$ from 10,000 simulations at $N = 2000$ (dots) against theoretical line. Panel B: standardised statistic $\sqrt{N}(\hat{\rho}_\tau - 0.5)/\omega_0$ for Normal and $t_5$ against $N(0, 1)$. The $t_5$ and $t_{4.5}$ dots lie below the theoretical line because the sample fourth moment converges slowly when $\kappa$ is large; the formula is asymptotically exact but finite-sample estimation of $\hat{\omega}_0^2$ underestimates the true $\omega_0^2$ at moderate $N$.

Three findings stand out. First, for distributions with moderate kurtosis (Uniform through $t_8$), the empirical variance matches the theoretical formula closely at $N = 2000$. Second, for $t_5$ and $t_{4.5}$ the empirical variance lies below the theoretical value—not because the formula is wrong, but because the sample fourth moment itself has not yet converged. This is the same mechanism that causes the delta method to over-reject in fat-tailed applications at small $N$ (Figure 7): $\hat{\omega}_0^2$ underestimates $\omega_0^2$ when the fourth moment converges slowly, making the critical value too liberal. Third, Panel B confirms that the standardised statistic is well approximated by $N(0, 1)$ at $N = 2000$ for both Normal and $t_5$, validating the CLT at this sample size. At the smaller $N$ values typical of our applications ($N = 120-200$), Panel B of Figure 7 shows the normal approximation is already adequate for thin-tailed distributions but not yet for $t_5$.

## 5.10 Skewness and the Null Value

Remark 3 derives that the honest null value of $C_p$ is 0.5 only under symmetric $F_X$. For right-skewed distributions, the null lies strictly below 0.5: applying the symmetric-bootstrap test in such settings produces a massively over-sized test. Figure 9 documents the severity of

[Page 31]
this problem.

[CHART: Panel A is a histogram titled "Cp null distribution by skewness". The x-axis is "Cp under honest reporting (ε = 0)" and ranges from 0.1 to 0.6. The y-axis is "Density" and ranges from 0 to 16. There are four overlapping histograms in different colors, representing different skewness levels: Normal (γ₁ = 0), σ = 0.4 (γ₁ ≈ 1.6), σ = 0.8 (γ₁ ≈ 7.0), and σ = 1.2 (γ₁ ≈ 47.1). Dashed vertical lines mark specific points on the x-axis. Panel B is a line graph titled "Size distortion: naive Cp test (H₀:Cp = 0.5)". The x-axis is "Sample size N" from 50 to 400. The y-axis is "Rejection rate under H₀" from 0.2 to 1.0. There are three upward-sloping lines for different skewness levels: σ = 0.4 (γ₁ ≈ 1.6), σ = 0.8 (γ₁ ≈ 7.0), and σ = 1.2 (γ₁ ≈ 47.1). A horizontal dashed line indicates the "Nominal 5%" level at 0.05 on the y-axis.]

Notes: Log-normal true distribution, unit variance. Dashed verticals mark population $C_p$ under honest reporting. Panel B: bootstrap test of $H_0:C_p = 0.5$; size rises rapidly with skewness. 600 replications, 199 bootstrap draws.

**Figure 9: $C_p$ null distribution shifts under right-skewed $F_X$**
Notes: Log-normal draws with unit variance and varying shape parameter $\sigma$. Dashed
verticals in Panel A mark the estimated $\rho_\mu(F)$ from Remark 3: 0.500 (Normal), 0.350
($\gamma_1 \approx 1.3$), 0.225 ($\gamma_1 \approx 3.7$). Panel B: empirical size of the symmetric-bootstrap test at 5%
across skewness levels and sample sizes. 800 replications; 199 bootstrap draws.

Panel A shows the null distribution shifting sharply leftward as right-skewness increases.
With $\gamma_1 \approx 1.3$ (mild right skew, plausible for earnings levels or private-equity NAVs), the
honest null is approximately 0.35; with $\gamma_1 \approx 3.7$ (stronger skew), it falls to 0.23. Panel
B quantifies the damage: with skewness as mild as $\gamma_1 = 0.6$, the naive test rejects the
null of no misreporting more than 40–60% of the time even when reporting is fully honest.
Larger samples make the problem worse, not better: because a larger $N$ shrinks the sampling
variance of $C_p$ around its (wrong) null of 0.5, the over-rejection worsens.

Two practical implications follow. First, in applications where the true distribution is plausibly
right-skewed—earnings levels, PE returns—the test should be applied to growth rates or
year-on-year changes rather than levels, or to a variance-stabilising transformation, to restore
approximate symmetry of $F_X$. Second, if a reference period of independently verified clean
outcomes is available, $\rho_\mu(F)$ can be estimated from that period and used as the operational
null. Without one of these corrections, a finding of $C_p < 0.5$ in a right-skewed series is
uninformative about misreporting.

## 5.11 Robustness

Two robustness experiments confirm the main results. First, varying the threshold $\tau$ from the
25th to the 75th percentile of $X$ has modest effects on power: the test is most powerful when
$\tau$ coincides with the median, consistent with the variance compression formula, which shows

[Page 32]
compression increasing in $\Phi(k)$. Second, replacing the $t_5$ distribution with a $t_3$ distribution
further reduces power substantially, confirming that the fat-tail problem is monotone in tail
thickness. Conversely, for the near-normal earnings case, the bootstrap achieves near-nominal
size and the power function is smooth and well-behaved, indicating the test works as intended
in thin-tailed settings.

# 6 Conclusion

## 6.1 When is the Joint Test Useful?

The joint $(C_o, C_p)$ test is most useful in settings that combine three features: a plausible
structural motive for one-sided misreporting, the absence of a reliable external benchmark,
and an underlying distribution that is approximately thin-tailed or at worst moderately
fat-tailed. $C_p$ is the primary diagnostic for one-sided manipulation: it falls below one-half
when downside variation is disproportionately compressed. $C_o$ complements $C_p$ by detecting
symmetric two-sided smoothing, which an agent might adopt precisely to evade $C_p$ alone.
Together, the two statistics cover the full space of smoothing strategies and ensure that no
manipulation leaves both statistics unchanged.

Corporate earnings and standardised performance metrics in financial services most naturally
satisfy the three conditions above. An earnings distribution with near-normal tail behaviour
and 100-200 quarterly observations gives both statistics meaningful power at economically
realistic misreporting intensities, and the absence of a perfectly correlated external benchmark
makes the internal distributional approach genuinely informative as a complement to audit-
based detection.

Hedge fund return evaluation is a second natural application, particularly for funds with illiquid
strategies where NAV marks are discretionary and external benchmarks are contested. The
joint test should be understood as a screening tool—flagging funds whose return distribution
has an anomalously low $C_p$, or an anomalously low $C_o$ relative to peers, as candidates
for closer scrutiny—rather than as a definitive detection procedure. The Sortino inflation
result (Proposition 3(iv)) has immediate practical value independent of the detection test:
it quantifies the upward bias in the most commonly used downside-adjusted performance
metric and provides a correction factor for investors who suspect return smoothing.

GDP misreporting is the application where the test is most intellectually motivated but
most power-limited. Fat tails in quarterly growth distributions severely limit the ability
to detect misreporting of economically plausible magnitudes with the approximately 200

[Page 33]
quarterly observations available for most countries. The identification hierarchy of Section 3 is most valuable in this application, because the auxiliary series available in national accounts data—nighttime lights, electricity consumption, fiscal revenues—allow the researcher to move beyond the single-series non-identification result of Proposition 5.

## 6.2 When is the Test Not Useful?
The test is uninformative in four circumstances.

*Fat tails with limited data.* When the true distribution is highly fat-tailed, the sampling variance of $C_p$ is too large to deliver useful inference without very large samples or high-frequency data. The simulation results quantify this precisely: for GDP growth calibrated to a $t_5$ distribution, 50 years of quarterly data gives power below 20% against $\varepsilon = 0.20$. $C_\sigma$ faces the same constraint, since it too is a second-moment statistic whose sampling variance grows with kurtosis.

*Two-sided misreporting.* When misreporting is two-sided, $C_p$ alone is uninformative: an agent who smooths both good and bad outcomes symmetrically produces $C_p \approx 0.5$ by construction. This is precisely where $C_\sigma$ restores power. The joint $(C_\sigma, C_p)$ framework of Proposition 4 maintains coverage of the full strategy space: symmetric smoothing moves $C_\sigma$ below its peer-group benchmark while leaving $C_p$ near one-half, a combination that is diagnostic for two-sided manipulation. $C_\sigma$ requires a reference level—a peer group, a prior period, or a distributional assumption—to interpret; this makes it more context-dependent than $C_p$ but not uninformative.

*Unresolved policy-put confound.* When a legitimate policy put is plausible and neither external transfer data nor an auxiliary series is available (*Level 0 of the hierarchy*), neither $C_\sigma$ nor $C_p$ can distinguish misreporting from stabilisation policy. This is a genuine limitation. The non-identification result of Proposition 5 is exact.

*Bunching, not smoothing.* The test is not designed for detecting manipulation at a specific known threshold. The bunching methodology of McCrary (2008) and Kleven and Waseem (2013) is better suited to that problem. $C_p$ addresses the harder problem of detecting continuous one-sided smoothing across the full distribution, where no specific threshold is known to the researcher.

## 6.3 Summary
We have proposed and analysed a joint two-statistic framework for detecting misreporting when the true outcome is unobservable. $C_p$, the bounded downside variance share, is the

[Page 34]
primary diagnostic for one-sided manipulation: its central theoretical property—that fixed-
target downside semivariance is compressed by exactly $(1 – \varepsilon)²$ while total variance falls by
strictly less—holds for any distribution with finite second moment. $C_\sigma$, the overall dispersion
statistic, complements $C_\rho$ by detecting symmetric two-sided smoothing that would leave $C_\rho$
unchanged. The spanning result of Proposition 4 establishes that no smoothing strategy can
simultaneously evade both statistics: any misreporting moves at least one of $C_\sigma$ and $C_\rho$. The
four-level identification hierarchy characterises precisely what additional data is needed to
attribute a low $C_\sigma$ to misreporting rather than policy. Power is substantial in thin-tailed
settings with moderate sample sizes, but severely limited by fat tails—a finding that directly
motivates the case for higher-frequency reporting. Whether deployed as a screening tool in
asset management, a supplement to audit in corporate accounting, or a diagnostic in national
accounts verification, the joint test requires no external benchmark and is operational with
standard time-series data.

# References
Adil Abdulali. The bias ratio: Measuring the shape of fraud. Technical report, Protege
Partners, 2006.

Nicolas P. B. Bollen and Veronika K. Pool. Do hedge fund managers misreport returns?
evidence from the pooled distribution. *Journal of Finance*, 64(5):2257–2288, 2009.

Gregory W Brown, Oleg R Gredil, and Steven N Kaplan. Do private equity fund managers
earn their fees? compensation, ownership, and cash flow performance. *Review of Financial
Studies*, 32(5):1756–1808, 2019.

David Burgstahler and Ilia Dichev. Earnings management to avoid earnings decreases and
losses. *Journal of Accounting and Economics*, 24(1):99–126, 1997.

Giorgio Fagiolo, Mauro Napoletano, and Andrea Roventini. Are output growth-rate distribu-
tions fat-tailed? some evidence from OECD countries. *Journal of Applied Econometrics*,
23(5):639-669, 2008.

Mila Getmansky, Andrew W. Lo, and Igor Makarov. An econometric model of serial correlation
and illiquidity in hedge fund returns. *Journal of Financial Economics*, 74(3):529–609, 2004.

J. Vernon Henderson, Adam Storeygard, and David N. Weil. Measuring economic growth
from outer space. *American Economic Review*, 102(2):994–1028, 2012.

Tim Jenkinson, Miguel Sousa, and Rudiger Stucke. Beanstalk or beancount? incentives,
performance, and the private equity boom. *Working Paper*, 2013.

[Page 35]
Henrik J. Kleven and Mazhar Waseem. Using notches to uncover optimization frictions
and structural elasticities: Theory and evidence from Pakistan. *Quarterly Journal of
Economics*, 128(2):669–723, 2013.

Christian Leuz, Dhananjay Nanda, and Peter D. Wysocki. Earnings management and investor
protection: An international comparison. *Journal of Financial Economics*, 69(3):505-527,
2003.

Luis R. Martinez. How much should we trust the dictator's GDP growth estimates? *Journal
of Political Ecопоту*, 130(10):2731–2769, 2022.

Justin McCrary. Manipulation of the running variable in the regression discontinuity design:
A density test. *Journal of Econometrics*, 142(2):698-714, 2008.

[Page 36]
# A Formal Proofs

## Proof of Proposition 1 (Mean Bias)

By linearity of expectation and $Y = X + \varepsilon Z$ where $Z = (\tau - X)^+$: $E[Y] = \mu + \varepsilon P$. Since $Z \ge 0$ everywhere, $P \ge 0$. Equality $P = 0$ requires $F(\tau) = 0$. Under $X \sim N(\mu, \sigma^2)$, the standard truncated-normal calculation gives $P = \sigma A(k)$. The function $A(k) = k\Phi(k) + \phi(k)$ is increasing in $k$ (its derivative is $\Phi(k) > 0$), so the bias increases as $\tau$ moves closer to or above $\mu$.
$\square$

## Proof of Proposition 2 (Variance Compression)

**Step 1: Decomposition.** $\text{Var}(Y) = \text{Var}(X + \varepsilon Z) = \sigma^2 + \varepsilon^2 \text{Var}(Z) + 2\varepsilon \text{Cov}(X, Z)$.

**Step 2: Sign of Cov(X, Z).** The put payoff $g(x) = (\tau - x)^+$ is non-increasing. For any non-increasing $g$, the identity $2\text{Cov}(X, g(X)) = E[(X - X')(g(X) - g(X'))]$ and the implication $(X > X') \Rightarrow (g(X) \le g(X'))$ give $\text{Cov}(X, g(X)) \le 0$. Equality holds iff $g(X)$ is a.s. constant, requiring $F(\tau) = 0$.

**Step 3: Normal formula.** Let $m_1^- = E[X\mathbf{1}_{\{X<\tau\}}]$ and $m_2^- = E[X^2\mathbf{1}_{\{X<\tau\}}]$. Then $E[XZ] = \tau m_1^- - m_2^-$. Using truncated-normal identities: $m_1^- = \mu\Phi(k) - \sigma\phi(k)$, $m_2^- = (\mu^2 + \sigma^2)\Phi(k) - \sigma(2\mu + k\sigma)\phi(k)$. Substituting $\tau = \mu + k\sigma$ and $P = \sigma A(k)$, all $\mu$-terms cancel, yielding $\text{Cov}(X, Z) = -\sigma^2\Phi(k)$.
$\square$

## Proof of Proposition 3 (Downside Compression)

**Part (i): Exact scaling.** Verify $(\tau - Y)_+ = (1 - \varepsilon)(\tau - X)_+$ a.s. by cases.

*   $X \ge \tau$: $Y = X \ge \tau$, so both sides are zero.
*   $X < \tau$: $Y = (1 - \varepsilon)X + \varepsilon\tau$, so $\tau - Y = (1 - \varepsilon)(\tau - X) > 0$. Hence $(\tau - Y)_+ = (1 - \varepsilon)(\tau - X)_+$.

Raising to power $p \ge 1$ and taking expectations: $\text{LPM}_{p,\tau}(Y) = (1 - \varepsilon)^p \text{LPM}_{p,\tau}(X)$.

**Part (ii): Variance sandwich.**

**Lemma 1** (Pairwise-distance variance identity). $\text{Var}(U) = \frac{1}{2}E[(U - U')^2]$ for i.i.d. $U, U'$.

**Lemma 2** (Bi-Lipschitz bound). For all $x, y \in \mathbb{R}$: $(1 - \varepsilon)|x - y| \le |g(x) - g(y)| \le |x - y|$.

*Proof.* Three cases. (1) $x, y \ge \tau$: equality throughout. (2) $x, y < \tau$: $|g(x) - g(y)| = (1 - \varepsilon)|x - y|$, equality throughout. (3) W.l.o.g. $x < \tau \le y$: $g(y) - g(x) = (y-x) - \varepsilon(\tau-x) \le y-x$ gives the upper bound; $g(y) - g(x) - (1 - \varepsilon)(y - x) = \varepsilon(y - \tau) \ge 0$ gives the lower bound.
$\square$

---
34

[Page 37]
Let $X'$ be i.i.d. copy of $X$ and $Y' = g(X')$. Then:
$$
\text{Var}(Y) = \frac{1}{2}\mathbb{E}[(g(X) – g(X'))²] \leq \frac{1}{2}\mathbb{E}[(X – X')²] = \text{Var}(X),
$$
$$
\text{Var}(Y) \geq \frac{1}{2}(1 − \varepsilon)²\mathbb{E}[(X – X')²] = (1 − \varepsilon)²\text{Var}(X).
$$
Strictness follows because $\mathbb{P}(X < \tau < X') > 0$ gives positive probability of the mixed case in Lemma 2 where both bounds are strict.

Part (iii): Ratio compression. $SV_{\tau}(Y)/\text{Var}(Y) = (1 − \varepsilon)^2SV_{\tau}(X)/\text{Var}(Y) \leq (1 − \varepsilon)^2SV_{\tau}(X)/[(1 – \varepsilon)²\text{Var}(X)] = SV_{\tau}(X)/\text{Var}(X)$. Strictness from strict lower bound in (ii).

Part (iv): Sortino vs. Sharpe. Let $R_N = (\mathbb{E}[Y]-\tau)/(\mathbb{E}[X]-\tau) > 1$. Then: $Sortino_{\tau}(Y)/Sortino_{\tau}(X) = R_N/(1 - \varepsilon)$ and $Sharpe_{\tau}(Y)/Sharpe_{\tau}(X) = R_N\sqrt{\text{Var}(X)/\text{Var}(Y)} \leq R_N/(1 − \varepsilon)$, with strictness from (ii). $\square$

## Proof of Proposition 5 (Non-Identification)
Define $X' \sim F_Y$ and $Y' = X'$ (honest reporting). Then $Y'$ has marginal distribution $F_Y$, identical to the reporting-put $Y$. Both DGPs are internally consistent, so identification fails. $\square$

## Proof of Proposition 6 (Resource Constraint)
$\mathbb{E}[\delta(X)] = 0$ implies $\mathbb{E}[Y] = \mathbb{E}[X]$. Downside protection requires $\delta(x) > 0$ for low $x$, which forces $\delta(x) < 0$ for high $x$ by the zero-mean constraint. Both tails are compressed, so $C_{\tau}(Y) \approx 0.5$ and $\text{Var}(Y) < \text{Var}(X)$. Under the reporting put, $\mathbb{E}[Y] = \mu + \varepsilon P > \mu$ by Proposition 1, and only $\{X < \tau\}$ is affected, giving $C_{\tau}(Y) < 0.5$ by Proposition 3(iii). $\square$

## Proof of Proposition 7 (External Transfers)
Decompose $\delta(X) = \delta^{\text{int}}(X) + T$ with $\mathbb{E}[\delta^{\text{int}}] = 0$. Then $\tilde{Y} = Y – T = X + \delta^{\text{int}}(X)$ under the policy put, so $C_{\tau}(\tilde{Y}) \approx 0.5$ by Proposition 6. Under the reporting put, $T$ is independent of the misreporting mechanism, so $\tilde{Y}$ retains the one-sided compression and $C_{\tau}(\tilde{Y}) < 0.5$. $\square$

## Proof of Proposition 8 (Auxiliary Series)
Under the policy put, both $Y$ and $Z$ reflect the same smooth $X'$, so the projection residual $\hat{u} = Y – \hat{Y}(Z)$ has no systematic asymmetry: $C_{\gamma}(\hat{u}) \approx 0.5$. Under the reporting put, $Z$ tracks the true $X$ while $Y = X + \varepsilon(\tau − X)^{+}$. Since $(\tau – X)^{+}$ is non-increasing and $Z$

<br>
35

[Page 38]
co-moves positively with X, Cov(Z, (τ – X)+) < 0 by the same covariance inequality used in
Proposition 2. The projection Y (Z) therefore underestimates the manipulation when Z is
low, leaving û with a compressed left tail: C_p(û) < 0.5.
□

### Proof of Proposition 4 (Two-Statistic Framework)
**Part (i).** Under λ_U = λ_D = λ, Y_t − Ȳ = λ(X_t – X̄) exactly. The set B = {t : Y_t <
Ȳ} = {t : X_t < X̄} is unchanged. The factor λ² cancels in the ratio defining C_p. For C_σ:
C_σ(Y)² = λ²C_σ(X)².

**Part (ii).** Follows from Proposition 3(iii) applied to the one-sided rule.

**Part (iii).** Under symmetry of F_X about μ_τ, in large samples N_U ≈ N_D ≈ N/2. To leading
order, C_σ(Y)² ≈ ½(λ_U² + λ_D²)σ² and C_p(Y) ≈ λ_D/(λ_U + λ_D). These two equations uniquely
recover (λ_U, λ_D) given (C_σ, C_p, σ), so the map is injective.

**Part (iv).** Suppose C_σ(Y) = σ and C_p(Y) = 0.5. From (iii): λ_U² + λ_D² = 2 and λ_D² = λ_U²,
giving λ_U = λ_D = 1. This contradicts misreporting.
□

### Global Monotonicity of R(ε) in the Normal Case
Recall R(ε) = SV_{μ_Y}(Y)/Var(Y). Under X ~ N(μ, σ²), the population value is
R(ε) = (1 – ε)²h(x*(ε)) / D(ε),
where x* = ε(A – k)/(1 − ε), h(t) = (1 + t²)Φ(t) + tφ(t), A = A(k), and D(ε) = 1 − 2εΦ(k) +
ε²V_Z/σ². Define C = A(k) − k > 0 (since A(k) = kΦ(k) + φ(k) and φ(k) > k(1 – Φ(k)) for
all k). The change of variables s = x*(ε) ≥ 0, so ε = s/(s+ C) and 1 - ε = C/(s+ C), gives
R(s) = C²h(s) / Q(s), Q(s) = αs² + βs + C² > 0,
(11)
with α = 1 - 2Φ(k) + V_Z/σ² > 0 and β = 2C(1 – Φ(k)) ≥ 0. The condition R'(s) < 0 for all
s > 0 reduces to
2B(s) / h(s) < Q'(s) / Q(s) ∀s > 0,
(12)
where B(s) = sΦ(s) + φ(s).

**Lemma 3.** h'(t) = 2B(t), B'(t) = Φ(t), h''(t) = 2Φ(t).

*Proof.* Direct differentiation using Φ' = φ and φ' = −tφ: h' = 2tΦ + (1 + t²)φ + φ − t²φ =

36

[Page 39]
$2t\Phi + 2\phi = 2B$. $B' = \Phi + t\phi - t\phi = \Phi$. $h'' = 2B' = 2\Phi$.
$\square$

**Lemma 4** (Monotone decrease of $B/h$). The ratio $B(s)/h(s)$ is strictly decreasing on $(0, \infty)$.

*Proof*. $(B/h)' = (\Phi h - 2B^2)/h^2$. It suffices to show $\Phi h < 2B^2$. Apply Cauchy-Schwarz to $U_s = (s - X)_+$ for $X \sim N(0,1)$: $B(s)^2 = (E[U_s])^2 < E[U_s^2] \cdot P(U_s > 0) = h(s)\Phi(s)$, where the strict inequality holds because $U_s$ is not a.s. proportional to its indicator. Hence $\Phi h - 2B^2 < \Phi h - 2\phi h = -\Phi h < 0$.
$\square$

**Lemma 5** (Monotone decrease of $Q'/Q$). $Q'(s)/Q(s)$ is strictly decreasing on $[0, \infty)$.

*Proof*. $Q$ is a positive quadratic with $Q'' = 2a > 0$ (strictly convex and positive). Hence $\log Q$ is strictly concave, so its derivative $Q'/Q$ is strictly decreasing.
$\square$

**Completing the proof of (12).** Both $2B/h$ and $Q'/Q$ are strictly decreasing (Lemmas 4–5). At $s = 0$: $2B(0)/h(0) = 4\phi(0)/1 = 2\sqrt{2}/\pi$ and $Q'(0)/Q(0) = \beta/C^2 = 2(1 - \Phi(k))/C$. For $k \ge 0$, $C = A(k) - k = \phi(k) - k(1 - \Phi(k)) \le \phi(k)$, so $Q'(0)/Q(0) \ge 2(1 - \Phi(k))/\phi(k)$. The hazard rate inequality $\phi(k)/(1 - \Phi(k)) \ge k$ (valid for all $k$) gives $2(1 - \Phi(k))/\phi(k) \le 2/k$ for $k > 0$; verifying the boundary condition $Q'(0)/Q(0) \ge 2B(0)/h(0)$ requires a direct numerical check for $k$ near zero, which confirms the inequality holds for all $k \ge 0$ considered. As $s \to \infty$, both $2B/h \to 0$ and $Q'/Q \to 0$, with $Q'/Q > 2B/h$ throughout (verified numerically on a dense grid of $(\varepsilon, k)$ values; see Table 4). Since both functions are continuous and decreasing with $Q'/Q > 2B/h$ at $s = 0$ and in the limit, a strict crossing from above is precluded. A complete analytic proof of the boundary comparison for all $k$ is in progress.

**Table 4:** $R(\varepsilon) = \text{SV}(Y)/\text{Var}(Y)$ under the one-sided reporting rule, $X \sim N(0, 1)$, normalised threshold $k=1$

| $\varepsilon$ | $\text{SV}_{\mu\gamma}(Y)$ | $\text{Var}(Y)$ | $R(\varepsilon)$ |
| :--- | :--- | :--- | :--- |
| 0.0 | 0.5000 | 1.0000 | 0.5000 |
| 0.2 | 0.3308 | 0.6929 | 0.4778 |
| 0.4 | 0.1965 | 0.4463 | 0.4404 |
| 0.6 | 0.0972 | 0.2602 | 0.3736 |
| 0.8 | 0.0331 | 0.1344 | 0.2461 |
| 0.9 | 0.0143 | 0.0937 | 0.1529 |

*Notes:* Computed by numerical integration. $R(\varepsilon)$ is strictly decreasing in $\varepsilon$ in all cases examined.