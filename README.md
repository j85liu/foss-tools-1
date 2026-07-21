# foss-tools-1: Meridian Trading

On August 1, 2012, a real trading firm deployed new software to 8
servers. One server didn't get the update — it kept running old,
dead code that reused a flag the new code also used, for a totally
different purpose. Nobody had an automated way to confirm all 8
servers matched. That one server fired unintended trades for 45
minutes. $460 million lost. The company was sold off within a week.
(Source: SEC's public order on the incident.)

Meridian Trading (fictional) just had the same thing happen. Look in
`ci-cd/configs/` — one server never got the update, just like the
real incident. Everything else in this repo is Meridian's tooling as
it existed that day: no CI, no required review, no license, no
documented process.

Two teams will build real fixes. A third piece — docs, licensing,
and dependency hygiene — gets covered as a group discussion, not a
build. By the end, Meridian will have gone from "nothing catches
this" to "this can't happen silently again."