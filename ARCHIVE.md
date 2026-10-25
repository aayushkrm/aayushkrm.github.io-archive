# Archived: aayushkrm.github.io

This repository is a **complete working archive** of the original
[aayushkrm.github.io](https://github.com/aayushkrm/aayushkrm.github.io) site,
taken on **25 October 2026** before the redesign.

GitHub does not allow one account to own both a repository and a fork of it, so this
archive is a full mirror instead of a GitHub fork. That is actually stronger: it keeps
**every branch, every tag, and the complete commit history**, not just the default branch.

## What is included

- `main` — the full al-folio / Jekyll source of the old site
- `gh-pages` — the previously deployed static output
- `archive/pre-redesign-2026-10-25` — annotated tag marking the exact pre-redesign commit
- A GitHub release containing a generated source ZIP

## Restore the old site

```bash
# 1. Clone the archive
git clone https://github.com/aayushkrm/aayushkrm.github.io-archive.git aayushkrm.github.io
cd aayushkrm.github.io

# 2. Point it at the live repository and push everything back
git remote set-url origin https://github.com/aayushkrm/aayushkrm.github.io.git
git push --force origin main gh-pages --tags
```

Or check out the exact snapshot:

```bash
git checkout archive/pre-redesign-2026-10-25
```

## Build the old site locally

The original README covers the Jekyll/al-folio setup. In short:

```bash
bundle install
bundle exec jekyll serve
```

or use the bundled Docker setup:

```bash
docker compose up
```

## Notes

- The snapshot's rendered homepage and full-page screenshot are stored in the local archive
  folder (`site-snapshot/` and `old-site-fullpage-2026-10-25.png`).
- This repository has no Pages deployment attached; it is a cold-storage copy.
