> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value. Counts only.

# Template, pre-run 45

The desk probe, every 20 s, on our own desk node. A minute with three samples takes the middle sample in time order. That is the cell. A minute with two samples is not given a middle. Template storage mass is the mass the template's transactions carry. "Under 400k" is how many of those samples had template storage mass under 400,000. The lane log is a different clock: its pending count is the lane's own in-flight count on that minute line. "Our heavy" is the probe's class for ids this lane had already written, at fee rate 920.

The lane was off in the start minute, in BASE (19:43–19:46Z) and in QUIET (19:46–19:58Z). CONGEST on the clock was 19:58–20:04Z, one hundred chains, no ready cap, rate 920, fee cap 8,000 tKAS. The lane's pause tripped at 19:59:53Z and cleared at 20:00:14Z, then tripped at 20:02:15Z and cleared at 20:02:35Z. The fee cap tripped at 20:03:55Z. RETURN on the clock was 20:04–20:07Z. The 20:03 lane minute was not flushed. The probe covers it. The phase map for the guest, the hops and the mint is [../FINDINGS-MAP.md](../FINDINGS-MAP.md).

| Minute (UTC) | Step | Samples | Mempool | Ready count | Ready mass, blocks of 500k | Template txs | Template storage mass | Samples under 400k | Fee estimate priority / normal / low | Our heavy in mempool | Lane pending | Lane submit-OK |
|---|---|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|
| 2026-11-14T19:42 | start | 2 | 0 | 0 | 0 | 0 | 0 | 2 of 2 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:43 | BASE | 3 | 4 | 4 | 1.18 | 3 | 460,297 | 2 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:44 | BASE | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:45 | BASE | 3 | 50 | 50 | 0.20 | 50 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:46 | QUIET | 3 | 2 | 2 | 0.03 | 2 | 284 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:47 | QUIET | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:48 | QUIET | 3 | 9 | 9 | 0.68 | 9 | 336,232 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:49 | QUIET | 2 | — | — | — | — | — | 2 of 2 | — | — | 0 | 0 |
| 2026-11-14T19:50 | QUIET | 3 | 6 | 6 | 0.51 | 6 | 255,809 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:51 | QUIET | 3 | 0 | 7 | 0.60 | 7 | 300,204 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:52 | QUIET | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:53 | QUIET | 3 | 8 | 8 | 0.69 | 8 | 345,760 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:54 | QUIET | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:55 | QUIET | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:56 | QUIET | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T19:57 | QUIET | 3 | 1 | 1 | 0 | 1 | 0 | 3 of 3 | 179.25 / 143.32 / 109.91 | 0 | 0 | 0 |
| 2026-11-14T19:58 | CONGEST | 3 | 1,490 | 1,495 | 64.21 | 1 | 266,685 | 3 of 3 | 1,469.54 / 196.70 / 115.38 | 99 | 100 | 651 |
| 2026-11-14T19:59 | CONGEST | 3 | 4,390 | 4,389 | 78.85 | 2 | 266,805 | 3 of 3 | 1,491.30 / 196.74 / 115.38 | 93 | 12 | 525 |
| 2026-11-14T20:00 | CONGEST | 3 | 1,032 | 1,032 | 57.11 | 2 | 310,994 | 3 of 3 | 1,470.15 / 196.70 / 115.38 | 92 | 99 | 523 |
| 2026-11-14T20:01 | CONGEST | 3 | 4,126 | 4,126 | 79.14 | 2 | 266,693 | 3 of 3 | 1,545.75 / 196.83 / 115.39 | 97 | 99 | 553 |
| 2026-11-14T20:02 | CONGEST | 3 | 8 | 8 | 0.70 | 8 | 348,211 | 3 of 3 | 100 / 100 / 100 | 0 | 99 | 506 |
| 2026-11-14T20:03 | CONGEST | 3 | 3,167 | 3,167 | 71.78 | 3 | 268,558 | 3 of 3 | 1,534.18 / 196.81 / 115.39 | 90 | — | — |
| 2026-11-14T20:04 | RETURN | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | — | — |
| 2026-11-14T20:05 | RETURN | 3 | 1 | 1 | 0 | 1 | 8 | 3 of 3 | 100 / 100 / 100 | 0 | — | — |
| 2026-11-14T20:06 | RETURN | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | — | — |

19:42 has two samples, 19:42:31Z and 19:42:51Z. Both are empty, fee estimate 100 / 100 / 100, and the lane submitted 0. They agree, so the row is both of them. It is not a middle of three.

The 19:43 cell is a trap if it is read alone. The sample at 19:43:11Z is empty. The middle sample, at 19:43:31Z, is the cell: mempool size 4, ready count 4, ready mass 1.18 blocks, template transactions 3, storage mass 460,297, heavy count 2, classed other, our heavy class 0, fee estimate 100. The 101–149 band in that sample holds 1 transaction, and that one is ready. The sample at 19:43:52Z is empty. This is the only sample in the run with a template heavy count above 1. It is before our lane. It is over 400,000. The other two samples of the minute are under 400,000, which is why the column says 2 of 3.

The 19:44 cell is empty. The sample at 19:44:53Z has a size field of 0, a ready count of 1, template storage mass 171, and one transaction in the 101–149 band. The cell hides it.

The 19:45 cell is mempool size 50. The samples at 19:45:14Z and 19:45:55Z are empty. The cell hides those.

The 19:46 cell is mempool size 2 and template storage mass 284. The sample at 19:46:15Z is empty. The sample at 19:46:56Z has mempool size 5, ready count 15, ready mass 0.81 blocks, template transactions 15, storage mass 338,155, heavy count 0, and 7 transactions in the 101–149 band. The cell hides that filled template.

The 19:47 cell is empty. The sample at 19:47:17Z has template storage mass 294,967, 7 transactions, heavy count 0. The sample at 19:47:58Z has template storage mass 340,930, 9 transactions, heavy count 0. The cell hides both.

19:49 has two samples. It is not given a middle. At 19:49:19Z the sample is empty, fee estimate 100. At 19:49:40Z mempool size is 8, ready count is 8, ready mass is 0.67 blocks, the template has 8 transactions and storage mass 336,454, heavy count 0, fee estimate 100. Both are under 400,000. The lane submitted 0.

The 19:51 cell has a size field of 0 and a ready count of 7, template storage mass 300,204, heavy count 0. The sample at 19:51:02Z has mempool size 8, ready count 16, template storage mass 342,048. The sample at 19:51:43Z has mempool size 8, ready count 8, template storage mass 340,642. The cell is the middle sample. It hides the two larger templates. We report the size field and the ready count as the probe wrote them.

The 19:53 cell is template storage mass 345,760, heavy count 0. The sample at 19:53:05Z has template storage mass 112,414, heavy count 1, classed other, our heavy class 0, fee estimate 100. The lane is still off. The cell hides that one. The sample at 19:53:45Z has template storage mass 342,169, heavy count 0.

The 19:57 cell is the quiet fee bump: priority 179.25, normal 143.32, low 109.91, mempool size 1, template storage mass 0. The sample at 19:57:10Z has template storage mass 348,560, 9 transactions, fee estimate 100. The sample at 19:57:51Z has template storage mass 348,625, 8 transactions, fee estimate 100. The cell hides those. One guest match in the previous minute logged a priority quote of 126.68. That quote is the guest log, not this cell.

The 19:58 cell is the first full congest minute: mempool size 1,490, ready count 1,495, ready mass 64.21 blocks, one template transaction, storage mass 266,685, heavy count 1, our heavy class 99, priority fee 1,469.54. The sample before it, at 19:58:11Z, has mempool size 564, ready count 564, ready mass 51.66, our heavy class 89, priority fee 1,400.22. The sample at 19:58:52Z has mempool size 2,599, ready count 2,598, ready mass 69.24, three template transactions, storage mass 266,726, heavy count 1, our heavy class 95. The 651 submits belong to the minute. The lane line says pending 100.

The 19:59 cell is not the pause. The middle sample, at 19:59:33Z, has mempool size 4,390, ready count 4,389, ready mass 78.85, two template transactions, storage mass 266,805, heavy count 1, our heavy class 93, priority fee 1,491.30. The sample at 19:59:53Z is the pause: mempool size 5,300, ready count 5,349, ready mass 86.68 blocks, three template transactions, storage mass 266,737, heavy count 1, our heavy class 96, the 101–149 band holds 5,207, priority fee 1,526.08. The lane wrote its hold at that same second. The lane's 19:59 minute line says pending 12 and held 1. That line is stamped at the first tick of 20:00, inside the hold that started at 19:59:53Z and cleared at 20:00:14Z. The 525 submits belong to the minute. The cell hides the hold.

The 20:00 cell is our class back, and it is the highest template storage mass while our class was present: 310,994, two template transactions, heavy count 1, our heavy class 92, mempool size 1,032, ready mass 57.11, priority fee 1,470.15. The sample at 20:00:13Z is the clear: mempool size 0, ready count 7, ready mass 0.13, fee estimate 100, our heavy class 0. The lane wrote its hold clear at 20:00:14Z. The sample at 20:00:54Z has our class again: mempool size 2,047, ready mass 63.29, our heavy class 91, priority fee 1,493.46. The cell hides the clear. The 523 submits belong to the minute. The lane line says pending 99.

The 20:02 cell is a trap if it is read alone. The sample at 20:02:14Z still has our class: mempool size 5,773, ready count 5,823, ready mass 88.34 blocks, two template transactions, storage mass 266,729, heavy count 1, our heavy class 93, the 101–149 band holds 5,667, priority fee 1,555.31. The lane wrote its second hold at 20:02:15Z. The middle sample, at 20:02:35Z, is the cell: mempool size 8, ready count 8, ready mass 0.70 blocks, template transactions 8, storage mass 348,211, heavy count 0, our heavy class 0, fee estimate 100. The lane wrote its clear at that same second. This clear is not an empty mempool. The sample at 20:02:55Z has our class back: mempool size 989, ready count 1,000, ready mass 61.78, one template transaction, storage mass 268,550, heavy count 1, our heavy class 99, priority fee 1,495.55. The 506 submits belong to the minute. The lane line says pending 99 and held 0, because that line is stamped after the clear.

Across the sixteen samples from 19:58:11Z through 20:03:56Z while our heavy class was present, skipping the clear at 20:00:13Z and the clear at 20:02:35Z, template storage mass runs from 266,682 to 310,994. All sixteen are under 400,000. The template's heavy count is 1 in each. Some of those samples have 2, 3 or 4 template transactions. The extra ones are not a second heavy of this shape. The 310,994 sample, at 20:00:33Z, is heavy count 1 and two template transactions. Our heavy class in those sixteen samples is 79 to 99 transactions, all ready, fee rate 920 on the class. The low of 79 is the sample at 20:03:56Z, one second after the fee cap. The probe did not see exactly 100. The same sixteen samples hold 461 to 5,667 other transactions in the 101–149 fee band. On the first six of those samples the band's ready count is one below its count. On the later ten the ready count matches the count. Mempool size in those samples is 564 to 5,773. Ready mass runs from 51.66 to 88.34 blocks. The two samples over 80 are 86.68 at 19:59:53Z and 88.34 at 20:02:14Z. The priority fee estimate on those sixteen samples is 1,400.22 to 1,555.31. In some samples the ready count is above the mempool size field: 1,495 and 1,490 at 19:58:32Z, 5,349 and 5,300 at 19:59:53Z, 4,897 and 4,839 at 20:01:54Z, 5,823 and 5,773 at 20:02:14Z, 1,000 and 989 at 20:02:55Z. We report both as the probe wrote them.

The lane's own minute lines say pending 100, 12, 99, 99 and 99, and submit-OK 651, 525, 523, 553 and 506. One hundred chains were available, the ready cap was off, and pending on the first of those lines is 100. The 12 is the 19:59 line, stamped inside the first hold. The lane's 20:02 line keeps held at 0. The holds are the phase log, not that column, except the 19:59 line, which does say held 1. The 20:03 lane minute was not flushed. The five flushed lines sum to 2,758 submit-OK. The end line says 3,259. The difference, 501, is arithmetic from those two figures. It is not a flushed minute row.

The lane's end line at 20:04:00Z: 3,259 submit-OK, 0 rejects, 0 lost, fees 8,001.53 tKAS, parked 122.21 tKAS, 273 coins taken, pending 56. Node rate on the lane's own lines was 919.94–920. The 20:01 line is the one that reads 919.94. Storage mass on the calibration line is 266,666 for the SDK figure and for the node figure. The second lane submitted 0. The fee cap of 8,000 tKAS tripped at 20:03:55Z, fees 8,001.53 tKAS, moved 8,123.74 tKAS. The moved cap of 10,000 tKAS did not trip. The pile floor of 200 did not trip. The start line is 476 coins and 13,036 tKAS.

BASE fee estimate stayed at 100 / 100 / 100. It was not an empty mempool. The 19:43:31Z sample is the heavy count of 2 above. The 19:45 cell is mempool size 50.

RETURN on the probe is a fee estimate of 100 / 100 / 100 and our heavy class 0. 20:04's middle sample is empty. One sample in that minute, at 20:04:57Z, has mempool size 5, ready count 5, ready mass 0.09, five template transactions, storage mass 0. 20:05's cell is mempool size 1 and template storage mass 8. 20:06's cell is empty. One sample at 20:06:59Z has mempool size 1, ready count 2, template storage mass 0. The lane has no minute line in these minutes. The end line, at 20:04:00Z, says pending 56. The probe samples after the stop do not show that pending count. We report both clocks.
