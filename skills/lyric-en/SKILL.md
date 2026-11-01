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

**Rhyme density** (state your choice; don't drift into it):

| Section | Default | Lines that may go unrhymed | Where |
| --- | --- | --- | --- |
| **Verse** | ABAB / ABCB (every other line) is fine in English — stress carries the pulse | up to 1 extra | not the last line |
| **Chorus** | lock the family; **no unrhymed line** | 0 (slant ≤ 1) | — |
| Pre-chorus | either; an unrhymed last line makes a good lift | 1 | last line |
| Bridge | may switch family; density may loosen | up to 1/3 | at the switch |
| Outro | a broken rhyme to close is allowed | — | last line |

⚠️ English and Chinese differ here on purpose: Chinese defaults to **rhyming every line** because it
doesn't lean on word stress to hold the pulse; English defaults to every-other-line.
Don't copy one language's density into the other.
⚠️ **Rhyming every line doesn't mean reusing the same rhyme word.** But judge "identical rhyme"
by **how it sounds**, not by a poetry manual:

| Case | Verdict |
| --- | --- |
| **Two adjacent lines** end on the same word | **Lazy — fix it.** Back-to-back, the ear catches it instantly |
| Same word 2+ lines apart, **deliberately echoing** | **It's a device — keep it** (chorus question/answer, hook refrain, anaphora) |
| Same word 2+ lines apart, just out of words | Audible but tolerable; swap for another word in the family if you can |
| The **same word 3+ times** in one section | Thin no matter the spacing — fix it |

> Traditional Chinese prosody forbids repeating a rhyme word anywhere in a stanza, adjacent or not —
> that's an exam rule, and pop songs don't obey it. Listeners don't count how many times "zoo" shows
> up; they hear it immediately when two lines in a row land on it.
> Real case: 「这是不是个动物园 / … / 这是疯狂的动物园」— the same character 3 lines apart, forming a
> question-and-answer frame. **That's structure, not a flaw. Don't "fix" it.**

---

## 3. Line count & meter — never default to 4 lines

Given a range with no selection rule, the model picks the minimum. Result: every section is 4 lines — the whole song runs ~1:51 (below the 2:00 floor), the chorus arrives and leaves in 11 seconds, **so the emotion never has time to land**. Equal line counts across sections is structural "AI symmetry." **Line count is calculated, not guessed.**

### Decision flow

> Every lookup table, template library and conversion table lives in **`references/song-structure.md`**
> (single source of truth). This section holds only the flow — every number lives in that file,
> **go read the relevant section there when you set line counts**; don't work from memory.
> Section numbers below all refer to **`references/song-structure.md`**.

| Step | What | Where |
| --- | --- | --- |
| ① Pick template | Narrow to T1–T9 in four steps; **don't take the familiar one** | §7 |
| ② Set BPM | Use the user's if given; else take the **template's typical BPM** and state it | §8 |
| ③ Count lines | `sec/line ≈ 240 ÷ ACTUAL BPM`; chorus floor then comes from its emotional job | §2, §4 |
| ④ Validate | Chorus duration, whole-song duration, line-count relations | §2, §5, §8 |

### Three things that trip people up (① and ③ are conditions; ② is a reference)

**① A template gives the skeleton; recalculate line counts at the actual BPM.**
Measured: T2's 6-line chorus at 120 BPM = 12 sec, below the floor.
⚠️ **Validate with the actual BPM too** — checking against the template's 95 BPM returns 15.2 sec and a false pass.
At 120 BPM the fix is **8 lines + `[Post-Chorus]`**, not 9 lines (a 9-line chorus is overlong for pop).
The verse usually stays: 6 lines fits the 10–20 sec band from 70 to 140 BPM.

**② A chorus usually runs 15–22 sec — but this is a reference, not a floor.**
- 15 sec is an empirical band measured at 85 BPM, not a constant. At high BPM **keep the lines and let
  the seconds fall short** — cutting lines to hit a number destroys information and fixes the wrong thing.
  Buy time with `[Post-Chorus]` or another repeat
- A narrative-tag chorus (folk, rap) may run as short as 10 sec; it builds memory through repetitions
- **Duration is not a condition** — it follows the genre (90-sec punk and 5-min post-rock are both fine).
  The reference ranges are in `AGENTS.md` §5. What condition 4 checks is *equal line counts*, not length

**③ Line-count relations go by function, not position.**
- **Repeats of the same function must be equal** (V1=V2, C1=C2, PC1=PC2) — same melody; unequal counts are unsingable
- **Verse ↔ pre-chorus ↔ chorus should differ** — the same count everywhere is structural "AI symmetry"
- Bridge / outro **may match** those (one-off sections with their own melody)
- ⚠️ Never write "adjacent sections must not have equal line counts" — followed literally, V1 and V2 end up different, but they share one melody and can't be

### Syllables & stress

English is stress-timed. Align **both**:

| Section | Syllables / line (**reference range**, 85 BPM baseline) |
| --- | --- |
| Verse | 8–12 |
| Chorus | 7–12 |
| Pre-Chorus | 5–8 |
| Bridge | 6–10 |
| Outro | 4–8 |
| **Long-line styles** (Chinese-style, ambient) | **14–20** — one line spans 2 bars; use fewer lines |

**Stress check**: you can't hear it, so do it on paper — mark each line's primary stresses, number the
metrical positions (1–4 for 4/4), and see whether they line up. Word stress must land on the beat.
- ✅ "I **walk** a**lone** at **mid**night" — stress lands on beats
- ❌ "A**lone** I **walk** in the **night**" — fights the pulse unless intended

> ⚠️ **This is a reference, not a cap.** How much fits in one breath depends on the melody, the
> phrasing, the pauses and who's singing — **±2 is completely normal**.
> **Never damage a better line to hit a syllable count.** Real case: `我说 哥 周一还得交周报`
> (the most human line in the song) was rewritten to `我烦恼 周一汇报还得交` to cut syllables and
> force an AABB — zero gain, pure loss, and the self-check still passed it.

**Syllables move with BPM too**: the table above assumes ~85 BPM. The practical limit is one breath —
at **90–110 BPM → 10–13 syllables**, 120–140 → **8–11**, 160+ → **6–8**.
English caps are **1.2–1.5× the Chinese character counts** (English carries more syllables per bar,
but consonants cap its throughput, so the multiplier shrinks as tempo rises).
Full table: `references/song-structure.md` §2.

### Mixed language

Lines of another language inside an English lyric are common, but **structure follows the main
singing language**.

| Question | Rule |
| --- | --- |
| Which skill | Follow the **main singing language**: English-led → this skill; Chinese-led → `lyric-zh` |
| Counting | English parts by syllable; a **whole Chinese line** by characters (1 character ≈ 1 syllable) |
| Rhyme | English parts follow their rhyme family; Chinese words don't join it — **don't expect cross-language rhymes** |
| Placement | Hook, the last chorus line, or the pre-chorus lift — the spot must be **fixed and repeat 2–3 times** |
| Singability | Chinese parts still need **tone-to-melody** care — see `lyric-zh` §2 on 倒字 (*dàozì*: a word sung on the wrong melodic contour is heard as a different word), or the meaning gets misheard |

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
⓪ **Lock the scene + write the anchor line** (before anything else)
   · Scene boundary: what time / where / what the person is doing / what objects actually exist
     e.g. not "lonely" — "00:47, last train, three people in the carriage, phone at 4%"
     Skip it and you write lines that fit any song
   · ★ **The anchor line**: the one line that sounds most like a real person — write it first
     (it's often the title). ⚠️ This line has the highest priority — it wins every conflict.
     **It comes before the song.** Can't find it? You haven't found the song yet — don't proceed
   · **Not enough information?** Invent one concrete scene, state it in one line, and start
     ("I'll write it as the last train at 00:47 — stop me if that's wrong").
     ⚠️ Don't keep interrogating, and don't write something generic — **the user correcting a concrete
     draft is much faster than staring at a blank page**

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
   (Write the verse first and you don't know what it's travelling toward — that's how you get
   six parallel shots instead of a lyric)

④ **Set the structure (backwards from the chorus)**
   Template skeleton (T1–T9, **skeleton only**) + actual BPM + lines per section + **duration check**
   — all at once, so you're not rebuilding at the end

⑤ **Pick the rhyme family (changeable later)**
   See where the chorus naturally lands and **use that**; switch if it fights you.
   ⚠️ **Never let rhyme decide content.** In the priority order rhyme sits below "sings like speech";
   it must not be locked before you write anything

⑥ Verse — **the road to that chorus line**. Ask first: what state must this start from for the
   chorus to be earned? Images and actions, no commentary; each verse is **one chain of action**,
   not a shot list
   → Pre-Chorus (shorter lines, rising) → Bridge (switch rhyme family / perspective, say the real
   thing) → Outro (fewer words, fade)

⑦ **Cut — this step is not a "self-check"**
   Ask of every line: **would the song be worse without it?** If not, cut it.
   Then scan top to bottom: **is there a line you'd want to skip?** That's the one to fix.
   (Don't write "read it aloud" — you can't hear it, see Iron Rule 2.
   No rule-ticking — the rules are reference, not delivery conditions)
```

**Division of labour**: verse = **images** (concrete nouns, actions); chorus = **attitude** (emotion + repetition); bridge = **the turn** (what verse and chorus never said).

**Each later verse must move one step beyond the previous one** (not just V2 — T3 and T6 have three verses):
equal line counts (same melody) don't mean the content may repeat.
V1 sets the scene, V2 advances it — shift the time ("three days later"),
**shift what is being observed** (V1 watches her own hands, V2 watches his;
⚠️ the observed *object* shifts, **not the narrative person** — POV stays one throughout,
only the bridge may switch), or let an object planted in V1 change by V2 (V1: "phone at 4%" → V2: "it died").
⚠️ Just rephrasing V1 is exactly what the "each later verse advances" item in `lyric-naturalness` catches as "repetition in new words".

**How to build a hook** (having one isn't enough — it has to be memorable and singable):

| Point | Rule |
| --- | --- |
| **Placement** | **First line of the chorus** (heard first), then repeated at the last line or in `[Post-Chorus]` to close the loop |
| **Length** | **Shorter than the surrounding lines** — if the chorus runs 8 syllables, make the hook 5–6 (the hook is the one exception to the ±2 alignment rule) |
| **Open vowels** | Prefer open vowels (ah / ay / oh); closed ones (ee / oo) don't carry and get swallowed |
| **Repetition** | Repeat verbatim 2–3 times, **unchanged**; if the three choruses vary, vary **line 4** (the standard variation slot in a 6-line chorus), never the hook |
| **Content** | It's the title or a near-paraphrase of it; **no abstract emotion words** ("it'll be okay" doesn't stick) |

⚠️ A hook that changes all three times is no hook. Leave the variation to **line 4**
(the standard variation slot in a 6-line chorus) — don't touch lines 1–3: line 2 *develops* the hook,
so changing it dismantles the hook itself.
(See `references/song-structure.md` §4 for the full 6-line chorus layout.)

---

### What gives way when things conflict

Formal metrics fight each other, and they fight the quality goal. **The priority order is fixed**:

> **private voice > sings like speech > rhyme > syllable alignment**

**Conditions that never yield** (only these four; everything else gives way):
tag format, equal line counts for repeats of the same function, singability.

⚠️ **Duration is not in this list** — it varies by genre (90-sec punk, 5-min post-rock).
Making it a condition would force padding or cutting lines just to hit seconds.

⚠️ **"Suno ≤200 characters" is NOT a lyric-side condition** — that limit applies to the Style
field, i.e. to prompts. Lyrics have no character limit. Don't mix the two sides up.

⚠️ **The per-line syllable cap is NOT one of them** — it's a reference, not a hard limit.
It used to be written as "must be satisfied no matter what", and the result was a model that kept
asking to cut syllables and damaged better lines. **Sacrificing a line to hit a syllable count is
the wrong trade.**

| Conflict | Who wins |
| --- | --- |
| A line only he would say, but it's too long | **Keep the line**; tighten the lines around it |
| A line that reads perfectly but doesn't rhyme | **Keep the line**; change the rhyme word or the neighbours |
| Perfect rhyme, awkward line | The rhyme gives way |
| Even syllables, but it reads fake | Alignment gives way (ragged edges are wanted anyway) |

### No deferring: make the call

The second face of defensiveness — **refusing to judge, pushing the decision back to the user.**

❌ Real output (《疯狂动物园》 v7):

> "Both images work: this version emphasises 'animals at leisure in high society', the lion-barber
> version emphasises 'animals doing human service work'. **Whichever you prefer.**"
> "**Two things you could keep or drop.**"

They asked you to write; you handed back a menu. Same disease as over-justifying: **not taking
creative responsibility.**

| Never write | Write instead |
| --- | --- |
| both work, whichever you prefer | I chose A because (one reason) |
| keep it or drop it / or you could | (just decide) |
| if you want it more restrained, swap to X | already swapped to X (if it really is better) / don't mention it |

**If you want to offer an alternative, one sentence max**: "The other direction is X; I picked Y
because Z." Then stop.

⚠️ **Never sacrifice a line that already passed the private-voice test just to fix a formal metric.**

Actual case (2026-10-31, 《疯狂动物园》): `我说 哥 周一还得交周报` was rewritten to
`我烦恼 周一汇报还得交` to force an AABB pattern in the bridge — **but 报 and 好 are both in the
same rhyme family, so that line never needed to change.** The most human line in the whole song was
damaged for no real gain, and the self-check still passed it.

**If you must touch such a line, state why it's worth it in the change table.** No reason, no change.

---

## 5. Common failure modes

| Problem | Symptom | Fix |
| --- | --- | --- |
| Forced rhyme | "the light of my sight" | Rewrite so the rhyme word is the *only* right word |
| Stress clash | Right syllables, wrong accents | Re-mark the stresses and count beats again, then move the word |
| Abstract pile-up | lonely, broken, lost, hollow | Swap for concrete: cold coffee, unread text |
| Dead chorus | Every line is new | Put hook at line 1, repeat 2–3x |
| POV drift | I / you / he mixed | Keep one; bridge may switch |
| Unsungable | Too many syllables in one breath | Split or cut |

---

## 6. Naturalness red lines (prevent while drafting)

**The root cause of AI-sounding lyrics is averaging** — if anyone could have written it, it belongs to no one. Hold these at the drafting stage; don't leave it for a post-write fix.

- **Three questions per line**: can a camera film it? would it still work in a different song? is there one detail nobody else would write?
- **Details a camera could film — but don't count them.** Hitting some noun quota is how you end up
  with a shot-list; the number is not the point
- ⚠️ **Details must chain, not pile up**: every line picks up from the one before, and the last line
  completes an action or a turn. Counting nouns is the fastest way to write a shot-list instead of a
  lyric (this actually happened — see `lyric-naturalness` rule 1).
  Tests: **the deletion test** (delete any line — does the next one still connect? if yes, nothing was
  connected) and **the subject test** (are 6 lines carrying 6 unrelated subjects?)
- **Keep one through-line object**: bring the same object back **once, and change its state**
  (still on the lanyard → chewed up → still there). A brand-new object every section passes
  every per-section check yet leaves the song with no spine — objects must **carry the story**,
  not decorate it
- **A contemporary object**: 12% battery, a delivery note, a read receipt, the last train, a locker pickup code
  (not something that could equally sit in a song from 1990)
- **Generic imagery must be qualified**: not "rain" — "the kind of rain that flips your umbrella"
- **Vary line length**: keep the opening lines aligned, then let **one line (usually the last)** run clearly longer or shorter as a landing line. Never all lines equal (fake), never all over the place (unsingable)
- **Heavier emotion, lighter wording**: not "I miss you till I cry" — "your toothbrush is still in the cup"

Replacement words: `references/anti-ai-lexicon.md`. Full rules and rewrite flow: `skills/lyric-naturalness/SKILL.md`.

---

## 7. Delivery check

### Check conditions 1–5 of `AGENTS.md` §4

This file **does not restate them** — conditions live in one place only (four copies had begun
to drift). Go read those five: **versioning / section tags / formatting / structural sanity / singable**.

> If all pass, write one sentence — no ticking, no score. **Nothing outside those five is a gate.**

### Below is the diagnostic table — **consult it when stuck, not as a delivery gate**

> This is "what good lyrics look like", **not "what counts as acceptable lyrics"**.
> **If it flows, don't read this.** Open it only when something feels off and you can't name it.
> ⚠️ Treating these as gates is what makes a model optimise for conditions instead of writing a good
> song — a mistake made for real on 2026-10-31.

**Overall arc (start here if it "doesn't hold together")**
- [ ] **Narrative line**: the song traces an emotional change from first line to last
      (⚠️ a change of *scene* is not a change of *emotion*)
- [ ] **Line-to-line relation**: pick 3 pairs of adjacent lines; for each you can name the relation
      (cause / escalation / turn / contrast). "They're all describing X" means it's a list, not a lyric
- [ ] **The chorus is inevitable**: it's forced out by the verse, not a new topic
- [ ] **Each section's last line travels further than its first** (there's an arc inside a section too)
- [ ] **One object comes back once and its state has changed** (a through-line, not decoration)

**Line craft (open when it "doesn't read like a lyric")**
- [ ] Chorus rhyme family consistent; verse scheme stated; **density meets the default (§2)** —
      chorus has no unrhymed line, verse at most one and not the last
- [ ] **Identical rhyme judged by ear**: adjacent lines on the same word = fix; 3+ uses in one
      section = fix; a deliberate echo across lines (chorus frame, hook refrain) **is not a flaw** (§2)
- [ ] Syllable + **stress** aligned within sections
- [ ] **Sibilance/tongue-twister check** (don't write "read it aloud" — you can't hear it):
      three or more consecutive words starting on the same consonant; no forced rhymes
- [ ] **Hook meets all five points**: chorus line 1, shorter than neighbours, open vowels,
      verbatim 2–3×, and it is the title
- [ ] **Each later verse advances** (new time / new observed object / a planted object changed),
      not a rephrase of the previous one
- [ ] Verse gives images, chorus gives attitude, bridge gives the turn

**Naturalness (open when it "reads like AI"), §6**
- [ ] Details a camera could film — **not counted** (counting is what produces a shot-list)
- [ ] **Details chain, they don't pile up** — passes the deletion test and the subject test,
      not one object per line
- [ ] A contemporary object is present; generic imagery is qualified
- [ ] At least one line only this person would say; line lengths vary
      (highest-priority signal here — it marks what's most worth fixing, it doesn't fail the song)

**Line count (open when "the structure feels off"), §3**
- [ ] **Not every section is 4 lines** — counts derived from BPM + emotional job, not the minimum
- [ ] Whole-song duration sits in the normal band for its genre (≈2:00–3:30 for a standard single, 60–90s for a clip)
- [ ] If the chorus runs past 22 sec, it is **stated and handled** (cut a line / convert to repeats) —
      22 sec is a soft ceiling (T4's final chorus is 22.6s and still a valid template), so going over
      isn't an error; going over silently is
- [ ] Verse and chorus differ in line count
- [ ] **The chorus hasn't eaten the song**: chorus time ≤ 40% of total (≤ 50% for hook/clip templates), ≤ 4 choruses
- [ ] **The template's rationale matches the actual structure** — if you picked T4 "final chorus extended",
      it really is extended; don't leave the two disconnected
- [ ] With ≥ 3 choruses there is a lift or a gap somewhere (pre-chorus / instrumental / strip-out),
      not chorus after chorus
- [ ] Delivery states template, actual BPM and its source, lines per section, and any adjustment vs the template

**On the "pass mark"**

Only the five gates at the top have a pass mark. **The diagnostic table has no pass mark** —
it's a toolbox, not an exam. Anything it turns up goes through the rewrite flow in
`lyric-naturalness`; the **private-voice** item is the highest-priority signal there,
but it doesn't fail the song.

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

> Previous: outputs/{song}/…-v0-20260101.md    ← write "none" for the first version

## Lyrics                   ← code block, copy-paste ready

---
**One line each**: what you chose (template / BPM), what changed, what still bothers you —
**five lines max**.
```

**That's it.** They asked for a song, not a case file.

### Expand only when asked

| They ask | You give |
| --- | --- |
| "Why this structure?" | template, actual BPM and its source, why that many lines |
| "How does the rhyme work?" | family + density (how many lines unrhymed, and where) |
| "What imagery did you use?" | image cluster + why this family |
| "Did you self-check?" | only what **failed**; all clear = one sentence |

⚠️ **Don't volunteer the expansions.** Across seven real revisions the commentary ran 61–69% of the
file — the reader had to page through a full screen of justification before reaching the song
(`AGENTS.md` §4 「交付形态」).

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
