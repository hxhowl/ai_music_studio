# Suno 标签速查库

> 供 `skills/song-prompt-builder/SKILL.md` 第 2 步取标签使用。
> 结构标签表在 §1，`lyric-zh` / `lyric-en` 引用这里。
> **Style of Music 字段**：≤ 1000 字符（V4.5 起）、主风格唯一、乐器 3–5 件；标签 8–15 个是经验区间。
> 上限、顺序、截断行为见下面 §0。
>
> **取词优先级**：能用**演奏法 / 器材**就不用类别名（`brush snare` > `drums`）。
> 演奏法、质感、反差配方、编曲事件句库见 **`references/production-lexicon.md`**；
> 安全词黑名单（`dreamy` `ethereal` 等）同见该文件 §1。

---

## 0. Style 字段怎么读（先看这个）

| 项 | 值 | 性质 |
| --- | --- | --- |
| 字符上限 | **1000**（V4.5 / V5 / V5.5）；V4 及更早 200 | 平台限制。**超了 App 静默截断、不报错**——必须自己数 |
| 标签个数 | 8–15 个好用；超 20 个开始互相矛盾 | **经验值，不是平台限制** |
| 顺序 | 多份实操指南实测"越靠前权重越高"，官方未公布 | **惯例**：主风格放第一个。混合曲风时，先写的那个更容易占主导 |
| 分隔 | 英文逗号 + 半角空格；不写句子、不加句号 | 格式 |

**Style 读得懂什么、读不懂什么**（区分清楚，否则两边都会写错）：

| | 能不能放进 Style |
| --- | --- |
| **描述整首听起来什么样**：`close-mic'd and barely above a whisper`、`dry intimate mix with room tone` | ✅ **能**。它按自然语言描述解析，不是只认单个标签 |
| **带位置或条件的指令**：`副歌前抽掉鼓`、`第二段加弦乐` | ❌ **不能**。Style 是全局的，它没有"第几段"这个概念 |

→ 分段事件交给歌词里的结构标签；Style 只回答"整首是什么声音"。

⚠️ **不要因为上限变 1000 就把字符用满。** 多份实操指南一致：**超过约 30 个词（≈200 字符）之后，
后面的词开始互相稀释**。所以"150–300 字符"这个实用区间要分两段看：

- **150–200 字符 / 8–12 个标签**：最稳，写什么都还在被读进去
- **200–300 字符**：只在"该写的还没写完"时才用，代价是尾部几个词被稀释——值不值，看那一件有多关键
- **300 以上**：基本白写，除非有非写不可的东西

上限放宽的用处只有一条——**不必为了不超过 200 而砍掉关键的那一件**，不是让你把额度填满。

---

## 1. 结构标签（写在歌词里，不是 Style 字段）

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
| `[End]` | 结束标记，**写在歌词最后一行** | ★ |

**`[End]` 什么时候加**：写在歌词最后一行，意思是"歌词到此结束，别再往后加"。
不加时模型常在尾奏多 noodle 10–20 秒。它**不改变你已经写的那几句尾奏**——
要渐弱，就把渐弱写进尾奏那几句，最后补一个 `[End]` 收住，两者不冲突。

**元标签**（写在歌词开头或段落内）：`[Style: ...]` `[Exclude: ...]` `[Title: ...]`

> ⚠️ 这三个也落在歌词文件里。**角色二可以直接插入标签**，但**不能改动一个词**——
> 标签归作曲侧，词归作词侧，界线就这一条（`agents/ai-song-producer.md` 边界）。
> 插入后歌词要出新版本（`AGENTS.md` 条件 1）。
**演唱指示**：`[whisper]` `[falsetto]` `[rap]` `[spoken]` `[chant]` `[ad-lib]`
**和声**：`[harmony]` `[background vocals]` `[backing vocals]`

> ⚠️ `[Breakdown]` `[Drop]` `[whisper]` `[falsetto]` 不只是结构标记——
> 它们是 **Suno 里编曲事件的主要落点**（Style 是全局描述，没有"第几段"这个概念）。
>
> ⚠️ **两类标签的可靠性不一样**：结构标签（`[Verse]` `[Chorus]` `[Breakdown]` `[Instrumental Break]`）
> 平台**当作编排指令**执行；表演标签（`[whisper]` `[falsetto]` `[spoken]`）**更像建议**，会被弱化。
> 所以关键事件优先用结构标签；表演标签最多 1–3 个词，写长了更容易被忽略。
> 事件共三个载体：① 歌词结构标签（主）② Style 动态词（辅）③ 元标签 `[Style: ...]`（补充）。
> 见 `skills/production-antislop/SKILL.md` 法则 2。

---

## 2. Style of Music 标签库

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
| 爵士 | `jazz` `smooth jazz` `bebop` `swing` `nu jazz` |
| 氛围 | `ambient` `cinematic`* `orchestral` `new age` `drone` `soundscape` |
| 拉丁 | `latin` `reggaeton` `salsa` `bossa nova` `samba` `flamenco` |
| 乡村 | `country` `country pop` `bluegrass` |
| 影视 | `film score` `trailer music` `hybrid orchestral` `epic orchestral` |

### ② 情绪 / 氛围（裸情绪词越少越好）

**可用的**：`nostalgic` `bittersweet` `hopeful` `uplifting` `euphoric` `triumphant` `heroic` `tense` `suspenseful` `dark` `brooding` `mysterious` `haunting` `tender` `yearning` `longing` `lonely` `wistful` `angry` `aggressive` `intense` `playful` `whimsical` `romantic` `sensual` `serene` `meditative` `grand` `anthemic`

> ⚠️ **不要用（安全词黑名单）**：完整清单与逐词替代写法见
> **`references/production-lexicon.md` §1**。
> 头号三个：`dreamy` `ethereal` `melancholic`。
> **`warm` / `intimate` 单独当情绪词同样无效**，但**带器材时有效且推荐**（`warm analog`、`intimate close-mic`）——
> 判据是：它描述的是"这张唱片怎么录的"（有效）还是"听起来感觉如何"（无效）。
> *`cinematic` 只在影视/氛围类里有效，流行歌里是泛词。

> **具体化技巧**：情绪词后面接**这个场景的边角**（几点、在哪、旁边有什么），不要接形容词。
> 具体写成什么，取决于这首歌的场景——**别照抄任何一个现成例子**，那会变成下一个安全词组合。
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

> ⚠️ 下表每行开头是**类别**（`piano` `bass` `drums` `strings` 等）。**类别名不能单独出现**——
> 条件 8 要的是每件乐器都带演奏法或器材。想不出演奏法时，往**具体器材**退一步
> （`Rhodes`、`upright bass`、`808 drums`），不要退回裸类别名。演奏法库见 `references/production-lexicon.md` §2。
>
> 💡 **乐器标签 = 类别（本表）+ 演奏法（lexicon §2）的组合**，不是固定字符串。
> 所以 `brush snare`、`felt piano`、`fingerpicked nylon-string guitar` 都不在本表里，但都合法——
> 校验时查**类别**在不在表里 + **有没有演奏法修饰**，不要要求整串匹配。

| 类别 | 标签 |
| --- | --- |
| 键盘 | `piano` `rhodes` `electric piano` `organ` `hammond organ` `synth pads` `analog synth` `arp synth` |
| 吉他 | `acoustic guitar` `electric guitar` `clean guitar` `distorted guitar` `fingerpicked guitar` `slide guitar` `12-string guitar` |
| 贝斯 | `bass` `upright bass` `synth bass` `808 bass` `slap bass` `sub bass` |
| 鼓组 | `drums` `drum machine` `808 drums` `brush drums` `taiko drums` `breakbeat` `tight drums` `loose drums` |
| 弦乐 | `strings` `string section` `violin` `cello` `pizzicato` `orchestral strings` |
| 管乐 | `brass` `horn section` `trumpet` `saxophone` `trombone` `flute` `clarinet` `oboe` |
| 中国乐器 | `erhu` `guzheng` `pipa` `dizi` `xiao` `sheng` `Chinese percussion` `yangqin` |
| 打击 | `shaker` `tambourine` `congas` `bongos` `hand claps` `finger snaps` `woodblock` |
| 电子音色 | `saw lead` `FM bells` `granular pads` `dub delay` |

### ⑤ 节奏 / 速度

`slow` `mid-tempo` `uptempo` `fast` `driving` `laid-back` `half-time` `four-on-the-floor` `swing` `syncopated` `polyrhythmic`
**BPM 直写**：优先**区间** `85-92 BPM` `120-128 BPM`——区间给生成器留调整余地，单值等于替它定死了；
单值 `92 BPM` 只在用户明确指定时用。

### ⑥ 调性（不确定就不写）

`major key` `minor key` `A minor` `C major` `modal` `dorian` `phrygian`

### ⑦ 制作质感 / 年代

**三行 = 条件 10 的三个维度**（选其中两行即可，别跨行混算）：

| 维度 | 标签 |
| --- | --- |
| **录音方式**（话筒距离 / 录制手法） | `close-mic` `intimate close-mic` `single-mic live take` `room mics` `direct-in` `re-amped` |
| **空间与介质**（房间感 / 载体） | `dry` `reverb-heavy` `spacious` `cathedral reverb` `spring reverb` `plate reverb` `ambient` `tape hiss` `tape saturation` `vinyl crackle` `lo-fi` |
| **年代** | `80s` `90s` `70s` `60s` `modern production`；`retro` `vintage` 单用是泛词，配上器材才立得住 |

**不算质感的第四类**（不属于上面任何一行，别拿它顶条件 10）：
`dynamic` `compressed` `wall of sound` `sparse` `minimal` `dense` `building` `sparse intro` `dynamic contrast` `slow build`——这些是**动态词**，用来承载编曲事件。

> ⚠️ **不要用合写去凑两项。** 条件 10 数的是**维度**，不是字符串里有没有空格——
> `dry close-mic` 拆开就是 `dry`（空间与介质）+ `close-mic`（录音方式）；写成一个标签也行，
> 但你得**说得出这两件事各自是什么**，否则老实拆成两个。
> **动态词（`sparse intro` `building`…）不管写几个，都不构成质感维度。**

> ⚠️ 年代词**单独写是泛词**，配上器材才立得住（`80s, gated reverb drums`）。
> 单写 `80s` / `retro` / `vintage` 仍然算一个年代维度，但它没告诉模型任何具体的音色，见 `references/production-lexicon.md` §1。

### ⑧ 地域 / 场景

`Tokyo night` `rainy city` `desert` `ocean` `mountain` `coffee shop` `late night drive` `warehouse` `church` `stadium` `bedroom`

---

## 3. Exclude Styles（负向提示，**建议填，不是条件**）

**写纯词，不写 `no`。** 这个字段本身就是"要排除的风格"，加 `no` 等于给它一个叫 `no autotune` 的风格名。

常用排除项：

`autotune` `vocoder` `distortion` `saxophone` `brass` `electronic drums` `choir` `rap` `screaming` `heavy reverb` `synth` `acoustic guitar` `claps` `four-on-the-floor`

**写法**：与 Style 字段同格式，英文逗号分隔；**≤ 200 字符**（所有版本都是 200。
V4.5 起 Style 放宽到 1000，Exclude 没动——**真正的窄口是这一项**）。

**该写什么**：不是"我不喜欢的"，是**这个风格最可能的失败形态**（见 `production-antislop` 法则 6）。

---

## 4. 配方模板（可直接套）

```
通用占位规则：`{vocal 音区}` `{vocal 音色}` `{vocal 唱法}` **三件必须全填**
（`female alto` + `breathy` + `near-spoken` 这种），只写 `female vocals` 等于没描述。
⚠️ **三件套的第三件是"唱法"**（音区 / 音色 / **唱法**，见 §2 ③人声表）。
`close-mic` 不是唱法，它属**录音方式**（话筒距离，见 ⑦），可以写但不要拿它顶唱法。

紧凑流行：
{genre}, {sub-genre}, {mood1}, {mood2}, {vocal 音区}, {vocal 音色}, {vocal 唱法},
{inst1}, {inst2}, {inst3}, {BPM 区间}, {production}, {era}

纯音乐：
{genre}, instrumental, no vocals, {mood}, {inst1}, {inst2}, {inst3},
{BPM 区间}, {production}

古风（⚠️ 别用「古筝+二胡+戏腔+大混响」——那正是 `production-antislop` 的反面例子）：
guofeng, pentatonic, {vocal 音区}, {vocal 音色}, {vocal 唱法}, close-mic, {空间与介质},
yangqin, {演奏法}, breathy xiao, muted upright bass, {反差乐器},
{BPM 区间}, sparse, dark
Exclude：operatic vocal, heavy reverb, vibrato
⚠️ **这是骨架不是配方**：`{反差乐器}` 要自己挑（古风里能形成反差的重型/电子音色），
乐器名后面要跟演奏法（条件 8）。直接抄下来就成了新的罐头。

电子舞曲（⚠️ 除非明确要四踩罐头，否则不写 four-on-the-floor）：
{edm sub-genre}, {mood}, {vocal 音区}, {vocal 音色}, {vocal 唱法},
synth bass, 808 drums, saw lead, {BPM 区间}, broken beat, {production}
Exclude：four-on-the-floor

说唱：
{hip-hop sub}, {mood}, {vocal 音区}, {vocal 音色}, rap,
{inst1}, {inst2}, {inst3}, {BPM 区间}, {production}
Exclude：singing, autotune
```

---

## 5. 常见错误

| 错误 | 后果 | 正确做法 |
| --- | --- | --- |
| 写歌手姓名 | 平台不理解，结果随机 | 写风格要素："中国风 + R&B + 说唱段落" |
| 标签堆 30 个 | 风格糊成一团 | 砍到 15 以内，1 主 1 辅 |
| 自相矛盾 | `fast lo-fi` `intimate arena rock` | 检查互斥，**自己删掉一个并说明为什么**（别让用户二选一）|
| 只写"好听的歌" | 完全随机 | 至少给流派 + 2 个其他维度 |
| 不声明纯音乐 | 意外出现人声 | 显式写 `instrumental, no vocals` |
| 情绪词抽象 | 效果平淡 | 情绪词后接具体场景 |
| 乐器列举 10 件 | 编曲混乱 | 3–5 件核心乐器 |
