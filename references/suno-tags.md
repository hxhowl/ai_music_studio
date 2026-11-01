# Suno 标签速查库

> 供 `skills/song-prompt-builder/SKILL.md` 第 2 步取标签使用。
> **结构标签（第一节）是 `lyric-zh` / `lyric-en` 的唯一事实源**，两个 skill 都不另存副本。
> **Style of Music 字段硬约束**：≤ 15 个标签、≤ 200 字符、主风格唯一、乐器 3–5 件。
>
> **取词优先级**：能用**演奏法 / 器材**就不用类别名（`brush snare` > `drums`）。
> 演奏法、质感、反差配方、编曲事件句库见 **`references/production-lexicon.md`**；
> 安全词黑名单（`dreamy` `ethereal` 等）同见该文件第一节。

---

## 一、结构标签（写在歌词里，不是 Style 字段）

| 标签 | 含义 | 常用度 |
| --- | --- | --- |
| `[Intro]` | 引子 | ★★★ |
| `[Verse]` / `[Verse 1]` | 主歌 | ★★★ |
| `[Pre-Chorus]` | 预副歌，情绪爬升 | ★★★ |
| `[Chorus]` | 副歌，记忆点 | ★★★ |
| `[Post-Chorus]` | 副歌尾缀 | ★★ |
| `[Bridge]` | 桥段，转折 / 升华 | ★★★ |
| `[Instrumental Break]` | 纯器乐间奏 | ★★ |
| `[Guitar Solo]` / `[Solo]` | 独奏段 | ★ |
| `[Hook]` / `[Refrain]` | 反复句 | ★★ |
| `[Breakdown]` / `[Drop]` | 电子乐段落 / **编曲事件落点** | ★ |
| `[Outro]` | 尾奏 | ★★★ |
| `[End]` | 结束标记 | ★ |

**元标签**（写在歌词开头或段落内）：`[Style: ...]` `[Exclude: ...]` `[Title: ...]`

> ⚠️ 这三个要**改歌词文件**，属作词侧落笔——角色二只提供内容，由角色一或用户插入。
> 作曲侧自己往词里写 = 越界（`agents/ai-song-producer.md` 边界）。
**演唱指示**：`[whisper]` `[falsetto]` `[rap]` `[spoken]` `[chant]` `[ad-lib]`
**和声**：`[harmony]` `[background vocals]` `[backing vocals]`

> ⚠️ `[Breakdown]` `[Drop]` `[whisper]` `[falsetto]` 不只是结构标记——
> 它们是 **Suno 里编曲事件的主要落点**（Style 字段只读得懂动态词，读不懂长句）。
> 事件共三个载体：① 歌词结构标签（主）② Style 动态词（辅）③ 元标签 `[Style: ...]`（补充）。
> 见 `skills/production-antislop/SKILL.md` 法则 2。

---

## 二、Style of Music 标签库

### ① 流派 / 曲风（选 1 主 + ≤1 辅）

| 大类 | 标签 |
| --- | --- |
| 流行 | `pop` `indie pop` `synth-pop` `dream pop` `electropop` `city pop` `k-pop` `j-pop` `c-pop` |
| 民谣 | `folk` `indie folk` `folk rock` `americana` `acoustic` `singer-songwriter` |
| 中国风 | `chinese style` `guofeng` `ancient style` `pentatonic` `chinese folk` |
| 摇滚 | `rock` `indie rock` `alternative rock` `punk` `post-rock` `shoegaze` `grunge` `metal` `progressive rock` |
| 电子 | `edm` `house` `deep house` `techno` `synthwave` `future bass` `dubstep` `drum and bass` `trance` `lo-fi` |
| 嘻哈 | `hip-hop` `trap` `boom bap` `lo-fi hip hop` `drill` `conscious rap` |
| R&B / 灵魂 | `r&b` `neo-soul` `soul` `motown` `funk` `gospel` |
| 爵士 | `jazz` `smooth jazz` `bebop` `bossa nova` `swing` `nu jazz` |
| 氛围 | `ambient` `cinematic`* `orchestral` `post-rock` `new age` `drone` `soundscape` |
| 拉丁 | `latin` `reggaeton` `salsa` `bossa nova` `samba` `flamenco` |
| 乡村 | `country` `country pop` `bluegrass` |
| 影视 | `film score` `trailer music` `hybrid orchestral` `epic orchestral` |

### ② 情绪 / 氛围（裸情绪词越少越好）

**可用的**：`nostalgic` `bittersweet` `hopeful` `uplifting` `euphoric` `triumphant` `heroic` `tense` `suspenseful` `dark` `brooding` `mysterious` `haunting` `tender` `yearning` `longing` `lonely` `wistful` `angry` `aggressive` `intense` `playful` `whimsical` `romantic` `sensual` `serene` `meditative` `grand` `anthemic`

> ⚠️ **不要用（安全词黑名单）**：完整清单与逐词替代写法见
> **`references/production-lexicon.md` 第一节**（唯一事实源，本文件不存副本）。
> 头号三个：`dreamy` `ethereal` `melancholic`。
> **`warm` / `intimate` 单独当情绪词同样无效**，但**带器材时有效且推荐**（`warm analog`、`intimate close-mic`）——
> 判据是：它描述的是"这张唱片怎么录的"（有效）还是"听起来感觉如何"（无效）。
> *`cinematic` 只在影视/氛围类里有效，流行歌里是泛词。

> **具体化技巧**：`lonely` → `lonely, empty subway station at 2am`（情绪词后接场景，效果显著更好）
> ⚠️ **不要数「用了几个」**——写成数字就会被当成指标去凑，凑完还是平均化。判据是有没有场景支撑。

### ③ 人声（性别 + 音色 + 语言）

| 类别 | 标签 |
| --- | --- |
| 性别 | `male vocals` `female vocals` `duet` `choir` `group vocals` `instrumental, no vocals` |
| 音区 | `deep male vocals` `baritone` `tenor` `alto` `soprano` `falsetto` `high-pitched` |
| 音色 | `breathy` `husky` `raspy` `gravelly` `smooth` `silky` `crisp` `powerful` `delicate` `airy` `clear` `nasal` `resonant` |
| 唱法 | `belting` `whisper` **`near-spoken`** `spoken word` `rap` `chant` `operatic` |
| 语言 | `mandarin` `cantonese` `english` `japanese` `korean` `mixed language` |

> ⚠️ **唱法只认上表那几个。** `vibrato` 是装饰、`ad-libs` 是即兴填充、`harmonies` 是织体——
> 它们可以单独写，但**不能顶三件套里的"唱法"这一位**。

> 💡 **性别与音区可以连写**：`female alto` / `male baritone`。闭集里的音区词
> 是"音区那半截"，单独写 `alto` 也行，但连上性别信息更多。
> ⚠️ 只有 `female vocals` / `male vocals`（不带音区、音色、唱法）时才算"没描述"。

### ④ 乐器（只点 3–5 件，**每件优先写演奏法或器材**）

> ⚠️ 下表每行开头的裸类别名（`piano` `bass` `drums` `strings` 等）**只在确实想不出演奏法时兜底**，
> 单独出现等于没描述（`production-antislop` 会指出这一点，但不判合格）。演奏法库见 `references/production-lexicon.md` 第二节。
>
> 💡 **乐器标签 = 类别（本表）+ 演奏法（lexicon 第二节）的组合**，不是固定字符串。
> 所以 `brush snare`、`felt piano`、`fingerpicked nylon-string guitar` 都不在本表里，但都合法——
> 校验时查**类别**在不在表里 + **有没有演奏法修饰**，不要要求整串匹配。

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
| 录音质感 | `lo-fi` `tape saturation` `vinyl crackle` `warm analog` `crisp digital` `raw` `polished` |
| 空间 | `reverb-heavy` `dry` `close-mic` `intimate close-mic` `spacious` `cathedral reverb` `ambient` |
| 年代 | `80s` `90s` `70s` `60s` `retro` `vintage` `modern production` `bedroom pop` |
| 响度 / 动态 | `dynamic` `compressed` `wall of sound` `sparse` `minimal` `dense` `building` `sparse intro` `dynamic contrast` `slow build` |

> ⚠️ **「响度 / 动态」这一行不算质感。** 条件 10 的质感只认**年代 / 录音方式 / 空间与介质**三行——
> `sparse intro` `building` 这类是**动态词**，用来承载编曲事件，拿它们顶质感等于条件白过。

> ⚠️ 年代词**必须配器材**才有效（`80s, gated reverb drums`）。单写 `80s` / `retro` / `vintage` 是泛词，
> 见 `references/production-lexicon.md` 第一节。

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
通用占位规则：`{vocal 音区}` `{vocal 音色}` `{vocal 唱法}` **三件必须全填**
（`female alto` + `breathy` + `near-spoken` 这种），只写 `female vocals` 等于没描述。
⚠️ **三件套的第三件是"唱法"**（音区 / 音色 / **唱法**，见第二节 ③人声表）。
`close-mic` 不是唱法，它属"空间"，可以写但要归位，不能拿它顶唱法。

紧凑流行：
{genre}, {sub-genre}, {mood1}, {mood2}, {vocal 音区}, {vocal 音色}, {vocal 唱法},
{inst1}, {inst2}, {inst3}, {bpm} BPM, {production}, {era}

纯音乐：
{genre}, instrumental, no vocals, {mood}, {inst1}, {inst2}, {inst3},
{bpm} BPM, {production}

古风（⚠️ 别用「古筝+二胡+戏腔+大混响」——那正是 `production-antislop` 的反面例子）：
guofeng, pentatonic, {vocal 音区}, {vocal 音色}, {vocal 唱法}, dry close-mic, {录音方式},
yangqin, {演奏法}, breathy xiao, muted upright bass, {反差乐器},
{bpm} BPM, sparse, dark
Exclude：no operatic vocal, no heavy reverb, no vibrato
⚠️ **这是骨架不是配方**：`{反差乐器}` 必须自己挑（古风里能形成反差的重型/电子音色），
乐器名后面必须跟演奏法。直接抄下来就成了新的罐头。

电子舞曲（⚠️ 除非明确要四踩罐头，否则不写 four-on-the-floor）：
{edm sub-genre}, {mood}, {vocal 音区}, {vocal 音色}, {vocal 唱法},
synth bass, 808 drums, saw lead, {bpm} BPM, broken beat, {production}
Exclude：no four-on-the-floor

说唱：
{hip-hop sub}, {mood}, {vocal 音区}, {vocal 音色}, rap,
{inst1}, {inst2}, {inst3}, {bpm} BPM, {production}
Exclude：no singing, no autotune
```

---

## 五、常见错误

| 错误 | 后果 | 正确做法 |
| --- | --- | --- |
| 写歌手姓名 | 平台不理解，结果随机 | 写风格要素："中国风 + R&B + 说唱段落" |
| 标签堆 30 个 | 风格糊成一团 | 砍到 15 以内，1 主 1 辅 |
| 自相矛盾 | `fast lo-fi` `intimate arena rock` | 检查互斥，**自己删掉一个并说明为什么**（别让用户二选一）|
| 只写"好听的歌" | 完全随机 | 至少给流派 + 2 个其他维度 |
| 不声明纯音乐 | 意外出现人声 | 显式写 `instrumental, no vocals` |
| 情绪词抽象 | 效果平淡 | 情绪词后接具体场景 |
| 乐器列举 10 件 | 编曲混乱 | 3–5 件核心乐器 |
