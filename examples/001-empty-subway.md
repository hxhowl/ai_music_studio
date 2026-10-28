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
屏幕暗下去只剩信号灯

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
耳机里这首歌循环不停
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

### 自检

- [x] 结构标签全英文 Suno 格式
- [x] 副歌固定中东辙：声 / 重 / 醒 / 空
- [x] 主歌同辙：领 / 停 / 静 / 灯；醒 / 中 / 停 / 层
- [x] 同段落对应句字数差 ≤ 2 字
- [x] Hook "空车厢 空站台 空的回声" 位于副歌句首，三次副歌字面一致
- [x] 默念顺口，无文言倒装
- [x] 主歌具象名词 ≥ 5 个（风、闸机、玻璃、屏幕、便利店、咖啡、耳机、站牌）
- [x] 桥段换视角（从"我撑得住"转为"我想有人等"），是唯一说真心话的地方
- [x] 尾奏"还在跳动的灯"承载"一点点希望"，不写成直白的"希望会来"

---

## 第 6 步：Suno 提示词

**Style of Music — 直接粘贴**
```
dream pop, indie pop, melancholic, empty subway station at 2am, hopeful ending, female vocals, breathy, intimate, electric piano, muted bass, brush drums, string pads, 85 BPM, warm analog, building
```

**中文说明**

| 标签 | 作用 |
| --- | --- |
| `dream pop` | 主风格，定混响与音色基调 |
| `indie pop` | 唯一辅助风格，避免过于电子化 |
| `melancholic` | 主情绪 |
| `empty subway station at 2am` | 场景化情绪词，比单独写 lonely 有效得多 |
| `hopeful ending` | 锁住"结尾要有希望" |
| `female vocals` / `breathy` / `intimate` | 女声 + 气声 + 近讲私密感 |
| `electric piano` `muted bass` `brush drums` `string pads` | 4 件核心乐器，冷色调 |
| `85 BPM` | 慢速，贴合疲惫感 |
| `warm analog` | 抵消数字冷硬，保留温度 |
| `building` | 情绪递进，配合双副歌结构 |

**Exclude Styles**
```
no autotune, no distortion, no choir, no rap, no heavy reverb, no saxophone
```

---

## 第 7 步：秒响提示词

**中文版 — 直接粘贴**
```
现代都市抒情流行，略带 dream pop 质感，成年女声，中低音区为主，副歌可上行至真声高音。
气声起句，咬字轻，句尾收音干净不拖泥带水；主歌接近独白，副歌转为舒展的实声。
电钢琴铺底，闷音贝斯，brush 军鼓，第二段副歌起加入弦乐 pad 垫底。
旋律以级进为主，副歌首句跳进后逐级回落，句尾不做装饰音。
约 85 BPM，前 12 秒纯电钢琴引子，第二段副歌后留 8 秒纯器乐桥段，尾奏人声渐弱至气声收尾。
录音室近声，带轻微空间混响，整体情绪由清冷转向微暖。完整旋律演唱，不要电音，不要 auto-tune，不要合唱。
```

**English 说明（对照，非逐句翻译）**

Modern urban pop ballad with a dream-pop sheen. Adult female vocal, mostly low-mid register, rising to full-voice high notes in the chorus. Breathy phrase openings, light diction, clean phrase endings. Verses near-spoken; chorus opens into sustained full voice. Electric piano bed, muted bass, brush snare, string pads entering from the second chorus. Melody moves mostly stepwise; the chorus opening line leaps then falls back stepwise. Around 85 BPM. 12-second solo electric-piano intro, 8-second instrumental break after the second chorus, outro vocal fading to breath. Close-mic studio sound with light room reverb; overall mood shifts from cold to faintly warm. Full melodic vocal. No electronic vocal effects, no autotune, no choir.

---

## 第 8 步：设计说明 + 待确认

**为什么这么选韵**：中东辙鼻音收尾自带冷感，且"声/重/醒/空/灯/程"这一族同时有冷调与光亮面，能承载清冷→微暖的转折，不需要换辙。

**为什么这么配器**：电钢琴 + 闷音贝斯 + brush 军鼓 = 冷色调且克制；弦乐 pad 从第二段副歌才进入，制造"希望慢慢渗进来"的听感，而不是一开始就温暖。

**最需要试听后确认的两点**：
1. **85 BPM 是否偏慢** —— 若觉得拖，可提到 95–100 BPM，但气声质感会减弱
2. **女声音区** —— 中低音区更贴"疲惫"，若想要更抓耳可整体上移一个调

---

**落盘**：歌词 → `outputs/20261028-空车厢-lyrics.md`；提示词 → `outputs/20261028-空车厢-prompts.md`
