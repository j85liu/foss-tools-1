# Section 3: CD (Continuous Deployment)
Led by the CD Lead — do this after CI and Version Control are done

CI verifies a change is safe. CD is what actually ships something
once it's verified. Right now, even a passing check at Meridian
doesn't *do* anything — it just reports pass or fail. Your job: make
a passing check trigger a real, automatic action.

**Real parallel:** even if the real 2012 incident had a check like
the CI Lead built, verification alone doesn't prevent damage — what
matters is that a verified state actually gets acted on
automatically, consistently, every time.

## Your task
Enable GitHub Pages (Settings → Pages → Source: "GitHub Actions").
Add a second job to the CI team's workflow that runs only after the
check passes and only on `main`, and publishes `cd/public/` as a live
status page.

```yaml
  deploy:
    needs: check
    if: github.ref == 'refs/heads/main'
    runs-on: ubuntu-latest
    permissions:
      pages: write
      id-token: write
    steps:
      - uses: actions/checkout@v4
      - uses: actions/configure-pages@v4
      - uses: actions/upload-pages-artifact@v3
        with:
          path: 'cd/public'
      - uses: actions/deploy-pages@v4
```

Edit `cd/public/index.html` to say something real, like "✅ Meridian
Trading — all servers consistent," then commit and watch the page go
live.

## Success looks like
A real URL (Settings → Pages will show it) that displays your status
text, and updates automatically whenever you push a change.

## What to hand the Presenter
A screenshot of the live status page, or the actual link if
presenting from a laptop. This becomes Slide 4