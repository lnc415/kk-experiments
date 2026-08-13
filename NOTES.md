# The Copper Whisk — Session Notes for Claude

## What this project is
A bakery website for **The Copper Whisk** — a home bakery run by a family member. The site is live (or going live) at **copper-whisk.com**, deployed automatically via Vercel whenever `main` is pushed to GitHub.

## Tech stack
- Pure static HTML/CSS/JS — no framework, no build step
- 4 pages: `index.html` (homepage), `menu.html`, `gallery.html`, `admin.html`
- Photos go in `photos/gallery/` and are referenced by filename
- Hosted on Vercel, connected to GitHub repo `lnc415/kk-experiments`

## How deployment works
Push to `main` → Vercel auto-deploys → site updates at copper-whisk.com within ~30 seconds.
**Claude handles all git operations.** The user never needs to touch the terminal.

## Admin panel
`admin.html` is a password-protected admin panel for managing menu items, orders, customers, and gallery photos. It's intentionally not linked from the public site — accessed directly by URL.

## What the user (daughter) can ask for
- Change text, prices, descriptions on any page
- Add or update menu items
- Adjust colors, fonts, layout
- Add photos to the gallery
- Any other content or design changes

## When changes are done
Commit and push to main:
```bash
git add -A
git commit -m "describe the change"
git push origin main
```
Vercel deploys automatically after the push. No other steps needed.

## Things already set up
- `.gitignore` excludes `.claude/`, `.vercel/`, `node_modules/`
- Remote is set to `https://github.com/lnc415/kk-experiments.git`
- Branch is `main`
- Domain: copper-whisk.com (via Vercel)
