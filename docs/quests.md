# Final Cast — 12 quests (v0.2 rewrite)

Every quest unlocks something new — tackle, a lure, a water, or a mechanic. Any quest that was only "catch X more fish" with no new choice or reward was cut or rewritten. Difficulty: 1 = first hour, 5 = endgame.

## Quest types and story beats (VEX 5.0 item 6)

The loop is not the same quest twelve times: each quest has a type, and
each water carries a story beat that breaks the repetition. The beats:
**Millpond** is learning the pond — dawn, the Sunken Log, the Old
Mossback watching from the deep. **Cedar Creek** is the chase — dusk at
Boulder Run, the Silver King, the first legend a player can name.
**Ember Lake** is the trial — night at the Hot Spring Inlet, the
Emberfin, the hardest fight in the game.

| # | Objective | Type | New unlock / mechanic | Water | Difficulty | Story beat |
|---|---|---|---|---|---|---|
| 1 | Cast your line and catch your first fish (idle line does the work) | Tutorial | Idle line + first rod | Millpond | 1 | Dawn on the Millpond — your line is in before you know how to fish. |
| 2 | Land your first hand-fought fish: hookset inside the bite window | Timing | Hand-fishing loop + bite cue | Millpond | 1 | The first BITE! — the rod is yours now, not the line's. |
| 3 | Try all three retrieve speeds (slow / medium / fast) and note which one bites | Experiment | Lure retrieves at three speeds | Millpond | 2 | Slow, medium, fast — the pond answers differently to each. |
| 4 | Fish at three worm depths and catch one fish from the deep | Experiment | Worm depth (shallow / mid / deep) | Millpond | 2 | Something old lives deep — the Sunken Log is down there. |
| 5 | Catch a fish from each of the three Millpond spots | Exploration | Fishing-spot choice | Millpond | 2 | Three spots, three moods of the same pond. |
| 6 | Unlock and equip your first lure | Economy | Lure unlocks + tackle shop | Millpond | 2 | Your first lure — bought with fish you caught, not money. |
| 7 | Upgrade your rod, then land a large fish | Upgrade | Rod upgrades | Cedar Creek | 3 | The creek runs faster — your old rod is not enough. |
| 8 | Fish Cedar Creek at dusk and meet the Silver King | Legend | Legend encounters + time of day | Cedar Creek | 3 | Dusk at Boulder Run — the Silver King shows itself. |
| 9 | Unlock the Ember Lake water by completing the Cedar Creek set | Unlock | New water: Ember Lake | Ember Lake | 4 | The water steams at night — a new pond, a new rule. |
| 10 | Catch the Emberfin at the Hot Spring Inlet at night | Legend | Legend tied to one spot + time | Ember Lake | 4 | Night at the Hot Spring Inlet — the Emberfin burns the line. |
| 11 | Complete the collection: one of every common fish across all three waters | Collection | Collection log + completion rewards | All waters | 5 | Every fish, every water — the log is the proof. |
| 12 | Land the Old Mossback at the Sunken Log at dawn — the third legend | Legend / finale | Third legend + endgame unlock | Millpond | 5 | Back where it started, at dawn — the Mossback was always there. |

## Quests cut or rewritten

- Any v0.1 quest that read as "catch X more fish" with no new choice or reward was rewritten above (quests 3, 4, 5 each add a mechanic instead of a count) or cut. The v0.1 quest list is in the audit file — confirm each cut quest against it during the line-by-line audit.

## Quest pacing log (VEX 5.0 item 4)

Play quests 1–12 in sequence and log minutes idle versus active, time
per quest, and where the loop repeats. The game logs this automatically
(`src/playtest.js`: `noteQuestClock` while playing, `logQuestComplete`
when a quest finishes, `questSummary()` in the export) — idle minutes
are time the line fished on its own, active minutes are time inside a
bite or a fight. A quest whose active minutes are a small slice of its
total is mostly waiting: vary it, shorten it, or give it a new mechanic
instead of leaving it as wait, fight, repeat.

**Status: no 1–12 playthrough recorded yet.** Fill this table from a
real playthrough; do not fill it from a guess.

| Quest | Idle min | Active min | Total min | Repeats? (what repeats) |
|---|---|---|---|---|
| 1 | _to be recorded_ | | | |
| 2 | _to be recorded_ | | | |
| 3 | _to be recorded_ | | | |
| 4 | _to be recorded_ | | | |
| 5 | _to be recorded_ | | | |
| 6 | _to be recorded_ | | | |
| 7 | _to be recorded_ | | | |
| 8 | _to be recorded_ | | | |
| 9 | _to be recorded_ | | | |
| 10 | _to be recorded_ | | | |
| 11 | _to be recorded_ | | | |
| 12 | _to be recorded_ | | | |

## Endgame — after quest 12 and legend 3

- **Collection completion**: finish the collection log; each completed set pays a coin bonus and a title.
- **Harder legend variants**: each legend returns as a "golden" variant with a tighter bite/hookset window.
- **Daily / spot rotation**: one spot per day is "hot" (better odds, noted in the game); legend spots rotate weekly.
- If none of those is chosen, the game ends cleanly with a completion screen and a free-play mode.

## Monetization (explicit decision)

**Free, no ads.** Recorded in the game settings. If this ever changes, the decision is re-recorded here and in Settings — never silently.
