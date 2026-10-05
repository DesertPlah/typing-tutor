# Teaching 9–12-year-olds to touch-type: what the evidence says

*Research brief for a browser-based typing-tutor game for a 4th grader and a 6th grader. Compiled Oct 4, 2026.*

## How to read this

Each finding gives **what the evidence says**, **sources** (with URLs), and a **confidence** rating:

| Rating | Meaning |
|---|---|
| **High** | Several well-designed studies or very large datasets agree, and they are about typing directly. |
| **Moderate** | Decent evidence, but indirect (adults instead of kids, other motor tasks instead of typing) or resting on one good study. |
| **Low** | Small, old, conflicting, or second-hand studies, or a reasonable extrapolation. |
| **Very low / practice wisdom** | Expert opinion, vendor claims, or common teaching practice with no controlled data that I could find. |

"Second-hand" means I could only read a summary of the study inside another paper, not the original. Vendor and marketing claims are labelled as such.

**The honest headline:** almost no rigorous experiments test *how to teach children touch typing*. The strong evidence is about (a) how skilled adult typing works, (b) general motor-learning principles, mostly from adults and sports tasks, and (c) motivation research. Child-specific keyboarding studies exist, but they are mostly quasi-experimental, use unvalidated measures, and some have conflicts of interest. The design should treat many choices as **reasonable bets to tune with your kids' own data**, not settled science.

---

## 0. Is touch typing worth teaching at all?

### F0.1 Self-taught typists can be fast, but consistent finger-to-key mapping and keeping eyes off the keyboard are what predict speed
- **Evidence:** Feit, Weir & Oulasvirta (CHI 2016) used motion capture on 30 everyday typists (34–79 WPM). Some self-taught typists using only 1–2 fingers per hand topped 70 WPM. The three predictors of high performance were (1) **unambiguous finger-to-key mapping** (the same finger always presses the same key), (2) **preparing the next keystroke** while finishing the current one, and (3) **little whole-hand movement**. Self-taught typists looked at the keyboard more. The authors say touch typing is still the best known route to very high speed.
- Logan, Ulrich & Lindsey (2016, n=48): standard touch typists averaged 80 WPM and non-standard typists 72 WPM. When the keyboard was hidden, the non-standard typists slowed down and made more errors, while the touch typists held steady. 14 of the 24 people who called themselves touch typists actually weren't.
- Pinet et al. (2022, n=1,301 university students, preregistered): the most proficient typists used more fingers and **looked at the keyboard much less**. Looking at the keyboard was the biggest habit difference between groups. Whether people did "deliberate practice" did not differ between groups. Total typing volume did differ.
- Dhakal et al. (CHI 2018, 136M keystrokes from ~168,000 people): more fingers and more hand/finger alternation went with faster typing. Faster typists made fewer errors.
- **Sources:** https://dl.acm.org/doi/10.1145/2858036.2858233 · http://darylweir.com/assets/howwetype.pdf · https://userinterfaces.aalto.fi/how-we-type/ · https://news.vanderbilt.edu/2016/10/18/todays-self-taught-typists-almost-as-fast-as-touch-typistsas-long-as-they-can-see-the-keyboard/ · http://www.psy.vanderbilt.edu/faculty/logan/LoganUlrichLindsey2016.pdf · https://pmc.ncbi.nlm.nih.gov/articles/PMC9356123/ · https://userinterfaces.aalto.fi/136Mkeystrokes/
- **Confidence: High** that consistent mapping and eyes-up typing go with skill in adults. **Moderate** that teaching the full ten-finger system is the best way to get there for kids. Logan himself questioned whether early school training pays off.
- **Design implication:** The real goals are **(1) the same finger for the same key, every time** and **(2) eyes on the screen**. Ten-finger touch typing is the standard, proven way to get both. The game should reward consistency and eyes-up typing more than raw WPM.

### F0.2 For kids, slow typing hurts their writing, so fluency matters
- **Evidence:** Connelly, Gee & Walsh (2007) studied primary-school children in the UK. Most typed more slowly than they wrote by hand, and their typed compositions were rated lower in quality than their handwritten ones (keyboarded work lagged up to about two years developmentally). Typing fluency was linked to composition quality. The authors concluded that children need explicit touch-typing instruction to benefit from word processing.
- Common Core W.4.6 (verified) asks 4th graders to "demonstrate sufficient command of keyboarding skills to type a minimum of one page in a single sitting". Per the TypingClub handbook's summary, Grade 5 asks for two pages and Grade 6 for three.
- A common benchmark is "type at least as fast as you handwrite". Per Donica et al. 2021, citing the Freeman et al. 2005 synthesis, handwriting-speed ranges are about 6.8–16.4 WPM for grade 4 and 7.6–16.6 for grade 5.
- **Sources:** https://pubmed.ncbi.nlm.nih.gov/17504558/ · https://www.thecorestandards.org/ELA-Literacy/W/4/ · https://static.typingclub.com/m/corp2/other/typingclub-teacher-handbook.pdf · https://scholarworks.wmich.edu/cgi/viewcontent.cgi?article=1819&context=ojot
- **Confidence: Moderate.** The link between transcription fluency and writing quality is well established. The benchmarks are rough.

### F0.3 Structured instruction beats unstructured typing games for kids (one quasi-experiment, with a conflict of interest)
- **Evidence:** Donica, Giroux, Kim & Branson (2021) compared 1,306 students in grades 1–5 over 2 years. One group used Keyboarding Without Tears (KWT, a structured curriculum) both years. The other used free web activities (PBS Kids games, a basic online tutor) in year 1 and then KWT. Both groups improved. KWT did better on net WPM in grades 2–4 and on technique in every grade. **At the end, 4th graders' median net WPM was about 11–13, and 5th graders' about 14–17.** Big caveats: not randomized; a single 30–60-minute computer class once a week for up to 27–31 weeks a year, with minutes actually spent on keyboarding not tracked; unvalidated measures; one KWT teacher also handed out stamps and tokens for using the home row, which confounds the comparison; and **the first two authors work part-time for the KWT publisher, which also funded the study.** The free-web tutor "did not provide feedback when a participant misspelled a word or pushed keys incorrectly."
- **Source:** https://scholarworks.wmich.edu/cgi/viewcontent.cgi?article=1819&context=ojot
- **Confidence: Low–moderate** that structured, technique-focused instruction beats unstructured games. The WPM figures are useful as **realistic expectations**: low teens for a trained 4th grader.

---

## 1. Motor learning applied to typing

### F1.1 Skilled typing runs as two loops: words go in, and the fingers handle the letters on their own (chunking)
- **Evidence:** Logan & Crump's two-loop theory. An **outer loop** produces words and checks the screen. An **inner loop** turns each word into keystrokes using feedback from the fingers and keyboard. Each loop knows little about the other. Skilled typists slow down when told to watch their hands. Word-level units activate their letters in parallel (Crump & Logan 2010).
- Skill tracks the statistics of the language. Behmer & Crump (2016, ~400 typists): novices are most sensitive to **letter** frequency, while skilled typists are more sensitive to **bigram/trigram** frequency.
- Yamaguchi & Logan (2014) moved one key to a new location. Relearning that key depended on letter, bigram, **and word-level units, and on the letters before *and after* the key.**
- **Sources:** https://www.crumplab.com/publications/Crump/files/3898/Logan%20and%20Crump%20-%202011%20-%20Hierarchical%20control%20of%20cognitive%20processes%20The%20c.pdf · http://www.psy.vanderbilt.edu/faculty/logan/Crump%20Logan%20JEPLMC2010.pdf · https://www.crumplab.com/publications/Crump/files/4991/Behmer%20and%20Crump%20-%202017%20-%20Crunching%20big%20data%20with%20finger%20tips%20How%20typists%20t.pdf · https://research.edgehill.ac.uk/en/publications/pushing-typists-back-on-the-learning-curve-contributions-of-multi-2/
- **Confidence: High** for how adult skill is organized. **Moderate** for what it implies about training.
- **Design implication:** Move from single letters to **real words and common letter clusters (th, he, in, er, an…) as fast as possible**. Practise each letter in **many different word contexts**, not the same drill string over and over.

### F1.2 The shift from looking to feeling: typists learn key positions implicitly, so drilling the keyboard map is the wrong target
- **Evidence:** Snyder et al. (2014): skilled typists (~72 WPM) placed only about **15 of 26** letters correctly on a blank keyboard. After learning Dvorak, their explicit knowledge of that layout was no better. Key-location knowledge seems to be **procedural, never consciously memorized**. Liu, Crump & Logan (2010) found the same thing for relative key directions.
- Tapp & Logan (2011): typists use vision to monitor their hands, and covering the hands makes some tasks harder. Under normal conditions, though, skilled control relies on touch and proprioception, and vision watches the screen (see the discussion in Pinet 2022).
- Non-standard typists depend on seeing the keyboard (Logan 2016, F0.1). Fitts & Posner's cognitive → associative → autonomous stages are the usual framework in the child-keyboarding literature (Donica 2021).
- **Sources:** https://link.springer.com/article/10.3758/s13414-013-0548-4 · https://news.vanderbilt.edu/2013/12/04/automatic-typing/ · http://www.psy.vanderbilt.edu/faculty/logan/2011Tapp_Logan_APP.pdf
- **Confidence: High** (adult typists, several studies).
- **Design implication:** Don't build "memorize where the keys are" quizzes. Build **lots of eyes-up practice with immediate feedback**, so finger-to-key links form through repetition. Visual keyboard aids are crutches for the earliest stage and should fade (see §3).

### F1.3 Blocked vs. interleaved practice: the "interleave for retention" effect is weak or absent in children
- **Evidence:** Contextual-interference research says random or interleaved practice hurts performance during practice but helps retention and transfer, at least in adult lab tasks. For **children**:
  - Graser et al. (2019 systematic review, 25 studies of typically developing children) found study quality was low and evidence was mostly "no or conflicting". There was limited evidence that **blocked practice is better during acquisition** for several tasks, and limited-to-moderate evidence that random practice helps retention or transfer for a few (including **handwriting** transfer).
  - Czyż et al. (2024 meta-analysis, transfer outcomes): medium overall effect favoring random practice (SMD 0.55). In **young participants (<18)** the effect was **negligible (SMD 0.12, not significant)**, and in applied, real-world settings it was small and not significant.
- **Sources:** https://journals.plos.org/plosone/article?id=10.1371%2Fjournal.pone.0209979 · https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2024.1377122/full
- **Confidence: Moderate** that heavy interleaving won't give kids a big boost. **Low** for any specific schedule.
- **Design implication:** Use a **blocked introduction** for a brand-new key (short and focused), then **move quickly to mixed practice**: new keys woven into words with old keys. That is what typing requires anyway. Mixed practice is justified by transfer to real text, not by the CI effect.

### F1.4 Spacing: shorter, distributed sessions beat massed practice, including for learning a keyboard
- **Evidence:** Baddeley & Longman (1978) trained postmen on a keyboard with four schedules. **One 1-hour session per day** was the most efficient. **Two 2-hour sessions per day** was the worst for speed and accuracy, even with more total hours. Retention loss after 1–9 months was about 30%. Cepeda et al. (2006, 317 experiments, verbal learning) confirmed the spacing benefit, including in children.
- **Session length for kids:** I found **no controlled study** of the best keyboarding session length for 9–12-year-olds. Practitioners recommend "little and often" (BBC Teach; Bartholome: start short and build stamina; his elementary model is about 30 minutes, 3 days a week).
- **Sleep-consolidation claims** (common in typing apps' marketing, e.g., ZType, BBC) are **contested**. Pan & Rickard's (2015) meta-analysis found that apparent sleep gains in motor learning were largely explained by confounds. Children's sleep effects are inconsistent.
- **Sources:** https://www.tandfonline.com/doi/abs/10.1080/00140137808931764 (PDF: https://gwern.net/doc/psychology/spaced-repetition/1978-baddeley.pdf) · https://pubmed.ncbi.nlm.nih.gov/16719566/ · https://www.bbc.co.uk/teach/articles/ztj9h4j · http://files.keyboardingonline.com/support-files/59026fd9abbd1-Keyboarding%20Instruction%20in%20Elementary%20Schools%20-%20Llyod%20W.%20Bartholome.pdf · https://rickardlab.ucsd.edu/pdf/PR_2015.pdf
- **Confidence: High** that distributed beats massed. **Very low** for any specific number of minutes for kids. A 10–15-minute daily session is a sensible bet based on attention span and practice wisdom, not data.
- **Design implication:** Default to about **12 minutes a day, 4–6 days a week**. Discourage marathons with a soft stop. Reward *days practised*, not hours.

### F1.5 Deliberate practice: total practice volume clearly matters, while the case for "deliberate" practice is mixed
- **Evidence:** Keith & Ericsson (2007, as summarized in Pinet 2022) found that deliberate practice with a goal of typing faster predicted skill in 60 intermediate typists. Pinet (2022, n=1,301) found **no** link with self-reported deliberate practice, and a clear link with daily typing time and years typing. Macnamara et al. (2014, cited in Pinet) found that deliberate practice explains only a modest share of skill differences across domains.
- **Source:** https://pmc.ncbi.nlm.nih.gov/articles/PMC9356123/
- **Confidence: Moderate** that volume and regularity are the big levers. **Low** for the extra value of "deliberate" targeting. Targeting weak keys is still sensible: it's cheap and keeps practice at the edge of skill.
- **Design implication:** The most important job of the game is to **get kids to practise regularly** with correct technique. Weak-key targeting is a bonus layered on top.

### F1.6 Errors: keeping error rates low during early practice helps children's accuracy (low-certainty evidence); correcting errors is itself a skill
- **Evidence:** Wong et al. (2026 meta-analysis, 29 studies on errorless motor learning) found no overall advantage for movement performance. They did find a moderate accuracy benefit **in children (g = 0.657)** and in learners with impairments. GRADE certainty was low to very low. Errorless learning means easy-to-hard progression that keeps early errors rare, not banning errors.
- Crump & Logan (2013, cited in Pinet 2022): modern typists develop automatic error-correction routines (backspacing), so correcting is a learned sub-skill.
- Grudin (1983) on error types: substitution errors are mostly **adjacent keys** (59% of novice substitutions were same-row neighbours). **Homologous** errors (same finger, other hand) were 16% for novices and 4% for experts. Video showed adjacent errors usually came from the finger that normally owns the wrong key, meaning the wrong finger was chosen.
- **Sources:** https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2026.1722743/full · https://gwern.net/doc/design/typography/1983-grudin.pdf · https://pmc.ncbi.nlm.nih.gov/articles/PMC9356123/
- **Confidence: Low** (errorless for kids) and **Moderate** (error-type patterns).
- **Design implication:** Control error rates by **making the material easier or harder, not by punishing errors**. Classify errors (adjacent, homologous, wrong row) to diagnose finger confusions. Teach backspace correction later as its own skill.

### F1.7 "Accuracy before speed": not well supported as usually stated
- **Evidence:** The classic typewriting research says otherwise. Leonard J. West's *Acquisition of Typewriting Skills* (1969) reportedly found, across studies of more than 5,000 typists, a **near-zero correlation between speed and errors** in straight-copy typing. He recommended practising speed (with generous error limits) and accuracy **separately**, warning that high accuracy standards during speed practice defeat its purpose. Dufrain (1945): high-school students taught speed-first reached higher speeds with **equal accuracy** to an accuracy-first group. Both are **second-hand**, via a 1980 master's thesis (Coleman), which itself found a mixed result for removing error penalties. Bartholome (practitioner) reports that the "perfect copy" standard was abandoned in the 1920s in favour of "technique and appropriate speed first, accuracy once responses are automated".
- Modern lab work: skilled typists do trade speed for accuracy, mostly inside the inner loop (Yamaguchi, Crump & Logan 2013). Faster typists make fewer errors overall (Dhakal 2018).
- **Sources:** https://digitalcommons.odu.edu/cgi/viewcontent.cgi?article=1503&context=ots_masters_projects · http://files.keyboardingonline.com/support-files/59026fd9abbd1-Keyboarding%20Instruction%20in%20Elementary%20Schools%20-%20Llyod%20W.%20Bartholome.pdf · https://www.crumplab.com/publications/Crump/files/13701/Yamaguchi%20et%20al.%20-%202013%20-%20Speed%E2%80%93accuracy%20trade-off%20in%20skilled%20typewriting%20D.pdf · https://userinterfaces.aalto.fi/136Mkeystrokes/
- **Confidence: Low.** The research is old, second-hand, and from teens and adults on typewriters. Still, it clearly does *not* support "never move on until 100% accurate".
- **Design implication:** Use **"technique and smoothness first"**: correct finger, eyes up, steady rhythm. Keep error rates moderate through difficulty adaptation (F4.4). Add **short, separate speed bursts** with relaxed error tolerance once keys are learned. Never use rigid error penalties that make kids freeze.

### F1.8 Feedback frequency: immediate feedback helps early learning, and "fade it" is plausible but not proven
- **Evidence:** The guidance hypothesis (Salmoni, Schmidt & Walter 1984 and later work) says constant augmented feedback helps practice performance but can create dependence. A 2022 meta-analysis of reduced feedback frequency (Psychology of Sport and Exercise) reportedly found **no significant overall benefit** for reducing it. I only saw the abstract-level summary because the full text was blocked. For children, a PLOS One systematic review (2022) reportedly gives moderate support to **self-controlled feedback** (the learner chooses when to get help). That is also from the search summary.
- Sigrist, Rauter, Riener & Wolf (2012, *Psychonomic Bulletin & Review*, review of augmented feedback) is more nuanced. Concurrent feedback tends to hurt retention in *simple* lab tasks, but it often helps in *complex* tasks and **early learning**. Their recommendation is to use guidance early, then reduce its frequency as skill grows (fading). They also review evidence that **self-controlled feedback** and including some **no-feedback trials** help learning. Most of the evidence comes from adults and non-typing tasks.
- **Sources:** https://link.springer.com/article/10.3758/s13423-012-0333-8 (Sigrist et al. 2012) · https://www.sciencedirect.com/science/article/abs/pii/S1469029222000334 · https://journals.plos.org/plosone/article?id=10.1371%2Fjournal.pone.0264873
- **Confidence: Low.**
- **Design implication:** Keep **immediate correctness feedback** on every keystroke (cheap and clearly useful). **Fade the "where is the key / which finger" guidance**, not the right/wrong signal. Let kids summon help themselves (self-controlled), and log it.

---

## 2. Key introduction order, pace, words vs. drills, n-grams

### F2.1 No controlled study compares home-row-first with frequency-first key orders
- **Evidence:** I found no head-to-head experiment. What exists:
  - **Home row first is near-universal in kids' curricula.** Dance Mat Typing (BBC): home row, then e/i, r/u, t/y, w/o, q/p, v/m, b/n, c/comma, x/z/apostrophe, slash/period, then shift. TypingClub starts with F and J (the bumps).
  - **Frequency-first** is keybr's approach. It starts with E N I T R L, adds the next letter only when all current letters are fast enough, and always generates pronounceable words.
  - The **"skip-around"** method, attributed to D.D. Lessenberry's research (second-hand, via Bartholome): home keys first, then keys introduced in mixed order, **avoiding same-finger/opposite-hand pairs (e.g., e and i) in the same lesson**. Note that Dance Mat does introduce e/i together, so practice varies.
  - The home row's main role is **physical**: an anchor the fingers return to, findable by touch through the F/J bumps.
- **Sources:** https://www.bbc.co.uk/bitesize/articles/z3c6tfr · https://static.typingclub.com/m/corp2/other/typingclub-teacher-handbook.pdf · https://www.keybr.com/help · http://files.keyboardingonline.com/support-files/59026fd9abbd1-Keyboarding%20Instruction%20in%20Elementary%20Schools%20-%20Llyod%20W.%20Bartholome.pdf
- **Confidence: Very low** that any particular order is better.
- **Design implication:** Use a **hybrid**: home row first for the physical anchor, then add letters roughly **by English frequency**, paired one per hand where possible, so real words appear quickly.

### F2.2 Real words beat jumbled letters (one small but direct study)
- **Evidence:** DeFulio et al. (2011, JABA). Adult novice typists reached fluency in nearly half the time when practising real words instead of matched jumbled-character strings. Peak correct rates were higher, and estimated training time was cut by up to 35%. keybr's pronounceable pseudo-words and the n-gram evidence (F1.1) point the same way.
- **Sources:** https://salemstate.elsevierpure.com/en/publications/using-words-instead-of-jumbled-characters-as-stimuli-in-keyboard-/ (DOI 10.1901/jaba.2011.44-921) · https://www.keybr.com/help
- **Confidence: Moderate** (small study, adults, direct comparison, consistent with theory).
- **Design implication:** Get to words fast. When few real words are possible with the letters unlocked so far, use **pronounceable pseudo-words** generated from English letter statistics, not random strings.

### F2.3 How fast to add keys: no evidence-based number, so use mastery criteria
- **Evidence:** No study gives a rate. keybr unlocks a letter when every current letter meets a speed target. TypingClub gates on per-lesson WPM and accuracy minimums (lesson 1 defaults to a minimum of 3 WPM and a goal of 8). Practitioners warn that "if students move through the material too quickly they tend to fall back to poor habits" (Bartholome).
- **Sources:** https://www.keybr.com/help · https://static.typingclub.com/m/corp2/other/typingclub-teacher-handbook.pdf
- **Confidence: Very low** for any specific threshold.
- **Design implication:** Gate on **per-key accuracy, speed, and minimum exposure**, cap unlocks at **one key pair per session**, and tune thresholds from pilot data.

### F2.4 Bigram/trigram training: plausible, with indirect support
- **Evidence:** Skill means growing sensitivity to bigrams and trigrams (Behmer & Crump). Bigram frequency and hand alternation affect inter-key intervals in both stronger and weaker typists (Pinet 2022). Letter pairs typed by different hands or fingers predict speed better than letter repetitions (Dhakal 2018). I found no training study on explicit bigram drills for kids.
- **Confidence: Low** for explicit bigram drills. **Moderate** that practising high-frequency real words naturally trains the right n-grams.
- **Design implication:** Track bigram timings, then **bias word choice toward words containing slow bigrams**, rather than drilling "th th th".

---

## 3. Preventing hunt-and-peck and keyboard-gazing

### F3.1 Emphasizing technique produces better technique
- **Evidence:** In Donica 2021 the KWT group, whose program "strongly emphasize[s] using proper keyboarding technique through visual reminders", scored one to two technique levels higher. Technique was rated on the 5-level scale from Weigelt-Marom & Weintraub (2015), where level 5 means all fingers while looking at the monitor. The KWT teacher for the lower grades also reinforced home-row use. (Conflict of interest noted in F0.3.)
- **Source:** https://scholarworks.wmich.edu/cgi/viewcontent.cgi?article=1819&context=ojot
- **Confidence: Low–moderate.**

### F3.2 Covering the hands: common advice, untested in kids as far as I found
- **Evidence:** BBC Teach: "The best way to make sure that you don't look at their hands is to cover them up." TypingClub sells keyboard covers. Covering takes away the visual guidance non-standard typists rely on (Logan 2016), which is the point. I found no controlled study of covers with children.
- **Sources:** https://www.bbc.co.uk/teach/articles/ztj9h4j · https://static.typingclub.com/m/corp2/other/typingclub-teacher-handbook.pdf
- **Confidence: Very low / practice wisdom.** Low risk and free (a dish towel works).
- **Design implication:** The game **cannot see hands or fingers**. That is a major limitation for any software tutor, and Bartholome makes the same point. Use parent spot-checks, a cover tip, and **hesitation detection** (unusually long pauses before a key suggest visual searching) as a proxy.

### F3.3 On-screen keyboards and finger color maps: universal in tools, little direct evidence, and they should fade
- **Evidence:** Every major tutor shows a color-coded keyboard and hands. Logan's lab used exactly this kind of color map to classify typists. I found no study measuring its effect for children. The guidance hypothesis (F1.8) suggests constant visual guidance could become a crutch, since the eyes go to the on-screen keyboard instead of the real one.
- **Confidence: Low.**
- **Design implication:** Show the full on-screen keyboard and finger colours **for new keys only**. Fade it **per key** as that key is mastered, and bring it back on errors or long hesitations.

### F3.4 Posture and ergonomics for kids: guidelines from expert consensus
- **Evidence:** Cornell's guidelines for children: neutral posture, feet supported (floor or footrest), knee angle above 90°, upper arms relaxed close to the body, **wrists neutral (<15°)**, screen at a height that avoids tilting the neck, smaller keyboards for small hands, and time-limited use with breaks. Cornell laptop tips: for use over about an hour, raise the screen and use an external keyboard. Short sessions on a laptop are fine.
- **Sources:** https://www.ergo.human.cornell.edu/cuweguideline.htm · https://ergo.human.cornell.edu/culaptoptips.html
- **Confidence: Moderate** as consensus guidance. Low for injury prevention in short sessions specifically.
- **Design implication:** A 20-second **"pre-flight check"** before each session (feet, back, wrists floating, find the F/J bumps) and a break nudge at 15 minutes.

---

## 4. Motivation and game mechanics

### F4.1 Gamification helps learning modestly and depends on the details
- **Evidence:** Sailer & Homner (2020 meta-analysis): **g = 0.49 for cognitive learning** (still 0.42 in high-rigor studies), g = 0.36 for motivation, and g = 0.25 for behavior. The motivation and behavior effects were *not* robust in the high-rigor studies. Game fiction and social interaction moderated behavioral outcomes, and **competition combined with collaboration** did best.
- **Source:** https://link.springer.com/article/10.1007/s10648-019-09498-w
- **Confidence: Moderate.**

### F4.2 Expected, performance-contingent tangible rewards can undermine intrinsic motivation, more in children; badges and leaderboards can backfire
- **Evidence:** Deci, Koestner & Ryan (1999 meta-analysis, 128 studies): **expected tangible rewards** reduced free-choice intrinsic motivation, especially when contingent on engaging in, completing, or performing well at the task (d ≈ −0.28 to −0.40). **Children were more negatively affected than college students.** Positive *verbal/informational* feedback did not undermine motivation and enhanced it more for college students.
- Hanus & Fox (2015, 16 weeks, college course): adding badges, coins, and a leaderboard **lowered intrinsic motivation, satisfaction, and empowerment**. Lower motivation mediated lower exam scores.
- **Sources:** https://pubmed.ncbi.nlm.nih.gov/10589297/ · https://selfdeterminationtheory.org/wp-content/uploads/2014/04/1999_DeciKoestnerRyan_Meta.pdf · https://www.sciencedirect.com/science/article/abs/pii/S0360131514002000
- **Confidence: Moderate** (the reward meta-analysis is robust but debated; Hanus & Fox is a single study with adults).
- **Design implication:** Prefer **informational feedback** (you're getting better at R) over currency. **No sibling leaderboard**: a 4th grader racing a 6th grader is a recipe for discouragement. No money or screen-time-per-lesson deals unless the parent decides otherwise, knowingly. Keep cosmetics small and tied to mastery milestones, with no shop or loot boxes.

### F4.3 Success expectancy, autonomy, and an external focus support motor learning
- **Evidence:** Wulf & Lewthwaite's OPTIMAL theory (2016) says learning improves with **enhanced expectancies** (experiencing success), **autonomy support** (choices), and an **external focus** (attention on the effect, not the body). Simpson, Ellison, Carnegie & Marchant (2021, *Int. Review of Sport & Exercise Psychology*) reviewed 55 child studies of fundamental movement skills: 35 on external focus, 12 on expectancies, and 8 on autonomy. They describe the support as **"emerging"** and note that children's developmental characteristics may moderate the effects.
- **Sources:** https://gwulf.faculty.unlv.edu/wp-content/uploads/2014/05/Wulf_Lewthwaite_OPTIMAL_PBR_2016.pdf · https://research.edgehill.ac.uk/en/publications/a-systematic-review-of-motivational-and-attentional-variables-on-/
- **Confidence: Low–moderate** for children.
- **Design implication:** Offer kid-chosen options (ship name and colour, word-theme packs, choice between two missions). Keep success rates high. Frame cues around the outcome ("smooth, steady rhythm") rather than micromanaging joints. Finger instructions are still needed for correct mapping.

### F4.4 The "85% rule" is real research but a different domain; adaptive challenge is the transferable idea
- **Evidence:** Wilson, Shenhav, Straccia & Cohen (2019, Nature Communications) show mathematically that for **gradient-descent learners on binary classification**, the best training error rate is about **15.87%** (about 85% accuracy). It is not a study of children, motor sequences, or typing. The Challenge Point Framework (Guadagnoli & Lee 2004) makes the more general claim: learning is best at an intermediate *functional* difficulty relative to the learner's current skill, and that optimum shifts as skill grows.
- **Per-keystroke reality check:** at 85% keystroke accuracy, a 5-letter word has only about a 44% chance of being typed cleanly (0.85⁵). Most words would contain an error, which is discouraging and practises mistakes. Combined with F1.6 (low errors help kids' accuracy), a **~92–96% per-keystroke** target is more defensible for typing practice.
- **Sources:** https://www.nature.com/articles/s41467-019-12552-4 · https://coachingvb.com/wp-content/uploads/2019/01/Challenge-Point-A-Framework-for-Conceptualizing-the-Effects-of-Various-Practice-Conditions-in-Motor-Learning.pdf
- **Confidence: Low** for any exact number. **Moderate** for "adapt difficulty to keep kids near the edge of their skill".

### F4.5 Streaks, short rounds, progress bars: little direct evidence
- **Evidence:** I found no rigorous studies of streak mechanics for children's skill learning. Practitioner sources stress visible progress and subgoals. Donica cites Sormunen (1993, second-hand): programs with subgoals and intermediate successes work best because **persistence** drives keyboarding success. Common Sense Media's parent and kid reviews of TypingClub complain about **"rigid scoring"**, **"speed over accuracy"**, and ads (anecdotal).
- **Sources:** https://scholarworks.wmich.edu/cgi/viewcontent.cgi?article=1819&context=ojot · https://www.commonsensemedia.org/website-reviews/typingclub
- **Confidence: Very low / practice wisdom.**
- **Design implication:** Use short rounds (1–2 minutes), a strong **visible mastery map**, and **forgiving weekly goals instead of fragile daily streaks** (a design judgement to avoid loss-aversion pressure, not an evidence-based rule).

---

## 5. Measurement

### F5.1 WPM, accuracy, and inter-key interval (IKI) each measure something different
- **Definitions in use:** gross WPM = characters typed ÷ 5 per minute. Accuracy = correct characters ÷ characters typed. Net WPM = gross WPM minus word errors (Typing Test Pro, used in Donica 2021). Pinet (2022) adds **reaction time** (stimulus to first key), **IKI** (time between successive keystrokes), and accuracy including corrections.
- **IKI is the most diagnostic measure for per-key learning.** Novices show stronger word-length effects on reaction time. Experts show stronger hand-alternation effects on IKI (Pinet 2022). keybr uses per-key "time to type".
- Browser timing is good enough: Pinet's online platform was validated for keystroke-timing reliability (Pinet et al. 2017, cited in Pinet 2022).
- Rollover (pressing the next key before releasing the previous one) is common and correlates with speed (Dhakal 2018). Measure keydown-to-keydown and don't penalize overlap.
- **Sources:** https://scholarworks.wmich.edu/cgi/viewcontent.cgi?article=1819&context=ojot · https://pmc.ncbi.nlm.nih.gov/articles/PMC9356123/ · https://userinterfaces.aalto.fi/136Mkeystrokes/ · https://www.keybr.com/help
- **Confidence: High** for the definitions. **Moderate** for IKI as the learning signal.

### F5.2 Detecting weak keys and finger confusions
- **Approach supported by the tools and literature:**
  1. Per-key **median IKI** on correct presses, excluding long pauses and word-initial keys, which mostly reflect reading (the outer loop).
  2. Per-key **first-try error rate**.
  3. A **confusion matrix** (intended key → pressed key), classified as adjacent, same column, or homologous (Grudin 1983).
  4. Per-bigram IKI.
  5. **Hesitations** (IKI far above the key's own median), a likely sign of visual search.
- keybr picks the single slowest key as the "target letter" and puts it in every generated word. When all letters are green, it adds a new one.
- **Sources:** https://www.keybr.com/help · https://gwern.net/doc/design/typography/1983-grudin.pdf
- **Confidence: Moderate** (sound measurement logic; learning gains from targeting are not experimentally established).

### F5.3 Realistic expectations for kids
- **Evidence:** Donica 2021 posttest medians: grade 4 about 12–13 net WPM, grade 5 about 16.5–17 (after up to 2 years of weekly classes, dosage unknown). Freeman 2005 (via Donica): grade 4 keyboarding speeds across studies ranged 7.1–30 WPM. Bartholome (expert opinion): about 30–35 hours of instruction for alphabetic keys at about 20 WPM in early grades, and about 20–25 WPM needed for responses to feel "somewhat automated".
- **Confidence: Low** (wide variance and unclear dosage).
- **Implication:** At 12 minutes a day, 5 days a week (1 hour per week), expect **months, not weeks**, to reach fluent full-alphabet typing. Set the kids' and your own expectations accordingly.

---

## 6. What existing tools do: strengths and weaknesses

| Tool | What it gets right | What it gets wrong or leaves out (for this goal) | Sources |
|---|---|---|---|
| **TypingClub** (EdClub) | Structured progression from F/J; immediate per-keystroke feedback; "anchoring" lessons (hold J while practising left-hand keys); teacher-adjustable WPM/accuracy goals; replay of attempts; strong emphasis on not looking at the keyboard; Chromebook support. | Stars blend speed and accuracy, and kid reviews say it feels "speed over accuracy" and "rigid"; ads in the free tier; skipping ahead possible; optional class scoreboard (competitive); requires accounts and internet. | https://static.typingclub.com/m/corp2/other/typingclub-teacher-handbook.pdf · https://www.commonsensemedia.org/website-reviews/typingclub |
| **Typing.com** | Free structured K-12 curriculum, tests, teacher reports, games. | Banner and some video ads in the free tier (Plus/Premium removes them). A third-party review calls the lessons repetitive for kids who already type 30–40 WPM. | https://www.typingbattles.com/blog/typing-com-review · https://www.typing.com/en-gb/plus |
| **Nitro Type** | Very motivating racing; good for **practice volume** once keys are known; teacher controls. | Not for beginners; rewards speed and competition; cars and in-game money economy (extrinsic, comparison-heavy); Common Sense privacy report flags ads for under-13s. | https://www.educatorstechnology.com/2022/12/nitro-type-learn-typing-through.html · https://privacy.commonsense.org/privacy-report/nitro-type |
| **keybr** | Best adaptive engine: per-key timing stats, always targets the weakest key, frequency-based unlocking, pronounceable pseudo-words, clear per-key colour indicators. | Built for adults: no story, nonsense-looking words, unlock order ignores the physical home-row anchor, no kid-friendly framing, no parent view. | https://www.keybr.com/help |
| **Dance Mat Typing** (BBC) | Designed for ages 7–11; home-row-first progression in 4 levels × 3 stages; playful characters; free; "little and often" and cover-your-hands advice. | Fixed linear content, no adaptivity, limited data, no long-term practice loop; best as an intro. | https://www.bbc.co.uk/bitesize/articles/z3c6tfr · https://www.bbc.co.uk/teach/articles/ztj9h4j |
| **ZType** | Fun arcade shooter, no accounts, localStorage scores, Chromebook-friendly, Kids Mode. | **Doesn't teach technique**. Falling words reward frantic visual scanning and time pressure, which suits fluency practice after keys are learned. The ztype.com "about" page makes neuroscience claims (Yerkes-Dodson, sleep consolidation) that are marketing, not evidence. Note ztype.com describes itself as a modern version of the original Phoboslab Z-Type. | https://ztype.com/about |
| **Epistory** | Beautiful typing adventure; themed word sets (tree words for trees, and so on); suggests E/F/I/J movement to keep hands on the home row; adaptive difficulty. | Not a tutor; assumes you can already type; paid game (PC/Switch). Critic reviews call the core mechanic repetitive. One parent review on Metacritic (anecdote) says the adaptive difficulty didn't suit his son, who quit after about an hour. | https://www.gamedeveloper.com/design/let-s-talk-about-epistory-typing-chronicles · https://www.metacritic.com/game/epistory-typing-chronicles/ |
| **Keyboarding Without Tears** (for reference) | The only one with a published multi-year school study (F0.3); developmental sequence and technique emphasis. | Paid school product; study funded by the publisher. | https://scholarworks.wmich.edu/cgi/viewcontent.cgi?article=1819&context=ojot |

**Gap this project can fill:** keybr-grade adaptivity plus Dance Mat-style kid framing, with no ads, no accounts, offline use, sibling profiles, and a parent view built around **technique proxies** (accuracy, hesitations, confusions), not just WPM.

---

## 7. Practical constraints (Chromebooks, offline, storage)

### F7.1 Managed school Chromebooks often block local HTML files
- **Evidence:** School IT can add `file://*` to the Chrome URL blocklist (Google Admin), and web filters like Linewize publish instructions for doing exactly that. K-12 sysadmins discuss blocking downloaded HTML files specifically (Reddit thread; it blocked automated fetching, so I'm citing it from the search result only). A single-file HTML game **may not open at all on a school Chromebook**, and downloading it may also be blocked.
- **Sources:** https://help.linewize.com/hc/en-gb/articles/29359995865116-Block-local-html-files-on-managed-devices · https://support.google.com/chrome/a/answer/9942583?hl=en · https://www.reddit.com/r/k12sysadmin/comments/1j81bxb/blocking_locally_downloaded_html_files_from_being/
- **Confidence: High** that it's possible and common. Whether *your* school does it is unknown.
- **Implication:** Plan for **a home computer or personal Chromebook as the main device**. If school devices matter, the option is hosting the file on a static site and asking the school to allow it. Respect the school's acceptable-use rules.

### F7.2 localStorage works for file:// in Chrome but is shared across all local files and can be wiped
- **Evidence:** In Chrome, all `file://` pages share one storage origin, so any local HTML page can read or clear another's data (Stack Overflow report, seen via search). The HTML spec leaves the origin of `file://` pages implementation-defined (WHATWG issue #3099). Clearing browsing data wipes it, and so does incognito. ZType warns its users that scores disappear when site data is cleared.
- **Sources:** https://stackoverflow.com/questions/38209974/duplicate-local-webpages-in-different-locations-grab-same-localstorage-data · https://github.com/whatwg/html/issues/3099 · https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API · https://ztype.com/about
- **Confidence: Moderate–high.**
- **Implication:** Namespace the keys, version the schema, save often, and **provide export/import of progress** (a file plus a copy-paste backup code).

### F7.3 Things to verify on your actual devices (not researched in depth)
- Some managed Chromebooks run in ephemeral or guest-like modes that delete local data at sign-out. Check before relying on school devices.
- Chromebook keyboards put a Search/Launcher key where Caps Lock usually sits. Home-row position is unaffected, but on-screen keyboard art should match. Check the kids' actual laptops.
- Small laptop keyboards and children's hand size: Cornell suggests smaller keyboards for small hands. A 4th grader's reach on a full-size laptop keyboard is usually fine but worth watching.

---

## Summary table of key findings

| # | Finding | Confidence |
|---|---|---|
| F0.1 | Consistent finger mapping and eyes off the keyboard predict skill; ten-finger is the proven route but not the only one | High / Moderate |
| F0.2 | Slow typing hurts kids' written composition; fluency matters | Moderate |
| F0.3 | Structured, technique-focused instruction beats ad-hoc games (COI) | Low–Moderate |
| F1.1 | Skill = word-level chunking plus n-gram statistics; practise letters in many word contexts | High (theory) / Moderate (training) |
| F1.2 | Key locations are learned implicitly; drill the motor habit, not a mental map | High |
| F1.3 | Interleaving benefit is negligible in kids; blocked intro then mixed words | Moderate |
| F1.4 | Distributed practice beats massed; exact minutes for kids unknown | High / Very low |
| F1.5 | Volume and regularity matter most; "deliberate" adds unclear value | Moderate |
| F1.6 | Low-error practice may help kids' accuracy; error types reveal finger confusions | Low / Moderate |
| F1.7 | "Accuracy before speed" is overstated; separate speed and accuracy practice | Low |
| F1.8 | Keep instant right/wrong feedback; fade location guidance; let kids ask for help | Low |
| F2.1 | No evidence for one key order; hybrid is reasonable | Very low |
| F2.2 | Real words beat jumbled letters | Moderate |
| F2.3 | Unlock pace: use mastery gates; no evidence-based rate | Very low |
| F2.4 | Bias toward words with slow bigrams rather than drilling bigrams | Low |
| F3.1–3.4 | Technique emphasis helps; covers and fading keyboard aids are practice wisdom; ergonomics by consensus | Low / Very low / Moderate |
| F4.1 | Gamification: modest positive effect, detail-dependent | Moderate |
| F4.2 | Expected tangible or performance-contingent rewards and leaderboards can backfire, especially for kids | Moderate |
| F4.3 | Success, autonomy, external focus | Low–Moderate |
| F4.4 | "85%" is from ML theory; target about 92–96% keystroke accuracy via adaptivity | Low |
| F4.5 | Streak and progress-bar evidence is thin | Very low |
| F5.x | IKI + first-try errors + confusion matrix + hesitations = good diagnostics | Moderate |
| F7.x | School Chromebooks may block file://; localStorage is fragile, so export/import | High / Moderate |
