---
name: lyric-en
description: 英文语境歌词创作与打磨。按 Suno 通用英文结构标签产出规范化英文歌词，涵盖 rhyme scheme 设计、音节数与重音对齐、韵族选择、hook 设计。当用户要写英文歌词、改英文词、设计押韵方案时使用。
---

# English Lyric Writing

## Iron Rules

1. **Section tags are Suno-standard English**, bracketed, on their own line.
2. Lyrics are **sung, not read**. Every line must be singable in one breath.
3. Stress alignment matters more than syllable count in English — a line with the right syllable count and the wrong stress pattern is unsingable.

---

## 1. Section tags & templates

### Tags

Full table (frequency ratings, meta tags, delivery tags): `references/suno-tags.md` §1 — single source; both lyric skills read from it, so don't keep a second copy here. Three things to remember:

1. **English, bracketed, own line**: `[Intro]` `[Verse]` `[Pre-Chorus]` `[Chorus]` `[Post-Chorus]` `[Bridge]` `[Instrumental Break]` `[Outro]` `[End]`
2. **`[Breakdown]` `[Drop]` `[whisper]` `[falsetto]` are where arrangement events land**, not just structural markers (Suno's Style field can't parse sentences)
3. **Instrumental-only sections carry the tag and nothing else** — one blank line after, no prose underneath

### Templates (skeleton only — line counts are computed at source)

> ⚠️ Line counts are deliberately **not listed here**. They must be computed at the ACTUAL BPM (§3);
> copying a number off a table is the most common failure. Full calculations, selection rules and the
> measured 120 BPM case: **`references/song-structure.md` §6, §7, §8**.

| Template | Style | Typical BPM |
| --- | --- | --- |
| T1 | Ballad | 85 |
| T2 | Standard pop | 95 |
| T3 | Story folk | 90 |
| T4 | Build (final chorus extended) | 85 |
| T5 | Short-form (60–90 sec; the only short template) | 100 |
| T6 | Rap-led (verse carries the song) | 90 |
| T7 | Long-line (2 bars per line) | 90 |
| T8 | EDM / dance (instrumental-heavy) | 128 |
| T9 | R&B / neo-soul (long chorus) | 92 |

**Four-step narrowing — don't take the familiar one** (offering nine templates with no selection rule means the first one gets picked):

1. **Target length**: 60–90 sec → **T5 only**; 2:00–3:30 → the rest
2. **What carries the song**: chorus-led (emotional, cathartic) → T1/T4/T9; verse-led (narrative, rap) → T3/T6; balanced → T2; instrumental-led → T8
3. **How many choruses, do they vary**: three with variation → 6 lines; final must peak → extend to 8 (T4); chorus only restates the title → 4
4. **Genre overrides**: long-line / Chinese-style → T7; EDM → T8; R&B → T9; rap → T6

**A template gives**: which sections, in what order, how many repeats; advice on optional sections; a typical BPM as default.
**It does not give**: line counts (they move with BPM), BPM (it moves with the user's request), or total runtime.

Don't add optional sections by default: Pre-Chorus may be dropped in T3/T4/T5; Bridge can be an instrumental break in T5/T6.
State **why** you chose this template.

---

## 2. Rhyme systems

### Schemes

| Scheme | Pattern | Feel |
| --- | --- | --- |
| **AABB** | Couplets | Simple, folk, nursery-solid |
| **ABAB** | Alternating | Forward motion, classic pop |
| **ABCB** | 2nd/4th only | Relaxed, conversational |
| **AABA** | Three same + turn | Vintage, jazzy |
| **AAAA** | Monorhyme | Driving, rap / chant |

### Types

| Type | Definition | Example |
| --- | --- | --- |
| **Perfect** | Identical vowel + coda | night / light |
| **Slant (near)** | Approximate | bridge / inch |
| **Assonance** | Vowel match only | time / light |
| **Consonance** | Coda match only | bill / wall |
| **Internal** | Rhyme inside the line | "I **crash** and I **burn**" |
| **Multi-syllabic** | 2+ syllables | "mo**tiva**tion" / "ele**va**tion" |
| **Rich** | Same spelling, diff. meaning | lie (deceive) / lie (recline) |

### Families (full tables: `references/rhyme-en.md`)

| Family | Words |
| --- | --- |
| -ight | night light bright fight high why try |
| -ay | day say away stay rain* again* |
| -ow | low slow go home* know alone* |
| -eart | heart apart start dark* |
| -ove | love above enough* blood* |
| -ime | time crime line* mind* |
| -ine | line fine shine mind* time* |
| -ong | long strong wrong alone* |

\* slant rhyme — usable but flag it.

### Choosing

- **Chorus**: lock one family; slant allowed on 1 line max
- **Verse**: looser — ABAB or ABCB, internal rhyme for density
- **Bridge**: switch family entirely = an audible turn
- **Multi-syllabic rhyme** reads as high craft; use in rap or the final verse
- Avoid forcing: "the **light** of my **sight**" is filler

---

## 3. Line count & meter — never default to 4 lines

Given a range with no selection rule, the model picks the minimum. Result: every section is 4 lines — the whole song runs ~1:51 (below the 2:00 floor), the chorus arrives and leaves in 11 seconds, **so the emotion never has time to land**. Equal line counts across sections is structural "AI symmetry." **Line count is calculated, not guessed.**

### Decision flow

> Every lookup table, template library and conversion table lives in **`references/song-structure.md`**
> (single source of truth). This section holds only the flow and the hard constraints —
> **go read the relevant section there when you set line counts**; don't work from memory.
> Section numbers below all refer to **`references/song-structure.md`**.

| Step | What | Where |
| --- | --- | --- |
| ① Pick template | Narrow to T1–T9 in four steps; **don't take the familiar one** | §7 |
| ② Set BPM | Use the user's if given; else take the **template's typical BPM** and state it | §8 |
| ③ Count lines | `sec/line ≈ 240 ÷ ACTUAL BPM`; chorus floor then comes from its emotional job | §2, §4 |
| ④ Validate | Chorus duration, whole-song duration, line-count relations | §2, §5, §8 |

### Three hard constraints

**① A template gives the skeleton; recalculate line counts at the actual BPM.**
Measured: T2's 6-line chorus at 120 BPM = 12 sec, below the floor.
⚠️ **Validate with the actual BPM too** — checking against the template's 95 BPM returns 15.2 sec and a false pass.
At 120 BPM the fix is **8 lines + `[Post-Chorus]`**, not 9 lines (a 9-line chorus is overlong for pop).
The verse usually stays: 6 lines fits the 10–20 sec band from 70 to 140 BPM.

**② Chorus 15–22 sec, whole song 2:00–3:30 — but the two constraints are asymmetric.**
- **The line floor is hard**: build 6–8, one-punch 4, needs-3-variations 6 (full table: `song-structure.md` §4)
- **The seconds floor is soft**: 15 sec is an empirical band measured at 85 BPM. At high BPM **keep the lines and let the seconds fall short** — cutting lines to hit seconds destroys information and fixes the wrong thing. Buy time with `[Post-Chorus]` or another repeat
- A narrative-tag chorus (folk, rap) may run as short as 10 sec; it builds memory through repetitions

**③ Line-count relations go by function, not position.**
- **Repeats of the same function must be equal** (V1=V2, C1=C2, PC1=PC2) — same melody; unequal counts are unsingable
- **Verse ↔ pre-chorus ↔ chorus should differ** — the same count everywhere is structural "AI symmetry"
- Bridge / outro **may match** those (one-off sections with their own melody)
- ⚠️ Never write "adjacent sections must not have equal line counts" — followed literally, V1 and V2 end up different, but they share one melody and can't be

### Syllables & stress

English is stress-timed. Align **both**:

| Section | Syllables / line |
| --- | --- |
| Verse | 8–12 |
| Chorus | 7–12 |
| Pre-Chorus | 5–8 |
| Bridge | 6–10 |
| Outro | 4–8 |
| **Long-line styles** (Chinese-style, ambient) | **14–20** — one line spans 2 bars; use fewer lines |

**Stress check**: read the line aloud and tap the beat. The natural word stress must land on the beat.
- ✅ "I **walk** a**lone** at **mid**night" — stress lands on beats
- ❌ "A**lone** I **walk** in the **night**" — fights the pulse unless intended

**Syllables move with BPM too**: the table above assumes ~85 BPM. The real constraint is one breath —
at 120–140 BPM cap lines at **6–9 syllables**, at 160+ at **5–7**. Full table: `references/song-structure.md` §2.

### Mixed language

Lines of another language inside an English lyric are common, but **structure follows the main
singing language**.

| Question | Rule |
| --- | --- |
| Which skill | Follow the **main singing language**: English-led → this skill; Chinese-led → `lyric-zh` |
| Counting | English parts by syllable; a **whole Chinese line** by characters (1 character ≈ 1 syllable) |
| Rhyme | English parts follow their rhyme family; Chinese words don't join it — **don't expect cross-language rhymes** |
| Placement | Hook, the last chorus line, or the pre-chorus lift — the spot must be **fixed and repeat 2–3 times** |
| Singability | Chinese parts still need **tone-to-melody** care (see `lyric-zh` on 倒字), or the meaning gets misheard |

⚠️ Three traps:
1. **No full foreign-language sections** — it breaks syllable alignment and rhyme density
2. **Don't add a language for flavour** — the borrowed line must say something English can't
3. **Section tags are unaffected** — they stay English regardless

**Rule of thumb**: within a section, corresponding lines must match syllable count within ±2 AND stress position.
**Long-line styles: check total syllables, not lines** — target **45–90 syllables in the chorus**.

**State at delivery**: which template (T1–T9) and why; **the actual BPM and its source** (user-specified / template default); lines per section and why (ACTUAL BPM + emotional job + duration check); if it differs from the template typical BPM, what changed.

---

## 4. Writing flow

```
⓪ **Lock the scene boundary** (before writing anything): what time / where / what the person is
   doing / what objects actually exist there
   e.g. not "lonely" — "00:47, last train, three people in the carriage, phone at 4%"
   This decides the material for the whole song. Skip it and you write lines that fit any song,
   which then has to be fixed afterwards by `lyric-naturalness`.
   Detail: `lyric-imagery-rhyme` mode A step 1
① Nail the premise — one concrete sentence, not an abstract mood word
② Pick a template (T1–T9, §1 four steps, **skeleton only**) → set the actual BPM → set line counts (§3)
   Output a table: which template, actual BPM and its source, lines per section, target seconds, why
③ Pick rhyme family for the chorus; lock it
④ Take images and rhyme candidates **within the ⓪ boundary** (call `lyric-imagery-rhyme`)
⑤ Verse — concrete nouns + verbs, no commentary
⑥ Pre-Chorus — shorter lines, rising
⑦ Chorus — hook at line OPENING, written to the line count decided in ②, leave a variation slot
⑧ Bridge — switch rhyme family / perspective, say the real thing
⑨ Outro — fewer words, fade
⑩ Self-check (includes line count + duration, §7)
```

**Division of labour**: verse = **images** (concrete nouns, actions); chorus = **attitude** (emotion + repetition); bridge = **the turn** (what verse and chorus never said).

**V2 must move one step beyond V1**: equal line counts (same melody) don't mean the content may repeat.
V1 sets the scene, V2 advances it — shift the time ("three days later"), shift the perspective
(from "I" to "you"), or let an object planted in V1 change by V2 (V1: "phone at 4%" → V2: "it died").
⚠️ Just rephrasing V1 is exactly what `lyric-naturalness` check #9 catches as "repetition in new words".

**How to build a hook** (having one isn't enough — it has to be memorable and singable):

| Point | Rule |
| --- | --- |
| **Placement** | **First line of the chorus** (heard first), then repeated at the last line or in `[Post-Chorus]` to close the loop |
| **Length** | **Shorter than the surrounding lines** — if the chorus runs 8 syllables, make the hook 5–6 |
| **Open vowels** | Prefer open vowels (ah / ay / oh); closed ones (ee / oo) don't carry and get swallowed |
| **Repetition** | Repeat verbatim 2–3 times, **unchanged**; vary lines 2–3 instead, never the hook |
| **Content** | It's the title or a near-paraphrase of it; **no abstract emotion words** ("it'll be okay" doesn't stick) |

⚠️ A hook that changes all three times is no hook. Leave the variation to the middle lines.

---

## 5. Common failure modes

| Problem | Symptom | Fix |
| --- | --- | --- |
| Forced rhyme | "the light of my sight" | Rewrite so the rhyme word is the *only* right word |
| Stress clash | Right syllables, wrong accents | Retap the beat, move the word |
| Abstract pile-up | lonely, broken, lost, hollow | Swap for concrete: cold coffee, unread text |
| Dead chorus | Every line is new | Put hook at line 1, repeat 2–3x |
| POV drift | I / you / he mixed | Keep one; bridge may switch |
| Unsungable | Too many syllables in one breath | Split or cut |

---

## 6. Naturalness red lines (prevent while drafting)

**The root cause of AI-sounding lyrics is averaging** — if anyone could have written it, it belongs to no one. Hold these at the drafting stage; don't leave it for a post-write fix.

- **Three questions per line**: can a camera film it? would it still work in a different song? is there one detail nobody else would write?
- **≥ 3 concrete nouns per verse**; **≤ 3 abstract emotion words** in the whole song
- **≥ 1 contemporary object**: 12% battery, a delivery note, a read receipt, the last train, a locker pickup code
- **Generic imagery must be qualified**: not "rain" — "the kind of rain that flips your umbrella"
- **Vary line length**: keep the opening lines aligned, then let **one line (usually the last)** run clearly longer or shorter as a landing line. Never all lines equal (fake), never all over the place (unsingable)
- **Heavier emotion, lighter wording**: not "I miss you till I cry" — "your toothbrush is still in the cup"

Replacement words: `references/anti-ai-lexicon.md`. Full rules and rewrite flow: `skills/lyric-naturalness/SKILL.md`.

---

## 7. Self-check before delivery

**Craft**
- [ ] Tags are Suno-standard English, bracketed
- [ ] Chorus rhyme family consistent; verse scheme stated
- [ ] Syllable + **stress** aligned within sections
- [ ] Read aloud — no tongue-twisters, no forced rhymes
- [ ] Verse gives images, chorus gives attitude, bridge gives the turn
- [ ] No artist names, brands, or unpronounceable proper nouns

**Naturalness (§6)**
- [ ] **≥ 3 concrete nouns per verse**; ≤ 3 abstract emotion words in the whole song
- [ ] ≥ 1 contemporary object; generic imagery is qualified
- [ ] At least one line only this person would say (**veto item**); line lengths vary

**Line count (§3)**
- [ ] **Not every section is 4 lines** — counts derived from BPM + emotional job, not the minimum
- [ ] **Validation used the ACTUAL BPM, not the template's typical BPM** (typical-BPM validation returns a false pass)
- [ ] Chorus meets the line floor for its job; under the 22-sec ceiling; whole song 2:00–3:30
- [ ] **Repeats of the same function have equal line counts** (V1=V2, C1=C2); verse and chorus differ
- [ ] Delivery states template, actual BPM and its source, lines per section, and any adjustment vs the template

**Format & versioning (§8, §9)**
- [ ] Lyrics inside a code block, one line per lyric line, **no blank lines between lines**, one blank line between sections
- [ ] Revisions wrote a **new file** with a version number; the original was not overwritten
- [ ] New version states what changed, what didn't, and the previous file path

**Pass mark**

- **Craft, Line count and Format groups must pass in full** — these are errors, not scores.
  There is no "mostly fine": a Chinese tag, validation at the template BPM, or an overwritten
  file is wrong, full stop
- **Naturalness**: pass **≥ 8 of 10** on `skills/lyric-naturalness/SKILL.md`, and the
  **private-voice** item is a veto — fail it and the lyric fails regardless of the rest

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

> Version note: what changed vs. previous; path to previous file

## 1. Lyrics                   ← code block, copy-paste ready
## 2. Structure & Line Count   ← lines per section, why (ACTUAL BPM + job + duration)
                              ← actual BPM and its source (user-specified / template default)
                              ← if it differs from the template typical BPM, what changed
## 3. Rhyme Check
## 4. Imagery & Rhyme Design   ← image cluster + why this family (write it when lyric-imagery-rhyme was used)
## 5. Design Notes
## 6. Self-Check
```

---

## 9. Versioning & output

One folder per song; both lyrics and prompts live inside it:

```
outputs/{song}/
  {song}-lyrics-v1-20261030.md
  {song}-prompts-v1-20261030.md
  {song}-lyrics-v2-20261031.md
  ...
```

| Type | Filename |
| --- | --- |
| Lyrics | `outputs/{song}/{song}-lyrics-v{N}-YYYYMMDD.md` |
| Prompts | `outputs/{song}/{song}-prompts-v{N}-YYYYMMDD.md` |

- **v1 is explicit** — no special case where the first file omits the version
- Lyrics and prompts **each increment independently**; numbers are globally unique, never reset or reused
- Date = **the day of the revision**, not the first version's date. Date goes last so files sort by type + version
- A prompt file must state **which lyrics version it was built from** (by path) in its header — that link lives in the header, not the filename. Do not embed the lyrics version in the prompt filename: the two iterate at different rates (one lyrics version may carry prompts v1–v5), and embedding two versions creates two "prompts-v1" files
- **Never overwrite** — revisions always create a **new file**: the user may want to go back, overwriting kills A/B comparison, and the version chain *is* the song's creative record
- Every new version must state: **what changed** (a per-item table is best), **what did not change**, **path to the previous file**, why, and **options considered and rejected**

See `examples/002-versioning.md` for the header + "changed / not changed" table format.
(`outputs/` is git-ignored — never reference a specific file inside it from a committed file; the link breaks after clone.)
