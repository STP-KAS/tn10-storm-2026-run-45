> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. Written before any submit.

# Plan

Pre-run 44 answered the heavy lane at rate 920 with a 12,000 tKAS fee cap. The six minutes completed. The 80-block pause tripped twice, and each clear was the next probe sample. The template's heavy count stayed 1 while our class was present. This run does not repeat that knob.

The question here is competition. Tic-tac-toe carriers, covenant hops at 200 sompi per gram, and one KCC-20 mint line at 100 sompi per gram share the desk mempool. Then the heavy lane joins them. We want to see what still lands.

The guest binary prices each carrier at the node's priority fee estimate. It has no separate fee knob. A match during the congest phase is the superior-fee match: the estimate is whatever the node quotes then, and the match log records that quote. We do not recompile the guest.

## Setup, after this page is on origin, before the window

A read at 19:14:47Z, after pre-run 44, on the same desk node:

- The funding key usable value was 17,905 tKAS, under the 18,000 line the family sender's budget has used.
- A reserve key holds enough to move about 8,000 tKAS onto the funding key, in chunks that fit one transaction. The stop is usable at or above 25,000, or the reserve's movable coins running out.
- The guest issuer held 1 coin and 40 tKAS. The guest gate wants 2 to 4 issuer coins and at least 40 tKAS. The operator held 4 coins and 743.67 tKAS. Before the window, the issuer is brought up to 4 coins, each a top-up of 100 tKAS from the reserve, so the count stays inside the gate. During the window, if the issuer falls below 3 coins, the same top-up runs again, still from the reserve, still capped at 4 coins.
- The heavy pile held 198 coins and 2,383 tKAS at or above 10 tKAS, and 2,044 coins and 11,934 tKAS between 2 and 10 tKAS. Before the lane process starts, coins in that 2–10 band are joined into coins of 40 tKAS, up to 200 new coins. The lane process is not started until that join has finished.

None of that is the question. It is so the window is not cut by an empty wallet.

## Window

One controller. One desk node. The node is not restarted.

| Phase | Clock | What is on |
|---|---|---|
| BASE | 3 min | Probe only |
| QUIET | 12 min | Twelve covenant families at 200 sompi per gram, schedule rate 1.2, the same number pre-run 35 used. One KCC-20 mint line at 100, one mint at a time, accept cap 30. Tic-tac-toe matches, one at a time, on the existing image, until this phase and the next one end |
| CONGEST | 6 min | The same three lines stay on. The heavy lane comes on: one hundred chains, no ready cap, rate 920, fee cap 8,000 tKAS, pile floor 200. The pause at 90,000 mempool entries or 80 blocks of ready mass stays |
| RETURN | 3 min | All four off |

Launch paths are new: `launch::storm-2026-10-30-p45-f1` through `f12`, and `launch::storm-2026-10-30-p45-kcc1`. Pre-run 35's paths are not reused.

The guest line stops on its own stop file at RETURN. A match that fails the gate twice stops the guest line and the rest of the window still counts. The mint stops at 30 accepts or at RETURN. The lane stops on its fee cap, its moved cap of 10,000 tKAS, its pile floor, or RETURN, whichever the log says.

Disk abort under 150 GB free. A read under 160 GB does not start the window.

The count is the desk node's. The table is filled from the probe, the hop log, the mint log, the guest match log, and the lane log. A findings map in this repo, written at the close, says what landed in each phase.

While the lane is on, it slows other users' low-fee transactions on our node.
