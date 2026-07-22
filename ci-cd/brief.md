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

## Stretch Goal (optional — only if you finish early)
Right now your check only reports pass/fail in the Actions tab. Add a
second job that automatically publishes a status page — but only
when your check passes.

1. Enable GitHub Pages: Settings → Pages → set source to "GitHub
   Actions"
2. Edit `public/index.html` to say something like
   "✅ [Your Company] passed its safety check"
3. Add a second job to your workflow that runs only after `check`
   succeeds and only on `main`, and deploys `public/` to Pages
4. Watch a real, live webpage go from not-existing to published,
   because your check passed

This is the difference between CI (test/verify) and CD (automatically
ship). Ask an instructor for the deploy job snippet if you want to
try this.