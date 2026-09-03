# Feng Lab website — notes for Claude Code

Hugo Blox (Wowchemy) academic site for the Feng Lab, deployed to
**https://yafenglab.com** via GitHub Pages.
Repo: `git@github.com:fenglab520/yafenglab.com.git` (branch `main`).

## Working across two machines (home + office)

This project folder lives in **Dropbox**, so the *files* already sync between
both computers automatically. The **Claude Code chat/session does not** — for
that, use **Remote Control** so a session started on one machine is visible and
resumable from the other (and from claude.ai/code or the Claude app).

**On each machine, to keep sessions synced both ways:**
1. Sign in with the **same claude.ai account** (`/login`, Pro/Max — API keys are
   not supported by Remote Control).
2. Start Claude Code with Remote Control on:
   ```bash
   claude --remote-control      # or run /remote-control inside a session
   ```
3. Keep the origin machine online — the session runs locally and other devices
   connect to it live.

A plain `claude` session (no `--remote-control`) will **not** appear on the other
device. Docs: https://code.claude.com/docs/en/remote-control

> Note: because the folder is in Dropbox, `.git/` (and this repo's
> `.claude/settings.local.json` permission allowlist) sync across machines too.

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
