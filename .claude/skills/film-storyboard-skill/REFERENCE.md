# Film Storyboard Skill - Platform & Style Reference

本文档包含平台特性、视觉风格库和技术参考。仅在需要时查阅。

---

## 平台支持

### Nano Banner（默认推荐）

**格式**: Episode Visual Script 模式

- 9 个 beats，每个 beat 包含 Visual Description + Lighting & Mood
- 优化用于 nano banner 3x3 网格生成
- 单次生成完整 9 宫格，保证一致性

**格式规范**:

```markdown
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT

Beat 1: [Beat 标题]
Visual Description: [镜头类型]. [角色规范描述] [动作/姿势] [场景细节] [关键视觉元素]. [80-120 词]
Lighting & Mood: [光影方向、质量、色温] [情绪氛围]. [30-50 词]

Beat 2: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...

[继续 Beat 3-9]
```

### Midjourney v6

**格式**: 独立 prompts + 参数

- 每个 beat 独立 prompt
- 包含`--ar 16:9 --style cinematic --v 6`参数
- 网格位置标注

**示例**:

```
Beat 1 (Grid Position: Top-Left):
[Prompt content]
--ar 16:9 --style cinematic --v 6
```

### Gemini Imagen 3 / DALL-E 3

**格式**: 标准叙事描述式 prompts

- 无特殊参数要求
- 依赖详细的叙事描述
- 每个 beat 80-150 词

---

## 视觉风格库

### 推荐风格组合

#### 写实风格

```
photorealistic, professional photography, cinematic lighting, high detail
```

**适用场景**: 现代剧情、纪录片风格、真人影片

#### 动漫风格

```
anime style, soft cel shading, vibrant colors, expressive characters
```

**适用场景**: 日式动画、漫画改编、青春题材

#### 概念艺术风格

```
digital concept art, painterly style, dramatic atmosphere, detailed environment
```

**适用场景**: 奇幻世界、科幻设定、游戏化叙事

#### 电影黑色风格

```
film noir aesthetic, high contrast black and white, dramatic shadows, moody atmosphere
```

**适用场景**: 悬疑、犯罪、复古侦探

#### 赛博朋克风格

```
cyberpunk aesthetic, neon lighting, rain-slicked streets, vibrant pink and cyan colors
```

**适用场景**: 未来都市、科技反乌托邦、夜间都市

#### 奇幻插画风格

```
fantasy illustration style, painterly, rich colors, epic composition
```

**适用场景**: 魔法世界、史诗冒险、童话改编

#### 水彩风格

```
watercolor painting style, soft edges, flowing colors, artistic paper texture
```

**适用场景**: 温馨故事、回忆场景、诗意叙事

---

## 光影方案候选

### 黄金时刻

```
warm golden hour sunlight, long soft shadows, orange and amber tones
```

**情绪**: 温暖、怀旧、希望

### 蓝色时刻

```
cool blue twilight, soft gradient from purple to dark blue, minimal shadows
```

**情绪**: 宁静、神秘、过渡

### 电影光影

```
cinematic lighting, dramatic contrast, three-point lighting setup
```

**情绪**: 戏剧性、专业、经典

### 自然柔光

```
soft diffused natural light, even illumination, gentle shadows
```

**情绪**: 平和、真实、日常

### 霓虹夜景

```
vibrant neon lighting in pink and cyan, colored reflections, high contrast
```

**情绪**: 未来感、都市感、活力

### 戏剧性侧光

```
dramatic side lighting, split lighting effect, deep shadows
```

**情绪**: 冲突、紧张、对立

---

## 宽高比选项

- **16:9** - 宽屏电影（推荐，主流视频平台）
- **1:1** - 方形（Instagram 帖子）
- **9:16** - 竖屏（TikTok, Reels, Stories）
- **4:3** - 传统电视
- **21:9** - 超宽电影（影院级体验）

---

## 与 Gemini 格式的区别

| 特性     | Nano Banner                               | Gemini/Midjourney |
| -------- | ----------------------------------------- | ----------------- |
| 结构     | Visual Description + Lighting & Mood 分离 | 单一 prompt 块    |
| 长度     | 80-120 词 + 30-50 词                      | 80-150 词总计     |
| 格式     | Episode Visual Script                     | 叙事描述式        |
| 输出     | 一次生成完整 3x3 网格                     | 逐个生成          |
| 一致性   | 系统保证同批次一致                        | 需手动管理种子    |
| 编辑能力 | 有限                                      | 可逐个调整        |

---

## 使用建议

### 选择平台

- **追求一致性** → Nano Banner
- **需要精细控制** → Midjourney v6
- **快速原型** → Gemini Imagen 3

### 选择风格

1. 根据故事类型选择基础风格
2. 考虑目标受众偏好
3. 保持全系列风格一致

### 选择光影

1. 根据情节情绪选择主导光影
2. 关键情节转折可切换光影方案
3. 保持同一场景的光影连贯性
