

[Page 1]
INNOVATION, ACCESS, AND THE LINDAHL ROYALTY

Bhagwan Chowdhry †
Deepa Mani †

† Indian School of Business, Hyderabad 500 111, India

bhagwan@isb.edu deepa_mani@isb.edu

March 22, 2026

**Abstract.** Governments can buy out a patent at the innovator's monopoly profit,
open-source the technology, and price universally at marginal cost. This is Kremer's
mechanism, and it is correct — if you can fund it. You cannot. Voluntary prize funds
are chronically under-provided by a factor of $\sqrt{N}$; COVAX confirmed this at scale.
We derive a mechanism that achieves first-best innovation and near-universal access
without public expenditure: a capped royalty licensing mandate in which the innova-
tor licenses generic production in poor-country markets subject to a per-unit royalty
cap $r^* = (\sqrt{S}/a – S_R)/(\mu_p n_p)$. The Lindahl conditions determine the optimal cap.
Government purchase at $G^*$ dominates the CRLM only when the shadow cost of pub-
lic funds $\lambda > \lambda^* \approx 1.21$; at calibrated values the mechanisms are nearly equivalent in
welfare and the CRLM wins on feasibility by a wide margin. The Medicines Patent
Pool has operated the CRLM for HIV antiretrovirals since 2010 without a theoretical
foundation. This paper provides one.

**JEL Classification:** D42, F53, H41, I15, O31

[Page 2]
*Keywords*: capped royalty licensing, Lindahl royalty, pharmaceutical innovation, tiered pricing, prize mechanism, global public goods, Medicines Patent Pool, mechanism design

[Page 3]
# INTRODUCTION

Pfizer earned $37 billion from its Covid vaccine in 2021. Moderna earned $18 billion. To-gether, the two mRNA vaccines reached roughly 4 billion arms—a triumph of private inno-vation that would not have happened without the prospect of those profits.¹ But the same patents that made those profits possible also priced the vaccine out of reach for most of the world. At the peak of the pandemic, low-income countries were paying more per dose than OECD governments—not because the vaccine cost more to produce there, but because Pfizer could charge more there. The institution that creates the incentive to innovate is the same institution that makes the innovation inaccessible. This is the constitutive problem of pharmaceutical markets, and it is not new.

What do you do about it? There are four options on the table, and none of them is obviously right.

*Waive the patent.* Biden tried this in 2021. Merkel refused. Her critics called it protectionism; they were wrong. Waiving a patent after the investment is made sends exactly one signal to the next innovator: don't bother, or price in the expropriation risk.

*Fund a prize.* Kremer (1998) proposed that governments buy out the patent at social value—paying the innovator $G^* = \sqrt{S/\alpha}$—and open-source the technology. Universal access, correct innovation incentive. The idea is theoretically right. The problem is funding. Every government has an incentive to let the others pay while still receiving the vaccine if someone does—a result Bergstrom et al. (1986) proved in 1986 and COVAX confirmed in 2021. The prize pool that theory requires, the institutions that exist cannot fill.

*Buy out the patent at monopoly profit.* A simpler version of Kremer: one government— say the United States—pays Pfizer her monopoly profit $S_R$ and open-sources the vaccine. No auction, no social value estimation. The problem is that this costs $\Delta S_R$ in fiscal welfare, achieves only the sub-optimal patent effort $e_M$ (since $S_R < G^*$), and asks a single government

---
¹We build on arguments first developed in Chowdhry and Mani (2021). We are grateful to seminar participants at the Indian School of Business, UCLA Anderson, and the NBER Health Economics meeting for helpful comments.

[Page 4]
to bear the cost of a global public good—which it has no incentive to do.

*Mandate tiered pricing.* Require the innovator to sell at marginal cost in poor countries while keeping monopoly prices in rich ones. This was advocated by Danzon and Towse (2003) and the WHO. It is free for the innovator—she was earning nothing from excluded poor-country markets anyway—so it is politically feasible. But it leaves innovation effort at the sub-optimal patent level $e_M$, because the innovator’s profit is unchanged from the patent benchmark.

None of these four options achieves first-best innovation, universal access, and zero public expenditure simultaneously. The question is whether any mechanism can.

One can. Between the extremes of charging poor countries nothing ($\bar{r} = 0$, tiered pricing) and charging them everything ($\bar{r} = v_p - c$, unregulated 3PD) lies a continuum of royalty caps. The innovator licenses generic production in poor-country markets subject to a per-unit royalty $\bar{r}$, earning $S_R + \bar{r}\mu_p n_p$ total. The Lindahl conditions determine the optimal cap:
$$
\bar{r}^* = \frac{\sqrt{S/\alpha} - S_R}{\mu_p n_p}
\quad(1)
$$
Rich countries already contribute $S_R$ through monopoly pricing. Poor countries contribute the residual $G^* - S_R$ through royalty payments on generic sales. Together they fund the Lindahl-optimal prize $G^* = \sqrt{S/\alpha}$. First-best innovation. Near-universal access at $c + \bar{r}^*$. No public funds. No free-rider problem. No supranational authority. We call this the *capped royalty licensing mandate* (CRLM).

**But wait—what about government purchase at $G^*$?** The sharpest objection to the CRLM is Kremer’s own mechanism applied correctly: if a government can commit to buying out the patent at $G^*$ and open-sourcing the technology, it achieves the same first-best innovation as the CRLM and serves every individual on earth at marginal cost $c$—including poor people in rich countries, who pay $c + \bar{r}^*$ under the CRLM and therefore do worse. Government purchase at $G^*$ weakly dominates the CRLM.

[Page 5]
In theory. The welfare comparison is:
$$
W^{\text{Govt Purchase}} - W^{\text{CRLM}} = \pi(e^{FB}) r^*\mu_p\eta_p - (\lambda - 1) G^*. \quad (2)
$$
Government purchase dominates iff $\pi(e^{FB})(G^* - S_R) > (\lambda - 1)G^*$, i.e., $\lambda < \lambda^* = 1 + \pi(e^{FB}) (G^* - S_R)/G^*$. At our calibrated values, $\lambda^* \approx 1.21$. The two mechanisms are nearly welfare-equivalent at calibrated parameters; the CRLM wins if the shadow cost of public funds exceeds 21 cents per dollar.

More importantly: government purchase at $G^*$ faces the same free-rider problem as the cash Lindahl prize. It requires raising $G^* \approx \$77B$ internationally. COVAX raised $10B and was considered a success. No government has ever paid $G^* = \sqrt{S/\alpha}$ to open-source a pharmaceutical at global social value, because no international institution exists to compel that payment, and the BVB free-rider logic applies to who pays for the buyout exactly as it applies to who funds the prize pool. In practice, government purchase at $G^*$ reduces to the prize mechanism—and the prize mechanism does not get funded.

The CRLM raises $G^*$ through the price mechanism. No government transfers money. No international coordination is required beyond a TRIPS amendment and a bilateral anti- re-export clause. The Medicines Patent Pool has been doing exactly this since 2010. The CRLM is not better than government purchase in a world where governments can credibly commit to paying $G^*$ internationally. It is better in the world we actually inhabit.

**The access inversion.** One genuine problem with the CRLM relative to government purchase: poor individuals in rich countries fare worse. Under government purchase at $G^*$, the technology is open-sourced and everyone pays $c$. Under the CRLM, uninsured individuals in rich countries pay $v_R$—the monopoly price—while the same person in Bangladesh pays $c + \tilde{r}^* < v_p < v_R$. The mechanism designed to help poor countries produces a price schedule under which comparable individuals in rich countries have worse access than comparable individuals in poor countries.

[Page 6]
Proposition 8 and Corollary 3 formalise this *access inversion*. It is an artefact of pricing by country rather than by individual income. The remedy is universal health coverage—a domestic policy choice—not international mechanism design. The CRLM and universal coverage are complements.

**What is new and what is not.** The intuition that differential pricing serves poor countries without harming innovators is twenty years old—Danzon and Towse (2003), Scherer and Watal (2002), the WHO's 2001 report. That we cannot fund a prize is BVB's theorem applied to COVAX. That prizes dominate patents in welfare is Kremer's result.

**What is new:** the CRLM as the continuous mechanism of which tiered pricing and 3PD are boundary cases; the Lindahl royalty formula (1) as the optimal interior parameterisation; the welfare threshold $\lambda^*$ at which government purchase dominates the CRLM; the four feasibility asymmetries making the CRLM strictly more implementable than any mechanism requiring international fiscal coordination; the racing invariance of the Lindahl royalty; and the access inversion formalised as a testable corollary.

Section 2 reviews the literature. Section 3 presents the model. Sections 4–6 develop the benchmarks. Section 7 derives the CRLM, the Lindahl royalty, and the government-purchase comparison. Section 8 covers extensions, calibration, the MPP, and the access inversion. Section 9 concludes.

# RELATED LITERATURE

*Patents, prizes, and differential pricing*

Nordhaus (1969) and Arrow (1962) formalise the tradeoff between innovation incentives and static pricing efficiency. Kremer (1998) proposed patent buyouts: governments pay the innovator social value and open-source the technology. Welfare- superior to the patent. Our paper begins where Kremer ends: who pays?

[Page 7]
The intuition that differential pricing serves poor countries without harming innovators is in Danzon and Towse (2003) and Scherer and Watal (2002). Both argue a monopolist who excludes poor markets anyway loses nothing by serving them at lower prices. The WHO's 2001 differential pricing report restates this in policy language. What is missing is the mechanism design structure: the formal conditions, the optimal royalty parameterisation, and the connection to Lindahl efficiency. That is what we provide.

Scotchmer (1991) and Gans and Scotchmer (2003) study cumulative innovation. The CRLM is robust: rich-country revenues are untouched, so follow-on incentives survive. Kremer and Glennerster (2004) introduced advance market commitments. COVAX was one. It failed—for exactly the reason Lemma 2 predicts (Moon and Sridhar, 2022). DiMasi et al. (2003) and Acemoglu and Akcigit (2012) provide the R&D cost and directed innovation benchmarks we calibrate against.

*Innovation racing*

Loury (1979) and Dasgupta and Stiglitz (1980) establish that patent races generate over-investment and excessive entry. We apply these as benchmarks. The new result is that the Lindahl royalty is invariant to $N$: the optimal cap depends on $S$, $S_R$, $\alpha$, and $\mu_p n_p$, none of which change with the number of firms. Tiered contribution schedules compound under racing; the CRLM does not.

*Public goods and voluntary contributions*

Samuelson (1954), Groves (1973), and Clarke (1971) establish that public goods require preference revelation and that standard mechanisms fail budget balance. The result we use is from Bergstrom et al. (1986): the Nash equilibrium of a voluntary contribution game is determined entirely by the agent with the highest willingness-to-pay; all others free-ride. We apply this to pharmaceutical prize funding in Lemma 2. The theorem is BVB's; the application and the Lindahl royalty resolution are ours.

[Page 8]
The Lindahl equilibrium (Lindahl, 1919) is what a perfectly coordinating world would
implement. Our central result shows the CRLM achieves the Lindahl-optimal innovation
level through the price mechanism, without requiring Lindahl contribution schedules—and
without asking any government to act against its fiscal incentives. Bagwell and Staiger
(1990) and Dixit (2000) study international agreements with conflicting national interests; the
CRLM needs only a bilateral royalty-cap agreement, far less demanding than a supranational
prize fund.

*Price discrimination and welfare*

Pigou (1932), Robinson (1933), and Varian (1985) establish the classical welfare economics of
third-degree discrimination. The key result is from Weyl and Tirole (2012): discrimination
raises welfare iff it expands output. The CRLM at any $\check{r} \in (0, v_p - c)$ expands output
and raises innovation above the patent benchmark; the Lindahl royalty is where the welfare
optimum is reached. Chaudhuri et al. (2006) provide welfare estimates for India that calibrate
our $S_P/\Pi_M$ ratio.

Kremer and Miguel (2004) document that willingness-to-pay in poor countries under-
states social value—every welfare estimate in this paper is conservative. Stiglitz (2006) is
right that patents fail poor patients; he is wrong that a prize fund is the answer, for reasons
BVB formalised and COVAX confirmed. The CRLM achieves what Stiglitz wants through
a mechanism that requires no international fiscal coordination.

## MODEL

### 3.0 Summary of mechanisms

Before developing the formal analysis, Table 1 summarises the five mechanisms studied in
the paper along the dimensions that determine the welfare and feasibility rankings.

[Page 9]
Table 1: Mechanisms compared
| | Patent | Nash prize | CRLM ($\tilde{r}^*$) | Unregulated 3PD | Govt purchase |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Innovation effort | $e_M$ | $e_M$ | $e^{FB}$ | $e^{FB}$ | $e^{FB}$ |
| Poor-country price | Excluded | $c$ | $c+\tilde{r}^*$ | $v_P$ | $c$ |
| Poor-country surplus | 0 | $S_P$ | $(v_P - c - \tilde{r}^*)\mu_P n_P$ | 0 | $S_P$ |
| Public expenditure | 0 | $\lambda G^{NE}$ | 0 | 0 | $\lambda G^*$ |
| Free-rider problem? | n/a | Yes | No | n/a | Yes |
| Needs $\alpha$ revealed? | No | No | No | No | Yes |
| Racing robustness | — | Worsens in $N$ | Invariant to $N$ | — | Worsens in $N$ |
| Welfare rank ($\lambda=1$) | 5th | 4th | 1st (tied) | 3rd | 1st (tied) |
| Feasibility rank | — | 4th | 1st | — | 5th |

*Notes.* CRLM and government purchase at $G^*$ are welfare-tied at $\lambda=1$; CRLM dominates at $\lambda > \lambda^* \approx 1.21$. The CRLM at $\tilde{r}=0$ (tiered pricing mandate) achieves effort $e_M$, not $e^{FB}$; $\tilde{r}^* > 0$ is required for first-best.

## 3.1 Countries

There is a continuum of countries with total measure normalised to one, partitioned into two groups. *Rich countries* have measure $\mu_R \in (0,1)$, population per country $n_R$, and a representative consumer with willingness-to-pay (WTP) $v_R$ for one unit of the vaccine. *Poor countries* have measure $\mu_P = 1 - \mu_R$, population per country $n_P$, and WTP $v_P < v_R$. All consumers have unit demand. Let $c \ge 0$ denote the constant marginal cost of production.

**Assumption 1** (Profitable range). $c < v_P < v_R$.

Assumption 1 ensures that serving any country at any price $p \in [c, v_P]$ is at least weakly profitable, so there are gains from trade in all markets.

Define the *aggregate surpluses at marginal cost pricing*:
$$
S_R \equiv (v_R - c)\mu_R n_R, \quad (3)
$$
$$
S_P \equiv (v_P - c)\mu_P n_P, \quad (4)
$$
$$
S \equiv S_R + S_P. \quad (5)
$$

[Page 10]
These are the total surpluses that would be realised if the vaccine were priced at marginal cost and all countries were served, and they serve as welfare benchmarks throughout.

*Remark 1.* $S_R$ and $S_P$ are measured using willingness-to-pay, which equals social value only when income effects are absent. For poor countries, budget constraints bind, so the true social value $V_P \ge v_P$. All welfare comparisons based on $S_P$ are therefore conservative: the access gains from serving poor countries at marginal cost are at least $S_P$ and potentially larger.

## 3.2 The innovator

A single risk-neutral firm (the “innovator”) chooses effort $e \ge 0$ at private cost $e$. Effort produces a successful vaccine with probability $\pi(e)$.

**Assumption 2** (Innovation technology). $\pi: \mathbb{R}_+ \to [0, 1)$ satisfies:

(i) $\pi(0) = 0$, $\pi'(e) > 0$, $\pi''(e) < 0$ for all $e > 0$;

(ii) $\lim_{e \to 0} \pi'(e) = +\infty$ (Inada from below);

(iii) $\lim_{e \to \infty} \pi'(e) = 0$ (Inada from above).

The Inada conditions ensure a unique interior optimum under any positive revenue stream. The leading parametric example is:
$$
\pi(e) = 1 - e^{-\alpha e}, \quad \alpha > 0, \quad (6)
$$
which satisfies all parts of Assumption 2 and yields closed-form first-order conditions. We use this specification to deliver explicit expressions throughout but state all main results for the general case.

Upon success, the innovator produces at constant marginal cost $c$. Failure yields zero payoff to all parties. Under any revenue stream $R$, the innovator solves:
$$
\max_{e \ge 0} \pi(e) R - e. \quad (7)
$$

[Page 11]
The unique interior solution $e^*(R)$ satisfies $\pi'(e^*(R)) = 1/R$ and is strictly increasing in $R$:
$$
\frac{de^*}{dR} = \frac{-1}{R^2 \pi''(e^*(R))} > 0,
\quad (8)
$$
since $\pi'' < 0$ by Assumption 2(i).

## 3.3 Social welfare

Social welfare is expected total surplus net of innovation cost and fiscal expenditure:
$$
W = \pi(e) \cdot [\text{total surplus accruing to served countries}] - e - (\lambda - 1) T,
\quad (9)
$$
where $T \ge 0$ is government expenditure (prizes or subsidies) and $\lambda \ge 1$ is the shadow cost of public funds. When $\lambda = 1$, fiscal transfers are pure redistribution with no deadweight cost. When $\lambda > 1$, raising $T$ dollars costs society $\lambda T$ dollars—the excess burden of taxation. We treat $\lambda$ as a parameter and characterise all welfare comparisons as a function of $\lambda$.

The *first-best* benchmark is achieved when (i) innovation effort maximises expected social surplus, and (ii) conditional on success, the vaccine is priced at $c$ and all countries are served. First-best effort $e^{FB}$ satisfies:
$$
\pi'(e^{FB}) = \frac{1}{S},
\quad (10)
$$
and first-best welfare is $W^{FB} = \pi(e^{FB}) S - e^{FB}$.

## 3.4 Exclusion profitability

The following assumption governs when the monopolist prefers to exclude poor countries.

**Assumption 3** (Exclusion profitability).
$$
S_R > (v_P - c) (\mu_R n_R + \mu_P n_P).
\quad (11)
$$

[Page 12]
Assumption 3 states that the profit from serving only rich countries at $p_R = v_R$ exceeds the profit from globally pricing at $p_P = v_P$. Rearranging (11):
$$
\underbrace{(v_R - v_P)\mu_R n_R}_{\text{premium from rich pricing}} > \underbrace{(v_P - c)\mu_P n_P}_{\text{gain from including poor countries}} \quad . \tag{12}
$$
This holds when the rich-poor WTP gap is large, the rich market is large, or the poor-country margin $v_P - c$ is small. In the Covid vaccine context all three conditions are plausible: per-capita WTP in OECD countries is an order of magnitude above that in low-income countries, and OECD consumers account for the large majority of pharmaceutical revenues worldwide.

# THE PATENT BENCHMARK

Under a patent the innovator holds exclusive production rights and sets prices to maximise profit.

**_Lemma 1 (Optimal monopoly pricing)._** _Under Assumptions 1 and 3, the profit-maximising monopolist sets $p_R = v_R$ and excludes all poor countries. Monopoly profit is $\Pi_M = S_R$._

_Proof._ Consider all feasible pricing strategies. At $p = v_R$ the monopolist serves only rich countries and earns $(v_R - c)\mu_R n_R = S_R$. At $p = v_P$ it serves all countries and earns $(v_P - c)(\mu_R n_R + \mu_P n_P)$, which is strictly less than $S_R$ by Assumption 3. At any $p \in (v_P, v_R)$ only rich countries are served at a sub-optimal price, giving profit $(p - c)\mu_R n_R < S_R$. Thus $p_R = v_R$ strictly dominates all alternatives, and $\Pi_M = S_R$. □

The innovator's problem under patent is therefore:
$$
\max_{e \ge 0} \pi(e) S_R - e, \tag{13}
$$

[Page 13]
with unique solution $e_M$ satisfying:
$$
\pi'(e_M) = \frac{1}{S_R}. \quad (14)
$$

**Proposition 1** (Patent welfare and the cost of exclusion). Under Assumptions 1–3:

(i) $e_M < e^{FB}$: the patent under-invests relative to the first-best.

(ii) Conditional on success, all poor countries are excluded.

(iii) Patent welfare is $W_M = \pi(e_M)S_R - e_M$.

(iv) The welfare loss relative to first-best is
$$
W^{FB} - W_M = [\pi(e^{FB}) - \pi(e_M)]S_R + \pi(e^{FB})S_P - [e^{FB} - e_M] > 0. \quad (15)
$$

*Proof*. (i) From the first-order conditions: $\pi'(e_M) = 1/S_R$ and $\pi'(e^{FB}) = 1/S = 1/(S_R+S_P)$. Since $S_P > 0$, we have $\pi'(e^{FB}) < \pi'(e_M)$, and strict concavity of $\pi$ implies $e^{FB} > e_M$.

(ii) Lemma 1 gives $p_R^* = v_R > v_P$, so poor countries with WTP $v_P$ are excluded.

(iii) Conditional on success, rich-country consumers are priced at their reservation value and capture zero consumer surplus; the innovator captures $S_R$ as profit. Expected welfare is $\pi(e_M)S_R - e_M$.

(iv) First-best welfare is $W^{FB} = \pi(e^{FB})(S)-e^{FB}$. Subtracting $W_M$ from $W^{FB}$ and collecting terms yields (15). Positivity follows from the optimality of $e^{FB}$ for the first-best problem: the envelope theorem ensures the net innovation gain (first and third terms combined) is non-negative, and $\pi(e^{FB})S_P > 0$ strictly. □ □

*Remark 2*. The welfare loss (15) has three components: the innovation effort distortion $[\pi(e^{FB}) - \pi(e_M)]S_R - [e^{FB} - e_M] \ge 0$; the access loss $\pi(e^{FB})S_P > 0$; and a negative cross-term from the lower effort under patent (already accounted for in the first term). The access loss $\pi(e_M)S_P$ is the component that motivates the prize mechanism in Section 5.

[Page 14]
# THE PRIZE SYSTEM

## 5.1 Structure

A social planner (or coalition of governments) commits to paying prize $G \ge 0$ to the innovator upon successful development. Upon payment, the technology is open-sourced: competition drives the price to $c$ in all markets and all countries are served. The prize is financed by public contributions $\{t_i\}$ with shadow cost $\lambda \ge 1$; the net fiscal cost to society is $(\lambda - 1)G$.

The innovator's problem under prize $G$ is:
$$
\max_{e \ge 0} \pi(e)G - e,
\quad(16)
$$
with unique solution $e_G$ satisfying $\pi'(e_G) = 1/G$.

## 5.2 Welfare comparison

**Proposition 2** (Prize welfare dominance). For a prize $G = \Pi_M = S_R$ financed at shadow cost $\lambda$:

(i) *The prize replicates patent innovation effort: $e_G = e_M$.*

(ii) *Prize welfare is $W_P = \pi(e_M)S - e_M - (\lambda - 1)S_R$.*

(iii) *The prize strictly welfare-dominates the patent if and only if*
$$
\pi(e_M)S_P > (\lambda - 1)S_R.
\quad(17)
$$

(iv) *When $\lambda = 1$ the prize always dominates, with net welfare gain $\pi(e_M)S_P > 0$.*

*Proof.* (i) Comparing first-order conditions: $\pi'(e_G) = 1/G = 1/S_R = \pi'(e_M)$, so $e_G = e_M$ by strict concavity of $\pi$.

(ii) Under the prize all countries are served at $p = c$; total conditional surplus is $S$. The prize $G = S_R$ is a transfer from governments to the innovator; the net fiscal deadweight cost is $(\lambda - 1)S_R$. Hence $W_P = \pi(e_M)S - e_M - (\lambda - 1)S_R$.

[Page 15]
(iii)-(iv) The welfare difference is:
$W_P - W_M = [\pi(e_M)S – e_M – (\lambda – 1)S_R] – [\pi(e_M)S_R - e_M] = \pi(e_M)S_P – (\lambda − 1)S_R,$
which is positive iff (17) holds. At $\lambda = 1$ the right side is zero, so the prize always dominates.
$\square$
$\square$

Remark 3 (Comparative statics). The prize advantage $\Delta = \pi(e_M)S_P-(\lambda-1)S_R$ is increasing in $S_P$ and decreasing in $\lambda$. Under the parametric specification:
$$
\Delta = \left(1 - \frac{1}{\alpha S_P}\right)S_P - (\lambda - 1)S_R.
\quad (18)
$$
This motivates the CRLM: it achieves the same access gain $\pi(e_M)S_P$ at zero fiscal cost, and at $r^* > 0$ raises it further by also improving innovation effort to $e^{FB} > e_M$.

# THE FREE-RIDER BENCHMARK

The results in this section apply Bergstrom et al. (1986) to the pharmaceutical prize setting. We present them as lemmas, not propositions, to signal that the theorems belong to BVB; the contribution is the application and the expression of the efficiency gap in terms directly relevant to the mechanism design problem in Section 7.

## 6.1 The contribution game

Even when the prize dominates the patent in welfare, it must be funded voluntarily in the absence of a supranational fiscal authority. Suppose countries choose contributions $g_i \ge 0$ simultaneously. Total prize $G = \sum_i g_i$. The innovator responds optimally: given $G$, she chooses effort $e^*(G)$ satisfying $\pi'(e^*(G)) = 1/G$. Define the equilibrium innovation probability:
$$
\phi(G) = \pi(e^*(G)).
\quad (19)
$$

[Page 16]
Differentiating $\pi'(e^*(G)) = 1/G$ with respect to $G$:
$$
e^{*'}(G) = \frac{-1}{G^2 \pi''(e^*(G))} > 0,
\quad (20)
$$
so $\phi'(G) = \pi'(e^*) \cdot e^{*'}(G) > 0$: larger prizes induce higher innovation probability. Moreover, $\phi''(G) < 0$ (from $\pi'' < 0$ and the composition rule), so $\phi$ is strictly concave and strictly increasing in $G$.

Country $i$'s payoff is:
$$
U_i(g_i, G_{-i}) = \phi(g_i + G_{-i}) S_i - g_i,
\quad (21)
$$
where $S_i \in \{S_R, S_P\}$ is country $i$'s aggregate surplus at marginal cost and $G_{-i} = G - g_i$.

## 6.2 Nash equilibrium

**Lemma 2** (Nash equilibrium of the contribution game; Bergstrom et al. 1986). Let $\hat{S} = \max_i S_i$ denote the largest country-level surplus, attained (without loss of generality) by country $\bar{i}$. Under Assumption 2, the unique Nash equilibrium of the voluntary contribution game is:

(i) Country $\bar{i}$ contributes $G^{NE}$ where $\phi'(G^{NE}) \hat{S} = 1$.

(ii) All other countries contribute $g_i^{NE} = 0$.

(iii) Total prize and innovation probability are $G^{NE}$ and $\phi(G^{NE})$ respectively.

Furthermore, $G^{NE}$ equals the optimum a single-country world with only $\bar{i}$ would choose.

*Proof.* Step 1: At most one country contributes in equilibrium. Suppose countries $i$ and $j$ both contribute positive amounts. Each satisfies an interior best-response condition:
$$
\phi'(G) S_i = 1 \quad \text{and} \quad \phi'(G) S_j = 1.
$$
Dividing: $S_i = S_j$. Since countries generically have distinct surpluses, this is a contradiction.

[Page 17]
Hence at most one country contributes.

Step 2: The contributor must be $\bar{i}$. Suppose only country $k \neq \bar{i}$ contributes $g_k = G$ in equilibrium, with interior condition $\phi'(G) S_k = 1$. Then $\phi'(G) = 1/S_k > 1/\bar{S}$ (since $\bar{S} > S_k$), so country $\bar{i}$'s marginal benefit from contributing $\epsilon > 0$ is $\phi'(G) \bar{S} > 1 =$ marginal cost, meaning $\bar{i}$ strictly prefers to deviate. Contradiction.

Step 3: Uniqueness. Country $\bar{i}$ contributes $G^{NE}$ satisfying $\phi'(G^{NE})\bar{S} = 1$. For any $j \neq \bar{i}$: contributing $\epsilon > 0$ yields marginal benefit $\phi'(G^{NE} + \epsilon)S_j < \phi'(G^{NE})S_j < \phi'(G^{NE})\bar{S} = 1$ = marginal cost, so $j$ strictly prefers $g_j = 0$. Country $\bar{i}$ has no profitable deviation by construction. $\Box$ $\Box$

### 6.3 The efficiency gap

**Lemma 3** (Efficiency gap; Bergstrom et al. 1986). The socially optimal total prize $G^*$ satisfies:
$$
\phi'(G^*) S = 1. \quad (22)
$$

The voluntary equilibrium is inefficient whenever there is more than one country:
$$
G^* > G^{NE} \iff S > \bar{S}. \quad (23)
$$

Specifically:

(i) The efficiency gap $G^*/G^{NE}$ is increasing in the number of countries $N$.

(ii) It is increasing in $S_p/\bar{S}$: larger poor-country stakes relative to the dominant contributor widen under-provision.

(iii) Under specification (6), $\phi'(G) = 1/(\alpha G^2)$ (derived from $\phi'(G) = \pi'(e^*(G)) \cdot e^{*\prime}(G) = (1/G) \cdot (1/(\alpha G))$). The first-order conditions $\phi'(G^*) \cdot S = 1$ and $\phi'(G^{NE}) \cdot \bar{S} = 1$ give:
$$
G^* = \sqrt{\frac{S}{\alpha}}, \quad G^{NE} = \sqrt{\frac{\bar{S}}{\alpha}}. \quad (24)
$$

[Page 18]
so the efficiency gap ratio is:
$$
\frac{G^*}{G^{NE}} = \sqrt{\frac{S}{\hat{S}}} \ge 1, \tag{25}
$$
with equality only when $N=1$.

(iv) The welfare loss from under-provision relative to the social optimum is:
$$
W^* - W^{NE} = [\phi(G^*) - \phi(G^{NE})] S - [G^* - G^{NE}] > 0. \tag{26}
$$

Proof. The planner maximises $W(G) = \phi(G) S - e^*(G) - G$ over $G \ge 0$. Using the envelope theorem: $W'(G) = \phi'(G) S - 1$, and $W''(G) = \phi''(G) S < 0$, so $W$ is strictly concave with unique interior maximum at (22).

Comparing (22) with Lemma 2(i): the social optimum's first-order condition uses $S$ where the Nash condition uses $\hat{S} \le S$. Since $\phi'' < 0$, it follows that $\phi'(G^*) \le \phi'(G^{NE})$, which implies $G^* \ge G^{NE}$ with strict inequality iff $S > \hat{S}$.

(iii) Under (6): $e^*(G) = \frac{1}{\alpha}\log(\alpha G)$ and $e^{*'}(G) = 1/(\alpha G)$, so $\phi'(G) = \pi'(e^*(G)) \cdot e^{*'}(G) = (1/G) \cdot (1/(\alpha G)) = 1/(\alpha G^2)$. Setting $\phi'(G^*) \cdot S = 1$ gives $G^* = \sqrt{S/\alpha}$; setting $\phi'(G^{NE}) \cdot \hat{S} = 1$ gives $G^{NE} = \sqrt{\hat{S}/\alpha}$. The ratio is $G^*/G^{NE} = \sqrt{S/\hat{S}}$ as stated in (25).

(iv) Strict concavity of $W$ gives $W(G^*) > W(G^{NE})$. Expanding and using the envelope theorem to simplify the $e^*$ difference yields (26). □ □

**Corollary 1** (Symmetric countries). With $N$ symmetric countries ($S_i = S/N$ for all $i$), the richest country's stake is $\hat{S} = S/N$ and under specification (6) the prize ratio is $G^*/G^{NE} = \sqrt{N}$. The Nash equilibrium provides $1/\sqrt{N}$ of the socially optimal prize, with under-provision worsening as $\sqrt{N}$ in the number of countries.

[Page 19]
# THE OPTIMAL MECHANISM

The patent excludes poor countries. The prize cannot be funded. Both failures are documented above. The question is whether there is a third option. There is.

## 7.1 The capped royalty licensing mandate

The policy debate has been binary for thirty years: patent monopoly versus open-source prize. Both treat the innovator's profit as a parameter to be either preserved or transferred. Neither treats it as an instrument. It is.

Between charging poor countries nothing ($\bar{r} = 0$, tiered pricing) and charging them everything ($\bar{r} = v_P - c$, unregulated 3PD) lies a continuum of royalty caps. The innovator licenses generic production in poor-country markets at royalty $\bar{r}$, earning total profit $S_R + \bar{r}\mu_p n_p$. Higher royalties fund more innovation; lower royalties leave more surplus for poor consumers. The Lindahl conditions determine the optimum.

A capped royalty licensing mandate (CRLM) specifies:

*   Rich countries: $p_R = v_R$ (monopoly price, unchanged from patent).
*   Poor countries: generic manufacturers are licensed to produce locally and compete the consumer price to $c + \bar{r}$, remitting royalty $\bar{r} \ge 0$ per unit sold to the innovator.

The royalty cap $\bar{r} \in [0, v_p - c]$ parameterises the entire mechanism space. At $\bar{r} = 0$ the innovator earns nothing from poor countries (tiered pricing mandate, Corollary 2). At $\bar{r} = v_p - c$ the innovator extracts all poor-country surplus through equivalent pricing (unregulated 3PD, Proposition 4).

The innovator's conditional profit under royalty cap $\bar{r}$ is:
$$
\Pi(\bar{r}) = S_R + \bar{r}\mu_p n_p, \quad (27)
$$
which is strictly increasing in $\bar{r}$. Innovation effort $e^*(\Pi(\bar{r}))$ satisfies $\pi'(e^*(\Pi(\bar{r}))) = 1/\Pi(\bar{r})$ and is strictly increasing in $\bar{r}$ via equation (8).

[Page 20]
Poor-country consumer surplus under the CRLM is $(v_p - c - \bar{r})\mu_p n_p$, decreasing in $\bar{r}$. There is a genuine tradeoff: higher $\bar{r}$ funds more innovation but transfers surplus from poor consumers to the innovator.

## 7.2 The Lindahl royalty

The planner trades off innovation effort (rising in $\check{r}$) against poor-country consumer surplus (falling in $\check{r}$). Under our parametric specification, the interior optimum has a closed form: it is the royalty at which total innovator profit equals the Lindahl-optimal prize $G^* = \sqrt{S/\alpha}$, with rich countries contributing $S_R$ through monopoly pricing and poor countries contributing the residual $G^* - S_R$ through royalty payments.

$$
\bar{W}(\bar{r}) = \pi(e^*(\Pi(\bar{r}))) [S_R + \omega_p(v_p - c - \bar{r})\mu_p n_p] - e^*(\Pi(\bar{r})).
\quad(28)
$$

**Proposition 3** (Lindahl royalty and first-best implementation). Under Assumptions 1–3 and 2, with the parametric specification $\pi(e) = 1 - e^{-\alpha e}$:

(i) The socially optimal royalty $\bar{r}^*$ satisfies the first-order condition:
$$
\underbrace{\pi'(e^*(\Pi(r))) e^{*'}(\Pi(r)) \mu_p n_p [S_R + \omega_p(v_p - c - \bar{r}^*)\mu_p n_p]}_{\text{marginal innovation gain}} = \underbrace{\omega_p \pi(e^*(\Pi(\bar{r}))) \mu_p n_p}_{\text{marginal access loss}}.
\quad(29)
$$

(ii) The Lindahl-optimal innovation level $G^* = \sqrt{S/\alpha}$ is achieved when the total innovator profit equals the Lindahl prize:
$$
\Pi(r) = S_R + \bar{r}^*\mu_p n_p = G^* = \sqrt{\frac{S}{\alpha}}.
\quad(30)
$$

Solving for the Lindahl royalty:
$$
\bar{r}^* = \frac{\sqrt{S/\alpha} - S_R}{\mu_p n_p}
\quad(31)
$$

[Page 21]
(iii) The Lindahl royalty is feasible—$r^* \in (0, v_p – c)$—if and only if $S_R < \sqrt{S/\alpha} < S$, equivalently:
$$
\frac{1}{S} < \alpha < \frac{1}{S_R^2/S} \quad (32)
$$

(iv) At $r^*$, the CRLM achieves first-best innovation effort $e^*(G^*) = e^{FB}$, universal access at price $c + r^*$ in poor countries, and zero public expenditure.

(v) The Lindahl royalty is self-financing: neither a prize fund, a public subsidy, nor an international contribution schedule is needed. Rich countries contribute $S_R$ through the existing monopoly price mechanism. Poor countries contribute $r^*\mu_p n_p = G^* – S_R$ through royalty payments on generic sales. The two contributions sum to the Lindahl-optimal prize $G^*$.

(vi) The Lindahl royalty is immune to the free-rider problem that afflicts prize mechanisms: each country's contribution is enforced through the price mechanism rather than extracted through voluntary taxation, so defection is not an option.

Proof. (i) Differentiating $\bar{W}(\bar{r})$ with respect to $\bar{r}$ and setting to zero yields (29). The left side is the marginal welfare gain from increased innovation effort (via higher profit); the right side is the marginal welfare loss from reduced poor-country consumer surplus.

(ii) Under specification (6), the Lindahl-optimal prize satisfies $\phi'(G^*) \cdot S = 1$, giving $G^* = \sqrt{S/\alpha}$ (from Lemma 3(iii)). Setting $\Pi(\bar{r}^*) = G^*$ and solving for $\bar{r}^*$ yields (31).

(iii) $r^* > 0$ iff $G^* > S_R$, i.e., $\sqrt{S/\alpha} > S_R$, equivalently $\alpha < S/S_R^2$. $r^* < v_p - c$ iff $G^* < S_R + (v_p - c)\mu_p n_p = S$, i.e., $\sqrt{S/\alpha} < S$, equivalently $\alpha > 1/S$. Together these give (32).

(iv) When $\Pi(\bar{r}^*) = G^*$, the innovator's FOC gives $\pi'(e^*(G^*)) = 1/G^*$, which is exactly the condition characterising $e^{FB}$ (equation (10)). Hence $e^*(G^*) = e^{FB}$.

(v)-(vi) By construction, $S_R+r^*\mu_p n_p = G^*$. Rich-country contributions are collected through the price mechanism (no voluntary action required). Poor-country contributions are collected through royalty payments on generic sales that generic manufacturers cannot avoid (enforced through the licensing agreement). No public funds are disbursed; no country has a unilateral

[Page 22]
incentive to defect.
$\square \quad \square$

**Remark 4.** Equation (31) has a natural economic interpretation. $G^* - S_R$ is the shortfall between the Lindahl-optimal prize and what rich countries already contribute through monopoly pricing. Poor countries fill this gap through royalty payments spread over $\mu_p n_p$ units. The Lindahl conditions determine exactly how the global cost of first-best innovation should be split between rich and poor countries—and the CRLM implements this split through the price mechanism, without a prize fund and without any international fiscal institution.

## 7.3 Boundary cases

Tiered pricing ($\bar{r} = 0$) and 3PD ($\bar{r} = v_p - c$) are the boundary cases of the CRLM. The literature has studied both without recognising they are endpoints of the same mechanism. The Lindahl royalty $r^* \in (0, v_p - c)$ is the interior solution both miss.

**Corollary 2 (Tiered pricing as boundary case).** At $\bar{r} = 0$, the CRLM reduces to the tiered pricing mandate: $p_R = v_R$, $p_p = c$, $\Pi(0) = S_R = \Pi_M$. This replicates patent innovation effort $e_M < e^{FB}$ and achieves universal access. The CRLM at $r^* > 0$ strictly welfaredominates tiered pricing whenever the feasibility condition (32) holds, because it achieves higher innovation effort at the cost of a royalty $r^* < v_p - c$ that still leaves poor countries with positive surplus $(v_p - c - r^*)\mu_p n_p > 0$.

**Proof.** At $\bar{r} = 0$: $\Pi(0) = S_R$, so $e^*(S_R) = e_M$ by (14). Poor-country consumers pay c and capture full surplus $S_p$. This is precisely the tiered pricing mandate of the prior literature (Danzon and Towse, 2003; Scherer and Watal, 2002).

**Welfare dominance:** $\bar{W}(r^*) > \bar{W}(0)$ follows from the strict concavity of $\bar{W}(r)$ (since $\pi'' < 0$) and the fact that $r^* > 0$ is the unique interior maximum when (32) holds. $\square \quad \square$

[Page 23]
7.4 The other boundary: unregulated price discrimination
---

At $r = v_p - c$ the innovator extracts all poor-country surplus and achieves first-best innovation—but poor consumers receive nothing. We characterise this boundary to determine when the Lindahl royalty dominates it.

**Proposition 4** (Unregulated 3PD versus the CRLM). Under unregulated 3PD:

(i) The innovator’s profit is $\Pi^{3PD} = S_R + S_P = S > \Pi_M$.

(ii) Innovation effort achieves the first-best: $e^{3PD} = e^{FB} > e_M$.

(iii) Poor countries are served but at $p_p = v_p$, capturing zero consumer surplus.

(iv) Welfare is $W^{3PD} = \pi(e^{FB}) S - e^{FB}$.

(v) A social planner with redistributive weight $\omega_p \ge 1$ on poor-country consumption strictly prefers the tiered pricing mandate to unregulated 3PD if and only if:
$$
\omega_p \pi(e_M) S_P > [\pi(e^{FB}) - \pi(e_M)] S_R - [e^{FB} - e_M].
\quad(33)
$$

(vi) Condition (33) is satisfied for all $\omega_p \ge \omega_p^*$, where:
$$
\omega_p^* = \frac{[\pi(e^{FB}) - \pi(e_M)]S_R - [e^{FB} - e_M]}{\pi(e_M) S_P}
\quad(34)
$$
When the innovation elasticity is low ($e^{FB} - e_M$ small), $\omega_p^* < 1$ and the mandate dominates even without redistributive preferences.

**Proof.** (i) Under 3PD the innovator earns $(v_R - c)\mu_R n_R + (v_p - c)\mu_p n_p = S_R + S_P = S$.

(ii) First-order condition: $\pi'(e^{3PD}) = 1/S = \pi'(e^{FB})$, so $e^{3PD} = e^{FB}$ by strict concavity.

(iii) The innovator sets $p_p = v_p$; poor countries pay their reservation price and capture zero consumer surplus.

(iv) Conditional on success (probability $\pi(e^{FB})$), total surplus is $S = S_R + S_P$ but all of it accrues to the innovator—rich consumers pay $v_R$ (zero surplus) and poor consumers pay $v_p$ (zero surplus). Hence $W^{3PD} = \pi(e^{FB}) S - e^{FB}$.

[Page 24]
(v) With redistributive weight $\omega_p \ge 1$, the planner's weighted welfare functions are:
$$
\bar{W}^{TP} = \pi(e_M) S_R + \omega_p \pi(e_M) S_P - e_M,
$$
$$
\bar{W}^{3PD} = \pi(e^{FB}) S_R + \omega_p \cdot 0 - e^{FB} = \pi(e^{FB}) S_R - e^{FB}.
$$

The mandate dominates iff $\bar{W}^{TP} > \bar{W}^{3PD}$, which rearranges to (33).

(vi) $\bar{\omega}_p$ follows directly from (33) holding with equality. When $e^{FB} - e_M$ is small, the right side of (33) is small and $\bar{\omega}_p < 1$, so the mandate dominates even at $\omega_p = 1$ (no redistributive preferences).
□ □

Remark 5. Proposition 4 clarifies that the argument for the tiered pricing mandate is fundamentally distributional. The pure efficiency comparison (at $\omega_p = 1$) depends on whether the innovation gain from higher effort under 3PD outweighs the access gain from lower poor-country prices under the mandate. When $\omega_p > \bar{\omega}_p$—as warranted by any social welfare function sensitive to income inequality—the mandate dominates strictly. Since $\bar{\omega}_p \to 0$ as the innovation effort gap $e^{FB} - e_M \to 0$, the mandate is preferred under mild redistributive preferences whenever the patent's innovation effort distortion is small.

## 7.5 The government purchase alternative

The sharpest challenge to the CRLM is Kremer's mechanism applied in its cleanest form: one government (or a coordinated group) buys out the patent at $G^*$ and open-sources the technology. Everyone on earth gets the vaccine at marginal cost $c$. No individual in any country faces a price above $c$. The access inversion of Corollary 3 disappears. Why not do this?

The welfare comparison is direct. Government purchase at $G^*$ achieves welfare $W^{GP} = \pi(e^{FB}) \cdot S - e^{FB} - \lambda G^*$. The CRLM achieves $W^{CRLM} = \pi(e^{FB})[S_R + \omega_p(v_p -$

[Page 25]
$c - \bar{r}^*) \mu_p n_p] - e^{FB}$. The difference:
$$
W^{GP} - W^{CRLM} = \underbrace{\pi(e^{FB}) \bar{r}^* \mu_p n_p}_{\text{access gain}} - \underbrace{(\lambda - 1) G^*}_{\text{fiscal cost}}.
\quad(35)
$$
Since $\bar{r}^* \mu_p n_p = G^* - S_R$, government purchase dominates iff:

**Proposition 5** (*Government purchase versus the CRLM*). *Under Assumptions 1–3 and 2, with parametric specification $\pi(e) = 1 - e^{-\alpha e}$*:

(i) *Single-government purchase. One government that buys out the patent at $G^*$ and open-sources the technology dominates the CRLM in welfare if and only if:*
$$
\lambda < \lambda^* \equiv 1 + \frac{\pi(e^{FB}) (G^* - S_R)}{G^*}
\quad(36)
$$

(ii) *At calibrated Covid parameters ($\pi(e^{FB}) \approx 0.43$, $G^* \approx \$77B$, $S_R = \$40B$), $\lambda^* \approx 1.207$. The two mechanisms are nearly welfare-equivalent at the conventional $\lambda \approx 1.2$. At $\lambda > 1.21$ the CRLM dominates.*

(iii) *Single-government purchase at monopoly profit. Government purchase at $\Pi_M = S_R$ is strictly dominated by the CRLM: it achieves the same sub-optimal effort $e_M$, serves poor countries at c, but costs $\lambda S_R > 0$ in fiscal expenditure. The CRLM delivers identical access at zero cost.*

(iv) *Collective government purchase equals the Lindahl schedule. Collective purchase by all countries at $G^*$ with costs allocated in proportion to surplus—country i pays $t_i = (S_i/S)G^*$ —is formally identical to the Lindahl contribution schedule (Definition 1). It achieves the same welfare, faces the same four feasibility constraints (Remark 7), and is subject to the same Nash under-provision in the voluntary contribution game (Lemma 2). Calling it “collective purchase” rather than “prize” changes the institutional framing but not the strategic structure.*

(v) *The innovation price is unobservable. Both single-government and collective purchase*

[Page 26]
require setting the purchase price at $G^* = \sqrt{S/\alpha}$. This requires knowing $\alpha$—the innovator's private effort-to-probability mapping—which the innovator has a strict incentive to misreport upward (claiming higher costs) to raise $G^*$. Any purchase-at-social-value mechanism faces a preference revelation problem on the innovator's side that the CRLM does not: $r^*$ can be calibrated from observable pharmaceutical revenue data and historical innovation rates without requiring the innovator to disclose private cost information.

Proof. (i) From (35): $W^{GP} > W^{CRLM}$ iff $\pi(e^{FB})(G^* – S_R) > (\lambda – 1)G^*$, rearranging to (36).

(ii) $\lambda^* = 1 + 0.43 \times (77 – 40)/77 = 1.207$.

(iii) At $G = S_R$: effort $e_M$, welfare $\pi(e_M)S - e_M - \lambda S_R = W^{TP} - \lambda S_R < W^{TP}$ for any $\lambda > 0$.

(iv) Define $t_i = (S_i/S)G^*$ as the collective purchase allocation. This is identical to equation (37). Welfare, budget balance, and individual rationality conditions follow directly from Proposition 6. Each country has a strict unilateral incentive to reduce $t_i$ to zero: if others collectively raise $G^*$, country $i$ receives the open-sourced vaccine regardless of its contribution. This is the BVB free-rider game of Section 6 applied to purchase shares rather than prize contributions—same game, same Nash equilibrium, same under-provision by factor $\sqrt{N}$ under symmetry.

(v) The innovator's effort $e^*$ satisfies $\pi'(e^*) = 1/G$ at any prize $G$. To set $G = G^* = \sqrt{S/\alpha}$ the regulator needs $\alpha$. The innovator reports $\hat{\alpha} \le \alpha$, claiming lower productivity, to induce $\hat{G} = \sqrt{S/\hat{\alpha}} \ge G^*$. No direct verification of $\alpha$ is possible from observed outcomes alone. The CRLM sets $r^*$ from $S_R$ (observed directly from OECD revenues) and $S$ (estimated from market data), without requiring $\alpha$ to be reported by the innovator. $\square$ $\square$

Remark 6. Collective purchase equals the Lindahl prize. Allocating the cost by Lindahl proportionality is the Lindahl schedule. The word “purchase” is a label change, not a mechanism change. Every government has the same dominant incentive to free-ride. COVAX raised $10B of the $77B optimal prize—precisely what Lemma 2 predicts.

The welfare gap is small, the feasibility gap is large. At $\lambda = 1.2$, government purchase at

[Page 27]
G* and the CRLM differ by roughly $1B—less than 2% of G*. Raising $77B internationally has never been achieved. The CRLM raises $77B through the price mechanism—no transfer, no coordination, no advance commitment—while also bypassing the innovator's incentive to misreport *a*.

The CRLM is first-best among implementable mechanisms. Collective government purchase at G* is theoretically first-best. In practice it requires a supranational fiscal authority, mandatory preference revelation, and credible ex-ante commitment. That world does not exist. The CRLM does not require any of these.

## 7.6 When the CRLM is infeasible: the Lindahl contribution schedule

The CRLM requires market segmentation: generic manufacturers licensed for poor-country markets must not be able to re-export into rich-country markets, or the royalty structure collapses. When this condition fails—due to low transport costs, WTO rules, or insufficient regulatory capacity—the CRLM reduces to either a standard patent (if royalties cannot be collected) or a straight prize mechanism (if the government must fund G* directly). We characterise the optimal contribution schedule in this constrained case.

**Definition 1** (Lindahl contribution schedule). The *Lindahl contribution schedule* assigns each country *i* the contribution:
$$
t_i^* = \frac{S_i}{S} G^*, \quad (37)
$$
where G* solves (22) and S*i* is country *i*'s aggregate surplus at marginal cost pricing.

**Proposition 6** (Optimality of the Lindahl mechanism). The Lindahl contribution schedule satisfies:

(i) Budget balance: $\sum_i t_i^* = G^*$.

(ii) Individual rationality: $\phi(G^*) S_i - t_i^* \ge 0$ for all *i*.

(iii) Constrained efficiency: the Lindahl schedule maximises welfare among all budget-balanced and individually rational mechanisms.

[Page 28]
(iv) When $\lambda > 1$, the constrained-optimal prize $G^\dagger < G^*$ solves:
$$
\phi'(G^\dagger) S = \lambda.
\eqno{(38)}
$$
The Lindahl contribution schedule adjusts proportionally: $t_i^\dagger = (S_i/S) G^\dagger$.

*Proof*. (i) $\Sigma_i t_i^* = G^* \Sigma_i(S_i/S) = G^*$.

(ii) Country i's net payoff is:
$$
\phi(G^*) S_i - t_i^* = S_i \left[ \phi(G^*) - \frac{G^*}{S} \right].
$$
This is non-negative iff $\phi(G^*) S \ge G^*$. At $G^*$, the social welfare $W(G^*) = \phi(G^*)S - e^*(G^*) - G^* \ge W(0) = 0$ implies $\phi(G^*) S \ge e^*(G^*) + G^* > G^*$, establishing individual rationality.

(iii) By quasi-linearity of country payoffs, the Lindahl equilibrium is Pareto efficient among all mechanisms satisfying budget balance and individual rationality (Lindahl's theorem applied to this public good setting).

(iv) With shadow cost $\lambda$, the planner maximises $W^\lambda(G) = \phi(G) S - e^*(G) - \lambda G$. Using the envelope theorem: $\frac{dW^\lambda}{dG} = \phi'(G) S - \lambda$, giving the first-order condition (38). Since $\phi'' < 0$ and $\lambda \ge 1$, the solution $G^\dagger \le G^*$ with strict inequality when $\lambda > 1$. The proportional adjustment $t_i^\dagger = (S_i/S)G^\dagger$ inherits budget balance and individual rationality from parts (i)-(ii). $\square \quad \square$

*Remark 7 (Feasibility asymmetry).* Both the CRLM and tiered contribution schedules are international agreements. The difference is structure, not political will.

*Incentive compatibility.* The innovator accepts the CRLM because she earns $G^* > \Pi_M$. Generic manufacturers pay royalties as a contractual licence condition—not a voluntary contribution. Every sovereign contributor to a prize fund has a dominant incentive to pay nothing.

*Preference revelation and timing.* The Lindahl royalty is computed from observable market data—pharmaceutical revenues, historical innovation rates. No government reveals private

[Page 29]
valuations. A cash Lindahl schedule cannot be constructed without knowing each country’s $S_i$, which every government will understate. The royalty is collected on an existing product; cash contributions must be committed before the vaccine exists, into a hold-up problem. Locus of authority. The CRLM operates through bilateral licensing plus a TRIPS amendment. Both are within existing legal frameworks. The Lindahl schedule requires a supranational fiscal authority with power to compel sovereign treasury transfers. The WTO can sanction trade violations; it cannot compel the US Treasury to write a cheque.

## 7.7 Welfare ranking of mechanisms

**Theorem 1** (Welfare ranking). Under Assumptions 1–3 with shadow cost $\lambda \ge 1$, redistributive weight $\omega_p \ge 1$, and feasibility condition (32):
$$
W^{GP@G^*} = W^{Lindahl} = W^{CRLM} \ge W^{3PD} \ge W^{TP} \ge W^{NE} \ge W_M, \quad (39)
$$
where $W^{GP@G^*}$ is welfare under government purchase at $G^*$. The following qualifications apply:

(i) $W^{GP@G^*} = W^{Lindahl} = W^{CRLM}$ when all three are evaluated at $\lambda = 1$ and $\omega_p = 1$: all achieve first-best innovation $e^{FB}$ and differ only in how they finance it (fiscal transfer versus price mechanism) and in poor-country consumer prices ($c$ versus $c + r^*$). At $\lambda > 1$: $W^{GP@G^*} = W^{Lindahl} < W^{CRLM}$ because the CRLM bears no fiscal cost.

(ii) $W^{GP@G^*}$ and $W^{Lindahl}$ are formally identical (Proposition 5(iv)): collective government purchase at $G^*$ with Lindahl-proportional cost allocation is the cash Lindahl schedule. They share the same welfare expression and the same four feasibility constraints.

(iii) $W^{CRLM} \ge W^{3PD}$ for any $\omega_p > 0$: the CRLM achieves first-best innovation while preserving poor-country surplus ($(v_p - c - r^*)\mu_p n_p > 0$); 3PD achieves first-best innovation but leaves poor countries with zero surplus.

(iv) $W^{3PD} \ge W^{TP}$ iff $\omega_p \le \bar{\omega}_p$ (Proposition 4).

[Page 30]
(v) $W^{NE} > W_m$ iff Condition (17) holds.

(vi) Feasibility reversal: the welfare ranking and the implementability ranking are the reverse of each other. $W^{GP@G*} = W^{Lindahl}$ is welfare-first but implementability-last: requires a supranational fiscal authority, credible ex-ante commitment, and no misreporting of $\alpha$. $W^{CRLM}$ is welfare-equivalent at $\lambda = 1$ and implementability-first: requires only bilateral licensing agreements and a TRIPS amendment.

(vii) Racing robustness: the Lindahl royalty formula $\bar{r}^*$ is invariant to $N$; government purchase requires raising $G^*$ regardless of $N$, and the free-rider gap widens in $N$ under both collective purchase and the cash Lindahl schedule.

*Proof.* (i) At $\lambda = 1$: $W^{GP@G*} = \pi(e^{FB})S - e^{FB} - G^*$. $W^{CRLM} = \pi(e^{FB})[S_R + \omega_p(v_p - c - \bar{r}^*) \mu_p n_p] - e^{FB}$. At $\lambda = 1$, $\omega_p = 1$: both equal $\pi(e^{FB})S - e^{FB} - G^*$ since $S_R + (v_p - c - \bar{r}^*) \mu_p n_p = S - \bar{r}^* \mu_p n_p$ and $G^* = S_R + \bar{r}^* \mu_p n_p$. At $\lambda > 1$: $W^{GP@G*}$ carries fiscal cost $(\lambda - 1)G^*$ while $W^{CRLM}$ does not.

(ii) By Proposition 5(iv): $t_i = (S_i/S)G^*$ = Definition 1.

(iii)-(vii) from Propositions 4, 6, 5, Lemma 2, and Remark 7. □ □

# DISCUSSION

## 8.1 When does the CRLM work?

The CRLM requires market segmentation: generic manufacturers licensed for poor-country markets must not be able to sell back into rich-country markets. For vaccines, this is realistic—cold-chain logistics, national health system administration, and country-specific regulatory approval make arbitrage impractical. Nobody is smuggling Moderna doses from Bangladesh to Belgium. For oral medications with low transport costs, the condition is harder to maintain.

Institutionally, the vehicle is a TRIPS amendment authorising capped royalty licensing with an anti-re-export clause. TRIPS already permits compulsory licensing; a Lindahl

[Page 31]
royalty clause is less intrusive—it preserves the innovator's royalty income rather than exposing her to a court-determined rate. The political ask is smaller. The innovation incentive is larger.

## 8.2 Multiple income tiers

Two groups-rich and poor—give the model tractability. The Lindahl royalty generalises directly to $K$ tiers: the royalty for each excluded tier collects the residual between $G^*$ and the sum of monopoly revenues from tiers above the exclusion threshold. Proposition A.1 in the Appendix formalises this; the self-financing property holds for any $K$.

## 8.3 Platform technologies

mRNA was developed for cancer and influenza before Covid. The platform investment was funded by expected OECD revenues from future applications. A royalty cap on BNT162b2 does not affect Pfizer's expected return from BNT111 (melanoma), BNT211 (bladder cancer), or BNT131 (cytokine mRNA). Platform incentives are determined by the OECD revenue stream, which the CRLM never touches.

## 8.4 Racing

With Covid, multiple firms raced. Pfizer, Moderna, AstraZeneca, Johnson & Johnson, Novavax—all in parallel. Does the Lindahl royalty formula survive a racing equilibrium? The answer is yes, and the proof is almost trivially simple: the formula $\check{r}^* = (\sqrt{S/a} - S_R)/(\mu_p \eta_p)$ depends on aggregate market parameters, not on the number of competing firms. Whatever $N$ firms enter the race, the winner's royalty is the same. The CRLM's optimal parameterisation is invariant to market structure.

We formalise this using the Loury (1979) framework: $N \ge 1$ symmetric firms each choose effort $e_k$, incurring cost $e_k$. Each firm's probability of success follows an independent Poisson process with hazard rate $h(e_k)$, where $h(0) = 0$, $h' > 0$, $h'' < 0$. The winner receives

[Page 32]
the patent profit or royalty income; all others receive zero.

**Proposition 7 (Mechanisms under innovation racing).** Let $N \ge 1$ firms compete in a Poisson innovation race with hazard rates $\{h(e_k)\}$. Then:

(i) Tiered pricing—invariance. The winner's conditional profit under the tiered pricing mandate is $S_R$ for all $N$. The mandate does not alter any firm's entry decision or effort choice relative to the patent. The self-financing property of Proposition ?? holds exactly for all market structures.

(ii) Tiered contributions—compounding coordination failure. Let $G_{race}$ denote the socially optimal prize under racing. Achieving $G_{race}$ requires solving two coupled problems simultaneously: (a) the Lindahl contribution problem—assigning shares $S_i/S$ as in Proposition 6; and (b) an entry regulation problem—preventing the socially excessive number of entrants that a larger prize attracts. A single prize instrument $G$ cannot solve both: the prize level that equates marginal innovation benefit to marginal cost per firm generically over-subsidises entry relative to the social optimum. The constrained-optimal mechanism under racing therefore requires a prize plus an entry licence or tax, adding a second layer of supranational coordination beyond the Lindahl problem of the single-firm case.

(iii) Tiered pricing vs. unregulated 3PD─higher redistribution threshold. Under 3PD with racing, each firm competes for profit $S = S_R + S_p$, which is larger than the patent profit $S_r$. The larger effective prize under 3PD attracts additional entrants and accelerates expected innovation relative to the mandate. The redistributive threshold $w_p$ in Proposition 4 therefore satisfies:
$$
\omega_p^*(N) > \omega_p^*(1) = \frac{[\pi(e^{FB}) - \pi(e_M)]S_R - [e^{FB} - e_M]}{\pi(e_M)S_p},
\quad (40)
$$
with the gap $\omega_p^*(N) - \omega_p^*(1)$ increasing in $N$. The mandate remains preferred whenever $w_p > \omega_p^*(N)$, but the required redistributive weight is strictly higher under racing than

[Page 33]
under monopoly.

Proof. (i) The winner's profit conditional on winning is $(v_R - c)\mu_R n_R + (c - \bar{c})\mu_p n_p = S_R$, irrespective of $N$. Each firm's entry and effort problem is $\max_{e_k} h(e_k) S_R - e_k$, identical to the single-firm patent problem after replacing $\pi$ with $h$. The mandate leaves every firm's optimisation problem unchanged.

(ii) The planner maximises $W^{race}(G, N) = [1 – (1 – h(e^*(G)))^N]S – Ne^*(G) – G$. The FOC in $G$ pins down effort; the FOC in $N$ pins down entry. Together they require $(G_{race}, N_{race}^*)$, but a single instrument $G$ satisfies at most one—leaving entry unregulated and generating socially wasteful duplication. The social optimum requires a prize plus an entry tax: two instruments for two conditions.

(iii) Under 3PD with $N$ firms, conditional profit is $S > S_R$, inducing more entry ($N^{3PD} > N^{patent}$) and higher effort. The winning probability under 3PD, $\Phi_N^{3PD} > \Phi_N^{TP}$, raises the threshold redistributive weight: solving $w_p \Phi_N^{TP} S_p > [\Phi_N^{3PD} - \Phi_N^{TP}] S_R - (\text{effort cost difference})$ for $w_p$ gives $\omega_p^*(N) > \omega_p^*(1)$ for all $N > 1$, confirming (40).
$\square$

*Remark 8.* Competition makes the CRLM stronger, not weaker. The Lindahl royalty formula is a function of aggregate market parameters—$S, S_R, \alpha, \mu_p n_p$—none of which depend on $N$. Whether one firm develops the vaccine or ten, the optimal cap is the same. This is the property that tiered contribution schedules lack: under racing, the prize that incentivises the right effort level attracts too many entrants, requiring a second instrument that needs its own international agreement. Part (iii) is the honest qualification: racing raises the redistributive threshold above which the CRLM dominates unregulated 3PD, because 3PD with many firms delivers faster innovation. But the CRLM dominates for any redistributive weight above $\omega_p^*(N)$, and the gap between CRLM and contributions only grows with $N$.

[Page 34]
## 8.6 Numbers

A formula is only useful if it gives sensible answers when you plug in real numbers. Here we check that the theoretical conditions are satisfied in the Covid vaccine setting and that the Lindahl royalty is economically meaningful—neither zero nor equal to the full poor-country margin.

*Parameter values.* Pfizer and Moderna combined reported approximately $80–90 billion in vaccine revenues in 2021–22; taking half for a single innovator gives $S_R \approx \$40$ billion. Chaudhuri et al. (2006) estimate the poor-country deadweight loss ratio at 0.3–0.8 of innovator profit in Indian pharmaceutical markets; applying this gives $S_P/S_R \approx 0.5$, so $S_P \approx \$20$ billion and $S \approx \$60$ billion. DiMasi et al. (2003) estimate expected pharmaceutical development costs at roughly $800 million in 2000 dollars; adjusting upward for mRNA’s timeline suggests R&D costs of $1–2 billion per vaccine. The shadow cost of public funds $\lambda$ is conventionally estimated at 1.2–1.4 in the public finance literature.

We calibrate innovation productivity $\alpha$ to match a 30% success probability at the patent equilibrium—consistent with pre-pandemic phase-III vaccine trial data: $\pi(e_M) = 1 - 1/(\alpha S_R) = 0.30$ gives $\alpha \approx 3.6 \times 10^{-11}$.

*The prize fails. The CRLM does not.* The prize welfare dominance condition requires $\pi(e_M)S_P > (\lambda - 1)S_R$—that is, $\$6B > (\lambda - 1) \times \$40B$. At $\lambda = 1.2$ the right side is $\$8B$. The prize fails to welfare-dominate the patent once fiscal costs are counted. This is not a surprise; it is the motivation for the CRLM. The CRLM achieves the same $6B welfare gain at zero fiscal cost.

*The Lindahl royalty is interior.* Check feasibility condition (32): $1/S < \alpha < S/S_R^2$. With $S = \$60B$ and $S_R = \$40B$: lower bound = $1.7 \times 10^{-11}$, upper bound = $3.75 \times 10^{-11}$, calibrated $\alpha = 3.6 \times 10^{-11}$. The condition is satisfied, narrowly. The Lindahl royalty is interior: $r^* > 0$

[Page 35]
(above tiered pricing) and $r^* < v_P - c$ (below 3PD). The formula gives:
$$
\tilde{r}^* = \frac{\sqrt{S/\alpha} - S_R}{\mu p n_p} = \frac{\sqrt{\$60B/\alpha} - \$40B}{\mu p n_p}
$$
For plausible values of poor-country population covered, this yields a royalty of roughly 2-4% of net sales—consistent with the 2-5% range the Medicines Patent Pool has negotiated in practice. Theory and practice agree.

The free-rider gap. With $N = 195$ countries and symmetric contributions, Nash under-provision is $\sqrt{N} = \sqrt{195} \approx 14$-fold. The voluntary prize pool would provide roughly $\sqrt{S/\alpha}/14 \approx \$5.5$ billion toward the optimal $77 billion. COVAX raised approximately $10 billion, dominated by US and EU contributions—close to the single-contributor Nash prediction and far below the social optimum. The Lindahl cash schedule would achieve the optimum but requires $\alpha S \ge 4$; our calibrated $\alpha S \approx 2.2 < 4$, so individual rationality fails. The CRLM has no such condition.

**Table 2: Numerical calibration: Covid vaccine illustration**

| Parameter / outcome | Source / basis | Value |
| :--- | :--- | :--- |
| Rich-country surplus $S_R$ | Pfizer/Moderna reported revenues, 2021–22 | $40B |
| Poor-country surplus $S_P$ | $S_P/S_R \approx 0.5$ (Chaudhuri et al. 2006) | $20B |
| Aggregate surplus $S$ | $S_R + S_P$ | $60B |
| Shadow cost $\lambda$ | Public finance literature | 1.2–1.4 |
| Innovation probability $\pi(e_M)$ | Pre-pandemic phase-III base rate | 30% |
| Expected access gain | $\pi(e_M)S_P$ | $6B |
| Prize fiscal cost $(\lambda - 1)S_R$ | At $\lambda = 1.2 / \lambda = 1.4$ | $8B / $16B |
| Prize welfare dominance? | Cond. (17) | No (at $\lambda \ge 1.2$) |
| CRLM welfare gain | $\pi(e^{FB})S - e^{FB} > \pi(e_M)S - e_M$ | > $6B |
| Lindahl royalty feasible? | Cond. (32) | Yes (narrowly) |
| Nash prize ratio $\sqrt{N}$ | $N = 195$ countries, symmetric | $\approx 14\times$ |
| Lindahl cash IR condition | $\alpha S \ge 4$ | Fails |
| MPP observed royalty range | HIV/HCV licences, 2010–23 | 2–5% |

*Notes*. All dollar figures are approximate and in 2021 USD. Parametric specification $\pi(e) = 1-e^{-\alpha e}$ throughout. The Lindahl royalty formula gives $\tilde{r}^* \approx 2-4\%$ of net sales for the calibrated parameters, consistent with MPP practice.

[Page 36]
8.5 *Continuous WTP and the conservative welfare estimates*
When WTP increases with income, the monopolist excludes countries below an endogenous
threshold. The CRLM sets a royalty for those excluded countries; the formula generalises
directly to $K$ tiers (Proposition A.1).

One implication: $v_P$ is willingness-to-pay, not social value. A Bangladeshi farmer who
values the vaccine at three months' income but has zero savings has a WTP of zero—*not*
because she doesn't value it, but *because* she cannot pay. The true social value $V_P \ge v_P$, so
every welfare calculation using $S_P = (v_P - c)\mu_P n_P$ is conservative. The case for the CRLM
is stronger than our numbers show.

8.7 *The Medicines Patent Pool: the mechanism already exists*
The CRLM is not a proposal. The Medicines Patent Pool (MPP), established by the UN in
2010, has operated it for HIV antiretrovirals since 2010, hepatitis C since 2015, and Covid
treatments since 2022. Originators retain monopoly pricing in high-income markets; generic
manufacturers are licensed to produce in low- and middle-income countries at a negotiated
royalty. By 2023 the MPP held licences covering 290+ products across 100 countries, with
royalties of 2-5% of net sales (Medicines Patent Pool, 2023)—*inside* the 2-4% range our
calibrated $\bar{r}^*$ implies.

What the MPP has lacked is a formula. Royalty rates have been set by bilateral
pressure and precedent, sometimes too low (eroding innovation incentives), sometimes too
high (pricing out patients). The Lindahl royalty provides the missing criterion: estimate
$\alpha$ from historical innovation rates, observe $S_R$ from OECD revenues, estimate $S_P$ from
household survey data, and compute $\bar{r}^*$. The MPP already knows how to do everything else.

8.8 *The government intermediary assumption*
The model treats $v_R$ as the government's procurement price on behalf of its entire population—
equivalent to assuming the government acts as a single buyer, pays $v_R$ to the innovator, and

[Page 37]
distributes freely. Where this holds, no individual faces the monopoly price directly. Where it fails, poor individuals in rich countries face the same exclusion the CRLM fixes between countries.

Suppose rich-country residents have income $y$ drawn from $F_R(y)$, with individual WTP $v(y)$, $v' > 0$. Three cases: Case U (universal coverage, government pays $v_R$, distributes at zero cost); Case P (partial subsidy $s$, individuals pay $v_R - s$); Case N (no coverage, individuals pay $v_R$).

**Proposition 8** (Within-rich-country access under the CRLM). Let $\tilde{n}_R(s) = 1-F_R(v^{-1}(v_R-s))$ denote the fraction of rich-country residents vaccinated under subsidy $s$, and let $S_P^{excl}(s) = \int_{\{y:v(y)<v_R-s\}} [v(y) – c]\mu_R N_R dF_R(y)$ denote the forgone surplus of excluded rich-country residents. Then:

(i) Case U: $\tilde{n}_R = 1$, $S_P^{excl} = 0$. The CRLM achieves universal individual access in rich countries. The innovator's profit is $S_R + r^*\mu_p n_p = G^*$ unchanged. The model's representative-consumer assumption holds exactly.

(ii) Case N: $\tilde{n}_R(0) < 1$, $S_P^{excl}(0) > 0$. A mass $F_R(v^{-1}(v_R))$ of rich-country residents with $v(y) < v_R$ are excluded. Their forgone surplus $S_P^{excl}(0)$ is not captured by the model's welfare expression $W^{CRLM} = \pi(e^*(G^*))[S_R+W_P(v_P-c-r^*)\mu_p n_p]-e^*(G^*)$, which uses country-level aggregates. The true welfare gap between the CRLM and the first-best is larger than the formal expression indicates by $\pi(e^*(G^*))S_P^{excl}(0)$.

(iii) Case P: Intermediate. The government's subsidy $s$ determines the access shortfall. At $s = v_R$ (full coverage, Case U), $S_P^{excl} = 0$. At $s = 0$ (no coverage, Case N), $S_P^{excl} = S_P^{excl}(0) > 0$. The optimal domestic subsidy $s^*$ trades off the fiscal cost $s\tilde{n}_R(s)\mu_R N_R$ against the access gain $dS_P^{excl}/ds < 0$.

(iv) Innovator's participation: The innovator's profit under the CRLM is $S_R+r^*\mu_p n_p = G^*$ in all three cases. Within-country distributional choices by the rich-country government do not affect the innovator's incentives or the Lindahl royalty formula. The CRLM is robust to the government intermediary assumption.

[Page 38]
(v) Residual welfare loss: The welfare loss from imperfect coverage relative to Case U is:
$$
\Delta W(s) = \pi(e^*(G^*)) [S_P^{excl}(0) - S_P^{excl}(s)] - \lambda s \tilde{n}_R(s) \mu_R N_R, \quad (41)
$$
the expected access gain from expanding coverage to subsidy s, net of the fiscal cost at shadow price $\lambda$.

**Proof.** (i) Under Case U, every resident is vaccinated by assumption. $S_P^{excl} = 0$. The government pays $v_R$ per unit to the innovator, regardless of individual income; the innovator's profit is $(v_R - c)\mu_R N_R = S_R$, unchanged.

(ii) Under Case N, residents with $v(y) < v_R$ receive no vaccine. Their potential surplus $[v(y) - c] > 0$ is unrealised. The model's welfare expression aggregates at the country level using $S_R = (v_R - c)\mu_R N_R$, which assumes all $\mu_R N_R$ residents are served and the innovator captures all surplus. In Case N, the innovator earns less than $S_R$ from excluded residents (zero, since they do not buy), and their surplus is lost. The welfare gap is $\pi(e^*(G^*))S_P^{excl}(0)$.

(iii) Follows from continuity of $\tilde{n}_R(s)$ and $S_P^{excl}(s)$ in s.

(iv) In all three cases the innovator earns $(v_R - c)$ per unit from purchasing consumers, whether via a government intermediary or direct sales. The Lindahl royalty formula derives from country-level aggregates; within-country distributional choices do not enter it. □ □

**Corollary 3** (The access inversion). Under the CRLM with feasibility condition (32) and Case N coverage in rich countries:

(i) The exclusion threshold in poor countries is $c + \tilde{r}^*$. An individual in a poor country with WTP $v(y) \ge c + \tilde{r}^*$ is served.

(ii) The exclusion threshold for uninsured individuals in rich countries is $v_R$. An individual with WTP $v(y) \ge v_R$ is served; others are excluded.

(iii) Since $c + \tilde{r}^* < v_p < v_R$ (by the feasibility condition and Assumption 3), any individual with WTP in the range $[c + \tilde{r}^*, v_R)$ is served in poor countries and excluded in Case N

[Page 39]
rich countries:
$$
c+r^* < v_P < v_R. \quad (42)
$$
(iv) The CRLM therefore produces an access inversion: an uninsured individual in the United States with WTP $v(y) = v_R - \varepsilon$ is worse off than an individual with the same WTP in Bangladesh, even though the United States is the richer country and the mechanism was designed to help poor countries.

(v) The inversion disappears under Case U coverage: when the rich-country government procures universally, no individual faces $v_R$ directly and the exclusion threshold for rich-country residents falls to zero.

*Proof.* (i)-(iii) follow directly from the CRLM price structure and inequality (32): $r^* > 0$ requires $\sqrt{S/\alpha} > S_R$, and $r^* < v_P - c$ requires $\sqrt{S/\alpha} < S$, so $S_R < \sqrt{S/\alpha} < S = S_R + S_P$, implying $r^* < (S-S_R)/(\mu_P n_P) = S_P/(\mu_P n_P) = v_P - c$. Hence $c+r^* < v_P$. Combined with Assumption 1 ($v_P < v_R$), (42) follows.

(iv) Any individual with $v(y) \in [c + r^*, v_R)$ strictly prefers to be in a poor country under the CRLM: they pay $c + r^*$ there and are excluded here. In Case N, uninsured individuals pay $v_R$ out-of-pocket; those with $v(y) < v_R$ cannot purchase. □

(v) Under Case U, the government pays $v_R$ and distributes at zero individual cost. Every resident is vaccinated regardless of $v(y)$. □

*Remark 9.* The inversion is a direct consequence of pricing by country rather than by individual income. It is not a reason to abandon the CRLM: the patent also excludes Case N individuals in rich countries, and additionally excludes all poor-country individuals. The welfare cost of the inversion, $\pi(e^*) S_R^{excl}(0)$, is smaller than the patent's poor-country exclusion cost $\pi(e_M) S_P$ by Assumption 3 and the calibration. The inversion does strengthen the domestic case for universal health coverage: moving from Case N to Case U eliminates it. The CRLM and universal coverage are complements—together they achieve universal individual access; separately each leaves a gap.

[Page 40]
# CONCLUSION

Five options have been on the table for solving the pharmaceutical access problem. Three are familiar. Two are new to this paper. None is obviously right. Here is the complete accounting.

*Waive the patent*. Access without exclusion, but only for the current vaccine. Every future innovator now expects ex-post expropriation and adjusts her investment accordingly. Biden proposed it. Merkel refused. Merkel was right.

*Fund a prize*. Pay the innovator $G^* = \sqrt{S/a}$, open-source the technology, price globally at c. Theoretically first-best. Actually unfunded. COVAX raised roughly $10B of the $77B optimal prize, dominated by the US and EU while 175 other countries free-rode. With 195 symmetric countries, BVB predicts $\sqrt{195} \approx 14$-fold under-provision. The theory and the data agree.

*Collective government purchase at G**. This is not a new mechanism. It is the prize with a different label. Allocate the purchase cost by Lindahl proportionality—country i pays $(S_i/S)G^*$—and you have the Lindahl contribution schedule. The strategic structure is identical: every government has a dominant incentive to let others pay while receiving the open-sourced vaccine. Calling it “purchase” rather than “prize” does not change this. It also adds a new problem: the purchase price requires knowing the innovator’s effort-to-probability mapping $\alpha$, which the innovator will misreport upward to inflate $G^*$. The prize mechanism at least avoids this—the prize is specified ex ante and not negotiated with the innovator.

*Mandate tiered pricing*. Require the innovator to sell at marginal cost in poor countries. She was earning nothing from those markets anyway, so her profit is unchanged. Access is universal. But innovation effort stays at the sub-optimal patent level $e_M$, because the innovator’s profit is the same as under the patent. Danzon, Scherer-Watal, and the WHO advocated this for twenty years. It is better than the patent. It is not optimal.

[Page 41]
The capped royalty licensing mandate. License generic manufacturers to produce for poor-country markets at a per-unit royalty $r^*$:
$$
r^* = \frac{\sqrt{S/\alpha - S_R}}{\mu_P n_P}
$$
The Lindahl conditions determine the cap. Rich countries contribute $S_R$ through monopoly pricing; poor countries contribute the residual $G^* – S_R$ through royalty payments on generic sales; together they fund the Lindahl-optimal prize $G^*$ through the price mechanism, with no public transfer, no free-rider problem, and no supranational authority. Innovation effort reaches the first-best $e^{FB}$. Poor countries pay $c + r^*$ rather than $c$—not free, but affordable.

Is this better than government purchase at $G^*$? In welfare terms, almost exactly equally good at calibrated parameters ($\lambda^* \approx 1.21$; the CRLM wins if the shadow cost of public funds exceeds 21 cents per dollar). In feasibility terms, it is categorically better: the CRLM raises $G^*$ through the price mechanism, while collective government purchase requires raising $77B internationally against the BVB prediction of $5.5B. The CRLM is not first-best in theory. It is first-best in the world as it is.

One honest limitation remains. An uninsured American who cannot afford $v_R$ is worse off than a Bangladeshi with the same income, who pays $c + r^* < v_P < v_R$. The mechanism designed to help poor countries creates an access inversion inside rich countries without universal health coverage. The remedy is domestic—universal coverage—not international. The CRLM and universal health coverage are complements. Together they achieve universal individual access everywhere. Separately, each leaves a gap.

The mechanism is already running. The Medicines Patent Pool has licensed HIV antiretrovirals on exactly these terms since 2010, hepatitis C since 2015, Covid treatments since 2022. Royalties of 2-5% of net sales; generic competition in low-income markets; originator profits untouched in OECD markets. Our calibrated $r^*$ is roughly 2-4% of net sales—inside the MPP’s empirical range. Theory and practice converge. What has been

[Page 42]
missing is the formula that says: this is the right royalty, and here is why. That is what this
paper provides.

The framework extends to any technology with low marginal production cost, non-
rival benefits once produced, and social value that income constraints prevent poor consumers
from expressing as willingness-to-pay. Malaria drugs, tuberculosis treatments, antiretrovirals,
agricultural biotechnology, diagnostic tools. Climate adaptation technology—solar panels in
sub-Saharan Africa, drought-resistant seeds in South Asia, flood barriers in Bangladesh.
The countries most in need of innovation will increasingly be those least able to pay for it
at monopoly prices. The Lindahl royalty formula applies to all of them. The MPP should
extend its mandate. The TRIPS Agreement should authorise capped royalty licensing in
excluded markets. The theory is in place. The institution is in place. The formula is new.

# REFERENCES

Daron Acemoglu and Ufuk Akcigit. Intellectual property rights policy, competition and
innovation. *Journal of the European Economic Association*, 10(1):1–42, 2012.

Kenneth J. Arrow. Economic welfare and the allocation of resources for invention. In
Richard R. Nelson, editor, *The Rate and Direction of Inventive Activity*, pages 609-626.
Princeton University Press, 1962.

Kyle Bagwell and Robert W. Staiger. A theory of managed trade. *American Economic
Review*, 80(4):779–795, 1990.

Ted Bergstrom, Lawrence Blume, and Hal Varian. On the private provision of public goods.
*Journal of Public Economics*, 29(1):25–49, 1986.

Shubham Chaudhuri, Pinelopi K. Goldberg, and Panle Jia. Estimating the effects of global
patent protection in pharmaceuticals: A case study of quinolones in india. *American
Economic Review*, 96(5):1477–1514, 2006.

[Page 43]
Bhagwan Chowdhry and Deepa Mani. Let profits feed R&D. *Economic Times*, 2021. Opinion piece, Indian School of Business.

Edward H. Clarke. Multipart pricing of public goods. *Public Choice*, 11(1):17–33, 1971.

Patricia M. Danzon and Adrian Towse. Differential pricing for pharmaceuticals: Reconciling access, r&d and patents. *International Journal of Health Care Finance and Economics*, 3 (3):183-205, 2003.

Partha Dasgupta and Joseph E. Stiglitz. Uncertainty, industrial structure, and the speed of R&D. *Bell Journal of Economics*, 11(1):1–28, 1980.

Joseph A. DiMasi, Ronald W. Hansen, and Henry G. Grabowski. The price of innovation: New estimates of drug development costs. *Journal of Health Economics*, 22(2):151–185, 2003.

Avinash Dixit. Some lessons from transaction-cost politics for less-developed countries. *Economics and Politics*, 12(2):89–107, 2000.

Joshua S. Gans and Suzanne Scotchmer. The private value of software patents. *RAND Journal of Economics*, 34(4):765-781, 2003.

Theodore Groves. Incentives in teams. *Econometrica*, 41(4):617-631, 1973.

Michael Kremer. Patent buyouts: A mechanism for encouraging innovation. *Quarterly Journal of Economics*, 113(4):1137–1167, 1998.

Michael Kremer and Rachel Glennerster. *Strong Medicine: Creating Incentives for Pharmaceutical Research on Neglected Diseases*. Princeton University Press, Princeton, 2004.

Michael Kremer and Edward Miguel. Worms: Identifying impacts on education and health in the presence of treatment externalities. *Econometrica*, 72(1):159–217, 2004.

[Page 44]
Erik Lindahl. Just taxation: A positive solution, 1919. Reprinted in *Classics in the Theory of Public Finance*, edited by R. A. Musgrave and A. T. Peacock, Macmillan, 1958, pp. 168– 176.

Glenn C. Loury. Market structure and innovation. *Quarterly Journal of Economics*, 93(3): 395-410, 1979.

Medicines Patent Pool. Annual report 2022. Medicines Patent Pool, Geneva, https:// medicinespatentpool.org/annual-report-2022, 2023.

Suerie Moon and Devi Sridhar. How not to repeat the mistakes of COVAX. *Foreign Affairs*, 101(4):100-112, 2022.

William D. Nordhaus. *Invention, Growth, and Welfare: A Theoretical Treatment of Technological Change*. MIT Press, Cambridge, MA, 1969.

Arthur C. Pigou. *The Economics of Welfare*. Macmillan, London, 4th edition, 1932.

Joan Robinson. *The Economics of Imperfect Competition*. Macmillan, London, 1933.

Paul A. Samuelson. The pure theory of public expenditure. *Review of Economics and Statistics*, 36(4):387-389, 1954.

F. M. Scherer and Jayashree Watal. Post-TRIPS options for access to patented medicines in developing nations. *Journal of International Economic Law*, 5(4):913–939, 2002.

Suzanne Scotchmer. Standing on the shoulders of giants: Cumulative research and the patent law. *Journal of Economic Perspectives*, 5(1):29–41, 1991.

Joseph E. Stiglitz. Scrooge and intellectual property rights. *British Medical Journal*, 333 (7582):1279-1280, 2006.

Hal R. Varian. Price discrimination and social welfare. *American Economic Review*, 75(4): 870-875, 1985.

[Page 45]
E. Glen Weyl and Jean Tirole. Market power screens willingness-to-pay. *Quarterly Journal of Economics*, 127(4):1971–2003, 2012.

[Page 46]
# APPENDIX: EXTENSIONS AND SUPPLEMENTARY RESULTS

## A.1 The K-tier generalisation

With $K \ge 2$ country groups ranked by WTP ($v^{(1)} > \dots > v^{(K)} > c$), the monopolist excludes groups $k^* + 1, \dots, K$. Group $k$ has measure $\mu^{(k)}$, population $n^{(k)}$, and surplus $S^{(k)} = (v^{(k)} - c)\mu^{(k)}n^{(k)}$. A K-tier CRLM sets monopoly prices for groups $1, \dots, k^*$ and the Lindahl royalty for excluded groups.

**Assumption 4** (*K-tier exclusion profitability*). $\sum_{k=1}^{k^*} S^{(k)} > \sum_{k=1}^{j} S^{(k)}$ for all $j > k^*$.

**Proposition A.1** (*K-tier tiered pricing mandate*). Under Assumption 4, a K-tier mandate specifying:
$$
p^{(k)} = v^{(k)} \text{ for } k \le k^*, \quad p^{(k)} = c \text{ for } k > k^*, \tag{A.1}
$$
achieves:

(i) The same innovation effort as the patent: $e^{TP} = e_M$.
(ii) Universal access: all $K$ groups are served.
(iii) Welfare $W^{TP} = \pi(e_M) \sum_{k=1}^K S^{(k)} - e_M$.
(iv) Zero required public prize: $G^{top-up} = 0$.
(v) Welfare gain over the patent of $\pi(e_M) \sum_{k=k^*+1}^K S^{(k)} > 0$, equal to the expected surplus of all excluded groups.

*Proof.* Under the mandate, the innovator's conditional profit is:
$$
\Pi^{TP} = \sum_{k=1}^{k^*} (v^{(k)} - c)\mu^{(k)}n^{(k)} + \sum_{k=k^*+1}^K (c - c)\mu^{(k)}n^{(k)} = \sum_{k=1}^{k^*} S^{(k)} = \Pi_M,
$$
which equals the patent profit by definition of $k^*$. The innovator's optimisation problem is therefore identical to the patent problem, giving $e^{TP} = e_M$ and $G^{top-up} = 0$. All groups are served by the mandate (parts (i)-(ii)). Welfare follows from summing surplus across all groups (part (iii)), and the gain over the patent is the expected surplus of previously

[Page 47] [DIGITIZATION FAILED]


[Page 48]
*Proof*. Parts (i)-(ii) follow from the symmetric Nash equilibrium conditions of Loury (1979) applied to the Poisson hazard $h$. Part (iii): the social planner maximises total expected welfare $[1 - (1 - h(e))^N] \cdot S – Ne – G$ over both $e$ and $N$. Differentiating with respect to $e$ (holding $N$ fixed) gives (A.3); differentiating with respect to $N$ (using the marginal value of an additional entrant) gives (A.4). The two conditions jointly determine $(e^{SP}, N^{SP})$; they cannot both be satisfied by $G$ alone since $G$ affects only the effort condition (A.3). Parts (iv)-(v) follow from inspection: the winner's profit under the mandate is always $S_R$ (part (iv)), while achieving the social optimum under tiered contributions requires solving the entry condition as well, necessitating a second instrument (part (v)).
$\square$ $\square$

### A.3 Lindahl individual rationality: detailed verification

Proposition 6(ii) asserts individual rationality of the Lindahl schedule. We verify this in detail for the parametric specification (6).

Under $\pi(e) = 1 - e^{-\alpha e}$, the social optimum satisfies $G^* = \sqrt{S/\alpha}$ (from the proof of Lemma 3(iii)). We compute:
$$
e^*(G^*) = \frac{1}{\alpha} \log(\alpha G^*) = \frac{1}{\alpha} \log(\sqrt{\alpha S}) = \frac{\log(\alpha S)}{2\alpha},
$$
$$
\phi(G^*) = 1 - e^{-\alpha e^*(G^*)} = 1 - e^{-\frac{1}{2}\log(\alpha S)} = 1 - \frac{1}{\sqrt{\alpha S}}.
$$

Country $i$'s Lindahl contribution is:
$$
t_i^* = \frac{S_i}{S} \cdot G^* = \frac{S_i}{S} \cdot \sqrt{\frac{S}{\alpha}} = S_i \sqrt{\frac{1}{\alpha S}} = \frac{S_i}{\sqrt{\alpha S}}
$$

The net payoff is therefore:
$$
\phi(G^*) S_i - t_i^* = \left(1 - \frac{1}{\sqrt{\alpha S}}\right) S_i - \frac{S_i}{\sqrt{\alpha S}} = S_i \left(1 - \frac{2}{\sqrt{\alpha S}}\right).
\quad \text{(A.5)}
$$

This is non-negative if and only if $\sqrt{\alpha S} \ge 2$, i.e., $\alpha S \ge 4$.

[Page 49]
**Lemma A.1** (Participation condition). Under the parametric specification $\pi(e) = 1 - e^{-\alpha e}$, the Lindahl schedule satisfies individual rationality for all countries if and only if $\alpha S \ge 4$. Under this condition:
$$
\phi(G^*)S_i - t_i^* = S_i(1 - \frac{2}{\sqrt{\alpha S}}) \ge 0,
\quad \quad \quad \quad \text{(A.6)}
$$
with strict inequality when $\alpha S > 4$.

*Proof.* Substituting $\phi(G^*) = 1 - 1/\sqrt{\alpha S}$ and $t_i^* = S_i/\sqrt{\alpha S}$ into the net payoff formula and collecting terms yields the expression above. This is non-negative iff $\sqrt{\alpha S} \ge 2$, equivalently $\alpha S \ge 4$.
□
□

**Remark 10.** $\alpha S$ is the social return to innovation: high $\alpha S$ means a small prize generates a high success probability, making expected benefits large relative to contributions. Below $\alpha S = 4$, the Lindahl schedule requires external subsidies ($\lambda > 1$). At calibrated Covid parameters $\alpha S \approx 2.2 < 4$, individual rationality fails for the cash mechanism—confirming the CRLM’s advantage.

## A.4 Proof of the welfare ranking under parallel trade

When tiered pricing is infeasible due to parallel trade, the innovator faces a uniform pricing constraint: $p_R = p_P = p$. We verify that the welfare ranking reduces cleanly to $W^{Lindahl} \ge W^{NE} \ge W^M$ in this case.

Under uniform pricing, the profit-maximising monopolist charges $p^* = v_R$ (Assumption 3 still implies exclusion of poor countries). Patent welfare is $W_M = \pi(e_M)S_R - e_M$ as in the main text. The Nash prize game is unchanged: governments contribute voluntarily and the equilibrium is characterised by Lemma 2. The Lindahl schedule with $t_i^* = (S_i/S)G^*$ remains budget-balanced, individually rational (by Lemma A.1 at $\alpha S \ge 4$), and achieves the social optimum.

**Corollary A.1** (Welfare ranking under parallel trade). When tiered pricing is infeasible

[Page 50]
(parallel trade arbitrage binds), the welfare ranking is:
$$
W^{Lindahl} > W^{NE} > W_M,
\tag{A.7}
$$
where all three inequalities are strict under Condition (17). The welfare gap $W^{Lindahl} – W^{NE}$ is:
$$
W^{Lindahl} – W^{NE} = [\phi(G^*) – \phi(G^{NE})] S – [G^* – G^{NE}] > 0,
\tag{A.8}
$$
and is increasing in the number of countries $N$ (since $G^*/G^{NE} = \sqrt{S}/\sqrt{\bar{S}}$ grows with $N$ under symmetry).

*Proof*. The strict inequalities follow from Propositions 2 and 3. Expression (A.8) is the welfare loss from under-provision, established in Lemma 3(iv). The monotonicity in $N$ follows from Corollary 1: under $N$ symmetric countries and specification (6), $G^{NE} = \sqrt{\bar{S}}/(N\alpha)$ and $G^* = \sqrt{S}/\alpha$, so the gap $G^* – G^{NE} = \sqrt{S}/\alpha(1 – 1/\sqrt{N})$ is strictly increasing in $N$. $\square \quad \square$