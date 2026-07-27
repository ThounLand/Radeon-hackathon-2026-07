# Benchmark results

Raw output of `scripts/benchmark.py`, reproducible with the commands in the
main README, section 5. Each file lists the 20 cases, their stability verdict,
their correctness score and per-case timings.

| File | Mode | Date | Hardware |
|---|---|---|---|
| `bench-local-sequentiel.json` | sequential | 2026-07-27 | 2x Radeon AI PRO R9700 (gfx1201), ROCm 7.2.4, TP=2 |
| `bench-local-parallele.json` | 6 concurrent | 2026-07-27 | same |

Both runs: **100% correctness, 20/20 cases perfect.** Sequential 2m52,
6 concurrent 0m42 — a 4.1x speed-up with no cross-session leakage.

Stability verdicts differ between runs (17/20 vs 19/20 identical). This is
expected and documented: form varies, correctness does not.
