# Ten Thousand Things — 10,000 Push-Up Challenge Tracker

A personal challenge tracker for doing **10,000 push-ups before January 1, 2027** (about 200 a day). Built to be copied: everyone runs their **own private copy** — there is no shared account and nobody else can see your numbers.

**Project home:** https://github.com/HamHockHQ/ten-thousand-things

**Live demo:** https://muse.ai/s/push-up-tracker-demo-page-xtc6xx6xx7bw4xf/qDCSPZPbLwPXKd3-tYsE9XPMP-9V1-8Uh0QsXU98E3g — try the tracker with sample data, then get your own copy below.

## Get your own copy — three ways

### 1. GitHub: fork it and run it (no AI needed)

1. Fork this repo (or download it and re-upload — see way 3).
2. Open **`tracker.html`** in a browser — that's the complete tracker. It saves your numbers in your own browser (local storage) and starts empty.
3. Want it on your phone like a website? Enable GitHub Pages (Settings → Pages → deploy from `main`, root) and open `https://<you>.github.io/<repo>/tracker.html`. Or rename `tracker.html` to `index.html` in your fork if you want the tracker at the root address.
4. `index.html` in this repo is the demo / get-a-copy page — good for sharing with friends, not for logging your own sets.

### 2. Have Muse (or any AI) build it for you from GitHub

1. Send your AI **this repo's GitHub URL** (the address of this page) — or attach the repo files / drop the unzipped folder into the chat.
2. Paste the **short bootstrap prompt** from [PROMPT.md](PROMPT.md). It tells the AI to read this README, follow PROMPT.md as the full spec, and use `tracker.html` as the reference implementation.
3. Answer four setup questions (or say "defaults") and it builds your private, remembering copy, with reminders if the platform supports them.
4. New to Muse? Join at https://muse.ai/join and redeem code **A6W679** in Settings within 48 hours of joining — we both get 1 billion bonus Muse tokens.

### 3. Download the zip and drop it in

1. Download this repo as a zip (GitHub: Code → Download ZIP) and unzip it.
2. Easiest: open `tracker.html` and just start logging.
3. Or drop `PROMPT.md` — or the whole folder — into a Muse / ChatGPT / Gemini chat with the bootstrap prompt, and let the AI build your copy.

No install works for you? [PROMPT.md](PROMPT.md) also contains the complete long prompt: copy it, paste it as the first message in any capable AI chat, done. The prompt is self-contained — **it needs no link, file, or demo to work**, and it says so right at the top, in case the AI asks.

## What's inside the tracker

- **Opens on the Log tab:** logging is the first thing you see
- **Giant logging screen:** huge rep number, oversized slider, quick chips (5/10/15/20/25 + suggested-set chip), a huge LOG button, **Copy last set** in one tap
- **Gesture logging, tuned behind a cog:** double-tap (a relaxed 0.7s window) or hold (650ms, ring fills) the big number to log, with a "+N logged" burst at the tap point, scroll-vs-gesture arbitration, and a 10-second lockout so a stray tap cannot double-log
- **Five bottom tabs:** Today · Log · Progress · Exercises · Reminders, plus a **floating Home button** above everything on every screen, spaced so it never covers a control
- **Today:** reps left today against a dynamic pace target, left in the challenge, ahead/behind pace, streak, max set, and a Replay button once the goal celebration has fired
- **Check-in rhythm card** (on Today and at the top of Reminders): a slider from every 5 to every 120 minutes, one-tap modes (Catch-up 10 · Normal 20 · Focused 45 · Deep work 60), a live preview of check-ins left and per-set size while you drag, instant re-spread of the day's plan when you save, and learned patterns it suggests back by weekday and time of day
- **Rest days:** a Today toggle (target 0, reminders quiet, anything logged counts as bonus) plus a weekly rest-day picker. Pace spreads over work days only, so a planned rest day never shows as behind and never breaks the streak
- **Goal celebration:** confetti and a flexing smoothie cup the moment the daily target lands, once a day, with a replay on the Today tab
- **Forgot to log some sets?** (collapsed by default): backfill missed sets as separate entries so totals rise without inflating your max set, or type a list like 12, 10, 8. **Split** turns any set into two near-halves on the same date, and Recent Sets starts collapsed too
- **Smart suggested sets:** what's left of today's target ÷ the check-ins remaining at your current rhythm until your day-end
- **Custom exercises** ("+ New exercise") with optional daily targets: squats and sit-ups included from the start. Exercises live in a swipe row on the Log tab with favorites starred first, and each exercise card keeps its details collapsed until you open them
- **Reminders tab:** snooze slider (15 min to 12 h), mute-for-today, mute-for-a-week, adjustable day-end (default 10:00 PM, resets daily), next-check-in countdown on your current rhythm, and a dot on the tab while reminders are paused or today is a rest day
- **Progress:** max-set records and graphs, daily/weekly analytics, streaks, badges, "Shake It Up" random mini-challenges
- **Export / Import (JSON)** so your history is yours to back up and move

## Files in this repo

| File | What it is |
| --- | --- |
| `README.md` | This page — the front door and install guide |
| `PROMPT.md` | The complete one-prompt build spec (v3) + the short bootstrap prompt |
| `tracker.html` | The full standalone tracker — open it and log; data lives in your browser |
| `index.html` | The demo / get-a-copy page (sample data; for trying and sharing) |

## Buy me a smoothie 🥤

The tracker is free. If it helps you, tips are welcome — suggested $1 / $3 / $5.

**Tip link:** https://ko-fi.com/tenthousandthings

## Privacy

Each copy is independent. The standalone tracker keeps its data in the visitor's own browser (local storage); AI-built copies keep data in that person's own account. Nothing is shared with the challenge creator, and no copy is seeded with anyone's real numbers.
