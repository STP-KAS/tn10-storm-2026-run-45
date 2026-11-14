> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value. Counts only. What we observed in this run.

# Findings map, pre-run 45

One desk node. The clock is the controller: BASE 19:43:00Z–19:46:00Z, QUIET 19:46:00Z–19:58:00Z, CONGEST 19:58:00Z–20:04:00Z, RETURN 20:04:00Z–20:07:00Z. Run end is 20:07:00Z. The desk node was not restarted. The minute cells are [chain/TEMPLATE.md](chain/TEMPLATE.md). This page is the other three lines, the lane, and where the two clocks disagree.

| Phase | What the logs say |
|---|---|
| BASE | Probe only. Fee estimate 100 / 100 / 100. The mempool was not empty. At 19:43:31Z the template heavy count is 2, storage mass 460,297, classed other, our class 0 |
| QUIET | Families 1–5 and 10–13 included. Families 6–9 dropped, reason no_funding, and were not retried. Eight families hopped at 200. Submit-OK 4,827, rejects 1,957. Mint 30 of 30, fees 1.2317 tKAS, ended 19:53:47Z on the cap. Guest matches 1–21 confirmed 8 of 8 on the desk. One quote was 126.68. The others in this phase were 100 |
| CONGEST | Lane on at 19:58:02Z, 476 coins, 13,036 tKAS, rate 920, fee cap 8,000. Submit-OK 3,259, 0 rejects, fees 8,001.53 tKAS. Two holds, about 21 s and about 20 s. While our class was present the template heavy count stayed 1. Hops submitted 181 OK and 3,243 rejects. Guest matches 22–31. The mint was already finished |
| RETURN | Stop at 20:04:00Z. Guest stopped at 20:04:02Z. Families stopped. Lane end line pending 56. Probe samples after the stop are at fee 100 and our class 0 |

## Genesis

Included: families 1, 2, 3, 4, 5, 10, 11, 12 and 13. Nine. Dropped at 19:46:04Z: families 6, 7, 8 and 9, each reason no_funding. The fee split line reads floor 1–12 at 200 and family 13 at 100, one builder, desk. The start line after the drops reads families 9, rate 1.2. That 9 is the eight hopping families plus the mint family. The coordinator did not retry a dropped family in this window.

## Covenant hops

Submit rows 10,208. Submit-OK 5,008. Rejects 5,200. The reason field is already_spent on 3,928 and orphan on 1,272.

| Phase | Submit-OK | Rejects | already_spent | orphan |
|---|---:|---:|---:|---:|
| QUIET | 4,827 | 1,957 | 750 | 1,207 |
| CONGEST | 181 | 3,243 | 3,178 | 65 |
| RETURN | 0 | 0 | 0 | 0 |

Full quiet minutes attempted 568 or 576 times. 576 is eight families at 1.2 per second for 60 seconds. The 19:46 minute is short because genesis finished at 19:46:06Z: 381 OK and 131 rejects. Landing in the full quiet minutes is 381 to 433 submit-OK. In congest the attempts stayed at 568 or 576, and landing fell to 14, 4, 86, 5, 71 and 1 submit-OK. No family ran away.

| Family | Submit-OK | Rejects |
|---|---:|---:|
| 1 | 648 | 628 |
| 2 | 624 | 652 |
| 3 | 625 | 651 |
| 4 | 630 | 646 |
| 5 | 630 | 646 |
| 10 | 618 | 658 |
| 11 | 620 | 656 |
| 12 | 613 | 663 |

Accept rows in the hop log: 5,030, all with an accept time, all source coord, 5,030 distinct ids. By accept time: QUIET 4,849, CONGEST 181, RETURN 0. Congest accepts match congest submit-OK at 181. Quiet does not match. Of the 5,030 accept ids and the 5,008 submit-OK ids, 5,000 are in both logs. 30 accept ids, all quiet, have no submit row. 8 submit-OK ids, all congest, have no accept row. We do not explain those 30 or those 8. Both counts are the logs.

As arithmetic from these lines, eight families at 1.2 per second is 9.6 attempts a second. Quiet submit-OK of 4,446 across the eleven full minutes 19:47Z through 19:57Z is about 6.7 a second. That is context for this log. It is not a rate finding.

## KCC-20 mint

Family 13. Cap 30. Gap 15,000 ms. Rate 100. Coins on the line at the start: 55. Accepted n=1 at 19:46:07Z through n=30 at 19:53:47Z. End line: accepted 30, tries 30, rejects 0, timeouts 0, fees 1.2317 tKAS, why cap. The mint finished in quiet, about four minutes before the lane. Congest did not measure this mint beside the lane.

## Tic-tac-toe

Aimed 120. Played 31. Submit-OK 225. Ids logged 229. Accepted on the desk 224. Gate fails 0. First error empty. Stopped 20:04:02Z. The four logged ids that are not in the submit-OK count are match 31, which logged 4 and submitted 0. The one submitted id that is not in the accepted count is match 22, which submitted 7 and was accepted 6.

The carrier fee is the node's priority estimate, logged per match. Issuer coins on the confirm lines stayed at 4. The first refill line reads operator 743.67 tKAS. The last refill line reads operator 683.20 tKAS. The 31 refill lines sent 30 coins and their fee fields sum to 49.98 tKAS. The first and the last of those lines both read issuer 4 coins and 340 tKAS. We do not add the refill fees to the lane fees.

| Match | Confirm (UTC) | Submit-OK | Ids logged | Accepted on desk | Priority quote |
|---|---|---:|---:|---:|---:|
| 1–15 | 19:46:35Z through 19:54:17Z | 8 | 8 | 8 | 100 |
| 16 | 19:54:50Z | 8 | 8 | 8 | 126.68 |
| 17–21 | 19:55:23Z through 19:57:33Z | 8 | 8 | 8 | 100 |
| 22 | 19:59:38Z | 7 | 7 | 6 | 100 |
| 23 | 19:59:57Z | 0 | 0 | 0 | 1,526.08 |
| 24 | 20:00:30Z | 8 | 8 | 8 | 100 |
| 25 | 20:00:53Z | 2 | 2 | 2 | 1,490.49 |
| 26 | 20:01:26Z | 8 | 8 | 8 | 1,520.34 |
| 27 | 20:01:59Z | 8 | 8 | 8 | 1,559.99 |
| 28 | 20:02:33Z | 8 | 8 | 8 | 1,555.31 |
| 29 | 20:03:06Z | 8 | 8 | 8 | 1,505.14 |
| 30 | 20:03:39Z | 8 | 8 | 8 | 1,544.44 |
| 31 | 20:04:01Z | 0 | 4 | 0 | 1,586.08 |

Matches 1–21 are quiet, including match 21 at 19:57:33Z. The lane starts at 19:58:02Z. Match 22's logged quote is 100. The probe during that match, from 19:58:11Z, is already at 1,400.22 and above. We report both. Match 23's logged quote is 1,526.08, the same figure as the probe sample at 19:59:53Z. The guest log at 19:59:54Z says init config was not submitted: output already spent by a transaction in the mempool. No carriers were logged. Gate fails stayed 0. Match 24's logged quote is 100. The probe at 20:00:13Z, inside that match's window, is fee 100 on mempool size 0. The probe at 20:00:33Z, three seconds after the confirm, is 1,470.15. We report both. Match 25 logged 1,490.49 and accepted 2 of 8. The guest log at 20:00:51Z says deposit of player B was not submitted, same already-spent text. Match 22's miss, at 19:58:04Z, is withdraw winnings, same already-spent text. Matches 26–30 confirmed 8 of 8 at quotes 1,505.14 to 1,559.99, including match 28 during the second hold. Match 31 was cut by the return stop.

## Lane, beside those lines

Start 19:58:02Z. Pause at 19:59:53Z on mempool size 5,300 and ready mass 86.68, clear at 20:00:14Z on mempool size 0. Pause at 20:02:15Z on mempool size 5,773 and ready mass 88.34, clear at 20:02:35Z on mempool size 8. Fee cap at 20:03:55Z. End at 20:04:00Z, pending 56. The template detail is the other page. While our class was present, template heavy count stayed 1.

## What we do not add up

Lane fees 8,001.53 tKAS. Mint fees 1.2317 tKAS. The pile join before the lane, 83 transactions, 200 coins, 0 rejects, rounds to 3.59 tKAS. The funding pass before the window, 29 transactions, 0 rejects, fees 2.97 tKAS, added 6,112.91 tKAS. At 19:36:06Z that pass reads 24,913 usable on the funding key. That figure was not sampled again at the phase boundaries. Refill fees on the 31 lines sum to 49.98 tKAS. These are separate lines. We do not publish a sum of them.

One node, one run. We do not read the one-heavy template as a correction of finding 33, or of finding 1. The heavy count of 2 at 19:43:31Z is classed other, and our class is 0.
