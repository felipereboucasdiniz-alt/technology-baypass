# Technology Bypass: Practical Playbook
## A Step-by-Step Guide for Executives and Policymakers

---

## How to Use This Playbook

This guide translates the Technology Bypass framework into actionable steps. Follow the four phases:

1. **DIAGNOSE** your coordination failure
2. **CALIBRATE** which technology channels to prioritize
3. **PILOT** with low-hanging fruit
4. **SCALE** strategically (accepting incompleteness)

Each section includes:
- ✅ **Checklist** (what to do)
- ⚠️ **Warning signs** (when to stop or pivot)
- 📊 **Metrics** (how to measure success)
- 💡 **Real examples** (how others did it)

---

## Phase 1: DIAGNOSE (2-3 months)

### Objective
Identify which type of coordination failure you're facing and quantify the cost.

---

### Step 1.1: Map the Strategic Interaction

**Question:** Why are people/organizations not doing what's socially optimal?

Use this decision tree:

```
START: Is there a socially beneficial outcome that isn't happening?
│
├─ NO → You don't have a coordination problem (stop here)
│
└─ YES → Continue
   │
   ├─ Q1: Would everyone be better off if everyone cooperated?
   │   └─ YES → Likely PRISONER'S DILEMMA
   │       └─ Q1a: Why don't they cooperate?
   │           ├─ "Each individual gains more by cheating" → Definitely PD
   │           └─ "They don't trust others to cooperate" → PD with coordination failure
   │
   ├─ Q2: Does one party gain only by harming another?
   │   └─ YES → Likely ZERO-SUM GAME
   │       └─ Q2a: Is total value destroyed?
   │           ├─ YES → Negative-sum (war, litigation)
   │           └─ NO → Pure zero-sum (redistribution)
   │
   └─ Q3: Do willing buyers and sellers exist but transactions don't happen?
       └─ YES → Likely FRICTION PROBLEM
           └─ Q3a: Why don't they transact?
               ├─ "Can't find each other" → Search friction
               ├─ "Don't trust each other" → Information asymmetry
               └─ "Too expensive to transact" → Transaction cost friction
```

---

### Step 1.2: Quantify the Baseline

**For Prisoner's Dilemmas:**

| Metric | How to Measure | Example |
|--------|----------------|---------|
| **Defection rate** | % of agents not cooperating | 85% of oil/gas facilities don't report methane leaks |
| **Cost of defection** | Annual social cost | $10B/year in procurement corruption (Ukraine pre-ProZorro) |
| **Temptation gap** | T − R (gain from cheating vs. cooperating) | Bribery wins $1M contract vs. honest bid wins $700K = $300K gap |

**For Zero-Sum Games:**

| Metric | How to Measure | Example |
|--------|----------------|---------|
| **Conflict frequency** | # of incidents per year | 50 terrorist attacks/year in region X |
| **Destruction** | Value destroyed (D_A + D_B) | $500B destroyed in Iraq War (direct costs) |
| **Miscalculation rate** | % of conflicts where one side overestimated P(victory) | ~80% of wars (Blainey's statistic) |

**For Friction Problems:**

| Metric | How to Measure | Example |
|--------|----------------|---------|
| **Transaction gap** | Potential trades − actual trades | 20M unfilled job vacancies + 10M unemployed = 10M missed matches |
| **Search cost** | Time × value of time | Average 4 weeks to fill a job × $50K/year salary = $3,800 per hire in search cost |
| **Market thickness** | Transactions / potential transactions | 30% of people with bank accounts can send instant payments (pre-Pix Brazil) |

---

### Step 1.3: Identify Heterogeneity (the θ distribution)

**Critical question:** Do all agents have the same cost of compliance, or is there a wide variance?

**How to test:**
1. Segment agents by size, location, resources, ideology
2. Estimate compliance cost for each segment
3. Plot the distribution

**Example: Methane Monitoring**

| Segment | % of Facilities | % of Emissions | Cost to Monitor (per facility) | θ (relative cost) |
|---------|----------------|----------------|-------------------------------|-------------------|
| Large industrial (>500 kg/h) | 5% | 70% | $10K/year | Low (θ = 0.2) |
| Medium (100-500 kg/h) | 15% | 25% | $50K/year | Medium (θ = 0.5) |
| Small (<100 kg/h) | 80% | 5% | $200K/year (need denser satellites) | High (θ = 5.0) |

**Implication:**
- Targeting top 5% captures 70% of benefit at 20% of cost of full coverage
- Last 80% (small emitters) is economically wasteful to monitor
- **Strategic abandonment** is optimal

---

### Step 1.4: Estimate Current Technology Levels

Rate your status quo on each channel (scale 0-1):

| Channel | 0 (None) | 0.5 (Moderate) | 1.0 (Perfect) | Your Score |
|---------|----------|----------------|---------------|------------|
| **t_p (Monitoring)** | No detection | Spot checks, ~50% detection | Real-time, near-perfect | |
| **t_s (Sanctions)** | No enforcement | Penalties after years of litigation | Instant, automatic | |
| **t_c (Cost)** | Compliance is prohibitively expensive | Moderate cost | Near-zero cost | |
| **t_k (Network)** | No network effects | Some benefits to participation | Massive lock-in | |
| **t_h (Resilience)** | Single point of failure | Moderate redundancy | Antifragile | |

**Example: Ukraine Procurement (pre-ProZorro)**
- t_p = 0.1 (paper records, rarely audited)
- t_s = 0.05 (convictions take 5+ years)
- t_c = 0.4 (electronic submission possible but not required)
- t_k = 0 (no network benefits to honest bidding)
- t_h = N/A (not applicable to corruption)

---

### ✅ Deliverable from Phase 1

A one-page business case with:

1. **Problem type** (Prisoner's Dilemma / Zero-Sum / Friction)
2. **Baseline metrics** (defection rate, conflict frequency, transaction gap)
3. **Annual cost** (social welfare loss from failure)
4. **Heterogeneity assessment** (θ distribution, can we target high-value segments?)
5. **Current technology vector** (t_p, t_s, t_c, t_k, t_h scores)

**Example:**

> **Problem:** Procurement corruption (Prisoner's Dilemma)
> **Cost:** $10B/year lost to inflated bids
> **Defection rate:** 85% of contracts involve some form of bribery
> **Heterogeneity:** Low (most suppliers face similar temptation)
> **Current tech:** t_p=0.1, t_s=0.05, t_c=0.4, t_k=0
> **Opportunity:** If we raise t_p to 0.9, model predicts defection falls to <10%

---

## Phase 2: CALIBRATE (1-2 months)

### Objective
Determine which technology channel(s) have the highest return on investment in your context.

---

### Step 2.1: Run Sensitivity Analysis

**The Question:** If I increase t_j by 10%, how much does social welfare improve?

**Elasticity formula:**
```
ε_j = (∂W/∂t_j) × (t_j / W)
```

Where:
- W = social welfare (baseline value − cost of failure)
- ∂W/∂t_j = marginal welfare gain from increasing channel j

**How to estimate (practical approach):**

1. **For Prisoner's Dilemmas:**
   - Elasticity of t_p (monitoring): typically 0.3 to 0.5 (high leverage)
   - Elasticity of t_s (sanctions): typically 0.2 to 0.4 (moderate)
   - Elasticity of t_c (cost): typically 0.1 to 0.2 (low, unless costs are currently prohibitive)

   **Rule of thumb:** Invest in t_p first (monitoring), then t_s (sanctions), then t_c (cost reduction)

2. **For Zero-Sum Games:**
   - Elasticity of t_k (trade/network): typically 0.4 to 0.6 (very high—creates positive-sum alternative)
   - Elasticity of t_h (resilience): typically 0.3 to 0.5 (high—reduces attack payoff)
   - Elasticity of t_p (transparency): typically 0.2 to 0.3 (moderate—reduces miscalculation)

   **Rule of thumb:** Invest in t_k (create trade gains) and t_h (reduce vulnerability) before t_p

3. **For Friction Problems:**
   - Elasticity of t_c (cost reduction): typically 0.5 to 0.8 (very high—direct impact on transaction volume)
   - Elasticity of t_k (network): typically 0.4 to 0.7 (very high—creates liquidity spiral)

   **Rule of thumb:** Invest in t_c and t_k together (they multiply each other)

---

### Step 2.2: Identify Complementarities

**The Question:** Which pairs of technology channels multiply each other's effectiveness?

**Key complementarities:**

| If you invest in... | Also invest in... | Why |
|-------------------|------------------|-----|
| **t_p (monitoring)** | **t_s (sanctions)** | No point detecting if you can't punish; no point punishing if you can't detect |
| **t_c (cost reduction)** | **t_k (network effects)** | Lower costs → more adoption → network effects kick in faster |
| **t_k (network/trade)** | **t_h (resilience)** | Larger network creates more value to protect; resilience makes network more stable |
| **t_p (information)** | **t_k (network)** | Better info → more trust → more participation → network growth |

**Practical test:**
Use the multiplier formula from the framework:
```
ΔWelfare ∝ t_p × t_s × (1 − t_c) × t_k × t_h
```

**Example calculation (simplified):**

| Scenario | t_p | t_s | (1 − t_c) | t_k | t_h | Product | Welfare Gain |
|----------|-----|-----|-----------|-----|-----|---------|--------------|
| **Baseline** | 0.2 | 0.1 | 0.7 | 0.1 | 0.5 | 0.0007 | Baseline |
| **Option A: Boost t_p only** | 0.8 | 0.1 | 0.7 | 0.1 | 0.5 | 0.0028 | 4× improvement |
| **Option B: Boost t_p + t_s** | 0.8 | 0.5 | 0.7 | 0.1 | 0.5 | 0.014 | 20× improvement |
| **Option C: Boost all (balanced)** | 0.5 | 0.5 | 0.4 | 0.4 | 0.7 | 0.028 | 40× improvement |

**Lesson:** Balanced investment (Option C) outperforms lopsided focus, even if baseline levels are lower, due to complementarities.

---

### Step 2.3: Calculate Break-Even Adoption

**The Question:** What % of agents need to adopt before benefits exceed costs?

**For network effect technologies (t_k):**
- Typical tipping point: **40-60% adoption**
- Before tipping point: Value grows linearly (slow)
- After tipping point: Value grows exponentially (fast)

**Formula:**
```
Break-even when: N × V(N) = κ × N + F

Where:
- N = number of adopters
- V(N) = value per user (function of network size)
- κ = marginal cost per user
- F = fixed cost
```

**Example: Pix (Brazil)**
- Fixed cost F = $100M (infrastructure)
- Marginal cost κ ≈ $0 (digital, near-zero)
- Value per user V(N) = $50 + $2×(N/1M) (base value + network effect)
- Break-even at N* ≈ 2M users (1% of population)
- **Actual adoption:** 76% (160M users) in 3 years → far beyond break-even

**Implication:**
If you can reach break-even with <20% of potential users, network effects will carry you the rest of the way. If break-even requires >80%, you'll struggle (need subsidies or mandates).

---

### Step 2.4: War-Game the Failure Modes

**Question:** Which of the three failure modes is most likely to kill your intervention?

| Failure Mode | Diagnostic Test | Risk Level (High/Med/Low) |
|--------------|-----------------|---------------------------|
| **Heterogeneity (high-θ)** | Does the top 20% of agents account for >70% of the problem? | If NO → High risk |
| **Transition costs (κ)** | Are upfront costs <30% of first-year benefits? | If NO → High risk |
| **Arms race (t^A vs t^D)** | Can adversaries deploy counter-tech faster than you can adapt? | If YES → High risk |

**Example: Methane Monitoring**
- Heterogeneity: LOW RISK (top 20% = 70% of emissions, can focus there)
- Transition costs: LOW RISK (satellites already exist, marginal cost to add monitoring is <10% of expected revenue from methane fees)
- Arms race: LOW RISK (emitters can't "hide" methane from satellites using affordable tech)
- **Overall:** GREEN LIGHT

**Example: Kenya IFMIS Procurement**
- Heterogeneity: MEDIUM RISK (corruption networks vary by region/sector)
- Transition costs: HIGH RISK (vested interests lose immediately, benefits accrue over 5+ years)
- Arms race: MEDIUM RISK (corrupt suppliers can collude to input false data)
- **Overall:** YELLOW LIGHT (proceed with caution, need political coalition)

---

### ✅ Deliverable from Phase 2

A technology investment plan with:

1. **Priority channels** (ranked by elasticity)
2. **Complementarity map** (which pairs of t_j to co-invest in)
3. **Break-even analysis** (adoption threshold for network effects)
4. **Risk assessment** (which failure mode is most likely)
5. **Budget allocation** (% of investment to each channel)

**Example:**

> **Priority:** t_p (monitoring) + t_s (sanctions) — highest elasticity and strong complementarity
> **Investment split:** 60% on t_p (satellite network), 30% on t_s (legal framework for auto-fines), 10% on t_c (subsidize detection equipment)
> **Break-even:** Need 15% of large emitters to participate for ROI >1
> **Main risk:** Transition costs (regulatory approval may take 2+ years)
> **Mitigation:** Start with voluntary pilot in 3 countries, use success to lobby for mandates

---

## Phase 3: PILOT (6-12 months)

### Objective
Test the technology bypass with a small, high-value segment (low-θ agents) and measure behavioral change.

---

### Step 3.1: Select the Pilot Segment

**Rule:** Start with agents who have the **lowest cost of compliance** and the **highest baseline defection rate** (biggest opportunity for improvement).

**Criteria for good pilot targets:**

| Criterion | Why it matters | How to measure |
|-----------|----------------|----------------|
| **Low θ (low compliance cost)** | Easy wins build momentum | Segment by size, location, resources—pick the segment where your technology is cheapest to deploy |
| **High baseline defection** | Large room for improvement | Pick segment where >60% currently defect/don't transact |
| **High visibility** | Success stories matter for scaling | Pick segment that peers pay attention to (e.g., tier-1 suppliers, major cities) |
| **Measurable** | Need clear before/after metrics | Pick segment where you can track behavior (e.g., transaction data, sensor data) |

**Example: Walmart Food Trust Blockchain**
- **Target:** Suppliers of leafy greens (romaine, spinach)
- **Why:** Recent E. coli outbreak made them high-priority (high visibility); they're mostly large farms (low θ); traceability was terrible (high defection)
- **Size:** 100 suppliers accounting for $1B in sales
- **Metric:** Trace time (7 days → target <1 hour)

---

### Step 3.2: Deploy Minimum Viable Technology Bypass

**Don't build the perfect system.** Deploy the simplest version that tests your core hypothesis.

**For Prisoner's Dilemmas:**
- **Minimum t_p:** Basic monitoring (doesn't need to be 99%, start with 70%)
- **Minimum t_s:** Clear sanctions (can be manual at first, automate later)
- **Skip t_c and t_k initially** (unless they're your priority channels)

**For Zero-Sum Games:**
- **Minimum t_k:** Facilitate a few high-value trades (proof that cooperation beats conflict)
- **Minimum t_h:** Harden a few critical nodes (show that attacks are less effective)

**For Friction Problems:**
- **Minimum t_c:** Reduce transaction cost for a single high-volume use case
- **Minimum t_k:** Seed the network with early adopters (subsidize if necessary)

**Example: Pix (Brazil) Pilot (2020)**
- Launched with just 8 participating banks (not all 700+ financial institutions)
- Focused on P2P transfers only (no merchant payments initially)
- Zero fees to kickstart adoption (t_c and t_k focus)
- **Result:** 1M users in first week → fast iteration based on feedback

---

### Step 3.3: Measure Behavioral Change

**The critical question:** Did defection/conflict/friction actually decrease, or did you just build cool technology?

**Key metrics by problem type:**

| Problem Type | Leading Indicator | Lagging Indicator |
|--------------|-------------------|-------------------|
| **Prisoner's Dilemma** | % of agents monitored (t_p coverage) | Defection rate (before vs. after) |
| **Zero-Sum Game** | # of peaceful transactions facilitated (t_k) | Conflict incidents (before vs. after) |
| **Friction Problem** | Transaction cost (before vs. after) | Transaction volume (before vs. after) |

**Statistical rigor:**
- Use a control group if possible (e.g., pilot in 3 regions, compare to 3 similar regions without intervention)
- Run before/after comparison with sufficient sample size
- Account for confounders (e.g., if defection falls, is it due to your tech or to unrelated regulatory changes?)

**Example: ProZorro (Ukraine) Pilot Metrics**

| Metric | Before ProZorro | After ProZorro (Year 1) | Change |
|--------|----------------|------------------------|--------|
| **t_p (transparency)** | <10% of bids audited | 100% of bids publicly visible | 10× increase |
| **Bid prices** | 15-30% above market | 5-10% above market | 50-67% reduction in overpayment |
| **Supplier diversity** | Avg 2.3 bids per tender | Avg 4.8 bids per tender | 2× increase in competition |
| **Estimated savings** | N/A | $1.9B over 2 years | High ROI |

---

### Step 3.4: Refine Cost Estimates

**Reality check:** Was the implementation cost close to your projection, or wildly off?

**Common cost surprises:**

| Cost Category | Initial Estimate | Actual Cost (Typical) | Why the Gap? |
|---------------|-----------------|----------------------|--------------|
| **Technology** | $X | 0.8X to 1.2X | Usually close if you scoped well |
| **Change management** | 0.1X | 0.5X to 2X | People resist, training takes time |
| **Political/coalition-building** | 0.05X | 0.3X to 5X | Vested interests fight back |
| **Legal/regulatory** | 0.1X | 0.2X to 3X | Compliance, lobbying, delays |

**Example: Kenya IFMIS vs. Ukraine ProZorro**

| System | Tech Cost | Total Cost (incl. political) | Ratio |
|--------|-----------|------------------------------|-------|
| **ProZorro** | $5M | ~$15M (civil society + govt buy-in) | 3:1 |
| **Kenya IFMIS** | $50M | $200M+ (resistance, sabotage, restarts) | 4:1+ |

**Lesson:** Budget 2-5× your pure technology cost for change management and coalition-building.

---

### ✅ Deliverable from Phase 3

A pilot report with:

1. **Before/after metrics** (defection rate, conflict rate, transaction volume)
2. **Statistical significance** (p-values, confidence intervals)
3. **Refined cost estimates** (actual vs. projected)
4. **User feedback** (qualitative insights)
5. **Go/No-Go decision** (scale, pivot, or kill)

**Decision criteria:**
- **GO (scale):** >30% improvement in key metric, costs within 2× projection, positive user feedback
- **PIVOT:** Some improvement but not enough; try different technology channel or segment
- **KILL:** No improvement, or costs spiraling beyond ROI; cut your losses

---

## Phase 4: SCALE (12-24 months)

### Objective
Expand to broader population, manage heterogeneity strategically, and reach self-sustaining network effects (if applicable).

---

### Step 4.1: Sequence Expansion (Low-θ to High-θ)

**Don't try to onboard everyone at once.** Move from easy segments to hard segments.

**Expansion sequence:**

1. **Wave 1 (Months 1-3):** Low-θ agents who were in the pilot (they're already convinced)
2. **Wave 2 (Months 4-6):** Low-θ agents who are peers of pilot participants (social proof)
3. **Wave 3 (Months 7-12):** Medium-θ agents (may need subsidies or mandates)
4. **Wave 4 (Months 13-24):** High-θ agents (only if benefits justify costs; often strategic abandonment is optimal)

**Example: Walmart Food Trust Blockchain**

| Wave | Segment | Size | Compliance Cost | Strategy |
|------|---------|------|----------------|----------|
| 1 | Tier-1 leafy greens suppliers | 100 | Low (large farms, existing IT) | Mandatory (pilot) |
| 2 | All fresh produce suppliers | 500 | Low-medium | Mandatory by Sept 2019 |
| 3 | Tier-1 suppliers in other categories | 2,000 | Medium (diverse IT capabilities) | Phased mandates 2020-2021 |
| 4 | Tier-2 and tier-3 suppliers | 50,000+ | High (small farms, no IT) | Strategic abandonment (not required; Walmart provides subsidized mobile apps for those who opt in) |

**Result:** 80% of supply chain value tracked on blockchain by 2023; last 20% (micro-suppliers) remain on traditional systems (optimal trade-off).

---

### Step 4.2: Monitor Network Effects Threshold

**For technologies with t_k (network effects), watch for the tipping point.**

**Signs you've crossed the threshold:**

1. **Adoption accelerates** (exponential curve, not linear)
2. **Organic growth** (new users joining without marketing spend)
3. **Lock-in** (users can't leave because everyone else is on the platform)

**Example: Pix (Brazil)**

| Quarter | Active Users (M) | Growth Rate (QoQ) | Network Effect Stage |
|---------|-----------------|-------------------|----------------------|
| Q4 2020 | 10 | N/A (launch) | Seeding |
| Q1 2021 | 25 | 150% | Early growth |
| Q2 2021 | 50 | 100% | Approaching tipping point |
| Q3 2021 | 90 | 80% | Tipping point (40% of population) |
| Q4 2021 | 120 | 33% | Post-tipping (slowing % growth but high absolute) |
| Q4 2024 | 160 | ~5% (mature) | Saturated (76% of population) |

**Tipping point:** ~Q3 2021 when adoption hit 40% of population. After that, growth became self-sustaining.

**Implication:**
Once you hit the tipping point (typically 40-60% for payment/communication networks), you can:
- Reduce marketing spend (organic growth takes over)
- Start charging fees (lock-in means users won't leave)
- Focus on adding features rather than acquiring users

---

### Step 4.3: Implement Strategic Abandonment

**Accept that 100% coverage is rarely optimal.**

**The math:**
```
Optimal coverage N* where:
Marginal Cost(N*) = Marginal Benefit(N*)

If MC curve is steeply rising (high-θ agents are very costly) and MB curve is flat or declining (you've already captured the high-value agents), then N* < 100%.
```

**Practical decision rule:**

| If... | Then... | Example |
|-------|---------|---------|
| Top 20% of agents account for >70% of the problem | Focus exclusively on top 20%; exempt the rest | Methane: top 5% of emitters = 70% of emissions |
| Marginal cost of next segment >3× previous segment | Stop expansion; declare current coverage "good enough" | Walmart: tier-3 suppliers cost 5× more to onboard than tier-1 |
| You've hit network effect saturation (>70% adoption) | Shift from user acquisition to feature development | Pix: at 76% adoption, focus on cross-border, merchant tools |

**Example: Global Methane Monitoring Strategy**

| Segment | % of Emitters | % of Emissions | Monitoring Cost per Tonne | Coverage Decision |
|---------|--------------|----------------|---------------------------|-------------------|
| Large industrial | 5% | 70% | $5/tonne | **100% coverage** (mandate satellite monitoring) |
| Medium facilities | 15% | 25% | $20/tonne | **50% coverage** (random audits + self-reporting with verification) |
| Small/artisanal | 80% | 5% | $200/tonne | **0% coverage** (strategic abandonment; not cost-effective) |

**Result:** 95% of emissions covered at 20% of the cost of 100% coverage (optimal trade-off).

---

### Step 4.4: Plan for Arms Race Dynamics

**If your adversaries are adaptive, expect them to deploy counter-technologies.**

**Defensive strategies:**

1. **Focus on t_h (resilience):** Attackers can't bypass your redundancy; it's structurally defensive
2. **Exploit t_k (network effects):** Once you have lock-in, attackers can't dislodge you
3. **Cost compression in legal alternatives (t_c):** Make crime/defection economically uncompetitive (they can't "arms race" against cheaper legitimate options)

**Example: Financial Regulation (Blockchain Transparency vs. Privacy Coins)**

| Technology Arms Race | Regulator's Move (t^D) | Criminal's Counter (t^A) | Next Regulator Response |
|---------------------|------------------------|--------------------------|-------------------------|
| **Round 1** | Mandate blockchain KYC (t_p ↑) | Switch to Monero/privacy coins (t_p ↓) | Ban privacy coins on regulated exchanges |
| **Round 2** | Forensic blockchain analysis (t_p ↑) | Use mixing services (t_p ↓) | Regulate mixing services |
| **Round 3** | Focus on fiat on-ramps (t_s ↑) | P2P cash exchanges (t_s ↓) | Make legal crypto cheaper/easier than illegal (t_c ↓ for legal, t_c ↑ for illegal) |

**Lesson:** Pure monitoring/sanctions (t_p, t_s) leads to arms race. Break the cycle by making legal activity so cheap and convenient (t_c, t_k) that crime becomes economically irrational.

---

### ✅ Deliverable from Phase 4

Full deployment with:

1. **Adoption metrics** (by segment, over time)
2. **Network effect analysis** (when did you hit tipping point?)
3. **Strategic abandonment rationale** (which segments you exempted and why)
4. **ROI documentation** (actual costs and benefits)
5. **Lessons learned** (what would you do differently?)

**Example final report (Pix):**

> **Adoption:** 76% of Brazilians (160M users) in 3 years
> **Tipping point:** Q3 2021 (40% adoption)
> **Strategic abandonment:** Did not mandate coverage for small rural cooperatives (high θ); waited for infrastructure to improve organically
> **ROI:** $100M investment → projected R$280B GDP boost by 2028 (2,800:1 ratio)
> **Key lessons:**
> 1. Zero fees (t_c) + bank mandates (t_k) = rocket fuel for adoption
> 2. Network effects kicked in faster than projected (40% vs. expected 50-60%)
> 3. Biggest surprise: Peer-to-peer use cases (friends splitting bills) drove initial adoption, not merchant payments

---

## Summary: The Complete Playbook at a Glance

| Phase | Duration | Key Question | Main Output | Success Metric |
|-------|----------|--------------|-------------|----------------|
| **1. Diagnose** | 2-3 months | What type of coordination failure? | Business case with baseline metrics | Clear problem type + quantified cost |
| **2. Calibrate** | 1-2 months | Which technology channels to prioritize? | Investment plan with elasticity analysis | ROI projection >3:1 |
| **3. Pilot** | 6-12 months | Does the technology actually change behavior? | Before/after metrics + refined costs | >30% improvement in key metric |
| **4. Scale** | 12-24 months | How to reach optimal coverage? | Full deployment with adoption curves | Target coverage reached; network effects (if applicable) self-sustaining |

---

## Appendix: Quick Reference Tables

### Table A: Problem Type Diagnostic

| Symptom | Problem Type | Priority Channels |
|---------|--------------|-------------------|
| Everyone could cooperate but doesn't (defection dominant) | Prisoner's Dilemma | t_p, t_s |
| Conflict/war despite cheaper peaceful alternatives | Zero-Sum | t_k, t_h, t_p |
| Willing buyers + sellers, but no transactions | Friction | t_c, t_k |
| Some cooperate, some don't (mixed equilibrium) | Coordination game | t_p (information), t_k (standards) |

---

### Table B: Technology Channel Selection by Context

| If your main challenge is... | Prioritize... | Example technology |
|----------------------------|---------------|-------------------|
| Detecting bad behavior | t_p (monitoring) | Satellites, blockchain audit trails, AI fraud detection |
| Making sanctions credible | t_s (automated penalties) | Smart contracts, instant disqualification, escrow |
| Compliance is too expensive | t_c (cost reduction) | Modular devices, mobile apps, zero-fee platforms |
| Not enough participants | t_k (network effects) | Open APIs, interoperability, zero fees, mandates |
| Attacks are too damaging | t_h (resilience) | Redundancy, decentralization, rapid recovery |

---

### Table C: Common Failure Modes and Fixes

| Failure Mode | Warning Sign | Fix |
|--------------|--------------|-----|
| **Heterogeneity** | Wide variance in compliance costs; long tail of high-θ agents | Segment and target low-θ first; accept strategic abandonment |
| **Transition costs** | Upfront investment >3× first-year benefits; long payback period | Phase rollout; secure multi-year funding; get quick wins |
| **Arms race** | Adversaries are well-resourced and adaptive | Focus on defensive tech (t_h, t_k); make legal options cheaper (t_c) |
| **Governance capture** | Incumbents control standards/regulation | Build coalitions; demonstrate pilot success; regulatory arbitrage |
| **User resistance** | Surveys show distrust or privacy concerns | Transparency about data use; opt-in initially; credible commitment not to abuse |

---

### Table D: Benchmarking Your ROI

Use this table to calibrate expectations:

| Problem Type | Typical Pilot ROI | Typical Full-Scale ROI | Payback Period |
|--------------|------------------|----------------------|----------------|
| **Prisoner's Dilemma (corruption)** | 5:1 to 20:1 | 50:1 to 500:1 | 1-3 years |
| **Zero-Sum (conflict prevention)** | Hard to measure (lives saved) | 10:1 to 100:1 (if war avoided) | 5-10 years (long horizon) |
| **Friction (market-making)** | 2:1 to 10:1 | 20:1 to 200:1 | 6 months to 2 years |

**Note:** These are rough benchmarks from literature and cases like ProZorro, Walmart Food Trust, Pix. Your context will vary.

---

**End of Practical Playbook**
