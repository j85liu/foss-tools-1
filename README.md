# foss-tools-1: Meridian Trading

On August 1, 2012, a real trading firm deployed new software to 8
servers. One server didn't get the update — it kept running old,
dead code that reused a flag the new code also used, for a totally
different purpose. Nobody had an automated way to confirm all 8
servers matched. That one server fired unintended trades for 45
minutes. $460 million lost. The company was sold off within a week.
(Source: SEC's public order on the incident.)

Meridian Trading (fictional) just had the same thing happen. Look in
`ci/configs/` — one server never got the update, just like the real
incident.

Your team has 5 roles: a CI Lead, a Version Control Lead, a CD Lead,
a Wrap-Up Lead, and a Presenter. Work through the four sections
together, in order — CI, then Version Control, then CD, then Wrap-Up
— each led by its own lead. The Presenter compiles everyone's
contributions into a 3-4 slide deck.

By the end, Meridian will have gone from "nothing catches this" to
"this can't happen silently again, and the fix ships itself."