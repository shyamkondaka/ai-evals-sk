# Ship/Hold Memo · Ascend IQ

> **Decision:** 🛑 HOLD

**To:** [CPO] · cc Eng Lead · Trust & Safety  
**From:** [Shyam K] · AI Evals Cohort · [07-30-2026]

## The Answer

I recommend we Hold as  hard gates are failing pre-launch (pricing hallucination, spec-contradicting hallucination), the trajectory eval verdict is itself HOLD at 0/6, and judge calibration (κ = –0.32) means we cannot yet trust our own quality signal. Shipping now risks handing a VP-level buyer a wrong number — the one failure this client base won’t forgive.

## The Arguments

### 1. Hallucination risk on financial summaries is contained but not eliminated.

Our P0 risk, fabricated financial figures in monthly enterprise summaries, was the most critical failure mode surfaced in our Module 2 audit. After the M3 eval suite + M4 hard-gate, the failure rate dropped from 9.2% to 2.1%. This is below our gate threshold of 3%, but above the 1% "zero-incident" bar enterprise leadership has signaled.

### 2. Bias remains a P1 we're explicitly accepting under a 30-day audit window.

Our Coverage Matrix from M5 shows the regional bias eval has 78% coverage, short of our 90% bar. The Eval Playbook mandates a 30-day post-launch audit with Trust & Safety as the escalation owner. We've sized this risk: any variance above 2% halts new enrollments until a fix lands.

### 3. Revenue exposure compounds if we hold for the perfect launch.

Three enterprise accounts ($4.2M ARR) have flagged Ascend IQ as a non-negotiable contract requirement for Q3 renewal. Holding for another sprint risks losing them to a rival who has publicly marketed a less-rigorous but shippable competitor. The trust debt we accept here is smaller than the revenue debt of inaction.

## Evidence · Trust Metrics

```
- Hallucination rate: 35% (Gate: < 3%) ✓ FAIL · Source: raw audit logs, n=20
- Trajectory path is not right
```

## Business Risk

SHIP path: Fix the pricing hallucinations and spec contradictions and make sure the trajecotory path is correct, not just the outcome
HOLD path: 3 enterprise contracts (~$4.2M ARR) at high churn risk in Q3; competitive window closes in 8 weeks.

## Next Step · Decision Needed

Decision needed by EOD Friday. If approved, we ship to canary on Monday with the 30-day bias audit committed. Trust & Safety reviews the audit results in the Sept 30 QBR with go/halt authority on continued enrollment.

## Reflection

_Defining "good enough" for hallucination was the hardest part, without the M1 Strategy Canvas and M2 severity ranking, our M4 gate would have been an arbitrary number. The discipline forced trade-offs the team had been silently disagreeing about for weeks._
