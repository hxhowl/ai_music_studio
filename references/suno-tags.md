# Suno 标签速查库

> 供 `skills/song-prompt-builder/SKILL.md` 第 2 步取标签使用。
> **Style of Music 字段硬约束**：≤ 15 个标签、≤ 200 字符、主风格唯一、乐器 3–5 件。
>
> **取词优先级**：能用**演奏法 / 器材**就不用类别名（`brush snare` > `drums`）。
> 演奏法、质感、反差配方、编曲事件句库见 **`references/production-lexicon.md`**；
> 安全词黑名单（`dreamy` `ethereal` 等）同见该文件第一节。

---

## 一、结构标签（写在歌词里，不是 Style 字段）

`[Intro]` `[Verse]` `[Verse 1]` `[Pre-Chorus]` `[Chorus]` `[Post-Chorus]` `[Bridge]` `[Hook]` `[Refrain]` `[Instrumental Break]` `[Guitar Solo]` `[Solo]` `[Breakdown]` `[Drop]` `[Outro]` `[End]`

**元标签**：`[Style: ...]` `[Exclude: ...]` `[Title: ...]`
**演唱指示**：`[whisper]` `[falsetto]` `[rap]` `[spoken]` `[chant]` `[ad-lib]`
**和声**：`[harmony]` `[background vocals]` `[backing vocals]`

---

## 二、Style of Music 标签库

### ① 流派 / 曲风（选 1 主 + ≤1 辅）

| 大类 | 标签 |
| --- | --- |
| 流行 | `pop` `indie pop` `synth-pop` `dream pop` `electropop` `city pop` `k-pop` `j-pop` `c-pop` |
| 民谣 | `folk` `indie folk` `folk rock` `americana` `acoustic` `singer-songwriter` |
| 中国风 | `chinese style` `guofeng` `ancient style` `pentatonic` `erhu` `guzheng` `chinese opera vocal` |
| 摇滚 | `rock` `indie rock` `alternative rock` `punk` `post-rock` `shoegaze` `grunge` `metal` `progressive rock` |
| 电子 | `edm` `house` `deep house` `techno` `synthwave` `future bass` `dubstep` `drum and bass` `trance` `lo-fi` |
| 嘻哈 | `hip-hop` `trap` `boom bap` `lo-fi hip hop` `drill` ` conscious rap` |
| R&B / 灵魂 | `r&b` `neo-soul` `soul` `motown` `funk` `gospel` |
| 爵士 | `jazz` `smooth jazz` `bebop` `bossa nova` `swing` `nu jazz` |
| 氛围 | `ambient` `cinematic` `orchestral` `post-rock` `new age` `drone` `soundscape` |
| 拉丁 | `latin` `reggaeton` `salsa` `bossa nova` `samba` `flamenco` |
| 乡村 | `country` `country pop` `bluegrass` |
| 影视 | `film score` `epic orchestral` `trailer music` `hybrid orchestral` |

### ② 情绪 / 氛围（选 2–3）

`melancholic` `dreamy` `ethereal` `nostalgic` `bittersweet` `hopeful` `uplifting` `euphoric` `triumphant` `heroic` `tense` `suspenseful` `dark` `brooding` `mysterious` `haunting` `intimate` `warm` `cozy` `tender` `yearning` `longing` `lonely` `wistful` `angry` `aggressive` `intense` `playful` `whimsical` `romantic` `sensual` `serene` `meditative` `epic` `grand` `cinematic` `anthemic`

> **具体化技巧**：`lonely` → `lonely, empty subway station at 2am`（情绪词后接场景，效果显著更好）

### ③ 人声（性别 + 音色 + 语言）

| 类别 | 标签 |
| --- | --- |
| 性别 | `male vocals` `female vocals` `duet` `choir` `group vocals` `instrumental, no vocals` |
| 音区 | `deep male vocals` `baritone` `tenor` `alto` `soprano` `falsetto` `high-pitched` |
| 音色 | `breathy` `husky` `raspy` `gravelly` `smooth` `silky` `crisp` `powerful` `delicate` `airy` `warm` `clear` `nasal` `resonant` |
| 唱法 | `belting` `whisper` `spoken word` `rap` `chant` `operatic` `vibrato` `ad-libs` `harmonies` `layered vocals` |
| 语言 | `mandarin` `cantonese` `english` `japanese` `korean` `mixed language` |

### ④ 乐器（只点 3–5 件，**每件优先写演奏法或器材**）

> 更多演奏法见 `references/production-lexicon.md` 第二节。

| 类别 | 标签 |
| --- | --- |
| 键盘 | `piano` `rhodes` `electric piano` `organ` `hammond organ` `synth pads` `analog synth` `arp synth` |
| 吉他 | `acoustic guitar` `electric guitar` `clean guitar` `distorted guitar` `fingerpicked guitar` `slide guitar` `12-string guitar` |
| 贝斯 | `bass` `upright bass` `synth bass` `808 bass` `slap bass` `sub bass` |
| 鼓组 | `drums` `drum machine` `808 drums` `brush drums` `taiko drums` `four-on-the-floor` `breakbeat` `tight drums` `loose drums` |
| 弦乐 | `strings` `string section` `violin` `cello` `pizzicato` `orchestral strings` |
| 管乐 | `brass` `horn section` `trumpet` `saxophone` `trombone` `flute` `clarinet` `oboe` |
| 中国乐器 | `erhu` `guzheng` `pipa` `dizi` `xiao` `sheng` `Chinese percussion` `yangqin` |
| 打击 | `shaker` `tambourine` `congas` `bongos` `hand claps` `finger snaps` `woodblock` |
| 电子音色 | `saw lead` `FM bells` `granular pads` `vinyl crackle` `tape hiss` `dub delay` |

### ⑤ 节奏 / 速度

`slow` `mid-tempo` `uptempo` `fast` `driving` `laid-back` `half-time` `four-on-the-floor` `swing` `syncopated` `polyrhythmic`
**BPM 直写**：`72 BPM` `85 BPM` `128 BPM` `140 BPM`

### ⑥ 调性（不确定就不写）

`major key` `minor key` `A minor` `C major` `modal` `dorian` `phrygian`

### ⑦ 制作质感 / 年代

| 类别 | 标签 |
| --- | --- |
| 录音质感 | `lo-fi` `tape saturation` `vinyl crackle` `warm analog` `crisp digital` `raw` `polished` `radio-ready` |
| 空间 | `reverb-heavy` `dry` `intimate close-mic` `spacious` `cathedral reverb` `ambient` |
| 年代 | `80s` `90s` `70s` `60s` `retro` `vintage` `modern production` `bedroom pop` |
| 响度动态 | `dynamic` `compressed` `wall of sound` `sparse` `minimal` `dense` `building` |

### ⑧ 地域 / 场景

`Tokyo night` `rainy city` `desert` `ocean` `mountain` `coffee shop` `late night drive` `warehouse` `church` `stadium` `bedroom`

---

## 三、Exclude Styles（负向提示，必填）

常用排除项：

`no autotune` `no vocoder` `no distortion` `no saxophone` `no brass` `no electronic drums` `no choir` `no rap` `no screaming` `no heavy reverb` `no synth` `no acoustic guitar` `no claps`

**写法**：与 Style 字段同格式，逗号分隔英文标签。

---

## 四、配方模板（可直接套）

```
紧凑流行：
{genre}, {sub-genre}, {mood1}, {mood2}, {vocal gender} vocals, {vocal timbre},
{inst1}, {inst2}, {inst3}, {bpm} BPM, {production}, {era}

纯音乐：
{genre}, instrumental, no vocals, {mood}, {inst1}, {inst2}, {inst3},
{bpm} BPM, {production}

古风：
guofeng, chinese style, ancient style, {mood}, female vocals, operatic,
guzheng, erhu, dizi, strings, {bpm} BPM, spacious reverb, cinematic

电子舞曲：
{edm sub-genre}, {mood}, {vocal}, synth bass, 808 drums, saw lead,
{bpm} BPM, four-on-the-floor, {production}

说唱：
{hip-hop sub}, {mood}, male vocals, rap, {inst}, 808 bass, {bpm} BPM,
{production}, no singing
```

---

## 五、常见错误

| 错误 | 后果 | 正确做法 |
| --- | --- | --- |
| 写歌手姓名 | 平台不理解，结果随机 | 写风格要素："中国风 + R&B + 说唱段落" |
| 标签堆 30 个 | 风格糊成一团 | 砍到 15 以内，1 主 1 辅 |
| 自相矛盾 | `fast lo-fi` `intimate arena rock` | 检查互斥，让 AI 提示用户二选一 |
| 只写"好听的歌" | 完全随机 | 至少给流派 + 2 个其他维度 |
| 不声明纯音乐 | 意外出现人声 | 显式写 `instrumental, no vocals` |
| 情绪词抽象 | 效果平淡 | 情绪词后接具体场景 |
| 乐器列举 10 件 | 编曲混乱 | 3–5 件核心乐器 |
