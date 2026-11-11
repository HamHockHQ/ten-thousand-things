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

- **Opens on the Log tab** — logging is the first thing you see
- **Giant logging screen:** huge rep number, oversized slider, quick chips (5/10/15/20/25 + suggested-set chip), a huge LOG button, **Copy last set** in one tap, and **double-tap to log**
- **Five bottom tabs:** Today · Log · Progress · Exercises · Reminders, plus a **floating Home button** above everything on every screen
- **Today:** reps left today, left in the challenge, ahead/behind pace, streak, max set
- **Smart suggested sets:** what's left ÷ remaining 20-minute check-ins until your day-end
- **Custom exercises** ("+ New exercise") with optional daily targets — squats and sit-ups included from the start
- **Reminders tab:** snooze slider (15 min – 12 h), mute-for-today, mute-for-a-week, adjustable day-end (default 10:00 PM, resets daily), next-check-in countdown
- **Progress:** max-set records and graphs, daily/weekly analytics, streaks, badges, "Shake It Up" random mini-challenges
- **Export / Import (JSON)** so your history is yours to back up and move

## Files in this repo

| File | What it is |
| --- | --- |
| `README.md` | This page — the front door and install guide |
| `PROMPT.md` | The complete one-prompt build spec (v2) + the short bootstrap prompt |
| `tracker.html` | The full standalone tracker — open it and log; data lives in your browser |
| `index.html` | The demo / get-a-copy page (sample data; for trying and sharing) |

## Buy me a smoothie 🥤

The tracker is free. If it helps you, tips are welcome — suggested $1 / $3 / $5.

**Tip link:** https://ko-fi.com/tenthousandthings

## Privacy

Each copy is independent. The standalone tracker keeps its data in the visitor's own browser (local storage); AI-built copies keep data in that person's own account. Nothing is shared with the challenge creator, and no copy is seeded with anyone's real numbers.
