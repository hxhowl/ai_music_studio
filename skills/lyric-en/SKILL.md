---
name: lyric-en
description: 英文语境歌词创作与打磨。按 Suno 通用英文结构标签产出规范化英文歌词，涵盖 rhyme scheme 设计、音节数与重音对齐、韵族选择、hook 设计。当用户要写英文歌词、改英文词、设计押韵方案时使用。
---

# English Lyric Writing

> **Premise** (what a lyric is, and why every rule below follows from it): `references/lyric-craft.md` §0.
> One person, in a particular situation, saying something to someone — set to music.

## Iron Rules

> Not all four sit on the same level: 1–3 map to conditions 2 and 5 (missing them is an error);
> 4 is a **symptom check**, not a gate — no test can compute "does this read like a lyric" (§5),
> and a line can pass every count and still be bad.

1. **Section tags are Suno-standard English**, bracketed, on their own line.
2. Lyrics are **sung, not read**. Every line must be singable in one breath.
3. Stress alignment matters more than syllable count in English — a line with the right syllable count and the wrong stress pattern is unsingable.
4. **One situation per line, not two things in sequence.** A line that narrates "then this happened, so then that happened" is prose. ⚠️ **Don't count actors or actions** — two actors is common in good lines (`我送你离开 千里之外`); one actor with two simultaneous actions is fine too. Structures that need a pause to finish — comparative clauses (`earlier than my sigh`), stacked pre-modifiers (`my overhead-eave school uniform`), conditional clauses (`if you ever come back, then I'll…`) — leave nowhere for the breath to land.

---

## 1. Section tags & shape

### Tags

Full table (frequency ratings, meta tags, delivery tags): `references/suno-tags.md` §1 — single source; both lyric skills read from it, so don't keep a second copy here. Three things to remember:

1. **English, bracketed, own line**: `[Intro]` `[Verse]` `[Pre-Chorus]` `[Chorus]` `[Post-Chorus]` `[Bridge]` `[Instrumental Break]` `[Outro]` `[End]`
2. **`[Breakdown]` `[Drop]` `[whisper]` `[falsetto]` are where arrangement events land**, not just structural markers (Suno's Style is a whole-song description — it has no notion of "which section")
3. **Instrumental-only sections carry the tag and nothing else** — one blank line after, no prose underneath

### Shape: write it first, name it later

> ⚠️ **Never fix the structure before writing.** Practitioners agree: **write the chorus first, the
> structure follows.** The chorus is the only part anyone hears repeatedly; the verse exists to
> deliver it. Laying out sections first = paving a road before you know the destination.

**Before you write, decide one thing only**: is this short (a clip / short-form) or a full song.
Everything else waits until the chorus exists.

**Come back to the shape afterwards** — `references/song-structure.md` §2–3 give the section list and the
common orderings (**patterns, not options**); build your own if none fit.

A shape is judged by four things — **every section has a job / the chorus repeats enough /
long songs need air / the energy moves** (`references/song-structure.md` §3).
**They measure quality; they are not delivery gates**: meeting all four won't save a song with
nothing to say, and no arrangement makes up for the missing section.

---

## 2. Rhyme & tone

**Two judgments only**: lock the chorus, loosen the verse; never let two adjacent lines end on the same
word (different structure). Schemes, rhyme types, word banks, identical-rhyme cases, cross-family rules →
`references/rhyme-en.md`. **Look it up when choosing a family, don't read it up front.**

| Section | Density |
| --- | --- |
| **Chorus** | **locked** — the hook lives here; slant on 1 line max |
| **Verse** | **loose** — ABAB / ABCB, or unrhymed stretches are fine |
| Pre-chorus | either; an unrhymed last line makes a good lift |
| Bridge / outro | may switch family entirely — that's an audible turn |

⚠️ **Rhyme is a memory aid, not the goal** — "rhyme is not required"; when you drop it use repetition, a
ring phrase, or the melody instead. Sacrificing a good line for a rhyme is a net loss.

⚠️ **Rhyming every line doesn't mean reusing the same word.** Always wrong: **two adjacent lines ending on
the same word with different structure.** Always fine: parallel structure ("wait three more minutes / hold
three more minutes") and deliberate echoes (chorus Q&A, hook refrain) — devices, keep them.
Case: 「这是不是个动物园 / … / 这是疯狂的动物园」 — same word 3 lines apart, a Q&A frame, not a flaw.

⚠️ English and Chinese differ on purpose: Chinese leans on rhyme harder (no word stress to hold the
pulse); English is fine with every-other-line verses. Don't copy one density into the other.

### English has no 倒字, it has stress

**Stress placement matters more than syllable count.** A line with the right syllable count and the
wrong stress pattern is unsingable. You can't hear it, so do it on paper: mark each line's primary
stresses, number the metrical positions (1–4 in 4/4), and check they line up.

- ✅ "I **walk** a**lone** at **mid**night" — stress lands on beats
- ❌ "A**lone** I **walk** in the **night**" — fights the pulse unless intended

---

## 3. Line count — never default to 4 lines

**A line count comes from how much this needs to say — not from seconds.**
One question decides it: **how many breaths does this take to say?**

Given a range with no rule, the model takes the minimum, so every section gets 4 lines. Two failures:
- **A 4-line chorus**: one pass of the hook and it's gone. Nothing sticks
- **Equal counts everywhere (4/4/4/4)**: structural "AI symmetry." Verse and chorus **being equal is fine**,
  but when *every* section matches you lose length as a way to tell them apart — ballads usually run
  longer in the chorus, story songs longer in the verse

**Only one thing here is a condition** (`AGENTS.md` §4, condition 4): **repeats of the same function must
have equal line counts** — V1=V2, C1=C2, PC1=PC2. Judge by **function, not position**: judging by
position writes V1 and V2 with different counts, but they share one melody and can't be sung.

**Everything else is reference** — skeletons, typical counts, tempo-vs-length → `song-structure.md`.
Count after the chorus exists (④), then relate the verse to it (narrative ≥ / lyrical ≤).

**Line length: a line has to be singable in one breath.** No syllable table —
syllable count is a *result* of tempo and phrasing, not a target.

**But within a section, corresponding lines must be roughly equal in length** — except the **hook** and the
**landing line**, which may run clearly shorter or longer (a landing line often gets an extra half-bar).
They sing the same melody, so **half the length cannot be filled** — a 6-syllable line won't stretch over
a 12-syllable slot. Relative (lines against each other), never a table.
⚠️ **Never damage a better line to hit a syllable count.** Real case: `我说 哥 周一还得交周报` (the most
human line in the song) was rewritten to `我烦恼 周一汇报还得交` to cut syllables and force an AABB —
zero gain, pure loss, and the self-check still passed it.

**Mixed language**: structure follows the **main singing language**; a whole foreign line counts by
syllable. Put it in the hook or last chorus line, fixed and repeated 2–3 times. No full foreign sections,
**don't expect cross-language rhymes**.

---

## 4. Writing flow

```
⓪ **Lock the scene + who is speaking + the anchor line** (before anything else)
   · Scene boundary: what time / where / what the person is doing / what objects actually exist
     e.g. not "lonely" — "5:40pm, closing time, mop bucket by the door, phone still on the counter"
     Skip it and you write lines that fit any song
   · **Who is speaking** (more important than the scene — answer all four):
     (1) who this person is (**their situation**, not their job)
     (2) who they're talking to (present / absent)
     (3) when they're saying it (how long after)
     (4) **what they want out of saying it** (to convince the other / to convince themselves / just to say it)
     ⚠️ The fourth one sets the tone. Without it you get "a writer describing a relationship",
     not "a person talking".
   · ★ **The anchor line**: the one line that sounds most like a real person
     (it's often the title, and the seed of the hook). ⚠️ Highest priority — it wins every conflict.
     ⚠️ **But it does not have to happen at ⓪** — it's the same thing as the chorus in ③.
     Can't find it? Keep going. It shows up once the chorus works; if the chorus doesn't have it,
     the song doesn't have it
   · **Not enough information?** Invent one concrete scene, state it in one line, and start ("I'll write it
     as a Tuesday-night hospital corridor — stop me if that's wrong"). ⚠️ Don't keep interrogating and don't
     write something generic — **correcting a concrete draft is faster than staring at a blank page**

① Clarify + nail the premise
   · **Only ask what you cannot default** (language). Style / mood / POV: pick a concrete default,
     restate it in one line, and start writing
   · Never re-ask what you were already told; don't invent questions to fill the step
   · The premise in one concrete sentence, not an abstract mood word
   (interchangeable with ⓪; whichever comes to you first)

② Set the tone: emotional arc / POV and address / who sings it / hook direction

③ **Write the chorus first — set the target** (⚠️ before any verse)
   Build it around the anchor line as the hook. Say what the song is about.
   The chorus is the answer the verses reach for — **know the answer before you build the road**.
   ⚠️ Can't write the chorus = the premise isn't clear yet → go back to ⓪, **don't force a verse**.
   ⚠️ **Never start the song from line 1.** This is the most consistent point across practitioners
   ("Start with the hook, not the first line" — see `references/lyric-craft.md` §1).
   ⚠️ **The chorus is the universal half**: the verse gives one specific scene, the chorus turns it
   into something everyone has felt. If the verse already says "I'm sad", the chorus has nothing to lift.

④ **Set the shape — only after the chorus exists**
   Count the chorus lines you actually wrote, then decide how the verse relates to it
   (narrative ≥ / lyrical ≤). Tempo sets a band, not line numbers.
   For the section layout, read `song-structure.md` §2–3 — common orderings, **not options to pick
   from**. Build your own if none fit.
   **Structure is a result of writing, not a premise for it.**

⑤ **Pick the rhyme family (changeable later)**
   See where the chorus naturally lands and **use that**; switch if it fights you.
   ⚠️ **Never let rhyme decide content.** In the priority order rhyme sits below "sings like speech";
   it must not be locked before you write anything

⑥ Verse — **the picture, not the road**. Ask first: what state must this start from for the
   chorus to be earned? Concrete images and actions, no commentary.
   One thing should run through it (eye line / one action / one object). **Juxtaposition is fine** —
   a list is not: a list is six things with no line through them (`lyric-craft.md` §3).
   ⚠️ Keep the verse **specific**. Generality belongs in the chorus.
   ⚠️ **A section walks toward one place** — cover the first three lines and read the last: does it
   stand on its own? If not, that line is just the last line.
   → Pre-Chorus (shorter lines, rising) → Bridge (switch rhyme family / perspective, say the real
   thing) → Outro (stop — don't summarize)

⑦ **Cut — this step is not a "self-check"**
   Ask of every line: **would the song be worse without it?** If not, cut it.
   Then scan top to bottom: **is there a line you'd want to skip?** That's the one to fix.
   (Don't write "read it aloud" — you can't hear it, see Iron Rule 2.
   No rule-ticking — the rules are reference, not delivery conditions)

   Then **check each line for looseness**: write a tighter version, compare what the cut lost.
   When nothing more can be cut, stop (`skills/lyric-naturalness/SKILL.md`).
```

**Division of labour**: verse = **specific** (one scene, one action, one moment — never explain the emotion); chorus = **universal** (turn that specific thing into what everyone has felt — never add new plot); bridge = **the turn** (what verse and chorus never said).

**Each later verse must move one step beyond the previous one** (not just V2 — narrative and rap songs
often have three): equal counts don't mean the content may repeat. V1 sets the scene, V2 advances it —
shift the time ("three days later"), **shift what is observed** (⚠️ the *object*, **not the narrative
person** — POV stays one throughout), or let an object planted in V1 change by V2 ("phone at 4%" → "it died").
⚠️ Rephrasing V1 is still repetition — the verse must move, not restate.

**How to build a hook** (having one isn't enough — it has to be memorable and singable):

| Point | Rule |
| --- | --- |
| **Placement** | **First line of the chorus** (heard first), then repeated at the last line or in `[Post-Chorus]` to close the loop |
| **Length** | **Usually shorter than the surrounding lines** — if the surrounding lines run 8 syllables, aim for 5–6. Not a rule: the hook can be the longest line if it's the most memorable (it's the exception to the roughly-equal-length guideline) |
| **Open vowels** | Prefer open vowels (ah / ay / oh); closed ones (ee / oo) don't carry and get swallowed |
| **Repetition** | Repeat verbatim 2–3 times, **unchanged**; if the three choruses vary, vary **line 4** in a 6-line chorus (**line 3** in a 4-line one), never the hook |
| **Content** | It's the title or a near-paraphrase of it; **no abstract emotion words** ("it'll be okay" doesn't stick) |

⚠️ A hook that changes all three times is no hook. In a **6-line** chorus leave the variation to
**line 4** — don't touch lines 1–3: line 2 *develops* the hook, so changing it dismantles the hook itself.
(A 4-line chorus varies **line 3**; full layout in `references/song-structure.md` §4.3–4.4.)

---

### What gives way when things conflict

Formal metrics fight each other, and they fight the quality goal. **The priority order is fixed**:

> **private voice > sings like speech > rhyme > syllable alignment**

**Conditions that never yield** (only these five; everything else gives way):
versioning, tag format, formatting, equal line counts for repeats of the same function, singability.

⚠️ **"Corresponding lines roughly equal within a section" is relative, not a syllable quota** — lines
against each other, never against a table; it sits last, so it yields to "singable".

⚠️ **Duration is not in this list** — it varies by genre (90-sec punk, 5-min post-rock); making it a
condition forces padding or cutting lines just to hit seconds.

⚠️ **Suno's Style character limit is NOT a lyric-side condition** — it applies to prompts. Lyrics have
no character limit. Don't mix the two sides up.

⚠️ **The per-line syllable cap is NOT one of them** — reference, not a hard limit. **Sacrificing a line
to hit a syllable count is the wrong trade.**

| Conflict | Who wins |
| --- | --- |
| A line only he would say, but it's too long | **Keep the line**; tighten the lines around it |
| A line that reads perfectly but doesn't rhyme | **Keep the line**; change the rhyme word or the neighbours |
| Perfect rhyme, awkward line | The rhyme gives way |
| Even syllables, but it reads fake | Alignment gives way (ragged edges are wanted anyway) |

## 5. Common failure modes

### A lyric line is not a prose sentence

The fastest way to sound like a diary entry: **transcribe the scene with full clauses.** Two people in
the scene makes it worse — it becomes dialogue.

| Prose | Lyric |
| --- | --- |
| The rain really came down, so you pulled me under the eaves | School uniform held up — that was our eave |
| You said it would rain, and I left my umbrella in the classroom | Only said it wouldn't rain, didn't argue |

**No checklist can compute "does this read like a lyric."** What you can see is whether the line says
**one situation**, or narrates **two things that happened in order**:

| | The relation between the two actions | Result |
| --- | --- | --- |
| `You said it would rain, I left my umbrella in class` | sequential (so → therefore) | plot. The listener waits for what happens next |
| `越过山丘 虽然已白了头` | simultaneous (the cost) | a situation. The two actions lock together |
| `我送你离开 千里之外` | two sides of one thing | a situation |

⚠️ **Don't count pronouns, and don't count actions.** Two actors is common in good lines —
`我送你离开 千里之外`, `天青色等烟雨 而我在等你`; one actor with two events is too — `越过山丘 虽然已白了头`.
**Counting can't decide this.**

**Devices that turn a line into a situation** (devices, not rules):

- **Leave the subject out most of the time** — recoverable, but it doesn't need saying
- **Use fewer sequencing conjunctions** — `so` / `then` / `because` string lines into a plot; ⚠️ contrast
  words (`though` / `but` / `while`) are not the same — they make tension, not sequence
- **The other person doesn't need an action to be present**: `Only said it wouldn't rain, didn't argue` —
  they didn't speak, but they're there

**Legal shapes** (all fine, don't force them): noun juxtaposition / dropped subject / fragment / repetition.

**Two people: don't alternate dialogue.** Ping-pong is a script; **juxtapose two actions from the same side**:

❌ `You said it would rain, I left my umbrella in class` — one action from you, one from me, glued by "so"
✅ `Only said it wouldn't rain, didn't argue` — one side, two actions; the other person shows up in "didn't argue"

> **A pronoun that carries the point of view stays**, in two cases: **the relationship itself is the
> content** (`You're my most accurate forecast`, `Others watch clouds, I watch your eyes`), or
> **cutting it leaves nobody in the frame** (`我会假装说 还行`). One test: cut it — is this still a
> line somebody is saying?

### Beyond "is it a lyric"

- **It leaves something hanging** — `故事的小黄花 从出生那年就飘着`: drifted where? Nothing left = explanation.
- **It has tension inside** — `越过山丘` × `已白了头` (arrival × cost). ⚠️ "Good" standards, not gates.

### Everything else — symptoms → fixes

**When stuck**, see `references/lyric-diagnostics.md` (forced rhyme, stress clash, abstract pile-up,
dead chorus, POV drift, unsingable lines).

---

## 6. Naturalness — one thing to hold while drafting

**Heavier emotion, lighter wording** — not "I miss you till I cry", but "I never deleted it".

The rest lives where it belongs; this file doesn't restate it:

| Question | Go to |
| --- | --- |
| Which words are empty / clichéd / need qualifying | `references/anti-ai-lexicon.md` |
| Is this line **loose** — do the words buy what it says? | `skills/lyric-naturalness/SKILL.md` |
| "Something's off and I can't name it" | `references/lyric-diagnostics.md` |

---

## 7. Delivery check

### Check conditions 1–5 of `AGENTS.md` §4

This file **does not restate them** — conditions live in one place only.
Go read those five: **versioning / section tags / formatting / equal line counts / singable**.

> If all pass, write one sentence — no ticking, no score. **Nothing outside those five is a gate.**

### Two of the four outside tests you can actually run

The other two need a human: **hum-back test** (can they hum the chorus 20 minutes later) and
**stranger's face** — you can't hear and can't see, don't pretend you ran them.

1. **Chorus only**: read just the chorus. Do you know what the song is about? If not, the chorus isn't doing its job.
2. **One line as a title**: is there a line short enough to be a title and strong enough to carry the whole song?

### Everything else — consult when stuck, **not a delivery gate**

The four symptom groups ("doesn't hold together", "doesn't read like a lyric", "too AI", "wrong shape")
live in `references/lyric-diagnostics.md`. **If it's flowing, don't look** — a checklist you always pass
teaches you to optimize for the checklist.

---

## 8. Formatting (hard rules)

**Always inside a code fence** — so it can be copied in one action.

```
[Intro]

[Verse 1]
first lyric line
second lyric line
third lyric line

[Chorus]
first lyric line
second lyric line
```

| Item | Rule |
| --- | --- |
| Section tag | Own line, English, bracketed, **no punctuation** |
| **Each lyric line** | **Own line, no blank line between lines** |
| Between sections | **One** blank line (exactly one) |
| Mid-line breaks | Half-width space; no comma or period unless the pause is intended |
| Delivery tags | `[whisper]` `[falsetto]` on their own line, before the section |
| Empty sections | Instrumental-only (`[Intro]`, `[Instrumental Break]`) — tag only, then one blank line |

> ⚠️ **Never put a blank line between every lyric line** — that's paragraph format, not lyric format, and it pastes into Suno full of empty lines.

### Delivery document

```markdown
# Lyrics · "{Title}" v1        ← v1 is explicit; no "first version omits it" special case

> Previous: outputs/{song}/…-lyrics-v1-20260101.md    ← write "none" for the first version

## Lyrics                   ← code block, copy-paste ready

---
**One line each**: what you chose (section layout / tempo band), what changed, what still bothers you —
**five lines max**.
```

**That's it.** They asked for a song, not a case file.

### Expand only when asked

| They ask | You give |
| --- | --- |
| "Why this structure?" | section layout, tempo band and why, lines per section |
| "How does the rhyme work?" | family + density (how many lines unrhymed, and where) |
| "What imagery did you use?" | image cluster + why this family |
| "Did you self-check?" | only what **failed**; all clear = one sentence |

⚠️ **Don't volunteer the expansions.** In seven real revisions the commentary ran 61–69% of the file —
a full screen of justification before the reader reached the song (`AGENTS.md` §4).

---

## 9. Output

**Filenames and version rules: `AGENTS.md` §4, condition 1** (single source; not restated here).

```
outputs/{song}/
  {song}-lyrics-v1-20261030.md
  {song}-prompts-v1-20261030.md
```

- Revisions always create a **new file**, never overwrite; each new version states **what changed** +
  **path to the previous file** + why. Template: `examples/002-versioning.md`
- Append **two lines** per round to `outputs/{song}/{song}-log.md` (`references/logging.md`);
  **don't paste the log into the reply**
- `outputs/` is git-ignored — **never reference a specific file inside it** from a committed file
