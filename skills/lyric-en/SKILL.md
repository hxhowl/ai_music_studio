---
name: lyric-en
description: 英文语境歌词创作与打磨。按 Suno 通用英文结构标签产出规范化英文歌词，涵盖 rhyme scheme 设计、音节数与重音对齐、韵族选择、hook 设计。当用户要写英文歌词、改英文词、设计押韵方案时使用。
---

# English Lyric Writing

## Iron Rules

1. **Section tags are Suno-standard English**, bracketed, on their own line.
2. Lyrics are **sung, not read**. Every line must be singable in one breath.
3. Stress alignment matters more than syllable count in English — a line with the right syllable count and the wrong stress pattern is unsingable.
4. **One action per line.** A line that packs three clauses (subject–verb, subject–verb, subject–verb) is a prose sentence, not a lyric. Structures that need a pause to finish — comparative clauses (`earlier than my sigh`), stacked pre-modifiers (`my overhead-eave school uniform`) — leave nowhere for the breath to land.

---

## 1. Section tags & templates

### Tags

Full table (frequency ratings, meta tags, delivery tags): `references/suno-tags.md` §1 — single source; both lyric skills read from it, so don't keep a second copy here. Three things to remember:

1. **English, bracketed, own line**: `[Intro]` `[Verse]` `[Pre-Chorus]` `[Chorus]` `[Post-Chorus]` `[Bridge]` `[Instrumental Break]` `[Outro]` `[End]`
2. **`[Breakdown]` `[Drop]` `[whisper]` `[falsetto]` are where arrangement events land**, not just structural markers (Suno's Style field can't parse sentences)
3. **Instrumental-only sections carry the tag and nothing else** — one blank line after, no prose underneath

### Templates (starting points, not a menu)

> ⚠️ **These nine are where to start, not the set of options.** Real songs go far beyond them —
> AABA, chorus-first, through-composed, five-verse folk ballads, two-chorus short forms.
> **Change them, combine them, or design your own**; the table only helps when you don't know
> where to begin.
>
> Line counts are deliberately **not listed here** — they come from the **emotional job** (§4)
> and the subject relation, *not* from tempo.
> **`references/song-structure.md` §2, §3, §4**.

| Template | Style | Tempo band |
| --- | --- | --- |
| T1 | Ballad | slow |
| T2 | Standard pop | mid |
| T3 | Story folk | mid |
| T4 | Build (final chorus extended) | slow |
| T5 | Short-form (60–90 sec; the only short template) | fast |
| T6 | Rap-led (verse carries the song) | mid |
| T7 | Long-line (2 bars per line) | mid |
| T8 | EDM / dance (instrumental-heavy) | fast |
| T9 | R&B / neo-soul (long chorus) | mid |

> **No BPM numbers here on purpose** — the lyric side only needs a tempo band to judge line length.
> Numbers and ranges belong to the production side (`song-structure.md` §6 maps bands to syllables).

**Four-step narrowing — don't take the familiar one** (offering nine templates with no selection rule means the first one gets picked):

1. **Scale**: clip / short-form (about a minute) → **T5 only**; a full song → the rest
2. **What carries the song**: chorus-led (emotional, cathartic) → T1/T4/T9; verse-led (narrative, rap) → T3/T6; balanced → T2; instrumental-led → T8
3. **How many choruses, do they vary**: three with variation → T1/T2/T4; final must peak → T4;
   chorus only restates the title → T3/T6 (**no line counts here** — write the chorus, then count; see §4)
4. **Genre overrides**: long-line / Chinese-style → T7; EDM → T8; R&B → T9; rap → T6

**None of the nine fit? Build your own.** Order sections by what this song needs, not by what's
in the table. Test it against four things: **every section has a job / the chorus repeats enough /
long songs need air / the energy moves** (the four tests at the end of §3 in
`references/song-structure.md`). Meet those and any order works; miss them and no template saves it.

**A template gives**: which sections, in what order, how many repeats; advice on optional sections; a tempo band (not a number).
**It does not give**: line counts (they come from how much the emotion needs to say), BPM numbers or
ranges (production side), or total runtime.

Don't add optional sections by default: Pre-Chorus may be dropped in T3/T4/T5; Bridge can be an instrumental break in T5/T6.
Be able to say **why** you chose this template (if asked — don't volunteer it).

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

> ⚠️ **Anadiplosis (chaining) may leave one line unrhymed — that's a device, not loose density.**
> When a line opens on the previous line's final word ("...getting **closer** / **closer** than I can
> hear"), it has to land in a different family to make the chain work.
> **The test is strict**: the next line must actually open with that word. Otherwise it's an ordinary
> broken rhyme and the table above applies.

⚠️ English and Chinese differ here on purpose: Chinese defaults to **rhyming every line** because it
doesn't lean on word stress to hold the pulse; English defaults to every-other-line.
Don't copy one language's density into the other.
⚠️ **Rhyming every line doesn't mean reusing the same rhyme word.** But judge "identical rhyme"
by **how it sounds**, not by a poetry manual:

| Case | Verdict |
| --- | --- |
| **Two adjacent lines** end on the same word, different structure | **Lazy — fix it.** Back-to-back, the ear catches it instantly |
| Two adjacent lines end on the same word, but it's **parallel structure** (identical frame, one word swapped) | **It's a device — keep it** — "wait three more minutes / hold three more minutes". The repetition is the escalation.<br>Test: strip the final word — is the rest of the two lines built the same way? Then it's parallelism |
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

Given a range with no selection rule, the model picks the minimum — so every section gets 4 lines. Two reasons why that fails:

- **A 4-line chorus**: one pass of the hook and it's gone. Nothing sticks. Building emotion needs at least 6 lines — line 1 plants it, line 2 opens it, line 3 pushes it
- **Equal counts everywhere (4/4/4/4)**: structural "AI symmetry." Real songs run a longer chorus than verse (ballads) or a shorter one (story songs) — **they almost never match**

**Line count comes from how much the emotion needs to say — not from seconds.**

### Decision flow

> Every lookup table, template library and conversion table lives in **`references/song-structure.md`**
> (single source of truth). This section holds only the flow — every number lives in that file,
> **go read the relevant section there when you check line counts**; don't work from memory.
> Section numbers below all refer to **`references/song-structure.md`**.

| Step | What | Where |
| --- | --- | --- |
| ① Pick template | Narrow to T1–T9 in four steps; **don't take the familiar one** | §3 |
| ② Set tempo band | Keep the user's number if they gave one; otherwise pick **slow / mid / fast** — **no numbers** (ranges belong to production) | §6 |
| ③ Count lines | **Count what you wrote**, then check it against the emotional job's range | §4 |
| ④ Check relations | Repeats equal; verse / pre-chorus / chorus differ | §5 |

> ⚠️ **Line count is decided by how much the emotion needs to say — not calculated.**
> Deriving it from seconds means every section is padding, and no line has a reason to exist.

### Three things that trip people up

**① A template gives the skeleton — line counts come from writing, not from the template.**
The numbers in the table are that template's *typical shape*, not a spec.
Write the chorus first, then **count what came out** and check it against §4's ranges — that's all.
**Don't decide the line count before the chorus exists.** Filling a pre-set number of slots is the
same failure as writing to a syllable quota.

**② A chorus runs as long as it takes to land the emotion — that's the only test.**
- Cutting lines to hit a duration destroys information; **adding lines to reach one is the same mistake in
  reverse.** If the chorus feels short, the fix is usually a `[Post-Chorus]` or another repeat — a new
  section, not a longer chorus
- A narrative-tag chorus (folk, rap) can be much shorter; it builds memory through repetitions
- **Duration is not a condition** — it follows the genre (90-sec punk and 5-min post-rock are both fine).
  Reference ranges are in `AGENTS.md` §5. What condition 4 checks is *equal line counts*, not length

**③ Line-count relations go by function, not position.**
- **Repeats of the same function must be equal** (V1=V2, C1=C2, PC1=PC2) — same melody; unequal counts are unsingable
- **Verse ↔ pre-chorus ↔ chorus should differ** — the same count everywhere is structural "AI symmetry"
- Bridge / outro **may match** those (one-off sections with their own melody)
- ⚠️ **Judge by function, not position** — judging by position writes V1 and V2 with different counts, but they share one melody and can't be sung.

### Stress & breath

English is stress-timed, so **stress placement matters more than syllable count**:

**Stress check**: you can't hear it, so do it on paper — mark each line's primary stresses, number the
metrical positions (1–4 for 4/4), and see whether they line up. Word stress must land on the beat.
- ✅ "I **walk** a**lone** at **mid**night" — stress lands on beats
- ❌ "A**lone** I **walk** in the **night**" — fights the pulse unless intended

> ⚠️ **This is a reference, not a cap.** How much fits in one breath depends on the melody, the
> phrasing, the pauses and who's singing — **±2 is completely normal**.
> **Never damage a better line to hit a syllable count.** Real case: `我说 哥 周一还得交周报`
> (the most human line in the song) was rewritten to `我烦恼 周一汇报还得交` to cut syllables and
> force an AABB — zero gain, pure loss, and the self-check still passed it.

### Line length: no table, one test

**A line has to be singable in one breath.** That's the whole rule.

- Faster songs naturally carry shorter lines; slower songs can stretch
- Long-line styles (Chinese-style, ambient) span 2 bars — roughly twice the syllables of a normal line
- **No syllable table.** Syllable count is a *result* of tempo and phrasing, not a target to write toward

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

**Rule of thumb**: within a section, corresponding lines should match in syllable count (roughly) AND stress position. Stress matters more.
**Long-line styles: length lives in syllables, not line count** — 4 long lines feel like 8 normal ones.

**Explainable if asked** (don't volunteer it, see `AGENTS.md` §4 delivery form): which template (T1–T9) and why; the tempo band; lines per section and why.
**Don't deliver a duration calculation.** The user asked for structure, not an arithmetic table.

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
Template skeleton (T1–T9, **skeleton only**) + lines per section + tempo band
Line counts come from the emotional job (chorus) and the subject relation (verse); tempo only changes line length, not counts

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
⚠️ Just rephrasing V1 is still repetition — the verse must move (new time / new observed object / a planted object changed), not restate.

**How to build a hook** (having one isn't enough — it has to be memorable and singable):

| Point | Rule |
| --- | --- |
| **Placement** | **First line of the chorus** (heard first), then repeated at the last line or in `[Post-Chorus]` to close the loop |
| **Length** | **Usually shorter than the surrounding lines** — if the chorus runs 8, try 5–6. Not a rule: the hook can be the longest line if it's the most memorable (it's the exception to the ±2 alignment rule) |
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

**Conditions that never yield** (only these five; everything else gives way):
versioning, tag format, formatting, equal line counts for repeats of the same function, singability.

⚠️ **Duration is not in this list** — it varies by genre (90-sec punk, 5-min post-rock).
Making it a condition would force padding or cutting lines just to hit seconds.

⚠️ **"Suno ≤200 characters" is NOT a lyric-side condition** — that limit applies to the Style
field, i.e. to prompts. Lyrics have no character limit. Don't mix the two sides up.

⚠️ **The per-line syllable cap is NOT one of them** — it's a reference, not a hard limit.
**Sacrificing a line to hit a syllable count is the wrong trade.**

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

### A lyric line is not a prose sentence

The fastest way to write something that reads like a diary entry instead of a song:
**transcribe the scene with full clauses.** Two people in a scene makes it worse — it turns into dialogue.

| Prose | Lyric |
| --- | --- |
| The rain really came down, so you pulled me under the eaves | School uniform held up — that was our eave |
| You said it would rain, and I left my umbrella in the classroom | Only said it wouldn't rain, didn't argue |
| You carried the noodles over and stood by the door | One bowl of noodles, standing by the door |

**Three checkable differences:**

1. **How many actions in one line** — prose packs two or three clauses; a lyric lands one
2. **Whether the subject is stated** — English usually needs it, but **don't give every action its own
   "I… you…"**; when two actions share one subject, let them share it
3. **Conjunctions** — `so` / `because` / `and then` in a lyric line means you're narrating events

**One talking head, not two.** Don't alternate dialogue; **juxtapose two actions from the same side**:

❌ `You said it would rain, I left my umbrella in class` — two subjects, two actions, ping-pong
✅ `Only said it wouldn't rain, didn't argue` — one side, two actions; the other person shows up in "didn't argue"

> **Test**: two or more subject switches in one line = prose. Keep the pronouns only where the
> *relationship itself* is the content (`You're my most accurate forecast`, `Others watch clouds, I watch your eyes`).

### Everything else

| Problem | Symptom | Fix |
| --- | --- | --- |
| Forced rhyme | "the light of my sight" | Rewrite so the rhyme word is the *only* right word |
| Stress clash | Right syllables, wrong accents | Re-mark the stresses and count beats again, then move the word |
| Abstract pile-up | lonely, broken, lost, hollow | Swap for concrete: cold coffee, unread text |
| Dead chorus | Every line is new | Put hook at line 1, repeat 2–3x |
| POV drift | I / you / he mixed | Keep one; bridge may switch |
| Unsungable | Too many syllables in one breath, or a comparative clause that needs a pause to finish | Split or cut |

---

## 6. Naturalness — three sights to keep in view (all of them point at *less*)

**The root cause of AI-sounding lyrics is averaging** — if anyone could have written it, it belongs to no one.

Only three things to watch while drafting:

1. **Could a camera film it?** You can't film "loneliness", you can film "your toothbrush still in the cup".
   Same for imagery: not "rain" — "the kind of rain that flips your umbrella"
2. **Heavier emotion, lighter wording** — not "I miss you till I cry", but "I never deleted it"
3. **One object comes back once, and its state has changed** (still on the lanyard → chewed up → still there)

⚠️ These are **sights, not a checklist** — look at them when you're stuck, don't walk through them one by one.

Still not reading like a person? Go to the **five rewrites** in `skills/lyric-naturalness/SKILL.md`
(drop the subject / drop the explaining / merge lines / cut the last line).
Replacement words: `references/anti-ai-lexicon.md`.

---

## 7. Delivery check

### Check conditions 1–5 of `AGENTS.md` §4

This file **does not restate them** — conditions live in one place only.
Go read those five: **versioning / section tags / formatting / structural sanity / singable**.

> If all pass, write one sentence — no ticking, no score. **Nothing outside those five is a gate.**

### Below is the diagnostic table — **consult it when stuck, not as a delivery gate**

> This is "what good lyrics look like", **not "what counts as acceptable lyrics"**.
> **If it flows, don't read this.** Open it only when something feels off and you can't name it.
> ⚠️ Treating these as gates is what makes a model optimise for conditions instead of writing a good
> song — a mistake made for real on 2026-10-31.

**Overall arc (start here if it "doesn't hold together")**
- [ ] **A direction**: the emotion or situation moves from first line to last
      (⚠️ a change of *scene* is not a change of *emotion*). It does **not** have to be a story —
      the eye moving downward (lift → corridor → neck → bed) counts
- [ ] **Lines are held together by something**: pick 3 pairs of adjacent lines; for each you can name
      the relation (cause / escalation / turn / contrast, **or juxtaposition** — two sides of one scene).
      ⚠️ **Juxtaposition is not a list.** A list is six unrelated things with no line through them
- [ ] **The chorus is inevitable**: it's forced out by the verse, not a new topic
- [ ] **Each section ends somewhere** — its last line stops at a place; it may travel further than the first, or simply settle
- [ ] **One object comes back once and its state has changed** (a through-line, not decoration)

**Line craft (open when it "doesn't read like a lyric")**
- [ ] **Not every line says "who did what"** — two or more subject switches in a line is a prose sentence
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
- [ ] **Details have a line through them, not a pile** — passes the deletion test, and you can supply
      the same subject for each line (supply it — don't write it out), not one object per line
- [ ] **Not every line says "who did what"** — two or more subject switches in a line is prose
- [ ] A contemporary object is present; generic imagery is qualified
- [ ] At least one line only this person would say; line lengths vary
      (highest-priority signal here — it marks what's most worth fixing, it doesn't fail the song)

**Line count (open when "the structure feels off"), §3**
- [ ] **Not every section is 4 lines** — counts come from the emotional job, not the minimum
- [ ] Verse and chorus differ in line count (equal is fine — T2/T7 do it; then pre-chorus and energy contrast have to tell them apart)
- [ ] **The chorus hasn't eaten the song**: ≤ 4 choruses — that's the only hard half. Two identical adjacent choruses are fine; the difference can come from performance and arrangement. **Never change a better line just to make the second chorus differ**
- [ ] **The template's rationale matches the actual structure** — if you picked T4 "final chorus extended",
      it really is extended; don't leave the two disconnected
- [ ] With ≥ 3 choruses there is a lift or a gap somewhere (pre-chorus / instrumental / strip-out),
      not chorus after chorus
- [ ] Be able to say (if asked) which template, the tempo band, lines per section — **don't volunteer it**

**On the "pass mark"**

Only the five gates at the top have a pass mark. **The diagnostic table has no pass mark** —
it's a toolbox, not an exam. Anything it turns up goes through the five rewrites in `lyric-naturalness`.

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
**One line each**: what you chose (template / tempo band), what changed, what still bothers you —
**five lines max**.
```

**That's it.** They asked for a song, not a case file.

### Expand only when asked

| They ask | You give |
| --- | --- |
| "Why this structure?" | template, tempo band and why, lines per section |
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
- Every new version must state: **what changed** (a per-item table is best), **path to the previous file**, and why.

**Do not write "what did not change" or "options considered and rejected"** — that's self-justification.
Revisions that only touch wording need nothing beyond the change table. Format: `examples/002-versioning.md`.
(`outputs/` is git-ignored — never reference a specific file inside it from a committed file; the link breaks after clone.)
