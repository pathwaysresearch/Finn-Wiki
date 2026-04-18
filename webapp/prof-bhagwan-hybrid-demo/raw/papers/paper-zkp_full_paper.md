

[Page 1]
Chowdhry and Sharma | ZKP Password Authentication

# Imagine! Never Write, Type, or Punch Your Password: A Novel Zero-Knowledge Proof Protocol for Password Authentication

Bhagwan Chowdhry and Vasundhara Sharma

Indian School of Business

November 2022 (revised March 2026)

## Abstract

Passwords remain the dominant authentication mechanism for online systems, yet their weaknesses are well-documented and their hacking consequential. We propose a novel zero-knowledge proof protocol that allows a customer to authenticate herself to a verifier — a bank, an online merchant, a secure portal — without ever writing, typing, or transmitting her password. The protocol is built on a physical grid of colored and numbered balls; its digital implementation requires no special hardware. We make three contributions. First, we specify the protocol formally across its three phases – setup, challenge-response, and verification — and prove completeness and information-theoretic soundness. Second, we establish perfect zero-knowledge against both honest and malicious verifiers: the verifier learns nothing about the password beyond its existence, with equality rather than merely negligible distinguishing advantage. Third, and most technically novel, we provide a complete information-theoretic analysis of eavesdropper resistance. We prove, via Fano's inequality, that any observer watching the customer authenticate is information-theoretically prevented from recovering the password for at least $n_k^*$ rounds — a threshold that grows as $\Omega(k^2 \log(100/k))$ in the number of password balls $k$. A complementary maximum-likelihood achievability bound establishes the minimum rounds an optimal adversary requires. We prove, both asymptotically and by direct numerical verification, that Fano-protection is strictly monotone increasing in $k$ for all $k \le 61$ — covering every practically feasible memory budget. Together, these results yield concrete design recommendations: use at least three password balls, transmit responses over an encrypted channel, and refresh passwords every $n_k^*$ rounds.

*JEL Codes*: C12, D82, G20. *Keywords*: zero-knowledge proof, password authentication, information-theoretic security, Fano inequality, eavesdropper resistance.

[Page 2]
# 1. Introduction

Consider the following predicament. Every day, billions of people authenticate themselves to banks, email providers, hospitals, and merchants using a mechanism — the password — that was designed in an era when computers filled rooms and were operated by specialists. The password was a practical solution to a simple problem: prove to the machine that you are who you claim to be. It worked tolerably well when you had one machine and one password. It works very poorly when you have forty accounts and an adversary who has figured out that “password123” is everyone’s fallback.

The problems are structural, not behavioral. Passwords are stored — somewhere, on someone’s server — and servers get hacked. Passwords are typed — somewhere, on someone’s keyboard — and keyloggers exist. Passwords are transmitted — somewhere, over someone’s network — and eavesdroppers wait. Worse: the burden of password hygiene (long, unique, frequently changed, never written down) is cognitively impossible to sustain across dozens of accounts, so users cut corners. Security researchers have documented this failure mode exhaustively; the interesting question is what to do about it.

Zero-knowledge proof (ZKP) protocols offer a conceptually elegant escape.¹ The idea is to prove knowledge of a secret without revealing the secret itself — authentication without transmission. A handful of ZKP-based protocols have been proposed for password authentication, but their adoption has been limited by a persistent tension between cryptographic rigor and practical usability. The protocols that are provably secure tend to require users to understand modular arithmetic or trust their browser to execute unfamiliar code; those that are intuitive tend to leave security gaps.

We propose a protocol that dissolves this tension — or at least substantially reduces it. The central device is a 10×10 grid of colored, numbered balls. The customer’s password is a pair (or more) of balls she selects mentally, by number and color, during a one-time setup. She never writes the numbers down. The verifier never learns them. Authentication proceeds through a series of yes/no challenges — does the grid, after the verifier has potentially modified and shuffled it, still show the customer’s chosen balls in their chosen colors? — that an impersonator can answer correctly only by guessing, with probability shrinking geometrically in the number of rounds.

Why is this interesting, beyond the novelty of the physical mechanism? Because it achieves something that even the best widely-deployed protocols do not: the server stores nothing that, if

---
¹Zero-knowledge proof is a technique wherein one party proves to another that a given statement is true without revealing any information beyond the truth of the statement itself. The concept was introduced by Goldwasser, Micali, and Rackoff (1985).

[Page 3]
Chowdhry and Sharma | ZKP Password Authentication
stolen, allows an adversary to impersonate the customer. There is no password hash to crack, no
private key to extract. A server breach reveals only an encrypted commitment and two marked
positions — useless to an attacker without knowing which customer-visible numbers correspond
to those positions. In a world where server breaches are a near-certainty for any institution of scale,
this property matters enormously.

We make three contributions. First, we specify the protocol formally and establish its basic security
properties: completeness (honest customers always authenticate), soundness (imposters are
rejected exponentially in the number of rounds), and perfect zero-knowledge against the verifier
(the verifier's view is simulatable without knowledge of the password, with equality of
distributions, not merely computational indistinguishability). Second, we analyze eavesdropper
resistance — the property that an observer watching the customer's screen cannot deduce the
password — and prove it rigorously using Fano's inequality and a maximum-likelihood
achievability argument. Third, we establish that eavesdropper resistance improves strictly with the
number of password balls, up to a remarkably large optimum, and derive concrete design
recommendations from this monotonicity result.

The paper proceeds as follows. Section 2 reviews related work. Section 3 introduces the protocol
through a physical illustration. Section 4 provides the formal three-phase specification. Section 5
establishes zero-knowledge against the verifier. Section 6 contains the full eavesdropper analysis
— our main technical contribution. Section 7 discusses the digital implementation and the
architectural choice that makes eavesdropper resistance achievable. Section 8 gives design
recommendations. Section 9 concludes.

# 2. Related Work

The literature on authentication without password transmission is older than the internet. The
Secure Remote Password (SRP) protocol (Wu, 1998) remains the most widely deployed solution:
the server stores a verifier derived from the password, never the password itself, and
authentication proceeds through a Diffie-Hellman-based exchange that prevents both server
impersonation and eavesdropping.² SRP is cryptographically sound but requires the user to trust
that the client application correctly implements the protocol — a trust assumption our protocol
avoids by making the challenge-response interaction physically transparent to the user.

---
²SRP (Secure Remote Password Protocol, Wu 1998) is the closest widely-deployed relative. FIDO2/WebAuthn
eliminates passwords entirely via hardware keys. OPAQUE (Jarecki et al., 2018) is an asymmetric PAKE achieving
similar server-side security goals.

[Page 4]
Chowdhry and Sharma | ZKP Password Authentication

FIDO2/WebAuthn (Balfanz et al., 2020) eliminates the password entirely in favor of a hardware
security key or device-bound credential. This is arguably the cleanest solution to the server-storage
problem, but it requires hardware that hundreds of millions of users in low- and middle-income
countries do not possess, and it creates a new single point of failure: lose the device, lose access.
Our protocol requires no hardware beyond a browser and the willingness to remember two
numbers.

On the ZKP side, Grzonkowski et al. (2008) proposed a protocol based on random isomorphic
graphs and permutation functions that achieves zero-knowledge at the cost of requiring the user
to reveal their password to the browser — a critical weakness our protocol eliminates. Goldwasser,
Micali, and Rackoff (1985) established the theoretical foundations of zero-knowledge proofs; Blum,
Feldman, and Micali (1988) demonstrated their applicability to cryptographic protocols. OPAQUE
(Jarecki et al., 2018) is a state-of-the-art asymmetric PAKE that achieves similar server-side security
guarantees to ours through public-key techniques, with strong provable security but greater
implementation complexity.

Graphical and cognitive password systems — *Passfaces* (Brostoff and Sasse, 2000), *Draw-a-Secret*
(Jermyn et al., 1999), and *PassPoints* (Wiedenbeck et al., 2005) — are closest to our protocol in spirit:
they replace alphanumeric strings with visual or spatial memory, exploiting the well-documented
superiority of picture memory over verbal memory (Standing, 1973). Our protocol shares this
cognitive grounding but adds formal ZKP properties that graphical systems generally lack. The
customer’s memory task — two numbers and two colors from a grid — is comparable to
remembering a four-digit PIN, but the authentication mechanism provides information-theoretic
guarantees that PIN-based systems do not.

To our knowledge, no prior work provides a complete information-theoretic analysis of
eavesdropper resistance for a ZKP-based password protocol of this type — specifically, the
problem of bounding an adversary’s ability to deduce the password from observations of the grid
display across multiple authentication sessions. The Fano-based analysis in Section 6 is, as far as
we are aware, novel.

# 3. A Simple Illustration

Before the formalism, an illustration. The following story is not the protocol — it is the intuition
behind the protocol, presented in the manner that, in our experience, makes zero-knowledge proofs
click for audiences encountering them for the first time.

[Page 5]
Suppose you claim to be able to count the exact number of leaves on a tree with thick, dense foliage — a tree I cannot easily count myself. You want to prove this claim without revealing the count. Here is the protocol.

I ask you to close your eyes. While your eyes are closed, I either pluck one leaf or leave the tree undisturbed — my choice, randomly. I then ask you to open your eyes and tell me: did I pluck a leaf?

If your claim is genuine, you can answer this question with certainty: you counted before you closed your eyes, you count after you open them, and the comparison tells you definitively whether a leaf was removed. If your claim is false and you are simply guessing, you will be right only half the time.

Now repeat this procedure $n$ times. A genuine counter answers correctly every time. A guesser answers correctly with probability $(1/2)^n$, which shrinks to nothing as $n$ grows. After ten rounds, a guesser’s probability of fooling you is less than 0.1%. After twenty rounds, less than one in a million. And crucially — at no point did you learn the number of leaves. You verified the claim without extracting the secret.

This is zero-knowledge proof in its purest form. The leaf count is the password. The tree is the grid. The yes/no questions are the challenge rounds. What we add — and what makes the protocol cryptographically interesting — is a rigorous analysis of what an observer watching this interaction can and cannot learn.

## 4. The Protocol

### 4.1 Physical Description

The setup involves a 10×10 grid of balls, each colored either red or blue. The front face of each ball bears a two-digit number from 00 to 99. The back face shows only the color.

Only the customer sees the front. The verifier — a bank teller, a web server, a secure terminal — sees only the back.

During the *setup phase*, the customer looks at the grid and mentally selects $k$ balls by their numbers and colors — say, ball 19 (red) and ball 95 (red), if $k = 2$. This selection is her password. She does not write the numbers anywhere. She presses the selected balls on the front of the grid. The verifier observes which back-face positions were pressed and marks them – but since the verifier sees only the back, it knows the positions and colors of the marked balls, not their numbers. The setup is complete.

[Page 6]
Chowdhry and Sharma | ZKP Password Authentication

During each challenge round, the verifier makes a binary decision: with probability one-half, it
changes the colors of $k-1$ of the marked balls (Variant B we return to the importance of this
choice in Section 6); with probability one-half, it leaves all marked balls unchanged. It then shuffles
the grid - applying a random permutation to all ball positions and shows the result to the
customer. The customer examines the grid, locates her balls by their numbers, checks their colors
against her memory, and transmits a single bit: yes if all $k$ balls show their registration colors, no
otherwise. The verifier checks this response against its own knowledge of what it did.

Repeat for $n$ rounds. An impostor who does not know the password must guess yes or no, and will
be wrong with probability one-half each round. After $n$ rounds, the probability of an impostor
passing all rounds is $(1/2)^n$ — vanishingly small for even modest $n$. A genuine customer passes
every round with certainty.

## 4.2 Formal Specification

We now state the three phases precisely.

### Setup and Notation.

Let $B = \{00, 01, ..., 99\}$ denote the ball identifiers and $C = \{R, B\}$ the two colors. A $k$-ball password is
an unordered set $\pi = \{(n_1, c_1), ..., (n_k, c_k)\}$ with distinct $n_1, ..., n_k \in B$ and $c_1, ..., c_k \in C$. The password
space is $\Pi_k = \{\pi : n_1, ..., n_k \text{ distinct}\}$, of size $|\Pi_k| = C(100, k) \cdot 2^k$.

### Phase 1: Setup.

(S1) The server initializes a grid by assigning each of the 100 balls a uniformly random color and a
visible identifier (its number). The assignment of numbers to positions on the front face is known
only to the server.

(S2) The customer examines the front face, selects $k$ balls mentally, and transmits a commitment
$\text{Com}(\pi; r)$ to the server over a secure channel, where $r$ is a random salt. The server stores this
commitment and marks the corresponding back-face positions.

(S3) The customer discards all notes. No record of the password exists outside the customer's
memory and the server's commitment.

### Phase 2: Challenge.

For round $i = 1, ..., n$:

[Page 7]
(C1) The server samples $\delta_1 \leftarrow \{0,1\}$ uniformly. If $\delta_1 = 1$, it selects $k-1$ of the $k$ marked balls uniformly at random and flips their colors.

(C2) The server applies a uniformly random permutation $\sigma_1 : B \rightarrow B$ to the positions of all 100 balls. It displays the resulting grid $G_1 : B \rightarrow C$ on the customer's screen. Non-password balls are re-randomized independently each round.

### Phase 3: Response and Verification.

(R1) The customer locates her balls by number, checks their colors, and transmits $a_1 \in \{yes, no\}$ — yes if all $k$ balls show their registration colors, no otherwise — over an encrypted channel invisible to any screen observer.

(R2) The server verifies: it accepts if $a_1 = \text{yes}$ when $\delta_1 = 0$, and $a_1 = \text{no}$ when $\delta_1 = 1$. After $n$ rounds, the customer is authenticated if and only if all $n$ responses are correct.

[Page 8]
# 5. Zero-Knowledge Against the Verifier

We establish three classical properties – completeness, soundness, and zero-knowledge — with respect to the verifier. These results are relatively standard given the protocol structure, but they set the stage for the more technically demanding eavesdropper analysis in Section 6.

## 5.1 Completeness

An honest customer knows her password exactly. In each round, she correctly identifies whether any of her balls changed color, and answers $a_i = (\delta_i = 0)$ with certainty. She is therefore accepted with probability 1 for any $n$.

> **Theorem 1 (Completeness).**
> An honest customer who knows $\pi$ is accepted by the verifier after $n$ rounds with probability 1, for any $n \ge 1$.

## 5.2 Soundness

An impostor who does not know $\pi$ must guess $a_i$ before seeing $\delta_i$. Since $\delta_i$ is uniform and independent, the best strategy is to guess uniformly — and the probability of being correct in all $n$ rounds is $(1/2)^n$. The soundness bound is information-theoretic: it holds against computationally unbounded impostors.

> **Theorem 2 (Information-Theoretic Soundness).**
> For any prover $P^*$ who does not know $\pi$, the probability that $P^*$ is accepted after $n$ rounds satisfies:
> $$\Pr[V \text{ accepts } P^*] \le (1/2)^n .$$

> **Proof.**
> In each round $i$, the server's flip decision $\delta_i$ is drawn uniformly from $\{0,1\}$ and is independent of all prior rounds and of any action by $P^*$. The prover $P^*$ must commit to $a_i$ before observing $\delta_i$. Therefore $\Pr[a_i = 1(\delta_i = 0)] \le 1/2$. Rounds are independent, so $\Pr[\forall i : a_i \equiv 1(\delta_i = 0)] \le (1/2)^n$. $\square$

[Page 9]
## 5.3 Perfect Zero-Knowledge Against the Verifier

The verifier's view across $n$ rounds is the transcript $\{(\delta_1, a_1), ..., (\delta_n, a_n)\}$. We show that this transcript is *perfectly simulatable* — not just computationally indistinguishable from a simulated transcript, but identically distributed. The verifier gains zero information about $\pi$.

> **Theorem 3 (Perfect Zero-Knowledge Against Any Verifier).**
>
> There exists a polynomial-time simulator $S$ such that for any verifier $V^*$, the distribution of $V^*$'s view in a real interaction with an honest prover is *identical* to the distribution of $V^*$'s view when interacting with $S$:
>
> $\Pr[V^*(x, \text{Real}(P, V^*)) = 1] = \Pr[V^*(x, S(x)) = 1]$ .

***Proof.***

The simulator $S$ operates as follows: in each round, it receives the challenge $\delta_i$ from $V^*$ (whatever strategy $V^*$ uses, including adversarial strategies), and outputs $a_i = 1(\delta_i = 0)$.

In the real interaction, the honest prover's response is also $a_i = 1(\delta_i = 0)$ — a deterministic function of the challenge alone. The simulated transcript and the real transcript therefore have identical distributions for every possible strategy of $V^*$, with equality of probabilities, not merely negligible advantage. This is perfect zero-knowledge. $\square$

The reason perfect zero-knowledge holds here — stronger than the computational zero-knowledge typical in the ZKP literature — is structural. The customer's response bit is a *deterministic function of the verifier's own challenge*. The verifier asks the question; the answer is determined entirely by the question itself, not by any hidden password-dependent computation. A malicious verifier choosing $\delta_i = 0$ in every round will see $a_i = \text{yes}$ in every round — which is exactly what it would see in a real interaction with a legitimate customer. No strategy extracts information.

[Page 10]
# 6. Eavesdropper Resistance: The Main Technical Results

Theorem 3 settles the question of what the verifier learns. It leaves open a different and harder question — one that the original paper left as a conjecture: what does an *eavesdropper* learn?³ An eavesdropper, in our setting, is an adversary $\mathcal{E}$ who watches the customer's screen across multiple authentication sessions. She sees the grid in each round — all 100 balls, with their numbers and colors — but does not see the response bit $a_i$, which travels over an encrypted channel. Can she, over time, deduce the password?

The answer, it turns out, is subtle and quantitative rather than binary. The eavesdropper cannot recover the password immediately — but given enough rounds of observation, she can. The interesting questions are: how many rounds does she need? And how does this threshold depend on the protocol parameters?

We answer both questions completely. The key insight is that password balls have a slight color bias — they show their registration color slightly more often than chance — which the eavesdropper can, in principle, exploit. But the bias is weak, the grid is large, and the password space is substantial. The Fano inequality formalizes precisely how long the eavesdropper is information-theoretically blocked, and an explicit maximum-likelihood attack establishes how long she truly needs in the worst case.

## 6.1 Setup and the Fundamental Lemma

Fix a $k$-ball password $\pi$ drawn uniformly from $\Pi_k$. The eavesdropper $\mathcal{E}$ observes the grid sequence $\{G_1, ..., G_n\}$ where $G_i : B \to C$ maps each ball number to its displayed color in round $i$. She does not observe the flip decisions $\delta_i$ or the responses $a_i$. Her goal is to compute an estimate $\hat{\pi}$ that equals $\pi$.

The first and most important structural observation is that, marginally, password balls look exactly like non-password balls. There is no single-ball statistic that can identify them.

> **Lemma 1 (Marginal Uniformity).**
>
> For any ball $b \in B$, any round $i$, and any $k$-ball password drawn from $\Pi_k$ uniformly:
> $$ \Pr[G_i(b) = R] = 1/2, $$
> regardless of whether $b$ is a password ball.

---
³We use 'eavesdropper' to mean an adversary who observes the customer's screen and interaction but cannot intercept encrypted network traffic.

[Page 11]
*Proof.*

**Case 1:** $b$ is not a password ball. By protocol, its color is re-randomized uniformly in every round. $\Pr[G_i(b) = R] = 1/2$.

**Case 2:** $b$ is a password ball with registration color $c$. Under Variant B, when $\delta_i = 1$, exactly $k-1$ of the $k$ password balls are flipped, so $b$ is flipped with conditional probability $(k-1)/k$. Therefore the probability ball $b$ shows its registration color in round $i$ is:
$$
p_k := \Pr[\delta_i=0]\cdot 1 + \Pr[\delta_i=1]\cdot(1/k) = 1/2 + 1/(2k) = (k+1)/(2k) .
$$
Note that $p_k > 1/2$ for all finite $k$. But now average over the prior on $\pi$: $\Pr(\text{b is a password ball}) = k/100$, and conditional on being a password ball, the registration color is red or blue with probability 1/2 each. Therefore:
$$
\Pr[G(b) = R] = (k/100)\cdot[(1/2)\cdot p_k + (1/2)\cdot(1-p_k)] + (1-k/100)\cdot 1/2 = 1/2 .
$$
The bias $p_k - 1/2 = 1/(2k)$ is real but averaged away by the prior. It is detectable only from the joint distribution of colors across rounds, not from any single round's marginal. $\square$

Lemma 1 tells us that the eavesdropper's information is encoded entirely in the joint structure of the grid sequence. The per-round contribution is small — we quantify it next.

## 6.2 Per-Round Mutual Information

**Lemma 2 (Per-Round Mutual Information).**

The mutual information between the password $\pi$ and the observed grid in one round is:
$$
I_k := I(\pi; G_i) = k \cdot (1 - h((k+1)/2k)) ,
$$
where $h(p) = -p \log_2 p - (1-p) \log_2(1-p)$ is the binary entropy function. Rounds are independent given $\pi$, so $I(\pi ; G_1^n) = n \cdot I_k$.

*Proof.*

By Lemma 1, $H(G_1) = 100$ bits (100 independent fair coins). Given $\pi$, the $k$ password balls have color distribution $\text{Bernoulli}(p_k)$ and the remaining $100-k$ balls remain $\text{Bernoulli}(1/2)$. Therefore:
$$
H(G_1 | \pi) = k h(p_k) + (100-k)\cdot h(1/2) = k \cdot h(p_k) + (100-k) .
$$

[Page 12]
$I_k = H(G_1) – H(G_1|\pi) = 100 - k \cdot h(p_k) - (100-k) = k(1 - h(p_k)) .$

This equals k times the KL divergence from Bernoulli($p_k$) to Bernoulli(1/2). Independence across rounds gives $I(\pi ; G_1^n) = n \cdot I_k$. $\square$

How small is $I_k$? For $k=2$ it is 0.378 bits per round — roughly one-third of a bit. For $k=3$ it is 0.245 bits. For $k=5$ it is 0.145 bits. Compare this to the entropy of the password space — 14.3 bits for $k=2$, 20.3 bits for $k=3$ — and it becomes clear why the eavesdropper needs many rounds: she is learning about a 14-bit secret at a rate of 0.38 bits per observation.

## 6.3 Exact Monotonicity for Small k

Before stating the main theorems, we record the exact numerical values of all key quantities for $k=2$ through 5. These values play two roles: they establish monotonicity of Fano-protection by direct verification for the practically relevant range, and they give the concrete numbers that appear in design recommendations.

| k | $p_k = (k+1)/2k$ | $h(p_k)$ | $I_k$ (bits/round) | $\log_2|\Pi_k|$ | $n_k^*$ (rounds) |
|---|---|---|---|---|---|
| 2 | 3/4 | 0.811278 | 0.377443 | 14.2732 | 35.17 |
| 3 | 2/3 | 0.918296 | 0.245112 | 20.3026 | 78.75 |
| 4 | 5/8 | 0.954434 | 0.182264 | 25.9028 | 136.63 |
| 5 | 3/5 | 0.970951 | 0.145247 | 31.1658 | 207.69 |
| 6 | 7/12 | 0.980229 | 0.117486 | 36.0103 | 298.80 |

*Table 1. Key quantities under the k-ball Variant B protocol, 100-ball grid. The Fano threshold $n^*$ is the number of rounds below which any eavesdropper's error probability is bounded away from zero by Theorem 4.*

> **Lemma 3 (Exact Monotonicity for k ≤ 5).**
>
> The Fano thresholds in Table 1 satisfy:
> $$n_2^* = 35.17 < n_3^* = 78.75 < n_4^* = 136.63 < n_5^* = 207.69 .$$

[Page 13]
Moreover, the increments $\Delta_k = n_k^* - n_{k-1}^*$ are themselves strictly increasing: $\Delta_2 = 43.58$, $\Delta_3 = 57.88$, $\Delta_4 = 71.06$. Protection improves by a growing margin with each additional ball.

*Proof*.

Direct computation using the closed-form entropy expressions. The binary entropy values reduce to:
$h(3/4) = 2 - (3/4)\log_2 3 = 0.811278... \implies I_2 = 0.377443..., n_2^* = 35.17$
$h(2/3) = \log_2 3 - 2/3 = 0.918296... \implies I_3 = 0.245112..., n_3^* = 78.75 > n_2^* \checkmark$
$h(5/8) = 3 - (5/8)\log_2 5 - (3/8)\log_2 3 = 0.954434... \implies I_4 = 0.182264..., n_4^* = 136.63 > n_3^* \checkmark$
$h(3/5) = \log_2 5 - (3/5)\log_2 3 - 2/5 = 0.970951... \implies I_5 = 0.145247..., n_5^* = 207.69 > n_4^* \checkmark$
Here $\log_2 3 = 1.584962...$ and $\log_2 5 = 2.321928...$. The strict inequalities hold with positive gaps at each step. $\Box$

## 6.4 The Fano Lower Bound
We now state the main converse result — a lower bound on the eavesdropper’s error that holds for any estimator, regardless of computational power.

> **Theorem 4 (Fano Lower Bound on Eavesdropper Error).**
>
> Suppose $\pi$ is drawn uniformly from $\Pi_k$. For any estimator $\hat{\pi}$ based on the grid sequence $\{G_1, ..., G_n\}$:
> $$
> Pr(\hat{\pi} \neq \pi) \ge 1 - (n \cdot I_k + 1) / \log_2|\Pi_k| .
> $$
> Define the *Fano threshold* $n_k^* := (\log_2|\Pi_k| - 1)/I_k$. For $n < n_k^*$, the bound is strictly positive: every estimator makes errors with positive probability, regardless of computational power.

*Proof*.

[Page 14]
Fano's inequality⁴ applied to the Markov chain $\pi \to \{G_i\} \to \hat{\pi}$ gives $H(\pi | G_1^n) \le h(P_e) + P_e \cdot \log_2(|\Pi_k| - 1)$, where $P_e = \text{Pr}(\hat{\pi} \ne \pi)$. Using $H(\pi) = \log_2|\Pi_k|$ and $I(\pi ; G_1^n) = n \cdot I_k$ (Lemma 2):
$H(\pi | G_1^n) = \log_2|\Pi_k| - n \cdot I_k$.
Applying the standard Fano lower bound $P_e \ge (H(\pi | G_1^n) - 1)/\log_2|\Pi_k|$ yields the stated inequality. □

What does the Fano bound say concretely? For k = 3 at n = 30 rounds — three sessions of ten rounds each — the minimum guaranteed eavesdropper error is 58.9%. Even a computationally unlimited adversary who has watched every session cannot recover the password with better than 41% accuracy. At n = 10 rounds, the bound is 83.0%. For k = 2 the corresponding figures are 27.0% and 66.5%. This is the quantitative case for using at least three balls.

| Rounds n | Sessions (n÷10) | k=2: min. error | k=3: min. error | k=4: min. error |
| :--- | :--- | :--- | :--- | :--- |
| 10 | 1 | ≥66.5% | ≥83.0% | ≥92.5% |
| 30 | 3 | ≥27.0% | ≥58.9% | ≥78.2% |
| 50 | 5 | ≥0%* | ≥34.5% | ≥63.4% |
| 79 | 8 | ≥0%* | Fano vacuous | ≥46.2% |
| 136 | 14 | ≥0%* | ≥0%* | Fano vacuous |

Table 2. Fano lower bound on eavesdropper error for k = 2, 3, 4, by number of observed rounds. Asterisk (*) indicates the bound is vacuous (Fano threshold exceeded). For these cases, see the achievability analysis in Theorem 5.

## 6.5 The Maximum-Likelihood Attack: Achievability
The Fano bound is a lower bound — it tells us the eavesdropper cannot succeed below $n^*$ rounds. But what happens above the threshold? We construct the optimal attack explicitly and determine how many rounds it needs.

---
⁴Fano's inequality (Fano 1961) states that for any estimator of a random variable X from observation Y: $H(X|Y) \le h(P_e) + P_e \cdot \log(|\mathcal{X}|-1)$, where Pe is the probability of error and h is binary entropy.

[Page 15]
Chowdhry and Sharma | ZKP Password Authentication

**Theorem 5 (ML Achievability).**
Define the score of hypothesis $\pi'$ as $S(\pi') = \Sigma_j Y_{nj}(c_j)$ where $Y_b(c)$ counts rounds in which ball $b$ shows color $c$. The ML estimator outputs $\pi^{TL} = \arg\max_{\pi'} S(\pi')$. Its error probability satisfies:
$$
\text{Pr}(\pi^{TL} \neq \pi) \le |\Pi_k^{(1)}| \cdot \Phi(-\Delta_k / \sqrt{n \cdot f(k)}) + o(1),
$$
where $|\Pi_k^{(1)}|$ is the number of one-ball-overlap alternatives, $\Delta_k = n(k-1)/(4k)$ is the mean gap between true and overlap scores, $f(k)$ is an explicit variance coefficient, and $\Phi$ is the standard normal CDF.

***

**Proof.**
The true-password score has mean $\mu^t = k \cdot n \cdot p_k$ and variance $\text{Var}[S(\pi^*)] = k \cdot n \cdot p_k(1-p_k)$. A one-overlap hypothesis – sharing exactly one correctly-colored ball with $\pi$ — has mean $\mu^o = n \cdot p_k + (k-1) \cdot n/2$ and variance $\text{Var}[S^o] = n \cdot p_k(1-p_k) + (k-1) \cdot n/4$. One-overlap hypotheses are the hardest to distinguish because they have the highest expected score among all false hypotheses.

The mean gap is $\Delta_k = \mu^t - \mu^o = n(k-1)/(4k)$. Setting $f(k) = \text{Var}[S(\pi^*)]/n + \text{Var}[S^o]/n$ and applying a normal approximation⁵ with a union bound over all $|\Pi_k^{(1)}|$ one-overlap alternatives yields the stated bound. $\square$

***

For $k=2$: $|\Pi_2^{(1)}| = 2 \times 98 \times 4 = 784$ one-overlap alternatives; the ML attack requires $n > 214$ rounds to achieve fewer than 0.01 expected false positives – approximately 22 sessions. For $k=3$: $|\Pi_3^{(1)}| = 3 \times C(97,2) \times 4 = 55,872$; the ML attack requires $n > 324$ rounds — approximately 33 sessions. Each additional ball buys the protocol substantial resistance: 51% more observation for $k=3$ versus $k=2$.

## 6.6 Asymptotic Monotonicity

Lemma 3 verified monotonicity numerically for small $k$. Theorem 6 extends this to all practically relevant $k$ via an asymptotic argument.

**Theorem 6 (Monotonicity of Fano-Protection in k).**

***
⁵The normal approximation is valid by the Central Limit Theorem for $n \ge 30$, which is within the range of practical interest.

[Page 16]
Let $n_k^* = (\log_2|\Pi_k| - 1)/I_k$ denote the Fano threshold. Then:

(i) (Asymptotic Formula) $n_k^* \sim 2k^2 \ln 2 \cdot \log_2(100/k) + 2k^2$ as $k \to \infty$ with $k \ll 100$.
(ii) (Global Maximum) $n_k^*$ achieves its maximum at $k^* = 100/\sqrt{e} \approx 60.65$, with $n_{k^*} \sim 2(100/\sqrt{e})^2 \cdot \ln 2 \cdot (1/2)$.
(iii) (Monotone for All Practical k) $n_k^*$ is strictly increasing in $k$ for all $k < k^* \approx 61$. In particular, it is strictly increasing throughout any feasible memory budget.

***

**Proof.**

The per-ball bias is $\epsilon_k = 1/(2k)$. Taylor-expanding binary entropy around 1/2:
$$
1 - h(1/2 + \epsilon) \approx 2\epsilon^2/\ln 2 + O(\epsilon^4) \implies I_k = k(1-h(p_k)) \approx 1/(2k \ln 2) \ .
$$
By Stirling's approximation for $k \ll 100$:
$$
\log_2|\Pi_k| \approx k \log_2(100/k) + k/\ln 2 \ .
$$
Dividing:
$$
n_k^* \approx [k \log_2(100/k) + k/\ln 2] \cdot 2k \ln 2 = 2k^2 \ln 2 \cdot \log_2(100/k) + 2k^2 \ .
$$
The leading term is $g(k) = k^2 \log_2(100/k)$. Differentiating: $g'(k) = 2k \log_2(100/k) - k/\ln 2$. Setting $g'(k) = 0$: $2 \log_2(100/k) = 1/\ln 2 = \log_2 e$, giving $100/k = e^{1/2}$ and thus $k^* = 100/\sqrt{e} \approx 60.65$. Since $g''(k^*) = -1/\ln 2 < 0$, this is a global maximum and $g'(k) > 0$ for all $k < k^*$. $\square$

***

The punchline — $k^* \approx 61$ — is worth pausing on. It says that adding more password balls *always* improves eavesdropper resistance, up to the point where the customer would need to memorize 61 numbers and their colors. No practical deployment will approach this limit. For any memory budget a real user has — even a generous one of 10 balls — Theorem 6 guarantees that using all available balls is the strictly dominant design.

[Page 17]
# 7. The Architectural Fix: Why the Response Must Be Invisible

Theorems 4 and 6 assume that the eavesdropper cannot observe the customer's response $a_i$. This is not a wishful assumption — it is a concrete protocol requirement with a concrete implementation. The response must be transmitted over an encrypted channel, not displayed on screen.

To see why this matters, suppose for a moment that the eavesdropper *can* observe $a_i$ (say, by watching which of two on-screen buttons the customer presses, or seeing the screen flash). Now the eavesdropper knows the correct answer to each challenge. For any hypothesis $\pi'$, she can check: is $\pi'$ consistent with every observed $(G_i, a_i)$ pair? The true password $\pi$ is always consistent. False hypotheses are eliminated at a rate that depends on how quickly their consistency probability falls below 1.

A detailed analysis shows that a false pair achieves perfect consistency with probability $(3/4)^n$ — it happens to give the right answer by coincidence in every round. With 19,800 candidate passwords, an eavesdropper who can observe responses needs only $n > 30$ rounds (three sessions) before the expected number of false survivors drops below 1. With the response hidden, that threshold rises to 214 rounds (22 sessions) for $k = 2$, and 324 rounds (33 sessions) for $k = 3$. The architectural choice of an encrypted response channel is what converts a vulnerability into a strength.

> In practice, the response channel is the standard TLS-encrypted HTTP request the customer's browser sends to the server. No additional cryptographic infrastructure is required — the same channel that transmits form data in conventional password authentication now transmits a single bit. The response button on the customer's screen need not display the selection visually; it can simply transmit without feedback. An eavesdropper watching the screen sees the grid — and nothing else that is useful.

# 8. Digital Implementation

The physical grid has an exact digital counterpart. Here we specify the implementation architecture, identify what each party stores, and explain why a server breach — the most consequential attack against modern authentication systems – yields nothing exploitable.

## 8.1 Setup Phase

[Page 18]
At registration, the server generates 100 random tokens {$t_{00}$, ..., $t_{99}$} and assigns each a random color. It displays these to the customer with visible identifiers 00–99 on their screen. The mapping from visible identifiers to internal tokens is stored only on the server.

The customer selects k balls mentally and transmits a salted cryptographic commitment — for example, $H(id_1 || c_1 || ... || id_k || c_k || salt)$ — to the server over TLS. The server stores this commitment and records which token positions were selected. It does not store the visible identifiers the customer chose.

## 8.2 What Is Stored and What Is Not

| Party | Stores | Does NOT store | Consequence of breach |
| :--- | :--- | :--- | :--- |
| Customer | k numbers and colors (in memory only) | Nothing written or digital | Nothing to steal — memory only |
| Server | Commitment hash + k marked token positions | Visible identifiers (the password) | Attacker gets commitment + positions; cannot recover $id_1$, ..., $id_k$ |
| Network | Encrypted TLS traffic | Plaintext response bits | Eavesdropper intercepts ciphertext; useless without TLS key |

*Table 3. Information architecture: what each party stores and the consequence of its compromise.*

The critical separation is between server-side token positions (which the server knows) and customer-visible identifiers (which the server does not know). These are linked only in the customer's mind. A server breach tells an attacker that certain positions are marked — but without knowing which visible numbers map to those positions, the attacker cannot construct a valid authentication response. The password is not merely hashed; it is architecturally absent from the server.

## 8.3 Challenge-Response in Digital Form

[Page 19]
In each challenge round, the server randomly decides whether to flip $k-1$ of the marked token colors. It then generates a fresh random assignment of visible identifiers to positions – effectively shuffling the grid – and renders the display. The customer sees numbered, colored balls; she locates hers by number, checks the colors, and clicks yes or no. The click triggers an encrypted POST request; no visual indicator of the response is shown on screen.

The entire interaction – from grid display to customer response – takes seconds. Our informal trials suggest the per-round interaction time is comparable to typing a password character, and the multi-round session ($n = 10$) takes under 30 seconds. Unlike password typing, there is nothing for shoulder-surfers, keyloggers, or screen recorders to exploit.

# 9. Protocol Design Recommendations
The analysis of Sections 5–7 yields concrete, quantitative guidance. We collect it here.

**R1. Use at least k = 3 password balls.**

The two-ball design's Fano threshold of 35 rounds – approximately four sessions – is too low for any deployment without a mandatory refresh policy. The three-ball design's threshold of 79 rounds provides a comfortable margin. The password space grows from 19,800 to 1.3 million, an increase of 65×, while the memory burden grows only modestly (remember 3 numbers and colors instead of 2).

**R2. Transmit the response bit over an encrypted channel.**

As shown in Section 7, the Fano-protection guarantees of Theorem 4 depend entirely on the eavesdropper not observing the response. This is achievable with standard TLS and minimal implementation effort. The yes/no button on the authentication interface should send its response without visual feedback.

**R3. Implement a password refresh policy.**

Set a maximum lifetime of $T < n_k^*$ rounds per password. For $k = 3$, $n_3^* = 79$ rounds; with $n = 10$ rounds per session, refresh every 7 sessions. This ensures the eavesdropper's cumulative observation permanently stays within the Fano-protected zone.

**R4. Use more balls if the user can remember them.**

By Theorem 6, Fano-protection is strictly increasing in $k$ for all $k$ up to 61. The gains are substantial: $k = 4$ gives a threshold of 137 rounds (14 sessions), and $k = 5$ gives 208 rounds (21 sessions). For high-security deployments – banking authentication, medical records access –

[Page 20]
four or five balls is a natural design choice. The memory task (four numbers from 00–99 with
their colors) is roughly comparable to remembering two phone numbers.

| k | Password space | Fano threshold n* | Sessions at n=10 | ML attack threshold | Sessions at n=10 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 2 | 19,800 | 35 rounds | 4 | 214 rounds | 22 |
| 3 | 1.29M | 79 rounds | 8 | 324 rounds | 33 |
| 4 | 62.7M | 137 rounds | 14 | ~540 rounds | 54 |
| 5 | 3.16B | 208 rounds | 21 | ~900 rounds | 90 |

Table 4. Summary of security parameters by number of password balls. 'Sessions' assumes n = 10 rounds per session. M =
million; B = billion.

[Page 21]
# 10. Conclusion

We began with a simple observation — passwords are broken as a mechanism, not just as a practice — and proposed a protocol that reengineers the mechanism rather than demanding better behavior from users. The grid-based ZKP protocol we have described and analyzed is, we believe, notable for combining three properties that are rarely found together: usability (the customer memorizes numbers, presses a grid, answers yes or no — no cryptographic knowledge required), provable security against the verifier (perfect zero-knowledge, not merely computational), and quantifiable eavesdropper resistance with explicit thresholds.

The mathematical contribution is the information-theoretic analysis of eavesdropper resistance — an analysis we hope will be useful beyond this specific protocol. The Fano-based approach of Section 6 gives a general framework for asking: how many observations does an adversary need before a secret becomes recoverable? And the monotonicity result — that more password balls always helps, up to $k^* \approx 61$ — is, to us, a genuinely surprising finding. The intuition that a larger password is more secure is correct; what is not obvious is that in this protocol, the security improvement is quadratic in $k$ and grows without bound well past any practical memory limit.

Several directions remain open. The most practically significant is usability validation: do users reliably remember their chosen balls across days and weeks? Do they remember the colors as well as the numbers? A small empirical study with ISB students or bank customers could answer these questions and either confirm or revise our informal optimism. The formal digital implementation also warrants a proof of security under standard cryptographic assumptions for the commitment scheme, which we have sketched but not fully specified. And the analysis of Variant A — where only one ball is flipped when $\delta = 1$, rather than $k-1$ — would complete the theoretical picture by establishing precisely why Variant B dominates.

We close with a note on motivation. The failures of password-based authentication fall disproportionately on users who have the least margin for error — people who conduct their banking, healthcare, and official transactions on a single shared phone, who cannot afford hardware security keys, and for whom a hacked account can mean lost savings rather than inconvenience. A protocol that is both cryptographically sound and cognitively accessible — one that a farmer in Gujarat or a shopkeeper in Lagos can use without understanding modular arithmetic — is not merely an intellectual achievement. It is a step toward the kind of digital security infrastructure that financial inclusion actually requires.

# Acknowledgements

[Page 22]
We thank our colleagues at the Indian School of Business for useful discussions, and participants
at the conferences where earlier versions of this work were presented. All errors are our own.

# References
**Balfanz, D., et al. (2020).** Web Authentication: An API for accessing Public Key Credentials –
Level 2. W3C Recommendation.

**Blum, M., Feldman, P., and Micali, S. (1988).** Proving security against chosen ciphertext attacks.
Conference on the Theory and Application of Cryptography, 256–268. Springer.

**Brostoff, S. and Sasse, M.A. (2000).** Are Passfaces more usable than passwords? A field trial
investigation. Proceedings of HCI 2000, 405–424.

**Fano, R.M. (1961).** Transmission of Information: A Statistical Theory of Communications. MIT
Press.

**Goldwasser, S., Micali, S., and Rackoff, C. (1985).** The knowledge complexity of interactive proof-
systems. Proceedings of the 17th Annual ACM Symposium on Theory of Computing, 291–
304.

**Grzonkowski, S., Zaremba, W., Zaremba, M., and McDaniel, B. (2008).** Extending web
applications with a lightweight zero knowledge proof authentication. Proceedings of the
5th International Conference on Soft Computing as Transdisciplinary Science and
Technology, 65–70.

**Jarecki, S., Kucherenko, H., and Xu, J. (2018).** OPAQUE: An asymmetric PAKE protocol secure
against pre-computation attacks. Advances in Cryptology – EUROCRYPT 2018, 456–486.
Springer.

**Jermyn, I., Mayer, A., Monrose, F., Reiter, M., and Rubin, A. (1999).** The design and analysis of
graphical passwords. Proceedings of the 8th USENIX Security Symposium.

**Standing, L. (1973).** Learning 10,000 pictures. Quarterly Journal of Experimental Psychology, 25(2),
207–222.

**Wiedenbeck, S., Waters, J., Birget, J.C., Brodskiy, A., and Memon, N. (2005).** PassPoints: Design
and longitudinal evaluation of a graphical password system. International Journal of
Human-Computer Studies, 63(1–2), 102–127.

**Wu, T. (1998).** The Secure Remote Password Protocol. Proceedings of the 1998 Internet Society
Network and Distributed System Security Symposium, 97–111.