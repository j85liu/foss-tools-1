# Team: CI/CD & Automation

Meridian Trading's 8 trading servers should all report the same flag
status. One doesn't — check `configs/server-1.md` through
`configs/server-8.md`.

**Real parallel:** this mirrors the actual 2012 incident where a
trading firm deployed to 8 servers, missed one, and lost $460M in 45
minutes because nothing automated checked that all 8 matched.

## Your task
Build a GitHub Actions workflow (`.github/workflows/`) that fails the
build if any server config doesn't match the rest.

## Success looks like
Your workflow fails on the current repo state (server-8 is the
outlier). Fix it, push again, it passes.

## If you get stuck
Screenshot the failing run and the error log. That's still a real
slide — explain what you tried and what you think is wrong.

## Your slides (aim for 3)
1. What the real 2012 incident got wrong, in this category
2. Your workflow — screenshot of the Actions tab (red, then green — or red, with your diagnosis)
3. One question for the class: why didn't a human catch this instead?