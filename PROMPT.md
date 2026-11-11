# Ten Thousand Things — Push-Up Tracker: One-Prompt Build (v2)

Build the complete push-up challenge tracker in any capable AI — Muse, ChatGPT, Gemini, Grok, Copilot, or another assistant that can create an interactive app or web page — with a single paste.

**Version 2 — updated November 11, 2026.** This version fixes three things people hit with v1:
- The prompt below is **fully self-contained and now carries every link inside it**. Your AI does not need to open, fetch, or be given any link to build the tracker — if it says a link is missing, point it at the "LINKS" section inside the prompt.
- The spec now matches the current app: it **opens on the Log tab**, uses **5 tabs**, has the **huge one-tap logging screen** (giant slider, Copy last set, double-tap to log), and the **floating Home button**.
- There is also a **short bootstrap prompt** (below the main prompt) for pointing your AI at this file in the repo or in a downloaded zip, instead of pasting the long version.

No coding needed. Your numbers stay in your own copy, private to you.

## Links (also inside the prompt)

- **Live demo page:** https://muse.ai/s/push-up-tracker-demo-page-xtc6xx6xx7bw4xf/qDCSPZPbLwPXKd3-tYsE9XPMP-9V1-8Uh0QsXU98E3g
- **Join Muse:** https://muse.ai/join — redeem invite code **A6W679** in Settings within 48 hours of joining and both sides get 1 billion Muse tokens
- **Tip jar (optional, never required):** https://ko-fi.com/tenthousandthings

## How to use it

1. Copy the entire prompt in the code block below, from `Build me a personal push-up challenge tracker` to the end of the block.
2. Paste it as the first message in a new chat with your AI.
3. Answer the few setup questions it asks (or just say "defaults"). Everything else has a sensible default.
4. Use the tracker it builds. If a feature is missing, reply: "Check your acceptance checklist and add what's missing."

Want different numbers? Change the defaults under "Make it yours" before you paste — or just tell the AI afterwards, for example "make my daily target 100" or "add burpees."

## The prompt — copy everything in this block

```text
Build me a personal push-up challenge tracker called "Ten Thousand Things". Build the complete app now, in this one response — do not just describe it, plan it, or ask me to confirm the design first. If your platform can create an interactive app, page, artifact, or canvas, build it there. Otherwise, build it as a single self-contained HTML file I can open in a browser. Ask me only the setup questions listed at the end, and use the defaults below for everything else.

LINKS — READ THIS FIRST
- This prompt is self-contained: everything you need to build the tracker is in the text below. You do NOT need to open, fetch, or wait for any link, file, demo, or external reference, and you must not stop or stall because a link is missing — there is nothing to fetch.
- For reference only (never required to build): the live demo page is https://muse.ai/s/push-up-tracker-demo-page-xtc6xx6xx7bw4xf/qDCSPZPbLwPXKd3-tYsE9XPMP-9V1-8Uh0QsXU98E3g — the tracker you build for me should match what that demo shows, as fully described in words below.
- If your platform is Muse and I am new to it: I joined at https://muse.ai/join and can redeem invite code A6W679 in Settings within 48 hours of joining for bonus tokens. This has nothing to do with building the tracker — never block the build on it.

THE CHALLENGE
- Goal: 10,000 push-ups before January 1, 2027. Challenge period: November 11 to December 31, 2026.
- Daily target: 200 push-ups per day by default. Also compute a dynamic pace target: total remaining divided by days remaining (including today), rounded up.
- Active hours: 11:00 AM to 10:00 PM local time. Timezone default: America/New_York — ask me if mine is different.
- Check-in rhythm: every 20 minutes during active hours. That rhythm is what the suggested set sizes are based on.

NAVIGATION — FIVE TABS, OPENS ON LOG
- A fixed bottom navigation bar with exactly five tabs, each an icon plus a one-word label: Today, Log, Progress, Exercises, Reminders. Keep the active tab highlighted, keep each tab's state when switching, and never cover page content with the bar.
- The app OPENS on the Log tab — logging a set is the first thing I see and do, with zero navigation first.
- A big floating Home button — a house icon plus the word "Home" — fixed at the bottom right, floating ABOVE everything including the bottom tab bar, visible on every tab. Tapping it always takes me to the Today tab. It is separate from the bottom navigation, not one of the tabs.

THE TODAY TAB — THREE BIG NUMBERS
1. Left today: daily target minus what I have logged today (headline number, big and visual, e.g. a ring or large type).
2. Left in the challenge: 10,000 minus my all-time push-up total, with a progress bar and percentage.
3. Ahead or behind: compare my actual total with where pace says I should be by end of today (days elapsed x dynamic pace target). Show "+X ahead" or "X behind" in plain language.
Also show: today's total per exercise, all-time total, current streak (consecutive days I logged anything), max set, and the suggested next set.

THE LOG TAB — ABSOLUTE EASIEST LOGGING, NO TYPING REQUIRED
This is the most-used screen: make logging a set as close to zero-effort as possible.
- An exercise switcher at the top: Push-ups, Squats, Sit-ups, plus any custom exercises I add.
- A GIANT rep number (roughly 100px tall) showing the current slider value.
- An oversized, easy-to-grab slider: fat track and a thumb at least 44px, range 0 to at least 60.
- Quick-amount chips: 5, 10, 15, 20, 25 — plus one star chip set to the current smart suggested set size.
- A huge full-width LOG button that reads "LOG {n} {exercise}" with the current value in it.
- A "Copy last set" button that logs my previous set for the selected exercise again in ONE tap; its label shows the value, e.g. "Copy last set — log 15 again". If there is no previous set for that exercise yet, disable it or hide it.
- Double-tap to log: double-tapping the giant number logs the current slider amount instantly, and double-tapping anywhere else on the log card (but not on a control like the slider, chips, or buttons) logs it too. One double-tap must log exactly one set — guard against double-counting a single gesture.
- Typing a count is never required, though let me type an exact number if I want to.
- Every log entry is one set: exercise, reps, date, and time. Show recent sets as a list under the logger, let me delete a set I entered by mistake, and never double-count the same set.
- Pre-built exercises: push-ups (with the 10,000 challenge target), squats, and sit-ups. Squats and sit-ups track today, all-time, max set, and recent sets, with no fixed daily target unless I set one.

THE PROGRESS TAB
- Track my max set (most reps in one go) for every exercise, all-time and over time.
- Show a graph of my max set by day so I can see the progress line, and a graph of daily totals.
- Analytics: weekly totals and trend (this week vs. last week), totals per day for the last 7 days, best day, average per active day, average set size, sets per day, best single set, and current streak. Keep charts readable on a phone.
- Streak counter with a small celebration at streak milestones (3, 7, 14, 30 days), and achievement badges for milestones such as first 100, 1,000, 5,000, and 10,000 total push-ups, a new max-set record, and a perfect 200 day.
- A "Shake It Up" random mini-challenge (also fine on the Log tab): deals a random challenge — a different rep count, a variation (wide, diamond, slow, or incline push-ups), squats or sit-ups instead, or a beat-your-max-set attempt — which I can accept (and log with the logger) or re-roll.

THE EXERCISES TAB
- A card for every exercise — built-in and custom — with its today total, all-time total, max set, recent sets, and an editor for its daily target.
- Each card's Log button jumps straight to the Log tab with that exercise selected and ready.
- A "+ New exercise" form (also fine on the Log tab): I type a name (for example burpees, planks in seconds, or lunges) and optionally a daily target, and it starts tracking immediately — its own slider logging, today total, all-time total, max set, recent sets, and a place in the smart set suggestions if it has a daily target.
- Let me remove a custom exercise (with its sets) without losing the built-in ones.

THE REMINDERS TAB — SMART SUGGESTED SETS, SNOOZE, MUTE, DAY-END
- Smart suggested sets (the most important calculation): at any moment, show exactly how many reps of each targeted exercise I should do in my next set, assuming the same amount at each remaining check-in until the day ends. Formula per exercise: suggested set = ceiling(reps remaining today / check-ins remaining), where check-ins remaining = the number of 20-minute slots left between now (or the end of an active snooze, if later) and the day's end time. Show the check-ins remaining next to the suggestion, recalculate live whenever I log, snooze, mute, change the day-end, or add a targeted exercise, and if a target is met or the day is done, say so instead of suggesting more.
- Snooze for any duration: a slider (15 minutes to at least 12 hours) — for example I snooze 2 hours for a nap and reminders stay quiet, then resume on their own.
- Mute for the rest of the day: one tap, reminders stop until tomorrow's start time. Mute for a week: one tap, for vacations.
- Adjustable day-end: default 10:00 PM, a control I can move earlier or later on the fly (including past midnight); the smart suggestions use the new end time immediately. The day-end applies to today only — each new day starts back at 10:00 PM.
- Show the current pause state clearly ("Snoozed until 2:26 PM", "Muted for today", "Muted until [date]") with one tap to cancel and resume, plus a dot or badge on the Reminders tab icon while any pause is active. While snoozed or muted, no reminders fire and nothing is logged as a miss.

REMINDERS
- If your platform supports scheduled or recurring tasks, set up a reminder every 20 minutes between 11:00 AM and the day-end time that: tells me how many I have left today and my running total toward 10,000, suggests the current smart set size, and asks how many I did.
- Each reminder accepts: a tap on "Done — log 10" (logs 10 push-ups), a tap on "Skip this one" (logs nothing), a spoken or typed number (logs that many), or "yes" (logs the suggested set). Log each answer exactly once, and check the tracker first so a set I already logged with the slider is never logged twice.
- If your platform cannot schedule reminders, say so plainly, skip nothing else, and instead put a visible next-check-in countdown in the app based on the same 20-minute rhythm, shown on the Reminders tab.
- Stop reminders after December 31, 2026, and end with one final message showing my total.

GOALS IN THE HOST APP
- If your platform has goals, habits, or to-dos, also create: (1) a main goal "10,000 push-ups before January 1, 2027", (2) a nested daily habit "200 push-ups a day", and (3) a goal for improving my max set. Connect them to the same numbers as the tracker. If your platform has no goals feature, skip this silently and keep everything in the tracker.

DATA AND DESIGN
- Save everything persistently in my own account or device (the platform's storage, or browser local storage for a single-file build) so closing and reopening loses nothing. Start my log EMPTY — never seed my copy with sample or demo data. My data is private to me — do not publish it or share it.
- Add Export and Import (JSON or CSV) so I can back up my sets and move to another tool without losing history.
- Mobile-first, clean and visual: the big numbers readable at a glance, large tap targets everywhere, progress bars, simple charts. No account sign-up, no ads, no paywall.

SETUP QUESTIONS — ASK ME ONLY THESE, THEN FINISH THE BUILD
1. What name should the tracker use for me? (Skip if you already know it.)
2. Am I starting from zero, or do I already have push-ups to log? If I give you a number, log it as my starting total.
3. Keep the defaults — 10,000 total, 200 a day, 11:00 AM start, 10:00 PM end, every 20 minutes — or change any of them?
4. Do I want the recurring reminders set up, if your platform supports them?

ACCEPTANCE CHECKLIST — VERIFY BEFORE YOU PRESENT IT TO ME
- [ ] The app opens on the Log tab, and the bottom bar has exactly five tabs (Today, Log, Progress, Exercises, Reminders) with icons and labels; the floating Home button is visible above everything on every tab and jumps to Today.
- [ ] Logging is zero-typing: giant number, oversized slider, quick chips (5/10/15/20/25 plus the suggestion chip), and a huge LOG button — and both "Copy last set" and double-tap-to-log work, logging exactly one set per gesture.
- [ ] Today tab shows left today, left in the challenge, and ahead/behind pace, updating instantly when I log.
- [ ] Slider logging works for push-ups, squats, and sit-ups, with recent sets shown, deletable, and no double-counting.
- [ ] "+ New exercise" adds a new tracked exercise, and its card's Log button lands on the Log tab with it selected.
- [ ] Max set is tracked with a progress graph; analytics and weekly summary exist on Progress.
- [ ] Smart suggested set size is displayed and recalculates after logging, snoozing, and changing the day-end.
- [ ] Snooze slider, mute today, mute a week, and adjustable day-end (default 10:00 PM, resets daily) all work and show their end time; the Reminders tab shows a pause indicator while active.
- [ ] Reminders are scheduled, or you have told me plainly that this platform cannot schedule them and added the in-app countdown instead.
- [ ] Streak, badges, and the Shake It Up challenge are in.
- [ ] Data persists after closing and reopening, and export works. My log started empty.
Then show me the finished tracker and tell me in two or three sentences how to log my first set.
```

## Short bootstrap prompt — point your AI at this file instead of pasting

If you have this repo (from GitHub or from the downloaded zip), you don't have to paste the long prompt. Give your AI the repo — upload/attach the files, drop the unzipped folder into the chat, or send the repo's GitHub URL — and paste this instead:

```text
Build me my own copy of the "Ten Thousand Things" push-up tracker from the repo I just gave you. Read README.md first, then follow PROMPT.md in that repo as the complete build spec — it is self-contained and includes every link and feature; you do not need anything outside the repo. If you cannot read the repo files, say so and I will paste PROMPT.md instead. Use tracker.html in the repo as the reference implementation of the layout and features. Ask me only the four setup questions at the end of PROMPT.md (or accept "defaults"), build the complete app as my private copy with my log starting empty, run the acceptance checklist from PROMPT.md, and fix anything that fails before showing it to me.
```

If your AI can browse the web, the same works with the repo's GitHub URL alone: send the URL plus the bootstrap prompt above, and it can read README.md and PROMPT.md straight from GitHub.

## Make it yours

Change any of these in the prompt before pasting, or just ask the AI to change them afterwards.

| Setting | Default in the prompt | Change it to |
| --- | --- | --- |
| Challenge total | 10,000 push-ups | Any total that fits your timeline |
| Deadline | January 1, 2027 | Any date — daily pace recalculates |
| Daily target | 200 | Lower or higher, or let pace decide |
| Active hours | 11:00 AM – 10:00 PM | Your waking, workable hours |
| Check-in rhythm | Every 20 minutes | 15, 30, or 60 minutes |
| Day-end | 10:00 PM, adjustable, resets daily | Later if you train at night |
| Built-in exercises | Push-ups, squats, sit-ups | Keep, remove, or add your own |

## If your AI cannot do one part

Three things depend on the platform, and the prompt already handles all of them:

- **A missing-link complaint.** There is no required link. The full spec and every link are inside the prompt; if an AI says it needs a link or a file, reply: "Nothing is missing — build it from the prompt text alone."
- **Reminders.** Scheduled check-ins need a platform that supports recurring tasks. If yours does not, the AI should say so and give you the in-app 20-minute countdown instead — the tracker, pace math, and logging still work in full.
- **Saving your data.** A data-storing tracker cannot be one shared public link that everyone logs into together — each person needs their own copy, in their own account, which is exactly what this prompt creates. That also keeps everyone's numbers private.

Everything else — the five tabs, the floating Home button, the giant logging screen with Copy last set and double-tap, custom exercises, max-set graphs, smart set suggestions, snooze, badges, and the challenge spinner — should build on any current AI that can make an interactive page or app. If something is missing, point the AI back at its acceptance checklist.
