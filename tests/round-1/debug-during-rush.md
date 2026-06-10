---
title: Fixing a live bug during dinner rush
pillar: build-log
status: idea
platform: [reels, tiktok]
hook_type: bts
length: 45s
created: 2026-06-09
shoot_date: 
posted_date: 
link: 
priority: normal
---

# Fixing a live bug during dinner rush

> Screen-recording himself patching a live order bug in the system while real orders are still coming in during the dinner rush. High pressure, real stakes.

## Hooks — write 5+, pick 1

1. The bug showed up at 7pm. Orders were still coming in.
2. *(chosen)* I'm fixing a bug in the ordering system right now. Live. Orders are still hitting it.
3. My code broke at the worst possible time and I had to fix it with one hand while running the floor with the other.
4. Dinner rush. System bug. About 40 orders already in the queue.
5. This is what it looks like when your own software breaks on you mid-service.
6. I built the ordering system. I also broke it. At 7pm on a Friday.

**Chosen hook:** I'm fixing a bug in the ordering system right now. Live. Orders are still coming in.

## Beat sheet

| Beat | Time | Voiceover | On-screen / B-roll |
|------|------|-----------|--------------------|
| Hook | 0–3s | "I'm fixing a bug in the ordering system right now. Live. Orders are still coming in." | Screen recording: orders dashboard with new tickets dropping in. Pinned text: "LIVE BUG. DINNER RUSH." |
| Context | 3–8s | "It's 7pm on a Friday. My busiest shop. The status field stopped updating, so the kitchen has no idea what's been sent and what hasn't." | B-roll: phone screen showing GoFood orders stacking. Cut to kitchen window — plates being called. |
| Body A | 8–15s | "I can see the bug. It's in the function that writes the status back to the database. One wrong condition and it just... stops writing. So orders come in, they just sit there marked as new forever." | Screen recording: VS Code open, cursor on the broken function. Scroll to the bad line. |
| Re-hook | 15–17s | "But here's the thing — I can't just turn it off." | Face, tight. Slight pause. |
| Body B | 17–28s | "If I take the system down to push a fix, orders that already came in are gone. So I'm writing a patch that runs alongside the live version. I fix the condition, test it on one order, watch the status flip. It works. I push it." | Screen recording: writing the patch, terminal showing the deploy. One order status flipping from "new" to "sent." |
| Re-hook 2 | 28–32s | "The kitchen didn't know anything happened. Orders kept moving." | Face return, slower. Slight exhale. |
| Payoff | 32–40s | "About 40 orders went through on the broken version. We had to manually check every one of them against the kitchen printouts after close. Took until midnight." | B-roll: paper kitchen printouts spread on a table. Staff cross-checking tickets. |
| Close | 40–45s | "I found the bug at 6:58. Two minutes before the rush hit." | Screen recording: git blame timestamp showing 6:58pm on the commit. |

## Voiceover — clean read
<!-- The full spoken track, exactly the way it's said. Read it aloud once. -->

I'm fixing a bug in the ordering system right now. Live. Orders are still coming in.

It's 7pm on a Friday. My busiest shop. The status field stopped updating, so the kitchen has no idea what's been sent and what hasn't.

I can see the bug. It's in the function that writes the status back to the database. One wrong condition and it just stops writing. So orders come in, they sit there marked as new forever.

But here's the thing — I can't just turn it off.

If I take the system down to push a fix, orders that already came in are gone. So I'm writing a patch that runs alongside the live version. I fix the condition, test it on one order, watch the status flip. It works. I push it.

The kitchen didn't know anything happened. Orders kept moving.

About 40 orders went through on the broken version. We had to manually check every one of them against the kitchen printouts after close. Took until midnight.

I found the bug at 6:58. Two minutes before the rush hit.

## On-screen text
- **Pinned (top):** "LIVE BUG. DINNER RUSH." — held for first 8s
- **Key captions / numbers (these carry the rupiah — never spoken):** Order count overlay showing tickets coming in real-time. "~40 orders affected" circled in the proof shot. Kitchen printout total visible in the cross-check B-roll — not spoken.

## B-roll shot list
- [ ] Screen recording: orders dashboard with new tickets dropping in, status column stuck on "new"
- [ ] Phone screen showing GoFood order notifications stacking up
- [ ] Kitchen pass/window — plates being called, staff moving
- [ ] VS Code screen recording — cursor on the broken function, slow scroll to the bad condition
- [ ] Terminal: deploy command running, success message
- [ ] Single order status flipping from "new" to "sent" in the dashboard — hold 2s
- [ ] Paper kitchen printouts spread across a table, staff cross-checking with a pen
- [ ] git blame or commit history showing 6:58pm timestamp — hold 2s for the close

## Proof shot
- **Number on screen:** "~40 orders affected" circled on the orders dashboard — a real screenshot with other tabs visible and a real timestamp showing
- **Lands on this line:** "About 40 orders went through on the broken version."

## Post caption + hashtags

Was fixing a live bug at 7pm Friday while orders were still hitting the system. Couldn't take it down — too many orders already in the queue. Had to patch it alongside the live version and pray one order would flip status correctly before I pushed it wide.

It worked. The kitchen never stopped. We were checking printouts until midnight anyway.

#buildinpublic #restauranttech #softwaredevelopment #operatorbuilder #reels

## Notes
- **Pronunciation flags:** "condition" — stress the second syllable (con-DI-tion). "database" — say it as two clean words, don't blur. "function" is fine. "manually" — four syllables, don't rush it.
- **Music / SFX:** low ambient kitchen noise under the first 8s (plates, hood fan, calls from the pass). Cut to silence or very low tension underscore when the screen recording starts. No beat drop. The tension is the content.
- **Shooting note:** the screen recording must be real — a real deploy, real orders, real timestamp. A mocked version kills the proof. If screen recording from that night isn't available, recreate in the actual system with real order data, same timestamp visible.
- **Re-hook at 15s:** face should look genuinely stressed, not performed. Camera-shy is fine here — even a side angle or just the voice works if face-forward feels forced.
