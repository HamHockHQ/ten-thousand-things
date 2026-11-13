# Ten Thousand Things — Push-Up Tracker: One-Prompt Build (v3)

Build the complete push-up challenge tracker in any capable AI — Muse, ChatGPT, Gemini, Grok, Copilot, or another assistant that can create an interactive app or web page — with a single paste.

**Version 3 — updated November 13, 2026.** What changed since v2:
- **Check-in rhythm is now adjustable in the app** (every 5 to 120 minutes) with one-tap modes, a live preview, and patterns the tracker learns from what you usually pick. Suggested sets and scheduled reminders both follow the rhythm.
- **Rest days**: a Today toggle plus a weekly rest-day picker, with pace math that spreads the goal over work days only, so a planned day off never puts you behind or breaks your streak.
- **Goal celebration**: confetti and a flexing smoothie cup the moment you hit the day's target, with a Replay button afterwards.
- **Missed-set backfill and splitting**: a collapsed "Forgot to log some sets?" card that adds missed sets as separate entries, and a Split action on any set.
- **Decluttered Log card**: gesture settings behind a cog, exercises in a swipe row with favorites first, and Recent Sets collapsed by default.
- **Full gesture system**: double-tap (0.7s) or hold (650ms) to log, with scroll arbitration, a tap-point burst, and a 10-second lockout.

Everything from v2 still holds: the prompt below is **fully self-contained and carries every link inside it**; the app **opens on the Log tab**, uses **5 tabs**, has the **huge one-tap logging screen** and the **floating Home button**; and there is a **short bootstrap prompt** (below the main prompt) for pointing your AI at this file instead of pasting the long version.

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

Want different numbers? Change the defaults under "Make it yours" before you paste, or just tell the AI afterwards, for example "make my daily target 100" or "add burpees."

## The prompt — copy everything in this block

```text
Build me a personal push-up challenge tracker called "Ten Thousand Things". Build the complete app now, in this one response — do not just describe it, plan it, or ask me to confirm the design first. If your platform can create an interactive app, page, artifact, or canvas, build it there. Otherwise, build it as a single self-contained HTML file I can open in a browser. Ask me only the setup questions listed at the end, and use the defaults below for everything else.

LINKS — READ THIS FIRST
- This prompt is self-contained: everything you need to build the tracker is in the text below. You do NOT need to open, fetch, or wait for any link, file, demo, or external reference, and you must not stop or stall because a link is missing — there is nothing to fetch.
- For reference only (never required to build): the live demo page is https://muse.ai/s/push-up-tracker-demo-page-xtc6xx6xx7bw4xf/qDCSPZPbLwPXKd3-tYsE9XPMP-9V1-8Uh0QsXU98E3g — the tracker you build for me should match what that demo shows, as fully described in words below.
- If your platform is Muse and I am new to it: I joined at https://muse.ai/join and can redeem invite code A6W679 in Settings within 48 hours of joining for bonus tokens. This has nothing to do with building the tracker — never block the build on it.

THE CHALLENGE
- Goal: 10,000 push-ups before January 1, 2027. Challenge period: November 11 to December 31, 2026.
- Daily target: 200 push-ups per day nominal. The working target is a dynamic pace target: total remaining divided by the days remaining (including today), rounded up. When I have a rest plan (see REST DAYS), it is total remaining divided by the remaining WORK days instead.
- Active hours: 11:00 AM to 10:00 PM local time. Timezone default: America/New_York — ask me if mine is different.
- Check-ins: how often the tracker checks in on me. This is a setting I control in the app (see CHECK-IN RHYTHM), starting at every 20 minutes. Suggested set sizes are computed from the current rhythm.

NAVIGATION — FIVE TABS, OPENS ON LOG
- A fixed bottom navigation bar with exactly five tabs, each an icon plus a one-word label: Today, Log, Progress, Exercises, Reminders. Keep the active tab highlighted, keep each tab's state when switching, and never cover page content with the bar.
- The app OPENS on the Log tab — logging a set is the first thing I see and do, with zero navigation first.
- A big floating Home button — a house icon plus the word "Home" — fixed at the bottom right, floating ABOVE everything including the bottom tab bar, visible on every tab. Tapping it always takes me to the Today tab. It is separate from the bottom navigation, not one of the tabs.
- Spacing rule: the floating Home button must never cover a control. Give every page enough bottom padding that the Log card's quick-rep chips and the slider's end labels can always scroll clear of it.

CHECK-IN RHYTHM — MY CADENCE, ADJUSTABLE ANY TIME
- A "Check-in rhythm" card that is ALWAYS visible on the Today tab and at the TOP of the Reminders tab. Never bury it in settings.
- A slider from every 5 minutes to every 120 minutes (starts at 20), with a plain-language label for the current band (for example "Catch-up: frequent, small sets", "Normal rhythm", "Focused: balanced", "Deep work: spaced out, fewer interruptions").
- One-tap mode chips: Catch-up · 10, Normal · 20, Focused · 45, Deep work · 60. Tapping one sets the rhythm immediately.
- Live preview while dragging: show how many check-ins are left today at the dragged value and the per-set size that would result. On save (slider release or a mode chip), the rhythm takes effect instantly: the pace plan, every suggested set size, the next-check-in countdown, and my scheduled reminders all re-spread around the new rhythm with no restart.
- Learning: remember every rhythm I save, tagged with weekday-or-weekend and time of day (morning / afternoon / evening). When one bucket has a clear favorite (the same value saved at least 3 times), suggest it back inside the card ("On weekday afternoons you usually pick every 45 min") with a one-tap "Use every 45 min" button and a dismiss option. Show my learned patterns as a small list in the card. Never change the rhythm on your own — only suggest.

REST DAYS — PLANNED DAYS OFF NEVER COST ME
- A "Rest day" card on the Today tab with a toggle for today. On a rest day: my target is 0, reminders stay quiet, the Today tab says it is a rest day, and anything I log still counts as bonus that shrinks what is left in the challenge.
- A weekly rest-day picker on the Reminders tab: None, or one weekday. That weekday is a rest day every week through the end of the challenge, and the picker shows the math ("Every Sunday is a rest day: 43 work days left, target 228 per work day, flat average 196 per day"). A one-off "work today anyway" on the Today toggle overrides the weekly rest day for that date only.
- Rest-aware pace: when any rest plan exists (a weekly rest day, or individual rest days ahead), the pace target and the ahead/behind math spread the remaining reps over the remaining work days, and rest days do not advance the expected total. A planned rest day never shows as behind, and it never breaks my streak: the streak counts days I logged anything, simply skipping planned rest days.
- On a rest day there is no suggested set and no check-in fires; the Reminders tab shows the rest state instead.

THE TODAY TAB — THREE BIG NUMBERS
1. Left today: today's target minus what I have logged today (headline number, big and visual, e.g. a ring or large type). On a rest day this reads as a rest day with target 0.
2. Left in the challenge: 10,000 minus my all-time push-up total, with a progress bar and percentage.
3. Ahead or behind: compare my actual total with where pace says I should be by end of today, using the rest-aware math above. Show "+X ahead" or "X behind" in plain language, and if behind, the extra per work day that closes the gap.
Also show: today's total per exercise, all-time total, current streak (consecutive days I logged anything, planned rest days skipped), max set, the suggested next set with check-ins remaining, the Check-in rhythm card, the Rest day card, and — once today's target is hit — a Replay celebration button (see CELEBRATION).

THE LOG TAB — ABSOLUTE EASIEST LOGGING, NO TYPING REQUIRED
This is the most-used screen: make logging a set as close to zero-effort as possible.
- An exercise switcher at the top as a HORIZONTAL SWIPE ROW: one pill per exercise, each with a star I can tap to favorite it. Favorites sort to the front of the row. A "+ New" pill at the end jumps to the new-exercise form.
- A GIANT rep number (roughly 100px tall) showing the current slider value.
- An oversized, easy-to-grab slider: fat track and a thumb at least 44px, range 0 to at least 60, with its 0 and top-end labels visible.
- Quick-amount chips: 5, 10, 15, 20, 25 — plus one star chip set to the current smart suggested set size.
- A huge full-width LOG button that reads "LOG {n} {exercise}" with the current value in it.
- A "Copy last set" button that logs my previous set for the selected exercise again in ONE tap; its label shows the value, e.g. "Copy last set: log 15 again". If there is no previous set for that exercise yet, disable it or hide it.
- Typing a count is never required, though let me type an exact number if I want to.
- Every log entry is one set: exercise, reps, date, and time. Never double-count the same set.

QUICK-LOG GESTURES: SETTINGS BEHIND A COG
- The Log card header has ONE icon-only settings cog (a gear, no text label). The quick-log options live behind it, closed by default, so the card stays clean. Inside: a gesture choice with plain-language hints: "Double-tap or hold", "Double tap to log", "Hold to log", "Buttons only". My choice persists.
- Double-tap to log: double-tapping the giant number logs the current slider amount. The window is a relaxed 0.7 seconds between taps. Double-tapping anywhere else on the log card (but not on a control like the slider, chips, or buttons) also logs it. One double-tap logs exactly one set.
- Hold to log: pressing and holding the giant number for about 650ms logs it. Show a ring around the number that fills as I hold, so I can see it working.
- Scroll arbitration: if my finger moves more than about 10px during a press, treat it as a scroll or drag and cancel the gesture. Only a stationary double-tap or hold logs.
- Suppress the iOS text-selection and callout popup on the big number (no copy menu when I double-tap it).
- Feedback: when a gesture logs, show a "+N logged" burst right at the point I tapped, staying for over 2 seconds so I can read it, and vibrate briefly where the platform supports it (note: iOS Safari ignores vibration, so the visual burst has to carry it there).
- Lockout: after a successful quick-log, gestures pause for 10 seconds and the big number shows the countdown. This stops an accidental second gesture from double-logging. The LOG button, Copy last set, and the missed-sets logger below stay live during the lockout.

FORGOT TO LOG SOME SETS? BACKFILL WITHOUT INFLATING MAX SET
- A card titled "Forgot to log some sets?" on the Log tab, COLLAPSED by default, under the main logger.
- Inside: log missed sets as SEPARATE entries dated today. Two ways: (1) pick how many identical sets (1 to 5) of the current slider value; (2) type a comma-separated list like "12, 10, 8". Either way each set becomes its own entry, so my totals rise while my max set stays honest. Show a confirmation listing what was logged, e.g. "Logged 3 separate sets: 12 + 10 + 8 ✓".
- Recent sets: the list of my sets (with delete) lives behind a collapsed summary header that reads like "Recent sets · 4 today · 31 total". Collapsed by default.
- Split: every recent set of 2 or more reps has a Split action that replaces it with two entries of near-halves (15 becomes 8 + 7) on the SAME date, so a set I logged combined stops counting as my max.

CELEBRATION: WHEN THE DAY'S TARGET LANDS
- The moment a logged set takes me to or past today's push-up target, fire a celebration: confetti falling over the screen plus a flexing smoothie cup character (a smoothie, never a beer — this is a workout app), with a short "Goal smashed!" message.
- It fires only on the set that crosses the target, at most once per day, and never during rest days (target 0) or from backfill that does not cross the target.
- After today's target is complete, show a "Replay celebration" button on the Today tab so I can fire it again on demand.
- Reaching the full 10,000 fires the celebration too, with a completion message.

THE PROGRESS TAB
- Track my max set (most reps in one go) for every exercise, all-time and over time.
- Show a graph of my max set by day so I can see the progress line, and a graph of daily totals.
- Analytics: weekly totals and trend (this week vs. last week), totals per day for the last 7 days, best day, average per active day, average set size, sets per day, best single set, and current streak. Keep charts readable on a phone.
- Streak counter with a small celebration at streak milestones (3, 7, 14, 30 days), and achievement badges for milestones such as first 100, 1,000, 5,000, and 10,000 total push-ups, a new max-set record, and a perfect 200 day.
- A "Shake It Up" random mini-challenge (also fine on the Log tab): deals a random challenge — a different rep count, a variation (wide, diamond, slow, or incline push-ups), squats or sit-ups instead, or a beat-your-max-set attempt — which I can accept (and log with the logger) or re-roll.

THE EXERCISES TAB
- A card for every exercise — built-in and custom. The card always shows its name, today total, all-time total, max set, and a Log button; its recent sets and daily-target editor start COLLAPSED behind a Details toggle.
- Each card's Log button jumps straight to the Log tab with that exercise selected and ready.
- A "+ New exercise" form (also fine on the Log tab): I type a name (for example burpees, planks in seconds, or lunges) and optionally a daily target, and it starts tracking immediately — its own slider logging, today total, all-time total, max set, recent sets, and a place in the smart set suggestions if it has a daily target.
- Let me remove a custom exercise (with its sets) without losing the built-in ones.
- Pre-built exercises: push-ups (with the 10,000 challenge target), squats, and sit-ups. Squats and sit-ups track today, all-time, max set, and recent sets, with no fixed daily target unless I set one.

THE REMINDERS TAB — RHYTHM, SMART SUGGESTED SETS, REST, SNOOZE, MUTE, DAY-END
- The Check-in rhythm card sits at the TOP of this tab (see CHECK-IN RHYTHM).
- Smart suggested sets (the most important calculation): at any moment, show exactly how many reps of each targeted exercise I should do in my next set, assuming the same amount at each remaining check-in until the day ends. Formula per exercise: suggested set = ceiling(reps remaining today / check-ins remaining), where check-ins remaining = the number of rhythm-length slots left between now (or the end of an active snooze, if later) and the day's end time, at my CURRENT rhythm setting. Show the check-ins remaining next to the suggestion, and recalculate live whenever I log, snooze, mute, change the rhythm, change the day-end, or add a targeted exercise. If a target is met, or today is a rest day, or the day is done, say so instead of suggesting more.
- Weekly rest-day picker (see REST DAYS).
- Snooze for any duration: a slider (15 minutes to at least 12 hours) — for example I snooze 2 hours for a nap and reminders stay quiet, then resume on their own.
- Mute for the rest of the day: one tap, reminders stop until tomorrow's start time. Mute for a week: one tap, for vacations.
- Adjustable day-end: default 10:00 PM, a control I can move earlier or later on the fly (including past midnight); the smart suggestions use the new end time immediately. The day-end applies to today only — each new day starts back at 10:00 PM.
- Show the current pause state clearly ("Snoozed until 2:26 PM", "Muted for today", "Muted until [date]", "Rest day today") with one tap to cancel and resume, plus a dot or badge on the Reminders tab icon while any pause or rest day is active. While snoozed, muted, or resting, no reminders fire and nothing is logged as a miss.

REMINDERS
- If your platform supports scheduled or recurring tasks, set up a recurring reminder at my current Check-in rhythm (every 20 minutes to start) between 11:00 AM and the day-end time that: tells me how many I have left today and my running total toward 10,000, suggests the current smart set size, and asks how many I did. When I change the rhythm in the app, reschedule future reminders to the new cadence. On rest days, send nothing.
- Each reminder accepts: a tap on "Done — log 10" (logs 10 push-ups), a tap on "Skip this one" (logs nothing), a spoken or typed number (logs that many), or "yes" (logs the suggested set). Log each answer exactly once, and check the tracker first so a set I already logged with the slider is never logged twice.
- If your platform cannot schedule reminders, say so plainly, skip nothing else, and instead put a visible next-check-in countdown in the app based on the current rhythm, shown on the Reminders tab.
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
3. Keep the defaults — 10,000 total, 200 a day, 11:00 AM start, 10:00 PM end, check-ins every 20 minutes to start (adjustable in the app from 5 to 120) — or change any of them?
4. Do I want the recurring reminders set up, if your platform supports them?

ACCEPTANCE CHECKLIST — VERIFY BEFORE YOU PRESENT IT TO ME
- [ ] The app opens on the Log tab, and the bottom bar has exactly five tabs (Today, Log, Progress, Exercises, Reminders) with icons and labels; the floating Home button is visible above everything on every tab, jumps to Today, and never covers the quick-rep chips or the slider's end labels.
- [ ] Logging is zero-typing: giant number, oversized slider, quick chips (5/10/15/20/25 plus the suggestion chip), and a huge LOG button — and both "Copy last set" and the gestures work, logging exactly one set per gesture.
- [ ] The Log card's quick-log options hide behind the icon-only cog, closed by default; the gesture choice (double-tap or hold / double tap / hold / buttons only) persists.
- [ ] Gestures: double-tap within 0.7s logs; a 650ms hold logs with the ring filling; a drag of more than about 10px scrolls instead of logging; the iOS selection/callout popup never appears on the big number; a "+N logged" burst shows at the tap point; after a quick-log the number counts down a 10-second lockout while the LOG button still works.
- [ ] Exercises sit in a horizontal swipe row; starring one moves it to the front and it stays there.
- [ ] "Forgot to log some sets?" starts collapsed; logging missed sets adds them as separate entries (totals rise, max set unchanged); Split turns one entry into two near-halves on the same date; Recent Sets starts collapsed behind its summary header.
- [ ] Today tab shows left today, left in the challenge, and ahead/behind pace, updating instantly when I log.
- [ ] The Check-in rhythm card is on Today and at the top of Reminders: the slider runs 5 to 120, the four mode chips set it in one tap, dragging previews check-ins left and per-set size, and saving instantly re-spreads today's suggested sets.
- [ ] After I save the same rhythm at least 3 times in the same weekday/time-of-day bucket, the card suggests it back with a one-tap Use button, and my learned patterns appear in the card.
- [ ] Rest days: the Today toggle sets target 0 and quiets reminders while logging still works as bonus; the weekly picker sets one weekday; with a rest plan the pace target is per work day, and a planned rest day shows neither as behind nor as a broken streak.
- [ ] Hitting the daily target fires the confetti and smoothie-cup celebration exactly once that day, and a Replay button appears on Today afterwards.
- [ ] Slider logging works for push-ups, squats, and sit-ups, with recent sets shown, deletable, and no double-counting.
- [ ] "+ New exercise" adds a new tracked exercise; exercise cards start with details collapsed, and each card's Log button lands on the Log tab with it selected.
- [ ] Max set is tracked with a progress graph; analytics and weekly summary exist on Progress.
- [ ] Smart suggested set size is displayed and recalculates after logging, snoozing, changing the rhythm, and changing the day-end.
- [ ] Snooze slider, mute today, mute a week, and adjustable day-end (default 10:00 PM, resets daily) all work and show their end time; the Reminders tab shows a pause indicator while any pause or rest day is active.
- [ ] Reminders are scheduled at my current rhythm (and skip rest days), or you have told me plainly that this platform cannot schedule them and added the in-app countdown instead.
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
| Check-in rhythm | Every 20 minutes to start | Adjustable in the app, every 5 to 120 minutes |
| Weekly rest day | None | Any weekday, or one-off rest days from the Today tab |
| Quick-log gesture | Double-tap or hold | Double tap only, hold only, or buttons only (behind the cog on the Log card) |
| Day-end | 10:00 PM, adjustable, resets daily | Later if you train at night |
| Built-in exercises | Push-ups, squats, sit-ups | Keep, remove, or add your own |

## If your AI cannot do one part

Three things depend on the platform, and the prompt already handles all of them:

- **A missing-link complaint.** There is no required link. The full spec and every link are inside the prompt; if an AI says it needs a link or a file, reply: "Nothing is missing — build it from the prompt text alone."
- **Reminders.** Scheduled check-ins need a platform that supports recurring tasks. If yours does not, the AI should say so and give you the in-app countdown on your current rhythm instead — the tracker, pace math, and logging still work in full.
- **Saving your data.** A data-storing tracker cannot be one shared public link that everyone logs into together — each person needs their own copy, in their own account, which is exactly what this prompt creates. That also keeps everyone's numbers private.

Everything else — the five tabs, the floating Home button, the giant logging screen with Copy last set and gesture logging, the rhythm card with learned patterns, rest days, the celebration, missed-set backfill, custom exercises, max-set graphs, smart set suggestions, snooze, badges, and the challenge spinner — should build on any current AI that can make an interactive page or app. If something is missing, point the AI back at its acceptance checklist.
