# Wrap-Up: Docs, Licensing & Dependency Hygiene

These three didn't get their own build task, but they're still real
gaps at Meridian Trading — cover them as a short group discussion,
not a build.

## Docs & Community
Meridian has no CONTRIBUTING.md. The real 2012 deploy process lived
in one engineer's head — no written runbook confirmed every server
had actually been checked. What would a one-page CONTRIBUTING.md
need to say to prevent that?

## Licensing
If Meridian wanted to open-source its validation tooling so other
trading firms could reuse it, it has no LICENSE file today. Pick one
license (check choosealicense.com) and explain in one sentence why it
fits a company that still sells a commercial product on top of this
code.

## Dependency Hygiene
Meridian's dependencies aren't pinned to specific versions — every
server could silently run different code. This is a smaller version
of the same root problem as the CI/CD gap: nothing confirms every
server matches. One sentence: why does this matter even if it's not
today's build task?

## Your slide (just 1)
One slide, 3 bullets — one per section above. No artifact required.
This is a discussion slide, not a demo.