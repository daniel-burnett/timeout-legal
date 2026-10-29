# Timeout legal-site (temporary stub)

Static, mobile-friendly HTML for **Privacy**, **Terms**, and **Support** — meant for a short-lived **GitHub Pages** (or Notion-mirrored) host while TestFlight / App Review prep is underway.

These pages mirror the drafts in `../docs/PRIVACY_POLICY_DRAFT.md` and `../docs/TERMS_OF_USE_DRAFT.md`. They are **not** lawyer-reviewed and still use `example.com` contacts.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Hub + self-help disclaimer |
| `privacy.html` | Privacy Policy draft |
| `terms.html` | Terms of Use draft |
| `support.html` | Support / Get help / feedback |
| `styles.css` | Shared calm charcoal / off-white styles |

## Publish with GitHub Pages

1. Create a public repo (e.g. `timeout-legal`) and push the **contents** of this folder to the default branch (`main`), **or** push this folder as `/docs` in an existing repo.
2. GitHub → **Settings → Pages**
   - Source: **Deploy from a branch**
   - Branch: `main` (or `gh-pages`)
   - Folder: `/` (root) **or** `/docs` if you placed these files under `docs/`
3. Wait for the Pages build, then open the site URL GitHub shows.

### Expected URLs (once live)

Replace `<user>` with the GitHub username or org that owns the repo. Repo name below is an example (`timeout-legal`).

| Page | URL |
| --- | --- |
| Hub | `https://<user>.github.io/timeout-legal/` |
| Privacy | `https://<user>.github.io/timeout-legal/privacy.html` |
| Terms | `https://<user>.github.io/timeout-legal/terms.html` |
| Support | `https://<user>.github.io/timeout-legal/support.html` |

If you deploy from a user/org **root** site (`<user>.github.io` repo) with these files at `/`, drop the `/timeout-legal` segment.

## After Pages is live

1. Copy the real HTTPS URLs into App Store Connect (Privacy, Terms/EULA, Support).
2. Update **only** `Timeout/Services/LegalURLs.swift` string constants (still `example.com` until then — do **not** invent a fake `github.io` username).
3. Replace `privacy@example.com` / `feedback@example.com` with real inboxes on these pages and in the app.
4. See `../docs/LEGAL_STUB.md` and `../docs/ASC_DAY1.md`.

## Local preview

Open `index.html` in a browser, or from this folder:

```bash
python3 -m http.server 8080
```

Then visit `http://127.0.0.1:8080/`.
