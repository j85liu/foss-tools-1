# Section 2: Version Control & Enforcement
Led by the Version Control Lead

Right now, anyone can push straight to Meridian's main branch — no
review, no required checks. Detection isn't the same as enforcement:
even if the CI Lead's check exists, nothing forces it to actually
block a bad merge.

**Real parallel:** the actual 2012 deploy was manual and unreviewed —
one engineer missed one server, and nothing forced a second person or
a second check to confirm before it went live.

## Your task
Turn on branch protection on this repo (Settings → Branches) so the
CI check is *required* before merging to main. Then draft a PR
template (`.github/PULL_REQUEST_TEMPLATE.md`) that makes a reviewer
explicitly confirm the check passed.

## Success looks like
Open a test PR with a change that fails the CI check — GitHub should
block the merge button. Fix it, confirm the merge button unblocks.

## If you get stuck
A written description of the settings you'd enable, even if you
couldn't apply them, is still useful to bring to the Presenter.

## What to hand the Presenter
A screenshot of the blocked PR and, ideally, the unblocked one after
the fix. This becomes half of Slide 3 (shared with CD).