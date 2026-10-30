# 编曲差异化词库

> 供 `skills/production-antislop/SKILL.md` 与 `skills/song-prompt-builder/SKILL.md` 取词使用。
> 核心用途：**当提示词写成了"安全词排列组合"时，从本表取一个专属锚点替换掉。**

---

## 一、Suno 安全词黑名单

这些词本身没错，错在**被用到烂**——模型对它们的响应已收敛到"最大公约数"，写进去等于没写。

| 安全词 | 为什么失效 | 换成什么 |
| --- | --- | --- |
| `dreamy` | 每个用户都写，结果千篇一律的混响糊 | `washed-out reverb`, `half-speed tape`, `hazy lo-fi` |
| `ethereal` | 同上，且几乎必然带来飘忽女声 | `wordless falsetto pads`, `shimmering tremolo guitar` |
| `beautiful` `amazing` | 主观评价，不是音乐参数 | 换成具体的质感或乐器 |
| `melancholic` `sad` | 太泛，情绪落不到编曲上 | `minor key`, `slow decay`, `dissonant strings` |
| `emotional` | 无法转成编曲决策 | 写成具体事件："副歌前抽掉所有伴奏" |
| `epic` `cinematic` | 触发固定的大编制套路 | 写明编制：`string section + taiko + distorted bass` |
| `catchy` `radio-ready` | 平台不理解"抓耳"是什么 | `four-on-the-floor`, `anthemic chorus`, `stacked harmonies` |
| `female vocals` 单独出现 | 等于没描述 | 必配音区 + 音色 + 唱法（见下） |
| `piano` `guitar` `drums` `strings` | 类别名，不是音色 | 换成**演奏法 + 器材**（见第二节） |
| `80s` `retro` `vintage` 单用 | 太宽泛 | 写明器材：`analog synth`, `gated reverb drums`, `tape saturation` |
| `warm` `intimate` 单用 | 形容不出是什么，不带器材 | **带器材时有效且推荐**：`warm analog`, `intimate close-mic`。判据：它描述的是"这张唱片怎么录的"（有效）还是"听起来感觉如何"（无效） |

**判据**：把这个标签换成同义词，出来的歌会不同吗？不会，就是安全词。

---

## 二、演奏法库（区分度最高的维度）

**乐器名给的是"谁来演"，演奏法给的是"怎么演"。后者决定听感。**

规则：每件核心乐器，能写演奏法就写演奏法。**`brush snare` 和 `drums` 是两个世界。**

### 键盘

| 写法 | 听感 |
| --- | --- |
| `felt piano` / `felt-damped piano` | 呢垫钢琴，闷、软、私密 |
| `prepared piano` | 预置钢琴，金属杂音、实验感 |
| `upright piano, slightly out of tune` | 走音立式琴，家庭感/酒馆感 |
| `Rhodes` / `Wurlitzer` | 电钢/电簧风琴，暖、带颤 |
| `Clavinet` | 放克键琴，短促、颗粒感 |
| `Hammond B3 with Leslie` | 教堂管风琴旋转音箱，厚重摇摆 |
| `Mellotron` | 磁带复音，60-70 年代迷幻 |
| `arpeggiated synth` | 琶音合成器，推进感 |
| `drone` / `sustained pad` | 持续音床，无节奏 |

### 吉他

| 写法 | 听感 |
| --- | --- |
| `fingerpicked nylon-string guitar` | 尼龙弦指弹，柔、古典 |
| `12-string acoustic` | 十二弦，闪、厚 |
| `slide guitar` | 滑棒，哭腔、乡村/蓝调 |
| `EBow guitar` | 无限延音，像弦乐 |
| `tremolo picking` | 颤音拨弦，紧张 |
| `clean chorus guitar` | 合唱效果清音，80 年代 |
| `fuzz bass` / `distorted guitar` | 法兹/失真 |
| `baritone guitar` | 低音吉他，沉、西部 |
| `harmonics` / `natural harmonics` | 泛音，空灵 |

### 贝斯

| 写法 | 听感 |
| --- | --- |
| `upright bass` | 立式贝斯，爵士/民谣 |
| `fretless bass` | 无品贝斯，滑音、软 |
| `muted bass` / `palm-muted bass` | 闷音，克制 |
| `Moog bass` / `analog synth bass` | 模拟合成贝斯，圆、厚 |
| `808 sub bass` | 808 低频，陷阱/电子 |
| `slap bass` | 击弦，放克 |
| `pizzicato bass` | 拨奏，短、跳跃 |

### 鼓与打击

| 写法 | 听感 |
| --- | --- |
| `brush snare` / `brush drums` / `brushed snare` | 刷鼓，jazz、安静 |
| `rimshot` | 打边，干、紧 |
| `gated reverb drums` | 门混响鼓，80 年代标志音 |
| `four-on-the-floor` | 每拍底鼓，舞曲 |
| `half-time` | 半速，重拍后移，厚重 |
| `breakbeat` / `broken beat` | 碎拍，不安定 |
| `tight drums` vs `loose drums` | 紧 vs 松（摇摆感） |
| `hand claps` / `finger snaps` | 拍手/响指，替代军鼓 |
| `shaker` / `woodblock` / `congas` | 色彩打击 |
| `taiko` / `frame drum` | 太鼓/框鼓，仪式感 |

### 弦乐与管乐

| 写法 | 听感 |
| --- | --- |
| `pizzicato strings` | 拨弦，俏皮、轻 |
| `col legno` | 弓杆敲弦，敲击感 |
| `tremolo strings` | 震弓，紧张、悬疑 |
| `glissando strings` | 滑音，戏剧 |
| `sul ponticello` | 近琴马，金属泛音 |
| `chamber strings`（四重奏编制） | 室内乐，比"弦乐团"亲密得多 |
| `muted trumpet` / `Harmon mute` | 弱音小号，爵士夜色 |
| `breathy flute` | 气声长笛 |

### 人声（必须三件套：音区 + 音色 + 唱法）

| 维度 | 选项 |
| --- | --- |
| 音区 | `deep male` `baritone` `tenor` `alto` `mezzo` `soprano` `falsetto` |
| 音色 | `breathy` `husky` `raspy` `gravelly` `silky` `nasal` `resonant` `thin` |
| 唱法 | `belting` `whisper` `spoken word` `chant` `vibrato` `yodel` `scat` `ad-libs` |
| 织体 | `solo` `layered harmonies` `stacked vocals` `call and response` `unison doubling` |
| 处理 | `dry close-mic` `slapback delay` `no reverb` `doubled vocal` `telephone-effect` |

---

## 三、质感库：这张唱片怎么录出来的

**两个提示词可以流派、乐器、人声完全相同，但录音质感不同 → 听感天差地别。**
这是最少人写、但区分度最高的维度。

### 年代

| 写法 | 指向 |
| --- | --- |
| `50s` | 单声道、房间混响、立式贝斯 |
| `60s` | 磁带、spring reverb、暖 |
| `70s` | 模拟调音台、tape saturation、宽 |
| `80s` | gated reverb、模拟合成、亮 |
| `90s` | 早期数字、lo-fi、grunge 质感 |
| `2000s` | 响度战争、压缩重 |
| `modern production` | 干净、低频紧 |

### 录音方式

| 写法 | 指向 |
| --- | --- |
| `close-mic` / `intimate close-mic` | 近讲，耳边、私密 |
| `room mic` / `live room` | 房间声，有空气 |
| `single-mic live take` | 一支麦同期录制，真实、有瑕疵 |
| `off-mic` / `recorded in a hallway` | 远拾音，有距离感 |
| `direct injection` | DI 直录，干、电 |
| `ribbon mic` | 铝带麦克风，暗、柔 |
| `recorded on a phone` / `voice memo quality` | 手机录音，bedroom pop 质感 |
| `live concert` / `stadium` | 现场，有观众 |

### 空间与介质

| 写法 | 指向 |
| --- | --- |
| `slapback delay` |  slap 回声，50-60s、摇滚abilly |
| `spring reverb` | 弹簧混响，吉他音箱 |
| `plate reverb` | 铁板混响，光滑 |
| `cathedral reverb` | 大教堂，宏大 |
| `dry` / `no reverb` | 干声，压迫、真实 |
| `tape saturation` / `tape hiss` | 磁带饱和/嘶声 |
| `vinyl crackle` | 黑胶噪点 |
| `wow and flutter` | 磁带速度抖动，走音感 |
| `bitcrushed` / `lo-fi digital` | 数字失真 |
| `sidechain compression` | 侧链压缩，舞曲抽吸感 |
| `wall of sound` | 声墙，密集 |
| `sparse` / `minimal` | 极简、留白 |

---

## 四、反差元素配方表

**好编曲几乎都有一个"不该出现在这里的东西"。** 从下表取一个，比堆十个情绪词管用。

| 风格 | 默认套路（要破除的） | 反差元素 | 效果 |
| --- | --- | --- | --- |
| 民谣 | 吉他 + 口琴 + 温暖 | `bitcrushed drum machine` | 土的变冷的 |
| 古风 | 古筝 + 二胡 + 大混响 | `808 sub bass` / `distorted bass` | 古的变重的 |
| 抒情 ballad | 钢琴 + 弦乐 + 高潮 | `talkbox` / `vocoder` 间奏 | 软的变怪的 |
| city pop | 电钢 + 铜管 + 明亮 | `cassette tape wobble` | 亮变旧 |
| 电子舞曲 | 合成器 + 四踩 + drop | `solo cello` / `string quartet` | 机械的变有人味 |
| 嘻哈 | 808 + hi-hat + 阴暗 | `music box` / `celesta` | 硬的变童真 |
| 摇滚 | 失真吉他 + 强鼓 | `accordion` / `harmonium` | 躁的变诡的 |
| 爵士 | 立式贝斯 + 刷鼓 | `analog synth drone` | 复古的变未来的 |
| 童谣感 | 铃铛 + 简单和弦 | `detuned piano` | 甜的变质感的 |
| 教堂/圣咏 | 合唱 + 管风琴 | `broken drum machine` | 神圣的变破碎的 |
| 朋克 | 三件套 + 快 | `pedal steel guitar` | 冲的变的 |
| 氛围 | pad + 无鼓 | `typewriter percussion` | 静的变具体的 |

**用法**：反差元素只加**一件**，且要说明它出现在哪一段（例："bridge 段加入 808 sub bass，其余段落不用"）。
加多了就是风格混乱，不是反差。

---

## 五、编曲事件语句库（时间轴指令）

**提示词写不出事件，就只有"是什么"没有"发生什么"。** 这是最容易被忽略、也最容易拉开差距的一维。

### 平台落法差异

| 平台 | 编曲事件怎么落 |
| --- | --- |
| **Suno** | Style 字段写不下长句。事件落在：① **歌词的结构标签**（`[Instrumental Break]` `[Breakdown]` `[Drop]` `[Guitar Solo]` `[whisper]`）；② Style 里的**动态词**（`building` `sparse intro` `dynamic contrast` `slow build`）；③ 元标签 `[Style: ...]` |
| **秒响** | **直接写中文时间轴**，这是秒响相对 Suno 最大的优势区 |

### 中文事件句库（秒响用）

| 事件 | 写法 |
| --- | --- |
| 入声时机 | "第 2 秒入声" / "前 12 秒纯器乐引子" |
| 抽空 | "第二段副歌后抽掉所有鼓，留 4 秒纯人声" |
| 渐入 | "弦乐从第二段副歌才进入" |
| 突变 | "桥段整体降半音，人声转为气声" |
| 收尾 | "尾奏人声渐弱至气声收尾" / "最后一句干声，无混响" |
| 停顿 | "副歌前留 1 拍静默" |
| 加倍 | "最后一次副歌加入二部和声叠唱" |
| 破格 | "桥段插入 8 秒纯 808 sub bass，其余段落不出现" |

### 英文事件句库（Suno 说明用 / English 对照用）

| 事件 | 写法 |
| --- | --- |
| 入声 | `vocal enters at 0:02`, `12-second instrumental intro` |
| 抽空 | `drums drop out before final chorus`, `4 seconds of bare vocal` |
| 渐入 | `strings enter only from the second chorus` |
| 突变 | `half-step key change at the bridge` |
| 收尾 | `outro vocal fades to breath`, `final line dry, no reverb` |
| 停顿 | `one beat of silence before the chorus` |
| 加倍 | `stacked harmonies on the last chorus` |
| 破格 | `808 sub bass appears only in the bridge` |
| 动态 | `sparse intro`, `building`, `dynamic contrast`, `slow build`, `wall of sound chorus` |

---

## 六、能量曲线落点表

不要只写 `dynamic` 或 `building`——要写明**哪一段是低谷、哪一段是顶点**。

| 结构 | 能量 | Suno 写法 | 秒响写法 |
| --- | --- | --- | --- |
| Intro | 最低 | `sparse` `ambient intro` | "前 12 秒只有电钢琴" |
| Verse 1 | 低 | `intimate` `minimal` | "主歌只有贝斯和刷鼓，接近独白" |
| Pre-Chorus | 爬升 | `building` `riser` | "预副歌加入弦乐，逐渐加密" |
| Chorus 1 | 高 | `anthemic` `wide` | "副歌全员进入，和声叠两层" |
| Verse 2 | 回落 | `sparse` | "第二段主歌重新收窄，只留贝斯" |
| Chorus 2 | 更高 | `wall of sound` `stacked harmonies` | "第二次副歌加铜管与二部合唱" |
| Bridge | 断崖或反转 | `breakdown` `stripped` `key change` | "桥段抽掉鼓，只留人声与 pad" |
| Final Chorus | 顶点 | `triumphant` `full` | "最后一次副歌全员 + 打击乐加倍" |
| Outro | 衰减 | `fading` `deconstructed` | "尾奏逐层退去，最后只剩气声" |

**最常用的一招**：**桥段或最后一次副歌前做一次"抽空"**。留白之后的爆发，比一路堆满有力得多。

---

## 七、常见风格的"默认套路 → 破除方法"

| 用户说 | 默认会得到 | 破除法 |
| --- | --- | --- |
| 古风 | 古筝 + 二胡 + 大混响 + 戏腔 | 换乐器（`yangqin` `xiao`）、降混响（`dry` `close-mic`）、加反差（`808 sub bass`） |
| 民谣 | 吉他扫弦 + 口琴 + 温暖 | 换演奏法（`fingerpicked`）、换质感（`single-mic live take`）、去掉口琴 |
| 电子 | 四踩 + drop + 亮合成器 | 换节奏（`broken beat` `half-time`）、换音色（`FM bells` `granular pads`） |
| 抒情 | 钢琴 + 弦乐 + 高潮 | 换编制（`chamber strings`）、换空间（`dry` `close-mic`）、加事件（副歌前抽空） |
| 说唱 | 808 + hi-hat + 阴暗 | 换采样质感（`vinyl crackle`）、换 bass（`upright bass`）、加乐器（`Rhodes`） |
| 摇滚 | 失真吉他 + 强鼓 | 换鼓（`loose drums` `half-time`）、换空间（`live room`）、加反差（`accordion`） |
