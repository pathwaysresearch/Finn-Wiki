

[Page 1]
# Which Firms Innovate, Which Do Not, and Why

## Real Options, Organizational Learning, and Creative Destruction

Bhagwan Chowdhry* Deepa Mani† Madan Pillutla‡

November 2025

## Abstract

Schumpeter's (1942) creative destruction and Aghion and Howitt's (1992) formaliza-
tion of it establish, at the level of the economy, that innovation drives sustained growth
and that incumbent firms will rationally resist it. But why do *some* incumbents inno-
vate while others do not? And what determines the scale and timing of the bets that
innovators make? We provide firm-level microfoundations for these macro results by
building a tractable three-date model that integrates three economic forces: (i) *mar-
ket uncertainty* ($\sigma^2$), which creates option value in the manner predicted by Aghion
and Howitt's models; (ii) *organizational learning* (s), Arrow's (1962) learning-by-doing
parameter, which makes initial investment productive even when intermediate-date
signals are weak; and (iii) the *caricature effect*, the identity lock-in that accumulates
alongside organization capital and raises the effective opportunity cost of redeployment.

The model yields five formal propositions. The optimal policy at the intermediate
date partitions the signal space into expansion, harvest, and abandonment regions.

***

* Indian School of Business, Hyderabad, India. Corresponding author: bhagwan.chowdhry@isb.edu.
† Indian School of Business, Hyderabad, India.
‡ Indian School of Business, Hyderabad, India.

[Page 2]
Firm value decomposes into a current-signals component and a call option on future
market realizations. A firm innovates if and only if the expansion option value ex-
ceeds the first-period loss a condition that is relaxed by higher volatility, stronger
learning, and greater scalability, and tightened by the incumbent's accumulated or-
ganization capital in existing businesses. The initial investment scale is governed by
a threshold on the current market signal that is decreasing in learning intensity. All
three parameters—$\sigma^2$, $s$, and maximum expansion scale $H$—are unambiguously value-
enhancing, inverting the conventional risk-return tradeoff.

We map these results onto Mokyr's (2017) institutional prerequisites for creative
destruction—translated from the societal to the organizational level—and derive six
testable empirical predictions. An eight-cell typology of firm behaviors, from Moon-
shots to Cash Cows to Rational Non-Entrants, organizes the predictions against ob-
servable firm archetypes in contemporary markets for artificial intelligence, electric
vehicles, and biotechnology.

[Page 3]
# 1 Introduction

In the summer of 2007, Netflix's DVD-by-mail business was generating healthy margins on a loyal customer base. Its CEO, Reed Hastings, chose that moment to bet heavily on streaming—a technology with no near-term path to profitability, uncertain content availability, and a user base that barely owned broadband connections. Every discounted cash flow model said the project was value-destroying. Hastings invested anyway.

Across town, Blockbuster—then nine thousand retail stores strong, with a logistics infrastructure that had taken a decade to build, and generating $800 million annually from late fees alone—chose not to match the bet. Blockbuster's board was not asleep. Their organization capital in physical retail was enormous, their margins were real, and every rational calculation about the returns to redirecting resources toward an unproven technology came up negative. They declined.

We know how both stories ended. But here is the question that the endings conceal: *Were both decisions rational at the moment they were made?* We argue the answer is yes, and we build a formal model to show why. More importantly, we show that the same three economic forces that made both decisions rational also determine, with mathematical precision, which types of firms will innovate, at what scale, and when they will abandon.

## Creative Destruction and the Firm

The macro-level backdrop is Schumpeter's (1942) concept of creative destruction—the process by which new innovations systematically replace older technologies and the firms built around them. Steam locomotives displaced horse-drawn wagons. E-commerce hollowed out shopping malls. Smartphones absorbed GPS devices, cameras, MP3 players, and calculators. The process is “creative" because it generates new products, new firms, and higher living standards. It is “destructive” because it renders existing products, capabilities, and expertise obsolete, often swiftly and irreversibly.

[Page 4]
Aghion and Howitt (1992) formalized Schumpeter's intuition in a mathematical growth
model that shows how innovation-driven creative destruction is the engine of long-run eco-
nomic growth. A central, and uncomfortable, implication of their framework is that estab-
lished firms not only fail to lead creative destruction—they have rational incentives to block
it. By deploying financial resources, leveraging regulatory relationships, exercising political
influence, and controlling distribution channels, incumbents can delay the competitive forces
that threaten their business models. From a narrow corporate perspective, such resistance
is defensible even to long-horizon shareholders. But the delay is not prevention. As Aghion
and Howitt (1992) demonstrate rigorously, and as economic history confirms repeatedly,
sustained growth ultimately requires that creative destruction prevail.

What neither Aghion and Howitt (1992) nor the broader macro-growth literature ad-
dresses is the firm-level question: *which firms choose to be agents of creative destruction,
which choose to resist it, and what determines the scale and timing of the bets that innovators
make?* That is the question this paper answers.

## Three Forces

Our analysis rests on three economic forces that interact to produce the innovation decisions
we observe.

**Force 1: Market uncertainty ($\sigma^2$)**. Aghion and Howitt (1992)'s models demonstrate
that innovation value increases nonlinearly with market uncertainty—a prediction that fol-
lows formally from the asymmetric payoff structure of innovative investment. When markets
are stable and predictable, established firms can extract rents from existing technologies
through incremental improvement. When uncertainty is high-when $\sigma^2$ is large because
multiple technological trajectories might succeed, customer preferences could shift dramati-
cally, or regulatory environments might change—the option to pivot, to experiment, and to
exploit upside realizations becomes disproportionately valuable. Our model formalizes this
precisely: the expansion option value is $H \cdot C(x_0, \sigma_0)$, a call-option expression that is strictly

[Page 5]
increasing in $\sigma_0$, with the full downside bounded by the abandonment option.

**Force 2: Organization capital and learning-by-doing ($s$).** Arrow's (1962) concept
of learning-by-doing establishes that investing in an activity generates specific capital—
knowledge, routines, customer relationships, and operational expertise—that makes future
production in that activity cheaper and more productive. In the short run, this is pure
advantage. Toyota makes cars better and cheaper than any startup could, because of ac-
cumulated expertise. But organization capital creates a trap: the better you become at
your existing business, the more expensive it is to redirect resources toward a new one. An
incumbent evaluating a new market competes not just against entrants but against its own
accumulated competence in the existing business. Startups, by contrast, have no organiza-
tion capital to protect and no opportunity cost of redeployment. They can commit fully to
the new technology.

This asymmetry same market opportunity, radically different opportunity costs—explains
why startups beat incumbents even when the incumbents see the threat clearly. Nokia's en-
gineers understood in 2010 that software was becoming the primary battleground for mobile
phones. The problem was not vision. It was that Nokia's decades of hardware expertise—
its accumulated $s$— made software look weak by comparison and made redeployment pro-
hibitively costly.

**Force 3: The caricature effect.** Success builds not only economic value and opera-
tional capability—it builds identity. We call this the *caricature effect*: the process by which
accumulated success in a domain narrows what an organization can credibly become, because
its identity has been shaped, reinforced, and ultimately constrained by that success.

The mechanism is illustrated by the trajectory of Amitabh Bachchan, the legendary
Bollywood actor. Early in his career, Bachchan was celebrated for his versatility. Then
a series of blockbuster films established his “angry young man” persona—a working-class
hero fighting injustice through action. The formula was enormously successful. Producers
demanded it. Audiences expected it. And so Bachchan became, in a sense, trapped by

[Page 6]
his own success: a brilliant, bankable caricature, but a caricature nonetheless. When he
attempted different roles, the audience resisted—they wanted the archetype, not the actor.

Organizations face an identical dynamic. When someone at Kodak proposed investing
seriously in digital photography, the response was not hostility—it was coherence: “That's
not who we are. We're a film company.” When Nokia engineers pushed for a software-
first strategy, the answer was not obtuse: “We make phones. Hardware is what we do.”
These responses are not pathological. They are attempts by rational agents to maintain
organizational coherence, to honor the implicit contracts with employees and partners who
built their careers around the firm's identity. But they impose a real economic cost: they
raise the effective hurdle rate for innovation by adding an identity-disruption premium to
the already-high opportunity cost of redeployment.

This mechanism connects to Mokyr's (2017) analysis of institutional prerequisites for
sustained technological progress. Mokyr shows that societies in which rigid social structures
lock people into predetermined roles—in which identity hierarchies constrain what individu-
als can credibly aspire to become—systematically under-produce innovation. The caricature
effect is the organizational analogue: rigid identity structures within firms lock resources and
attention into predetermined strategic roles, with the same consequences at the firm level
that rigid social structures produce at the societal level.

## The Medium-Term Trap

These three forces converge to produce what we call the medium-term trap. In the short
run, an incumbent's business is visibly thriving—stores are full, revenue is strong, margins
are healthy. In the long run, the incumbent may genuinely believe that the technology
will eventually make its model obsolete. But in the medium term, every economic incentive
pushes toward optimizing the existing business rather than cannibalizing it. High $\sigma^2$ in a new
market creates option value for a startup (pure upside from zero) while creating threat for
the incumbent (downside from a profitable baseline). High s in the existing business makes

[Page 7]
the new venture look inefficient by comparison. And the caricature effect makes internal
advocates for disruption politically costly to support.

Consider Blockbuster in 2000. Nine thousand stores worldwide, each requiring expensive
real estate in convenient locations. An $800 million annual late-fee revenue stream that was
not a side effect but a cornerstone of the business model. When Netflix proposed no late
fees as part of a subscription offering, they were not merely offering a customer perk—they
were attacking the foundation of Blockbuster's profitability. And they could do so precisely
because they carried none of Blockbuster's organization capital in physical retail, none of
its identity as a store-based brand, and faced pure upside in a world of high streaming
uncertainty. Blockbuster's failure was not a failure of intelligence. It was the medium-term
trap operating in its purest form.

# Contribution and Roadmap

Our paper provides formal microfoundations for the patterns that Schumpeter (1942), Aghion
and Howitt (1992), and the broader creative destruction literature have documented at the
macro level. The model is deliberately parsimonious—three dates, a random-walk market
signal, a discrete investment space—but it generates precise, signed predictions about which
firms innovate, at what scale, and how they respond to interim market signals, predictions
that are both formally derived and empirically testable.

Our paper connects to several streams of research. Within strategic management, we are
closest to the real-options strand pioneered by Bowman and Hurry (1993) and Kogut (1991),
and extended by McGrath (1999), who argues that real options reasoning helps explain the
productive role of entrepreneurial failure. Adner and Levinthal (2004) provide an important
corrective to over-application of the real options lens, noting that many putative options are
not in fact optional; our model respects this critique by ensuring that the discretion to aban-
don is a genuine choice with bite. March's (1991) exploration-exploitation framework is a
natural reference point; our model endogenizes the choice between exploration and exploita-

[Page 8]
tion as a function of observed market signals rather than treating it as an organizational
design variable. The incumbent failure literature─Henderson and Clark (1990) on archi-
tectural innovation, Tripsas and Gavetti (2000) on capabilities and cognition-emphasizes
firm-specific mechanisms; our contribution is to show that the aggregate pattern of incum-
bent non-innovation is consistent with rationality, without requiring any cognitive failure or
agency problem.

The most proximate antecedent in the finance literature is Bernardo and Chowdhry
(2002), who develop a real options model of corporate strategy in which firms learn about
the level of their resources- -general capabilities applicable across businesses and specific
capabilities tied to one business—by undertaking investments and observing their outcomes.
Their central result is a life-cycle prediction: firms specialize first (to learn about total
resources), then experiment in a general line of business (to disentangle specific from general
capabilities), then either expand into a multisegment firm (if general resources are high)
or scale up the specialized business (if general resources are low). Our model differs from
theirs in a fundamental way that is worth making explicit: Bernardo and Chowdhry study
learning about pre-existing resources -the firm discovers what it already has—whereas we
study the active accumulation of new organization capital through learning-by-doing. In their
framework, $\sigma^2$ measures uncertainty about an existing stock of capabilities; the information
is valuable because it guides where to deploy resources the firm already possesses. In our
framework, $s$ measures how rapidly the act of investing in a new business creates capabilities
that would not exist otherwise; the accumulation is valuable because it generates future rents
even when the market signal remains below the investment hurdle. The two mechanisms are
complementary: a complete theory of corporate innovation requires both the Bernardo and
Chowdhry channel (learn what you have) and our channel (build what you need). Crucially,
Bernardo and Chowdhry also show that firm value is increasing in resource uncertainty
$\sigma^2$ exactly paralleling our Proposition 4—but for a different reason: in their model higher
uncertainty means more to learn and therefore more valuable options to expand; in our model

[Page 9]
higher volatility $\sigma_0$ means a wider right tail for the market signal and therefore a higher expansion option value $H \cdot C(x_0, \sigma_0)$. A noteworthy contrast concerns signal noise. Bernardo and Chowdhry show that lower signal noise $\sigma_e$—sharper observations of cash flows—raises firm value by accelerating learning. In our model, the analogous object is the precision of the market signal $x_1$, which is not a choice variable; higher $\sigma_0$ raises value through the option channel rather than the learning channel. The two papers thus identify two distinct and additive sources of innovation option value.

The paper proceeds as follows. Section 2 presents the formal model. Section 3 states and proves the five propositions. Section 4 develops the typology of firm behaviors. Section 5 states six testable empirical predictions and connects them to existing evidence. Section 6 discusses contemporary applications and implications for organizational design. Proofs are collected in the Appendix.

# 2 The Model

## 2.1 Setup and Timeline

There are three dates, $t = 0, 1, 2$. We interpret them as the present, the short run, and the long run. At $t = 0$, the firm decides whether and how much to invest in a new business. At $t = 1$, the firm observes realized cash flows, learns the true intermediate-date market signal, and decides whether to expand, harvest, or abandon. At $t = 2$, long-run cash flows are realized and the firm is liquidated.

Let $x_t$ denote the publicly observed market signal at date $t$ about the business's cash flow at date $t + 1$. We model market signals as a random walk with zero drift:
$$
x_t = x_{t-1} + \varepsilon_t, \quad E_{t-1}[\varepsilon_t] = 0, \quad \text{Var}_{t-1}[\varepsilon_t] = \sigma_{\varepsilon_{t-1}}^2 \quad (1)
$$
The random walk implies that the best forecast of the future market signal is the current

[Page 10] [DIGITIZATION FAILED]


[Page 11]
Cash flow from operations at date $t$ is proportional to capital and the market signal:
$$
C_t = K_{t-1} x_t.
\tag{4}
$$
At date $t = 0$ the business is not yet operational, so $C_0 = 0$. Future cash flows are discounted at rate zero, justified by assuming a risk-free rate and market risk premium of zero; this normalization entails no loss of generality for the qualitative predictions.²

## 2.3 The Firm's Objective

The firm maximizes the present value of all cash flows. Starting at $t = 0$, firm value is:
$$
V_0 = -I_0 + E_0[V_1],
\tag{5}
$$
$$
V_1 = -I_1 + C_1 + E_1[C_2].
\tag{6}
$$
The firm also has a limited liability option: at date $t = 1$, it can choose to abandon the business, in which case it collects the current cash flow $C_1$ and carries no further obligations.

We impose one distributional assumption to obtain closed-form results.

**Assumption 1** (Gaussian signal shocks). $\varepsilon_1 \sim N(0, \sigma_0^2)$, so that $x_1 | x_0 \sim N(x_0, \sigma_0^2)$.

Let $\Phi(\cdot)$ and $\phi(\cdot)$ denote the standard normal cumulative distribution function and probability density function, respectively. Define:
$$
d \equiv \frac{x_0 - 1}{\sigma_0} < 0,
\tag{7}
$$
$$
C(x_0, \sigma_0) \equiv (x_0 - 1) \Phi(d) + \sigma_0 \phi(d),
\tag{8}
$$
$$
P(x_0, \sigma_0) \equiv \sigma_0 \phi(\frac{x_0}{\sigma_0}) - x_0 \Phi(-\frac{x_0}{\sigma_0}) \ge 0.
\tag{9}
$$

---
²Incorporating a positive discount rate would scale the option value term downward but would not change the sign of any comparative static.

[Page 12]
The quantity $C$ is the value of a European call option on the market signal $x_1$ with strike price one—the investment hurdle rate—and $P$ is the value of a put option on $x_1$ with strike price zero, capturing the value of limited liability (the option to abandon when $x_1 < 0$).

# 3 Analysis

We solve the model by backward induction, beginning at $t = 1$.

## 3.1 Optimal Policy at Date 1

At $t = 1$, the firm has observed $x_1$ and collected cash flow $C_1 = I_0 x_1$ (where $I_0$ is now sunk). It chooses $I_1 \in \{0, L, H\}$ and whether to abandon.

If the firm continues with investment $I_1$, value from $t = 1$ onward is:
$$
\begin{align}
V_1(I_1) &= -I_1 + C_1 + E_1[K_1x_2] \\
&= -I_1 + I_0x_1 + (I_1 + sI_0) x_1 \\
&= I_0(1 + s) x_1 + I_1(x_1 - 1). \tag{10}
\end{align}
$$
The marginal value of new investment $I_1$ is $(x_1 - 1)$: positive if and only if the observed market signal exceeds the investment hurdle rate.

If the firm abandons at $t = 1$ (setting $K_1 = 0$), it collects current cash flow and receives nothing at $t = 2$:
$$
V_1^{\text{abandon}} = C_1 = I_0 x_1. \tag{11}
$$

[Page 13]
**Lemma 1** (Optimal policy at date 1). *The firm's optimal decision at date 1 is:*
$$
(I_1^*, \text{action}^*) = \begin{cases}
(H, \text{expand}) & \text{if } x_1 > 1, \\
(0, \text{harvest}) & \text{if } 0 \le x_1 \le 1, \\
(\text{abandon}) & \text{if } x_1 < 0.
\end{cases}
\quad(12)
$$

*The associated values are:*
$$
V_1^* = \begin{cases}
I_0(1+s)x_1 + H(x_1-1) & \text{if } x_1 > 1, \\
I_0(1+s)x_1 & \text{if } 0 \le x_1 \le 1, \\
I_0 x_1 & \text{if } x_1 < 0.
\end{cases}
\quad(13)
$$

*Proof.* See Appendix A.
$\square$

Lemma 1 partitions the signal space into three qualitatively distinct firm behaviors.

**Expansion** ($x_1 > 1$). The market signal exceeds the investment hurdle, so each dollar of new investment earns a positive return ($x_1 - 1) > 0$. The firm pours in as much capital as possible, choosing $I_1 = H$. Organization capital amplifies returns: total capital is $K_1 = H + sI_0$, so prior investment at date 0 generates a compounding dividend in the expansion regime.

**Harvest** ($0 \le x_1 \le 1$). The market signal is positive but below the hurdle rate, so new investment earns a negative marginal return. The firm sets $I_1 = 0$ and continues operating solely on the organization capital $sI_0$ it built at date 0. This is the “cash cow” phase: no new investment, but positive expected cash flows from accumulated capabilities. The firm earns rents on its organization capital as long as $sx_1 > 0$, which holds in this region.

**Abandonment** ($x_1 < 0$). The market signal is negative, implying that even carrying forward the organization capital $sI_0$ creates negative expected value. The firm exercises its limited-liability option by setting $K_1 = 0$, absorbing the date-1 loss $I_0x_1$ and walking away.

[Page 14]
*Remark 1.* The three-region structure of Lemma 1 maps directly onto March's (1991) distinction between exploration and exploitation. Expansion corresponds to renewed exploration; harvest corresponds to exploitation of existing capabilities; abandonment corresponds to strategic exit. The model endogenizes the choice among these three modes as a function of the observed market signal.

## 3.2 Firm Value at Date 0
Taking expectations of $V_1^*$ under Assumption 1, we obtain a closed-form expression for firm value at date 0.

**Proposition 1** (*Firm value at date 0*). *Under Assumption 1, the value of the firm at date 0, given investment $I_0 > 0$, is:*
$$
V_0 = I_0 \underbrace{[(1 + s) x_0 + s \mathcal{P}(x_0, \sigma_0) - 1]}_{\text{current-signals component}} + \underbrace{H \cdot C(x_0, \sigma_0)}_{\text{expansion option}},
\quad (14)
$$
*where $C$ and $\mathcal{P}$ are defined in equations (8) and (9), respectively.*

*Proof.* See Appendix A.
$\tag*{$\Box$}$

Equation (14) has a clean interpretation. The first term, the current-signals component, captures the expected value of the project if the firm could only harvest its organization capital and benefit from the limited-liability option—but could not expand at date 1. Because $x_0 < 1$, this term is negative when $s$ and $\mathcal{P}$ are small, confirming the project's negative NPV on current signals. The second term, the expansion option $H \cdot C(x_0, \sigma_0)$, is always positive: it is the expected profit from the option to scale up to $I_1 = H$ when $x_1 > 1$, multiplied by the maximum scale $H$.

The expansion option $C(x_0, \sigma_0)$ has the structure of a Black-Scholes call option: the current market signal $x_0$ plays the role of the underlying asset price, the investment hurdle

[Page 15]
rate 1 plays the role of the strike price, and $\sigma_0$ plays the role of volatility.³ This means that all of the intuitions from options theory apply directly. Most importantly, higher volatility increases the option value because it widens the right tail without affecting the bounded downside.

*Remark 2.* When $x_0/\sigma_0$ is large—equivalently, when the probability that $x_1 < 0$ is negligible— the put component $P$ vanishes and (14) simplifies to:
$$
V_0 \approx I_0 [(1 + s) x_0 - 1] + H \cdot C(x_0, \sigma_0). \quad (15)
$$
This simplified form is used in the comparative statics below. The full form with $P$ is required when $x_0$ is close to zero or when $\sigma_0$ is very large.

*Remark 3* (Connection to Bernardo and Chowdhry (2002)). The decomposition in equation (14) allows a precise comparison with the real options framework of Bernardo and Chowdhry (2002), who model firms as learning about pre-existing general resources $G$ (applicable across businesses) and specific resources $S$ (tied to one business) by observing investment outcomes. In their model, firm value is also increasing in resource uncertainty $\sigma^2$, for a reason that is structurally analogous to but economically distinct from ours. In Bernardo and Chowdhry, higher $\sigma^2$ means more to learn about what the firm already has: greater uncertainty about $G$ expands the option value of continued experimentation and raises the critical threshold $Z_H$ at which the firm optimally commits to multisegment expansion. In our model, higher $\sigma_0$ means a wider distribution of future market outcomes: it expands the right tail of $x_1$, increasing the expected payoff from the expansion option $H \cdot C(x_0, \sigma_0) = H [(x_0 - 1)\Phi(d) + \sigma_0\phi(d)]$ through the $\sigma_0\phi(d)$ term.

A further connection: Bernardo and Chowdhry's parameter $K_G$ (the scale multiplier for the multisegment business) is the analogue of our $H$. Both papers predict that the option value, and hence the willingness to absorb first-period losses, is increasing in the potential

---
³The analogy is not perfect because $x_1$ is normally (not log-normally) distributed, but the pricing formula is structurally identical.

[Page 16]
scale of second-stage expansion ($\partial V_0 / \partial H > 0$ here; $\partial V / \partial K_G > 0$ in their Fig. 5). Their parameter $K_S$ (scale of the specialized business) has no direct analogue in our model because we do not distinguish between specialization and generalization at date 1; instead, both the harvest and the expansion outcome in our framework involve the same business. Introducing a $K_S$-style distinction—a specialized scale-up versus a general-market expansion—would be a natural bridge between the two frameworks.

The sharpest contrast concerns signal noise. Bernardo and Chowdhry show that lower observation noise $\sigma_\epsilon$ raises firm value because it accelerates learning, allowing the firm to make the irreversible expansion decision sooner and with greater confidence. In our model, $\sigma_0$—which is closer to Bernardo and Chowdhry’s resource uncertainty $\sigma$ than to their noise $\sigma_\epsilon$—raises value through the option channel, not the learning channel. The two mechanisms are therefore additive: a firm benefits both from high underlying uncertainty (our $\sigma_0$, their $\sigma$) and from low observation noise (their $\sigma_\epsilon$), but through entirely separate routes.

## 3.3 The Innovation Decision

**Proposition 2** (*Innovation threshold*). A firm invests $I_0 > 0$ in a new business if and only if
$$
H \cdot C(x_0, \sigma_0) > I_0 [1 - (1+s) x_0 - s P(x_0, \sigma_0)]. \quad (16)
$$

The left-hand side is the expansion option value; the right-hand side is the first-period loss net of the harvest option. Under the approximation of Remark 2, this simplifies to:
$$
H \cdot C(x_0, \sigma_0) > I_0 [1 - (1+s) x_0]. \quad (17)
$$

*Proof.* Since $V_0(I_0 = 0) = 0$ and $V_0$ is linear in $I_0$, the firm invests if and only if $V_0 > 0$ for some $I_0 > 0$, which yields (16) directly from (14). $\Box$

Condition (17) has a natural economic interpretation: the firm absorbs a certain first-

[Page 17]
period loss in exchange for an uncertain but potentially large second-period gain. The option value is larger when (i) the expansion scale $H$ is large, (ii) the volatility $\sigma_0$ is high, or (iii) the current signal $x_0$ is not too far below the hurdle rate. The loss is smaller when learning intensity $s$ is high, because the firm recovers more from organization capital even in the harvest regime.

This condition directly captures why some firms innovate and others do not. Two firms facing the same current market signal $x_0$ may make different innovation decisions if they differ in $H$ (their ability to scale), $s$ (their learning intensity in the new business), or $\sigma_0$ (their assessment of market signal volatility).

## 3.4 The Initial Scale Decision

Among firms that choose to innovate ($I_0 > 0$), how much should they invest initially?

**Proposition 3** (Initial scale choice). Among firms that invest at date 0, the firm prefers $I_0 = H$ to $I_0 = L$ if and only if
$$
(1+s) x_0 + s P(x_0, \sigma_0) > 1, \quad (18)
$$
or equivalently (under Remark 2),
$$
x_0 > \frac{1}{1+s}. \quad (19)
$$

**Proof.** From (14), $V_0(I_0 = H) – V_0(I_0 = L) = (H – L) [(1 + s)x_0 + sP – 1]$. Since $H > L$, the sign is determined by (18). □

Proposition 3 has a striking implication: the initial scale decision is entirely determined by the current-signals component; the expansion option value $H \cdot C$ is the same regardless of $I_0$.

The threshold $x_0 > 1/(1 + s)$ is decreasing in $s$: firms with higher learning intensity optimally enter at larger initial scale. Intuitively, a higher $s$ means more organization cap-

[Page 18]
ital is built per dollar of initial investment, making the date-0 investment more productive regardless of the date-1 signal realization. A firm with $s = 0$ (no learning) would never find it optimal to invest $I_0 = H$ when $x_0 < 1$, because the current-signals component is strictly negative in that case. But a firm with large $s$ may find it worth sustaining a larger first-period loss to build a larger platform for future operations.

**Corollary 3.1.** As $s \to \infty$, the threshold $x_0 > 1/(1+s)$ approaches zero: any firm with a positive current market signal will enter at maximum initial scale. As $s \to 0$, the threshold approaches one, and no firm with $x_0 < 1$ enters at maximum scale.

## 3.5 Comparative Statics

**Proposition 4** (Comparative statics). Under Assumption 1 and the approximation of Remark 2:
$$
\frac{\partial V_0}{\partial \sigma_0} = H \cdot \phi(d) > 0, \quad (20)
$$
$$
\frac{\partial V_0}{\partial s} = I_0 x_0 > 0, \quad (21)
$$
$$
\frac{\partial V_0}{\partial H} = C(x_0, \sigma_0) > 0, \quad (22)
$$
$$
\frac{\partial V_0}{\partial x_0} = I_0(1+s) + H \Phi(d) > 0. \quad (23)
$$

Furthermore, $\sigma_0$ and $I_0$ are complementary in $V_0$: $\partial^2 V_0 / \partial \sigma_0 \partial I_0 = 0$ (the expansion option does not depend on $I_0$), but $\partial^2 V_0 / \partial s \partial I_0 = x_0 > 0$ (learning intensity and initial investment are complementary).

*Proof.* See Appendix A. $\quad \square$

Each result in Proposition 4 has a direct managerial and theoretical interpretation.

**Volatility** ($\partial V_0 / \partial \sigma_0 > 0$). Higher market signal volatility unambiguously raises firm value. This is the option theoretic insight applied to corporate strategy: risk is not the enemy of innovative investment—it is its friend. A firm that is uncertain about where the market is

[Page 19]
heading benefits from that uncertainty, because the expansion option allows it to profit from
upside realizations while limiting its losses on downside realizations through abandonment.
The magnitude of the effect, $H\Phi(d)$, is proportional to the maximum expansion scale $H$ and
to the option's gamma (the density at the strike).

**Learning intensity** ($\partial V_0 / \partial s > 0$). A higher learning-by-doing parameter $s$ raises firm
value by increasing the productivity of initial investment. The complementarity $\partial^2 V_0 / \partial s \partial I_0 =
x_0 > 0$ implies that firms in industries with steeper learning curves should invest more ag-
gressively at the initial date. This connects to the empirical finding that industries with
rapid learning (semiconductors, biotech, renewable energy) exhibit large initial capital com-
mitments by early entrants (Pisano, 1994).

**Expansion capacity** ($\partial V_0 / \partial H > 0$). Firm value increases in the maximum second-
stage investment scale. This result identifies an often-overlooked dimension of competitive
advantage: the ability to *rapidly scale up* conditional on a good market signal is itself
valuable, even before any scaling occurs. Firms that have secured large-scale production
capacity, distribution networks, or regulatory approval in advance are therefore holding an
option worth $C(x_0, \sigma_0)$ per unit of pre-committed scale.

**Current market signal** ($\partial V_0 / \partial x_0 > 0$). Firm value is increasing in the current market
signal. The effect has two components: a direct effect $I_0(1 + s)$ from higher current and
harvest-period cash flows, and an indirect effect $H\Phi(d)$ from the expansion option becoming
more in-the-money as $x_0$ approaches the strike of 1. Note that $\Phi(d) < 1/2$ when $x_0 < 1$, so
the option delta is below one-half. This means that a unit increase in $x_0$ raises the value
of new investment less than it raises the expected value of existing operations, a result that
has direct implications for how firms should prioritize scale-up versus new entry.

[Page 20]
# 3.6 The Incumbent Trap: Organizational Analogues of Mokyr's Institutional Prerequisites

The model contains the seeds of an explanation for a canonical strategic management puzzle: why do successful incumbent firms systematically under-invest in new markets that ultimately displace their core businesses?

Consider two types of firms facing the same new market opportunity with parameters $(x_0, \sigma_0, s_{new})$, where $s_{new}$ is the learning intensity specific to the new market.

**Startups** are firms with no operations in related markets. Their opportunity cost of investing $I_0$ in the new business is zero. Their innovation threshold is given directly by Proposition 2.

**Incumbents** are firms with substantial operations in an existing market, in which they have accumulated organization capital $s_{ex|ex}$ at $s_{ex} \gg s_{new}$. An incumbent that reallocates resources from the existing business to the new business bears an opportunity cost equal to the forgone harvest value of its existing organization capital. Denoting this opportunity cost by $\Delta_{opp} > 0$, the incumbent's effective innovation threshold becomes:
$$
H \cdot C(x_0, \sigma_0) > I_0[1 - (1 + s_{new})x_0] + \Delta_{opp}. \quad (24)
$$
Comparing (24) with (17), the incumbent requires a strictly higher option value to innovate. This is the *incumbent trap*: the very organization capital that makes an incumbent firm valuable in its existing business raises the bar for entry into new markets.

**Remark 4.** The incumbent trap requires no managerial myopia, agency problems, or organizational inertia. It is a consequence of rational opportunity cost accounting, and it matches the central prediction of Aghion and Howitt (1992): incumbents will rationally resist creative destruction even when they understand its long-run inevitability. The implication for corporate governance is that boards evaluating incumbent innovation proposals should apply a lower hurdle rate than a startup would apply, precisely because the incumbent's

[Page 21]
opportunity cost is higher—proposals that a startup would reject on NPV grounds may still
be value-creating for an incumbent because the alternative is to concede the new market
entirely.

## Mokyr's Prerequisites at the Organizational Level

Mokyr (2017) identifies three institutional prerequisites that determine whether creative
destruction can operate at the societal level. Each has a precise organizational analogue
that follows from our model.

**Prerequisite 1: Intellectual property rights that balance incentives with dif-
fusion.** At the societal level, rights that are too weak prevent innovators from capturing
value; rights that are too strong lock up knowledge and prevent cumulative recombination.
At the organizational level, the analogue is the firm's *internal incentive design* for innova-
tion. Compensation systems that tie innovation leaders entirely to current profitability (too
weak) fail to reward the option value being created; but systems that reward innovation
leaders so generously that they have no incentive to deliver near-term results (too strong)
fail to align innovation investment with business needs. The optimal design—consistent with
real options logic—compensates innovation leaders on a blend of learning-progress metrics
and long-run outcome measures, with explicit recognition that negative current NPV is not
evidence of failure.

**Prerequisite 2: Genuinely competitive internal markets that prevent domi-
nant projects from blocking new technologies.** Mokyr shows that when incumbent
industries can leverage monopoly power or regulatory capture to block new entrants, techno-
logical progress stalls. The organizational analogue is the internal capital allocation process.
When the core business—generating strong current cash flows--can claim unlimited resources
at the expense of exploratory businesses, internal creative destruction is suppressed. Chris-
tensen (1997) documents this mechanism in detail; our model formalizes why it happens:
the core business's current-signals component is always positive (since it operates above the

[Page 22]
hurdle rate), while the exploratory business’s current-signals component is negative (since $x_0 < 1$). Any resource allocation process that weights current NPV will systematically disadvantage innovation. The solution—creating separate profit-and-loss units with their own resource pools—is the organizational equivalent of Mokyr’s competitive market condition. Amazon’s decision to build AWS as a separate business unit reporting directly to the CEO, insulated from the retail organization’s capital allocation process, exemplifies this design.

**Prerequisite 3: Social mobility that allows talented people to pursue new ideas regardless of position in existing hierarchies.** At the societal level, when rigid social structures trap people in predetermined roles, potential innovation never happens. At the organizational level, the caricature effect creates an analogous trap: the firm’s identity constraints determine who can credibly advocate for what. In a firm whose identity has hardened around a core technology—Kodak as a film company, Nokia as a hardware maker—individuals who advocate for identity-disrupting innovations face not just resource competition but social sanctioning. The formal mechanism is that the caricature effect adds an implicit cost $\delta_{\text{caricature}} > 0$ to the incumbent trap condition (24), tightening the innovation threshold further. Organizational interventions that reduce this cost—creating explicit permission for internal disruption, rewarding advocates for new ideas irrespective of seniority—are the organizational equivalent of Mokyr’s social mobility prerequisite.

# 4 A Typology of Firm Behaviors

Proposition 2 implies that whether a firm innovates depends on the interplay of three parameters: the volatility of market signals ($\sigma_o$), the learning intensity ($s$), and the realized intermediate-date market signal ($x_1$). Crossing high and low values of each—eight cells in all—generates a typology that encompasses the full range of firm behaviors observed in practice. Table 1 presents the typology; we discuss each archetype in turn.

Cell 1 (*Moonshot*). High volatility, high learning, favorable signal. The firm enters

[Page 23]
Table 1: A Typology of Firm Behaviors

| Cell | $\sigma_0$ | $s$ | $x_1$ | $I_0/I_1$ | Archetype | Exemplars |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | H | H | H | H / H | Moonshot | Amazon AWS; Apple iPhone |
| 2 | H | H | L | H / 0 | Costly Pivot | Google Glass; Apple Newton |
| 3 | H | L | H | L / H | Lean Scaler | Classic VC-backed startups |
| 4 | H | L | L | L / 0 | Cheap Failure | Most failed startups |
| 5 | L | H | H | H / H | Incumbent Expander | Toyota Kaizen; TSMC capacity |
| 6 | L | H | L | H / 0 | Cash Cow | Kodak film; Nokia feature phones |
| 7 | L | L | H | 0 / – | Missed Bet | Blockbuster; Kodak digital |
| 8 | L | L | L | 0 / – | Rational Non-entry | Established firms in stable markets |

H/L = High/Low. Cell 7 did not invest at t = 0; the signal realization is counterfactual. Exemplars are illustrative; see tex

at full scale ($I_0 = H$) because the learning intensity justifies a large initial platform, and expands further at date 1 ($I_1 = H$) because the market signal is strong. The organization capital built at date 0 generates compounding returns in the expansion regime: total capital at date 2 is $(1+s)H$, much larger than $H$ alone. Amazon's investment in AWS is a canonical example: the initial infrastructure investment was enormous and negative NPV on current signals, but the learning-by-doing in cloud operations was rapid and highly specific, and the expansion at date 1 was aggressive.

**Cell 2 (Costly Pivot)**. High volatility, high learning, unfavorable signal. The firm entered at full scale on the strength of option value, but the market signal turns out weak. It does not expand ($I_1 = 0$), but harvests the organization capital it has built. Google Glass belongs here: the option value of AR wearables was real, the learning in miniaturized computing was genuine, but the market signal at date 1—consumer rejection—was unambiguous. What distinguishes this cell from failure is the harvest: Google's learning in wearable hard-

[Page 24]
ware was not wasted; it fed into subsequent products and the broader ambient computing
strategy.

**Cell 3 (Lean Scaler).** High volatility, low learning, favorable signal. The firm enters
small ($I_0 = L$) because with low learning intensity there is no benefit to a large initial
platform, and scales aggressively when the signal is confirmed ($I_1 = H$). This is the canonical
venture-capital playbook: a lean initial bet followed by aggressive scale-up conditional on
product-market fit. The model predicts that this firm type is most prevalent in markets
with high volatility (consumer tech, software, biotech) but low initial organization-capital
intensity.

**Cell 4 (Cheap Failure).** High volatility, low learning, unfavorable signal. The firm
entered small, the signal was bad, it exits quickly. This is the healthy entrepreneurial
ecosystem outcome: failures are fast and cheap, capital is redeployed, and the economy
learns quickly which directions are not worth pursuing. McGrath (1999) argues persuasively
that the ability to generate cheap failures is itself a source of competitive advantage at the
portfolio level.

**Cell 5 (Incumbent Expander).** Low volatility, high learning, favorable signal. The
firm enters large because learning intensity is high and the current signal, while below the
hurdle rate, is not far below it. When the signal is confirmed, it expands further. This is the
pattern of firms in industries with steep learning curves and predictable demand: TSMC's
capital investment programs, Toyota's kaizen-driven capacity expansion, and ASML's gen-
erational investments in lithography.

**Cell 6 (Cash Cow).** Low volatility, high learning, unfavorable signal. This is the most
consequential cell for the strategy literature. The firm entered at large scale, built enormous
organization capital, and now faces a market signal below the hurdle rate for new investment.
It neither expands nor exits; it harvests. Kodak's film business fits here precisely. Kodak
had massive organization capital in film chemistry, photo labs, and retail distribution. When
digital photography produced a weak signal (low consumer adoption, uncertain quality, high

[Page 25]
cost), Kodak's rational response was not to abandon film but to harvest it—which it did for
two decades. The problem was not irrationality; it was that the harvest regime is absorbing:
the longer a firm harvests, the more its organization capital becomes locked to the obsolete
technology.

**Cell 7 (Missed Bet).** Low volatility, low learning: the firm correctly chose not to invest
at date 0 because the option value was insufficient. But the signal turns out favorable. From
the outside, this looks like a strategic error. From the model, it is a rational response to
ex-ante parameters. Blockbuster falls here. In 2007, the volatility of the streaming market
was real, but Blockbuster lacked the organizational platform (low $s$ for digital distribution)
to exploit it, and the option value of a small streaming bet did not clear the hurdle given
the opportunity cost of its retail infrastructure.

**Cell 8 (Rational Non-Entry).** Low volatility, low learning, unfavorable signal. The
firm correctly chose not to invest, and it was right. Most incumbent non-innovation in
stable industries falls here. The model predicts that observers who label all non-innovation
as “incumbent failure” are systematically over-diagnosing pathology: Cell 8 non-innovators
should be celebrated, not criticized.

**The Innovation Paradox.** Cells 1 and 2 appear identical at date 0: both firms invested
at full scale in a negative-NPV project. Only the realization of $x_1$ distinguishes them. The
model predicts that we cannot, at date 0, identify whether an innovative investment is a
Moonshot or a Costly Pivot—and that we should not penalize managers for investments
that turn out to be Cell 2 if the ex-ante parameters (high $\sigma_0$, high $s$) justified the bet.
This has direct implications for the design of managerial incentive contracts and innovation
governance.

[Page 26]
# 5 Empirical Predictions and Evidence

We derive five testable predictions from the model and discuss existing empirical evidence that is consistent with each.

**Prediction 1: Volatility and innovation investment.** *Firms operating in higher-volatility market environments invest more in exploratory innovation, conditional on current market signals.*

From Proposition 4, $\partial V_0 / \partial \sigma_0 = H\phi(d) > 0$, so higher volatility raises the value of innovation investment. The empirical prediction is that, among firms with similar current financial performance ($x_0$), those in higher-volatility industries should exhibit greater R&D and innovation expenditure. This prediction is consistent with the large literature on uncertainty and investment (Dixit and Pindyck, 1994), but our model specifies that the effect should be strongest for firms with high $H$ (large scalable operations) and should be non-monotone in $x_0$ (strongest for firms not too far below the investment hurdle). Bloom, Bond, and Van Reenen (2007) provide evidence that uncertainty raises investment in productive activities and reduces investment in routine maintenance; the mechanisms are consistent with ours.

**Prediction 2: Learning intensity and initial scale.** *Firms in industries with steeper learning curves enter new markets at larger initial scale.*

From Proposition 3, the threshold $x_0 > 1/(1+s)$ is decreasing in $s$: industries with faster learning should exhibit larger initial investments by entrants. A testable implication is that average deal size in venture capital financing should be increasing in the learning-curve steepness of the industry, measured as the rate of cost reduction per unit of cumulative output. Pisano (1994)’s study of learning dynamics in pharmaceutical manufacturing provides direct evidence consistent with this prediction: firms with stronger learning trajectories invested more heavily upfront in plant capacity.

[Page 27]
Prediction 3: The harvest regime and “zombie” firms. Firms with high learning
intensity in their existing businesses are more likely to persist in a harvest regime rather than
exiting cleanly when the market signal weakens.

Lemma 1 predicts a harvest regime ($0 \le x_1 \le 1$) in which firms continue operating
without new investment. The duration of this regime is increasing in s, because higher
organization capital generates positive operating rents even when new investment would be
value-destroying. A testable implication is that “zombie firms" —those that neither exit nor
grow—should be concentrated in industries with high organization-capital intensity. This
prediction is consistent with evidence on exit dynamics in capital- intensive industries (Nelson
and Winter, 1982): industries with high sunk costs and specific assets exhibit persistently
low exit rates even when measured profitability is below cost of capital.

Prediction 4: Conditional performance and volatility versus learning. Among
firms that invested in a new business at date 0, subsequent scale-up ($I_1 = H$) is uncorre-
lated with initial investment size when $\sigma_0$ is the primary driver of innovation, but positively
correlated when s is the primary driver.

When the innovation decision is driven by high $\sigma_0$, all innovating firms enter small ($I_0 =
L$, from Proposition 3, since $x_0 < 1/(1 + s)$ for low s) and scale up only upon observing
a favorable signal. When the innovation decision is driven by high s, firms enter large
($I_0 = H$) and continue expanding when the signal is favorable. This distinction implies that
the distribution of outcomes—measured as (initial investment, subsequent scale-up) pairs—
should exhibit a bimodal pattern in high-$\sigma_0$ industries (small then large or small then exit)
and a more concentrated large-large/large-exit pattern in high-s industries. This prediction
can be tested using investment trajectory data from industries classified by R&D intensity
(a proxy for $\sigma_0$) versus production learning-curve steepness (a proxy for s).

Prediction 5: Incumbent versus startup innovation patterns. When incumbents
do innovate in new markets, they should tend to enter at larger initial scale and exit less

[Page 28]
quickly than startups in the same market.

From Proposition 3, firms with higher $s$ (or higher $x_0$, because incumbents typically have stronger baseline signals from adjacent market experience) prefer larger initial investments. And from Lemma 1, firms with higher $s$ persist longer in the harvest regime. Both predictions run counter to the common narrative—that incumbents are slow to enter and quick to abandon—and instead predict that when incumbents do commit, they commit heavily and persist. Consistent with this, Henderson and Clark (1990) document that established firms in architectural transitions that did invest tended to do so at large scale; their undoing was not small bets that failed but large bets in the wrong architectural direction.

**Prediction 6: Creative destruction blocking and delay.** The duration of incumbent resistance to a new technology is increasing in $s_{ex}$ (existing organization capital) and decreasing in $\sigma_0$ (volatility of the new market’s signals); incumbents in higher-$\sigma_0$ markets face a shorter window of rational delay before competitive pressure makes resistance untenable.

This prediction extends Aghion and Howitt (1992)’s macro result—that incumbents rationally block creative destruction—to the cross-sectional variation in blocking duration. Incumbents with large accumulated organization capital in their existing businesses (high $s_{ex}$) bear a larger $\Delta_{opp}$ and therefore require a higher option value to innovate, sustaining rational resistance for longer. But high $\sigma_o$ in the new market causes the expansion option $H \cdot C(x_0, \sigma_0)$ to grow rapidly, eventually crossing the incumbent’s threshold. Empirically, this predicts that technology transitions in high-volatility markets (software, biotechnology, AI) should exhibit shorter incumbent blocking episodes than transitions in low-volatility markets (automotive, energy), where the new technology’s signal uncertainty is resolved slowly. Evidence consistent with this prediction appears in the contrast between Nokia’s protracted resistance (spanning nearly a decade in a moderate- volatility market) and the rapid displacement of established search companies by AI-native challengers in a high-volatility market.

[Page 29]
# 6 Discussion and Conclusion

This paper develops a tractable model of corporate innovation that integrates real options theory with Arrow's learning-by-doing framework, and positions both within the broader context of Schumpeter's creative destruction and Aghion and Howitt's formalization of it. The model is deliberately parsimonious—three dates, a random walk market signal, a discrete investment space—but generates a rich set of predictions about which firms innovate, how aggressively they invest, and how they respond to interim market signals.

The central contribution is analytical: by solving the model in closed form, we obtain clean comparative statics and threshold conditions that can be mapped to empirical tests. Most models of innovation are either qualitative (case studies of incumbents and disruptors) or econometric (reduced-form regressions of R&D on firm characteristics); we provide the formal intermediate layer—a model parsimonious enough to be solved and rich enough to generate the pattern of facts that both literatures have documented.

## 6.1 Contemporary Applications

The three forces—market uncertainty, organization capital, and the caricature effect—are not historical curiosities. They are operating in three technology transitions of immediate consequence.

**Artificial intelligence.** Established technology companies face the medium-term trap in its most acute modern form. Their current businesses generate prodigious cash flows: cloud computing, advertising, enterprise software. But large language models threaten each revenue stream simultaneously. In our framework, the $\sigma^2$ of AI market signals is extremely high: multiple model architectures may dominate, customer adoption trajectories are uncertain, and regulatory environments across jurisdictions are in flux. This high volatility creates large option values for AI-native startups (pure upside, no revenue to cannibalize, no $s_{ex}$ to protect) while creating threat for established firms whose high-$x_0$ baselines make new-market

[Page 30]
cannibalization costly. Prediction 6 implies that the high $\sigma^2$ of AI should produce a short blocking window, and indeed we observe rapid displacement dynamics in search and coding tools that contrast sharply with the decade-long resistance Nokia mounted in smartphones.

**Electric vehicles and the organization-capital trap.** Traditional automakers have built a century of organization capital in internal combustion engines: design, fuel system optimization, complex powertrain supply chains. When Toyota or General Motors evaluate EV investments, they compete against their own expertise in a technology that EVs render irrelevant. Tesla had no engine organization capital to protect; it could commit entirely to electric drivetrains—high $\sigma_o$ in the early 2010s, zero $s_{ex}$, high $s_{new}$ in battery systems. Proposition 3 predicts Tesla should enter at large scale ($x_o > 1/(1+s_{new})$ was satisfied in the premium segment), which it did, making large initial bets on manufacturing and technology infrastructure rather than following a lean-scaler strategy.

The societal stakes extend beyond corporate competition. Transportation accounts for approximately 25 percent of global greenhouse gas emissions. Understanding the economic forces that slow the EV transition—incumbent resistance driven by rational opportunity cost of redeploying combustion-engine organization capital—is essential for designing policies that accelerate adoption. Carbon pricing and EV subsidies function, in our framework, by raising $x_o$ for EV investments toward the incumbent's effective hurdle rate.

**Biotechnology and negative-NPV miracles.** When Moderna and BioNTech invested in mRNA technology through the 2010s, the current-signals component of firm value was substantially negative: no approved drug had used the platform, clinical trial success rates were well below established modalities, and manufacturing scale-up was unproven. Established pharmaceutical companies, operating with high $s_{ex}$ in traditional drug development and correspondingly large $\Delta_{opp}$, looked at mRNA and rationally declined. Biotechnology startups faced $s_{ex} = 0$ and hence no opportunity cost; the expansion option $H \cdot C(x_o, \sigma_o)$ cleared the hurdle for them even though it could not clear it for incumbents.

The human welfare consequences are measurable. mRNA vaccines were developed in

[Page 31]
under twelve months upon the COVID-19 emergency—a timeline impossible with established
modalities. The economic and mortality costs averted by that speed are measured in trillions
of dollars and millions of statistical lives. This is Mokyr (2017)’s argument made concrete
at the firm level: societies—and the organizations within them—that permit resources to
flow toward high-volatility, negative-current-NPV innovations realize sustained welfare gains
that dwarf the displacement costs borne by legacy modalities.

## 6.2 Implications for Organizational Design

The model’s managerial implications translate Mokyr’s three prerequisites into actionable
organizational interventions.

**Separate pockets** (the competitive-markets prerequisite). Create profit-and-loss units
with independent resource pools, insulated from competition with the core business on cur-
rent NPV. Amazon’s AWS, built as a separate business unit reporting directly to the CEO
and shielded from the retail organization’s capital allocation process, exemplifies this design.

**Real-options incentive design** (the IP rights prerequisite). Compensate innovation
leaders on learning-progress metrics and long-run option-value creation, not quarterly prof-
itability. An explicit recognition that negative current NPV is not evidence of failure— but
rather an expected feature of the expansion-option regime—is a prerequisite for sustaining
innovation investment through the medium-term trap.

**Permeable identity hierarchies** (the social mobility prerequisite). The caricature ef-
fect adds $\delta_{\text{caricature}} > 0$ to the incumbent trap threshold, raising the effective hurdle rate for
internal disruption advocates. Organizational interventions that create explicit permission
for identity- disrupting advocacy─career protections for innovation champions, leadership
behaviors that model strategic flexibility-reduce $\delta_{\text{caricature}}$ directly. Grove’s (1996) “con-
structive confrontation” culture at Intel exemplifies this: it created organizational permission
to raise existential concerns without career penalty, allowing the strategic pivot from mem-
ory chips to microprocessors to be executed from within rather than imposed by competitive

[Page 32]
crisis.

## 6.3 Extensions and Limitations

*Competitive dynamics.* The model is in partial equilibrium. A richer model would endogenize the market signal through competitive interaction, generating the preemption dynamics studied by Reinganum (1983) and Gilbert and Newbery (1982).

*Two-business formalization of the incumbent trap and resource types.* A two-business extension—allocating a fixed resource pool between an existing business (high $s_{ex}$) and a new business (high $\sigma_0$, low $s_{new}$)—would formalize both $\Delta_{opp}$ and $\delta_{caricature}$ as endogenous functions of accumulated organization capital. Such an extension would also allow direct integration of the Bernardo and Chowdhry (2002) resource-type distinction: in their framework, a firm that has established its specialized business ($K_S$ scaling complete) and is now experimenting with a general project is facing exactly the two-business allocation problem we describe here. The key difference is that Bernardo and Chowdhry take the resource stock as given and study its discovery, while our extension would model the simultaneous accumulation of new organization capital and the forgone harvest of the existing stock—combining the two channels into a single, richer framework.

*Continuous investment.* The discrete space $\{0, L, H\}$ restricts the scale decision to a binary choice; a continuous space would yield interior optima at the cost of closed-form tractability.

Despite these limitations, the core insight is robust: the risk-return tradeoff is inverted for innovative investments. Uncertainty is not the enemy of innovation—it is the precondition for the option value that makes innovation worthwhile. The question is not whether creative destruction will reach any given industry—Aghion and Howitt (1992) and economic history confirm that it will. The real question is whether a firm will be a victim of that destruction or an active agent of it. Our model shows that the answer depends on three parameters that are, at least partially, within the firm’s control: the volatility of market signals it chooses

[Page 33]
to face, the learning intensity it builds in new domains, and the rigidity of the identity it permits itself to accumulate. Getting these parameters right is not merely a matter of corporate strategy. It is, as Mokyr (2017) demonstrates across centuries of economic history, a matter of whether the institutional structures that govern resource allocation—at the firm level as at the societal level—are capable of permitting the creative destruction that has driven every major improvement in human welfare throughout recorded history.

# A Proofs

*Proof of Lemma 1.* **Step 1: Optimal $I_1$ given that the firm continues.**

From equation (10), $V_1(I_1) = I_0(1 + s)x_1 + I_1(x_1 - 1)$. The term $I_0(1 + s)x_1$ does not depend on $I_1$, so the marginal value of investment is $(x_1 - 1)$. Since $I_1 \in \{0, L, H\}$:

*   If $x_1 > 1$: $(x_1 - 1) > 0$, so $V_1$ is maximized at $I_1 = H$.
*   If $x_1 \le 1$: $(x_1 - 1) \le 0$, so $V_1$ is maximized at $I_1 = 0$.

**Step 2: Continue versus abandon.**

Given the optimal $I_1^*$, compare continuation value with the abandonment value $V_1^{\text{abandon}} = I_0x_1$.

*Case $x_1 > 1$*: $V_1(I_1 = H) = I_0(1+s)x_1 + H(x_1 - 1) > I_0x_1$ since both $s > 0$, $x_1 > 0$, and $H(x_1 - 1) > 0$. Continuation dominates.

*Case $0 \le x_1 \le 1$*: $V_1(I_1 = 0) = I_0(1 + s)x_1 \ge I_0x_1$ since $s \ge 0$. Continuation (weakly) dominates; the firm harvests organization capital.

*Case $x_1 < 0$*: $V_1(I_1 = 0) = I_0(1 + s)x_1 < I_0x_1$ since $s > 0$ and $x_1 < 0$. Abandonment dominates.

Combining Steps 1 and 2 yields the policy in (12) and the associated value functions in (13).
□

[Page 34]
*Proof of Proposition 1.* From (5) and Lemma 1:
$$
E_0[V_1^*] = E_0[I_0 x_1 \mathbf{1}_{x_1<0}] + E_0[I_0(1+s)x_1 \mathbf{1}_{0 \le x_1 \le 1}] + E_0[(I_0(1+s)x_1 + H(x_1-1))\mathbf{1}_{x_1>1}]
$$
$$
= I_0 E_0[x_1 \mathbf{1}_{x_1<0}] + I_0(1+s)E_0[x_1 \mathbf{1}_{x_1 \ge 0}] + H E_0[(x_1-1)\mathbf{1}_{x_1>1}].
$$

Define $P = -E_0[x_1 \mathbf{1}_{x_1<0}] \ge 0$ and use $E_0[x_1 \mathbf{1}_{x_1<0}] + E_0[x_1 \mathbf{1}_{x_1 \ge 0}] = E_0[x_1] = x_0$ to obtain $E_0[x_1 \mathbf{1}_{x_1 \ge 0}] = x_0 + P$:
$$
E_0[V_1^*] = -I_0 P + I_0(1+s)(x_0+P) + H C(x_0, \sigma_0)
$$
$$
= I_0[(1+s)x_0 + sP] + H C(x_0, \sigma_0).
$$
Subtracting the initial investment $I_0$ gives (14).

To evaluate $C(x_0, \sigma_0)$: under Assumption 1, let $d = (x_0-1)/\sigma_0$ and substitute $u = (x-x_0)/\sigma_0$:
$$
C = \int_1^\infty (x-1) \cdot \frac{1}{\sigma_0} \phi(\frac{x-x_0}{\sigma_0}) dx = \int_{-d}^\infty (x_0 + \sigma_0 u - 1) \phi(u) du
$$
$$
= (x_0-1)[1-\Phi(-d)] + \sigma_0 \int_{-d}^\infty u \phi(u) du
$$
$$
= (x_0-1)\Phi(d) + \sigma_0 \phi(d),
$$
using $1-\Phi(-d) = \Phi(d)$ and $\int_a^\infty u\phi(u)du = \phi(a)$.

Similarly, $P(x_0, \sigma_0) = \sigma_0 \phi(x_0/\sigma_0) - x_0 \Phi(-x_0/\sigma_0)$ by the same integration method with strike zero.
□

*Proof of Proposition 4.* Working with the simplified form (15): $V_0 = I_0[(1+s)x_0 - 1] + HC(x_0, \sigma_0)$.

*Equation (20):* $\partial C / \partial \sigma_0 = \phi(d)$ because $\partial[(x_0-1)\Phi(d) + \sigma_0 \phi(d)]/\partial \sigma_0 = (x_0-1)\phi(d) \cdot (x_0-1)/(-\sigma_0^2) + \phi(d) + \sigma_0 \phi'(d) \cdot (-d)/\sigma_0 = \phi(d)[-(x_0-1)^2/\sigma_0^2 + 1 + d(x_0-1)/\sigma_0]$; noting

[Page 35]
$d = (x_0 - 1)/\sigma_0$, the bracket simplifies to $-d^2 + 1 - d^2 \cdot (-1) = 1...$

*Direct route:* $\partial_{\sigma_0}[\sigma_0\phi(d)] = \phi(d) + \sigma_0\phi'(d) \cdot (-1/\sigma_0) = \phi(d) + d\phi(d) \cdot \sigma_0/\sigma_0^2...$

*Standard result:* By direct differentiation and use of $\phi'(d) = -d\phi(d)$:
$$
\frac{\partial C}{\partial \sigma_0} = (x_0 - 1)\phi(d) \cdot \frac{1}{-\sigma_0} + \Phi(d) + \sigma_0\phi(d) \cdot \frac{d}{\sigma_0^2} = \phi(d)[-d + 1 + d] = \phi(d).
$$
Therefore $\partial V_0/\partial \sigma_0 = H\phi(d) > 0$.

**Equation (21):** $\partial V_0/\partial s = I_0x_0 > 0$ since $x_0 > 0$ (maintained assumption) and $I_0 > 0$.

**Equation (22):** $\partial V_0/\partial H = C(x_0, \sigma_0) > 0$ since $C > 0$ whenever $\mathbb{P}(x_1 > 1) > 0$, which holds for all finite $\sigma_0 > 0$.

**Equation (23):** By the standard result $\partial C/\partial x_0 = \Phi(d)$ (the option delta): $\partial V_0/\partial x_0 = I_0(1 + s) + H\Phi(d)$. Since $d < 0$, $\Phi(d) < 1/2$ but $\phi(d) > 0$; and since $I_0(1 + s) > 0$, the sum is positive.

**Complementarity** $\partial^2 V_0/\partial s \, \partial I_0 = x_0 > 0$ follows directly from $\partial V_0/\partial s = I_0x_0$. $\square$

# References
Aghion, P., & Howitt, P. (1992). A model of growth through creative destruction. *Econometrica*, 60, 323-351.

Aghion, P., & Howitt, P. (1998). *Endogenous Growth Theory*. MIT Press, Cambridge, MA.

Arrow, K. J. (1962). The economic implications of learning by doing. *Review of Economic Studies*, 29, 155-173.

Adner, R., & Levinthal, D. A. (2004). What is not a real option: Considering boundaries for the application of real options to business strategy. *Academy of Management Review*, 29, 74-85.

[Page 36]
Bernardo, A. E., & Chowdhry, B. (2002). Resources, real options, and corporate strategy.
*Journal of Financial Economics, 63*, 211–234.

Benner, M. J., & Tushman, M. L. (2003). Exploitation, exploration, and process manage-
ment: The productivity dilemma revisited. *Academy of Management Review, 28*, 238–256.

Bloom, N., Bond, S., & Van Reenen, J. (2007). Uncertainty and investment dynamics.
*Review of Economic Studies, 74*, 391-415.

Bowman, E. H., & Hurry, D. (1993). Strategy through the option lens: An integrated view
of resource investments and the incremental-choice process. *Academy of Management
Review, 18*, 760–782.

Christensen, C. M. (1997). *The Innovator's Dilemma: When New Technologies Cause Great
Firms to Fail*. Harvard Business School Press, Boston, MA.

Cohen, W. M., & Levinthal, D. A. (1990). Absorptive capacity: A new perspective on
learning and innovation. *Administrative Science Quarterly, 35*, 128–152.

Dixit, A. K., & Pindyck, R. S. (1994). *Investment under Uncertainty*. Princeton University
Press, Princeton, NJ.

Gilbert, R., & Newbery, D. (1982). Preemptive patenting and the persistence of monopoly.
*American Economic Review, 72*, 514–526.

Grove, A. S. (1996). *Only the Paranoid Survive: How to Exploit the Crisis Points That
Challenge Every Company*. Currency Doubleday, New York, NY.

Henderson, R. M., & Clark, K. B. (1990). Architectural innovation: The reconfiguration of
existing product technologies and the failure of established firms. *Administrative Science
Quarterly, 35*, 9–30.

Kogut, B. (1991). Joint ventures and the option to expand and acquire. *Management Science,
37*, 19–33.

[Page 37]
Lucas, R. E., Jr. (1988). On the mechanics of economic development. *Journal of Monetary Economics*, 22, 3-42.

March, J. G. (1991). Exploration and exploitation in organizational learning. *Organization Science*, 2, 71-87.

McGrath, R. G. (1999). Falling forward: Real options reasoning and entrepreneurial failure. *Academy of Management Review*, 24, 13–30.

Mokyr, J. (2017). *A Culture of Growth: The Origins of the Modern Economy*. Princeton University Press, Princeton, NJ.

Myers, S. C. (1977). Determinants of corporate borrowing. *Journal of Financial Economics*, 5, 147-175.

Nelson, R. R., & Winter, S. G. (1982). *An Evolutionary Theory of Economic Change*. Harvard University Press, Cambridge, MA.

Pisano, G. P. (1994). Knowledge, integration, and the locus of learning: An empirical analysis of process development. *Strategic Management Journal*, 15, 85-100.

Reinganum, J. F. (1983). Uncertain innovation and the persistence of monopoly. *American Economic Review*, 73, 741-748.

Schumpeter, J. A. (1942). *Capitalism, Socialism and Democracy*. Harper & Brothers, New York, NY.

Teece, D. J., Pisano, G., & Shuen, A. (1997). Dynamic capabilities and strategic manage- ment. *Strategic Management Journal*, 18, 509–533.

Tripsas, M., & Gavetti, G. (2000). Capabilities, cognition, and inertia: Evidence from digital imaging. *Strategic Management Journal*, 21, 1147–1161.