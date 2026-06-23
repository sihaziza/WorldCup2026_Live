# 🏆 Live World Cup 2026 — Brackets & Standings

A single-page, real-time tracker for the **2026 FIFA World Cup** (48 teams, 12 groups).
Live group standings, the official knockout bracket with automatic seeding, and an
interactive "pick the winner" mode — all in one self-contained HTML file.

👉 **Live site:** _add your GitHub Pages URL here_

---

## ✨ Features

- **Live group standings** — pulled automatically from ESPN's free public feed and
  refreshed every 60 seconds. No API key, no backend.
- **In-progress games** — a live ticker shows ongoing matches with the score, minute,
  and goal scorers / assists (smaller line under each match).
- **Outcome dots** — next to each team in the group tables, a blinking dot shows how its
  live match is going: 🟢 **green** = winning · ⚪ **grey** = drawing · 🔴 **red** = losing.
  In-progress results are folded into the table provisionally.
- **Official knockout bracket** — Round of 32 → Final, laid out as a pyramid with
  connector lines, including the third-place play-off.
- **Correct third-place seeding** — the 8 best third-placed teams are slotted into the
  Round of 32 using FIFA's official eligibility rules (Annex C), not just rank order.
- **Interactive picks** — click a team to send it through; click again to undo. Your
  picks are saved locally in your browser (each visitor has their own).
- **Champion celebration** — picking the final winner triggers fireworks in that nation's
  flag colours, plus a champion box and a bronze (3rd-place) box.

---

## 🗂️ Files

| File | Purpose |
|------|---------|
| `index.html` | The entire app (HTML + CSS + JS). |
| `mbappe.avif` | Header image (left). |
| `messi.jpg` | Header image (right). |
| `trophy.svg.webp` | Centre-of-bracket image. |

All four files must live in the **same folder** — the HTML references the images by
relative path.

---

## 🚀 Run it

**Locally:** just double-click `index.html` (open it in any modern browser).

**Host it (free) on GitHub Pages:**
1. Put all four files in a public repo.
2. **Settings ▸ Pages ▸ Deploy from a branch ▸ `main` / root**.
3. Wait ~1 minute → your site is live at `https://<username>.github.io/<repo>/`.

The standings update themselves, so once it's hosted you never need to touch it again.

---

## 🔌 Data sources (ESPN, free, no key)

- Standings: `https://site.api.espn.com/apis/v2/sports/soccer/fifa.world/standings`
- Scoreboard (live games / goals): `https://site.api.espn.com/apis/site/v2/sports/soccer/fifa.world/scoreboard`

If the feed is ever unreachable, the app falls back to a built-in snapshot and shows a
🟡 notice. Standings are always fetched live; only your bracket picks are stored locally.

---

## ⚠️ Notes

- Requires an internet connection for live data and for the flag images (flagcdn.com).
- Not affiliated with, endorsed by, or sponsored by FIFA or ESPN. Team/competition data
  belongs to its respective owners; this is a personal, non-commercial project.
