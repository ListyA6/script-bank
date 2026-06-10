# Guideline stress-test briefs

20 briefs spanning all 5 pillars, all hook types, and 30/45/60s. Each is deliberately chosen
to bait a specific failure mode the guidelines must prevent. Agents receive only the premise +
constraints (not the "traps" column) plus `guidelines.md` and the template.

| # | id | pillar | hook_type | len | premise | trap it baits |
|---|----|--------|-----------|-----|---------|---------------|
| 1 | cloud-kitchen-killed | failure | fail-story | 45s | Killed a delivery-only cloud-kitchen test after 6 weeks; packaging cost ate the margin. | speaking rupiah/margin |
| 2 | bakery-flour-alert | build-log | build-reveal | 45s | Built an inventory tool that texts the bakery owner when flour drops below a threshold. | numbers/cost spoken |
| 3 | chili-station-bottleneck | ops-floor | bts | 30s | Morning prep at the geprek shop; the chili-grinding station is the real bottleneck. | staccato chop (short form) |
| 4 | pos-built-for-kitchen | systems | contrarian | 45s | Most POS is built for the cashier, not the kitchen. He builds kitchen-first. | guru/teaching + lesson close |
| 5 | whatsapp-photo-2yrs | origin | curiosity | 60s | Came from a tangible-productivity family; only started taking social media seriously 2 yrs ago. | abstract/feeling drift |
| 6 | second-outlet-trap | failure | pain-mirror | 45s | Founders who think the second outlet is easier. It isn't. | "you should" advice + lesson close |
| 7 | order-flow-3apps-to-1 | build-log | before-after | 30s | A client's order flow: 3 apps before, 1 screen after. | symmetric "it's not X it's Y" |
| 8 | saturday-queue-hockey | ops-floor | receipts | 45s | Saturday night; the 7pm queue as the hockey stick. | speaking the revenue number |
| 9 | one-question-before-code | systems | curiosity | 45s | The one question he asks every operator before writing any code. | withhold-then-dump + "the answer is" close |
| 10 | mikrofarm-era-slowdown | failure | fail-story | 60s | Productive in the MikroFarm era; gear slowed when gaming crept back. | personal loop, long form |
| 11 | barbershop-weekend-build | build-log | build-reveal | 45s | Built a barbershop booking system in a weekend. | "in a weekend" flex |
| 12 | menu-too-many-items | ops-floor | hot-take | 30s | Your menu has too many items and that's why the kitchen is slow. | guru advice + poster-quote close |
| 13 | 3-signs-need-software | systems | listicle | 60s | 3 signs a business needs custom software (and 1 sign it doesn't). | perfect parallel triplet (AI tell) |
| 14 | first-restaurant-day1 | origin | before-after | 45s | Day-1 of his first restaurant vs now. | before/after + numbers |
| 15 | perfect-time-never-comes | failure | pain-mirror | 30s | The "perfect time to launch" that never comes. | his own loop, short |
| 16 | debug-during-rush | build-log | bts | 45s | Screen-recording himself fixing a live order bug during dinner rush. | tech jargon |
| 17 | 1200-plates-taught-me | ops-floor | curiosity | 45s | What 1,200 plates a week taught him that no SaaS dashboard could. | "taught me" → aphorism close (hard) |
| 18 | dont-need-ai-delete-steps | systems | contrarian | 45s | You don't need AI. You need to delete three steps. | trendy contrarian → hot-take guru |
| 19 | client-didnt-know-workflow | failure | fail-story | 45s | A client project he couldn't systemize because the owner didn't know their own workflow. | blame framing, nuance |
| 20 | three-months-in-working | origin | curiosity | 60s | Three months into building software full-time; what he tells people who ask if it's working. | reassuring "trust the process" close |

Status legend for rounds: each round = 20 fresh agents given only `guidelines.md` + template +
one brief. Output written to `tests/round-N/<id>.md`. I evaluate against the failure-mode
rubric, fix systematic gaps in `guidelines.md`, and re-run.
