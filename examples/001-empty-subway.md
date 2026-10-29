# 示例 ·《空车厢》

> 端到端演示：一句模糊描述 → 歌词 + 意象词组 + Suno 提示词 + 秒响提示词。
> 对照 `AGENTS.md` 第 9 节的标准工作流阅读。

---

## 用户输入

> "想做一首关于深夜加班后走在空荡地铁站的歌，女生唱，清冷孤独一点，但结尾要有一点点希望。"

---

## 第 1 步：需求澄清

信息基本齐全，只确认一项：

- **语言**：中文（默认）
- **风格**：都市抒情流行 + dream pop 质感（推荐）
- **情绪基调**：清冷 → 微暖（推荐，贴合"结尾有希望"）

无需追问，直接开工。

---

## 第 2–3 步：调性与结构

- **立意**：不是"孤独"本身，而是"发现这座城市睡了，但自己还有一班车的路要走"——疲惫里带着一点不肯熄的劲儿。
- **情绪弧线**：麻木 → 松动 → 承认脆弱（桥段）→ 微光（尾奏）
- **视角**：第一人称，独白式
- **结构**：`Intro - V1 - PC - C - V2 - PC - C - B - C - Outro`（紧凑流行模板，双副歌 + 桥段，情绪递进强）

---

## 第 4 步：选韵 + 意象词组

**韵辙**：中东辙（eng / ing / ong）。
理由：鼻音收尾、共鸣厚、天然带冷感；同时"声/重/醒/空/灯/程"这一族字既有冷调也有光亮面，正好承载"清冷 → 微暖"的转折。

### 意象词组矩阵

**场景边界**：凌晨 00:47 / 地下二层末班地铁站 / 独自一人 / 闸机、屏蔽门、站牌、手机、凉咖啡

| 维度 | 词组 |
| --- | --- |
| 视觉 | 闸机红点、熄灭的站牌、玻璃里的倒影、白炽灯频闪、空荡的车厢 |
| 听觉 | 末班车报站、风穿过通道、脚步回声、自动门"叮"、耳机漏音 |
| 触觉 | 金属扶手的凉、凉掉的咖啡杯、外套上的夜露、风灌进领口 |
| 嗅觉/味觉 | 消毒水、雨后沥青、便利店关东煮、凉掉的黑咖啡 |
| 动作 | 刷卡、低头系鞋带、数站牌、反复解锁屏幕、把耳机线绕两圈 |

**通感可选项**：报站声发黄 / 灯光有重量 / 风是钝的
**建议避开**：灯火阑珊、岁月如歌、孤独寂寞（陈词）
**最终选用**：闸机红点、玻璃倒影、凉掉的咖啡、循环不停的耳机、数出口、信号灯

### 押韵推荐字（中东辙）

- **高频**：空 声 灯 风 中 城 影 静 停 重 懂 梦 疼 冷 等 同 通 红 动 松 浓 终 钟 听 清 轻 晴 醒 幸 定 应 映 行 冰 平 零 星
- **冷门**：穹 罄 磬 觥 邛 淙 琮 潀 翀 忡 艟 憧
- **双音词**：回**声**、脚**步**声、信**号灯**、路**程**、晴**空**、微**风**、安**静**、心**情**

---

## 第 5 步：歌词

```
[Intro]
（纯电钢琴引子，约 12 秒）

[Verse 1]
末班车的风穿过衣领
闸机的红点亮了又停
玻璃里那张脸太安静
屏幕暗下去 剩信号灯 和百分之四的提醒

[Pre-Chorus]
再等三分钟
再撑三分钟
出口的风会比这里轻

[Chorus]
空车厢 空站台 空的回声
一个人的脚步声很重
整座城睡了 只有灯还醒
总有一班车 会开往晴空

[Verse 2]
便利店的白灯太清醒
凉掉的咖啡握在手中
你嫌吵的那首歌 我循环到不停
我数着出口 数到地下几层

[Pre-Chorus]
再等三分钟
再撑三分钟
出口的风会比这里轻

[Chorus]
空车厢 空站台 空的回声
一个人的脚步声很重
整座城睡了 只有灯还醒
总有一班车 会开往晴空

[Bridge]
其实也没有那么难撑
只是忽然想有人等
想有人问我一句 今天疼不疼
我会假装说 还行

[Chorus]
空车厢 空站台 空的回声
一个人的脚步声很重
整座城睡了 只有灯还醒
总有一班车 会开往晴空

[Outro]
出口的风迎面撞过来
天就快要亮了
我还有一班车的路程
和一点点 还在跳动的灯

[End]
```

### 自检：技术规范

- [x] 结构标签全英文 Suno 格式
- [x] 副歌固定中东辙：声 / 重 / 醒 / 空
- [x] 主歌同辙：领 / 停 / 静 / 提醒；醒 / 中 / 停 / 层；桥段：撑 / 等 / 疼 / 行
- [x] 主歌前 3 句对齐（10/9/9），末句放宽至 15 作落句 —— 法则「制造毛边」
- [x] Hook "空车厢 空站台 空的回声" 位于副歌句首，三次副歌字面一致
- [x] 默念顺口，无文言倒装，无为押韵而倒装的句子

### 自检：自然度（`lyric-naturalness` 10 条）

| 检测项 | 本例如何满足 |
| --- | --- |
| 抽象情绪词 ≤3 | **0 个**。全首没有一个"孤独""寂寞""思念" |
| 每段 ≥3 个可拍照细节 | 主歌1：末班车 / 闸机红点 / 玻璃 / 屏幕 / 信号灯；主歌2：便利店白灯 / 凉咖啡 / 耳机 / 出口 |
| 当代生活物件 ≥1 | 手机电量"百分之四"、便利店、地铁末班车 |
| **私人口吻 ≥1 句** | "你嫌吵的那首歌"、"我会假装说 还行" —— 两句都是别人写不出来的 |
| 通用意象已限定 | 不写"风"，写"末班车的风"、"出口的风" |
| 句长有毛边 | 主歌1：10/9/9/15；主歌2：10/9/13/12；桥段：9/8/11/7 |
| 不为押韵倒装 | 全部顺语序 |
| 情绪最强处最克制 | 桥段不写"我快撑不住了"，写"我会假装说 还行" |
| 每段有新信息 | 主歌1 铺场景 → 主歌2 加物件 → 桥段转折 → 尾奏给微光 |
| 念一遍像人话 | "我会假装说 还行""想有人问我一句 今天疼不疼" |

**10/10 通过**。

### 对照：平均化写法长什么样

同样的主题，按"安全模板"写会变成：

```
深夜我独自在地铁站
孤独像潮水般涌来
回忆在心头蔓延开
找不到你的存在
```

差在哪：

| 平均化 | 本例 |
| --- | --- |
| 深夜 | 凌晨一点、末班车 |
| 孤独 | 屏幕剩百分之四的提醒 |
| 回忆蔓延 | 你嫌吵的那首歌，我循环到不停 |
| 找不到你的存在 | 我会假装说 还行 |

**差的不是文采，是一个具体细节。** 抽象词换成可拍照的物件，AI 味就掉了一大半。

---

## 第 6 步：Suno 提示词

**Style of Music — 直接粘贴**
```
dream pop, empty subway station at 2am, female alto, breathy, close-mic, felt piano, muted upright bass, brush snare, chamber strings, 70s tape saturation, 85 BPM, sparse intro, dynamic contrast
```
（12 个标签 / 194 字符，单行，可直接粘贴）

**中文说明**

| 标签 | 作用 |
| --- | --- |
| `dream pop` | 唯一主风格，定混响与音色基调 |
| `empty subway station at 2am` | **场景化情绪词**，替代裸情绪词 `melancholic`（黑名单词） |
| `female alto` | 女声中低音区 —— 比 `female vocals` 多一个音区决定 |
| `breathy` | 气声，贴合疲惫感 |
| `close-mic` | 近讲，耳边私密感（**空间**质感） |
| `felt piano` | **专属锚点**：呢垫钢琴，闷而软，不是通用 `piano` |
| `muted upright bass` | 闷音立式贝斯，冷且克制 |
| `brush snare` | 刷鼓，避免军鼓的"打点感" |
| `chamber strings` | 室内乐四重奏编制 —— 比 `strings` 亲密得多，不会变罐头弦乐 |
| `70s tape saturation` | **年代 + 质感**，一个标签给两个维度 |
| `85 BPM` | 慢速，贴合疲惫感 |
| `sparse intro` | 事件一：引子极简 |
| `dynamic contrast` | 事件二：动态对比（配合歌词里的 `[Breakdown]`） |

**Exclude Styles**
```
no autotune, no vocoder, no choir, no saxophone, no four-on-the-floor
```

> **为什么 Exclude 是这五个**：都市抒情 dream pop 最可能的失败形态是——被做成 auto-tune 电音抒情、
> 加合唱煽情、加萨克斯廉价煽情、或变成四踩舞曲。排除的是"它最可能塌成的样子"，不是随便写几个。

**编曲事件的落点**：Suno 的 Style 字段写不下长句，事件分两处承载——

| 载体 | 内容 |
| --- | --- |
| Style 字段 | 只放动态词：`sparse intro`、`dynamic contrast` |
| **歌词结构标签** | 真正的事件落点：`[Intro]`（12 秒纯器乐）、`[Bridge]`（抽掉节奏组）、`[Outro]`（渐退）。<br>若要进一步强调断崖感，可把 `[Bridge]` 换成 `[Breakdown]` |

⚠️ 把"副歌前抽掉鼓"直接写进 Style 字段是常见错误 —— Suno 读不懂长句。

**字符预算的真实取舍**：`sub bass drone`（地铁在地下的低频嗡鸣）是最贴题的反差音色，
但加上会超 200 字符上限。取舍结果：**反差元素放到秒响版与歌词结构标签承载**，
Suno 版用「演奏法器材（`felt piano`）+ 质感设定（`70s tape saturation`）」满足锚点要求。
这比硬塞进 200 字符更稳。

---

## 第 7 步：秒响提示词

**中文版 — 直接粘贴**
```
现代都市抒情流行，略带 dream pop 质感，成年女声中低音区，副歌可上行至真声高音；
气声起句，咬字轻，句尾收音干净不拖泥带水；主歌接近独白，副歌转为舒展的实声。
呢垫电钢琴铺底，闷音立式贝斯，brush 军鼓，弦乐为室内乐四重奏编制、从第二段副歌才进入。
旋律以级进为主，副歌首句跳进后逐级回落，句尾不做装饰音。约 85 BPM。
前 12 秒只有电钢琴与低频持续音（地铁在地下的嗡鸣），人声第 12 秒进入；
主歌鼓组半速进入；桥段抽掉全部节奏乐器，留 4 秒纯人声干声、只留低频持续音垫底，
再全员进入最后一次副歌；尾奏逐层退去，最后一句气声收尾。
录音质感：单支铝带麦克风同期录制，70 年代磁带饱和，房间混响很短，保留一点录音室的空气声。
整体由清冷转向微暖。完整旋律演唱，不要 auto-tune，不要电音人声，不要合唱，不要萨克斯。
```

**English 说明（对照，非逐句翻译）**

Modern urban pop ballad with a dream-pop sheen. Adult female vocal, low-mid register, rising to full-voice high notes in the chorus. Breathy phrase openings, light diction, clean phrase endings; verses near-spoken, chorus opening into sustained full voice. Felt piano bed, muted upright bass, brush snare, chamber string quartet entering only from the second chorus. Melody mostly stepwise; the chorus opening line leaps then falls back stepwise. Around 85 BPM. First 12 seconds are piano and a low-frequency drone only (the hum of a subway underground), vocal entering at 0:12; drums enter half-time in the verses; the bridge strips all rhythm instruments for 4 seconds of dry solo vocal over the drone, then everything returns for the final chorus; the outro deconstructs layer by layer, last line on breath. Recorded live with a single ribbon mic, 70s tape saturation, very short room reverb, a little studio air retained. Shifts from cold to faintly warm. Full melodic vocal. No autotune, no electronic vocal effects, no choir, no saxophone.

**为什么秒响版比 Suno 版具体这么多**：秒响接受中文长句，**时间轴指令可以直接写**。
"第 12 秒入声""桥段抽掉节奏组留 4 秒"这类事件在 Suno 里只能靠结构标签暗示，在秒响里能明说。
这是秒响相对 Suno 最大的优势区，不用白不用。

---

## 第 8 步：设计说明 + 待确认

### 差异化自检（`production-antislop` 10 条）

| 检测项 | 本例如何满足 |
| --- | --- |
| 裸情绪词 ≤ 2 个 | **0 个**。`melancholic` 换成 `empty subway station at 2am` |
| 无安全词黑名单词汇 | 已剔除 `dreamy` `ethereal` `intimate` `warm analog` 等泛词 |
| **≥ 1 条编曲事件** | 前 12 秒纯器乐入声 / 主歌鼓组半速 / 桥段抽空 4 秒 / 尾奏渐退 |
| **≥ 1 个专属锚点** | `felt piano`（器材）+ `70s tape saturation`（质感）+ 低频持续音（反差） |
| 质感 ≥ 2 项 | 空间 `close-mic` + 年代介质 `70s tape saturation` + 录音方式（秒响版：单支铝带麦克风同期） |
| 乐器全带演奏法/器材 | 呢垫电钢琴 / 闷音立式贝斯 / brush 军鼓 / 室内乐弦乐 |
| 能量曲线有落点 | sparse intro → 主歌半速 → 副歌全员 → **桥段断崖** → 末次副歌顶点 → 渐退 |
| Exclude 有针对性 | 针对"都市抒情最可能塌成的样子"：auto-tune / 合唱 / 萨克斯 / 四踩 |
| 秒响人声四项齐全 | 音区（中低音）+ 发声（气声起句）+ 咬字（轻）+ 句尾（干净收音） |
| 换掉任一标签会不同 | 换掉 `felt piano` 就变成通用钢琴抒情；换掉 `chamber strings` 就变罐头弦乐 |

**10/10 通过**。

### 对照：安全词写法长什么样

同样的需求，按"安全模板"写会变成：

```
dream pop, indie pop, melancholic, dreamy, ethereal, female vocals, breathy,
intimate, piano, bass, drums, strings, 85 BPM, warm, beautiful
```

差在哪：

| 安全词版 | 本例 | 差别 |
| --- | --- | --- |
| `melancholic dreamy ethereal` | `empty subway station at 2am` | 三个通胀情绪词 → 一个场景 |
| `female vocals` | `female alto` | 只给性别 → 给性别 + 音区 |
| `piano bass drums strings` | `felt piano, muted upright bass, brush snare, chamber strings` | 类别名 → 演奏法 + 编制 |
| `warm` | `70s tape saturation, close-mic` | 形容词 → 可执行的年代 + 空间 + 录音方式 |
| `beautiful` | —— | 主观评价，不是音乐参数，删掉 |
| 无 | `sparse intro, dynamic contrast` + `[Breakdown]` | 零事件 → 有能量曲线 |
| `no autotune, no distortion, no rap` | `no autotune, no vocoder, no choir, no saxophone, no four-on-the-floor` | 随便排除 → 针对失败形态 |

**差的不是标签数量，是每个标签的信息量。** 安全词版 15 个标签，有效信息约等于本例的 5 个。

---

**为什么这么选韵**：中东辙鼻音收尾自带冷感，且"声/重/醒/空/灯/程"这一族同时有冷调与光亮面，能承载清冷→微暖的转折，不需要换辙。

**为什么这么配器**：呢垫电钢琴 + 闷音立式贝斯 + brush 军鼓 = 冷色调且克制；室内乐弦乐从第二段副歌才进入，制造"希望慢慢渗进来"的听感，而不是一开始就温暖。

**这首歌区别于同类的是什么**：桥段那 4 秒 —— 抽掉全部节奏乐器，只剩干声人声压在地铁低频嗡鸣上。
留白之后的爆发，比一路堆满有力得多，也是这首最不像"罐头抒情"的地方。

**最需要试听后确认的两点**：
1. **85 BPM 是否偏慢** —— 若觉得拖，可提到 95–100 BPM，但气声质感会减弱
2. **低频持续音的强度** —— 若掩盖人声，就把它限制在引子与桥段，不进主歌

---

**落盘**：歌词 → `outputs/20261028-空车厢-lyrics.md`；提示词 → `outputs/20261028-空车厢-prompts.md`
