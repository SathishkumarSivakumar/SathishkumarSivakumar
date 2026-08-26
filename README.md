# Setup — Sathishkumar S GitHub Profile README

This is a "special" GitHub profile README — the one that shows on your
profile page above your pinned repos.

## 1. Create the special repo
Create a new **public** repository named **exactly** your username:

```
SathishkumarSivakumar
```

(GitHub auto-detects a repo with this exact name and shows its README on
your profile page.)

## 2. Add these files, keeping this exact structure

```
SathishkumarSivakumar/
├── README.md
├── assets/
│   ├── header.svg
│   ├── footer.svg
│   ├── divider.svg
│   ├── skills-radar.svg     (new — radar chart in Tech Stack section)
│   └── stats-strip.svg      (new — impact numbers under the hero)
└── .github/
    └── workflows/
        └── snake.yml        (optional — animates your contribution graph)
```

The header/footer/divider SVGs are custom-designed for this README (dark
navy + cyan + amber, matching your portfolio site) — they're referenced
with **relative paths** (`./assets/header.svg`), so the `assets` folder
must sit next to `README.md` in the repo root.

## 3. Push it
```bash
git init
git add .
git commit -m "Update profile README"
git branch -M main
git remote add origin https://github.com/SathishkumarSivakumar/SathishkumarSivakumar.git
git push -u origin main
```

## 4. Enable the contribution snake (optional but recommended)
The snake animation needs a one-time Action run:
1. Push `.github/workflows/snake.yml` (already included).
2. Go to your repo → **Actions** tab → run "Generate Snake Animation" manually once (or wait for the daily cron).
3. It creates an `output` branch with the generated SVGs — the README already points at it, so it'll just start working.
4. Make sure **Settings → Actions → General → Workflow permissions** is set to "Read and write permissions" or the push step will fail.

## 5. Things worth double-checking / personalizing
- **GitHub stats accuracy**: `count_private=true` in the stats badge only shows private-repo counts to *you* when logged in — visitors see public-only, which is normal.
- **Streak stats service**: uses `streak-stats.demolab.com` (the actively maintained mirror — the old `herokuapp.com` one is dead).
- **Mosquito-repellent project**: no public repo link was available, so it's listed without a "View on GitHub" link. Add one if you publish it.
- I removed the Naukri/Indeed badges from the earlier draft since those links weren't pointing to your actual profiles — happy to add them back with the real URLs if you want them in.

## Color tokens used (for future edits)
| Token | Hex |
|---|---|
| Background | `#070b10` |
| Surface | `#0d141b` |
| Cyan (primary accent) | `#5fe3c8` |
| Amber (secondary accent) | `#f2a154` |
| Text | `#e9eef2` |
| Muted text | `#8ea0ac` |
