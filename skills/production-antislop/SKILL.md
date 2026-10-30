---
name: production-antislop
description: 编曲提示词反套路与去同质化。诊断"安全词组合"问题（dreamy/ethereal 等通胀词、只有音色属性没有编曲事件、乐器只写类别名、缺录音质感、Exclude 空泛），按六条法则改写为有专属锚点、有时间轴、有反差、有质感的提示词。当用户说"出来的歌都一个样""太套路""没特点""像别人的歌""编曲太素""不够抓耳"时使用；也用于提示词交付前的差异化自检。
---

# 编曲反套路：去同质化

## 病理：AI 出歌雷同 = 安全词组合 + 只有属性没有事件

歌词侧的 AI 味是"感受的统计平均"，编曲侧是**"标签的排列组合"**。

`dreamy, ethereal, melancholic, female vocals, breathy, piano, strings` ——
每个词都正确，但**每个词都被用烂了**。模型对它们的响应早已收敛到最大公约数，写进去等于没写。

> **这条提示词换掉其中任意两个词，出来的歌会明显不同吗？不会，就是安全词组合。**

还有第二个更隐蔽的病：**提示词全是名词，没有动词。**
真人的编曲最有力量的是"什么时候发生什么"——副歌前抽掉所有乐器、桥段突然插一个不该出现的音色。
这部分几乎没人写，因为 Style 字段看起来只该填属性。

**总判据**：提示词里有没有一条指令是**别的歌不会写的**？没有，就是平均化的。

---

## 六条法则

### 1. 去安全词 —— 情绪词不能裸用

`references/production-lexicon.md` 第一节列了黑名单。两类处理：

- **场景化**：`lonely` → `lonely, empty subway station at 2am`（情绪词后接具体场景）
- **转质感**：`dreamy` → `half-speed tape, washed-out reverb`（换成可执行的声音参数）

**硬约束**：裸情绪词 ≤ 2 个，且必须带限定或直接换成质感词。

### 2. 写事件，不只写属性 —— 至少 1 条时间轴指令

提示词必须包含至少一条**"在第 X 段发生 Y"**的指令。

| 平台 | 怎么落 |
| --- | --- |
| **Suno** | Style 字段写不下长句。事件落在：① 歌词**结构标签**（`[Instrumental Break]` `[Breakdown]` `[Drop]` `[Guitar Solo]` `[whisper]`）；② Style 里的**动态词**（`sparse intro` `building` `dynamic contrast`）；③ 元标签 `[Style: ...]` |
| **秒响** | **直接写中文时间轴**。这是秒响相对 Suno 最大的优势区，不用白不用 |

**最好用的一招**：桥段或最后一次副歌前做一次**"抽空"**——留 2–4 秒只剩人声，再全员进入。
留白之后的爆发，比一路堆满有力得多。

> ⚠️ 常见错误：把"副歌前抽掉鼓"塞进 Suno 的 Style 字段。它读不懂长句，
> 正确做法是写 `dynamic contrast` + 在歌词里插 `[Breakdown]`。

### 3. 至少一个专属锚点（三选一，反差最强）

| 锚点类型 | 做法 | 例 |
| --- | --- | --- |
| **反差音色**（最有效） | 加一件**不该出现在这个风格**的乐器 | 古风里的 `808 sub bass`；电子里的 `solo cello` |
| **演奏法/器材** | 把乐器名换成"怎么演" | `brush snare` 而非 `drums`；`felt piano` 而非 `piano` |
| **质感设定** | 写成"这张唱片怎么录出来的" | `single-mic live take, 70s tape saturation` |

**只加一件，并说明出现在哪一段。** 加多了就是风格混乱，不是反差。

配方表见 `references/production-lexicon.md` 第四节。

### 4. 质感维度必填 —— 年代 / 录音方式 / 空间与介质，三选二

**这是最少人写、区分度最高的一维。**

两个提示词可以流派、乐器、人声完全相同，但一首是 1972 磁带录音室、一首是手机备忘录音质，听感天差地别。

- ❌ `warm`（形容不出来是什么）
- ✅ `70s tape saturation, close-mic, spring reverb`（年代 + 录音 + 空间，全可执行）

### 5. 乐器写演奏法，不写类别名

**每件核心乐器，能写演奏法就写演奏法。**

- ❌ `piano, bass, drums, strings`（万能配方，什么都不说明）
- ✅ `felt piano, muted upright bass, brush snare, chamber strings`（四个明确的音色决定）

区分度排序：**演奏法 > 乐器名；器材 > 类别。**

### 6. Exclude 要排除"这个风格最可能的平庸结果"

不是随便排除几个不相关的东西，而是**预判：如果生成失败，最可能变成什么样？把那个排除掉。**

| 需求 | 最可能的失败形态 | 该排除 |
| --- | --- | --- |
| 古风 | 变成大混响戏腔罐头 | `no operatic vocal, no heavy reverb` |
| 民谣 | 加了口琴和弦乐糖精 | `no harmonica, no string section` |
| 抒情 | 变成 auto-tune 电音 | `no autotune, no vocoder` |
| 电子 | 变成四踩罐头舞曲 | `no four-on-the-floor` |
| 摇滚 | 变成金属嘶吼 | `no screaming, no metal` |
| 极简 | 被自动填满 | `no choir, no brass, no stacked harmonies` |

---

## Before / After · Suno（英文标签串）

### 例 1 · 安全词 → 有锚点

**同质化**
```
dream pop, melancholic, dreamy, ethereal, female vocals, breathy,
piano, strings, 85 BPM, beautiful
```
> 4 个情绪词（`melancholic` `dreamy` `ethereal` `beautiful`）全是黑名单词；乐器全是类别名；零质感；零事件；`beautiful` 不是音乐参数。
> 换掉任意两个词，出来几乎一样。

**改后**
```
dream pop, minor key, empty subway station at 2am, female alto, breathy,
close-mic, felt piano, muted bass, brush snare, tape hiss,
85 BPM, sparse intro, building, dynamic contrast
```
> 情绪词只剩 1 个且带场景；4 件乐器全带演奏法；`close-mic` + `tape hiss` 定质感；
> `sparse intro` + `building` + `dynamic contrast` 给能量曲线；`felt piano` 是专属锚点。

### 例 2 · 只有属性 → 有事件

**同质化**
```
indie folk, male vocals, acoustic guitar, warm, nostalgic, 92 BPM
```
> 全是静态属性。没有任何一句告诉模型"什么时候发生什么"。

**改后（Style）**
```
indie folk, fingerpicked nylon-string guitar, upright bass, male baritone,
dry close-mic, single-mic live take, 92 BPM, sparse intro, breakdown
```
**改后（歌词里配结构标签，这才是事件真正的落点）**
```
[Intro]（12 秒纯吉他引子）
[Verse 1]
[Breakdown]（桥段抽掉所有伴奏，只留人声与吉他）
[Chorus]
[Outro]（逐层退去，最后一句干声收尾）
```
> `breakdown` 在 Style 里给动态，具体事件由歌词结构标签承载 —— 这是 Suno 里事件的主要落点。

### 例 3 · 反差元素

**同质化**
```
guofeng, chinese style, ancient style, female vocals, operatic,
guzheng, erhu, strings, cinematic, spacious reverb
```
> 古风的默认罐头：古筝 + 二胡 + 戏腔 + 大混响。生成一百次都是这个。

**改后**
```
guofeng, pentatonic, female vocals, clear tone, no vibrato, dry close-mic,
yangqin, xiao, muted upright bass, 808 sub bass, 76 BPM, sparse, dark
```
> 换掉古筝二胡（用 `yangqin` `xiao`）、`dry close-mic` 拿掉大混响、
> **`808 sub bass` 是反差锚点**——古的变重的。这一件乐器，比十个情绪词都管用。

---

## Before / After · 秒响（中文长句）

### 例 1 · 事件缺失 → 有时间轴

**同质化**
```
现代都市抒情流行，女声，气声，电钢琴，贝斯，鼓，85 BPM，情绪清冷，结尾温暖。
```
> 全是属性。"清冷"和"温暖"没有落到任何一个声音决策上。

**改后**
```
现代都市抒情流行，成年女声中低音区，气声起句，咬字轻，句尾收音干净。电钢琴铺底（带轻微磁带抖动），
闷音立式贝斯，brush 军鼓；旋律以级进为主，句尾下行收住；前 12 秒只有电钢琴入声，主歌鼓组半速进入，
第二段副歌起加入室内乐弦乐四重奏；桥段抽掉全部节奏乐器，留 4 秒纯人声干声，
再全员进入最后一次副歌；尾奏逐层退去，最后一句气声收尾。约 85 BPM，
录音室单支铝带麦克风同期录制，70 年代磁带饱和，房间混响很短。完整旋律演唱。不要 auto-tune，不要合唱。
```
> 时间轴完整（12 秒引子 / 半速 / 第二段副歌加弦乐 / 桥段抽空 4 秒 / 尾奏渐退）；
> 质感具体到"单支铝带麦克风同期录制 + 磁带饱和"。
> ⚠️ 注意区分：**「桥段抽掉全部节奏乐器」是那条编曲事件**（清单第 3 项），**不是锚点**；
> 本例的专属锚点是**质感设定**——「单支铝带麦克风同期录制 + 70 年代磁带饱和」（清单第 4 项）。
> 一条指令不能同时抵掉两条红线。

---

## 差异化检测清单（交付前逐条过）

- [ ] 裸情绪词 ≤ 2 个，且都带场景限定或已换成质感词
- [ ] 无安全词黑名单里的词（完整清单见 `references/production-lexicon.md` 第一节；头号三个是 `dreamy` `ethereal` **`melancholic`**）
- [ ] **≥ 1 条编曲事件**（时间轴指令），且落在了正确的位置（Suno → 结构标签；秒响 → 长句）
- [ ] **≥ 1 个专属锚点**（反差音色 / 演奏法器材 / 质感设定，三选一）
- [ ] 质感维度已填：年代 / 录音方式 / 空间与介质，至少两项
- [ ] 核心乐器全部带演奏法或器材，无裸类别名（`piano` `drums` `strings` 单独出现）
- [ ] 能量曲线有落点（哪段低谷、哪段顶点），不是只写 `dynamic`
- [ ] Exclude 针对"这个风格最可能的失败形态"
- [ ] 秒响版人声描述覆盖：音区 + 发声方法 + 咬字 + 句尾处理
- [ ] **Suno 版人声三件套齐全**：音区 + 音色 + 唱法（`female vocals` / `male vocals` 不得单独出现）
- [ ] 换掉任意一个标签，出来的歌会不同

**≥ 8 项通过**才算合格。**第 3 项（编曲事件）与第 4 项（专属锚点）不可豁免** ——
少任何一项，其余都过了也不行。第 4 项是同质化的总开关。

---

## 改写流程

```
① 标记  通读提示词，圈出：安全词 / 裸类别乐器 / 静态属性 / 空泛 Exclude
② 诊断  判断病型：太素？太像别人？还是太乱？
③ 去词  用 `references/production-lexicon.md` 第一节替换安全词
④ 加锚  从第四节反差配方表取一件，或从第二、三节取演奏法/质感
⑤ 补事件  加至少一条时间轴指令，确认落在正确的平台位置
⑥ 定质感  补齐年代 / 录音方式 / 空间
⑦ 复检  过一遍检测清单
```

**定向原则**：用户说"太素"只动配器密度，说"都一个样"才动锚点。不要一次全改，否则无法 A/B 对比。

---

## 与其它 skill 的关系

| 阶段 | 用谁 |
| --- | --- |
| 构建提示词时预防 | `skills/song-prompt-builder/SKILL.md` 的「第 1.5 步：反套路红线」 |
| 写完自检 | **本 skill**（检测清单） |
| 用户说"都一个样""太套路" | **本 skill**（改写流程） |
| 取替换词 | `references/production-lexicon.md` |
| 取标签 | `references/suno-tags.md` |

**不要等写完才想起差异化。** 九维定参时就该：第 ③ 项带演奏法、第 ⑦ 项填质感、第 ⑧ 项写事件。
本 skill 主要负责事后诊断与补救。
