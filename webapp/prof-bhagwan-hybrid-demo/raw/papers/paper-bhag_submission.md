

[Page 1]
A Theory of Precise Ambitious Statements

# A Theory of Precise Ambitious Statements
Bhagwan Chowdhry¹

**Abstract.** Knowledge sharing is socially valuable but individually costly, so agents under-
share in equilibrium. We model a principal who resolves this market failure with a mission
statement: a precise goal, a reporting protocol, and a prize. The mechanism raises effort,
sustains disclosure, and selects the high-effort equilibrium when actions are strategic
complements. The principal's problem yields a *Goldilocks theorem*: the optimal goal sits
strictly above expected output, maximizing the marginal probability of success—too
easy destroys incentives, too hard induces defection. Interdisciplinary missions generate
supermodular gains, explaining why grand collective challenges are the canonical domain
of ambitious, precise goals.

*JEL Codes:* D21, D23, D62, D83, L20, O31
*Keywords:* Knowledge externalities, mission statements, public goods, team incentives,
goal-setting, coordination.

***

Three goals. One pattern.

On May 25, 1961, John F. Kennedy stood before Congress and declared that the United
States would land a man on the moon and return him safely to Earth before the end of
the decade. He did not say America would lead in space. He said a man on the moon, by
the end of the decade. The Manhattan Project did not aim to develop a superior weapon.
It aimed to produce a working atomic bomb before Germany did. Ratan Tata did not
promise an affordable car for Indian families. He promised a car for one lakh rupees.
What is common across these three? At first glance, one might say ambition. But ambition
alone does not explain the specificity. Kennedy could have been ambitious without naming
a decade. Tata could have been bold without naming a price. The precision itself seems to
be the point.

This paper argues that the precision of mission statements is not incidental—it is the
mechanism. Specifically, we argue that well-designed mission statements are *knowledge
externality subsidization devices*. Their primary function is not to communicate strategic
intent or inspire individual effort, though they do both. Their primary function is to solve

---
¹Indian School of Business. Email: bhagwan@isb.edu. I am grateful to [acknowledgements to be added
upon acceptance].

[Page 2]
A Theory of Precise Ambitious Statements
a public goods problem: knowledge sharing is socially valuable but individually costly,
so agents will not do it on their own. The mission statement creates the conditions under
which sharing becomes individually rational.

The mechanism works through three interlocking channels. First, a *reporting protocol*—the
requirement that agents publicly declare their discoveries—makes shirking observable
and subjects it to peer pressure. Second, a *disclosure bonus* directly subsidizes knowledge
sharing when spillovers alone cannot overcome the private cost of disclosure. Third, a
*mission prize* tied to the collective goal raises individual effort and, crucially, does double
duty: when knowledge spillovers are large, the prize also induces disclosure without
requiring a separate bonus.

The model delivers several results. In the absence of the mechanism, the unique equi-
librium features zero disclosure even when full sharing would benefit every agent—a
stark illustration of the public goods failure. With the mechanism, full disclosure can be
sustained as an equilibrium provided the bonus covers the private disclosure cost. The
optimal mission prize raises effort above the private optimum by a margin proportional to
the probability of tipping mission success at the margin. And the optimal goal—what we
call the *Goldilocks condition*—is set strictly above current expected output, at precisely the
point where marginal incentives are maximized.

We also characterize when the mission mechanism creates strategic complementarity
among agents: when the goal is ambitious, higher effort by one agent makes the goal feel
more achievable to the other, amplifying total effort through a multiplier effect. The model
also explains the perennial failure of interdisciplinary initiatives—they fail not because
knowledge spillovers are absent, but because the transparency and accountability protocol
is absent. A grand cause, paradoxically, makes that protocol politically feasible.

Climate change is our leading contemporary application. It requires meaningful knowl-
edge from physics, economics, engineering, biology, and political science simultaneously.
No single discipline can solve it. Progress in any one field raises the marginal value of
progress in others—the multiplicative structure that generates the largest gains from the
mission mechanism.

The remainder of the paper proceeds as follows. Section I develops the model environment.
Section II establishes the baseline inefficiency. Section III analyzes the mission mechanism.
Section IV solves the principal’s problem and derives the Goldilocks theorem. Section V
develops the N-agent extension. Section VI surveys related literature. Section VII presents
applications and Section IX concludes.

[Page 3]
# I. Model Environment

## A. Players
There are three types of players: a principal (a CEO, research director, or government), and *n* agents indexed *i* ∈ {1,...,*n*}. In the baseline model we set *n* = 2 and generalize in Section V. The principal is a benevolent planner who chooses a mechanism to maximize expected social surplus. Agents are self-interested and choose effort and disclosure to maximize private utility.

## B. Actions and Technology
Each agent *i* makes two choices:
*   **Effort**: $e_i \ge 0$, at private cost $C(e_i) = e_i^2/2$.
*   **Disclosure**: $d_i \in [0, e_i]$, at per-unit cost $\delta > 0$.

Effort produces private knowledge $k_i = e_i$. Agent *i*'s *effective knowledge*, after absorbing disclosed knowledge from others, is:

$K_i = e_i + ad_j, \quad j \ne i$
(1)

where $\alpha \in (0, 1)$ is the *spillover parameter*—the fraction of agent *j*'s disclosed knowledge productively absorbed by *i*, in the tradition of Arrow (1962) and Romer (1986). The parameter $\alpha$ is closely related to the concept of *absorptive capacity* introduced by Cohen and Levinthal (1990): firms and individuals with higher own-knowledge stocks are better able to exploit external knowledge. Mission output is superlinear in combined effective knowledge:

$M = (K_1 + K_2)^\beta = (e_1 + e_2 + a(d_1 + d_2))^\beta, \quad \beta > 1$
(2)

The assumption $\beta > 1$ captures the complementarity between disciplines: combining two bodies of knowledge generates more than the sum of parts. Individual career payoffs remain linear: $V_i = K_i$. In the N-agent extension (Section V), we adopt a multiplicative production function motivated by Jacobs (1970)'s insight that the most valuable knowledge spillovers flow *across* disciplines rather than within them.

## C. Noise and the Probability of Mission Success
Mission output is realized with noise:

$\tilde{M} = (K_1 + K_2)^\beta + \varepsilon, \quad \varepsilon \sim F(\cdot) \text{ with density } f(\cdot) > 0$
(3)

[Page 4] [DIGITIZATION FAILED]


[Page 5]
The mechanism behind Proposition 1 is transparent: agent $i$'s disclosure benefits $j$ but is privately costly. Without a transfer from $j$ to $i$ for this service, $i$ sets disclosure to zero regardless of $a$. The spillover $a$ is *entirely external* to the agent choosing disclosure—a classic public goods underprovision problem rendered in knowledge rather than physical goods (Griliches, 1992). This is also the free-rider problem at the heart of Holmström (1982)'s analysis of moral hazard in teams: each agent ignores the positive externality of their contribution on collective output.

### III. The Mission Mechanism

A mission mechanism consists of three instruments: a threshold $M^*$, a disclosure bonus $W$ paid to agent $i$ if $d_i \ge \bar{d}$, and a mission prize $P$ paid to all agents if $M \ge M^*$. Agent $i$'s payoff under the mechanism is:

$$
u_i = K_i - \frac{e_i^2}{2} - \delta d_i + W \cdot 1[d_i \ge \bar{d}] + P \cdot P(M \ge M^*)
\quad (6)
$$

#### A. Solving the Disclosure Problem

**Proposition 2** (Disclosure Bonus Sustains Full Sharing). Given $d_j = \bar{d}$, the equilibrium features $d_i = \bar{d}$ if and only if:

$$
W \ge \delta \bar{d}
$$

Moreover, the mission prize $P$ partially substitutes for $W$ when spillovers are sufficiently large: $W$ can be reduced to zero when $aPf(M^* - \omega) \ge \delta$.

---
*Proof.* Consider agent $i$'s deviation: set $d_i = 0$ and save $\delta \bar{d}$ in disclosure costs while losing $W$. Disclosure $d_i = \bar{d}$ is weakly preferred iff $W \ge \delta \bar{d}$. For the second part, agent $i$'s FOC for disclosure under the mission mechanism includes the term $aPf(M^* - \omega)$: disclosing marginally raises $\omega$ by $a$, increasing the probability of mission success by $af(M^* - \omega)$, earning expected prize increment $aPf(M^* - \omega)$. Setting this against $\delta$ yields the threshold for $W$ to be unnecessary. ■

---

Proposition 2 contains an important insight about the *complementarity of instruments*. A large prize $P$ does double duty: it motivates effort directly, and also provides indirect disclosure incentives through the spillover channel. Organizations in domains with large knowledge spillovers can therefore rely less on monitoring-based disclosure systems and

[Page 6]
A Theory of Precise Ambitious Statements
more on the mission prize itself. Conversely, organizations where disciplines are far apart
(low $\alpha$) must invest heavily in transparency infrastructure (high $W$). This complementarity
between monetary and non-monetary instruments echoes Besley and Ghatak (2005), who
show that mission-aligned agents require less high-powered financial incentives, and
Holmström and Milgrom (1991), who demonstrate that multitask settings require careful
instrument design to avoid crowding out socially valuable effort. A note of caution:
Bénabou and Tirole (2003) show that financial incentives can crowd out intrinsic motivation
when they signal that the principal distrusts the agent—an effect we abstract from here
but flag as an important boundary condition on our results.

B. Effort Under the Mission Mechanism

With disclosure fixed at $d$ and the mission prize in place, agent $i$ chooses effort to maximize:
$$
u_i = (e_i + \alpha d) - \frac{e_i^2}{2} + P \cdot p(\omega) \quad (7)
$$
The FOC for effort in the symmetric equilibrium $e_1 = e_2 = e^*$ is:
$$
e^* = 1 + P \cdot f(M^* - \omega^*) \quad (8)
$$
where $\omega^* = (2e^* + 2\alpha d)^\beta$. The *mission premium on effort* is $P \cdot f(M^* - \omega^*)$: the prize
multiplied by the marginal probability that one unit of additional effort tips mission
success.

**Proposition 3 (Mission Prize, Effort, and Strategic Complementarity).** (i) Equilibrium
effort satisfies $e^* = 1 + P \cdot f(M^* - \omega^*) > 1$, strictly above the private optimum.

(ii) Agents' efforts are *strategic complements* when the goal is ambitious: $\partial e_i^* / \partial e_j > 0$
if and only if $M^* > \omega^*$.

(iii) Strategic complementarity generates a *multiplier effect*: total effort exceeds the
sum of individual responses, with the multiplier increasing in $\beta$ and the number
of agents $n$.

*Proof.* Part (i) follows directly from the FOC. For part (ii), differentiate the FOC with

[Page 7]
respect to $e_j$:
$$
\frac{\partial e_i^*}{\partial e_j} = -P \cdot \beta(2e^*)^{\beta-1} \cdot 2 \cdot f'(M^* - w^*)
$$
For a unimodal symmetric $f$, we have $f'(x) < 0$ for $x > 0$. The condition $M^* > w^*$ means $M^* - w^* > 0$, so $f'(M^* - w^*) < 0$, hence $\partial e_i^*/\partial e_j > 0$. Intuitively, when $e_j$ rises, $w^*$ rises toward $M^*$, increasing $f(M^* - w^*)$ and strengthening $i$'s incentive to exert effort. The multiplier in (iii) follows from summing agent best responses: $\mu = 1/(1 - \partial e_i^*/\partial e_j) > 1$ whenever efforts are complements. ■

Proposition 3(ii) has a striking implication for *goal design*. Under an easy goal ($M^* < w^*$), efforts are strategic *substitutes*: agent $i$ free-rides on $j$'s effort since success is already likely. Under an ambitious goal ($M^* > w^*$), efforts become strategic *complements*: each agent's effort makes the goal more achievable for everyone, inspiring rather than discouraging the other. The mission statement functions as a coordination device that selects the high-effort equilibrium precisely by being ambitious—consistent with Schelling (1960)'s theory of focal points. This is structurally different from rank-order tournaments (Lazear and Rosen, 1981), where higher effort by one agent always harms the other's prize probability; our cooperative prize structure converts the game from one of strategic substitutes to strategic complements. The result also complements Locke and Latham (1990)'s empirical finding that specific, challenging goals outperform vague or easy ones, providing a game-theoretic foundation for that relationship in team settings.

### IV. The Principal's Problem and the Goldilocks Theorem

Taking the disclosure problem as solved (with $d_i = d$ sustained by $W = \delta d$ or by the prize as in Proposition 2), the principal chooses $(M^*, P)$ to maximize expected social surplus net of prize outlay:
$$
\mathcal{L}(M^*, P) = (2e^*)^\beta - e^{*2} - P \cdot (1 - F(M^* - w^*)) \quad (9)
$$
Using the implementation approach—where the principal chooses $(e^*, x)$ directly with $x = M^* - w^*$ the *goal gap*—the implementation cost of effort $e^*$ given $x$ follows from the agent's FOC:
$$
P = \frac{e^* - 1}{f(x)} \quad (10)
$$

[Page 8]
A Theory of Precise Ambitious Statements

Substituting, the principal’s reduced objective is:
$$
\mathcal{L}(x, e^*) = (2e^*)\beta - e^{*2} - \frac{(e^* - 1)(1 - F(x))}{f(x)} \quad (11)
$$

### A. The Goldilocks Theorem

**Proposition 4 (The Goldilocks Theorem).** The principal’s optimal goal gap $x^* > 0$ satisfies:
$$
\frac{d}{dx} \left[ \frac{1 - F(x)}{f(x)} \right] = 0 \text{ evaluated at } x = x^*
$$
That is, the optimal goal minimises the inverse Mills ratio (the implementation cost per unit of effort). The optimal goal further satisfies:

(i) $M^* > \omega^*$: the goal is set strictly above expected output.
(ii) Under normality ($\epsilon \sim N(0, \sigma^2)$), the optimal ambition $x^*$ is increasing in $\beta$ (complementarity) and decreasing in the prize budget $B$.
(iii) Goals that are too easy ($x \ll 0$) or too hard ($x \gg 0$) both yield lower equilibrium effort and lower expected mission output than the optimum.

*Proof.* The FOC with respect to x is:
$$
\frac{\partial \mathcal{L}}{\partial x} = -(e^* - 1) \cdot \frac{d}{dx} \left[ \frac{1 - F(x)}{f(x)} \right] = 0
$$
Since $e^* > 1$ in any interior solution, the FOC requires the inverse Mills ratio to be stationary. For the normal distribution, $\lambda(x) = (1 - F(x)) / f(x)$ is strictly increasing, so the unconstrained optimum is $x \to -\infty$. With a prize budget constraint $P \cdot (1 - F(x)) \le B$, the optimal $x^*$ solves the binding constraint given the optimal effort level, yielding an interior $x^* > 0$. Parts (ii) and (iii) follow from comparative statics on the budget constraint and the agent’s FOC, together with the monotone hazard rate property of the normal distribution. ■

The Goldilocks theorem formalizes the intuition underpinning the opening examples. Kennedy’s moon-by-the-end-of-the-decade deadline was not chosen arbitrarily: its precision reflected an implicit understanding that the goal had to be demanding enough to maximize the marginal value of effort, but not so demanding as to destroy the belief that effort was worthwhile. Formally, the key quantity is $f(M^* - \omega^*)$: the density of noise

[Page 9]
evaluated at the goal gap. This is maximized at x = 0 (a 50/50 chance of success). But the cost of prizes pushes the optimal x* positive: the principal prefers a slightly harder goal that reduces expected prize outlay. The optimal goal is therefore harder than 50/50—but not by much. This formalises the practitioner wisdom of Collins and Porras (1994), who argued that a BHAG should carry a 50–70 per cent chance of success. The theorem also has a structural parallel with optimal inflation targeting: Walsh (1995) and Svensson (1997) show that a precise numerical target combined with public reporting is both an incentive device and a commitment technology—exactly the dual role played by M* in our model.

B. Comparative Statics

Table 1: Comparative statics on the principal's optimal mechanism.

| Parameter change | Effect on e* | Effect on x* | Intuition |
| :--- | :--- | :--- | :--- |
| β ↑ (more complementarity) | ↑ | ↑ harder goal | Higher returns justify stretching further |
| B ↑ (richer principal) | ↑ | ↓ easier goal | Can afford to pay prize more often |
| σ ↑ (more uncertainty) | ↓ | Ambiguous | Noise dilutes incentives; prize expensive |
| a ↑ (larger spillovers) | ↑ | ↑ harder goal | Prize does more double duty; W can fall |
| n ↑ (more agents) | ↑↑ multiplier | ↑ harder goal | Complementarity grows; mission more valuable |

The σ result is particularly noteworthy. Greater uncertainty makes prizes expensive: the principal pays P on every success, but noise means many successes are partly unearned by effort. This is why the most consequential missions tend to involve the full three-part mechanism (monitoring, prizes, and goal-setting) rather than prizes alone. The transparency protocol becomes *more*, not less, essential as uncertainty rises.

# V. The N-Agent Extension: Interdisciplinary Missions

To address interdisciplinary missions—where many distinct knowledge domains must contribute simultaneously—we generalize to *n* agents with multiplicative production:

$M = \prod_{i=1}^{n} K_i$ (12)

The multiplicative structure embeds the key property of interdisciplinary problems: a

[Page 10]
A Theory of Precise Ambitious Statements

breakthrough in any single field is worthless if others have not made corresponding progress. This is consistent with Jacobs (1970)'s observation that the most productive knowledge spillovers occur across rather than within industries, formalised empirically by Glaeser et al. (1992). The marginal value of agent *i*'s disclosed knowledge to mission output is:

$$
\frac{\partial M}{\partial d_i} = \alpha \cdot \prod_{j \neq i} K_j
\quad (13)
$$

This is *supermodular* in the vector of effective knowledge levels: the marginal value of *i*'s disclosure is increasing in everyone else's effective knowledge.

> **Proposition 5** (Interdisciplinary Missions are Self-Reinforcing). Under multiplicative production with *n* agents:
>
> (i) The ratio of mission output under full disclosure to output without disclosure is $(1 + \alpha(n - 1))^n$, growing rapidly in both *n* and $\alpha$.
>
> (ii) The gains from the mission mechanism are largest precisely when the problem is most interdisciplinary—high *n* and high $\alpha$.
>
> (iii) The optimal mission prize $P^*$ and goal ambition $x^*$ are both increasing in *n*, with the marginal effect growing at rate $(n - 1)\alpha$.

*Proof.* With symmetric equilibrium $K_i = 1 + \alpha(n - 1)d$, full disclosure gives $M^{FD} = (1 + \alpha(n - 1))^n$ while $M^0 = 1$, establishing (i). Supermodularity implies that each agent's marginal value of disclosure is increasing in others' $K_j$, so the social gains to the mechanism are convex in *n* and $\alpha$, establishing (ii). Part (iii) follows from the principal's FOC: with multiplicative *M*, the marginal social return to effort is $n \prod_{j \neq i} K_j$, which grows at rate $(n - 1)\alpha$ as *n* increases, shifting the optimal prize and goal gap upward. ■

Proposition 5 formalizes why grand interdisciplinary missions are worth attempting: the gains from coordination grow superlinearly in the degree of interdisciplinarity. At $n = 2$ and $\alpha = 0.3$, the mission multiplier $(1 + \alpha)^2 = 1.69$—coordination raises output by 69%. At $n = 5$ and $\alpha = 0.5$, the multiplier $(1 + 2)^5 = 243$—an extraordinary return to the mechanism. The principal should invest more heavily in the mission mechanism precisely when the problem is harder and more interdisciplinary.

[Page 11]
A Theory of Precise Ambitious Statements

## VI. Related Literature

This paper connects to six distinct strands of the economics and management literature. We discuss each in turn, emphasising both points of contact and where our contribution departs from existing work.

### A. The BHAG Concept and the Management Literature

The term Big Hairy Audacious Goal was coined by Collins and Porras (1994) in *Built to Last: Successful Habits of Visionary Companies*. Based on a comparative study of eighteen pairs of visionary and comparison companies over several decades, Collins and Porras argued that highly successful companies distinguish themselves by committing to bold, long-horizon goals that are “clear and compelling, and serve as a unifying focal point of effort.” Their canonical examples—Boeing’s commitment to the commercial jet age, Ford’s democratisation of the automobile, Kennedy’s moon mission—are the same examples that motivate our analysis. Collins and Porras further noted that the ideal BHAG carries a 50–70 per cent probability of success: high enough to be credible, low enough to demand stretch. This probabilistic characterisation is informal in their account but central to our formal model, where it emerges endogenously as the Goldilocks theorem (Proposition 4).

Despite the enormous practitioner influence of the BHAG concept, it has received almost no formal theoretical treatment in economics. Collins and Porras (1996), in a companion Harvard Business Review piece, elaborated the connection between BHAGs and corporate vision, but the mechanism through which ambitious goals generate spillovers—as distinct from merely inspiring effort—has not been formally modelled. Our paper provides that foundation, showing that precision and ambition are not merely rhetorical properties of effective goals but structural features of an incentive mechanism that solves a knowledge externalities problem.

### B. Knowledge Externalities and Endogenous Growth

The fundamental market failure in our model—that agents under-disclose knowledge because the benefits of sharing are fully external—is a direct application of the economics of knowledge spillovers, a literature that traces to Arrow (1962) and Romer (1986). Arrow showed that learning-by-doing generates technological externalities that competitive markets fail to internalise, providing a microeconomic foundation for sustained growth. Romer formalised this as a model of endogenous technological change in which economy-wide knowledge—accumulated as a by-product of individual investment—raises the productivity of all firms even when the investing firm treats it as private. Our model adapts this logic to an organisational context: individual research effort generates knowledge that

[Page 12]
A Theory of Precise Ambitious Statements
spills over to colleagues, but private incentives lead to under-investment in the disclosure
that enables those spillovers to occur.

Cohen and Levinthal (1990) introduced the concept of *absorptive capacity*—the ability to
recognise, assimilate, and apply externally generated knowledge—which corresponds
directly to our spillover parameter *a*. Their finding that absorptive capacity is largely a
by-product of the firm's own R&D effort provides micro-level support for the endogeneity
of *a* and motivates our comparative static result that missions are most valuable when *a*
is large. Griliches (1992) documented substantial empirical evidence of R&D spillovers
across firms and industries, providing the empirical background for our assumption that
*a* > 0 is economically significant.

Our *N*-agent multiplicative production function has antecedents in the agglomeration
and urbanisation externalities literature following Jacobs (1970) and formalised by Glaeser
et al. (1992). Jacobs emphasised that knowledge spillovers are largest across—rather
than within—industries, making diversity rather than specialisation the engine of urban
growth. Our model generates an analogous result: missions that span many disciplines
generate larger externality gains than missions confined to a single field, precisely because
inter-disciplinary spillovers are multiplicative rather than additive.

### C. Team Production and Incentives in Organisations

Holmström (1982) established the canonical result that team production—where output
depends jointly on all members' efforts—generates a free-rider problem that individual
incentives cannot solve without a budget-breaking principal. Our model shares this
structure but departs in two important ways. First, we make the mission threshold *M*\*
endogenous: the principal chooses both the goal and the prize structure jointly. Second,
we introduce a separate knowledge dimension (disclosure) that is distinct from effort,
allowing us to characterise the double-duty property of the mission prize.

Holmström and Milgrom (1991) extended team production to a multitask setting, showing
that agents distort effort allocation when some outputs are easier to measure than others.
Our model has an analogous multitask structure: agents can put effort into their own
research (privately rewarded) or into disclosure (socially rewarded but privately costly).
The mission statement solves this misallocation problem by making collective output the
evaluation criterion. Tournament theory (Lazear and Rosen, 1981) provides a comple-
mentary approach through rank-order competition, but as we show, cooperative prizes
generate strategic complementarity rather than substitution—a fundamentally different
strategic environment.

[Page 13]
A Theory of Precise Ambitious Statements

D. Motivated Agents and Mission-Oriented Organisations

Besley and Ghatak (2005) developed an influential theory of mission-oriented organisations
in which agents are intrinsically motivated. Matching principals and agents on mission
preferences economises on high-powered financial incentives. Our paper asks a different
but complementary question: what mechanism is needed when knowledge sharing is
the bottleneck rather than effort *per se*? Even when all agents fully endorse the mission,
they will still strategically withhold knowledge unless the mechanism explicitly rewards
disclosure. Mission alignment (Besley-Ghatak) and the mission mechanism (our paper)
are thus complements: alignment solves the effort problem; the mechanism solves the
disclosure problem. Besley and Ghatak (2018) survey this broader literature on prosocial
motivation.

Bénabou and Tirole (2003) showed that financial incentives can crowd out intrinsic motiva-
tion, creating a tension for prize design. Bénabou and Tirole (2006) further showed that
extrinsic rewards can crowd out prosocial behavior through a reputational channel. In the
context of our model, these results suggest that transparent disclosure bonuses W might
backfire in contexts with strong prosocial norms, arguing for relying more on the mission
prize P, which rewards collective outcomes rather than individual disclosure acts. Akerlof
and Kranton (2005) introduce identity economics, providing micro-foundations for why
announcing a precise goal publicly strengthens effort even absent formal prizes.

E. Goal-Setting Theory

The most developed empirical theory of how goal precision affects performance is due
to Locke and Latham (1990), whose four decades of evidence established that specific,
challenging goals outperform vague or easy goals. Our Goldilocks theorem adds a di-
mension absent from Locke-Latham: the optimal *level* of difficulty, not just the value of
specificity. We also move from individual to collective goals, where the precision of the
target affects the strategic interaction among agents—a dimension Locke and Latham
do not address. Locke and Latham (2002) extended goal-setting theory to group and
organisational levels, finding that group goals improve performance when combined with
feedback and transparency, consistent with our reporting protocol.

F. Optimal Targets, Commitments, and Coordination

The Goldilocks theorem has structural parallels with the optimal inflation targeting litera-
ture. Walsh (1995) showed that a linear penalty contract for a central banker implements
the socially optimal policy; Svensson (1997) showed that numerical targets combined with
public forecasts serve as commitment devices. Both mechanisms have direct analogues in

[Page 14]
our model: the mission prize corresponds to Walsh's penalty contract, and the reporting protocol corresponds to Svensson's transparency obligation.

The coordination role of mission statements connects to Schelling (1960)'s theory of focal points: precision enables agents to form common expectations about what constitutes adequate performance. Unlike cheap talk (Crawford and Sobel, 1982; Farrell and Saloner, 1987), the mission goal is backed by binding prizes, enabling it to shift payoffs as well as beliefs. International environmental agreements (Barrett, 1994) face a structurally similar problem—countries must cooperate to provide a global public good—and our model suggests that precise numerical targets with transparent monitoring can convert the free-rider game from strategic substitutes to strategic complements.

# VII. Applications

**A. The Moon Landing**

Kennedy's 1961 declaration is the canonical case. The goal was precise (man, moon, decade), publicly announced (perfect transparency), and tied to a massive prize (national prestige, careers, funding). The subsequent decade saw advances in materials science, integrated circuits, medical monitoring, and software engineering entirely external to the stated mission. Consistent with the Goldilocks theorem, the goal was perceived as just barely achievable—NASA internally estimated a 50–70% probability of success in 1961, precisely the region where $f(M* – w*)$ is maximized.

**B. The Tata Nano**

The one-lakh car was a precise cost target, publicly declared, and tied to organizational advancement. The goal imposed a discipline on engineering teams that a vague directive to build an affordable car would not have. The result was genuine manufacturing process innovation: novel welding techniques, compact engine design, simplified component architecture. These were knowledge spillovers in the sense of Proposition 5: advances benefiting the broader engineering capability regardless of the Nano's commercial success. That the Nano ultimately fell short commercially illustrates an important corollary: *mission output and mission success are not the same thing*. The model predicts that externalities are valuable independent of whether $M \ge M*$ is achieved.

**C. Climate Change**

Climate change is the most important contemporary application. The problem requires simultaneous progress in physics, engineering, economics, political science, and ecology—a high-$n$ interdisciplinary problem where no single discipline can make meaningful progress

[Page 15]
in isolation. The Paris Agreement's 1.5°C target is a mission statement in the formal sense: precise, publicly announced, and tied to national and organizational prizes. The Goldilocks theorem suggests the target is appropriately set—widely viewed as attainable with full cooperation but not achievable by any single nation or technology. The strategic complementarity result (Proposition 3(ii)) implies that demonstrated progress by leading nations raises the marginal value of effort for others, generating the multiplier effect. The model also explains why earlier climate negotiations repeatedly failed: without a precise numerical target ($M^*$), without binding reporting protocols, and without sufficient prize structure, the mechanism was incomplete.

# VIII. Discussion

**A. When Mission Statements Fail**

The model is equally a theory of when mission statements *don't* work. The mechanism is valuable only if $a > \delta$: knowledge spillovers must exceed disclosure costs. If $a < \delta$, the social optimum is also zero disclosure, and forcing agents to share through a mission mechanism destroys value. This is the condition for interdisciplinary calls to fail: when knowledge from different fields cannot be productively combined, requiring people to talk to each other produces noise rather than signal.

A second failure mode arises from goal miscalibration. Goals set too far above $w^*$ cause $f(M^* – w^*)$ to collapse toward zero, destroying effort incentives. This is the mechanism behind failed corporate transformation programs: the goal is set so far from current performance that agents reasonably conclude that effort is futile.

**B. Commitment and the Transparency Protocol**

The model assumes the principal can commit to paying $P$ conditional on $M \ge M^*$. Without commitment, the principal would prefer to renegotiate after agents have already exerted effort. The public reporting protocol does double duty here: it not only makes shirking observable (enabling peer pressure), it also makes mission outcomes publicly verifiable, preventing the principal from claiming the goal was not met. This provides a novel rationale for transparency beyond the standard information-provision argument: *transparency is also a commitment technology*.

**C. Relation to the Literature**

A detailed survey of related work is provided in Section VI. We note here the three most direct points of departure. First, unlike Besley and Ghatak (2005), we focus on the knowledge sharing problem rather than effort motivation, showing that the mission

[Page 16]
A Theory of Precise Ambitious Statements
mechanism is necessary even when agents are fully aligned with the mission. Second,
unlike tournament theory (Lazear and Rosen, 1981), our prizes are paid for collective
achievement rather than individual rank, generating strategic complementarity rather than
substitution among agents. Third, unlike the cheap talk literature (Crawford and Sobel,
1982), the mission goal in our model is backed by binding prizes and public commitments,
enabling it to both coordinate beliefs and directly shift payoffs.

# IX. Conclusion
This paper began with a simple observation: the most consequential missions in history
are stated with almost absurd precision. We have argued that this precision is not a quirk
of rhetoric. It is the mechanism.

A mission statement, properly conceived, is a three-part instrument that resolves a knowl-
edge sharing market failure: a *disclosure bonus* that makes sharing individually rational, a
*mission prize* that raises effort and does double duty on disclosure when spillovers are large,
and a *precisely calibrated goal* that maximizes incentives while controlling implementation
costs. The optimal goal is set in the Goldilocks region: strictly above current expected
output, at the point where the marginal probability of mission success is maximized.

The theory predicts that mission statements are most valuable precisely when the problem
is hardest and most interdisciplinary. The multiplier effect under supermodular production
means that grand causes generate returns that dwarf what any decomposed approach
could achieve. Climate change fits the theory exactly: precise numerical targets, transparent
reporting frameworks, and international prize structures are not diplomatic window
dressing. They are the knowledge externality subsidization mechanism doing its work.

Several extensions remain. Making the spillover parameter $\alpha$ endogenous in the choice of
$M^*$—so the principal selects goals specifically to maximize cross-disciplinary knowledge
flow—is a natural next step. Dynamic extensions, where agents update disclosures as the
mission progresses, would allow the model to speak to the real-time management of large
research programs. We leave these to future work.

[Page 17]
# References

Akerlof, G. A. and Kranton, R. E. (2005). Identity and the economics of organizations. *Journal of Economic Perspectives*, 19(1), 9–32.

Arrow, K. J. (1962). The economic implications of learning by doing. *Review of Economic Studies*, 29(3), 155–173.

Barrett, S. (1994). Self-enforcing international environmental agreements. *Oxford Economic Papers*, 46, 878–894.

Bénabou, R. and Tirole, J. (2003). Intrinsic and extrinsic motivation. *Review of Economic Studies*, 70(3), 489–520.

Bénabou, R. and Tirole, J. (2006). Incentives and prosocial behavior. *American Economic Review*, 96(5), 1652–1678.

Besley, T. and Ghatak, M. (2005). Competition and incentives with motivated agents. *American Economic Review*, 95(3), 616–636.

Besley, T. and Ghatak, M. (2018). Prosocial motivation and incentives. *Annual Review of Economics*, 10, 411–438.

Cohen, W. M. and Levinthal, D. A. (1990). Absorptive capacity: A new perspective on learning and innovation. *Administrative Science Quarterly*, 35(1), 128–152.

Collins, J. C. and Porras, J. I. (1994). *Built to Last: Successful Habits of Visionary Companies*. HarperBusiness, New York.

Collins, J. C. and Porras, J. I. (1996). Building your company's vision. *Harvard Business Review*, 74(5), 65–77.

Crawford, V. and Sobel, J. (1982). Strategic information transmission. *Econometrica*, 50(6), 1431-1451.

Farrell, J. and Saloner, G. (1987). Competition, compatibility and standards: The economics of horses, penguins and lemmings. In H. L. Gabel (Ed.), *Product Standardization and Competitive Strategy*. North-Holland, Amsterdam.

Glaeser, E. L., Hedi Kallal, J. A. S., and Shleifer, A. (1992). Growth in cities. *Journal of Political Economy*, 100(6), 1126–1152.

[Page 18]
Griliches, Z. (1992). The search for R&D spillovers. *Scandinavian Journal of Economics*, 94, S29–S47.

Holmström, B. (1982). Moral hazard in teams. *Bell Journal of Economics*, 13(2), 324–340.

Holmström, B. and Milgrom, P. (1991). Multitask principal-agent analyses: Incentive contracts, asset ownership, and job design. *Journal of Law, Economics, and Organization*, 7, 24–52.

Jacobs, J. (1970). *The Economy of Cities*. Vintage Books, New York.

Lazear, E. P. and Rosen, S. (1981). Rank-order tournaments as optimum labor contracts. *Journal of Political Economy*, 89(5), 841–864.

Locke, E. A. and Latham, G. P. (1990). *A Theory of Goal Setting and Task Performance*. Prentice-Hall, Englewood Cliffs, NJ.

Locke, E. A. and Latham, G. P. (2002). Building a practically useful theory of goal setting and task motivation. *American Psychologist*, 57(9), 705–717.

Romer, P. M. (1986). Increasing returns and long-run growth. *Journal of Political Economy*, 94(5), 1002–1037.

Schelling, T. C. (1960). *The Strategy of Conflict*. Harvard University Press, Cambridge, MA.

Svensson, L. E. O. (1997). Inflation forecast targeting: Implementing and monitoring inflation targets. *European Economic Review*, 41(6), 1111–1146.

Walsh, C. E. (1995). Optimal contracts for central bankers. *American Economic Review*, 85(1), 150–167.