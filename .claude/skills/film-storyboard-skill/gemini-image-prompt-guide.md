# 📖 Nano Banner 提示词写作指南（仅供参考）

> **注意**: 这是参考指南。**仅在对 Nano Banner 提示词格式有疑问时查阅**。
> **不要自动加载此文件** - 仅在困惑或需要时参考。

---

# Nano Banner Prompt Guide

专为 Nano Banner 3x3 网格生成优化的提示词写作指南。

**重要说明**:

- 本指南专注于**Nano Banner Episode Visual Script 格式**
- Nano Banner 格式与标准 Gemini/Midjourney 格式**不同**
- 提示词内容**使用英文**以获得最佳生成效果
- 这是 📖 **Reference Only** 文档，不会自动加载到上下文中

---

## Nano Banner 核心格式

### Episode Visual Script 结构

Nano Banner 使用特殊的"Episode Visual Script"格式，优化用于一次性生成完整 3x3 网格：

```markdown
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT

Beat 1: [Beat 标题]
Visual Description: [80-120 词详细视觉描述]
Lighting & Mood: [30-50 词光影和氛围]

Beat 2: [Beat 标题]
Visual Description: [80-120 词详细视觉描述]
Lighting & Mood: [30-50 词光影和氛围]

[继续 Beat 3-9，总共 9 个 beats]
```

### 格式要求

**标题行**:

```
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT
```

- 必须包含 episode 编号
- 固定格式，不可省略

**每个 Beat 结构** (恰好 3 行):

1. `Beat X: [标题]` - Beat 编号和标题
2. `Visual Description:` - 80-120 词的详细视觉描述
3. `Lighting & Mood:` - 30-50 词的光影和氛围

**总计**: 1 个标题行 + 9 个 beats × 3 行 = 28 行

### 3x3 网格布局

9 个 beats 对应 nano banner 的 3x3 网格位置：

```
┌─────────┬─────────┬─────────┐
│ Beat 1  │ Beat 2  │ Beat 3  │
│ 左上    │ 中上    │ 右上    │
├─────────┼─────────┼─────────┤
│ Beat 4  │ Beat 5  │ Beat 6  │
│ 左中    │ 中心    │ 右中    │
├─────────┼─────────┼─────────┤
│ Beat 7  │ Beat 8  │ Beat 9  │
│ 左下    │ 中下    │ 右下    │
└─────────┴─────────┴─────────┘
```

**关键点**:

- Nano banner 会将这 9 个 beats 同时渲染为 3x3 网格
- Beat 1-3 是第一行（上）
- Beat 4-6 是第二行（中）
- Beat 7-9 是第三行（下）
- 保持所有 beats 的角色/风格一致性至关重要

---

## Visual Description 编写规则

### 必需元素（按顺序）

1. **镜头规格** (Shot Type + Angle)

   ```
   Wide shot, high angle.
   Medium shot, eye-level.
   Close-up, low angle.
   ```

2. **角色描述** (Canonical Description)

   ```
   A young woman in her late 20s with waist-length straight silver hair,
   pale porcelain skin, and bright violet eyes, wearing a long black coat
   over a white high-neck shirt
   ```

   **关键**: 所有 9 个 beats 必须使用**完全相同**的角色描述

3. **动作/姿势**

   ```
   stands alone on a crowded platform
   sits in a dimly lit subway car, the journal open on her lap
   reaches toward a glowing object
   ```

4. **场景设定**

   ```
   Modern metropolitan subway station with fluorescent lighting and
   yellow safety lines on the ground
   ```

   包含 2-4 个独特场景特征

5. **关键视觉元素**
   ```
   Commuters rush past her in blurred motion while she remains perfectly still,
   staring at an ancient leather-bound journal in her hands
   ```

### 长度控制

- **最佳**: 80-120 词
- **过短** (<60 词): 缺少必要细节
- **过长** (>140 词): 信息过载，nano banner 可能忽略

### 叙事描述式风格

❌ **错误** (关键词堆砌):

```
woman, silver hair, black coat, subway, neon, dramatic, 8k, detailed
```

✅ **正确** (叙事描述):

```
Wide shot, high angle. A young woman in her late 20s with waist-length straight
silver hair, pale porcelain skin, and bright violet eyes, wearing a long black
coat over a white high-neck shirt, stands alone on a crowded train platform.
Commuters rush past her in blurred motion while she remains perfectly still,
staring at an ancient leather-bound journal in her hands. Modern metropolitan
subway station with fluorescent lighting and yellow safety lines on the ground.
```

---

## Lighting & Mood 编写规则

### 必需元素

1. **光源和方向**

   ```
   Harsh overhead fluorescent lights creating flat, institutional illumination
   Warm golden sunlight streaming from the left
   Flickering cool fluorescent overhead light mixing with warm amber glow
   ```

2. **光影质量**

   ```
   Soft diffused natural light
   Dramatic high contrast lighting
   Rim lighting creating silhouette effect
   ```

3. **色温**

   ```
   Cool blue-white color temperature
   Warm amber and orange tones
   Cold silvery moonlight
   ```

4. **情绪氛围**
   ```
   Isolated, contemplative atmosphere
   Mysterious and tense mood
   Eerie, supernatural feeling
   ```

### 长度控制

- **最佳**: 30-50 词
- **过短** (<20 词): 不够具体
- **过长** (>60 词): 应该属于 Visual Description

---

## 角色一致性技巧

### 建立规范描述

在 Beat 1 建立完整的角色描述，然后在所有 9 个 beats 中**逐字重复**关键识别符：

**规范描述**:

```
A young woman in her late 20s with waist-length straight silver hair,
pale porcelain skin, and bright violet eyes, wearing a long black coat
over a white high-neck shirt
```

**在后续 beats 中重复**:

```
Beat 1: ...the silver-haired woman in her late 20s with violet eyes and
        a long black coat stands...

Beat 5: ...the same woman with waist-length silver hair and bright violet
        eyes, still wearing the long black coat, walks...

Beat 9: ...the young woman with silver hair and violet eyes in the black coat...
```

### 关键识别符

必须在所有 beats 中保持一致：

- 发型、发色、发长
- 眼睛颜色
- 主要服装（外套、裙子等）
- 肤色
- 显著标记（疤痕、纹身等）

---

## 完整示例

```markdown
EPISODE 01: BEAT BOARD VISUAL SCRIPT

Beat 1: The Isolated Spark
Visual Description: Wide shot, high angle. A young woman in her late 20s with waist-length straight silver hair, pale porcelain skin, and bright violet eyes, wearing a long black coat over a white high-neck shirt, stands alone on a crowded train platform. Commuters rush past her in blurred motion while she remains perfectly still, staring at an ancient leather-bound journal in her hands. Modern metropolitan subway station with fluorescent lighting and yellow safety lines on the ground.
Lighting & Mood: Harsh overhead fluorescent lights creating flat, institutional illumination. Cool blue-white color temperature. Isolated, contemplative atmosphere with contrast between her stillness and surrounding chaos.

Beat 2: Crossing the Threshold
Visual Description: Medium shot, eye-level. The silver-haired woman in the long black coat sits in a dimly lit subway car, the journal open on her lap. Her violet eyes are narrowed as she studies a page filled with hand-drawn symbols and glowing six-pointed star diagrams. The fluorescent lights flicker above. Other passengers visible in soft focus in the background, unaware of the otherworldly glow emanating from the pages.
Lighting & Mood: Flickering cool fluorescent overhead light mixing with warm amber glow from the journal pages. Creates an eerie, supernatural mood. Mysterious and tense atmosphere.

Beat 3: The Hidden Message
Visual Description: Close-up, slightly high angle. The open journal fills the frame, showing intricate hand-drawn diagrams, cryptic symbols in an unknown language, and a central six-pointed star radiating soft golden light. The woman's pale hands with delicate fingers hold the edges of the pages. Aged paper texture visible, with slight yellowing and worn edges indicating the journal's antiquity.
Lighting & Mood: Warm golden glow radiating from the star diagram, illuminating the aged paper. Soft ambient light from above creates gentle shadows. Mystical, ancient atmosphere with hints of magic.

Beat 4: The First Sign
Visual Description: Medium shot, low angle. The young woman with waist-length silver hair and violet eyes, still wearing the long black coat, stands at the subway door as it opens. She looks up sharply, her expression shifting from concentration to alert awareness. Through the open door, a swirling vortex of purple and blue energy is visible instead of the normal platform. Other passengers continue moving normally, oblivious.
Lighting & Mood: Cool fluorescent car interior lighting contrasts with vibrant purple-blue ethereal glow from the vortex. Heightened tension and anticipation. Supernatural energy becoming visible.

Beat 5: Stepping Into the Unknown
Visual Description: Full shot, eye-level. The silver-haired woman in her black coat steps through the subway doorway toward the swirling energy vortex. Her right foot crosses the threshold while her left remains in the car. Her silver hair begins to float and swirl as if caught in an invisible wind. The journal is clutched tightly to her chest. Reality appears to distort around the doorway, with warped perspective and bending light.
Lighting & Mood: Dramatic contrast between flat subway lighting and the dynamic, swirling purple-blue glow of the portal. Hair-raising, momentous atmosphere. Point of no return energy.

Beat 6: The In-Between
Visual Description: Wide shot, Dutch angle. The woman with silver hair and violet eyes floats in a vast void of swirling purple, blue, and silver energy streams. The black coat billows around her as if underwater. Fragments of reality—pieces of the subway, glimpses of strange otherworldly architecture—float past in the background. She holds the glowing journal close, its light creating a protective sphere around her.
Lighting & Mood: Ethereal, omnidirectional glow from energy streams in purple and blue hues. The journal's warm golden light provides a safe anchor point. Surreal, dreamlike yet slightly unsettling atmosphere.

Beat 7: Arrival
Visual Description: Medium shot, low angle. The young woman with waist-length silver hair and bright violet eyes in the long black coat emerges from a doorway of light into a vast ancient library with impossibly tall bookshelves reaching into darkness above. Thousands of leather-bound books line the shelves. Floating candles provide illumination. She stands in the center, looking around in wonder and apprehension, journal still in hand.
Lighting & Mood: Warm golden candlelight from hundreds of floating candles creates dancing shadows. Mixture of welcoming warmth and mysterious darkness in the unreachable upper shelves. Ancient, magical atmosphere filled with hidden knowledge.

Beat 8: The Revelation
Visual Description: Close-up, eye-level. The woman's face fills the frame, her bright violet eyes wide with realization and fear. Her pale skin is illuminated by the warm glow of candlelight from below, creating dramatic upward shadows. Silver hair frames her face. Over her shoulder, blurred in the background, shelves of ancient books are visible. Her expression conveys the weight of understanding something profound and dangerous.
Lighting & Mood: Dramatic upward lighting from candles below creates shadows under her eyes and cheekbones. Warm golden-orange color temperature. Tense, revelatory mood mixing awe with creeping dread.

Beat 9: Acceptance of Destiny
Visual Description: Wide shot, high angle. The young woman with silver hair and violet eyes in the long black coat walks determinedly down a long corridor between towering bookshelves, journal held at her side. Floating candles light her path. Her shadow stretches long behind her. Ancient stone floor beneath her feet. The perspective creates a sense of journey and purpose. She's small against the vast library but moving forward with resolve.
Lighting & Mood: Warm candlelight creating a path forward while darkness looms on either side. Long dramatic shadows emphasizing her solitary journey. Determined, resolute atmosphere with underlying tension of the unknown ahead.
```

---

## 常见错误

### ❌ 角色描述不一致

```
Beat 1: woman with long silver hair
Beat 5: woman with short blonde hair
```

**问题**: Nano Banner 会生成两个不同外观的人物

### ❌ 过度简短

```
Visual Description: A woman stands in a train station. (7词)
```

**问题**: 信息不足，nano banner 无法生成详细图像

### ❌ 关键词堆砌

```
Visual Description: woman, silver hair, black coat, subway, mysterious, 8k, cinematic, detailed
```

**问题**: Nano Banner 需要叙事描述式，非关键词列表

### ❌ 缺少镜头规格

```
Visual Description: A woman with silver hair stands on a platform...
```

**问题**: 缺少"Wide shot, high angle"等镜头信息

### ❌ Lighting & Mood 过长

```
Lighting & Mood: The lighting consists of harsh overhead fluorescent lights that
create a very flat and institutional type of illumination with a cool blue-white
color temperature, and the overall mood is one of isolation and contemplation,
with a strong contrast between her stillness and the chaos of the surrounding
commuters rushing past... (65词)
```

**问题**: 超过 50 词限制，应归入 Visual Description

---

## 质量自查清单

**每个 Beat 检查**:

- [ ] Visual Description: 80-120 词
- [ ] Lighting & Mood: 30-50 词
- [ ] 包含镜头类型和角度
- [ ] 角色描述与 Beat 1 一致
- [ ] 使用叙事描述式（非关键词）
- [ ] 场景包含 2-4 个独特特征
- [ ] 已指定光源、方向、色温
- [ ] 已描述情绪氛围

**整体检查**:

- [ ] 恰好 9 个 beats
- [ ] 标题行格式正确："EPISODE XX: BEAT BOARD VISUAL SCRIPT"
- [ ] 角色外观在所有 beats 中 100%一致
- [ ] 无 frontmatter 或元数据
- [ ] 无模板说明或注释

---

本指南专为 Nano Banner 3x3 网格生成优化。遵循这些规则可确保生成的 9 个 panels 具有视觉一致性和专业质量。
