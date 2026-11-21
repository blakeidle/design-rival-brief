# Design Rival Brief

Vertical competitor-intelligence newsletter + landing page for design SaaS (Canva, Figma, Adobe Express, …).

## What’s here

| Path | Purpose |
| --- | --- |
| `index.html` | Landing page + embedded Issue #1 sample; Stripe Payment Link placeholders |
| `issues/issue-001.md` | Full sourced edition (email / Substack / Beehiiv ready) |
| `scripts/snapshot_diff.py` | Stdlib CLI: snapshot public pricing/changelog URLs → markdown diffs |
| `snapshots/` | Timestamped HTML/text baselines + `latest_diff.md` |

## Pricing (product)

- **Starter — $49/mo** · 3 rivals
- **Pro — $99/mo** · 10 rivals

Wire live Stripe Payment Links (Axon Stewardship, LLC) by replacing `STRIPE_STARTER_LINK` / `STRIPE_PRO_LINK` in `index.html`.

## Snapshot routine (Mon / Thu)

```bash
cd /workspace/design-rival-brief
python3 scripts/snapshot_diff.py
# optional: python3 scripts/snapshot_diff.py --rival canva
```

## One-command deploy (when Vercel + GitHub are reconnected)

```bash
cd /workspace/design-rival-brief && npx --yes vercel --prod --yes
```

Or push this folder as a static site repo and import in the Vercel dashboard (Framework Preset: Other / static).
