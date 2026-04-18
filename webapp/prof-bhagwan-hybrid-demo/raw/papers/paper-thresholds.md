

[Page 1]
Why Nothing Happens, Then Everything
Does:
Persistent Noise and the Theory of
Thresholds*
Bhagwan Chowdhry
Indian School of Business & UCLA Anderson School of Management
bhagwan@isb.edu
March 22, 2026
Abstract
Why do small signals accumulate without apparent effect, until one large signal
triggers sudden, disproportionate action? A spouse's daily complaints go unheeded
for months; a single sentence ends the marriage. This paper derives threshold
behavior—long silences, sudden jumps, slow corrections—from the time-series
properties of noise alone. When noise is fractionally integrated with memory
parameter $d$, threshold crossing time is $T^*(d) = A^{2/(1-2d)}$, where A captures signal
difficulty. As $d \to 1/2$, silence becomes permanent. Signal difficulty and noise
memory are supermodular: each amplifies the damage done by the other. The
framework unifies financial crises, credit ratings, neural firing, grade boundaries,
and lumpy investment under a single equation and a single parameter.
**Keywords**: thresholds, long memory, fractional integration, signal detection, financial
crises, credit ratings
**JEL Codes**: C22, D83, G01, G24
***
*I thank seminar participants for comments. All errors are mine.
1

[Page 2]
# 1 Introduction

Consider a marriage in trouble.

For months—perhaps years—one partner has been signaling distress. A complaint about the dishes. Irritation at a forgotten anniversary. A quiet withdrawal from conversation. Tears that come a little too easily. Each signal is real. Each carries genuine information about the state of the relationship. And yet the other partner does not act. They accommodate, perhaps. They apologize, occasionally. But they do not fundamentally change. Life continues. The marriage drifts.

Then one evening, without apparent warning, comes the sentence that changes everything: *I think we should separate.*

Suddenly, everything moves. Couples therapy is booked. Promises are made. Patterns of decades are re-examined overnight. The response to this single sentence exceeds the cumulative response to a thousand prior signals. How is this possible? The information content of “I want a separation” is not a thousand times greater than the information in a year of daily complaints. The underlying truth of the marriage—its actual health—has been deteriorating continuously. Nothing discrete happened in the world. And yet the response is violently discrete.

The standard answer is unsatisfying. Behavioral economists call it inattention. Psychologists call it denial. Sociologists call it habituation. These are labels, not explanations. They tell us that people ignore small signals and respond to large ones— without telling us *why* this is the rational, indeed the only sensible, response to a world structured in a particular way.

This paper offers a different account. The discontinuity is not a failure of rationality. It is the correct response to a fundamental property of how information accumulates in the presence of noise with memory.

The complaining spouse is generating a signal:

$y_t = \beta \cdot x_t + \varepsilon_t$

where $\beta$ is the true state of the marriage, $x_t$ is the amplitude of today’s complaint, and $\varepsilon_t$ is the noise that surrounds it—the bad day at work that explains the irritability, the accumulated small frictions that have nothing to do with the core problem. The listening partner is running an estimation problem: they observe $y_t$ every day but cannot observe $\beta$ or $\varepsilon_t$ separately. They are trying to estimate whether $\beta$ exceeds a

[Page 3]
critical level that warrants action.
What they can learn depends not on the signal—which has been present all along—
but on the *memory of the noise*.
Daily marital complaints are not independent draws. They are serially correlated—
deeply, persistently so. The irritation of Monday bleeds into Tuesday. The resentment
of last month colors the complaint of this morning. This noise $\epsilon_t$ is not white. It is
fractionally integrated, with a memory parameter *d* that may be close to 1/2. And
this matters enormously. Under white noise (*d* = 0), each complaint is an independent
signal; the listener gradually accumulates precision and eventually detects the true
state. Under persistent noise (*d* close to 1/2), averaging fails—old noise does not wash
out—and the listener's estimate never converges to the truth no matter how many
observations accumulate.
The key result is the *threshold crossing time*:
$$
T^*(d) = \left( \frac{\tau^*\sigma\sqrt{C_d}}{\delta \cdot x} \right)^{2/(1-2d)}
$$
where $\delta$ is the true excess signal, $\sigma$ is noise intensity, $x$ is signal amplitude, $\tau^*$ is the
detection criterion, and $C_d = \Gamma(1 - 2d)/\Gamma(1 - d)^2$ diverges as $d \to 1/2$. Define the
signal difficulty $A \equiv \tau^*\sigma\sqrt{C_d}/(\delta x)$. Then $T^*(d) = A^{2/(1-2d)}$.
The waiting time is not linear in *d*. It is the signal difficulty raised to a power
that itself explodes as *d* approaches 1/2. Under white noise, $T^* = A^2$. Under *d* = 0.4,
$T^* = A^{10}$. A signal that would be detected in $A^2 = 100$ periods under white noise takes
$A^{10} = 10^{10}$ periods under *d* = 0.4 noise. The marriage is not just hard to read. It is, for
all practical purposes, permanently unreadable through gradual accumulation—until
one large signal, or a collapse in the noise regime, allows crossing in a single period.
The phenomenon is not peculiar to marriages. It appears wherever agents must
detect a true state from noisy signals.
A bank accumulates small signs of counterparty stress for months before suddenly
refusing to roll over overnight funding. A rating agency watches a firm's coverage ratios
gradually deteriorate for years before a single-notch downgrade triggers index exclusion
and a cascade of forced selling. A neuron integrates thousands of sub-threshold synaptic
inputs in near-silence before a single large input triggers an action potential. A student
works at a steady pace through a semester, then suddenly intensifies effort in the final

[Page 4]
weeks before a grade boundary. An economy absorbs rising debt ratios and widening
current account deficits for a decade before a sudden stop.

These phenomena have been studied separately—in corporate finance, macroeco-
nomics, neuroscience, education, and sociology. They share a common vocabulary
of “tipping points,” “thresholds,” and “cascades.” But the vocabulary has lacked a
mechanism. Why do thresholds exist? Why are they crossed suddenly? Why is the
response discontinuous even when the underlying truth changes continuously? Why
does more information sometimes fail to help?

The answer, we argue, is the memory parameter $d$ of the noise surrounding the signal.
When $d$ is low, signals accumulate into readable estimates. When $d$ approaches 1/2,
signals drown in their own persistent noise. When the noise regime breaks—through a
large exogenous shock or a structural change in $d$—the accumulated signal becomes
suddenly readable, and action follows all at once. The theory unifies these phenomena
under a single equation. It predicts how long the silence lasts, how large the jump is,
how slowly the correction occurs—all as functions of $d$.

The paper’s contribution is to *derive* this pattern from first principles. We do not
assume a binary action space—discreteness emerges from the accumulation process. We
do not impose an exogenous threshold—the crossing point is determined endogenously
by the cost structure and the noise environment. We do not restrict payoff functions to
be non-smooth—the jump follows from the mathematics of learning under persistent
noise alone.

The remainder proceeds as follows. Section 2 develops the formal model, derives the
master equation, and establishes the main result. Section 3 works out the comparative
statics—what makes the silence longer, the jump larger, and the correction slower.
Section 4 maps the theory onto five applications: financial crises, credit ratings, neurons,
grade boundaries, and investment indivisibilities. Section 5 develops the identification
and estimation strategy. Section 6 concludes.

# 2 The Model

## 2.1 The Estimation Environment

An agent observes a stream of outcomes over time. Each outcome carries information
about an unknown state of the world—the true health of a relationship, the true quality

[Page 5]
of a borrower, the true return to an investment. The agent cannot observe the state directly; they must infer it.

Let $\beta \in \mathbb{R}$ denote the true state—fixed, unknown, and constant. At each period $t = 1, 2, ...$, the agent observes:
$$
y_t = \beta \cdot x_t + \varepsilon_t
$$
where $x_t > 0$ is the amplitude of the period-$t$ signal and $\varepsilon_t$ is noise. The agent knows $x_t$ and observes $y_t$. They do not observe $\beta$ or $\varepsilon_t$ separately.

We normalize signal amplitude to $x_t = x > 0$ for all $t$. This is not innocuous—we relax it in Section 4 when we derive crossing by large shocks—but it is the right baseline, because it isolates the role of noise memory from the role of signal size.

## 2.2 The Noise Process and Its Memory

The noise $\varepsilon_t$ is a fractionally integrated process of order $d$, written $\varepsilon_t \sim I(d)$. It is generated by:
$$
\varepsilon_t = (1 - L)^{-d} \eta_t = \sum_{j=0}^{\infty} \psi_j(d) \eta_{t-j}
$$
where $L$ is the lag operator, $\eta_t \stackrel{i.i.d.}{\sim} N(0, \sigma^2)$, and the moving-average weights are:
$$
\psi_j(d) = \frac{\Gamma(j+d)}{\Gamma(d) \Gamma(j+1)} \sim \frac{j^{d-1}}{\Gamma(d)} \quad \text{as } j \to \infty
$$
The weight $\psi_j(d)$ governs how much influence a shock from $j$ periods ago retains today. Its decay is hyperbolic—proportional to $j^{d-1}$—rather than the exponential decay $\rho^j$ of a standard AR(1). Exponential decay means the past is effectively forgotten after a finite horizon. Hyperbolic decay means the past is never fully forgotten. A shock from $j = 1,000$ periods ago still retains weight $\sim 1000^{d-1}$: small, but present, and summing over all past shocks, non-negligible in aggregate.

The autocovariance at lag $k$ satisfies:
$$
\gamma(k) = \mathbb{E}[\varepsilon_t \varepsilon_{t-k}] \sim \frac{\sigma^2}{1-2d} k^{2d-1} \quad \text{as } k \to \infty
$$
For $d > 0$, the autocovariances are not summable: $\sum_{k=1}^{\infty} \gamma(k) = \infty$. This is the technical definition of long memory, and it is what breaks the standard central limit theorem.

[Page 6]
underlying ordinary inference.
Three benchmark cases organize the parameter space. At $d = 0$, white noise: each period’s noise is independent, the past irrelevant. At $d \in (0, 1/2)$, stationary long memory: the process is persistent but mean-reverting—the closer to 1/2, the more it resembles a random walk over any finite horizon. At $d = 1/2$, the boundary: the long-run variance is infinite and no finite accumulation of signals crosses the detection threshold. At $d < 0$, anti-persistence: shocks are negatively correlated across time, the process mean-reverts faster than white noise. As we show in Section 4, this is the regime of the neuron.

## 2.3 The Precision Accumulation Result
After $T$ periods, the OLS estimate of $\beta$ is:
$$
\hat{\beta}_T = \beta + \frac{1}{Tx} \sum_{t=1}^T \varepsilon_t = \beta + \frac{S_T}{Tx}
$$
where $S_T = \sum_{t=1}^T \varepsilon_t$ is the partial sum of the noise. The fundamental result for fractionally integrated processes (Granger and Joyeux, 1980; Hosking, 1981) gives:
$$
\text{Var}(S_T) \sim C_d \cdot \sigma^2 \cdot T^{2d+1}
$$
where $C_d = \Gamma(1 - 2d) / \Gamma(1 - d)^2$ is a constant that diverges as $d \to 1/2$ and reduces to $C_0 = 1$ at $d = 0$.

The variance of the estimator is therefore:
$$
\text{Var}(\hat{\beta}_T) = \frac{C_d \sigma^2}{x^2} \cdot T^{2d-1}
$$
and the *effective precision*—the reciprocal of variance—is:
$$
P_T(d) = \frac{x^2}{C_d \sigma^2} \cdot T^{1-2d}
$$
The exponent $1 - 2d$ governs everything. It is positive for $d < 1/2$, zero at $d = 1/2$, and negative for $d > 1/2$. Precision grows, stays constant, or falls depending entirely on which side of 1/2 the memory parameter lies.

[Page 7]
## 2.4 The Detection Statistic
The agent acts when their estimate of $\beta$ is sufficiently precise to conclude that $\beta$ exceeds a threshold $\beta_0$. Define the excess signal $\delta \equiv \beta - \beta_0 > 0$. The t-statistic for detecting $\delta > 0$ after $T$ periods is:
$$
T_T(d) = \frac{\hat{\beta}_T - \beta_0}{\sqrt{\text{Var}(\hat{\beta}_T)}} = \frac{\delta x}{\sigma \sqrt{C_d}} \cdot T^{(1-2d)/2}
$$
The agent acts when $T_T(d) \ge \tau^*$, where the detection criterion:
$$
\tau^* = \Phi^{-1}\left(\frac{c_1}{c_1+c_2}\right)
$$
is determined by the loss function: $c_1$ is the cost of acting on a false signal (Type I error), $c_2$ is the cost of missing a true signal (Type II error). No binary action space is assumed; the agent acts when the posterior probability that $\beta > \beta_0$ crosses the threshold implied by this cost structure.

## 2.5 The Central Result
Setting $T_{T^*}(d) = \tau^*$ and solving:

> **Proposition 1** (Threshold Crossing Time). *Under the regression model with I(d) noise, $d \in (-1/2, 1/2)$, constant signal amplitude $x$, and detection criterion $\tau^*$, the threshold crossing time is:*
> $$
T^*(d) = \left(\frac{\tau^* \sigma \sqrt{C_d}}{\delta \cdot x}\right)^{2/(1-2d)} = A^{2/(1-2d)}
> $$
> *where $A \equiv \tau^* \sigma \sqrt{C_d} / (\delta x)$ is the signal difficulty index. For $d \ge 1/2$, $T^* = \infty$: no finite accumulation of signals crosses the threshold.*

> **Corollary 1.1** (Supermodularity). *Signal difficulty and noise memory are strict complements:*
> $$
\frac{\partial^2 \log T^*}{\partial \log A \partial d} = \frac{4}{(1-2d)^2} > 0
> $$
> *Each amplifies the damage done by the other.*

[Page 8]
**Corollary 1.2** (Monotonicity in d). For fixed $A > 1$, $T^*(d)$ is strictly increasing and convex in $d$ on $(−1/2, 1/2)$, with $T^* \to A$ as $d \to −1/2$ and $T^* \to \infty$ as $d \to 1/2$.

**Corollary 1.3** (The Endogenous Jump). Any outcome variable that is a continuous functional of $T_r(d)$ and is zero below $\tau^*$ is continuous in $T$ for $T \neq T^*$ and discontinuous at $T = T^*$. The jump is derived, not assumed.

The third corollary is where the paper does the work it set out to do. We have not assumed a binary action space. We have not imposed an exogenous threshold. The discrete jump at $T^*$ follows from the precision path crossing an endogenously determined critical level. The discreteness is a property of the noise, not of the model’s architecture.

## 2.6 Two Mechanisms of Crossing When $d \ge 1/2$
Proposition 1 states that for $d > 1/2$, $T^* = \infty$. Gradual accumulation never crosses the threshold. Yet crises occur, diagnoses are made, ratings change. Two mechanisms restore finite crossing without contradicting the proposition.

**Mechanism A: High-amplitude shock.** At time $T_b$, signal amplitude jumps from $x$ to $x_T \gg x$. The single-period contribution to $T_r$ is $\delta x_T / (\sigma\sqrt{C_d} \cdot \sqrt{Q_T})$. If $x_T$ is large enough, this single increment crosses $\tau^*$ regardless of $d$. The separation announcement, the Lehman filing, the sudden test-result deterioration—each is a large $x_T$ that crosses in one period a threshold the small daily signals could never reach.

**Mechanism B: Structural break in d.** At time $T_b$, the memory parameter drops from $d_H \ge 1/2$ to $d_L < 1/2$—a regime change in the noise process. The crossing time after the break is:
$$
s^* = \left( \frac{(\tau^{*2} - P_{T_b}) C_{d_L} \sigma^2}{x^2} \right)^{1/(1-2d_L)}
$$

The system was storing no useful information for $T_b$ periods. Once $d$ drops below $1/2$, the estimation process resumes and crosses relatively quickly, because the precision needed above $P_{T_b}$ is smaller than starting from zero. The observable signature: a period of compressed volatility immediately before the crisis event—the calm before the storm—followed by rapid action once the regime change occurs.

[Page 9]
## 2.7 The Overshoot and the Correction
The crossing at $T^*$ is not clean. In discrete time, the t-statistic arrives at $T_r^* = \tau^* + O$ where the overshoot $O \ge 0$ is the amount by which the threshold is exceeded at the crossing moment. By Wald's identity applied to the stopped process:
$$
\mathbb{E}[O] \approx \frac{\sigma\sqrt{C_d}}{2\delta x} (T^*)^{2d/(1-2d)} = \frac{1}{2} A^{2d/(1-2d)} \cdot \frac{\sigma\sqrt{C_d}}{\delta x}
$$

The overshoot is increasing in $d$: near-boundary systems overshoot more. This is the formal expression of the “I had no idea it was this bad" phenomenon. The listener did not underestimate the marriage's problem because they were irrational. The persistent noise prevented precise estimation, so when the crossing finally occurred, the jump in the posterior was discontinuous and large—an overshoot—followed by a correction as subsequent signals refine the estimate toward the true $\beta$.

The post-crossing correction half-life—the time for the overshoot to halve—is:
$$
k^* \sim \left(\frac{O}{2}\right)^{1/(1-2d)} \cdot \frac{C_d \sigma^2}{x^2}
$$

High-$d$ systems overshoot more *and* correct more slowly. Both the jump and the recovery are governed by the same parameter.

Collecting the three phases, the complete temporal anatomy of a threshold event is:
$$
\underbrace{T^* = A^{2/(1-2d)}}_{\text{silence}} \xrightarrow{\text{cross}} \underbrace{\mathcal{O} \approx \frac{1}{2} A^{2d/(1-2d)} \cdot \frac{\sigma\sqrt{C_d}}{\delta x}}_{\text{jump}} \xrightarrow{\text{correct}} \underbrace{k^* \sim \mathcal{O}^{1/(1-2d)} \cdot \frac{C_d \sigma^2}{x^2}}_{\text{recovery}}
$$

All three phases are governed by a single number: $d$.

# 3 Comparative Statics

## 3.1 What Makes the Silence Longer
Define the memory multiplier $\kappa(d) = 2/(1 - 2d)$—the common elasticity of $T^*$ with respect to every parameter. It equals 2 at $d = 0$ (the white-noise baseline) and diverges as $d \to 1/2$.

[Page 10]
**Proposition 2** (Comparative Statics on Waiting Time). The signed elasticities of $T^*$ with respect to each parameter are:

| | |
| :--- | :--- |
| $\frac{\partial \log T^*}{\partial \log \tau^*} = \kappa(d)$ | $\frac{\partial \log T^*}{\partial \log \sigma} = \kappa(d)$ |
| $\frac{\partial \log T^*}{\partial \log \delta} = -\kappa(d)$ | $\frac{\partial \log T^*}{\partial \log x} = -\kappa(d)$ |

where $\kappa(d) = 2/(1-2d)$ is the common elasticity multiplier, increasing in $d$ and diverging as $d \to 1/2$.

The structure is clean and surprising: memory amplifies every other comparative static. A parameter that would have elasticity 2 under white noise has elasticity 10 under $d = 0.4$ and elasticity 100 under $d = 0.49$. Doubling signal amplitude under $d = 0.4$ does not halve the waiting time—it reduces it by a factor of $2^{10} = 1,024$.

This is why the design of information systems matters so much more in high-$d$ environments than intuition suggests. More frequent monitoring under white noise helps in proportion to frequency. More frequent monitoring under $d = 0.4$ barely moves the needle—because the problem is not information frequency but information accumulation, and accumulation fails when $d$ is high.

## 3.2 The Supermodularity of Silence and Noise

The most important comparative static is not about any single parameter but about their interaction. Define the threshold difficulty index $D = \tau^*\sigma/(\delta x)$. Under white noise, $T^* = D^2$. Under $I(d)$ noise:
$$
T^*(d) = (D \cdot \sqrt{C_d})^{2/(1-2d)}
$$
**Proposition 3** (Supermodularity). $\partial^2 \log T^*/(\partial \log D \, \partial d) = 4/(1-2d)^2 > 0$. Detection difficulty and noise memory are strict complements: each makes the other's effect on waiting time larger.

Supermodularity means that improving on one dimension is most valuable when the other is also improving. Reducing $D$—lowering $\tau^*$, strengthening the signal, reducing noise—has the largest effect on $T^*$ precisely when $d$ is high. And reducing $d$ has the largest effect precisely when $D$ is large. They are complements, not substitutes, and their joint effect is supermodular. This has a direct policy implication that is frequently

[Page 11]
missed: regulators in high-$d$ environments should not simply lower their detection
criterion. They should simultaneously address the noise memory itself.

## 3.3 What Makes the Jump Larger
**Proposition 4** (Overshoot Comparative Statics). The expected jump magnitude at
threshold crossing satisfies:
$$
\frac{\partial \log E[O]}{\partial d} > 0, \quad \frac{\partial \log E[O]}{\partial \log \sigma} > 0, \quad \frac{\partial \log E[O]}{\partial \log \delta} < 0, \quad \frac{\partial \log E[O]}{\partial \log x} < 0
$$
Systems with higher memory, higher noise, weaker true signals, or smaller amplitude
shocks overshoot more when they finally cross.

Three empirical implications follow. First, rating changes at consequential boundaries should be followed by larger market reactions than interior changes—because consequential boundaries have higher $T^*$, producing larger $T^*$ and therefore larger overshoots. Second, financial crises that follow longer calm periods should produce larger initial dislocations. Third, medical diagnoses made later in disease progression should be associated with more aggressive initial treatment—because later diagnosis implies harder detection (higher $d$ or lower $δ$), which implies a larger overshoot in estimated disease severity.

## 3.4 What Makes the Correction Slower
**Proposition 5** (Correction Speed). The half-life of the post-crossing overshoot is
increasing in $d$ and $σ$, and decreasing in $x$ and $δ$. High-memory systems overshoot more
and correct more slowly—the jump and the recovery are governed by the same parameter
$d$.

The ratio $k^*/T^*$ is not constant: at $d = 0$, correction takes roughly as long as
detection. At high $d$, crossing is sudden but correction is very slow. The crisis is brief;
the recovery is long. This matches the empirical pattern of financial crises—sharp onset,
protracted recovery—and of marital breakdown—sudden crisis, years of adjustment.

[Page 12]
## 3.5 Summary of Comparative Statics

Table 1 summarizes the signed effects. Every parameter moves all three phases in the same direction. There is no tradeoff: whatever makes the silence longer also makes the jump larger and the recovery slower. The single index $d$ governs the entire phenomenology.

Table 1: Signed elasticities of the three phases with respect to model parameters. All elasticities evaluated at $d \in (0,1/2)$, $A > 1$. $\kappa = 2/(1 - 2d)$.

| Parameter | Silence $T^*$ | Jump $O$ | Recovery $k^*$ | Mechanism |
| :--- | :--- | :--- | :--- | :--- |
| $d \uparrow$ | + (explosive) | + | + | Memory amplifies all three phases |
| $\sigma \uparrow$ | +$\kappa$ | + | + | Noise buries signal, slows correction |
| $\delta \uparrow$ | $-\kappa$ | — | — | Stronger signal compresses all phases |
| $x \uparrow$ | $-\kappa$ | — | — | Larger amplitude compresses all phases |
| $\tau^* \uparrow$ | +$\kappa$ | + | + | Stricter criterion delays and amplifies |

## 3.6 The Anti-Persistence Region

For $d \in (-1/2,0)$, $\kappa(d) \in (1,2)$—below the white-noise baseline. Anti-persistence actively compresses the sensitivity of $T^*$ to signal difficulty. And the overshoot at crossing is smaller: the system arrives at the threshold with less accumulated estimation error, because old signals are actively discounted.

This is a design principle, not just a parameter variation. A system that wants fast, accurate threshold detection should engineer anti-persistence into its noise structure. The nervous system does this through the refractory period. Sequential testing procedures in statistics do this through alpha-spending functions. Efficient markets do this, imperfectly, through short-selling─mechanisms that mean-revert prices toward fundamentals, reducing $d$ below what it would be in their absence.

[Page 13]
# 4 Applications

## 4.1 Overview

The master equation places domains on a one-dimensional spectrum parameterized by $d$. Each domain supplies an estimate of $d$ from its empirical noise structure; the model then predicts silence, jump, and recovery. Table 2 summarizes the five applications.

Table 2: Predicted threshold characteristics by domain, for $A = 2$.

| Domain | $d$ | $\kappa(d)$ | Silence $T^*$ ≈ | Design objective |
| :--- | :--- | :--- | :--- | :--- |
| Neurons | -0.30 | 1.25 | $2^{1.25} \approx 2.4$ | Speed (engineered) |
| Grades (within) | 0.05 | 2.10 | $2^{2.1} \approx 4.3$ | Feedback |
| Investment | 0.25 | 2.70 | $2^{2.7} \approx 6.5$ | Efficiency |
| Financial markets | 0.40 | 10.0 | $2^{10} = 1,024$ | Emergent |
| Credit ratings | 0.45 | 20.0 | $2^{20} \approx 10^6$ | Stability (imposed) |

The range from neurons to credit ratings is not a modest quantitative difference. Under $A = 2$, the neuron detects in 2.4 periods; the rating agency in 1,048,576 periods. Both are doing the same thing—integrating a noisy signal and acting when the estimate is sufficiently precise. The difference is one number: $d$.

## 4.2 Financial Crises

Financial volatility has long memory. The foundational result of Ding, Granger, and Engle (1993), confirmed across asset classes and time periods, estimates $d \approx 0.35-0.45$ for realized volatility and related spread processes. Under $d = 0.4$, the crossing time is $T^* = A^{10}$.

For a typical financial system where $A \approx 2$, the silence lasts $2^{10} = 1,024$ periods. If periods are weeks, this is roughly twenty years of apparent stability—not inconsistent with the observed periodicity of major systemic crises in developed economies. The Minsky cycle maps directly onto the model: displacement (the onset of $d > 0$), euphoria (the long silence under $d \approx 0.4$, where agents rationally continue leveraging because signals are undetectable), and panic (the crossing, triggered by Mechanism A or a volatility collapse under Mechanism B).

The overshoot under $d = 0.4$, $A = 2$ is $O \approx \frac{1}{2} \cdot 2^4 = 8$: the system was not eight times more distressed than it appeared before the crisis, but the estimate of distress

[Page 14]
jumped by eight units at the crossing moment. The subsequent recovery under the same $d$ has half-life $k^* \sim 8^5 = 32,768$ periods—years, not months. The long aftermath of financial crises is not a separate phenomenon from the delayed detection. It is the same phenomenon viewed from the other side of $T^*$.

Three novel predictions emerge. First, pre-crisis calm duration should scale as $A^{10}$ with the pre-crisis estimate of $d$—testable in a cross-country panel of sovereign spread series. Second, crises following longer calm periods should be triggered by larger-amplitude events, because the system requires a larger $x_T$ to cross through Mechanism A. Third, post-crisis revisions in pre-crisis risk assessments should scale with $O(d)$—systems with higher estimated pre-crisis $d$ should show larger “we had no idea” revisions.

## 4.3 Credit Ratings
Credit ratings present a richer noise structure because two distinct values of $d$ operate simultaneously. Firm fundamentals—cash flows, coverage ratios—have moderate persistence, with $d_{\text{firm}} \approx 0.2–0.3$. But rating agencies explicitly apply through-the-cycle smoothing, averaging performance over multi-year horizons to reduce rating volatility. A moving-average filter applied to an $I(d)$ process amplifies persistence: the effective memory parameter $d_{\text{eff}}$ substantially exceeds $d_{\text{firm}}$. If $d_{\text{eff}} \approx 0.45$ and $d_{\text{market}} \approx 0.2$, the lag ratio:
$$ \frac{T^*_{\text{rating}}}{T^*_{\text{market}}} = A^{2/(1-2d_{\text{eff}})}/A^{2/(1-2d_{\text{market}})} = A^{20-5} = A^{15} $$
For $A = 1.5$: a factor of $1.5^{15} \approx 438$. Ratings lag markets by a factor that is exponential in the difference between their memory parameters—not merely proportional to the smoothing window.

A counterintuitive prediction concerns the investment-grade/junk boundary. At this boundary, the categorical prize $\Delta V$ is large—index inclusion, regulatory capital requirements, investor mandates. Large $\Delta V$ implies lower effective $\tau^*$ at this boundary. Lower $T^*$ reduces $A$, which reduces $T^*$. So rating transitions at consequential boundaries occur faster than interior transitions, conditional on fundamentals—not because the signals are clearer, but because agents care more and apply lower effective detection criteria. The model also predicts that boundary crossings produce larger overshoots than interior crossings, explaining the well-documented “fallen angel” effect: spread widening at investment-grade-to-junk downgrades substantially exceeds widening at

[Page 15]
interior downgrades even controlling for fundamental deterioration.

## 4.4 Neurons
Neurons are the purest implementation of the threshold model: integrate inputs, cross a threshold ($\approx -55$ mV), fire an action potential, reset. But the neuron does something the basic model does not: it engineers $d < 0$ into its noise structure through the refractory period.

Immediately after firing, the neuron hyperpolarizes—the membrane potential drops to approximately -80 mV before recovering. During this period, the neuron is less sensitive to new inputs, creating negative serial correlation in noise: a period of elevated noise (which triggered firing) is followed by suppressed sensitivity. The autocovariance $\gamma(1) < 0$, consistent with $d \approx -0.2$ to $-0.4$.

Under $d = -0.3$, $\kappa(-0.3) = 2/1.6 = 1.25$, and $T* = A^{1.25}$ versus $A^2$ under white noise. The neuron detects the same signal in fewer than half the periods a white-noise system would require. The refractory period is not a limitation on firing rate. It is the mechanism by which the nervous system engineers anti-persistence into the noise structure, accelerating threshold detection.

This reinterpretation generates a cross-modal prediction: modalities requiring faster detection—auditory onset, which triggers startle and attention shifts—should have shorter refractory periods (more negative $d$, lower $T*$). Modalities signaling sustained states—pain, thermal sensation—require less speed and tolerate higher $d$ (longer refractory periods). Neural adaptation—reduced firing under sustained stimulation—follows directly from Proposition 5: the same $d < 0$ that accelerated detection also accelerates the post-crossing correction, quickly registering that further firing is unnecessary.

## 4.5 Grades and Academic Boundaries
Academic performance involves two nested noise structures with different memory parameters.

*Within semesters*, individual assignments are approximately independent conditional on ability: $d_{within} \approx 0$. Each assessment is nearly its own experiment; students receive fast, accurate feedback about their position relative to a grade boundary.

*Across semesters*, cumulative GPA is a running average of all past grades. An

[Page 16]
average of T i.i.d. observations has effective memory approaching:
$$
d_{GPA} \approx \frac{1}{2} - \frac{1}{2T}
$$
as $T$ grows—approaching 1/2 as the degree progresses. A student in their final semester of a four-year degree faces $d_{GPA} \approx 0.47$: each new grade contributes approximately $1/T$ of its value to the GPA, and precision growth has nearly stalled.

Two predictions emerge. First, grade bunching is sharp within semesters and smooth across them. Within a course, $d \approx 0$ and $\kappa = 2$: the effort response to being near a boundary is strong and the impact of effort on the grade outcome is direct. Across courses, $\kappa = 20$ but the marginal impact of a semester's effort on cumulative GPA is only $1/T$—these forces partly offset, producing muted cross-semester bunching.

Second, GPA recovery is far slower than GPA decline—and the asymmetry worsens with seniority. A bad first year is a large negative $x_{iT}$: Mechanism A, which crosses any threshold instantly regardless of $d$. But recovery requires gradual accumulation against a high-$d$ averaging filter. At $d_{gpa} \approx 0.47$, recovery time is $A^{20}$ periods—near-impossible within a degree program. GPA lock-in is not a property of the grading system. It is the mathematics of averaging under long memory.

## 4.6 Investment Indivisibilities

Firms observing demand for their products face signals with moderate persistence. Empirical estimates of $d$ for demand-side variables—retail sales, industrial production, capacity utilization—cluster around $d \approx 0.2-0.35$. Under $d = 0.25$, the crossing time is $A^{2.67}$—moderately slow. Investment decisions compound this with irreversibility. Real-options theory shows that irreversibility raises the effective $\tau^*$ above the zero-NPV threshold; in the model's terms, irreversibility increases $A$, which under $d = 0.25$ raises $T^*$ by $A^{2.67}$.

The combined effect—moderate $d$ plus irreversibility-inflated $\tau^*$—generates the observed investment pattern: long inaction, lumpy investment when the threshold is crossed, followed by slow correction as firms discover they may have over-invested.

Sectoral variation offers a sharp prediction. High-$d$ sectors—infrastructure, mining, commercial real estate—face demand signals with long memory and speculative noise that itself exhibits persistence. The model predicts longer boom-bust cycles, larger overshoots at the investment spike, and slower capital adjustment afterward. Low-$d$

[Page 17]
sectors—retail, consumer services—face mean-reverting demand; investment should
be more frequent, smaller, and faster to correct. The key interaction is that $d$ and
minimum efficient scale (which determines $\tau*$) are supermodular in their effects on
lumpiness—a prediction testable across sectors with cross-sectional variation in both.

## 4.7 The Unifying Pattern
Across all five applications, $d$ is not randomly assigned. It reflects the design objective
of the system that generates the signal environment. Neurons, optimized for speed,
engineer $d < 0$ through the refractory period. Rating agencies, optimizing for stability
of assessment, push $d$ toward 1/2 through through-the-cycle smoothing. Financial
markets, neither designed for speed nor stability but emerging from the interaction of
many agents, occupy the critical region $d \approx 0.4$. The differences in $d$ across domains
are not measurement error. They are the fingerprints of the design objectives, implicit
or explicit, that shaped each system.

# 5 Identification and Estimation
## 5.1 The Identification Logic
The master equation $T^*(d) = A^{2/(1-2d)}$ generates three observables—silence, jump, and
recovery—as functions of two composites: $d$ and $A$. Three moments, two unknowns:
the system is overidentified. The identification strategy exploits this.

**Step 1: Estimate d.** Estimate the memory parameter from the time-series properties of
the noise process—the residuals from the signal regression $y_t = \beta x_t + \hat{\epsilon}_t$—independently
of any threshold event.

**Step 2: Identify A.** Given $\hat{d}$ and observed silence duration $T^*$:
$$
\hat{A} = (T^*)^{(1-2d)/2}
$$
Standard error from the delta method: $se(\hat{A}) \approx \hat{A} \cdot \log T^* \cdot se(d)$.

**Step 3: Test overidentification.** With $d$ and $\hat{A}$ in hand, the model predicts jump
and recovery without additional free parameters. The Hansen J-statistic:
$$
J = T \cdot m' \Omega^{-1} m \sim \chi^2(2)
$$

[Page 18]
where m stacks the three moment conditions (silence, jump, recovery), has 2 degrees of freedom because there is one free parameter ($d$) and three moments. The J-test has power against two alternatives: wrong functional form for $T^*(d)$, and wrong cross-equation restrictions (i.e., the same $d$ does not govern all three phases). Both failures are informative.

## 5.2 Estimating d
Three estimators are available. The Geweke-Porter-Hudak (GPH) estimator regresses log periodogram ordinates on log frequency near zero, exploiting the spectral representation of $I(d)$ processes. It is consistent and asymptotically normal under standard regularity conditions. The local Whittle estimator (Robinson, 1995) maximizes an approximate Whittle likelihood and allows for short-run ARMA dynamics and conditional heteroskedasticity—preferred for financial applications where GARCH effects are ubiquitous. The rescaled range (R/S) statistic provides a nonparametric alternative for short series, though with poor small-sample properties for $T < 100$.

In applications where the signal $x_t$ is unobserved—relationship health, true credit quality—$d$ must be estimated from the full process $y_t = \beta x_t + \varepsilon_t$. Separating signal memory from noise memory then requires additional structure, and this is where domain knowledge enters.

## 5.3 Domain-Specific Strategies
Financial crises. Estimate $d$ from sovereign spread or CDS series in a five-year pre-crisis window using the local Whittle estimator. Measure silence duration using structural break tests on fundamental series (credit-to-GDP ratio, leverage) as the vulnerability onset date. Measure the jump as spread widening in the first week post-trigger, normalized by pre-crisis weekly volatility. Run the cross-sectional prediction:
$$
\log T_i^* = 2 \cdot \frac{\log \tilde{A}_i}{1 - 2d_i} + u_i
$$
instrumenting $d_i$ with institutional variables—financial development, regulatory quality, central bank independence—that affect noise memory without directly affecting crisis timing.

[Page 19]
**Credit ratings.** Estimate $d_{firm}$ from quarterly fundamentals and $d_{eff}$ from residuals of a rating-on-fundamentals regression. The difference $d_{eff} - d_{firm}$ is the methodology- induced memory increment. Test the boundary-speed prediction by sorting rating transitions into boundary-crossing and interior, then regressing transition time on $\hat{d}_{eff}$, noise, and a boundary indicator: $\hat{\gamma} < 0$ confirms that boundary transitions occur faster conditional on fundamentals.

**Neurons.** Apply GPH and R/S to inter-spike interval series across sensory modalities. Regress $d$ on refractory period duration; the model predicts $\beta < 0$: longer refractory periods imply more negative $d$. Test adaptation dynamics against the post-crossing recovery formula under estimated $d$.

**Grades.** Estimate within-semester $d$ from serial correlation of sequential assignment grades; test $d_{within} \approx 0$. For cumulative GPA, test $d_{GPA} \approx 1/2 - 1/(2T)$ as a function of seniority. Test grade bunching with the cross-cutoff restriction: bunching at boundary $c$ should scale with $\Delta V(c)$, the categorical prize—testable without estimating $d$ directly.

**Investment.** Estimate $d_{demand}$ from industry-level real sales growth. Predict that lumpiness—the fraction of years with zero net investment—is increasing in $d_{sector}$, increasing in minimum efficient scale (which proxies $\tau^*$), and that the two are supermodular in their joint effect on lumpiness.

# 5.4 Threats to Identification

Three threats recur across applications. Regime changes in $d$ invalidate the fixed- parameter assumption; the Breitung-Hassler test for structural breaks in long memory provides a diagnostic, though it has low power in samples of $T < 200$. Endogenous signal amplitude creates bias when agents suppress disclosure near detection thresholds (raising $T^*$) or request additional information (lowering it); mandatory disclosure reforms provide plausible instruments. Composition of $A$ bundles four parameters; cross-sectional variation in analyst coverage, mandatory reporting frequency, and accounting quality provide instruments for $x$, while distance-to-default measures proxy $\delta$ in financial applications.

The identification strategy reduces to three concentric rings of ambition. The inner ring—estimating $d$ from financial spread series, testing the duration-volatility prediction

[Page 20]
in sovereign crises, and the fallen angel overshoot regression—is feasible with existing data and standard methods. The middle ring—the three-moment overidentification test and the boundary-speed test in ratings—requires careful design. The outer ring—causal identification through quasi-experiments and joint estimation across domains—is the long-run research program.

# 6 Conclusion

## 6.1 What the Paper Has Done

This paper set out to explain the pattern that opens it: a spouse's daily complaints go unheeded for months, and then one sentence ends the marriage. The conventional explanations—inattention, denial, habituation—are labels, not mechanisms. They describe the phenomenon without deriving it.

The paper has derived it from a single structural change to the estimation environment: allowing the noise $\varepsilon_t$ in the regression $Y_t = \beta x_t + \varepsilon_t$ to be fractionally integrated with memory parameter $d$. From this change alone, three results follow without additional assumptions.

First, discreteness emerges from continuity. The agent's estimate $\hat{\beta}_T$ evolves continuously, but the precision path $P_T \sim T^{1-2d}$ stalls near the detection boundary when $d$ is close to 1/2. The system sits below the threshold for a long time, then crosses in a single period when a high-amplitude signal arrives or the noise regime shifts. The jump is a property of the accumulation process, not an architectural assumption.

Second, the threshold is derived, not assumed. The crossing point is determined by when accumulated precision reaches the detection criterion implied by the cost structure—no exogenous $\beta^*$ required.

Third, the full temporal anatomy is governed by one equation: $T^*(d) = A^{2/(1-2d)}$. The silence, the jump, and the recovery are all functions of $d$, and their magnitudes grow in concert as $d$ approaches 1/2. The differences between a neuron firing and a financial crisis erupting are, in this framework, differences in a single number.

## 6.2 The Three Core Claims

The *mathematical claim*—that fractional integration generates threshold-crossing behavior from continuous primitives—is established. The *empirical claim*—that $d$ estimated

[Page 21]
from noise predicts silence, jump, and recovery jointly and consistently across domains—
is the agenda of Section 5, whose inner ring is feasible now. The conceptual claim—that
$d$ reflects the design objective of each system—is the deepest and most speculative:
neurons engineer $d < 0$ for speed; rating agencies push $d$ toward 1/2 for stability;
markets sit where their emergent dynamics place them.

## 6.3 What the Paper Opens

The most valuable output of a theory is the questions it generates. This one generates
at least four.

*The optimal design of noise.* If $d$ is a design choice, what is the $d$ that minimizes
expected social loss from threshold misses and false alarms? The answer—minimize
$T^*(d) + \lambda O(d) + \mu k^*(d)$ over $d$—delivers an optimal memory parameter as a function of
the social weights on delayed detection, disproportionate response, and slow correction.
For financial regulators, the implication is concrete: optimal disclosure policy sets
amplitude rather than frequency, because amplitude reduces $A$ while frequency barely
moves $T^*$ in high-$d$ environments.

*The epidemiology of crises.* If crisis timing follows $T^*(d) = A^{10}$ under $d = 0.4$, the
cross-country distribution of crisis timing becomes a formal object of study: predicted
by the joint distribution of $A$ and $d$ across countries, not by historical narrative alone.

*The neuroscience of decision-making.* Human decision latency, overreaction mag-
nitude, and correction speed should vary systematically across task types according
to the master equation, because different cognitive tasks expose subjects to different
noise memory structures. Response-time distributions should follow inverse Gaussian
laws with parameters that vary with the estimated $d$ of the task's noise environment—a
falsifiable prediction for controlled experiments.

*The theory of marriage.* Marital stability is not primarily a function of how bad
things are ($\delta$ small) or how strict the threshold for action is ($\tau^*$ large), but of how
persistent the emotional noise of daily life is ($d$ close to 1/2). Longitudinal data on
relationship quality, daily mood, and communication patterns could estimate $d$ from the
time-series of relational signals and test whether the master equation predicts separation
timing. We leave this as an exercise for a braver empiricist than ourselves.

[Page 22]
## 6.4 The Deeper Point

There is a temptation in economics to locate discrete behavior in discrete things: binary choices, step-function payoffs, institutional bright lines. The approach is natural. But it comes at a cost—the discreteness is assumed rather than derived, and the model cannot speak to why the bright lines are where they are, how they change, or what happens if they are drawn differently.

This paper has taken a different approach. The discrete behavior—the long silence, the sudden jump, the slow correction—is derived entirely from the properties of the noise process. No binary actions. No exogenous cutoffs. No non-smooth payoffs. Just a regression model in which the noise has memory, and the mathematical consequences of that memory for what an agent can and cannot learn.

The gain is that the model speaks to things the standard approach cannot. It says how long the silence will last. It says how large the jump will be. It says how slowly the correction will unfold. And it says all three as functions of a single measurable parameter—the memory of the noise—that differs systematically and predictably across domains.

The deeper implication is not fatalistic. The duration of the silence, the magnitude of the jump, and the speed of the recovery are all functions of d—a parameter that, in principle, can be engineered. Neurons found a solution: the refractory period pushes d negative and compresses the silence to milliseconds. Institutions can find analogous solutions through disclosure design, stress testing, and the deliberate introduction of high-amplitude signals at regular intervals.

The long silence is not fate. It is a design problem. And design problems have solutions.

# References

Baillie, Richard T., Tim Bollerslev, and Hans Ole Mikkelsen. 1996. “Fractionally integrated generalized autoregressive conditional heteroskedasticity.” *Journal of Econometrics* 74(1): 3–30.

Breitung, Jörg, and Uwe Hassler. 2002. “Inference on the cointegration rank in fractionally integrated processes.” *Journal of Econometrics* 110(2): 167–185.

Ding, Zhuanxin, Clive W.J. Granger, and Robert F. Engle. 1993. “A long memory

[Page 23]
property of stock market returns and a new model.” *Journal of Empirical Finance* 1(1): 83-106.

Dixit, Avinash K., and Robert S. Pindyck. 1994. *Investment under Uncertainty*. Princeton, NJ: Princeton University Press.

Drehmann, Mathias, and Mikael Juselius. 2014. “Evaluating early warning indicators of banking crises: Satisfying policy requirements.” *International Journal of Forecasting* 30(3): 759-780.

Granger, Clive W.J. 1980. “Long memory relationships and the aggregation of dynamic models." *Journal of Econometrics* 14(2): 227-238.

Granger, Clive W.J., and Roselyne Joyeux. 1980. “An introduction to long-memory time series models and fractional differencing.” *Journal of Time Series Analysis* 1(1): 15-29.

Granovetter, Mark. 1978. “Threshold models of collective behavior.” *American Journal of Sociology* 83(6): 1420-1443.

Hamilton, James D. 1989. “A new approach to the economic analysis of nonstationary time series and the business cycle.” *Econometrica* 57(2): 357-384.

Hosking, J.R.M. 1981. “Fractional differencing.” *Biometrika* 68(1): 165–176.

Laeven, Luc, and Fabian Valencia. 2012. “Systematic banking crises database: An update." IMF Working Paper 12/163.

Lee, David S., and Thomas Lemieux. 2010. “Regression discontinuity designs in economics.” *Journal of Economic Literature* 48(2): 281-355.

Minsky, Hyman P. 1977. “The financial instability hypothesis: An interpretation of Keynes and an alternative to ‘standard' theory.” *Nebraska Journal of Economics and Business* 16(1): 5–16.

Phillips, Peter C.B. 1987. “Towards a unified asymptotic theory for autoregression.” *Biometrika* 74(3): 535-547.

Reinhart, Carmen M., and Kenneth S. Rogoff. 2009. *This Time Is Different: Eight Centuries of Financial Folly*. Princeton, NJ: Princeton University Press.

[Page 24]
Robinson, Peter M. 1995. “Gaussian semiparametric estimation of long range depen-
dence.” *Annals of Statistics* 23(5): 1630–1661.

Schelling, Thomas C. 1978. *Micromotives and Macrobehavior*. New York: W.W. Norton.