# Starkeys: design brief for a browser-based touch-typing game (v1)

*Working title "Starkeys". Audience: a 4th grader (~9–10) and a 6th grader (~11–12). Single-file HTML/canvas, offline, no accounts.*
*Each design choice links to a finding in `research.md` (tags like **[F1.4]**). Choices with no supporting research are marked **(design bet)**.*

---

## 1. Design goals, in priority order

1. **Same finger for the same key, every time, with eyes on the screen.** This habit is what separates skilled from unskilled typists **[F0.1, F1.2]**. Speed comes later.
2. **Regular short practice**: about 12 minutes, 4–6 days a week **[F1.4, F1.5]**.
3. **Keep the error rate low by adjusting the material, not by punishing the child** **[F1.6, F4.4]**.
4. **Move to real words quickly** and practise each letter in many different words **[F1.1, F2.2]**.
5. **Motivation that doesn't backfire.** The child should see their own mastery and get informational feedback. No currency, no sibling leaderboard **[F4.1, F4.2]**.
6. **Honest data for the parent.** Show accuracy, rhythm and hesitation, plus a technique check the software can't do on its own **[F3.2, F5.x]**.

**Non-goals for v1:** maximizing WPM, competitive play, teaching numbers and symbols, or composition/writing skills.

---

## 2. Theme and hook: "Relight the Galaxy"

**Premise.** The Keyboard Galaxy has gone dark. The child is a new pilot on the starship *Home Row*. The crew is **eight finger pilots plus Thumbs, the co-pilot**. Each pilot is colour-coded and in charge of a few stars (keys). Typing letters cleanly relights stars. Steady rhythm makes the ship cruise.

**Why this works for learning:**
- **The galaxy map is the keyboard.** Stars sit in QWERTY positions and are coloured by finger. As the child plays, the main progress screen turns into a mastery heatmap of their own keyboard. The story and the learning measure are the same thing.
- **The finger pilots carry the finger mapping.** Lines like "That's Rio's star: right ring finger!" teach which finger without lecturing.
- **The calm "cruise" metaphor matches the goal.** Smooth, steady rhythm is the target, not panicked bursts. The ship's speed follows a smoothed typing rate. The ship never explodes and nothing is lost.
- It works for both ages. The 4th grader gets characters and stars; the 6th grader gets ship customization, the "Warp Sprint", and stats.

**Deliberately avoided:** falling words or shooting as the core mechanic. It pulls the eyes around the screen and rewards panic, and it tends to hurt accuracy-first technique. That is the ZType/Epistory pattern, which suits fluency practice after the keys are learned **[F6 table]**. A falling-words *review mini-game* is listed for later (§13).

**Screen layout (practice):**
```
┌──────────────────────────────────────────────────────────┐
│  ☆ Mission: Relight the E-star        ⏱ 4:12  ▓▓▓▓░ line 3/6 │
│                                                          │
│        f e e d   [d]e e p   s e e d   f l e d            │  ← current line, ≥32px mono,
│        d e a l   l e a f   j e l l   k e e l            │    current char boxed, typed chars dim
│                                                          │  ← next line faded
│     · ✦ ·  (canvas starfield; ship drifts, speed ∝ rhythm)  │
│  ┌──────────── on-screen keyboard (fades per key) ─────┐ │
│  │  q w [e] r t  y u i o p                              │ │
│  │   a s  d  f g  h j k l ;    (finger colours)         │ │
│  └──────────────────────────────────────────────────────┘ │
└──────────────────────────────────────────────────────────┘
```
- The text line dominates the screen and sits in the upper-middle, so eyes rest near it.
- The on-screen keyboard sits at the bottom, below the text. It is never between the child's eyes and the line being typed.

---

## 3. Session structure (default 12 min; parent can set 8–15)

| # | Segment | Length | What happens | Basis |
|---|---|---|---|---|
| 1 | **Pre-flight check** | ~20 s | Four animated cards, one key press each: feet flat or on a box, sit tall, wrists floating (not resting on the edge), **find the F and J bumps**. A hands-covered tip is shown once a week. | Ergonomics consensus **[F3.4]**; home-row anchor **[F2.1]** |
| 2 | **Warm-up** | ~1 min | 3 lines of words using only "learned" keys, aiming to feel easy. | Success expectancy **[F4.3]** |
| 3 | **New Star** (only when a key pair was unlocked) | ~2 min | Introduce 2 new keys: finger-pilot demo animation → *anchor drill* (keep the home finger down, reach, and return: `fdf frf fff`) → bigrams with known keys → real words. Full hints. | Blocked intro, then mixed **[F1.3]**; TypingClub anchoring **[F6]** |
| 4 | **Missions ×3** | 90–120 s each | Adaptive lines (§6) aimed at the weakest keys, with a short summary card after each. | Weak-key targeting **[F5.2]**, challenge point **[F4.4]** |
| 5 | **Warp Sprint** (stage 6+) | 45–60 s | Mastered keys only, common words, a pacer ghost at the child's median speed +10%, errors don't stop the line. A separate speed score. | Train speed separately with relaxed error limits **[F1.7]** |
| 6 | **Debrief** | ~30 s | The galaxy map animates any stars that got brighter. One process-focused sentence ("Your R-star got 20% quicker — your left index is learning the reach"). The day's beacon lights up. | Informational feedback **[F4.2]** |

- **Soft stop** when the set time is reached: "Great flight! One bonus mission, or dock for today?" At most one bonus round. **Hard stop at 20 minutes.** This uses the spacing finding: more minutes per day is not more efficient **[F1.4]**.
- **Pause** on window blur, and after 10 s with no input ("Paused — hands on F and J when ready").
- **Weekly goal:** 4 of 7 days. There is no fragile streak that resets to zero (a design bet to avoid loss-aversion pressure **[F4.5]**).

---

## 4. Key progression plan

Hybrid order: **home row first** as the physical anchor, then pairs roughly by English letter frequency, **balanced across hands** so real words appear quickly **[F2.1, F2.2]**. Where practical, the order avoids teaching same-finger/opposite-hand pairs together (the Lessenberry "skip-around" advice, second-hand). Exception: e/i come early because they are so frequent, and Dance Mat does the same.

| Stage | New keys | Fingers | Sample real words available | Checkpoint |
|---|---|---|---|---|
| 1 | **f j** + space | L/R index | (letter drills, "fj jf") | |
| 2 | **d k** | L/R middle | (drills, bigrams) | |
| 3 | **s l** | L/R ring | (no vowels yet) drills like `sls dkd` + short pseudo-words | |
| 4 | **a ;** | L/R pinky | lad, sad, fall, flask, salad, dad | |
| 5 | **g h** | L/R index reach | glad, half, shall, flash, gash | ✦ **Home Base** |
| 6 | **e i** | L middle up / R middle up | feel, side, like, shield, field | |
| 7 | **r u** | L/R index up | rule, fire, hurl, safer, ridge | |
| 8 | **t o** | L index up / R ring up | the, that, store, hotel, toast | ✦ **Top Row Rookie** |
| 9 | **n c** | R index down / L middle down | can, nice, chance, ocean | |
| 10 | **m w** | R index down / L ring up | moon, window, swim, warm | |
| 11 | **y b** | R index up / L index down | baby, yellow, brain, yes | |
| 12 | **p v** | R pinky up / L index down | very, apple, vapor, pivot | ✦ **Star Navigator** |
| 13 | **, .** + **Shift** (opposite-hand) | R middle/ring down; pinkies | sentences with capitals | |
| 14 | **x z** | L ring / L pinky down | box, zone, fizz, extra | |
| 15 | **q '** | L pinky up / R pinky | quiz, quest, don't, it's | ✦ **Galaxy Restored** |

- **Checkpoints** are a 1-minute copy test of real kid-level sentences using only unlocked keys. The checkpoint result is recorded for the parent view and the child gets a badge, but it **does not block progress**. Mastery gates (below) already control unlocks. Checkpoints exist to measure transfer to real text.
- **Placement / test-out (optional, mostly for the 6th grader):** a 2-minute diagnostic on the first launch. A stage counts as "already learned" when the child scores ≥94% accuracy at or above that stage's target speed, *and* the parent ticks "uses the right fingers" after watching **[F0.1]**. Hunt-and-peck kids who are already fast should still start at stage 1 to rebuild the finger mapping. Expect them to move through the early stages quickly.
- Numbers, symbols, Tab/Enter drills: later (§13).

### Mastery and unlock rules **(thresholds are design bets, to be tuned in the pilot [F2.3])**
- **Target speed per profile:** `targetWPM = base + 0.75 × stage`, capped at a parent goal.
  - Defaults: 4th grader base 8 (cap 20); 6th grader base 10 (cap 28).
  - These sit inside or slightly above the handwriting-speed ranges and the observed grade 4–5 medians **[F0.2, F5.3]**.
  - `targetIKI_ms = 12000 / targetWPM` (5 chars/word → 60000/(5·WPM)).
- A key is **Learned** (star fully lit) when it has ≥40 graded presses, EWMA first-try accuracy ≥ 0.94, and median IKI ≤ targetIKI.
- A key is **Red** (needs work) if accuracy < 0.90 or median IKI > 1.25 × targetIKI.
- **Unlock the next pair** when both newest keys are Learned **and** no unlocked key is Red. At most **one unlock per session**, which spreads new material across days **[F1.4]**.
- **No re-locking.** A key that decays becomes the focus key again. Losing content feels punitive **[F4.3]**.

---

## 5. Measurement (what the engine records)

All timing uses `performance.now()` on `keydown`.

| Metric | Definition | Notes |
|---|---|---|
| **First-try accuracy** | correct-on-first-attempt ÷ graded positions | The main learning signal. |
| **WPM (net)** | (correct chars ÷ 5) ÷ minutes | Shown to the child only in the Warp Sprint and checkpoints, never as the main score. |
| **IKI per key** | Time from the previous keydown to the correct keydown for this key | **Exclude** the first char of a line and any IKI after a pause >2 s (that's reading or resting, the outer loop **[F1.1]**). |
| **Hesitation** | IKI > max(2000 ms, 3 × the child's overall median IKI) | A proxy for visual search or looking down **[F3.2]**. |
| **Confusions** | Matrix `expected → pressed` for wrong first presses | Classified using Grudin's categories **[F1.6]**. |
| **Bigram IKI** | IKI of key B when preceded by key A (correct both) | Top 200 bigrams kept. |
| **Peeks** | Times the child pressed the "show keyboard" help key | Self-controlled help **[F1.8]**. |

**Input handling details:**
- Use `event.key` for the character and `event.code` for the physical key (finger mapping, keyboard art).
- Ignore `event.repeat`. `preventDefault` on Space, `'`, `/`, Backspace (to stop page navigation) and Tab.
- Detect Caps Lock via `getModifierState('CapsLock')` and show a banner: "Caps Lock is on — tap it off".
- Rollover is normal for skilled typists **[F5.1]**. Grade on keydown order and never require key-up first.
- Non-US layouts: v1 assumes US QWERTY. Detect the mismatch with `event.code` vs `event.key` on the first keystrokes and warn.

---

## 6. Adaptive algorithm

### 6.1 Per-key state (stored per profile)
```js
keyStat = {
  acc: 0.9,          // EWMA of first-try correctness, alpha = 0.1, prior 0.9
  n: 0,              // graded presses (lifetime)
  ikis: [],          // ring buffer, last 30 valid IKIs (ms) → median
  hes: 0, hesN: 0,   // hesitations over last 50 presses (EWMA ok)
  conf: {},          // pressedKey → count (last ~200 errors)
  hintLevel: 3,      // 3..0 scaffolding level (§7)
  firstSeen, lastSeen
}
```

### 6.2 Weakness score (for unlocked keys)
```
accGap   = max(0, 0.96 − acc) / 0.06            // 0 at 96%, 1 at 90%
speedGap = max(0, medianIKI / targetIKI − 1)     // 0 when at/under target
hesRate  = hesitations / presses (last 50)
fewData  = n < 20 ? 0.5 : 0

weakness = 2·accGap + speedGap + 0.5·hesRate + fewData
```
- Accuracy is weighted twice as heavily as speed, matching the technique-and-accuracy-first goal **[F1.6]**. Speed still counts, as in keybr's approach **[F5.2]**.
- **Focus key** = the highest weakness score. **Second focus** = the next one. Ties go to the more recently unlocked key.
- **Weak bigrams** = bigrams with ≥10 samples whose median IKI is >1.4× the median of their two keys' IKIs.

### 6.3 Confusion detection
A pair `expected E → pressed P` becomes a **confusion** when count ≥3 and it makes up ≥5% of E's presses (over the last 200 presses of E). Classify it:

| Type (Grudin 1983) | Example | Likely cause | Response |
|---|---|---|---|
| **Adjacent, same row** | d→f, i→o | Wrong finger chosen or hand drifted | Contrast line: `did fid dif fed` alternating E and P words; finger-pilot reminder "D belongs to Dex (left middle)". |
| **Same finger, other row** | r→v, e→c | Reach direction | Anchor drill: home → up → home (`frf fvf frf`). |
| **Homologous (same finger, other hand)** | e→i, d→k | Mirror confusion | Contrast line mixing words containing each; shows which *hand*. |
| **Other** | — | Spelling/reading | No special drill; counts as a normal error. |

> Contrast drills follow logically from the error research but **have not been tested** as a training method. Label them as experimental in code comments and the parent view **[F1.6]**.

### 6.4 Line generation
Each mission line is **6–8 words**, built from:
- **40%** words containing the focus key
- **15%** words containing the second focus key
- **15%** words containing a weak bigram (or a confusion contrast word, when a confusion is active)
- **30%** review words drawn from all unlocked keys, weighted toward less recently practised keys (light spacing)

**Word source:** a curated, kid-safe list of ~3,000 common English words, embedded in the file and filtered at runtime to words that use only unlocked letters. **No repeated word within a line**, and each word is reused at most twice per mission, so each letter appears in many different words **[F1.1]**.

**Fallback:** when fewer than 8 eligible real words contain the focus key (early stages), generate **pronounceable pseudo-words** using a letter-bigram Markov model trained on the word list, restricted to unlocked letters (as keybr does **[F2.2]**). Filter them against a profanity/near-miss blocklist. Mark them visually (italic) so kids know they're "alien words".

**Themed word packs (autonomy, [F4.3]):** the child picks Space / Animals / Sports / Food. The pack biases word choice only within eligible words. If a pack has too few eligible words, it falls back to the general list.

### 6.5 Difficulty band: aiming for ~92–96% first-try accuracy
Evaluated on a rolling 60-keystroke window after each line:

| Rolling accuracy | Action |
|---|---|
| > 97% for 2 lines | **Harder:** focus density +10% (max 60%), average word length +1 (max 8), the focus key's hint level fades one step sooner. |
| 90–97% | Hold. |
| < 90% | **Easier:** focus density −15% (min 20%), shorter words, hints come back one level for the focus key, insert a "confidence line" (learned keys only). |
| < 80% on a single line | Gentle pause card ("Shake out your hands, find F and J"), then a line of mastered words. |

**Why not 85%?** The "85% rule" comes from machine-learning classification theory. At 85% per keystroke, most 5-letter words would contain an error **[F4.4]**. The lower-error band also follows the errorless-learning evidence for children, which is low certainty **[F1.6]**. **Tune this band from pilot data.**

---

## 7. Feedback and scaffolding (and how it fades)

### 7.1 Every keystroke (never fades)
- **Correct:** the character dims and a soft tick plays (WebAudio, optional). The ship nudges forward.
- **Wrong (default "stop-on-error" mode):** the wrong character is **not inserted**, the target letter flashes amber, and a soft low "bonk" plays. No red screen shake and no lost points. The child just presses the right key.
- This immediate right/wrong signal stays on permanently. It's cheap, clearly useful, and is what the free-web tutor in the Donica study lacked **[F0.3, F1.8]**.

### 7.2 Hint escalation within a key press
1. First wrong press → **no location hint** (let them self-correct by feel).
2. Second consecutive wrong press, *or* a hesitation >2.5 s → the on-screen keyboard highlights the target key in its finger colour, with the finger pilot's name.
3. Third → an animated hand overlay shows the finger reaching from home row.

### 7.3 Per-key fading of the on-screen keyboard **[F3.3, F1.8]**
Each key has `hintLevel` 3→0, driven by its own stats:

| Level | Shown when the next char is this key | Promote when | Demote when |
|---|---|---|---|
| **H3** | Full keyboard, target highlighted in finger colour + finger name | acc ≥ 0.92 and n ≥ 15 | — |
| **H2** | Keyboard visible; highlight only after 1.5 s or an error | acc ≥ 0.94, n ≥ 30, hesRate < 10% | acc < 0.88 |
| **H1** | Only a thin home-row colour strip; full keyboard pops up after 2.5 s or a 2nd error | Learned | acc < 0.90 or hesRate > 15% |
| **H0** | Nothing; keyboard appears only after 2 consecutive errors | — | acc < 0.90 |

- The keyboard panel shows the **minimum hint level needed for the next character**. Once most keys are H0–H1, the panel naturally disappears most of the time.
- **Self-controlled peek:** holding `Tab` (or clicking a "radar" button; Esc is avoided because it exits fullscreen) shows the full keyboard. Peeks are allowed and counted, never penalized. Frequent peeking on a key slows its fade.
- **No-hint "Stealth Missions"** appear once all current keys are ≥H1. A full line runs with the keyboard hidden, which acts as built-in retention testing (no-feedback trials help learning **[F1.8]**).

### 7.4 Backspace correction mode (stage 9+)
One mission per session uses "free typing" mode. Wrong characters *are* inserted, and the child must notice and fix them with Backspace. Correcting errors is a real sub-skill of everyday typing **[F1.6]**. Score accuracy-after-correction separately.

### 7.5 Anti-look-down measures (the software can't see hands, [F3.2])
- **Parent tip in setup:** cover the hands with a light cloth or a box lid for practice. Offer it as "Stealth mode", which kids tend to enjoy.
- **Hesitation tracking** is the proxy measure. A rising hesitation rate on known keys is flagged to the parent.
- **Monthly technique check:** the parent watches 1 minute and rates it on the 5-level scale (Weigelt-Marom & Weintraub, as used by Donica **[F3.1]**). It takes about 2 minutes and is logged in the parent view.
- **Laptop-specific:** draw the keyboard art to match the device (standard laptop vs Chromebook with a Search key in the Caps Lock position, chosen in setup).

### 7.6 Finger map (US QWERTY)
| Finger (pilot name, colour) | Keys |
|---|---|
| L pinky, *Pip*, purple | q a z (+ L Shift, Tab) |
| L ring, *Rae*, blue | w s x |
| L middle, *Dex*, green | e d c |
| L index, *Fen*, orange | r f v t g b |
| R index, *Jet*, orange-red | y h n u j m |
| R middle, *Kit*, green | i k , |
| R ring, *Rio*, blue | o l . |
| R pinky, *Pax*, purple | p ; / ' (+ R Shift, Enter) |
| Thumbs, *Thumbs* (co-pilot), grey | space |

- Use colour **plus a text label and a small pattern** per finger, so colour-blind children aren't left out.
- **Shift rule:** use the opposite-hand Shift. The game grades this using `event.code` (ShiftLeft/ShiftRight) and gives a gentle hint if the same-side Shift is used.

---

## 8. Reward and motivation system

**Principles:** informational, mastery-based, autonomy-supporting. No expected tangible rewards, no currency, no sibling comparison **[F4.1–F4.3]**.

| Mechanic | v1? | Why / guardrails |
|---|---|---|
| **Galaxy map** (stars brighten with each key's mastery) | ✅ core | Visible progress tied to actual skill. It doubles as the heatmap. |
| **Per-line feedback card** ("Clean line! 96% · smooth rhythm") | ✅ | Informational feedback on the process. |
| **Personal bests**: "Smoothest line" (lowest IKI variability at ≥95%), best checkpoint, best Warp Sprint | ✅ | Self-referenced, not social. |
| **Stage milestones** unlock small cosmetics (ship paint, trail, crew hat) | ✅ small | Unexpected, symbolic, and tied to mastery, which is less undermining than expected, performance-contingent tangible rewards **[F4.2]**. No shop. |
| **Daily beacon / weekly 4-of-7 goal** | ✅ | Encourages spacing **[F1.4]**. Missing a day costs nothing. |
| **Choice:** ship name and colour, word pack, choice of 2 missions when possible | ✅ | Autonomy support **[F4.3]**. |
| **Family Fleet meter** (both kids' clean lines fill one shared meter → a shared cosmetic, e.g., a new constellation) | ✅ optional, parent toggle | Collaboration without head-to-head comparison **[F4.1]**. The meter counts *effort units* (clean lines), never speed. |
| Coins/currency, shop, loot boxes | ❌ | Extrinsic-reward risk **[F4.2]**. |
| Sibling leaderboard / WPM ranking | ❌ | Unfair across ages, discourages the younger one; Hanus & Fox pattern **[F4.2]**. |
| Lives / failure states / timers that end a mission | ❌ | Rewards panic and hurts the low-error goal. |
| Daily streak that resets | ❌ | Replaced by the forgiving weekly goal (design bet). |

**Copy guidelines (design bet):** praise strategy and effort ("you kept your eyes up that whole line"), never "you're a natural". Tone: friendly crew radio chatter, 1 sentence max, skippable.

**Parent guidance shown in the parent view:** "Avoid paying or trading screen time per lesson. If you want to celebrate, do it occasionally and unexpectedly, and talk about what improved." **[F4.2]**

---

## 9. Kid profiles

- Up to **4 profiles** (2 by default). The launch screen shows big ship cards with names, so it's one click to start.
- Each profile has: name, avatar/ship, grade band (sets base target WPM), parent goal WPM cap, session length, sound on/off, word pack, device keyboard style, reduced-motion and high-contrast options.
- **No passwords for kids.** Siblings *could* open each other's profiles. An optional per-profile 4-digit "hangar code" is offered if that becomes a problem.
- Each profile's data is completely separate (separate storage key, §11).

---

## 10. Parent progress view

**Access:** press and hold the gear icon for 3 seconds, or an optional parent PIN. This is friction, not real security; say so in the UI.

**Per child, one screen:**
1. **Summary strip:** days practised this week (n/7), total minutes this month, current stage, last checkpoint WPM and accuracy.
2. **Trends (sparklines, last 30 sessions):** first-try accuracy, Warp Sprint WPM, median IKI, hesitation rate, peek count.
3. **Keyboard heatmap:** each key coloured by status (locked / red / learning / learned), with a toggle between accuracy and speed.
4. **Top 5 weak keys** in plain language: "**R** — 89% accurate, slower than target; often typed as **T** (neighbouring key → likely using the wrong finger). The game is giving extra R/T practice."
5. **Confusion pairs**, classified by type with a one-line explanation. Contrast drills are marked as experimental.
6. **Checkpoint history:** a table of 1-minute tests (date, net WPM, accuracy) compared against grade reference ranges, with a caveat that the ranges are rough **[F0.2, F5.3]**.
7. **Technique log:** a monthly "watch 1 minute and rate 1–5" form with a notes field and a reminder when one is due **[F3.1]**.
8. **Rule-based suggestions** (simple if-thens), for example:
   - hesitation rate rising for 3 sessions → "Your child may be looking down; try Stealth mode with a cloth over the hands."
   - accuracy <90% for 3 sessions → "Shorter sessions or slower pace this week; the game has already eased off."
   - <3 days/week for 2 weeks → "Short and frequent beats long and rare."
9. **Settings:** session length (8–15), goal WPM cap, Family Fleet on/off, sound, PIN, reset a profile (with a typed confirmation).
10. **Backup:** "Download progress" (a JSON file of all profiles), "Restore from file", and a **copy-paste backup code** (compressed base64 of the JSON) for devices that block downloads.

---

## 11. Storage and data model

- **localStorage keys:**
  - `keyquest:v1:index` → `{ schema: 1, profiles: [{id, name, ship, createdAt}], parentPinHash?, settings }`
  - `keyquest:v1:p:<id>` → the profile document below.
- Store **aggregates only**, no raw keystroke logs, and keep the size under ~200 KB per profile.
```js
profile = {
  schema: 1, id, name, gradeBand, settings: {...},
  stage, unlockedKeys: "fjdksla;gh...",
  keys: { "f": keyStat, ... },
  bigrams: { "th": {ikis:[...], n} },      // top 200 by count
  sessions: [ {date, mins, lines, acc, wpmSprint, medIKI, hesRate, peeks, unlocked:"ei"} ], // last 365
  checkpoints: [ {date, stage, netWPM, acc} ],
  technique: [ {date, level, note} ],
  cosmetics: [...], personalBests: {...}, fleetContribution: n
}
```
- **Save** after every line, on the debrief, and on `visibilitychange → hidden`.
- **Migrations:** a `schema` number with a `migrate(doc)` function.
- **Failure handling:** wrap storage calls in try/catch. If storage is unavailable (private mode, blocked), show a persistent banner: "Progress won't be saved on this device. Use Download progress at the end."
- **Caveats to state in the UI or README:** clearing browser data wipes progress. Under `file://`, all local HTML files share one storage area, which is why the keys are namespaced **[F7.2]**. Some managed Chromebooks wipe local data at sign-out **[F7.3]**. Hence backup codes.

---

## 12. Technical architecture (single file)

- **One `starkeys.html`**, with vanilla JS and CSS inline, **no network requests**, no external fonts (system monospace for the text line), and no analytics.
- **Rendering:** DOM for the text line and the on-screen keyboard (crisp, accessible, easy to style). One `<canvas>` behind them for the starfield and ship, using `requestAnimationFrame`, capped work, and paused when hidden.
- **Audio:** WebAudio oscillators for tick/bonk/chime. No audio files. A mute toggle.
- **Accessibility:** `prefers-reduced-motion` support plus a manual toggle that freezes the starfield; a high-contrast theme; minimum 32 px text line, scalable; finger identity shown by colour **and** label.
- **Modules** (inside the file, as IIFEs or classes): `Input`, `Stats`, `Adaptive`, `LineGen` (word list + Markov), `Hints`, `Session`, `Progression`, `Storage`, `UI` (screens: launch, pre-flight, practice, debrief, galaxy map, parent), `Theme`.
- **Embedded data:** ~3k-word list (~25 KB), a blocklist, the finger map, and keyboard layouts (laptop / Chromebook).
- **Target size:** under ~250 KB. It must run on a low-end Chromebook at 60 fps (the canvas starfield is the only animation).
- **Deployment options, in order of reliability:**
  1. Home computer or personal device: open the file directly (`file://`).
  2. If school Chromebooks matter: host the single file on a static host the school allows, or ask IT to allowlist it. Managed devices may block `file://` and filter unknown sites **[F7.1]**. Respect school acceptable-use rules.
  3. Later: a PWA with a service worker for offline use when hosted.

---

## 13. Version 1 scope

**In v1:**
- Stages 1–15 (letters, space, comma, period, apostrophe, Shift); semicolon is on home row.
- Pre-flight, warm-up, New Star lesson, 3 adaptive missions, Warp Sprint, debrief.
- Per-key stats, weakness score, confusion detection (with experimental contrast lines), bigram tracking.
- Real-word line generation, Markov pseudo-word fallback, 4 word packs.
- Difficulty band controller, hint escalation, per-key scaffolding fade, peek, Stealth Missions, backspace mode.
- Galaxy map, cosmetics at milestones, personal bests, weekly goal, optional Family Fleet.
- Profiles (2–4), parent view, backup/restore (file + code), placement test, checkpoints.
- Sound, reduced motion, high contrast, laptop/Chromebook keyboard art.

**Later (v2+):**
- Number row and symbols; Enter/Tab; capital-letter-heavy text.
- Composition prompts ("type your answer") to bridge copying and writing. Copying speed overstates composing speed (Logan 2016 anecdote **[F0.1]**).
- Dictation mode (spoken words via speechSynthesis) to train the outer loop without visual copying.
- A ZType-style review mini-game for fluency, unlocked only for mastered keys.
- More themes and skins; seasonal word packs.
- PWA, optional sync across devices, a teacher/class mode.
- Other layouts (UK, Dvorak, Colemak) and other languages.
- Longer stamina tests (3–5 min), and page-length goals tied to Common Core W.4.6/W.6.6.
- Smarter scheduling (spaced review of keys not seen in N days), Bayesian estimates of key skill.

---

## 14. Build plan and evaluation

| Milestone | Deliverable | Est. effort |
|---|---|---|
| M1 Engine | Input capture, line display, stop-on-error, stats, WPM/accuracy/IKI | 1–2 days |
| M2 Progression + hints | Stages, mastery/unlock, line generator, difficulty band, hint levels | 2–3 days |
| M3 Profiles + storage | Profile picker, save/load, migrations, backup/restore | 1 day |
| M4 Theme | Starfield, ship, galaxy map, crew, sounds, cosmetics | 2–3 days |
| M5 Parent view | Trends, heatmap, weak keys, technique log, suggestions | 1–2 days |
| M6 Pilot (2 weeks) | Both kids play; check thresholds; adjust | 2 weeks |

**Pilot checks (tune these from data):**
- Is rolling accuracy actually sitting in the 90–97% band? Do lines feel too easy or too hard? (Ask the kids.)
- Pace of unlocks: aim for roughly 1 pair every 2–4 sessions. If it's much faster, tighten the thresholds; if slower, loosen them.
- Are hints fading? Is the peek count dropping?
- Session completion: are they finishing 12 minutes without fatigue?

**Evaluating whether it works (the parent's own small-n check):**
- **Baseline before starting:** a 1-minute copy test on unfamiliar text (any free test, or the game's checkpoint), plus a technique rating 1–5.
- **Monthly:** the same test and technique rating. Track net WPM, accuracy, and technique level. Technique level should rise first; WPM may dip temporarily while hunt-and-peck habits are replaced **[F0.1]**.
- **Realistic expectations:** ~12 min × 5 days ≈ 1 hour a week. Expert opinion suggests roughly 30+ hours to fluent alphabetic typing for young students **[F5.3]**, so expect **several months** for the full alphabet at comfortable speed. A good medium-term target is "faster than handwriting" (roughly the low-to-mid teens WPM for these grades) with technique level 5.

---

## 15. Open design questions (to resolve with the parent)

1. **Device:** home computer or a personal device, or a school-managed Chromebook? This decides whether `file://` works, whether data persists, and whether hosting is needed.
2. **Starting point:** can either child already type, and how (hunt-and-peck, partial touch typing)? Has the 6th grader had school typing classes? (Run the baseline test.)
3. **Sibling setup:** Family Fleet (cooperative) on or off? Separate rooms or times to avoid comparison?
4. **Targets:** "faster than handwriting" first, or set WPM caps from the Common Core page counts?
5. **Theme:** is space a hit with both kids? Should each pick a skin?
6. **Sound:** on by default?
7. **Outside rewards:** any plans? (Recommend no per-lesson payment or screen-time deals.)
8. **Learning differences:** any dyslexia, coordination or handwriting difficulties? (Would change pacing, fonts, and maybe word lists.)
9. **Parent PIN:** wanted?
10. **Technique checks:** willing to do a 2-minute monthly technique check, and to use a cloth or keyboard cover?
