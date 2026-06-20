# FunTimes 🎯

**Make prospecting a game.** A single-page, zero-backend web app that turns a broker's
daily prospecting grind into something with points, streaks, and levels.

Line-agnostic — works for any broker (work comp, commercial P&C, benefits, personal lines).

## What it does

- **Log activity in one tap** — Dial, Live convo, Email/DM, Meeting set, Quote sent, Policy won.
  Each is worth points (a dial is 5, a won policy is 100).
- **Daily goal + progress bar** — set a points target; the bar fills as you work. Hit it and
  you get confetti.
- **Streaks 🔥** — consecutive days with at least one activity. Miss a day, it resets. Keeps you
  coming back.
- **Ranks** — Rookie → Dialer → Connector → Closer → Rainmaker → Legend, based on all-time points.
- **Spin an opener 🎡** — stuck on what to say? Spin the wheel for a battle-tested conversation
  starter.
- **Stats** — today's points, this week, all-time, and recent activity log.

## Privacy

100% client-side. Everything is stored in your browser's `localStorage` — no account,
no server, nothing leaves your device. Export your data to JSON anytime.

## Run it

It's a static page. Just open `index.html`, or host the folder anywhere:

```bash
# local preview
python3 -m http.server 8000
# then visit http://localhost:8000
```

### Deploy to GitHub Pages

Push this folder to a repo and enable Pages (Settings → Pages → deploy from branch).
The app is a single `index.html` with no build step or dependencies.

## Customize

Everything lives in `index.html`:

- **Point values & activities** — edit the `ACTIVITIES` array.
- **Ranks** — edit the `RANKS` array (`at` = points threshold).
- **Openers** — edit the `OPENERS` array (`[label, script]`).

## Roadmap ideas

- Weekly leaderboard (shareable link / paste-in codes for an agency)
- Configurable activity types per broker
- Optional "lead magnet" mode: a shareable savings-estimator the broker sends to prospects
