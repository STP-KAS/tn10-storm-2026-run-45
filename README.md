> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is a pre-run. Pre-run 45.** It is not the Wednesday run. It is not the Tuesday run. It is not pre-run 1 to 44, and it does not edit their repos. A read does not start a runner.

# tn10-storm-2026-11-11-prerun-45

**Pre-run 45: tic-tac-toe matches, covenant hops, and one KCC-20 mint line, first on their own, then beside our heavy lane, on the desk node.** The neuron stays [tn10-storm-2026-11-11](https://github.com/STP-KAS/tn10-storm-2026-11-11). This repo does not edit that repo.

> **Our own testing.** This is our own Kaspa Testnet-10 testing, run on our own machines and nodes. What these pages report is what we observed in this run; it is not a claim of how TN10 or Kaspa behave in general.

| Field | Value |
|---|---|
| Target | A table of what landed, by phase: tic-tac-toe carriers, covenant hops, and KCC-20 mints, with the desk template and the desk fee estimate. Quiet first, then the heavy lane on, then everything off |
| The change | A new question after pre-run 44. The three lines run together. The heavy lane comes on only in the congest phase. The guest binary prices a carrier at the node's priority fee estimate. That estimate is logged per match. No recompile |
| Met or not met | **met** on the table. BASE 19:43–19:46Z: fee estimate 100 / 100 / 100. QUIET: eight hopping families, submit-OK 381–433 a full minute; mint 30 of 30, fees 1.2317 tKAS, ended 19:53:47Z on its cap; guest matches 1–21 confirmed 8 of 8, one quote 126.68. CONGEST: in the sixteen samples while our heavy class was present, the template's heavy count is 1 and storage mass is 266,682–310,994. Guest matches 26–30 confirmed 8 of 8 at quotes 1,505.14–1,559.99. Hops at 200 submitted 181 OK. The mint was already finished, so it was not beside the lane. The fee cap stopped the lane at 20:03:55Z on 8,001.53 tKAS. RETURN fee estimate is back near 100. The lane end line says pending 56. The probe samples after the stop are empty |
| Retry count | 0. The next attempt is a new repo. This one is not resumed |
| Core tags | — |
| Status | done. Closed from the probe, the lane log, the guest log and the family submit log |

Plan, lock, and the prediction are in [plan/PLAN.md](plan/PLAN.md), [locks/LOCKED.md](locks/LOCKED.md), and [plan/PREDICTIONS.md](plan/PREDICTIONS.md). Written before any submit.

While the heavy lane is on, it slows other users' low-fee transactions on our node. We say so here.

The minute table is [counts/chain/TEMPLATE.md](counts/chain/TEMPLATE.md). The phase map is [counts/FINDINGS-MAP.md](counts/FINDINGS-MAP.md). The lessons are [logs/LESSONS.md](logs/LESSONS.md).
