# Feng Lab website — notes for Claude Code

Hugo Blox (Wowchemy) academic site for the Feng Lab, deployed to
**https://yafenglab.com** via GitHub Pages.
Repo: `git@github.com:fenglab520/yafenglab.com.git` (branch `main`).

## Working across two machines (home + office)

This project folder lives in **Dropbox**, so the *files* sync between both
computers automatically. Claude Code **sessions** sync separately, and how
depends on which tool you use.

**Primary setup: the Claude Desktop app** (`/Applications/Claude.app` →
"Claude Desktop – Code"). This is what's used here. Its sessions sync across
devices through your **Claude account**, so to see them on both machines:
1. Sign **both** Desktop apps into the **same account**
   (`annejanefeng@gmail.com`, Pro/Max) and keep both apps updated.
2. If a session on one machine doesn't show on the other, the usual cause is an
   account/sign-in mismatch (or the app being out of date) — not the code, which
   Dropbox already syncs.

**Optional: the terminal CLI.** The standalone `claude` command is *not*
required and isn't installed by default on these machines (no `node`/`npm`
needed either). Install it only if you want a terminal workflow:
```bash
brew install --cask claude-code            # Homebrew (already installed here)
# or: curl -fsSL https://claude.ai/install.sh | bash   # native installer, auto-updates
claude --version                            # verify, then `claude` to start + log in
```
With the CLI you can also use **Remote Control** to view/resume a running
terminal session from another device: `claude --remote-control` (or
`/remote-control` inside a session). Docs:
https://code.claude.com/docs/en/remote-control

> The folder is in Dropbox, so `.git/` and the `.claude/settings.local.json`
> permission allowlist travel between machines too.

## Local preview / build

The theme is pinned to **Hugo Extended v0.128.0** (see
`.github/workflows/hugo.yml`, `HUGO_VERSION`). Newer Hugo (e.g. 0.16x) **breaks
the build** (`getCSV`/render-hook errors), so match the CI version locally:

```bash
hugo server   # must be Hugo Extended 0.128.0
```

Deploy: push to `main` → GitHub Actions builds and publishes to yafenglab.com
(usually live within ~1–2 minutes).

## Conventions worth keeping

- **Images**: optimize before committing (auto-orient, ~1600px long side,
  quality ~82) so the repo stays lean. News-post body images and gallery photos
  should be web-sized (≤ ~1 MB).
- **News posts** live in `content/post/<date-slug>/` with a `featured.jpg`
  (card + pop-up top image) and body photos via `![image](file.jpg)`.
- **People** are in `content/authors/<chinese-name>/`; `user_groups` sets the
  section (Graduate Student, Previous Members = shown as "Lab Alumni", etc.) and
  `role` drives the position ordering within a group.
- **SEO**: taxonomy pages, individual posts/papers/member pages (except the PI),
  and projects are `noindex` + kept out of the sitemap; gallery images are
  blocked from Google via `robots.txt` (`layouts/robots.txt`).
