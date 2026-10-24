# Tasks

## GitHub issues (synced 2026-10-24)

- [x] #1 Third-party action pinned to mutable branch (medium) — .github/workflows/update-trophies.yml:20 — FIX — fixed in 9e55634
- [ ] #1 Write token persisted by actions/checkout for later steps (low) — .github/workflows/update-trophies.yml:17 — FIX — open: not safe as written, the upstream action runs a bare git push that relies on the persisted checkout credentials
- [x] #1 actions/checkout pinned to mutable major tag v4 (low) — .github/workflows/update-trophies.yml:17 — FIX — fixed in 9e55634
- [x] #1 Productive Time card uses UTC because UTC_OFFSET is not set (low) — .github/workflows/update-trophies.yml:23-25 — FIX — fixed in f6fc163
- [x] #1 Nuke-unused-themes step is unreachable dead code (low) — .github/workflows/update-trophies.yml:28-49 — FIX — fixed in aad5132
- [x] #1 git add -A stages the whole worktree in the cleanup step (low) — .github/workflows/update-trophies.yml:37 — FIX — fixed in aad5132 (step removed)
- [x] #1 No concurrency guard around scheduled and manual runs (low) — .github/workflows/update-trophies.yml:1-13 — FIX — fixed in b8322fc
- [x] #1 Third-party action on mutable branch with write token (medium, same as the first item) — .github/workflows/update-trophies.yml:20 — FIX — fixed in 9e55634
- [x] #1 Theme preview says all themes but workflow keeps one (low) — profile-summary-card-output/README.md:4 — FIX — fixed in 38ba65b
- [x] #1 Generate-then-delete workaround for unwanted themes (low) — .github/workflows/update-trophies.yml:27 — FIX — fixed in aad5132
- [ ] #1 Possible GITHUB_TOKEN limitation not addressed (low) — .github/workflows/update-trophies.yml:21 — SKIP — checked: all five SVG cards contain data and no error text, no change needed
- [x] #1 No concurrency guard around the scheduled push (low) — .github/workflows/update-trophies.yml:46 — FIX — fixed in b8322fc
- [x] #1 github.ref interpolated directly into the shell script (low) — .github/workflows/update-trophies.yml:46 — FIX — fixed in aad5132
