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

| Template | Structure | Best for |
| --- | --- | --- |
| **Standard Pop** | Intro - V1 - PC - C - V2 - PC - C - B - C - Outro | Mainstream, hook-forward |
| **Story Folk** | V1 - V2 - C - V3 - C - B - C - Outro | Narrative, verse-heavy |
| **Build** | Intro - V1 - C - V2 - C - B - C - C - Outro | Emotional escalation |
| **Short-form** | Intro - V - PC - C - C - Outro | 60–90s, social clips |
| **Rap-led** | Intro - V1(rap) - C - V2(rap) - C - B - C - Outro | Multi-syllabic rhyme in verses |

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

## 4. Meter: Syllables + Stress

English is stress-timed. Align **both**:

| Section | Syllables / line | Lines |
| --- | --- | --- |
| Verse | 8–12 | 4–8 |
| Pre-Chorus | 5–8 | 2–4 |
| Chorus | 7–12 | 4–6 |
| Bridge | 6–10 | 2–4 |
| Outro | 4–8 | 2–4 |

**Stress check**: read the line aloud and tap the beat. The natural word stress must land on the beat.
- ✅ "I **walk** a**lone** at **mid**night" — stress lands on beats
- ❌ "A**lone** I **walk** in the **night**" — fights the pulse unless intended

**Rule of thumb**: within a section, corresponding lines must match syllable count within ±2 AND stress position.

---

## 5. Writing Flow

```
① Nail the premise — one concrete sentence, not an abstract mood word
② Pick structure template
③ Pick rhyme family for chorus; lock it
④ Call lyric-imagery-rhyme for image clusters + rhyme word bank
⑤ Verse — concrete nouns + verbs, no commentary
⑥ Pre-Chorus — shorter lines, rising
⑦ Chorus — hook at line OPENING, high repetition, wording fixed
⑧ Bridge — switch rhyme family / perspective, say the real thing
⑨ Outro — fewer words, fade
⑩ Self-check
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

- [ ] Tags are Suno-standard English, bracketed
- [ ] Chorus rhyme family consistent; verse scheme stated
- [ ] Syllable + **stress** aligned within sections
- [ ] Read aloud — no tongue-twisters, no forced rhymes
- [ ] Verse has ≥5 concrete nouns; chorus has attitude
- [ ] No artist names, brands, or unpronounceable proper nouns
- [ ] Hook is at the opening of the chorus

## 9. Output

Save to `outputs/YYYYMMDD-{song}-lyrics.md`, following the output format in `agents/ai-lyricist.md`.
