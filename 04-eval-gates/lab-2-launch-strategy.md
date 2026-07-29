# Module 4 · Launch Strategy · Section 4.0 Release Criteria

_Generated from the M4 Launch Strategy Builder. Drop this into your PRD as Section 4.0._

## 4.0 Release Criteria

The following thresholds must be met by Model Candidate v1.x before approval for production deploy. Eval Specs from Module 3 define the measurement methodology.

| Severity | Metric | Threshold | Dataset | Method |
|---|---|---|---|---|
| 🔴 Hard (Blocker) | Pricing Hallucination rate | 0 % | `Ascend_IQ_Logs` | 03-eval-suites/lab-2-eval-spec.md |
| 🟡 Soft (Review) | Latency | < 1.0 sec | `Ascend_IQ_Logs` | _[Example Spec]_ |
| 🔵 Advisory (Monitor) | Tone Consistency | > 4 | `Ascend_IQ_Logs` | _[Example Spec]_ |

## 4.1 CI Gate Policy

These thresholds run in a GitHub Actions gate on every pull request, replaying deterministic fixtures from the regression golden set (≥ 30 cases). PM owns the policy; Engineering owns the YAML.

> enforces the deterministic checks like pricing at that moment and the thresholds like it should always equal to 0 %

## 4.2 Mitigation Plan · Soft Gate

**Selected Lever:** Staged Rollout

> If our Soft Gate fails (if soft gate fails, e.g latency hits >2 sec threshold, we recommend staged rollout to continuously keep on improving that metric for the better customer / user experience), we recommend **Staged Rollout** because customer experience for internal/ external user is an important factor for the product success,  so the latency as a metric should be improved with every stage of the process to make it better

---

_Lab artifact for Module 4, AI Evals Certification, Product School. Becomes the Eval Gates slide of the Final Project deck._
