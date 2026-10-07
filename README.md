# Ava’s VerbQuest

A standalone browser app for **3 minutes of daily English irregular-verb retrieval practice**. Open `verbquest.html` in a modern browser. Progress is stored locally on that device.

## Current test format

Every item is **test-first**. There is no teaching card before the question.

Ava sees the **German meaning** and one semantic visual cue, then fills the complete English paradigm on a **single page**:

1. infinitive
2. simple past
3. past participle

For example:

> **bringen**  →  [ bring ]  [ brought ]  [ brought ]

Any field may be left blank if Ava does not know that form. There is also an **“I don’t know this paradigm”** button.

After checking, each form is scored separately. Audio is available beside each answer, and every audio button pronounces **only that single English form**; the app never reads a whole paradigm aloud.

## Verb inventory

The app currently contains **268 irregular / mixed-irregular three-part paradigms**, from the high-frequency core to less common verbs and common irregular compounds. Standard variants such as `learned / learnt`, `got / gotten`, `dived / dove`, etc. are accepted where appropriate.

The three-field drill is specifically for verbs that have a meaningful infinitive–past–participle paradigm. Defective modal verbs such as `can/could` do not have a normal past participle and therefore are not forced into this exercise format.

## Adaptive practice

VerbQuest stores memory evidence separately for the infinitive, simple past, and past participle, while selecting **whole paradigms** for testing.

- Due reviews come first.
- A paradigm with an error is recycled again after several intervening verbs in the same session.
- When currently due material is cleared, the app continues through **unseen verbs instead of repeatedly drilling the same small set**.
- A completely correct first encounter is treated as evidence that Ava already knew the paradigm and starts at a longer interval.
- Correct retrievals expand spacing roughly through 1 → 3 → 7 days and then longer intervals.
- Errors shorten the interval.
- A paradigm counts as mastered only when all three component forms are stable.
- High-utility verbs are encountered before obscure ones during the initial sweep.

The result is an initial diagnostic sweep through the full inventory, followed increasingly by practice concentrated on the forms Ava actually forgets.

## Visual cues and Ava

Every verb has a semantic visual cue. Where a human agent naturally fits the meaning (for example *run, write, eat, bring, speak, choose*), Ava’s illustrated avatar is integrated into the cue. More object- or event-like verbs (for example *cost, ring, freeze*) use the semantic cue without the avatar. Visual cues fade after a paradigm becomes stable and can also be switched off in Settings.

The avatar is embedded in the HTML, so the main app remains a single offline file.

## Other features

- 3-minute daily target and optional 2-minute review
- XP, levels, streaks, perfect-paradigm combos, badges, and mastery map
- local progress only; no account or server required
- common British and American irregular variants accepted where appropriate

## October 6 minor scheduling update

- **Alternative forms:** when a paradigm lists more than one accepted form (for example `learned / learnt`, `got / gotten`, or `was / were`), entering **either one** counts as fully correct for that field. Ava never has to type both alternatives.
- **Broad first pass before repetition:** no paradigm is repeated until Ava has attempted at least **half of the full inventory once**. With the current 268-paradigm deck and three fields per page, that is 134 paradigms = **402 individual form prompts** before the first repeat can occur. After that coverage threshold, normal adaptive review resumes: due/weak forms and recent errors receive priority.

## October 7 update
- Ava scene cues for **get, bring, eat, and read** are now embedded directly in the standalone HTML as image data, so they also appear when `verbquest.html` is opened by itself.
- The three paradigm fields are stacked vertically.
- Simple-past and past-participle retrieval now occurs inside sentence frames (for example: `I ___ at school this morning.` / `I have ___ sleeping all day.`), while the infinitive remains a direct German→English retrieval field.
- Common verbs have hand-written example frames; rarer verbs use category-appropriate fallback frames.
