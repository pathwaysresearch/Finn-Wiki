---
type: synthesized
aliases: ["Profitability Ratio Method", "PI Method"]
tags: ["capital-budgeting", "project-evaluation", "finance-theory"]
relationships:
  - target: net-present-value
    type: extends
  - target: capital-budgeting
    type: extends
  - target: stub-mit15-401f08-ses18-300ksrt
    type: extends
---

# Profitability Index vs NPV: Identical Decisions, Different Rankings

# Profitability Index vs NPV: Identical Decisions, Different Rankings

The **profitability index (PI)**, also called the profitability ratio method, is a capital budgeting technique defined as:

> PI = PV of future cash flows / Initial investment

Equivalently, PI = 1 + (NPV / Initial investment).

## Equivalence for Independent Projects

For independent projects, PI and NPV produce **identical accept/reject decisions**:

- PI > 1 ⟺ NPV > 0 → Accept
- PI < 1 ⟺ NPV < 0 → Reject
- PI = 1 ⟺ NPV = 0 → Indifferent

This equivalence is mathematical, not coincidental: since PI = 1 + NPV/I₀ and the initial investment I₀ is positive, the sign of (PI − 1) always matches the sign of NPV.

## Where the Methods Diverge

The two methods **diverge when ranking mutually exclusive projects**, particularly when projects differ in scale (size of initial investment). PI normalizes NPV by investment size, which can favor smaller, higher-ratio projects over larger projects that contribute more absolute value to the firm.

**Example:**
- Project A: NPV = $100, Investment = $200 → PI = 1.50
- Project B: NPV = $150, Investment = $500 → PI = 1.30

PI ranks A higher; NPV ranks B higher. If only one can be chosen, NPV maximization (choosing B) is the correct criterion because it maximizes shareholder wealth in absolute terms.

## Practical Use and Limitations

The PI method is sometimes used when **capital is rationed** — i.e., when a firm cannot fund all positive-NPV projects. In that constrained setting, ranking projects by PI helps allocate a fixed budget to maximize total NPV per dollar invested. However, even in capital-rationing scenarios, PI-based rankings are only approximate and may fail with project indivisibilities.

As covered in MIT 15.401 Session 18, NPV remains the theoretically superior method. Alternatives like PI (or the payback period) persist in practice due to simplicity and ease of communication, but they should be understood as approximations or heuristics rather than replacements for NPV analysis.

## Summary

| Criterion | Independent Projects | Mutually Exclusive Projects |
|---|---|---|
| PI vs NPV agreement | Always identical | May diverge |
| Correct method | Either | NPV (absolute value) |
| PI useful when | Capital rationing | As a rough screen only |