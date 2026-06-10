---
title: Bakery flour alert
pillar: build-log
status: idea
platform: [reels, tiktok]
hook_type: build-reveal
length: 45s
created: 2026-06-09
shoot_date: 
posted_date: 
link: 
priority: normal
---

# Bakery flour alert

> Built a small inventory tool for a bakery client that automatically texts the owner when flour stock drops below a set threshold, so they stop running out mid-morning.

## Hooks — write 5+, pick 1
1. I built a thing this week that texts a bakery owner when she's about to run out of flour.
2. A bakery was running out of flour by 9am. I fixed it with about 40 lines of code.
3. My bakery client ran out of flour three times last month. Same problem, same morning rush.
4. I built a stock alert for a bakery in maybe two hours. She hasn't run out since.
5. The bakery owner didn't need a big system. She needed one text message at the right time.
6. Ran out of flour mid-morning, three times in one month. So I built her something small.

**Chosen hook:** A bakery was running out of flour by 9am. I fixed it with about 40 lines of code.

## Beat sheet

| Beat | Time | Voiceover | On-screen / B-roll |
|------|------|-----------|--------------------|
| Hook | 0–3s | A bakery was running out of flour by 9am. I fixed it with about 40 lines of code. | Face, tight. Pinned top text: "ran out of flour. 3x." |
| Context | 3–8s | She's the owner, she also runs the counter, so by the time she noticed the bin was low, the bread was already in the oven. | B-roll: bakery counter, bread on display, early morning light |
| Body A | 8–15s | So I built a small inventory tracker, basically a form her staff fills in at 7am. Weight of the flour bin, that's it. And if it's below the threshold, it sends her a WhatsApp. | Screen recording: simple input form on tablet, one field, submit button |
| Re-hook | 15–17s | But the part that took the longest wasn't the code. | Cut to face, tight, dry delivery |
| Body B | 17–28s | It was figuring out what "low" actually means for her kitchen. First time I set it, the alert fired when she still had two days of stock. So we sat down and ran the math together — how much flour per tray, how many trays by 8am, what's one day's buffer. Took about an hour. | B-roll: whiteboard with simple numbers, then screen: threshold config field being adjusted |
| Re-hook 2 | 28–32s | After that the number made sense and she stopped second-guessing it. | Face return, slower, sets up the resolve |
| Payoff | 32–40s | Now she gets one text, usually around 7:20, and she calls the supplier before the rush starts. Three weeks in, she hasn't run out once. | Proof shot: phone notification screenshot with WhatsApp alert, key detail circled. B-roll: bread coming out of oven, full trays |
| Close | 40–45s | The tool is basically three screens and a WhatsApp API key. | B-roll: code editor, ~40 lines visible, no fluff |

## Voiceover — clean read
<!-- The full spoken track, exactly the way it's said. Read it aloud once. -->

A bakery was running out of flour by 9am. I fixed it with about 40 lines of code.

She's the owner, she also runs the counter, so by the time she noticed the bin was low, the bread was already in the oven. So I built a small inventory tracker, basically a form her staff fills in at 7am. Weight of the flour bin, that's it. And if it's below the threshold, it sends her a WhatsApp.

But the part that took the longest wasn't the code. It was figuring out what "low" actually means for her kitchen. First time I set it, the alert fired when she still had two days of stock. So we sat down and ran the math together, how much flour per tray, how many trays by 8am, what's one day's buffer. Took about an hour.

After that the number made sense and she stopped second-guessing it. Now she gets one text, usually around 7:20, and she calls the supplier before the rush starts. Three weeks in, she hasn't run out once.

The tool is basically three screens and a WhatsApp API key.

## On-screen text
- **Pinned (top):** ran out of flour. 3x.
- **Key captions / numbers (these carry the rupiah — never spoken):** Threshold config screen showing the final agreed number (circled). WhatsApp notification on phone screen with timestamp ~7:20 circled. Word "40 lines" highlighted in caption at hook.

## B-roll shot list
- [ ] Bakery counter with bread on display, early morning, low light warming up
- [ ] Flour bin or bag, close-up, showing approximate level
- [ ] Staff member entering weight into tablet form, one field visible
- [ ] Whiteboard with simple tray-count math (not a polished diagram)
- [ ] Screen recording: threshold config field, value being typed in
- [ ] Phone notification: WhatsApp alert, timestamp visible, number circled
- [ ] Bread trays coming out of oven, full and intact
- [ ] Code editor showing the script, roughly 40 lines, scrolled to the WhatsApp send call

## Proof shot
- **Number on screen:** WhatsApp notification screenshot with the flour alert and 7:20 timestamp circled. Real notification, other messages visible above it for authenticity.
- **Lands on this line:** "Now she gets one text, usually around 7:20"

## Post caption + hashtags

Built a flour alert for a bakery. One form, one WhatsApp, one threshold number we figured out together. Three weeks and she hasn't run out mid-morning once.

The code took two hours. Getting the number right took one more.

#buildinpublic #automation #smallbusiness #whatsapp #operatorbuilder #bakery #nocode #lowcode #buildlog

## Notes
- **Pronunciation flags:** "threshold" — two syllables, stress first: THRESH-old. "WhatsApp" is clean. "supplier" — stress second syllable: su-PLY-er. "inventory" — four syllables, watch pacing: in-VEN-tor-y.
- **Music / SFX:** low ambient kitchen hum under the bakery B-roll, drop to near-silence at the code/screen shots. No beat drop. Keep it understated.
