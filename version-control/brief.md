# Team: Version Control & Enforcement

Right now, anyone can push straight to Meridian's main branch — no
review, no required checks. Detection isn't the same as enforcement:
even if the CI/CD team's check exists, nothing forces it to actually
block a bad merge.

**Real parallel:** the actual 2012 deploy was manual and unreviewed —
one engineer missed one server, and nothing forced a second person or
a second check to confirm before it went live.

## Your task
Turn on branch protection on this repo (Settings → Branches) so the
CI/CD team's check is *required* before merging to main. Then draft a
PR template (`.github/PULL_REQUEST_TEMPLATE.md`) that makes a
reviewer explicitly confirm the check passed.

## Success looks like
Try opening a test PR with a change that fails the CI/CD check —
GitHub should block the merge button. Screenshot that blocked state.

## If you get stuck
A written description of the exact settings you'd enable, even if you
couldn't apply them, is still a real slide.

## Your slides (aim for 3)
1. What "detection without enforcement" means, concretely
2. Screenshot: a bad PR blocked from merging
3. One question for the class: what's the tradeoff of requiring review — speed vs. safety?