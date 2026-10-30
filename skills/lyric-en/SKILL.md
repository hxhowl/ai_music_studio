---
name: lyric-en
description: 英文语境歌词创作与打磨。按 Suno 通用英文结构标签产出规范化英文歌词，涵盖 rhyme scheme 设计、音节数与重音对齐、韵族选择、hook 设计。当用户要写英文歌词、改英文词、设计押韵方案时使用。
---

# English Lyric Writing

## Iron Rules

1. **Section tags are Suno-standard English**, bracketed: `[Verse]`, `[Chorus]`, etc.
2. Lyrics are **sung, not read**. Every line must be singable in one breath.
3. Stress alignment matters more than syllable count in English. A line with the right syllable count but the wrong stress pattern is unsingable.

---

## 1. Section Tag Library (Suno standard)

| Tag | Use |
| --- | --- |
| `[Intro]` | Opening |
| `[Verse]` / `[Verse 1]` | Story, imagery |
| `[Pre-Chorus]` | Build / lift |
| `[Chorus]` | Payoff, hook |
| `[Post-Chorus]` | Hook tail |
| `[Bridge]` | Turn / reveal |
| `[Instrumental Break]` | Instrumental section |
| `[Guitar Solo]` / `[Solo]` | Solo section |
| `[Hook]` / `[Refrain]` | Repeated line |
| `[Breakdown]` / `[Drop]` | Electronic sections |
| `[Outro]` | Closing |
| `[End]` | End marker |

**Meta / delivery tags**: `[Style: ...]`, `[Exclude: ...]`, `[harmony]`, `[background vocals]`, `[backing vocals]`, `[whisper]`, `[falsetto]`, `[rap]`, `[spoken]`, `[chant]`, `[ad-lib]`

---

## 2. Structure Templates

> Durations are computed at each template's **typical BPM** (running everything at 85 BPM badly
> underestimates fast templates). ※ = narrative-tag / short-line-repeat chorus; it may run
> under 15 sec (see the exception in §4).

| # | Template | Structure (numbers = **line counts**) | Typical BPM | Chorus | Whole song | Best for |
| --- | --- | --- | --- | --- | --- | --- |
| **T1** | Ballad | Intro - V1(4) - PC(2) - C(6) - V2(4) - PC(2) - C(6) - B(4) - C(6) - Outro(3) | 85 | 16.9s | ≈ 1:56 | Slow, short verse / long chorus |
| **T2** | Standard Pop | Intro - V1(6) - PC(3) - C(6) - V2(6) - PC(3) - C(6) - B(4) - C(6) - Outro(3) | 95 | 15.2s | ≈ 2:10 | Mainstream, hook-forward |
| **T3** | Story Folk | V1(8) - V2(8) - C(4) - V3(8) - C(4) - B(5) - C(4) - Outro(3) | 90 | 10.7s※ | ≈ 2:09 | Narrative, verse-heavy |
| **T4** | Build | Intro - V1(4) - C(6) - V2(4) - C(6) - B(4) - C(6) - **C(8)** - Outro(3) | 85 | 16.9→22.6s | ≈ 2:07 | Final chorus extended to a peak |
| **T5** | Short-form | Intro - V1(4) - PC(2) - C(6) - C(6) - Outro(2) | 100 | 14.4s | ≈ 1:08 | 60–90s, social clips |
| **T6** | Rap-led | Intro - V1(16) - C(4) - V2(16) - C(4) - B(6) - C(8) - Outro(4) | 90 | 10.7s※ | ≈ 2:46 | Multi-syllabic rhyme in verses |
| **T7** | Long-line | Intro - V1(4) - PC(2) - C(4) - V2(4) - PC(2) - C(4) - B(4) - C(4) - Outro(2) | 90 | 21.3s | ≈ 2:36 | Long lines (2 bars each), few lines / many words |
| **T8** | EDM / Dance | Intro - V1(4) - PC(2) - Drop(4) - Br - V2(4) - PC(2) - Drop(4) - Drop(6) - Outro(2) | 128 | 7.5s※ | ≈ 2:19 | Instrumental-heavy (vocals only 0:52) |
| **T9** | R&B / Neo-soul | Intro - V1(6) - PC(2) - C(8) - V2(6) - PC(2) - C(8) - B(4) - C(8) - Outro(3) | 92 | 20.9s | ≈ 2:24 | Long chorus, runs and melisma |

### How to pick (**don't just take the familiar one**)

Offering nine templates with no selection rule means the first one gets picked — the same failure
mode as "given a range, take the minimum." Narrow it down in four steps:

1. **Target length**: 60–90 sec → **T5 only**; 2:00–3:30 → the rest
2. **What carries the song**: chorus-led (emotional, cathartic) → T1/T4/T9; verse-led (narrative, rap) → T3/T6; balanced → T2; instrumental-led → T8
3. **How many choruses, and do they vary**: three with variation → chorus of 6; final one must peak → extend to 8 (T4); chorus only restates the title → 4
4. **Genre overrides**: long-line / Chinese-style → T7; EDM → T8; R&B → T9; rap → T6

**Don't add every optional section by default**: Pre-Chorus may be dropped in T3/T4/T5;
Bridge can be replaced by an instrumental break in T5/T6; `[Instrumental Break]` is the carrier
for arrangement events — add it only when you need a solo or an emptied-out contrast.

State **why** you chose this template. Line counts are decided in §4, not copied blindly.

---

## 3. Rhyme Systems

### Rhyme schemes

| Scheme | Pattern | Feel |
| --- | --- | --- |
| **AABB** | Couplets | Simple, folk, nursery-solid |
| **ABAB** | Alternating | Forward motion, classic pop |
| **ABCB** | 2nd/4th only | Relaxed, conversational |
| **AABA** | Three same + turn | Vintage, jazzy |
| **AAAA** | Monorhyme | Driving, rap / chant |

### Rhyme types

| Type | Definition | Example |
| --- | --- | --- |
| **Perfect** | Identical vowel + coda | night / light |
| **Slant (near)** | Approximate | bridge / inch |
| **Assonance** | Vowel match only | time / light |
| **Consonance** | Coda match only | bill / wall |
| **Internal** | Rhyme inside the line | "I **crash** and I **burn**" |
| **Multi-syllabic** | 2+ syllables | "mo**tiva**tion" / "ele**va**tion" |
| **Rich** | Same spelling, diff. meaning | lie (deceive) / lie (recline) |

### Rhyme families (see `references/rhyme-en.md` for full tables)

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

- **Chorus**: lock one family, slant allowed on 1 line max
- **Verse**: looser, ABAB or ABCB, internal rhyme for density
- **Bridge**: often switch family entirely = audible turn
- **Multi-syllabic rhyme** reads as high craft; use in rap or final verse
- Avoid forcing: "the **light** of my **sight**" is filler

---

## 4. Line Count & Meter — **never default to 4 lines**

### ⚠️ Common failure

**Given a range with no selection rule, the model picks the minimum.** Result: every section is 4 lines —
the whole song runs ~1:38 (a third shorter than a standard pop song), the chorus arrives and leaves in 11 seconds,
**so the emotion never has time to land**. And equal line counts across sections is structural "AI symmetry."

**Line count is calculated, not guessed.**

### Syllables & stress

English is stress-timed. Align **both**:

| Section | Syllables / line |
| --- | --- |
| Verse | 8–12 |
| Pre-Chorus | 5–8 |
| Chorus | 7–12 |
| Bridge | 6–10 |
| Outro | 4–8 |
| **Long-line styles** (Chinese-style, ambient) | **14–20** — one line spans 2 bars; **use fewer lines** (see long-line check below) |

**Stress check**: read the line aloud and tap the beat. The natural word stress must land on the beat.
- ✅ "I **walk** a**lone** at **mid**night" — stress lands on beats
- ❌ "A**lone** I **walk** in the **night**" — fights the pulse unless intended

**Rule of thumb**: within a section, corresponding lines must match syllable count within ±2 AND stress position.

### Step 1 — derive from BPM

```
seconds per line ≈ 240 ÷ BPM        (4/4 time, one line ≈ one bar; long lines = 2 bars)
lines = target seconds ÷ seconds per line
```

| Section | Target |
| --- | --- |
| **Chorus** | **15–22 sec** (below this = "the emotion doesn't land") |
| Verse | 10–20 sec (ballads may take the lower end) |
| Pre-Chorus | 6–10 sec |
| Bridge | 10–16 sec |
| Outro | 8–15 sec |
| **Whole song** | **2:00–3:30** |

Example: 85 BPM + 18-sec chorus → 18 ÷ 2.82 ≈ **6 lines**. 120 BPM + 16 sec → **8 lines**.

> **Exception: a narrative-tag chorus may run under 15 sec.** In folk and rap the chorus often
> only restates the title (4 lines ≈ 10–12 sec). It builds memory through **how many times it
> arrives** (4×, 40+ sec of total exposure), not through one long statement.
> The 15–22 sec band is for **build-type choruses**, where the emotion has to climb inside a
> single pass.

### Step 2 — chorus length by emotional job (outranks genre)

| Chorus job | Lines |
| --- | --- |
| **Build** (heartbreak, confession, anthemic) | **6–8** |
| **One punch** (attitude, punchline, snark) | 4 |
| **Narrative tag** (folk; chorus only restates the title) | 4 |
| **Atmosphere** (dream pop; timbre over information) | 4–6 (long lines) |
| **Needs 3-verse variation** | **6** |

### Step 3 — vary line counts between sections

| Ratio | Use |
| --- | --- |
| Verse 4 / Chorus 6 | Ballad — short story, long feeling |
| Verse 6 / Chorus 6 | **Standard pop only** (the sole exception — contrast comes from the Pre-Chorus and energy, not line count) |
| Verse 8 / Chorus 4 | Folk narrative, rap |
| Verse 4 / Chorus 8 | Catharsis, rock |

⚠️ The axis is **function**, not position:

| Relation | Line count | Why |
| --- | --- | --- |
| **Repeats of the same function** (V1↔V2, C1↔C2↔C3, PC1↔PC2) | **Must be equal** | Same melody, same phrase — different counts make it unsingable |
| **Verse ↔ chorus ↔ pre-chorus** | **Should differ** | Each owns a melody; the same count everywhere = structural "AI symmetry" |
| Bridge / outro | **May match the above** | One-off sections with their own melody — no need to force a difference |

> Don't write "adjacent sections must not have equal line counts." Followed literally it makes
> V1 and V2 differ — but both verses share one melody, so they can't.

### Long-line styles: check total syllables, not lines

A 14-syllable line spans 2 bars, so 4 lines is not 11 sec but ~21 sec.
**The real constraint is total duration (or total syllables), not line count.**

| Chorus shape | Total syllables | Verdict |
| --- | --- | --- |
| 4 × 7 = 28 | 28 | Short — only for fast songs / one-punch attitude |
| 6 × 9 = 54 | 54 | Comfort zone — standard ballad |
| 8 × 8 = 64 | 64 | Catharsis / stacking |
| 4 × 14 = 56 | 56 | Long-line — few lines, plenty of syllables; equally valid |

Target: **chorus ≈ 45–90 syllables total**.

### Inside a 6-line chorus

```
Line 1    hook at the opening, sets the memory      (same all 3 times)
Line 2    expands the hook                          (same all 3 times)
Line 3    push / give an image                      (same all 3 times)
Line 4    ★ VARIATION SLOT: emotional state shifts  (different each time)
Lines 5-6 landing / scene closes                    (same all 3 times; scene doesn't follow mood)
```

Full tables (BPM lookup, genre × line count, template library, how to pick): **`references/song-structure.md`**.

**State at delivery**: which template (T1–T9) and why; lines per section and why (BPM + emotional job + duration check).

---

## 5. Writing Flow

```
① Nail the premise — one concrete sentence, not an abstract mood word
② Set BPM (if unknown, use the genre default — it drives line count)
③ Pick a template (T1–T9, §2 four steps) + set line counts: §4 three-step (BPM → emotional job → section variance)
   Output a table: which template, lines per section, target seconds, why
④ Pick rhyme family for chorus; lock it
⑤ Call lyric-imagery-rhyme for image clusters + rhyme word bank
⑥ Verse — concrete nouns + verbs, no commentary
⑦ Pre-Chorus — shorter lines, rising
⑧ Chorus — hook at line OPENING, written to the line count decided in ③, leave a variation slot
⑨ Bridge — switch rhyme family / perspective, say the real thing
⑩ Outro — fewer words, fade
⑪ Self-check (includes line count + duration)
```

**Division of labour**:
- Verse = **images** (concrete nouns, actions)
- Chorus = **attitude** (emotion + repetition)
- Bridge = **the turn** (what verse and chorus never said)

---

## 6. Common Failure Modes

| Problem | Symptom | Fix |
| --- | --- | --- |
| Forced rhyme | "the light of my sight" | Rewrite so the rhyme word is the *only* right word |
| Stress clash | Right syllables, wrong accents | Retap the beat, move the word |
| Abstract pile-up | lonely, broken, lost, hollow | Swap for concrete: cold coffee, unread text |
| Dead chorus | Every line is new | Put hook at line 1, repeat 2–3x |
| POV drift | I / you / he mixed | Keep one; bridge may switch |
| Unsungable | Too many syllables in one breath | Split or cut |

---

## 7. Naturalness Red Lines (prevent while drafting)

**The root cause of AI-sounding lyrics is averaging** — if anyone could have written it, it belongs to no one. Hold these at the drafting stage; don't leave it for a post-write fix.

- **Three questions per line**: can a camera film it? would it still work in a different song? is there one detail nobody else would write?
- **≥ 3 concrete nouns per verse**; **≤ 3 abstract emotion words** in the whole song
- **≥ 1 contemporary object**: 12% battery, a delivery note, a read receipt, the last train, a locker pickup code
- **Generic imagery must be qualified**: not "rain" — "the kind of rain that flips your umbrella"
- **Vary line length**: keep the opening lines aligned, then let **one line (usually the last)** run clearly longer or shorter as a landing line. Never all lines equal (fake), never all over the place (unsingable)
- **Heavier emotion, lighter wording**: not "I miss you till I cry" — "your toothbrush is still in the cup"

Replacement words: `references/anti-ai-lexicon.md`. Full rules and rewrite flow: `skills/lyric-naturalness/SKILL.md`.

---

## 8. Self-Check Before Delivery

**Craft**
- [ ] Tags are Suno-standard English, bracketed
- [ ] Chorus rhyme family consistent; verse scheme stated
- [ ] Syllable + **stress** aligned within sections
- [ ] Read aloud — no tongue-twisters, no forced rhymes
- [ ] Verse has ≥5 concrete nouns; chorus has attitude
- [ ] No artist names, brands, or unpronounceable proper nouns
- [ ] Hook is at the opening of the chorus

**Line count (§4)**
- [ ] **Not every section is 4 lines** — counts derived from BPM + emotional job, not the minimum
- [ ] Chorus runs 15–22 sec; whole song 2:00–3:30
- [ ] **Repeats of the same function have equal line counts** (V1=V2, C1=C2); verse and chorus differ
- [ ] Delivery states which template, lines per section, and why

**Format & versioning (§9, §10)**
- [ ] Lyrics inside a code block, one line per lyric line, **no blank lines between lines**, one blank line between sections
- [ ] Revisions wrote a **new file** with a version number; the original was not overwritten
- [ ] New version states what changed, what didn't, and the previous file path

## 9. Formatting (hard rules)

### Lyric block

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
| Delivery tags | `[whisper]` `[falsetto]` on their own line, before the section |
| Empty sections | Instrumental-only (`[Intro]`, `[Instrumental Break]`) — tag only, then one blank line |

> ⚠️ **Never put a blank line between every lyric line** — that's paragraph format, not lyric format,
> and it pastes into Suno full of empty lines.

### Delivery document

```markdown
# Lyrics · "{Title}" v1        ← v1 is explicit; no "first version omits it" special case

> Version note: what changed vs. previous; path to previous file

## 1. Lyrics                   ← code block, copy-paste ready
## 2. Structure & Line Count   ← lines per section, why (BPM + job + duration)
## 3. Rhyme Check
## 4. Design Notes
## 5. Self-Check
```

## 10. Versioning & Output

### Folder layout

One folder per song; both lyrics and prompts live inside it:

```
outputs/{song}/
  {song}-lyrics-v1-20261030.md
  {song}-prompts-v1-20261030.md
  {song}-lyrics-v2-20261031.md
  ...
```

### Naming

| Type | Filename |
| --- | --- |
| Lyrics | `outputs/{song}/{song}-lyrics-v{N}-YYYYMMDD.md` |
| Prompts | `outputs/{song}/{song}-prompts-v{N}-YYYYMMDD.md` |

- **v1 is explicit** — no special case where the first file omits the version
- Lyrics and prompts **each increment independently**; numbers are globally unique, never reset or reused
- Date = **the day of the revision**, not the first version's date. Date goes last so files sort by type + version
- A prompt file must state **which lyrics version it was built from** (by path) in its header — that link lives in the header, not the filename

> Do not embed the lyrics version in the prompt filename (e.g. `-lyrics-v1-prompts-v1-`).
> The two iterate at different rates (changing BPM or tone doesn't touch the lyrics, so one
> lyrics version may carry prompts v1–v5), and a wording-only lyrics revision often needs no
> prompt change at all. Embedding two versions also creates two "prompts-v1" files, so every
> version reference would need a prefix to stay unambiguous.

### Hard rule: never overwrite

Revisions always create a **new file**. Reasons:

1. Iteration is trial and error — the user may want to go back ("v2's chorus was better")
2. Overwriting kills A/B comparison
3. The version chain *is* the song's creative record

### Every new version must state

- What changed vs. the previous version (a per-item table is best)
- **Path to the previous file**
- **What did NOT change** (so the user doesn't think the whole song was rewritten)
- Why this change, plus **options considered and rejected** and why

See `examples/002-versioning.md` for the header + "changed / not changed" table format.
(`outputs/` is git-ignored — never reference a specific file inside it from a committed file; the link breaks after clone.)
